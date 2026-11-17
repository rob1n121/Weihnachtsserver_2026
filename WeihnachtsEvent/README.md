# 🎅 WeihnachtsEvent

**Version 2.7.2** · Das Herzstück des Winterservers. Es kümmert sich um Status, Teams, Homes, Teleports, Kistenschutz, das Shopping-Viertel und Portale.

## ✨ Features

- **Status:** Status wie AFK, Bauen oder Questen per Menü wählen. Freigeschaltete Adventsstatus aus AdventQuests sind mit ✦ markiert.
- **Präfixe:** Vor dem Namen steht immer genau ein Präfix (Team, Status oder Owner). Ein gesetzter Status hat Vorrang vor dem Owner-Präfix.
- **Teams:** Bis zu 5 Spieler, eigene Teamfarbe, Teamchat mit `/tc`. Friendly Fire ist immer an.
- **Homes & TPA:** Standardmäßig 3 Homes, mehr über Rechte. Teleports mit 3 Sek. Wartezeit und 10 Sek. Cooldown.
- **Kistenschutz:** Mit `/lock` sperrst du eine Kiste, dann können nur du und dein Team sie öffnen.
- **Shopping-Viertel:**
  - Jeder Spieler bzw. jedes Team bekommt beim ersten `/hub` automatisch einen eigenen Platz.
  - Die Platzgrenzen kann man als Partikel anzeigen lassen.
  - In der Schutzzone darf man nur auf dem eigenen Platz bauen, es spawnen keine Mobs und TNT macht nichts kaputt.
- **Portale:** Admins bauen Teleport-Portale mit eigener Nachricht.

<!-- Screenshot: ../docs/screenshots/shopping-viertel.png -->

## 📜 Befehle (Auswahl)

| Befehl | Beschreibung |
|---|---|
| `/status` | Status wählen |
| `/team` | Team erstellen und verwalten |
| `/tc <Nachricht>` | Teamchat |
| `/sethome` · `/home` · `/homes` | Homes |
| `/tpa` · `/tpahere` · `/tpaccept` | Teleport-Anfragen |
| `/lock` · `/unlock` | Kisten sperren |
| `/hub` | Shopping-Viertel |

Alle Befehle mit Rechten, auch die für Admins, findest du in der [PERMISSIONS.md](../PERMISSIONS.md#-weihnachtsevent--status).

## 🔗 Abhängigkeiten

- **AdventQuests** für die Adventsstatus in `/status`

---

> 📁 **Hier deinen Plugin-Code einfügen:** `src/`, `build.gradle` bzw. `pom.xml` usw.
