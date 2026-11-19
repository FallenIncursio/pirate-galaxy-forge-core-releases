# Pirate Galaxy Forge Core

Inoffizieller 64-Bit-Communityclient für Pirate Galaxy.

**[Windows-Installer herunterladen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/download/v0.2.0-alpha.11/PirateGalaxyForgeCore-0.2.0-alpha.11-Setup.exe)** · **0.2.0-alpha.11** · [Releasehinweise und Prüfsummen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/tag/v0.2.0-alpha.11)

Core enthält die gemeinsame 64-Bit-Technik, allgemeine Korrekturen und begrenzten Komfort. Die ursprüngliche Hilfe bleibt erhalten. Zusätzliche Optionen stehen in der nativen Erweiterung der Spieleinstellungen.

[Core / Enhanced und 32-Bit-Vergleich](FEATURES.md) · [Änderungen dieser Ausgabe](0.2.0-alpha.11.md) · [Installation und Profilübernahme](INSTALLER-UPDATER.md) · [Spielversion 1002133](GAME-BASIS-1002133.md) · [Normalenvergleich und Diagnose](ALPHA11-TERRAIN-NORMALS.md)

Core und Enhanced verwenden jetzt die offizielle Spielversion 1002133 mit aktualisierten Schiffsinformationen und Ressourcen. Die alpha.11-Normalenberechnung nach dem 32-Bit-Original, die begrenzte Grafikdiagnose und alle bisherigen Forge-Korrekturen bleiben enthalten. Profile und Einstellungen bleiben bei Updates erhalten.

Enthalten sind modernisierte Bibliotheken, allgemeine Sicherheits- und Ressourcenverbesserungen, der D3D11-HUD-Texturfix, FPS/VSync, HUD-Größe, Chat-Uhrzeit, verschiebbare Komponenten, Ping/FPS unten rechts, Remnant-Filter, Sirius-Bauplanfarben und Kryonitmengen.

Orbitalwarnungen, Bossleisten und weitere Zusatzanzeigen gehören zu **[Forge Enhanced](https://github.com/FallenIncursio/pirate-galaxy-forge-releases)**. Beide Editionen teilen dieselbe Core-Implementierung.

Voraussetzungen: Windows 10/11 x64 und .NET Framework 4.8. Der Starter lädt die geprüfte Spielbasis und Java-Laufzeit bei Bedarf. Core nutzt einen eigenen Datenordner und übernimmt keine Enhanced-Profile automatisch.

Bekanntes Problem: Starke kamerabhängige Helligkeitswechsel sind weiterhin gemeldet und mit diesem Release nicht abschließend behoben. Die weitere Untersuchung folgt separat. Beide Editionen bestanden 52 Editionssuiten und native D3D9-/D3D11-Prüfungen; Enhanced wurde mit D3D11 auf Spielversion 1002133 angemeldet bis in den Orbit getestet. Eine gesonderte Core-Spielsitzung, weitere GPUs, Wine und Langzeittests bleiben offen. [Prüfstand](RELEASE-STATUS-0.2-alpha.11.md).

Updates sind RSA-signiert; der Installer besitzt keine Windows-Authenticode-Signatur. Bibliotheksquellen und Lizenzhinweise gehören zu den Release-Downloads. Forge bleibt eine experimentelle Alpha ohne behauptete offizielle Splitscreen-Freigabe.
