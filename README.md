# Pirate Galaxy Forge Core

Inoffizieller 64-Bit-Communityclient für Pirate Galaxy.

**[Windows-Installer herunterladen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/download/v0.2.0-alpha.6/PirateGalaxyForgeCore-0.2.0-alpha.6-Setup.exe)** · **0.2.0-alpha.6** · [Releasehinweise und Prüfsummen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/tag/v0.2.0-alpha.6)

Core enthält die gemeinsame 64-Bit-Technik, allgemeine Korrekturen und begrenzten Komfort. Die ursprüngliche Hilfe bleibt erhalten. Zusätzliche Optionen stehen in der nativen Erweiterung der Spieleinstellungen.

[Core / Enhanced und 32-Bit-Vergleich](FEATURES.md) · [Änderungen dieser Ausgabe](0.2.0-alpha.6.md) · [Installation und Profilübernahme](INSTALLER-UPDATER.md) · [Material- und Remnant-Fixes](ALPHA6-REMNANT-MATERIALS.md) · [Bekannter Absturz](ALPHA6-CRASH-MATERIAL-CLEANUP.md)

Diese Ausgabe korrigiert verspätet geladene und erneut erzeugte Partikelmaterialien unter D3D11, darunter Aggrobeacon, sowie die Materialübernahme geklonter Schiffe. Enhanced beschränkt Remnant-Auftritte auf XC/SC; MN/DL behalten ihre Bossleisten und Effektanzeigen. Einstellungen und Profile werden erhalten.

Enthalten sind modernisierte Bibliotheken, allgemeine Sicherheits- und Ressourcenverbesserungen, der D3D11-HUD-Texturfix, FPS/VSync, HUD-Größe, Chat-Uhrzeit, verschiebbare Komponenten, Ping/FPS unten rechts, Remnant-Filter, Sirius-Bauplanfarben und Kryonitmengen.

Orbitalwarnungen, Bossleisten und weitere Zusatzanzeigen gehören zu **[Forge Enhanced](https://github.com/FallenIncursio/pirate-galaxy-forge-releases)**. Beide Editionen teilen dieselbe Core-Implementierung.

Voraussetzungen: Windows 10/11 x64 und .NET Framework 4.8. Der Starter lädt die geprüfte Spielbasis und Java-Laufzeit bei Bedarf. Core nutzt einen eigenen Datenordner und übernimmt keine Enhanced-Profile automatisch.

Bekannter Fehler: In einer Enhanced-D3D11-Sitzung trat ein nativer Absturz bei der Material-/Shader-Bereinigung auf. Dieser Absturz ist in alpha.6 noch nicht behoben; derselbe native Code wird auch von Core verwendet. Die Veröffentlichung dieser Alpha mit dem bekannten Fehler wurde ausdrücklich beauftragt. Prüfungen und weitere Grenzen stehen im [Release-Prüfstand](RELEASE-STATUS-0.2-alpha.6.md).

Updates sind RSA-signiert; der Installer besitzt keine Windows-Authenticode-Signatur. Bibliotheksquellen und Lizenzhinweise gehören zu den Release-Downloads. Forge bleibt eine experimentelle Alpha ohne behauptete offizielle Splitscreen-Freigabe.
