# Pirate Galaxy Forge Core

Inoffizieller 64-Bit-Communityclient für Pirate Galaxy.

**[Windows-Installer herunterladen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/download/v0.2.0-alpha.5/PirateGalaxyForgeCore-0.2.0-alpha.5-Setup.exe)** · **0.2.0-alpha.5** · [Releasehinweise und Prüfsummen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/tag/v0.2.0-alpha.5)

Core enthält die gemeinsame 64-Bit-Technik, allgemeine Korrekturen und begrenzten Komfort. Die ursprüngliche Hilfe bleibt erhalten. Zusätzliche Optionen stehen in der nativen Erweiterung der Spieleinstellungen.

[Core / Enhanced und 32-Bit-Vergleich](FEATURES.md) · [Änderungen dieser Ausgabe](0.2.0-alpha.5.md) · [Installation und Profilübernahme](INSTALLER-UPDATER.md) · [Terrain-Fix und 32-Bit-Vergleich](ALPHA5-TERRAIN-LIGHTING.md)

Diese Ausgabe korrigiert kamerabhängige Bodenhelligkeit unter D3D11: spätere planetenspezifische Texturzuweisungen, Terrain-Material-LOD und die ursprüngliche COLOR-Semantik älterer Shader. Auf Molikar wird wieder die originale Reflexionstextur verwendet. Core und Enhanced enthalten denselben Fix. Alle bisherigen Korrekturen bleiben enthalten; Einstellungen und Profile werden erhalten.

Enthalten sind modernisierte Bibliotheken, allgemeine Sicherheits- und Ressourcenverbesserungen, der D3D11-HUD-Texturfix, FPS/VSync, HUD-Größe, Chat-Uhrzeit, verschiebbare Komponenten, Ping/FPS unten rechts, Remnant-Filter, Sirius-Bauplanfarben und Kryonitmengen.

Orbitalwarnungen, Bossleisten und weitere Zusatzanzeigen gehören zu **[Forge Enhanced](https://github.com/FallenIncursio/pirate-galaxy-forge-releases)**. Beide Editionen teilen dieselbe Core-Implementierung.

Voraussetzungen: Windows 10/11 x64 und .NET Framework 4.8. Der Starter lädt die geprüfte Spielbasis und Java-Laufzeit bei Bedarf. Core nutzt einen eigenen Datenordner und übernimmt keine Enhanced-Profile automatisch.

72 kontrollierte Molikar-Ansichten wurden mit dem originalen 32-Bit-Client verglichen; alle 34 Texturbelegungen stimmen überein. Enhanced wurde mit D3D11 in der Sandbox verbunden gestartet und der Molikar-Test vom Nutzer bestätigt. Die automatische Prüfung und ihre Grenzen stehen im [Release-Prüfstand](RELEASE-STATUS-0.2-alpha.5.md). Eine gesonderte Core-Spielsitzung, alle Planeten, weitere GPUs/Treiber, Wine und Langzeitmessungen bleiben offen. Keine vollständige Bildgleichheit oder pauschale Leistungszusage.

Updates sind RSA-signiert; der Installer besitzt keine Windows-Authenticode-Signatur. Bibliotheksquellen und Lizenzhinweise gehören zu den Release-Downloads. Forge bleibt eine experimentelle Alpha ohne behauptete offizielle Splitscreen-Freigabe.
