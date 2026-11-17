# 🔑 Befehle & Berechtigungen (LuckPerms)

Hier findest du alle Befehle und Rechte der Winterserver-Plugins und wie die Gruppen in **LuckPerms** eingerichtet sind.

**Stand:** 17.11.2026 · WeihnachtsEvent 2.7.2 · AdventQuests 1.4.7 · Wintermarkt 1.1.0 · WinterMonitor 1.2.1 · Paper 26.3

> Mit ⚠️ markierte Angaben sind nicht geprüft.

**Inhalt:** [Gruppen](#-gruppen) · [Spieler-Befehle](#-spieler-befehle) · [Admin-Befehle](#️-admin-befehle) · [LuckPerms einrichten](#-luckperms-einrichten)

---

## 👥 Gruppen

| Gruppe | Für wen | Gewicht |
|---|---|---|
| `default` | Alle Spieler | – |
| `extrahome` | Spieler mit 4 statt 3 Homes | – |
| `mods` | Nur Lag- und TPS-Werkzeuge | 50 |
| `admin` | Volle Rechte (`*`) | 100 |

Der Owner spielt als normaler Spieler und gibt sich nur bei Bedarf Admin-Rechte:

```
lp user <Name> parent add admin
lp user <Name> parent addtemp admin 1h
```

---

## 🎮 Spieler-Befehle

> Alle Spieler-Rechte stehen in den Plugins schon auf `default: true`. Man muss sie in LuckPerms also **nicht eintragen**, sondern nur bei Bedarf sperren.

### 🎅 WeihnachtsEvent – Status

| Befehl | Beschreibung |
|---|---|
| `/status` | Menü öffnen, Status per Klick wählen |
| `/status <name>` | Status direkt setzen: AFK, Bauen, Questen, Farmen, Erkunden, Beschäftigt oder ein freigeschalteter Adventsstatus (✦) |
| `/status aus` | Status entfernen |
| `/status liste` | Alle Status anzeigen |

| Permission | Wirkung |
|---|---|
| `weihnachtsevent.status` | Status benutzen |
| `weihnachtsevent.status.helfer` | Darf den Status „Helfer“ wählen |

### 👥 WeihnachtsEvent – Teams

| Befehl | Beschreibung |
|---|---|
| `/team erstellen <Name> [Farbe]` | Team gründen, man wird Leiter |
| `/team einladen <Spieler>` | Spieler einladen (nur Leiter, 5 Min. gültig) |
| `/team beitreten <Team>` | Einladung annehmen |
| `/team verlassen` | Team verlassen |
| `/team kick` · `leiter` · `farbe` · `aufloesen` | Team verwalten (nur Leiter) |
| `/team info [Team]` · `/team liste` | Mitglieder bzw. alle Teams ansehen |
| `/tc <Nachricht>` | Teamchat |

| Permission | Wirkung |
|---|---|
| `teams.benutzen` | Team-Befehle und Teamchat |
| `teams.erstellen` | Teams gründen |

Max. 5 Spieler pro Team, Friendly Fire ist immer an.

### 🏠 WeihnachtsEvent – Homes & TPA

| Befehl | Beschreibung |
|---|---|
| `/sethome [name]` | Home setzen |
| `/home [name]` | Zum Home teleportieren |
| `/delhome <name>` | Home löschen |
| `/homes` | Homes auflisten |
| `/tpa <Spieler>` | Anfrage: Du willst zu ihm |
| `/tpahere <Spieler>` | Anfrage: Er soll zu dir |
| `/tpaccept` · `/tpdeny` | Anfrage annehmen / ablehnen |

| Permission | Wirkung |
|---|---|
| `weihnachtsevent.home` | Homes benutzen |
| `weihnachtsevent.tpa` | TPA benutzen |
| `weihnachtsevent.homes.<anzahl>` | Mehr Homes (Standard: 3, die höchste Zahl gilt) |

Vor jedem Teleport wartet man 3 Sek., danach gibt es 10 Sek. Pause. Anfragen laufen nach 60 Sek. ab.

### 🔒 WeihnachtsEvent – Kisten sperren

| Befehl | Beschreibung |
|---|---|
| `/lock` | Angeschaute Kiste sperren (öffnen nur Besitzer + Team) |
| `/lock info` | Zeigt, wem die Kiste gehört |
| `/unlock` | Sperre aufheben |

**Permission:** `chestlock.use`

### 🛍️ WeihnachtsEvent – Shopping-Viertel

| Befehl | Beschreibung |
|---|---|
| `/hub` | Zum Spawn bzw. Viertel. Beim ersten Mal bekommt man automatisch einen Platz |
| `/hub platz` | Zum eigenen Platz |
| `/hub info` | Infos zum Platz, auf dem man steht |
| `/hub anzeigen` | Platzgrenzen als Partikel an/aus |

**Permission:** `weihnachtsevent.hub`

### 🎁 AdventQuests & 🏪 Wintermarkt

| Befehl | Beschreibung | Permission |
|---|---|---|
| `/advent fortschritt` | Eigener Questfortschritt | – |
| `/advent location` | Quest-Orte mit Koordinaten | `advent.location` |
| `/markt` · `/wintermarkt` | Wintermarkt öffnen, wenn Eberwin in der Nähe ist (sonst Schleichen + Rechtsklick auf Eberwin) | `wintermarkt.use` |

### 🎄 WeihnachtsDeko

| Befehl | Beschreibung | Permission |
|---|---|---|
| `/deko` | Deko-Shop (Bezahlung mit Smaragden) | `deko.use` |
| `/moebel` | Möbel-Shop (Bezahlung mit Smaragden) | `moebel.use` |
| – | Möbel platzieren | `moebel.platzieren` |

### 📈 WinterMonitor

| Befehl | Beschreibung | Permission |
|---|---|---|
| `/tpsbar` | TPS-Leiste an/aus | `wintermonitor.tpsbar` (per LuckPerms freigeschaltet) |

---

## 🛡️ Admin-Befehle

> Alle Admin-Rechte haben standardmäßig nur OPs. Die Gruppe `admin` bekommt sie über `*`.

### 🎅 WeihnachtsEvent

| Befehl | Beschreibung | Permission |
|---|---|---|
| `/weihnachtsevent reload` | Config neu laden | `weihnachtsevent.admin` |
| `/weihnachtsevent portal pos1\|pos2\|erstellen <n>\|ziel <n>\|nachricht <n> <Text>\|liste\|loeschen <n>` | Teleport-Portale bauen und verwalten | `weihnachtsevent.admin` |
| `/teamadmin` · `/ta` `[liste\|info\|erstellen\|loeschen\|hinzufuegen\|entfernen\|umbenennen\|farbe\|leiter]` | Alle Teams verwalten (Menü oder Befehl, auch Konsole) | `teams.admin` |
| `/statusadmin <Spieler> <status\|aus>` | Status eines Spielers setzen | ⚠️ vermutlich `weihnachtsevent.admin` |
| – | Eigenes Owner-Präfix (ein gesetzter Status hat Vorrang) | `weihnachtsevent.owner` |
| – | Kein Teleport-Cooldown | `weihnachtsevent.cooldown.bypass` |
| – | Unbegrenzte Homes | `weihnachtsevent.homes.unlimited` |
| `/lock reload`, fremde Kisten öffnen | ChestLock verwalten | `chestlock.admin` |

**Shopping-Viertel** – alle Befehle brauchen `weihnachtsevent.hub.admin`:

| Befehl | Beschreibung |
|---|---|
| `/hub setzen` | Spawn setzen. Beim ersten Mal entstehen auch das Viertel-Zentrum und die Schutzzone |
| `/hub zentrum [bestaetigen]` | Zentrum verschieben (⚠️ verschiebt **alle** Plätze!) |
| `/hub zuweisen <Spieler> [team\|allein]` | Platz unter den Füßen vergeben, alte Plätze werden frei |
| `/hub verbinden <Spieler> [team\|allein]` | Zusätzlichen Platz geben, angrenzende Plätze verschmelzen |
| `/hub wegnehmen <Name>` · `/hub wegnehmen hier` | Alle Plätze bzw. nur diesen Platz wegnehmen |
| `/hub liste` · `/hub reload` | Plätze auflisten / neu laden |

### 🎁 AdventQuests

**Gesamtrecht:** `adventquests.admin` (enthält alle `advent.admin.*`-Rechte)

| Befehl | Beschreibung | Permission |
|---|---|---|
| `/advent admin` | Admin-Terminal mit allen Befehlen als Knöpfe | `adventquests.admin` |
| `/advent start` | Event starten, Quest-Villager spawnen | `advent.admin.villagers` |
| `/advent villagers set\|list\|spawnall\|removeall` | Quest-Villager verwalten | `advent.admin.villagers` |
| `/advent spieler` | Spielermenü | `adventquests.admin` |
| `/advent reset <tag>` | Eigene Quest zurücksetzen | `adventquests.admin` |
| `/advent resetplayer <name> <tag\|all>` | Quest eines Spielers zurücksetzen | `adventquests.admin` |
| `/advent debug player <name>` | Debug-Infos zu einem Spieler | `adventquests.admin` |
| `/advent reward quest <tag>` | Quest-Belohnung geben | `adventquests.admin` |
| `/advent give <seide\|glueck> [spieler]` | Nordwind-Spitzhacke geben | `adventquests.admin` |
| `/advent questbook give <spieler>` | Winter-Reiseführer geben | `advent.admin.questbook` |
| `/advent quest <tag> objekt\|list\|remove\|clear` | Questobjekte verwalten | `adventquests.admin` |
| `/advent quest <tag> npc start\|finish\|remove` | Quest-NPCs setzen | `adventquests.admin` |
| `/advent quest 2 tree list\|remove\|respawn` | Bäume für Quest 2 | `adventquests.admin` |
| `/advent quest 4 trace <id\|line\|list\|remove\|clear>` | Schneespuren für Quest 4 | `adventquests.admin` |
| `/advent quest 5 ice list\|remove\|respawn` | Eisfelder für Quest 5 | `adventquests.admin` |
| `/advent quest 24 arena set\|info\|clear` | Bossarena für Quest 24 | `adventquests.admin` |
| `/advent crate set\|remove\|list\|preview\|key` | Winter-Crates | `adventquests.admin` |
| `/advent location set <ort>\|list\|meine` | Quest-Orte (werden automatisch geschützt) | `advent.admin.locations` |
| `/advent schutz set <name> <radius> [unten] [oben]\|list\|remove <name>\|hier` | Schutzzonen | `advent.admin.schutz` |
| `/aqlegendary give <id\|alle> [spieler]` | Endgame-Legendaries geben | `adventquests.admin` |

### 🏪 Wintermarkt · 🎄 WeihnachtsDeko · 📈 WinterMonitor

| Befehl | Beschreibung | Permission |
|---|---|---|
| `/markt reload` | Wintermarkt neu laden | `wintermarkt.admin` |
| `/deko …` | Händler setzen/entfernen, verschenken, reload, fremde Deko abbauen | `deko.admin` ⚠️ genauer Wortlaut ungeprüft |
| `/lag` (+ `throttle off` \| `reload` \| `redstone`) | TPS/MSPT anzeigen, Drosselung | `wintermonitor.admin` |
| `/uc start\|stop\|top\|tp` | Lag-Chunks finden | `wintermonitor.admin` / `updatecheck.use` |
| `/updates true\|false` | Block-Updates im Chat anzeigen | `wintermonitor.admin` |

---

## 💻 LuckPerms einrichten

Gib die Befehle in der Server-Konsole ein (ohne `/`) oder im Spiel mit `/`.

### Gruppe `default` – Sperren & Freigaben
```
lp group default permission set bukkit.command.plugins false
lp group default permission set bukkit.command.version false
lp group default permission set bukkit.command.help false
lp group default permission set backuper.* false
lp group default permission set backuper.backup_alert true
lp group default permission set wintermonitor.tpsbar true
```
Die ersten drei Zeilen verstecken die Plugin-Liste. Danach wird Backuper gesperrt, der Backup-Hinweis bleibt sichtbar, und die TPS-Leiste wird freigeschaltet.

### Gruppe `extrahome`
```
lp creategroup extrahome
lp group extrahome permission set weihnachtsevent.homes.4 true
lp user <Name> parent add extrahome
```

### Gruppe `mods` – nur Lag- und TPS-Werkzeuge
```
lp creategroup mods
lp group mods parent add default
lp group mods permission set wintermonitor.* true
lp group mods permission set updatecheck.use true
lp group mods permission set bukkit.command.tps true
lp group mods permission set bukkit.command.mspt true
lp group mods setweight 50
```

### Gruppe `admin`
```
lp creategroup admin
lp group admin permission set * true
lp group admin setweight 100
```

### 🔍 Rechte prüfen
```
lp verbose on <Spieler>
lp verbose off
```
`lp verbose on` zeigt beim Ausführen eines Befehls alle abgefragten Rechte in der Konsole an.

---

<details>
<summary><b>Rechte von Fremd-Plugins auf dem Server</b> (nicht Teil dieses Repos)</summary>

| Plugin | Funktion | Permission |
|---|---|---|
| DimensionLock | `/dimensionen` zeigt, wann Nether (21.11.) und End (12.12.) öffnen. Früher betreten mit Recht | kein Recht nötig · `dimensionlock.*` |
| TradeCycling | `/handelneu` würfelt Villager-Angebote neu (auch Schleichen + Linksklick oder F im Handelsfenster) · `/tradecycling` | `tradecycling.use` · `tradecycling.admin` |
| Unsichtbare Rahmen | Craften: 8 Rahmen + 1 Glasscheibe · `/urahmen` gibt Rahmen | `unsichtbarerahmen.herstellen` · `unsichtbarerahmen.geben` |
| squaremap | `/map hide` · `/map show` | ⚠️ ungeprüft |
| ArmorStandEditor | Schleichen + Rechtsklick | kein Recht nötig |
| Simple Voice Chat | Voice-Chat (Mod nötig) | `voicechat.speak`, `voicechat.listen` |
| Timber | Baum mit Axt fällt ganz | kein Recht nötig |
| LightMaker | Lichtblöcke craften | ⚠️ ungeprüft |
| Backuper | `/backup …` | `backuper.*` |
| WorldEdit, LogBlock | – | `worldedit.*`, `logblock.*` |
| Chunky, LuckPerms | – | nur Admin |
| Paper | `/msg`, `/tps`, `/mspt` | Standard · `bukkit.command.tps`, `bukkit.command.mspt` |

Nicht enthalten, weil die Befehle unbekannt sind: Wings, IslandFlight, FreedomChat.

</details>
