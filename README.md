# Pirate Galaxy Forge Core

Inoffizieller 64-Bit-Communityclient für Pirate Galaxy.

**[Windows-Installer herunterladen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/download/v0.2.0-alpha.3/PirateGalaxyForgeCore-0.2.0-alpha.3-Setup.exe)** · **0.2.0-alpha.3** · [Releasehinweise und Prüfsummen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/tag/v0.2.0-alpha.3)

Core enthält die gemeinsame 64-Bit-Technik, allgemeine Korrekturen und begrenzten Komfort. Die ursprüngliche Hilfe bleibt erhalten. Zusätzliche Optionen stehen in der nativen Erweiterung der Spieleinstellungen.

[Core / Enhanced und 32-Bit-Vergleich](FEATURES.md) · [Änderungen dieser Ausgabe](0.2.0-alpha.3.md) · [Installation und Profilübernahme](INSTALLER-UPDATER.md)

Diese Ausgabe verbessert Fehlerberichte und Grafikstart, ergänzt eine Reparaturfunktion mit Profilerhalt und vereinfacht die Installation. Neue Installationen verwenden „Automatisch“: D3D11 wird geprüft, bei fehlender Unterstützung oder einem erkannten Startfehler ist D3D9 verfügbar. Vorhandene manuelle Einstellungen bleiben erhalten. Die bisherigen Calon-, Materialbereinigungs- und Erebos-Korrekturen bleiben enthalten.

Enthalten sind modernisierte Bibliotheken, allgemeine Sicherheits- und Ressourcenverbesserungen, der D3D11-HUD-Texturfix, FPS/VSync, HUD-Größe, Chat-Uhrzeit, verschiebbare Komponenten, Ping/FPS unten rechts, Remnant-Filter, Sirius-Bauplanfarben und Kryonitmengen.

Orbitalwarnungen, Bossleisten und weitere Zusatzanzeigen gehören zu **[Forge Enhanced](https://github.com/FallenIncursio/pirate-galaxy-forge-releases)**. Beide Editionen teilen dieselbe Core-Implementierung.

Voraussetzungen: Windows 10/11 x64 und .NET Framework 4.8. Der Starter lädt die geprüfte Spielbasis und Java-Laufzeit bei Bedarf. Core nutzt einen eigenen Datenordner und übernimmt keine Enhanced-Profile automatisch.

Installer, Upgrades ab Alpha 73 und alpha.2, Reparatur, Profilübernahme, Abbruch und Rollback sind für die exakten Paketbytes geprüft. Enhanced wurde mit D3D11 in der Sandbox bis zur verbundenen Spielsitzung gestartet und vom Nutzer bestätigt. Core-Ingame-Abnahme dieser Ausgabe, längere Spielsitzungen, weitere GPU-/Treiberkombinationen und Wine bleiben offen. 240 FPS ist eine Obergrenze, keine Leistungszusage.

Updates sind RSA-signiert; der Installer besitzt keine Windows-Authenticode-Signatur. Bibliotheksquellen und Lizenzhinweise gehören zu den Release-Downloads. Forge bleibt eine experimentelle Alpha ohne behauptete offizielle Splitscreen-Freigabe.
