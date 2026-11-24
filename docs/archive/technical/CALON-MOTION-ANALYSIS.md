> Historischer Stand. Versionen, Freigaben und Tests gelten für den damaligen Zeitpunkt. [Aktuelle Übersicht](../../../README.md).

# Calon: kurze Bewegungsruckler, Analyse vom 17.11.2026

Auftrag: kurze Aufnahme, Codeanalyse und Fixvorschlag. Keine Implementierung,
kein Neustart, Commit, Push oder Releasewechsel. Quellbasis
`381afd529be5e61a42f618603648c892e785a606`.

## Beobachtung und Messung

Laufender Enhanced-OTB-Sandboxstand mit D3D11; Spiel-JAR bytegleich zum
veröffentlichten Enhanced alpha.8. 240-FPS-Limit, VSync ausgeschaltet,
3440×1440. Der Nutzer bestätigt zur aufgenommenen Flugbewegung auf Calon:
„Ja, wie sonst auch“. Die Bildfolge zeigt Flug und Kamerabewegung über Wasser
und Land mit sichtbaren Schiffen, Effekten und KW-Widget.

25 Sekunden Video ohne Audio, parallel 47 Sekunden PresentMon. Zusätzlich
zwei Messungen ohne Video. Das Video hat 1.246 Bilder, durchschnittlich 49,84
Bilder/s trotz angeforderter 60; der Recorder meldet 158 verworfene Bilder.
Es dient zur Szenen-/Symptombestätigung, nicht als exakte Framezeitmessung.
Die Aufnahme erhöht die Last deutlich; ihr mittlerer Wert ist keine
unverfälschte Spielleistung.

| Ausschnitt | Dauer | Ø FPS | P99 Framezeit | Längster Frame | Frames >16,67 ms |
| --- | ---: | ---: | ---: | ---: | ---: |
| Vor dem Video, Sekunden 1–9 | 8 s | 227,6 | 9,00 ms | 34,42 ms | 9 |
| Video, Sekunden 12–34 | 22 s | 169,0 | 15,64 ms | 57,85 ms | 36 |
| Nach dem Video, Sekunden 37–46 | 9 s | 223,7 | 8,57 ms | 54,69 ms | 8 |
| Spätere Kontrolle ohne Video, Sekunden 15–39 | 24 s | 235,5 | 7,14 ms | 39,57 ms | 11 |

Im letzten Ausschnitt liegt die GPU-Arbeitszeit im Mittel bei 1,55 ms,
P99 bei 2,15 ms. Das spricht gegen durchgehende GPU-Sättigung als Erklärung.
Lange Frameabstände sind auch außerhalb der Aufnahme belegt. PresentMons
`CPUBusy` bedeutet hier Zeit außerhalb des Present-Aufrufs; es beweist weder
aktive CPU-Auslastung noch die verursachende Java-/native Methode.

Alle 9.188 Presents der ersten Messung laufen über
`Composed: Copy with GPU GDI`, SyncInterval 0. Typische Anzeigedauer 6,06 ms
entspricht etwa 165 Hz; längere Anzeigedauern treten ebenfalls auf. Die
Kombination mit 240-Hz-Erzeugung ist ein plausibler zusätzlicher Beitrag zu
ungleichmäßiger Bewegung. Sie ist ohne A/B-Test keine allein bewiesene Ursache.

Die externe JFR-Aktivierung schlug fehl; der gestartete Client setzt
`-XX:+DisableAttachMechanism`. Die Schutzkonfiguration blieb unverändert.
Auch der passive jstat-Zugriff auf Sandbox-PerfData war nicht verfügbar.
Es liegen somit keine JFR-, GC- oder Java-Stackdaten aus diesen Versuchen vor.
Die spätere 24-Sekunden-Kontrolle schließt die Anlaufphase dieser Hilfsprozesse aus.
Kein Paketmitschnitt, kein Heapdump, keine zusätzlichen Spielserverabfragen.

## Konkrete Codebefunde

### D3D11-Bildausgabe

Gepinnter OGRE-14.6.3-Quellstand, `OgreD3D11RenderWindow.cpp`:

- `mUseFlipMode` startet mit `false` (Zeile 372); die HWND-Erstellung liest
  optional `useFlipMode` (um 682). Der tatsächlich gemessene Pfad ist Copy/Blt.
- Ohne Flip: ein Swapchain-Puffer, `DXGI_SWAP_EFFECT_DISCARD` (889–893).
- `swapBuffers()` verwendet bei Flip aktuell `max(1, mVSyncInterval)`
  unabhängig von `mVSync` (562). Nur Flip einzuschalten würde daher die
  VSync-aus-Auswahl nicht korrekt beibehalten.
- Mehrfachabtastung wird beim Flip-Pfad bereits über einen separaten
  Renderpuffer und `ResolveSubresource` behandelt (421 ff., 542 ff.).
  Die existierenden Kantenglättungs- und Gammafälle müssen erhalten bleiben.

Ein gemeinsamer neuer OGRE-Patch gehört zur vorhandenen gepinnten Patchkette
unter `project/client-runtime-modernization/ogre14`, nicht als manuelle Änderung
einer generierten `.build`-Quelle in den Releaseprozess.

### Frameuhr und Bewegung

`project/client-quality/src/pg64/client/FrameClock.java:24` wartet ausschließlich
mit `LockSupport.parkNanos` bis zur absoluten Frist. Die tatsächlich verstrichene
Zeit wird anschließend an die unveränderten Spiel-Updates übergeben.
`QualityPatcher.java:149` setzt daraus `nf.SJ` und `nf.SI`. Größere lokale Pausen
können daher sichtbare größere Bewegungsschritte ergeben. Eine Rückkehr zu
pauschal geglätteter Spielzeit wäre ohne Prüfung von Weg, Kamera und Serverzeit
kein belastbarer Fix.

