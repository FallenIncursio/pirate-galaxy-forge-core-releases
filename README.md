# Pirate Galaxy Forge Core

Inoffizieller 64-Bit-Communityclient für Pirate Galaxy.

**[Windows-Installer herunterladen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/download/v0.2.0-alpha.16/PirateGalaxyForgeCore-0.2.0-alpha.16-Setup.exe)** · **0.2.0-alpha.16** · [Releasehinweise und Prüfsummen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/tag/v0.2.0-alpha.16)

Core enthält die gemeinsame 64-Bit-Technik, allgemeine Korrekturen und begrenzten Komfort. Die ursprüngliche Hilfe bleibt erhalten. Zusätzliche Optionen stehen in der nativen Erweiterung der Spieleinstellungen.

[Core / Enhanced und 32-Bit-Vergleich](FEATURES.md) · [Änderungen dieser Ausgabe](0.2.0-alpha.16.md) · [Installation und Profilübernahme](INSTALLER-UPDATER.md) · [Cache-Upgrade und Startdiagnose](ALPHA16-CACHE-UPGRADE.md)

Core und Enhanced korrigieren die Übernahme alter und vom Spiel veränderter Ressourcencaches. Fehlgeschlagene Updates zeigen die installierte und die gewünschte Version; eine bekannte veraltete Spielbasis wird nicht mehr still gestartet. Diagnoseberichte erhalten den fehlgeschlagenen Schritt, sichere Fehlerstellen und die tatsächlich gestartete Version. Profile, Einstellungen und Anmeldedaten bleiben erhalten.

Enthalten sind modernisierte Bibliotheken, allgemeine Sicherheits- und Ressourcenverbesserungen, der D3D11-HUD-Texturfix, FPS/VSync, HUD-Größe, Chat-Uhrzeit, verschiebbare Komponenten, Ping/FPS unten rechts, Remnant-Filter, Sirius-Bauplanfarben und Kryonitmengen.

Orbitalwarnungen, Bossleisten und weitere Zusatzanzeigen gehören zu **[Forge Enhanced](https://github.com/FallenIncursio/pirate-galaxy-forge-releases)**. Beide Editionen teilen dieselbe Core-Implementierung.

Voraussetzungen: Windows 10/11 x64 und .NET Framework 4.8. Der Starter lädt die geprüfte Spielbasis und Java-Laufzeit bei Bedarf. Core nutzt einen eigenen Datenordner und übernimmt keine Enhanced-Profile automatisch.

Prüfungen und Sandbox-Ergebnisse stehen im [Release-Prüfstand](RELEASE-STATUS-0.2-alpha.16.md). Der reproduzierte Cachefehler ist behoben; die Behebung aller Ladehänger auf betroffenen Spielerrechnern ist damit nicht nachgewiesen. Kamerabhängige Helligkeit, native Sirius-Absturzursache, weitere GPUs, Wine/macOS und Langzeit-Gameplay bleiben offen.

Updates sind RSA-signiert; der Installer besitzt keine Windows-Authenticode-Signatur. Bibliotheksquellen und Lizenzhinweise gehören zu den Release-Downloads. Forge bleibt eine experimentelle Alpha ohne behauptete offizielle Splitscreen-Freigabe.
