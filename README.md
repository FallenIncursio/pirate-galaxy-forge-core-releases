# Pirate Galaxy Forge Core

Inoffizieller 64-Bit-Communityclient für Pirate Galaxy.

**[Windows-Installer herunterladen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/download/v0.2.0-alpha.14/PirateGalaxyForgeCore-0.2.0-alpha.14-Setup.exe)** · **0.2.0-alpha.14** · [Releasehinweise und Prüfsummen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/tag/v0.2.0-alpha.14)

Core enthält die gemeinsame 64-Bit-Technik, allgemeine Korrekturen und begrenzten Komfort. Die ursprüngliche Hilfe bleibt erhalten. Zusätzliche Optionen stehen in der nativen Erweiterung der Spieleinstellungen.

[Core / Enhanced und 32-Bit-Vergleich](FEATURES.md) · [Änderungen dieser Ausgabe](0.2.0-alpha.14.md) · [Installation und Profilübernahme](INSTALLER-UPDATER.md) · [Ladebildschirm und Wiederherstellung](ALPHA14-STARTUP-RECOVERY.md)

Core und Enhanced begrenzen Ressourcen-Downloads und abhängige Warteaufträge. Fehler optionaler lokaler Anmeldedateien verhindern die Anmeldemaske nicht mehr. Der Starter erkennt ausbleibenden Ladefortschritt und bietet nach 45 Sekunden Warten, Diagnoseexport, Neustart und Reparatur an. Er beendet einen langsamen Start nicht automatisch. Profile, Einstellungen und geschützte Anmeldedaten bleiben erhalten; Spielversion 1002133 und bisherige Fixes sind enthalten.

Enthalten sind modernisierte Bibliotheken, allgemeine Sicherheits- und Ressourcenverbesserungen, der D3D11-HUD-Texturfix, FPS/VSync, HUD-Größe, Chat-Uhrzeit, verschiebbare Komponenten, Ping/FPS unten rechts, Remnant-Filter, Sirius-Bauplanfarben und Kryonitmengen.

Orbitalwarnungen, Bossleisten und weitere Zusatzanzeigen gehören zu **[Forge Enhanced](https://github.com/FallenIncursio/pirate-galaxy-forge-releases)**. Beide Editionen teilen dieselbe Core-Implementierung.

Voraussetzungen: Windows 10/11 x64 und .NET Framework 4.8. Der Starter lädt die geprüfte Spielbasis und Java-Laufzeit bei Bedarf. Core nutzt einen eigenen Datenordner und übernimmt keine Enhanced-Profile automatisch.

60 Editionssuiten, sechs Negativkontrollen sowie 109 Installations-, Upgrade- und Reparaturprüfungen bestanden. Die Hängerdiagnose wurde zusätzlich mit echten 45-Sekunden-Prozessprüfungen getestet. Enhanced wurde über Starter 14 mit D3D11 in der Sandbox gestartet; der Nutzer meldet bisher störungsfreien Betrieb. Die konkrete Ursache auf betroffenen Spielerrechnern ist damit noch nicht nachgewiesen. Kamerabhängige Helligkeit, die native Sirius-Absturzursache, eine separate Core-Spielsitzung, andere GPUs, Wine und Langzeittests bleiben offen. [Prüfstand](RELEASE-STATUS-0.2-alpha.14.md).

Updates sind RSA-signiert; der Installer besitzt keine Windows-Authenticode-Signatur. Bibliotheksquellen und Lizenzhinweise gehören zu den Release-Downloads. Forge bleibt eine experimentelle Alpha ohne behauptete offizielle Splitscreen-Freigabe.