Die bisherigen Uhrtests prüfen feste Raten, einen einzelnen 60-Hz-Jitterfall
und eine Gesamtzeitgrenze. Sie prüfen keinen vollständigen eigenen Schiffsflug
mit den jetzt gemessenen wechselnden Framezeiten. Der frühere
`awu`-/`retainedHalf`-Fix betrifft Clanbojen, nicht die eigene Schiffsbewegung.

### Terrainarbeit im Renderthread

`native-terrain/src/src/OgrePagingLandScapePageManager.cpp:163` arbeitet am
Frameende Lade- und Entladequeues ab. `processLoadQueues()` ab Zeile 626
steuert dies über Framezähler und ruft `load`, `loadTexture` oder `preload`
synchron auf; es iteriert dabei über Kameras. Der Default `PageLoadInterval`
ist 30 Frames, kann aber durch Terrainoptionen ersetzt werden. Es gibt an
dieser Stelle kein gemessenes Zeitbudget. Das ist ein Prüfpunkt für hohe
Bildraten und Planetenwechsel, noch kein Nachweis für die beobachteten Peaks.

### Grenzen der bestehenden Diagnose

`ForgeDiagnostics.java` erfasst alle 200 ms bereits aggregierte Werte;
`ComfortMetrics` berechnet Statistiken im Sekundenrhythmus über zehn Sekunden.
Das zählt lange Frames, ordnet sie aber keiner konkreten Arbeit zu. Der
Aussetzerzähler betrachtet zudem erst >50 ms, obwohl viele bestätigte Ruckler
darunter liegen. Die aktuelle G1-Konfiguration hat ein **weiches** 20-ms-Ziel;
ohne GC-Ereignisse ist eine GC-Ursache weder bestätigt noch ausgeschlossen.

## Empfohlene Umsetzung

1. **Kurze interne Rucklerdiagnose ergänzen.** Begrenzter Ringpuffer mit
   monotonen Frame-/Phasenzeitpunkten für Limiter, Spielupdate, Terrain,
   HUD und Render/Present. GC-/Safepoint-Daten über eine explizit gestartete,
   begrenzte JFR-Aufnahme innerhalb der JVM; Attach-Schutz bleibt aktiv.
   Export asynchron, keine Profil-/Chat-/Anmeldedaten. Zähler relativ zum
   Bildbudget sowie bei 16,7/33/50 ms, Messaufwand selbst ausweisen.

2. **D3D11-Flip-Pfad als getrennten Core-Testkandidaten erproben.** Zwei Puffer,
   korrekte VSync-aus-Semantik, Tearing nur nach Featureprüfung und mit
   konsistenten Create-/Resize-/Present-Flags. Begrenzte Warteschlange bzw.
   frame-latency waitable object prüfen; nicht zusätzlich doppelt warten.
   AA/Resolve, Gamma, Fensterwechsel, Alt-Tab, Resize, Device-Loss, MyGUI und
   vorhandene Fensterintegration prüfen. Unterstützungsprüfung und getesteten
   bisherigen Fallback erhalten. Kein automatisches Umschreiben des FPS-Wunschs.

3. **Lange Frames anhand der Phasen korrigieren.** Bei belegter Terrainarbeit
   Vorbereitung/Decodierung auslagern und Upload/Integration in kleine Schritte
   zerlegen; OGRE-Objekte bleiben im vorgesehenen Thread. Ein Budgetcheck vor
   einem weiterhin 30-ms-langen Einzelaufruf reicht nicht. Bei belegten
   GC-Pausen die gemessenen Allokationsstellen reduzieren. Nur bei belegtem
   Aufwachjitter einen begrenzten präziseren Warteabschluss prüfen, mit
   gemessenen CPU-Kosten. Keine pauschale Collector-, Textur- oder
   Bewegungsänderung ohne Ursachenbeleg.

Vergleich auf derselben Route: 60/165/240 FPS, VSync an/aus, alter/neuer
Present-Pfad sowie D3D9 und Original32 als gesonderte Referenzläufe. Eigene
Schiffsposition, Kamera und Framezeiten getrennt prüfen. Die neuen Tests sollen
die aufgezeichneten variablen Zeitfolgen abspielen und gleiches Weg-/Zeitverhalten
prüfen. Auf Calon, einem Planeten ohne vergleichbare Wasserflächen und nach
mehreren Orbitwechseln abnehmen. Gleiche Qualitäts-/AA-Einstellungen beibehalten.

Die allgemeinen Korrekturen gehören in Core und werden von Enhanced übernommen.
Enhanced-Overlays nur dann gezielt ändern, wenn die Phasenmessung sie belastet.
Die bisherige Aufnahme belegt keinen OTB-Widget-, Netzwerk- oder Wassertexturfehler.

## Nachweise und Quellen

Sanitisierter lokaler Messbeleg: `distribution/tests/calon-motion-analysis.json`.
Video, Screenshots, CSV-Dateien und Rohlogs verbleiben ausschließlich im privaten
Chat-Arbeitsordner `work/calon-motion-analysis`; nicht committen oder hochladen.

- [PresentMon: Definitionen der Messwerte und Present-Modi](https://github.com/GameTechDev/PresentMon/blob/main/README-ConsoleApplication.md)
- [Microsoft: DXGI Flip Model, Voraussetzungen und Kompatibilität](https://learn.microsoft.com/en-us/windows/win32/direct3ddxgi/for-best-performance--use-dxgi-flip-model)

Der Aufnahmeauftrag ist erfüllt. Die vorgeschlagene Umsetzung und ihre
Ingame-/Referenztests sind noch nicht durchgeführt; nichts veröffentlicht.
