[README.md](https://github.com/user-attachments/files/34967481/README.md)
<h1 align="center">❄️ Winterserver</h1>
<p align="center"><b>Eine Sammlung selbst entwickelter Minecraft-Plugins für einen Event-Server zur Weihnachtszeit</b></p>

<p align="center">
  <img src="https://img.shields.io/badge/Minecraft-26.3-62B47A?style=flat-square" alt="Minecraft 26.3"/>
  <img src="https://img.shields.io/badge/Server-Paper-F7F7F7?style=flat-square" alt="Paper"/>
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java"/>
  <img src="https://img.shields.io/badge/Lizenz-MIT-blue?style=flat-square" alt="Lizenz MIT"/>
</p>

---

## 📖 Über das Projekt

Dieses Repository enthält die Plugins, die ich für einen eigenen Minecraft-Server zur Weihnachtszeit entwickelt habe. Die Plugins sind aufeinander abgestimmt und bilden zusammen ein komplettes Event: von Quests und Belohnungen über Teams und Spielerfunktionen bis zur Überwachung der Server-Performance.

<!-- <p align="center"><img src="docs/screenshots/spawn.png" width="700"/></p> -->

---

## ✨ Was die Plugins können

- 🎁 **Quests & Belohnungen:** Ein Adventskalender mit Quests, Crates und seltenen Items
- 👥 **Community:** Teams, Status und Präfixe, Teamchat
- 🏠 **Komfort:** Homes, Teleport-Anfragen und Kistenschutz
- 🛍️ **Wirtschaft:** Händler, Shops und ein Viertel mit eigenen Plätzen für die Spieler
- 📈 **Performance:** TPS-Anzeige, Lag-Suche und automatische Drosselung

---

## 🧩 Plugins

| Plugin | Kurzbeschreibung |
|---|---|
| [**WeihnachtsEvent**](WeihnachtsEvent/) | Die Kernfunktionen des Servers für Spieler und Teams |
| [**AdventQuests**](AdventQuests/) | Adventskalender mit Quests, Crates und Belohnungen |
| [**Wintermarkt**](Wintermarkt/) | Händler-NPC mit eigenem Markt |
| [**WeihnachtsDeko**](WeihnachtsDeko/) | Shop für Deko und Möbel |
| [**WinterMonitor**](WinterMonitor/) | Überwachung und Optimierung der Performance |

Details zu jedem Plugin stehen in der README im jeweiligen Ordner. Alle Befehle und Rechte findest du in [PERMISSIONS.md](PERMISSIONS.md).

---

## ⚙️ Voraussetzungen

- **Paper 26.3**
- **Java 25** oder neuer
- **[LuckPerms](https://luckperms.net/)** für Rechte und Gruppen

## 📦 Installation

1. Lade die `.jar`-Dateien unter [Releases](../../releases) herunter.
2. Lege sie in den Ordner `plugins/` deines Servers.
3. Starte den Server neu und passe die Configs an.

## 🔨 Selbst bauen

Jedes Plugin ist ein eigenes Projekt und lässt sich mit `./gradlew build` bzw. `mvn package` im jeweiligen Ordner bauen.

---

## 👤 Autor

**Robin** – [@rob1n121](https://github.com/rob1n121)

Dieses Projekt steht unter der [MIT-Lizenz](LICENSE).
