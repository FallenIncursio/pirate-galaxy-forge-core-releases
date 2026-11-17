# Pirate Galaxy Forge Core

Inoffizieller 64-Bit-Communityclient für Pirate Galaxy.

**[Windows-Installer herunterladen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/download/v0.2.0-alpha.7/PirateGalaxyForgeCore-0.2.0-alpha.7-Setup.exe)** · **0.2.0-alpha.7** · [Releasehinweise und Prüfsummen](https://github.com/FallenIncursio/pirate-galaxy-forge-core-releases/releases/tag/v0.2.0-alpha.7)

Core enthält die gemeinsame 64-Bit-Technik, allgemeine Korrekturen und begrenzten Komfort. Die ursprüngliche Hilfe bleibt erhalten. Zusätzliche Optionen stehen in der nativen Erweiterung der Spieleinstellungen.

[Core / Enhanced und 32-Bit-Vergleich](FEATURES.md) · [Änderungen dieser Ausgabe](0.2.0-alpha.7.md) · [Installation und Profilübernahme](INSTALLER-UPDATER.md) · [Absturzursache und Fix](ALPHA7-MATERIAL-CLEANUP.md)

Diese Ausgabe behebt einen nachgestellten nativen D3D11-Absturz bei der Material-/Shader-Bereinigung. Vor dem Zugriff auf einen Render-Pass wird dessen Lebensdauer geprüft, sodass bereits freigegebener und wiederverwendeter Speicher nicht mehr dereferenziert wird. Core und Enhanced enthalten denselben Fix. Die Remnant-/Aggrobeacon-Korrekturen aus alpha.6 bleiben erhalten; ebenso D3D9, Einstellungen und Profile.

Enthalten sind modernisierte Bibliotheken, allgemeine Sicherheits- und Ressourcenverbesserungen, der D3D11-HUD-Texturfix, FPS/VSync, HUD-Größe, Chat-Uhrzeit, verschiebbare Komponenten, Ping/FPS unten rechts, Remnant-Filter, Sirius-Bauplanfarben und Kryonitmengen.

Orbitalwarnungen, Bossleisten und weitere Zusatzanzeigen gehören zu **[Forge Enhanced](https://github.com/FallenIncursio/pirate-galaxy-forge-releases)**. Beide Editionen teilen dieselbe Core-Implementierung.

Voraussetzungen: Windows 10/11 x64 und .NET Framework 4.8. Der Starter lädt die geprüfte Spielbasis und Java-Laufzeit bei Bedarf. Core nutzt einen eigenen Datenordner und übernimmt keine Enhanced-Profile automatisch.

800 gezielte Bereinigungszyklen in acht Szenarien bestanden; fünf Fehlerfälle reproduzieren den Absturz mit alpha.5 und alpha.6. Enhanced wurde mit D3D11 in der Sandbox getestet; der Nutzer berichtet bisher keine weiteren Abstürze. Dauer und Wechselzahl dieser Sitzung sind nicht erfasst. Der genaue frühere Ingame-Auslöser ist nicht vollständig rekonstruiert. Eine gesonderte Core-Spielsitzung, andere Absturzursachen, weitere GPUs/Treiber, Wine und quantitative Langzeitmessungen sind dadurch nicht abgedeckt. Automatische Prüfungen stehen im [Release-Prüfstand](RELEASE-STATUS-0.2-alpha.7.md).

Updates sind RSA-signiert; der Installer besitzt keine Windows-Authenticode-Signatur. Bibliotheksquellen und Lizenzhinweise gehören zu den Release-Downloads. Forge bleibt eine experimentelle Alpha ohne behauptete offizielle Splitscreen-Freigabe.
