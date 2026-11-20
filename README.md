# Pirate Galaxy Forge Core

Inoffizieller 64-Bit-Communityclient für Pirate Galaxy.

**[Windows-Installer herunterladen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/download/v0.2.0-alpha.15/PirateGalaxyForgeCore-0.2.0-alpha.15-Setup.exe)** · **0.2.0-alpha.15** · [Releasehinweise und Prüfsummen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/tag/v0.2.0-alpha.15)

Core enthält die gemeinsame 64-Bit-Technik, allgemeine Korrekturen und begrenzten Komfort. Die ursprüngliche Hilfe bleibt erhalten. Zusätzliche Optionen stehen in der nativen Erweiterung der Spieleinstellungen.

[Core / Enhanced und 32-Bit-Vergleich](FEATURES.md) · [Änderungen dieser Ausgabe](0.2.0-alpha.15.md) · [Installation und Profilübernahme](INSTALLER-UPDATER.md) · [Live-Logs und Startdiagnose](ALPHA15-STARTUP-DIAGNOSTICS.md)

Live-Logs und Startdiagnose sind direkt im Starter, über das Taskleistensymbol und den Startmenüeintrag erreichbar. Erneutes Öffnen des Starters zeigt die laufende Diagnose. Eine freiwillige 30-Sekunden-Aufnahme erfasst Prozesszustand und mehrere technische JVM-Aufnahmen, auch nach gemeldeter Loginbereitschaft. Unabhängiger Downloadfortschritt verdeckt keine blockierte Ressourcenabhängigkeit mehr. Speichern und Senden enthalten denselben begrenzten Diagnoseumfang; Rohlogs und Anmeldedaten werden nicht übertragen. Profile, Spielversion 1002133 und bisherige Fixes bleiben erhalten.

Enthalten sind modernisierte Bibliotheken, allgemeine Sicherheits- und Ressourcenverbesserungen, der D3D11-HUD-Texturfix, FPS/VSync, HUD-Größe, Chat-Uhrzeit, verschiebbare Komponenten, Ping/FPS unten rechts, Remnant-Filter, Sirius-Bauplanfarben und Kryonitmengen.

Orbitalwarnungen, Bossleisten und weitere Zusatzanzeigen gehören zu **[Forge Enhanced](https://github.com/FallenIncursio/pirate-galaxy-forge-releases)**. Beide Editionen teilen dieselbe Core-Implementierung.

Voraussetzungen: Windows 10/11 x64 und .NET Framework 4.8. Der Starter lädt die geprüfte Spielbasis und Java-Laufzeit bei Bedarf. Core nutzt einen eigenen Datenordner und übernimmt keine Enhanced-Profile automatisch.

Prüfumfang und Sandbox-Abnahme stehen im [Release-Prüfstand](RELEASE-STATUS-0.2-alpha.15.md). Das Update verbessert die Erkennung und Nachvollziehbarkeit; die konkrete Ursache aller gemeldeten Ladehänger ist damit nicht bewiesen. Kamerabhängige Helligkeit, die native Sirius-Absturzursache, weitere GPUs, Wine und Langzeittests bleiben offen.

Updates sind RSA-signiert; der Installer besitzt keine Windows-Authenticode-Signatur. Bibliotheksquellen und Lizenzhinweise gehören zu den Release-Downloads. Forge bleibt eine experimentelle Alpha ohne behauptete offizielle Splitscreen-Freigabe.
