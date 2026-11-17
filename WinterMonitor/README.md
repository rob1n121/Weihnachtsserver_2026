# 📈 WinterMonitor

**Version 1.2.1** · Performance-Werkzeuge für den Winterserver: TPS-Anzeige, Lag-Suche und automatische Drosselung.

## ✨ Features

- **TPS-Leiste:** Spieler können sie mit `/tpsbar` ein- und ausblenden.
- **TPS/MSPT-Übersicht** mit `/lag`
- **Drosselung** bei Lag, auch für Redstone
- **Lag-Chunks finden:** `/uc` zeigt die Chunks mit den meisten Updates, man kann direkt hinteleportieren.
- **Block-Updates im Chat:** zum Debuggen mit `/updates`

## 📜 Befehle

| Befehl | Beschreibung | Permission |
|---|---|---|
| `/tpsbar` | TPS-Leiste an/aus | `wintermonitor.tpsbar` |
| `/lag` (+ `throttle off` \| `reload` \| `redstone`) | TPS/MSPT, Drosselung | `wintermonitor.admin` |
| `/uc start\|stop\|top\|tp` | Lag-Chunks finden | `wintermonitor.admin` / `updatecheck.use` |
| `/updates true\|false` | Block-Updates im Chat | `wintermonitor.admin` |

---

> 📁 **Hier deinen Plugin-Code einfügen:** `src/`, `build.gradle` bzw. `pom.xml` usw.
