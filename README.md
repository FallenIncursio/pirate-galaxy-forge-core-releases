# Pirate Galaxy Forge Core

Inoffizieller 64-Bit-Communityclient für Pirate Galaxy.

**[Windows-Installer herunterladen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/download/v0.2.0-alpha.12/PirateGalaxyForgeCore-0.2.0-alpha.12-Setup.exe)** · **0.2.0-alpha.12** · [Releasehinweise und Prüfsummen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/tag/v0.2.0-alpha.12)

Core enthält die gemeinsame 64-Bit-Technik, allgemeine Korrekturen und begrenzten Komfort. Die ursprüngliche Hilfe bleibt erhalten. Zusätzliche Optionen stehen in der nativen Erweiterung der Spieleinstellungen.

[Core / Enhanced und 32-Bit-Vergleich](FEATURES.md) · [Änderungen dieser Ausgabe](0.2.0-alpha.12.md) · [Installation und Profilübernahme](INSTALLER-UPDATER.md) · [Fokusfix und Testfehler](ALPHA12-WINDOW-FOCUS.md)

Gewöhnliche Spielfenster und Buttons blockieren Komponententasten nach dem Anklicken nicht mehr. Der gemeinsame Fokusfix entspricht dem geprüften 32-Bit-Verhalten und gilt für Core und Enhanced mit D3D9 und D3D11. Chat, Suchfelder und modale Dialoge behalten ihren Eingabeschutz. Spielversion 1002133, bisherige Forge-Fixes, Profile und Einstellungen bleiben erhalten.

Enthalten sind modernisierte Bibliotheken, allgemeine Sicherheits- und Ressourcenverbesserungen, der D3D11-HUD-Texturfix, FPS/VSync, HUD-Größe, Chat-Uhrzeit, verschiebbare Komponenten, Ping/FPS unten rechts, Remnant-Filter, Sirius-Bauplanfarben und Kryonitmengen.

Orbitalwarnungen, Bossleisten und weitere Zusatzanzeigen gehören zu **[Forge Enhanced](https://github.com/FallenIncursio/pirate-galaxy-forge-releases)**. Beide Editionen teilen dieselbe Core-Implementierung.

Voraussetzungen: Windows 10/11 x64 und .NET Framework 4.8. Der Starter lädt die geprüfte Spielbasis und Java-Laufzeit bei Bedarf. Core nutzt einen eigenen Datenordner und übernimmt keine Enhanced-Profile automatisch.

56 Editionssuiten und sechs Build-Negativkontrollen bestanden. Vier native Fokusproben prüfen je 2.253 Fälle; beide bisherigen Renderer-DLLs scheitern als Negativkontrolle gezielt am alten Fensterstandard. Der Nutzer bestätigt den Fokusfix in Enhanced/D3D11. Die Sitzungslogs zeigen keine neue Exception oder Absturzspur; bekannte Tracking-, UI- und Szenenmeldungen bleiben dokumentiert. Kamerabhängige Helligkeitswechsel bleiben offen, ebenso eine gesonderte Core-Spielsitzung, andere GPUs, Wine und Langzeittests. [Prüfstand](RELEASE-STATUS-0.2-alpha.12.md).

Updates sind RSA-signiert; der Installer besitzt keine Windows-Authenticode-Signatur. Bibliotheksquellen und Lizenzhinweise gehören zu den Release-Downloads. Forge bleibt eine experimentelle Alpha ohne behauptete offizielle Splitscreen-Freigabe.
