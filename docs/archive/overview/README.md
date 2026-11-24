> Historischer Stand. Versionen, Freigaben und Tests gelten für den damaligen Zeitpunkt. [Aktuelle Übersicht](../../../README.md).

# Pirate Galaxy Forge Core

Inoffizieller 64-Bit-Communityclient für Pirate Galaxy.

**[Windows-Installer herunterladen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/download/v0.2.0-alpha.17/PirateGalaxyForgeCore-0.2.0-alpha.17-Setup.exe)** · **0.2.0-alpha.17** · [Releasehinweise und Prüfsummen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/tag/v0.2.0-alpha.17)

Core enthält die gemeinsame 64-Bit-Technik, allgemeine Korrekturen und begrenzten Komfort. Die ursprüngliche Hilfe bleibt erhalten. Zusätzliche Optionen stehen in der nativen Erweiterung der Spieleinstellungen.

[Core / Enhanced und 32-Bit-Vergleich](FEATURES.md) · [Änderungen dieser Ausgabe](../releases/0.2.0-alpha.17.md) · [Installation und Profilübernahme](INSTALLER-UPDATER.md) · [Zielanzeigen und Diagnose](../technical/ALPHA17-TARGET-UI-AUDIO.md)

Core und Enhanced korrigieren die Initialisierung von Schiffsnamen und Symbolen sowie unabhängige Lebens-/Schildbalken. Begrenzte UI- und Audio-Diagnose erleichtert die Fehlersuche, ohne automatische Berichte oder zusätzliche Spielserverabfragen.

Enthalten sind modernisierte Bibliotheken, allgemeine Sicherheits- und Ressourcenverbesserungen, der D3D11-HUD-Texturfix, FPS/VSync, HUD-Größe, Chat-Uhrzeit, verschiebbare Komponenten, Ping/FPS unten rechts, Remnant-Filter, Sirius-Bauplanfarben und Kryonitmengen.

Orbitalwarnungen, Bossleisten und weitere Zusatzanzeigen gehören zu **[Forge Enhanced](https://github.com/FallenIncursio/pirate-galaxy-forge-releases)**. Beide Editionen teilen dieselbe Core-Implementierung.

Voraussetzungen: Windows 10/11 x64 und .NET Framework 4.8. Der Starter lädt die geprüfte Spielbasis und Java-Laufzeit bei Bedarf. Core nutzt einen eigenen Datenordner und übernimmt keine Enhanced-Profile automatisch.

Build-, Installations- und Sandbox-Prüfungen stehen im [Release-Prüfstand](../verification/RELEASE-STATUS-0.2-alpha.17.md). Vollständige OTB-Matchabläufe, weitere GPUs, Wine/macOS und Langzeittests sind separat zu prüfen. Kamerabhängige Helligkeit, die native Sirius-Absturzursache und ein reproduzierter D3D11-Materialfehler bleiben offen.

Updates sind RSA-signiert; der Installer besitzt keine Windows-Authenticode-Signatur. Bibliotheksquellen und Lizenzhinweise gehören zu den Release-Downloads. Forge bleibt eine experimentelle Alpha ohne behauptete offizielle Splitscreen-Freigabe.
