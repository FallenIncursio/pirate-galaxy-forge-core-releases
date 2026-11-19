# Pirate Galaxy Forge Core

Inoffizieller 64-Bit-Communityclient für Pirate Galaxy.

**[Windows-Installer herunterladen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/download/v0.2.0-alpha.13/PirateGalaxyForgeCore-0.2.0-alpha.13-Setup.exe)** · **0.2.0-alpha.13** · [Releasehinweise und Prüfsummen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/tag/v0.2.0-alpha.13)

Core enthält die gemeinsame 64-Bit-Technik, allgemeine Korrekturen und begrenzten Komfort. Die ursprüngliche Hilfe bleibt erhalten. Zusätzliche Optionen stehen in der nativen Erweiterung der Spieleinstellungen.

[Core / Enhanced und 32-Bit-Vergleich](FEATURES.md) · [Änderungen dieser Ausgabe](0.2.0-alpha.13.md) · [Installation und Profilübernahme](INSTALLER-UPDATER.md) · [Ressourcen, Diagnose und Updates](ALPHA13-RELIABILITY-UPDATES.md)

Core und Enhanced sichern Ressourcenanfragen bei fehlendem Dienst, Verbindungswechsel und Abbruch ab. Die Absturzdiagnose trennt Java-Ereignisse und ergänzt vorhandene native Fehlerdaten. Komprimierte Updatepakete sind rund 63 % kleiner als in alpha.12; sichere Downloadfortsetzung, geprüfte Laufzeit- und Cacheübernahme sowie ein verschiebbares Update mit Fortschrittsanzeige verbessern die Einrichtung. Spielversion 1002133, bisherige Fixes, Profile und Einstellungen bleiben erhalten.

Enthalten sind modernisierte Bibliotheken, allgemeine Sicherheits- und Ressourcenverbesserungen, der D3D11-HUD-Texturfix, FPS/VSync, HUD-Größe, Chat-Uhrzeit, verschiebbare Komponenten, Ping/FPS unten rechts, Remnant-Filter, Sirius-Bauplanfarben und Kryonitmengen.

Orbitalwarnungen, Bossleisten und weitere Zusatzanzeigen gehören zu **[Forge Enhanced](https://github.com/FallenIncursio/pirate-galaxy-forge-releases)**. Beide Editionen teilen dieselbe Core-Implementierung.

Voraussetzungen: Windows 10/11 x64 und .NET Framework 4.8. Der Starter lädt die geprüfte Spielbasis und Java-Laufzeit bei Bedarf. Core nutzt einen eigenen Datenordner und übernimmt keine Enhanced-Profile automatisch.

58 Editionssuiten, sechs Build-Negativkontrollen sowie Diagnose-, Transport-, Installer-, Reparatur- und Profilübernahmeprüfungen bestanden. Der Nutzer bestätigt bisher störungsfreien Betrieb von Enhanced mit D3D11 in der Sandbox. Der konkrete native Sirius-Landeabsturz ist weiterhin nicht nachweislich behoben; die Ressourcenhärtung ist keine Zusage von Absturzfreiheit. Kamerabhängige Helligkeit, eine separate Core-Spielsitzung, andere GPUs, Wine und Langzeittests bleiben offen. Weniger Paketvolumen bedeutet keine entsprechend kürzere gesamte Installation. [Prüfstand](RELEASE-STATUS-0.2-alpha.13.md).

Updates sind RSA-signiert; der Installer besitzt keine Windows-Authenticode-Signatur. Bibliotheksquellen und Lizenzhinweise gehören zu den Release-Downloads. Forge bleibt eine experimentelle Alpha ohne behauptete offizielle Splitscreen-Freigabe.
