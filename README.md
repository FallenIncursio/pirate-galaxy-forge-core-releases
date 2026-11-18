# Pirate Galaxy Forge Core

Inoffizieller 64-Bit-Communityclient für Pirate Galaxy.

**[Windows-Installer herunterladen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/download/v0.2.0-alpha.9/PirateGalaxyForgeCore-0.2.0-alpha.9-Setup.exe)** · **0.2.0-alpha.9** · [Releasehinweise und Prüfsummen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/tag/v0.2.0-alpha.9)

Core enthält die gemeinsame 64-Bit-Technik, allgemeine Korrekturen und begrenzten Komfort. Die ursprüngliche Hilfe bleibt erhalten. Zusätzliche Optionen stehen in der nativen Erweiterung der Spieleinstellungen.

[Core / Enhanced und 32-Bit-Vergleich](FEATURES.md) · [Änderungen dieser Ausgabe](0.2.0-alpha.9.md) · [Installation und Profilübernahme](INSTALLER-UPDATER.md) · [Calon-Messung und verbleibende Spitzen](ALPHA9-ATLAS-LOD-LIVE-ANALYSIS.md)

Diese Ausgabe verringert wiederholte Schrift-, Layout- und Vegetationsarbeit auf Calon: begrenzte Schriftatlanten, vorbereitete manuelle LODs, gestufter Seitenaufbau und weniger D3D11-Readbacks. ZGC, wiederverwendete Werte, zeitliche Wasserupdates, AWT-kompatibler Grafikstart und eine freiwillige lokale 30-Sekunden-Rucklerdiagnose ergänzen die gemeinsamen Verbesserungen. Sichtweite, Pflanzenzahl, Einstellungen und Profile bleiben erhalten.

Enthalten sind modernisierte Bibliotheken, allgemeine Sicherheits- und Ressourcenverbesserungen, der D3D11-HUD-Texturfix, FPS/VSync, HUD-Größe, Chat-Uhrzeit, verschiebbare Komponenten, Ping/FPS unten rechts, Remnant-Filter, Sirius-Bauplanfarben und Kryonitmengen.

Orbitalwarnungen, Bossleisten und weitere Zusatzanzeigen gehören zu **[Forge Enhanced](https://github.com/FallenIncursio/pirate-galaxy-forge-releases)**. Beide Editionen teilen dieselbe Core-Implementierung.

Voraussetzungen: Windows 10/11 x64 und .NET Framework 4.8. Der Starter lädt die geprüfte Spielbasis und Java-Laufzeit bei Bedarf. Core nutzt einen eigenen Datenordner und übernimmt keine Enhanced-Profile automatisch.

Im Enhanced-Calon-Test sank die gemessene Vegetationsspitze von 15,15 auf 2,92 ms und der Zielanzeigenaufbau von 24,26 auf 1,02 ms; unvorbereitete LOD-Lesezugriffe entfielen. Die Strecken waren nicht kontrolliert identisch. Acht Frameabstände über 16,67 ms und ein Maximum von 49,36 ms bleiben bekannt; Timer-/JNI- und Renderausreißer werden weiter untersucht. Der Nutzer hat die Verbesserung für dieses Update akzeptiert. Keine vollständige Rucklerfreiheit, pauschale FPS-Zusage oder neue Original32-Flugvergleichsmessung. Core-Liveprüfung, weitere GPUs, Wine und Langzeittests bleiben gesondert. [Prüfstand](RELEASE-STATUS-0.2-alpha.9.md).

Updates sind RSA-signiert; der Installer besitzt keine Windows-Authenticode-Signatur. Bibliotheksquellen und Lizenzhinweise gehören zu den Release-Downloads. Forge bleibt eine experimentelle Alpha ohne behauptete offizielle Splitscreen-Freigabe.
