# Erste Schritte, Konto, Abo, Installation und Updates

Dieser Bereich erklärt, wie du Cash Lister installierst, dich im Dashboard anmeldest und abmeldest, was es mit deinem Zugang und deinem Abo auf sich hat, wie du deine Einstellungen sicherst und zurückholst und wie du die Extension aktualisierst. Das Dashboard selbst (Kennzahlen, Vorgänge, Checkliste „Heute", Glocke) ist im Bereich Dashboard (`references/dashboard.md`) beschrieben, jede einzelne Einstellung im Bereich Einstellungen (`references/einstellungen.md`).

> Hinweis für die Hilfe: Alles hier ist am aktuellen Stand der Extension (Version 46.3) geprüft. Stellen mit **Nicht sicher belegt:** sind offene Punkte. Sag dem Kunden dort ehrlich, dass du es nicht sicher weißt, und verweise ihn an den Betreiber. Erfinde nichts dazu. Fragen zu Preisen, Abo und Vertrag beantwortest du nur mit dem, was in Abschnitt 7 steht; rechtlich verbindlich sind allein die AGB auf der Webseite.

## Inhaltsverzeichnis

1. [Überblick: Woraus Cash Lister besteht](#1-überblick-woraus-cash-lister-besteht)
2. [Installation unter Windows (Ersteinrichtung)](#2-installation-unter-windows-ersteinrichtung)
3. [Installation auf dem Mac](#3-installation-auf-dem-mac)
4. [Dashboard, Einstellungen und Versionsnummer finden](#4-dashboard-einstellungen-und-versionsnummer-finden)
5. [Anmelden, angemeldet bleiben, abmelden](#5-anmelden-angemeldet-bleiben-abmelden)
   - [5.1 Was du siehst, wenn du nicht angemeldet bist](#51-was-du-siehst-wenn-du-nicht-angemeldet-bist)
   - [5.2 Anmelden mit Name und Passwort](#52-anmelden-mit-name-und-passwort)
   - [5.3 Anmelden mit der Einrichtungsdatei](#53-anmelden-mit-der-einrichtungsdatei)
   - [5.4 Das Feld Server-Adresse](#54-das-feld-server-adresse)
   - [5.5 Alle Meldungen beim Anmelden](#55-alle-meldungen-beim-anmelden)
   - [5.6 Wo du siehst, ob du angemeldet bist](#56-wo-du-siehst-ob-du-angemeldet-bist)
   - [5.7 Angemeldet bleiben](#57-angemeldet-bleiben)
   - [5.8 Abmelden](#58-abmelden)
   - [5.9 Meldungen anderer Bereiche, die „nicht angemeldet" bedeuten](#59-meldungen-anderer-bereiche-die-nicht-angemeldet-bedeuten)
6. [Zugang, Freischaltung, Kosten, Produkt-Vergabe](#6-zugang-freischaltung-kosten-produkt-vergabe)
7. [Abo und Zahlung](#7-abo-und-zahlung)
   - [7.1 Preise und Ablauf im Überblick](#71-preise-und-ablauf-im-überblick)
   - [7.2 Zahlungslink und Abschluss des Abos](#72-zahlungslink-und-abschluss-des-abos)
   - [7.3 Die Karte „Dein Abo" im Dashboard](#73-die-karte-dein-abo-im-dashboard)
   - [7.4 „Abo verwalten": das Kundenportal](#74-abo-verwalten-das-kundenportal)
   - [7.5 Warnungen bei offener Zahlung](#75-warnungen-bei-offener-zahlung)
   - [7.6 Abo-Sperre: was passiert und wie sie endet](#76-abo-sperre-was-passiert-und-wie-sie-endet)
   - [7.7 Kündigen, Shops ändern, Vertragsende](#77-kündigen-shops-ändern-vertragsende)
   - [7.8 Webseite mit AGB, Datenschutz und Impressum](#78-webseite-mit-agb-datenschutz-und-impressum)
8. [Produkt-Datenbank: jetzt je Konto auf dem Server](#8-produkt-datenbank-jetzt-je-konto-auf-dem-server)
9. [Einstellungs-Sicherung auf dem Server](#9-einstellungs-sicherung-auf-dem-server)
10. [Einstellungen als Datei exportieren und importieren](#10-einstellungen-als-datei-exportieren-und-importieren)
11. [Erste Schritte nach der Anmeldung (Checkliste)](#11-erste-schritte-nach-der-anmeldung-checkliste)
12. [Updates unter Windows](#12-updates-unter-windows)
13. [Updates auf dem Mac](#13-updates-auf-dem-mac)
14. [Den Updater einmalig erneuern](#14-den-updater-einmalig-erneuern)
15. [Mindestversion: wenn deine Version zu alt ist](#15-mindestversion-wenn-deine-version-zu-alt-ist)
16. [Zurück zur vorherigen Version](#16-zurück-zur-vorherigen-version)
17. [Chrome richtig schließen und den Hintergrunddienst aktualisieren](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)
18. [Probleme und Lösungen (Sammelstelle)](#18-probleme-und-lösungen-sammelstelle)
19. [Was diese Hilfe nicht sicher weiß](#19-was-diese-hilfe-nicht-sicher-weiß)
20. [Neu in Version 46.0](#20-neu-in-version-460)

---

## 1. Überblick: Woraus Cash Lister besteht

Cash Lister ist eine Chrome-Erweiterung („Extension") zum Listen von Amazon-Produkten bei eBay und zum Abgleich von Preis und Bestand. Sie besteht aus mehreren Teilen:

| Teil | Wo du ihn findest | Wofür |
|---|---|---|
| **Dashboard** („Cash Lister – Dashboard") | Klick auf das Cash-Lister-Symbol oben rechts in Chrome | Startseite: Anmeldung und Abmeldung, Überblick über den Tag, Karte „Dein Abo", Hinweise. Beschrieben im Bereich Dashboard (`references/dashboard.md`). |
| **Seitenleiste** | Links auf dem Dashboard, auf den Einstellungen und auf den Modulseiten | Öffnet alle Module, zeigt unten Verbindung, Anmeldung und die Versionsnummer |
| **Einstellungen** („Cash Lister – Einstellungen") | Seitenleiste → „Einstellungen" (Gruppe „System") | Alle Einstellungen in sechs Reitern, darunter „Preise & Listing" und „Sicherung" |
| **Module** (je ein eigener Tab) | Seitenleiste bzw. Karten im Dashboard | Produkt-Datenbank, CSV-Lister, Browser-Lister, Tracker, Verkaufs-Übersicht, Konkurrenz-Scanner |
| **Helfer auf Amazon- und eBay-Seiten** | Erscheinen von selbst auf den Seiten | Arbeiten beim Listen und beim Einsammeln von Produkten im Hintergrund |
| **Hintergrunddienst** | Unsichtbar | Erledigt Anmeldung, Listen, Tracker, Sicherung und die Verbindung zum Server |
| **Update-Programm** | Im Programmordner neben dem Ordner `extension` (`update.bat`, auf dem Mac `update.command`) | Holt neue Versionen |

Das frühere kleine Fenster (Popup), das sich beim Klick auf das Symbol öffnete, gibt es seit Version 46.0 nicht mehr. Seine Einstellungen stehen jetzt in den Einstellungen im Reiter „Preise & Listing", seine Sicherungs-Knöpfe im Reiter „Sicherung", die Anmeldung im Dashboard (siehe [Abschnitt 20](#20-neu-in-version-460)).

Wichtig zum Verständnis:

- **Deine Einstellungen liegen in Chrome, nicht im Ordner.** Der Ordner `extension` enthält nur das Programm. Einstellungen, Schlüssel (z. B. dein OpenAI-Schlüssel) und Anmeldung speichert Chrome im jeweiligen Chrome-Profil. Deshalb bleiben sie bei einem Update erhalten.
- **Die Produkt-Datenbank liegt seit 46.0 auf dem Server, je Konto.** Alle Geräte und Chrome-Profile, die mit demselben Konto angemeldet sind, sehen dieselbe Liste (siehe [Abschnitt 8](#8-produkt-datenbank-jetzt-je-konto-auf-dem-server)).
- **Jedes Chrome-Profil ist für sich.** Hast du mehrere Chrome-Profile, hat jedes seine eigenen Einstellungen und seine eigene Anmeldung. Für die Einstellungs-Sicherung zählt jedes Profil wie ein eigenes „Gerät".
- **Die Extension entfernt sich nicht selbst.** Sie kann sich nicht aus Chrome löschen.

---

## 2. Installation unter Windows (Ersteinrichtung)

Du bekommst vom Betreiber zwei Dinge:

1. das **Paket** (eine ZIP-Datei) mit dem Programmordner. Im Paket heißt dieser Ordner `LeckAtakan` (ein technischer Name, du musst ihn nicht ändern),
2. deine **Einrichtungsdatei**. Sie heißt `zugang.json` oder `leck-atakan-einrichtung-<dein Benutzername>.json`. Beide Namen funktionieren, du musst nichts umbenennen. Die Datei enthält deinen Anmeldenamen und dein Passwort, **gib sie nicht weiter**.

### So muss es am Ende bei dir liegen

```
LeckAtakan\
   update.bat        <- damit aktualisierst du
   update.ps1        <- gehört dazu, nicht löschen
   LIESMICH.txt
   zugang.json       <- deine Einrichtungsdatei (oder leck-atakan-einrichtung-<name>.json)
   extension\        <- DIESER Ordner wird in Chrome geladen
```

`update.bat` liegt **neben** dem Ordner `extension`, nicht darin.

### Schritt für Schritt

1. Lege einen Ordner an, am besten direkt auf Laufwerk C:, zum Beispiel `C:\LeckAtakan`.
2. Entpacke das Paket dorthin, sodass die Struktur wie oben aussieht. Wichtig: richtig entpacken (Rechtsklick auf die ZIP → „Alle extrahieren"), nicht nur in die ZIP hineinschauen.
3. Lege deine Einrichtungsdatei in den Programmordner, also neben `update.bat`.
4. Öffne in Chrome die Adresse `chrome://extensions`.
5. Schalte oben rechts den **„Entwicklermodus"** ein.
6. Klicke auf **„Entpackte Erweiterung laden"** und wähle den Ordner **`extension`** aus (den Ordner, in dem die Datei `manifest.json` liegt, nicht den Programmordner darüber).
7. Die Karte „Cash Lister" erscheint. Klicke oben in Chrome auf das Puzzle-Symbol und hefte Cash Lister mit der Stecknadel an, damit das Symbol immer sichtbar ist.
8. Klicke auf das Cash-Lister-Symbol. Das **Dashboard** öffnet sich in einem neuen Tab und zeigt den Anmeldebereich. Am einfachsten meldest du dich mit **„Einrichtungsdatei einlesen"** an (siehe [Abschnitt 5.3](#53-anmelden-mit-der-einrichtungsdatei)).
9. Danach die Checkliste in [Abschnitt 11](#11-erste-schritte-nach-der-anmeldung-checkliste) durchgehen.

### Wichtige Regeln nach der Installation

- **Den Ordner `extension` nicht verschieben und nicht umbenennen** (auch den Programmordner darüber nicht). Chrome merkt sich, wo er liegt. Findet Chrome ihn nicht mehr, kann die Extension nicht mehr starten.
- **Den Entwicklermodus eingeschaltet lassen.** Entpackt geladene Erweiterungen brauchen ihn.
  **Nicht sicher belegt:** Ob und ab welcher Chrome-Version Chrome solche Erweiterungen von selbst abschaltet, wenn der Entwicklermodus aus ist. Einschalten lassen ist auf jeden Fall richtig.
- **Niemals in `chrome://extensions` auf „Entfernen" klicken**, wenn du deine Einstellungen behalten willst. „Entfernen" löscht alle Einstellungen, Schlüssel und die Anmeldung dieser Extension in Chrome. (Die Produkt-Datenbank liegt seit 46.0 auf dem Server und ist davon nicht betroffen.) Der Kreispfeil (neu laden) und der Ein/Aus-Schalter löschen dagegen nichts.

### Häufige Fragen zur Installation

**Muss ich die Einrichtungsdatei umbenennen?**
Nein. `zugang.json` und `leck-atakan-einrichtung-<name>.json` werden beide erkannt, vom Update-Programm und von „Einrichtungsdatei einlesen" im Dashboard.

**Wofür brauche ich die Einrichtungsdatei nach der Anmeldung noch?**
Das Update-Programm meldet sich damit beim Server an, um neue Versionen zu holen. Sie muss deshalb neben `update.bat` liegen bleiben.

**Kann ich den Ordner woanders hinlegen, z. B. auf Laufwerk D: oder einen USB-Stick?**
Besser nicht. Empfohlen ist ein Ordner auf C:, z. B. `C:\LeckAtakan`. Das Update-Programm entpackt neue Versionen zuerst im temporären Ordner von Windows (normalerweise auf C:) und schiebt sie dann in deinen Ordner. Liegt dein Ordner auf einem anderen Laufwerk, kann dieser letzte Schritt scheitern (Meldung „Konnte die neue Fassung nicht einsetzen. Alte Fassung wiederhergestellt.").

**In meinem Paket liegt ein Ordner „Relay". Brauche ich den?**
Nein. Die aktuelle Extension benutzt ihn nicht, der Tracker arbeitet nur im Browser. Lass ihn einfach liegen, er stört nicht. Auf dem Mac lässt sich das Programm darin ohnehin nicht starten.

**Liegt mein Ordner auf dem Desktop oder in „Dokumente", ist das schlimm?**
**Nicht sicher belegt:** Manche Kunden hatten das Problem, dass die Extension verschwand. Eine mögliche, aber nicht bewiesene Ursache sind Programme, die Desktop oder „Dokumente" verschieben oder synchronisieren (z. B. OneDrive), oder Virenscanner. Ein eigener Ordner direkt auf C: wie `C:\LeckAtakan` ist die sichere Wahl.

**Öffnet sich nach der Installation von selbst etwas?**
Nein. Du öffnest das Dashboard mit einem Klick auf das Cash-Lister-Symbol.

### Probleme und Lösungen bei der Installation

| Problem | Lösung |
|---|---|
| Chrome meldet beim Laden, dass die Manifestdatei fehlt | Du hast den falschen Ordner gewählt. Wähle den Ordner `extension`, in dem direkt `manifest.json` liegt. Liegt im Ordner `extension` noch einmal ein Ordner `extension`, wurde doppelt entpackt: nimm den inneren oder räume die Struktur auf, bevor du lädst. |
| Knopf „Entpackte Erweiterung laden" fehlt | Der „Entwicklermodus" oben rechts in `chrome://extensions` ist aus. Einschalten. |
| Das Symbol ist nicht zu sehen | Puzzle-Symbol oben rechts in Chrome → bei „Cash Lister" die Stecknadel anklicken. |
| Nach dem Klick auf das Symbol passiert nichts | Siehe [Abschnitt 18](#18-probleme-und-lösungen-sammelstelle), „Klick auf das Symbol tut nichts". |
| Es öffnet sich ein kleines Fenster statt des Dashboards | Chrome hat noch eine ältere Fassung geladen. Chrome komplett neu starten bzw. die Extension neu laden ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)). |

---

## 3. Installation auf dem Mac

Die Extension selbst läuft auf dem Mac genauso wie unter Windows. Nur das Update-Programm ist anders: Statt `update.bat` gibt es `update.command`. Mac-Kunden bekommen diese Datei vom Betreiber einzeln (oft als `update-mac.zip`). `update.bat` und `update.ps1` kannst du auf dem Mac einfach liegen lassen, sie tun dort nichts.

### So muss es bei dir liegen

```
LeckAtakan/
   update.command    <- damit aktualisierst du
   zugang.json       <- deine Einrichtungsdatei (oder leck-atakan-einrichtung-<name>.json)
   extension/        <- DIESER Ordner wird in Chrome geladen
```

### Schritt für Schritt

1. Lege einen Ordner an, z. B. `LeckAtakan` in deinem Benutzerordner.
2. Entpacke die Extension dort in den Unterordner `extension`.
3. Lege deine Einrichtungsdatei daneben.
4. Lege `update.command` daneben (neben `extension`, nicht hinein). Hast du `update-mac.zip` bekommen: per Doppelklick entpacken und `update.command` an diese Stelle ziehen.
5. In Chrome: `chrome://extensions` → „Entwicklermodus" an → „Entpackte Erweiterung laden" → Ordner `extension` wählen.
6. Cash Lister anheften, auf das Symbol klicken und im Dashboard anmelden (siehe [Abschnitt 5](#5-anmelden-angemeldet-bleiben-abmelden)).
7. Einmalig `update.command` startklar machen (siehe [Abschnitt 13](#13-updates-auf-dem-mac)).

Auch auf dem Mac gilt: Ordner `extension` nicht verschieben oder umbenennen, Entwicklermodus anlassen, nie auf „Entfernen" klicken.

---

## 4. Dashboard, Einstellungen und Versionsnummer finden

### Das Dashboard öffnen

- **Klick auf das Cash-Lister-Symbol** oben rechts in Chrome öffnet das Dashboard („Cash Lister – Dashboard") in einem eigenen Tab. Ist das Symbol nicht zu sehen: Puzzle-Symbol → „Cash Lister".
- **Ist das Dashboard schon offen**, öffnet der Klick keinen zweiten Tab, sondern springt zum offenen Dashboard-Tab, auch in ein anderes Chrome-Fenster.
- Das Dashboard bleibt offen wie jede andere Webseite. Es schließt sich nicht, wenn du woanders hinklickst (anders als das frühere Popup).
- Was das Dashboard im Einzelnen zeigt, steht im Bereich Dashboard (`references/dashboard.md`).

### Die Seitenleiste

Links auf dem Dashboard, den Einstellungen und den Modulseiten steht dieselbe Seitenleiste:

- oben das Logo mit „Cash Lister" und „Listing & Tracking",
- Gruppe **„Arbeiten"**: „Dashboard", „Produkt-Datenbank", „CSV-Lister", „Browser-Lister", „Tracker" (den CSV-Lister sehen seit 46.0 alle Kunden),
- Gruppe **„Auswerten"**: „Verkaufs-Übersicht", „Konkurrenz-Scanner",
- Gruppe **„System"**: „Einstellungen",
- unten ein Kasten mit dem Verbindungs- und Anmeldestand (siehe [Abschnitt 5.6](#56-wo-du-siehst-ob-du-angemeldet-bist)),
- ganz unten die **Versionsnummer**, z. B. „Version 46.0".

**Module öffnen im eigenen Tab.** Ein Klick auf ein Modul öffnet es in einem neuen Tab. Ist es schon offen, springt der Klick zu diesem Tab, statt ein zweites Mal zu öffnen. Ohne Anmeldung sind alle Module außer „Dashboard" und „Einstellungen" grau und nicht anklickbar.

### Die Einstellungen öffnen

- Seitenleiste → **„Einstellungen"**. Das geht auch ohne Anmeldung.
- Oder Rechtsklick auf das Cash-Lister-Symbol → „Optionen".
- Oder `chrome://extensions` → bei „Cash Lister" auf „Details" → „Erweiterungsoptionen".

Die Seite heißt „Cash Lister – Einstellungen" und hat sechs Reiter: **„Preise & Listing"** (beim Öffnen gewählt), **„Produkt-Filter"**, **„eBay & Rahmenbedingungen"**, **„Beschreibungsvorlage"**, **„KI"** und **„Sicherung"**. Die einzelnen Einstellungen erklärt der Bereich Einstellungen (`references/einstellungen.md`). Den Reiter „Sicherung" und die Karte „Server & Produkt-Vergabe" im Reiter „eBay & Rahmenbedingungen" erklärt diese Datei ([Abschnitt 6](#6-zugang-freischaltung-kosten-produkt-vergabe), [9](#9-einstellungs-sicherung-auf-dem-server) und [10](#10-einstellungen-als-datei-exportieren-und-importieren)).

Gespeichert wird von selbst: Oben auf der Seite steht „jede Änderung wird gespeichert, sobald du das Feld verlässt". Der Knopf **„Speichern"** unten bestätigt das nur (Meldung „Einstellungen gespeichert"); du musst ihn nicht drücken. Der zuletzt gewählte Reiter wird nicht gemerkt: Nach dem Neuladen steht die Seite wieder auf „Preise & Listing".

### Die Versionsnummer

- Steht **unten in der Seitenleiste**, z. B. „Version 46.0" (früher oben im kleinen Fenster).
- Sie zeigt, welche Fassung Chrome geladen hat. Nach einem Update ist das deine erste Kontrolle.

### Rechtsklick auf das Symbol

Beim Rechtsklick auf das Cash-Lister-Symbol zeigt Chrome ein Menü. Ganz oben steht „Cash Lister". Das öffnet eine Infoseite im Internet (nicht die Webseite cash-lister.de). **Nicht sicher belegt:** was dort gerade steht und ob sie zum aktuellen Stand passt. Weicht etwas ab, gilt, was du in deiner Extension siehst. „Optionen" in diesem Menü öffnet die Einstellungen.

---

## 5. Anmelden, angemeldet bleiben, abmelden

Die Anmeldung findet seit 46.0 im **Dashboard** statt. Ohne Anmeldung sind alle Module gesperrt (in der Seitenleiste grau). Browser-Lister, Tracker, Produkt-Datenbank, das Listen auf Amazon-Seiten und die Produkt-Vergabe funktionieren nur angemeldet. Dashboard und Einstellungen kannst du auch ohne Anmeldung öffnen.

### 5.1 Was du siehst, wenn du nicht angemeldet bist

Oben im Dashboard steht „Willkommen bei Cash Lister", darunter Datum und „nicht angemeldet". Oben rechts im Kontofeld steht ein Fragezeichen und „Nicht angemeldet". Ein Klick auf dieses Kontofeld setzt den Cursor ins Anmeldeformular.

Darunter erscheint die Karte zum Anmelden. Sie hat zwei Spalten:

**Links:**
- Überschrift „Nicht angemeldet" und der Text „Melde dich mit deinem Zugang an. Danach füllt sich diese Seite von selbst."
- Feld „Benutzername"
- Feld „Passwort"
- Knopf „Anmelden"
- darunter eine Hinweiszeile. Hier erscheinen „Melde an …" und Fehlermeldungen (in Rot).

**Rechts (Überschrift „Einrichtungsdatei"):**
- Text „Datei vom Betreiber bekommen? Sie bringt die Einstellungen und deinen Zugang mit und meldet dich gleich an."
- Knopf **„Einrichtungsdatei einlesen"** mit einer Statuszeile darunter
- ganz unten ein zugeklappter Eintrag **„Server-Adresse (nur auf Ansage ändern)"**. Aufgeklappt zeigt er ein Feld mit dem grauen Platzhalter „wird automatisch gesetzt".

Die Karte erscheint auch, wenn dein Zugang abgeschaltet ist (Überschrift „Zugang abgeschaltet") oder dein Abo gesperrt ist (Überschrift „Abo gesperrt", siehe [Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet)).

### 5.2 Anmelden mit Name und Passwort

1. Auf das Cash-Lister-Symbol klicken. Das Dashboard öffnet sich.
2. Bei „Benutzername" deinen Anmeldenamen eintragen, bei „Passwort" dein Passwort. Beides bekommst du vom Betreiber. Es steht auch in deiner Einrichtungsdatei.
3. Auf „Anmelden" klicken oder Enter drücken. Der Knopf wird kurz grau, darunter steht „Melde an …".
4. Klappt es, verschwindet die Anmeldekarte. Oben steht dann „Guten Morgen, <Name>", „Guten Tag, <Name>" oder „Guten Abend, <Name>" (je nach Uhrzeit), oben rechts im Kontofeld dein Name mit „angemeldet". Die Module in der Seitenleiste werden anklickbar. Das Passwortfeld wird geleert.
5. Hast du die Einstellungen schon in einem anderen Tab offen, lade diesen Tab nach der **ersten** Anmeldung auf einem Gerät neu. Direkt nach der Anmeldung holt die Extension unter Umständen deine gesicherten Einstellungen vom Server (siehe [Abschnitt 9](#9-einstellungs-sicherung-auf-dem-server)). Ein schon offener Einstellungs-Tab zeigt noch die alten Werte.

Die Anmeldung wartet höchstens etwa 20 Sekunden auf den Server. Kommt bis dahin keine Antwort, erscheint „Server nicht erreichbar (…). Adresse prüfen oder später erneut versuchen.". Antwortet der Hintergrunddienst der Extension selbst nicht, erscheint nach etwa 30 Sekunden „Keine Antwort vom Hintergrunddienst – bitte noch einmal versuchen.".

### 5.3 Anmelden mit der Einrichtungsdatei

Das ist der bequemste Weg, du musst nichts abtippen.

1. Dashboard öffnen (nicht angemeldet).
2. In der rechten Spalte „Einrichtungsdatei" auf **„Einrichtungsdatei einlesen"** klicken.
3. Im Dateifenster deine Einrichtungsdatei wählen (`zugang.json` bzw. `leck-atakan-einrichtung-<name>.json`). Angeboten werden `.json`-Dateien.
4. Die Extension übernimmt die Einstellungen aus der Datei, trägt Name und Passwort links in die Felder ein und meldet dich sofort an. Unter dem Knopf steht dann z. B. „3 Einstellungen übernommen – melde an …".
5. Nach kurzer Zeit verschwindet die Anmeldekarte, und oben steht dein Name.

Name und Passwort aus der Datei werden nur zum Anmelden benutzt und **nicht** als Einstellung gespeichert. Steht in der Datei eine Server-Adresse, erscheint sie im Feld „Server-Adresse".

Meldungen unter dem Knopf:

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „<N> Einstellungen übernommen – melde an …" | Datei gelesen, Anmeldung läuft | Kurz warten. Danach ist die Karte weg, oder links erscheint eine Fehlermeldung. |
| „<N> Einstellungen übernommen. Die Datei enthielt keine Zugangsdaten – bitte von Hand anmelden." | Die Datei war gültig, enthielt aber keinen Namen und kein Passwort (z. B. eine eigene Export-Datei) | Name und Passwort links eintippen und „Anmelden" klicken. |
| „Die Datei ist kein gültiges JSON." | Die Datei ist beschädigt oder keine Einstellungsdatei | Richtige Datei wählen bzw. neue beim Betreiber anfordern. Die Datei nicht mit einem Textprogramm öffnen und speichern. |
| „Das ist keine Einstellungsdatei." | Die Datei hat nicht den erwarteten Aufbau | Richtige Datei wählen. |
| „Import fehlgeschlagen: …" | Chrome konnte nicht speichern | Chrome neu starten, erneut versuchen. Bleibt es: Betreiber fragen. |

Nach einem Fehler kannst du dieselbe Datei gleich noch einmal wählen.

**Achtung:** „Einrichtungsdatei einlesen" übernimmt **alles**, was in der Datei steht. Wählst du hier eine eigene Export-Datei (siehe [Abschnitt 10](#10-einstellungen-als-datei-exportieren-und-importieren)), werden auch deren Einstellungen und Schlüssel übernommen und ersetzen die auf diesem Gerät. Für eigene Export-Dateien ist der Import im Reiter „Sicherung" der Einstellungen gedacht.

Den Knopf „Einrichtungsdatei einlesen" gibt es nur, solange du nicht angemeldet bist (er steht in der Anmeldekarte).

### 5.4 Das Feld Server-Adresse

Du findest es in der Anmeldekarte rechts unten unter „Server-Adresse (nur auf Ansage ändern)" (zum Aufklappen anklicken).

- **Normalerweise nichts eintragen.** Ohne eigenen Eintrag nimmt die Extension automatisch die richtige Adresse. Dass das Feld vor der Anmeldung leer ist und nur „wird automatisch gesetzt" zeigt, ist richtig so.
- Nur ändern, wenn der Betreiber es dir ausdrücklich sagt. Gespeichert wird, sobald du nach einer Änderung das Feld verlässt.
- **Wichtig:** Dieses Feld zeigt vor der Anmeldung normalerweise **nichts** an, auch dann nicht, wenn früher einmal eine eigene Adresse gespeichert wurde. Ob bei dir eine eigene Adresse gespeichert ist, siehst du nur in den **Einstellungen → Reiter „eBay & Rahmenbedingungen" → Karte „Server & Produkt-Vergabe" → Feld „Server-Adresse"**.
- Hast du versehentlich eine falsche Adresse eingetragen und bekommst jetzt „Server nicht erreichbar": Einstellungen öffnen (geht auch ohne Anmeldung), Reiter „eBay & Rahmenbedingungen", in der Karte „Server & Produkt-Vergabe" das Feld „Server-Adresse" **komplett leeren**, einmal in ein anderes Feld klicken, dann im Dashboard neu anmelden. Ein leeres Feld bedeutet wieder „automatisch". (Auch dort gilt: Feld nur leer lassen oder auf Ansage des Betreibers ändern.)

### 5.5 Alle Meldungen beim Anmelden

Fehler erscheinen in Rot direkt unter dem Anmeldeformular (Hinweiszeile unter „Anmelden").

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Name oder Passwort falsch." | Name oder Passwort stimmen nicht (die Meldung unterscheidet absichtlich nicht, welches von beiden) | Groß-/Kleinschreibung prüfen, keine Leerzeichen davor oder dahinter. Am sichersten: „Einrichtungsdatei einlesen". Klappt es dann auch nicht: Betreiber fragen (evtl. wurde das Passwort geändert). |
| „Zu viele Fehlversuche. Bitte … Sekunden warten." bzw. „Zu viele Fehlversuche. Bitte kurz warten." | Nach mehreren falschen Versuchen ist die Anmeldung kurz gesperrt | Die genannte Zeit warten, dann sorgfältig noch einmal versuchen. |
| „Dieser Zugang ist abgeschaltet." | Dein Zugang ist vom Betreiber abgeschaltet | An den Betreiber wenden. Selbst lässt sich das nicht lösen. |
| „Anmeldung abgelehnt: Abo gesperrt." | Dein Abo ist wegen einer offenen Zahlung gesperrt. Die Karte zeigt dazu groß „Abo gesperrt" und den Text des Betreibers. | Zahlung erledigen, dann neu anmelden ([Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet)). |
| „Deine Version der Extension ist veraltet und wird nicht mehr unterstuetzt. Bitte melde dich beim Betreiber - du bekommst dann die neue Version." | Die Extension, die gerade im Hintergrund von Chrome läuft, ist älter als die Mindestversion | Update machen ([Abschnitt 12](#12-updates-unter-windows)), danach Chrome komplett neu starten. Mehr dazu in [Abschnitt 15](#15-mindestversion-wenn-deine-version-zu-alt-ist). |
| „Server nicht erreichbar (…). Adresse prüfen oder später erneut versuchen." | Innerhalb von etwa 20 Sekunden kam keine Antwort. In der Klammer steht die Adresse, die benutzt wurde. | Internetverbindung prüfen. VPN, Firewall oder Virenscanner können die Verbindung blockieren. In den Einstellungen (Reiter „eBay & Rahmenbedingungen", Karte „Server & Produkt-Vergabe") prüfen, ob im Feld „Server-Adresse" etwas steht, und es leeren, wenn der Betreiber nichts anderes gesagt hat ([Abschnitt 5.4](#54-das-feld-server-adresse)). Später erneut versuchen. |
| „Keine Antwort vom Hintergrunddienst – bitte noch einmal versuchen." | Der Hintergrunddienst der Extension hat innerhalb von etwa 30 Sekunden nicht reagiert. Typisch nach einem Update ohne Chrome-Neustart. | Noch einmal versuchen. Bleibt es: Chrome komplett neu starten oder die Extension neu laden ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)). |
| „Name und Passwort noetig" | Eines der Felder war leer (oder enthielt beim Namen nur Leerzeichen) | Beide Felder ausfüllen. |
| „Keine Server-Adresse hinterlegt. Bitte eintragen (Einstellungen → eBay → „Server & Produkt-Vergabe")." | Sollte praktisch nie vorkommen. Mit „eBay" ist der Reiter „eBay & Rahmenbedingungen" gemeint. | Nichts eintragen, sondern Chrome neu starten. Bleibt es: Betreiber fragen. |
| „Anmeldung fehlgeschlagen (HTTP …)." oder ein anderer Text | Unerwartete Antwort vom Server | Später erneut versuchen. Bleibt es: Betreiber mit genauer Meldung informieren. |

### 5.6 Wo du siehst, ob du angemeldet bist

| Stelle | Angemeldet | Nicht angemeldet | Zugang abgeschaltet | Abo gesperrt |
|---|---|---|---|---|
| Dashboard, Überschrift | „Guten Morgen/Guten Tag/Guten Abend, <Name>" | „Willkommen bei Cash Lister" | „Willkommen bei Cash Lister" | „Willkommen bei Cash Lister" |
| Dashboard, Zeile unter der Überschrift | „<Wochentag, Datum> · Server verbunden" (oder „· Server nicht erreicht") | „… · nicht angemeldet" | „… · Zugang abgeschaltet" | „… · Abo gesperrt" |
| Dashboard, Kontofeld oben rechts | Kürzel, Name, „angemeldet" | „?", „Nicht angemeldet" | Kürzel, Name, „Zugang abgeschaltet" | dein Name oder „Nicht angemeldet", darunter „Abo gesperrt" |
| Seitenleiste, Kasten unten | „Server verbunden", „angemeldet als <Name>", „Produkt-Vergabe aktiv" | „Nicht angemeldet", „Produkt-Vergabe aus" | „Zugang abgeschaltet", „angemeldet als <Name>", „Produkt-Vergabe aus" | „Abo gesperrt", „Details im Dashboard", „Produkt-Vergabe aus" |
| Module in der Seitenleiste | anklickbar | grau (außer Dashboard und Einstellungen) | grau | grau |

Weitere Anzeigen im Kasten der Seitenleiste:
- „Verbindung wird geprüft …": erscheint kurz beim Öffnen einer Seite.
- „Server nicht erreicht" mit „antwortet nicht seit …" oder „zuletzt erreicht …" und „Lister nehmen keine Produkte": Du bist angemeldet, aber der Server hat zuletzt nicht geantwortet. Ohne Server nehmen die Lister keine Produkte aus der Produkt-Datenbank; der Browser-Lister wartet und macht danach von selbst weiter. Einzelheiten im Bereich Dashboard (`references/dashboard.md`).

### 5.7 Angemeldet bleiben

- Die Anmeldung bleibt gespeichert, auch nach einem Chrome-Neustart oder einem Update. Du musst dich nicht jedes Mal neu anmelden.
- Die Extension prüft regelmäßig im Hintergrund, beim Chrome-Start und beim Öffnen des Dashboards, ob dein Zugang noch gilt. Ohne Server nehmen die Lister keine Produkte aus der Produkt-Datenbank ([Abschnitt 8](#8-produkt-datenbank-jetzt-je-konto-auf-dem-server)).
- Hat der Betreiber deinen Zugang abgeschaltet, ist alles gesperrt („Zugang abgeschaltet – bitte beim Betreiber melden. …"). Dann hilft nur der Betreiber.
- Ist dein Abo gesperrt, ist ebenfalls alles gesperrt, bis die Zahlung erledigt ist ([Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet)).
- Manchmal wirst du ohne Meldung abgemeldet (oben im Dashboard steht dann „Nicht angemeldet"). Dann einfach neu anmelden. Das passiert z. B., wenn dein Passwort geändert wurde, wenn deine Sitzung abgelaufen ist, oder wenn die im Hintergrund laufende Version zu alt ist. Im letzten Fall kommt beim erneuten Anmelden die Meldung „Deine Version der Extension ist veraltet …".
  **Nicht sicher belegt:** Nach welcher Zeit ohne Nutzung eine Sitzung abläuft. Frag den Betreiber.

### 5.8 Abmelden

1. Im Dashboard oben rechts auf das **Kontofeld** (Kürzel und dein Name) klicken.
2. Es klappt ein Feld auf: dein Name, darunter „Angemeldet · Server verbunden" (oder „Angemeldet · Server nicht erreicht"), und der Eintrag **„Abmelden"** mit dem Zusatz „Danach sperren sich die Module bis zur nächsten Anmeldung.".
3. Auf „Abmelden" klicken.
4. Läuft gerade auf diesem PC der Tracker, der Browser-Lister oder der CSV-Lister, fragt Chrome vorher: „Gerade läuft auf diesem PC: <Module>. Nach dem Abmelden sperren sich die Module. Trotzdem abmelden?". Mit „Abbrechen" bleibst du angemeldet.
5. Während des Abmeldens steht im Kontofeld „wird abgemeldet …". Danach erscheint wieder die Anmeldekarte.

Das Aufklappfeld schließt sich mit Escape oder mit einem Klick daneben.

Was beim Abmelden passiert:
- Deine Anmeldung wird auf dem Server und in Chrome beendet.
- **Deine Einstellungen und dein OpenAI-Schlüssel bleiben auf dem Gerät erhalten.** Deine Produkt-Datenbank bleibt auf dem Server und ist nach der nächsten Anmeldung wieder da.
- Solange du abgemeldet bist, sind alle Module gesperrt. Auch die **Produkt-Vergabe ist aus**. Melde dich wieder an, bevor du Produkte einsammelst (siehe [Abschnitt 6](#6-zugang-freischaltung-kosten-produkt-vergabe)).
- Die automatische Sicherung deiner Einstellungen pausiert, bis du wieder angemeldet bist.
- Ist dieses Gerät in den Einstellungen als Server eingetragen (Reiter „eBay & Rahmenbedingungen", Karte „Server-Modus"), verschwindet es beim Abmelden aus den Dashboards deiner anderen Geräte.

**Mit einem anderen Konto anmelden:** Erst abmelden, dann mit dem anderen Konto anmelden. Meldet sich im selben Chrome-Profil ein anderes Konto an, beginnt die Einstellungs-Sicherung für dieses Konto von vorn ([Abschnitt 9](#9-einstellungs-sicherung-auf-dem-server)).

### 5.9 Meldungen anderer Bereiche, die „nicht angemeldet" bedeuten

| Wo | Meldung | Bedeutung |
|---|---|---|
| Browser-Lister, Klick auf „Starten" | „Nicht angemeldet oder Zugang deaktiviert - bitte im Dashboard anmelden." bzw. „Nicht angemeldet oder Sitzung abgelaufen - bitte im Dashboard anmelden, dann starten." | Im Dashboard anmelden, dann neu starten. |
| Browser-Lister, Bestandsanzeige | „nicht angemeldet – bitte im Dashboard anmelden" | Im Dashboard anmelden. |
| Tracker (beim Öffnen) | „Für den Tracker brauchst du die Ultimate-Mitgliedschaft." und danach eine leere Seite | Trotz des Wortlauts kein Hinweis auf eine Zusatzbuchung. Es heißt: nicht angemeldet, Zugang abgeschaltet oder Abo gesperrt. Im Dashboard anmelden, dann den Tracker neu öffnen. |
| Amazon-Produktseite beim Listen | Fenster „Nicht angemeldet - bitte im Dashboard anmelden." und Tab-Titel „Auto-Listing - <ASIN>  FEHLER! Nicht angemeldet!" | Im Dashboard anmelden und den Lauf neu starten. |
| Produkt-Datenbank, Import | „Nichts importiert – bitte zuerst im Dashboard anmelden." | Anmelden, dann erneut importieren. |
| Verschiedene Stellen (Produkt-Datenbank, Lister) | „Nicht angemeldet – bitte im Dashboard anmelden.", „Sitzung abgelaufen – bitte im Dashboard neu anmelden.", „Zugang abgeschaltet – bitte beim Betreiber melden." oder „Abo gesperrt – bitte im Dashboard nachsehen." | Je nach Text: neu anmelden, Betreiber fragen oder Abo prüfen ([Abschnitt 7](#7-abo-und-zahlung)). |
| Einstellungen, Reiter „eBay & Rahmenbedingungen", Karte „Server & Produkt-Vergabe" | „● Produkt-Vergabe: AUS – keine Server-Adresse hinterlegt." | Trotz des Wortlauts heißt das in der Praxis: **du bist nicht angemeldet.** Im Dashboard anmelden, dann die Einstellungen neu laden. Danach muss dort „● Produkt-Vergabe: AN (über deine Anmeldung)" stehen. |
| Konkurrenz-Scanner beim Übernehmen | „⚠️ <N> Produkte wurden OHNE Reservierung übernommen – die Produkt-Vergabe hat nicht bestätigt. Sie sind für andere Nutzer weiter frei." | Die Produkte wurden nicht für dich reserviert. Anmeldung und Verbindung prüfen. |

(ASIN = die zehnstellige Amazon-Artikelnummer eines Produkts.)

### Häufige Fragen zur Anmeldung

**Wo melde ich mich an? Das kleine Fenster ist weg.**
Im Dashboard. Klick auf das Cash-Lister-Symbol, das Dashboard öffnet sich, die Anmeldekarte steht darin, solange du nicht angemeldet bist.

**Ich habe mein Passwort vergessen. Kann ich es selbst zurücksetzen?**
Nein, dafür gibt es in der Extension keine Funktion. Schau in deine Einrichtungsdatei, dort steht es. Sonst den Betreiber fragen.

**Kann ich mein Passwort selbst ändern?**
In der Extension gibt es dafür keine Funktion. Wende dich an den Betreiber. Nach einer Änderung brauchst du eine neue Einrichtungsdatei, sonst meldet das Update-Programm „Name oder Passwort stimmen nicht".

**Darf ich mich auf mehreren Geräten oder Chrome-Profilen mit demselben Konto anmelden?**
Technisch ist das vorgesehen: Die Produkt-Datenbank ist für alle Geräte eines Kontos gemeinsam ([Abschnitt 8](#8-produkt-datenbank-jetzt-je-konto-auf-dem-server)), und die Einstellungs-Sicherung ist auf „mehrere Geräte, ein Konto" ausgelegt ([Abschnitt 9](#9-einstellungs-sicherung-auf-dem-server)). Laut AGB darfst du deine Zugangsdaten nicht an Dritte weitergeben; Mitarbeiter, die für deine Shops arbeiten, gelten nicht als Dritte.
In der Extension ist keine Grenze für die Zahl der Geräte zu sehen.
**Nicht sicher belegt:** Ob der Betreiber die Zahl der Geräte je Konto trotzdem begrenzt. Frag ihn im Zweifel.

**Brauche ich für jeden Shop einen eigenen Zugang?**
Ja. Im Abo zählt jeder Shop als eigener Zugang mit eigenem Anmeldenamen; auf deiner Zahlungsseite stehen die Namen dieser Shops ([Abschnitt 7.2](#72-zahlungslink-und-abschluss-des-abos)). Einen weiteren Shop buchst du per E-Mail beim Betreiber hinzu ([Abschnitt 7.7](#77-kündigen-shops-ändern-vertragsende)), die Zugangsdaten für den neuen Shop bekommst du vom Betreiber. Produkt-Datenbank und Einstellungs-Sicherung gelten je Zugang, also je Shop.

**Wo sehe ich meine E-Mail-Adresse?**
Das Dashboard zeigt nur deinen Namen, keine E-Mail-Adresse.

**Muss ich nach jedem Update neu anmelden?**
Nein. Die Anmeldung bleibt erhalten. Nur wenn deine alte Version vom Server abgewiesen wurde („veraltet"), musst du dich nach dem Update einmal neu anmelden.

### Probleme und Lösungen bei der Anmeldung

Siehe die Tabellen oben und ausführlich [Abschnitt 18](#18-probleme-und-lösungen-sammelstelle): „Anmelden tut nichts", „Meldung veraltet", „Abo gesperrt".

---

## 6. Zugang, Freischaltung, Kosten, Produkt-Vergabe

### Zugang und Freischaltung

- Dein Zugang ist **an dein Konto** (Name + Passwort) gebunden und wird vom Betreiber ein- oder ausgeschaltet.
- Es gibt **keine Ausbaustufen** in der Extension. Mit aktivem Zugang und gültigem Abo sind alle Module freigeschaltet.
- Ist der Zugang abgeschaltet, kommt beim Anmelden „Dieser Zugang ist abgeschaltet." bzw. im Dashboard „Zugang abgeschaltet – bitte beim Betreiber melden. Mit einem anderen Zugang kannst du dich hier neu anmelden.".
- Ist dein Abo wegen einer offenen Zahlung gesperrt, ist das etwas anderes als „abgeschaltet": siehe [Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet).
- **Wie bekommst du einen Zugang?** Laut AGB nimmst du über das Anfrageformular auf der Webseite oder per E-Mail Kontakt mit dem Betreiber auf. Er legt dein Konto an und schickt dir einen persönlichen Zahlungslink ([Abschnitt 7.2](#72-zahlungslink-und-abschluss-des-abos)). Du bekommst deine Zugangsdaten und eine Einrichtungsdatei. Laut AGB kann der Betreiber den Zugang schon vor dem Abschluss zum Einrichten freischalten (am Tag der Freischaltung und an den zwei folgenden Kalendertagen, für diese Einrichtungszeit kostenlos). Kommt der Vertrag bis dahin nicht zustande, wird der Zugang laut AGB wieder gesperrt.
- **CSV-Lister:** Seit Version 46.0 sehen alle Kunden den CSV-Lister in der Seitenleiste und im Dashboard, eine eigene Freischaltung ist nicht mehr nötig. In der Seitenleiste ist er grau, solange du nicht angemeldet bist, wie alle Module. Seine Bedienung steht im Bereich Produktübersicht und CSV-Lister (`references/produktuebersicht-und-csv-lister.md`).

### Was kostet was?

- **Das Abo für Cash Lister** (Preise, Zahlung, Kündigung): [Abschnitt 7](#7-abo-und-zahlung).
- **In der Extension gibt es kein Guthaben und keine Credits.** Nirgends wird je Listing etwas abgezogen, und es gibt keine Guthaben-Anzeige. Das Wort „Ultimate" in der Tracker-Meldung „Für den Tracker brauchst du die Ultimate-Mitgliedschaft." ist keine Stufe, sondern heißt nur „nicht angemeldet, Zugang abgeschaltet oder Abo gesperrt". Der CSV-Lister hat ein Tageskontingent (wie viele Produkte du am Tag damit bearbeiten darfst); das ist eine Tagesgrenze, kein Guthaben (Einzelheiten im Bereich Produktübersicht und CSV-Lister).
- **Die KI läuft über deinen eigenen OpenAI-Schlüssel** (KI-Titel, KI-Artikelmerkmale). Das bezahlst du direkt bei OpenAI, das ist laut AGB nicht im Abo enthalten. Den Schlüssel trägst du in den Einstellungen im Reiter „KI" bei „OpenAI-API-Schlüssel (für die Titel-Generierung)" ein. Der Browser-Lister listet immer mit KI-Titel, ohne Schlüssel geht es also nicht. Typische Meldungen, z. B. im Status des Browser-Listers:
  - „Kein OpenAI API Key gesetzt (Options-Seite)." → Schlüssel in den Einstellungen, Reiter „KI", eintragen.
  - „OpenAI: API-Key ungültig oder abgelaufen – bitte prüfen (Einstellungen → KI → „OpenAI-API-Schlüssel")." → Schlüssel prüfen bzw. bei OpenAI neu erzeugen.
  - „OpenAI-Guthaben leer: kein Guthaben mehr auf dem OpenAI-Konto. Bitte unter platform.openai.com unter Billing Guthaben aufladen." → Das ist dein OpenAI-Konto, nicht Cash Lister.
  - „OpenAI: Rate-Limit (zu viele Anfragen) – kurz warten und erneut versuchen."
- **Gebühren bei eBay** (z. B. Verkaufsprovision, Anzeigengebühr) rechnet eBay mit dir ab, nicht Cash Lister.

### Produkt-Vergabe (auf Kundenebene erklärt)

- Die Produkt-Vergabe sorgt dafür, dass **nicht zwei Kunden von Cash Lister dasselbe Produkt listen**. Produkte, die du übernimmst, werden für dich reserviert. Hat sich ein anderer Kunde ein Produkt schon gesichert, bekommst du es nicht. Vor anderen eBay-Verkäufern schützt sie nicht.
- **Sie läuft nur, wenn du angemeldet bist.** Achte darauf, angemeldet zu sein, bevor du Produkte einsammelst.
- Den Zustand siehst du unten in der Seitenleiste („Produkt-Vergabe aktiv" bzw. „Produkt-Vergabe aus") und ausführlicher in den **Einstellungen → Reiter „eBay & Rahmenbedingungen" → Karte „Server & Produkt-Vergabe"** (Zusatz „verhindert doppeltes Listen"):
  - „● Produkt-Vergabe: AN (über deine Anmeldung)": alles in Ordnung.
  - „● Produkt-Vergabe: AUS – keine Server-Adresse hinterlegt.": Trotz des Wortlauts bedeutet das in der Praxis **„nicht angemeldet"**. Im Dashboard anmelden, dann die Einstellungen neu laden.
  - „● Produkt-Vergabe: AUS – nicht angemeldet. Es wird NICHTS reserviert!": kommt auf dieser Seite praktisch nicht vor; falls doch: im Dashboard anmelden, dann die Einstellungen neu laden.
  - Die Zeile prüft nur, ob auf diesem Gerät eine Anmeldung gespeichert ist. Ist dein Zugang abgeschaltet oder dein Abo gerade gesperrt worden, kann dort noch „AN" stehen. Maßgeblich ist dann der Kasten unten in der Seitenleiste („Produkt-Vergabe aus"); „Verbindung prüfen" zeigt den echten Stand.
  - Darunter steht ein Warnkasten: „Achtung: Ohne Anmeldung ist die Produkt-Vergabe komplett aus." mit „Es kommt keine Fehlermeldung – es wird dann einfach nichts mehr reserviert.".
- Mit dem Knopf **„Verbindung prüfen"** daneben testest du die Verbindung. Während der Prüfung steht dort „prüfe …". Mögliche Ergebnisse:
  - „OK – angemeldet als „<Name>", <N> Produkte reserviert.": alles in Ordnung. Die Zahl nennt die Produkte, die gerade für dich reserviert sind.
  - „Keine Server-Adresse hinterlegt.": Auch das heißt in der Praxis: nicht angemeldet. Im Dashboard anmelden.
  - „Nicht angemeldet – bitte im Dashboard anmelden.": im Dashboard anmelden.
  - „Anmeldung abgelehnt (401) – bitte im Dashboard neu anmelden.": deine Anmeldung ist abgelaufen. Im Dashboard neu anmelden (steht dort noch dein Name, vorher abmelden).
  - „Zugang ist abgeschaltet (403).": an den Betreiber wenden. Prüfe auch im Dashboard, ob dein Abo gesperrt ist.
  - „Keine Antwort: …": Verbindungsproblem (Internet, VPN, Firewall, Virenscanner). Später erneut versuchen.
  - „Server antwortet mit HTTP …", „Server erreichbar, kennt aber … nicht – …" oder eine andere Meldung: Betreiber mit dem genauen Text informieren.
  - Unter dem Ergebnis steht bei einer echten Prüfung zusätzlich eine Zeile „Server: …". Das ist nur zur Information.
- Einzelheiten zur Vergabe beim Import und Listen findest du in den Bereichen Produkt-Datenbank (`references/produkte-finden-und-datenbank.md`) und Listen auf eBay (`references/listen-auf-ebay.md`).

---

## 7. Abo und Zahlung

Cash Lister wird als **Monatsabo** abgerechnet. Hier steht, was du als Kunde davon siehst und tun kannst. Rechtlich verbindlich sind die AGB auf der Webseite ([Abschnitt 7.8](#78-webseite-mit-agb-datenschutz-und-impressum)). Bei Fragen zu deinem konkreten Vertrag, deiner Rechnung oder deinem Zugang hilft nur der Betreiber.

### 7.1 Preise und Ablauf im Überblick

**Preise (laut AGB § 5):**
- **150 Euro pro Monat** für den ersten Shop,
- **50 Euro pro Monat** für jeden weiteren Shop,
- alles **Nettopreise**, dazu kommt die gesetzliche Umsatzsteuer, derzeit **19 %**.
- Ein „Shop" ist laut AGB ein eBay-Verkäuferkonto. In Cash Lister hat jeder Shop deines Abos einen eigenen Zugang (Anmeldename).

Rechenbeispiele (netto → mit 19 % USt):

| Shops | Netto pro Monat | Mit 19 % USt |
|---|---|---|
| 1 | 150 € | 178,50 € |
| 2 | 200 € | 238,00 € |
| 3 | 250 € | 297,50 € |

Nicht im Abo enthalten sind laut AGB die Kosten für OpenAI (eigener Schlüssel) und Gebühren von eBay, Amazon und anderen Anbietern.

**Wer kann abschließen?** Laut AGB nur **Unternehmer** (§ 14 BGB) mit gewerblichem eBay-Verkäuferkonto. Das bestätigst du beim Abschluss mit einem Pflicht-Haken.

**Ablauf in Kurzform:**
1. Der Betreiber legt dein Konto an und schickt dir deinen **persönlichen Zahlungslink**.
2. Du öffnest den Link, prüfst Shops, Betrag und den Tag der ersten Abbuchung und gehst weiter zur Zahlung.
3. Beim Zahlungsdienst **Stripe** hinterlegst du Karte oder SEPA-Lastschrift, setzt den Pflicht-Haken (Unternehmer + AGB) und schließt ab.
4. Ab dann wird zu Beginn jedes Abrechnungszeitraums (ein Monat) im Voraus abgebucht.
5. Im Dashboard zeigt die Karte **„Dein Abo"** den Stand; über **„Abo verwalten"** kommst du ins Kundenportal (Rechnungen, Zahlungsart, Kündigen).
6. Bleibt eine Zahlung offen, warnt das Dashboard vorher. Wird nicht bezahlt, wird der Zugang gesperrt; nach der Zahlung wird er wieder frei ([Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet)).

**Ab wann?** Den Tag deiner ersten Abbuchung nennt deine persönliche Zahlungsseite. Laut AGB (§ 3) bleiben Zeiträume, die du nach einer bisherigen Vereinbarung schon bezahlt hast, bezahlt und werden nicht noch einmal berechnet.

### 7.2 Zahlungslink und Abschluss des Abos

Die Zahlungsseite gehört nicht zur Extension, sondern ist eine Webseite, die du über deinen Link öffnest. Ihr Wortlaut kann sich ändern. Stand jetzt sieht der Abschluss so aus:

1. **Link öffnen.** Du bekommst ihn vom Betreiber. Er gehört zu deinem Konto, gib ihn nicht weiter. Im Dashboard findest du ihn später auch über den Knopf „Zahlungsseite" in der Karte „Dein Abo" (falls dort angezeigt).
2. **Seite „Zahlung einrichten".** Dort stehen:
   - eine Begrüßung mit deinem Namen,
   - die Zahl deiner Shops und ihre Namen,
   - groß der Monatsbetrag netto, daneben der Zusatz mit der Umsatzsteuer und dem Bruttobetrag „im Monat",
   - eine Zeile zum Beginn, z. B. „Bezahlt bis <Datum> – erste Abbuchung am <Datum> (…), danach monatlich." oder „Abbuchung heute (…), danach monatlich.",
   - der Hinweis „Du hinterlegst jetzt Karte oder SEPA-Lastschrift bei unserem Zahlungsdienst Stripe. Kündigen geht jederzeit zum Ende des laufenden Abrechnungszeitraums.",
   - die Zeile „Es gelten die AGB von Cash Lister (…)." mit einem Link zu den AGB, meist mit dem Zusatz „Du bestätigst sie im nächsten Schritt bei Stripe.",
   - der Knopf **„Weiter zur Zahlung"**.
3. **Bestellseite von Stripe.** Dort wählst du die Zahlungsart (Karte oder SEPA-Lastschrift, je nachdem, was angeboten wird) und gibst die Angaben ein, die Stripe abfragt (z. B. Rechnungsadresse).
4. **Pflicht-Haken.** Vor dem Abschluss musst du ankreuzen: „Ich handle als Unternehmer (§ 14 BGB) und stimme den AGB von Cash Lister (…) zu." Ohne diesen Haken ist kein Abschluss möglich.
5. **Abschließen.** Damit kommt laut AGB der Vertrag zustande.
6. **Kontrolle im Dashboard:** Die Karte „Dein Abo" zeigt danach „eingerichtet" (erste Abbuchung steht noch aus) oder „aktiv". Hast du die Zahlungsseite über einen Knopf im Dashboard geöffnet, holt das Dashboard den Stand neu, sobald du in seinen Tab zurückkommst. Sonst das Dashboard einmal neu laden.

Andere Seiten, die dein Link zeigen kann:

| Seite | Bedeutung | Was tun |
|---|---|---|
| „Dein Abo" mit einer farbigen Zeile „Dein Abo: …" | Dein Abo läuft schon. Darunter je nach Lage die Knöpfe „Offene Rechnung bezahlen", „Zahlungsart ändern, Rechnungen, kündigen" (Anmeldung dort über einen Link an deine E-Mail-Adresse) und, falls nötig, „Abo neu abschließen". | Je nach Anliegen den passenden Knopf. Ist dir unklar, ob du „Abo neu abschließen" brauchst: Betreiber fragen. |
| „Keine Zahlung nötig" | Für dein Konto wird nichts abgerechnet. | Nichts tun. |
| „Noch nicht bereit" | Für dich sind noch keine Shops eingetragen. | Betreiber fragen. |
| „Zahlung gerade nicht möglich" | Die Zahlung geht im Moment nicht. | Später erneut versuchen oder Betreiber fragen. |

Laut AGB kündigt Stripe eine SEPA-Lastschrift spätestens zwei Kalendertage vor dem Einzug per E-Mail an. Rechnungen bekommst du als PDF per E-Mail oder im Kundenportal.

### 7.3 Die Karte „Dein Abo" im Dashboard

Du findest sie im Dashboard ganz unten, unter der Karte „Heute". Sie erscheint nur, wenn du angemeldet bist und für dein Konto ein Abo abgerechnet wird. Ohne Abrechnung (z. B. bei Konten, für die der Betreiber nichts abrechnet) bleibt sie weg.

Aufbau:
- Überschrift **„Dein Abo"**, daneben ein farbiges Kennzeichen (Marker) und eine Statuszeile.
- **„Shops"**: wie viele Shops dein Abo umfasst.
- **„Monatlich"**: der Monatsbetrag netto, darunter klein „zzgl. 19 % USt".
- Je nach Stand eine dritte Angabe: **„Erste Abbuchung"** (Abo eingerichtet, noch nichts abgebucht), **„Gekündigt zum"** (nach einer Kündigung) oder **„Zugang bis"** (Zahlung offen, überfällig, fehlgeschlagen, kein Abo, beendet).
- Knopf **„Abo verwalten"** (Kundenportal, [Abschnitt 7.4](#74-abo-verwalten-das-kundenportal)).
- Knopf **„Zahlungsseite"** (nur, wenn der Link bekannt ist), öffnet deine persönliche Zahlungsseite in einem neuen Tab.
- Darunter der Hinweis „Kündigen, Zahlungsart ändern, Rechnungen: alles im Kundenportal unter „Abo verwalten"." Nach einer Meldung kehrt dieser Text nach etwa 10 Sekunden zurück.

Die Marker und was sie bedeuten:

| Marker | Bedeutung | Was tun |
|---|---|---|
| „aktiv" (grün) | Bezahlt, das Abo läuft. | Nichts. |
| „eingerichtet" | Abo abgeschlossen, die erste Abbuchung kommt noch (Datum bei „Erste Abbuchung"). | Nichts. |
| „Zahlung unterwegs" | Eine SEPA-Lastschrift läuft noch. Bei Lastschrift steht erst einige Werktage nach dem Einzug fest, ob er geklappt hat. | Abwarten, für Deckung sorgen. |
| „gekündigt" | Du hast gekündigt, das Abo läuft bis zum Ende des Zeitraums (Datum bei „Gekündigt zum"). | Nichts, außer du willst weitermachen: Betreiber fragen. |
| „Zahlung offen" | Eine Zahlung ist fällig und noch nicht da. | Bezahlen, siehe [Abschnitt 7.5](#75-warnungen-bei-offener-zahlung). |
| „überfällig" | Eine Abbuchung hat nicht geklappt. | Zahlungsart prüfen bzw. bezahlen ([Abschnitt 7.5](#75-warnungen-bei-offener-zahlung)). |
| „Zahlung fehlgeschlagen" | Die erste Abbuchung hat nicht geklappt. | Wie „überfällig". |
| „kein Abo" | Für dich ist noch kein Abo abgeschlossen. „Zugang bis" zeigt, wie lange dein bisheriger Zugang läuft. | Abo über die Zahlungsseite einrichten. |
| „beendet" | Dein Abo ist beendet (z. B. nach einer Kündigung). | Weitermachen: über die Zahlungsseite neu einrichten oder Betreiber fragen. |
| „gesperrt" | Ein Shop deines Abos ist wegen einer offenen Zahlung gesperrt. | Bezahlen ([Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet)). |

Die **Statuszeile** neben dem Marker kommt vom Server und nennt die Daten genauer, zum Beispiel:
- „Aktiv bis <Datum> – nächste Abbuchung <Datum>"
- „Eingerichtet – erste Abbuchung am <Datum>"
- „Lastschrift unterwegs – Sperre spätestens <Datum>"
- „Gekündigt zum <Datum> – Zugang bis <Datum>"
- „Aktiv, Zahlung offen – Sperre ab <Datum>"
- „Überfällig seit <Datum> – Sperre ab <Datum>" (ist der Tag schon da: „… – Sperre fällig seit <Datum>")
- „Erste Zahlung fehlgeschlagen – Sperre ab <Datum>"
- „Kein Abo – Zugang bis <Datum>"
- „Abo beendet – Zugang bis <Datum>"
- „Gesperrt seit <Datum>"

Der genaue Wortlaut kann leicht abweichen.

**Wann wird die Karte aktualisiert?** Die Extension holt den Abo-Stand bei jeder erfolgreichen Prüfung deiner Anmeldung (regelmäßig im Hintergrund, beim Chrome-Start und beim Öffnen bzw. Neuladen des Dashboards), direkt nach dem Anmelden und wenn du aus dem Kundenportal oder von der Zahlungsseite in den Dashboard-Tab zurückkommst (sofern du sie über einen Knopf im Dashboard geöffnet hast). Antwortet der Server nicht, bleibt der letzte Stand stehen.

### 7.4 „Abo verwalten": das Kundenportal

Im Kundenportal unseres Zahlungsdienstes Stripe kannst du **deine Rechnungen abrufen** (laut AGB als PDF), **die Zahlungsart ändern** und **kündigen** (zum Ende des laufenden Abrechnungszeitraums). So steht es auch unter dem Knopf: „Kündigen, Zahlungsart ändern, Rechnungen: alles im Kundenportal unter „Abo verwalten"."

So kommst du hin:
1. Dashboard öffnen (angemeldet).
2. Ganz unten in der Karte „Dein Abo" auf **„Abo verwalten"** klicken.
3. Der Knopf wird kurz grau, darunter steht „Kundenportal wird geöffnet …".
4. Das Kundenportal öffnet sich in einem **neuen Tab**, im Dashboard steht „Kundenportal im neuen Tab geöffnet.".
5. Wenn du fertig bist, zurück in den Dashboard-Tab wechseln. Das Dashboard holt dann den Abo-Stand neu.

Meldungen unter dem Knopf:

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Kundenportal wird geöffnet …" | Die Extension fragt den Server nach dem Zugang zum Portal. | Kurz warten. |
| „Kundenportal im neuen Tab geöffnet." | Hat geklappt. | Im neuen Tab weitermachen. |
| „Noch kein Abo eingerichtet – das geht über die Zahlungsseite." | Für dich gibt es noch kein Abo, also auch kein Portal. Der Knopf „Zahlungsseite" erscheint. | Über „Zahlungsseite" das Abo einrichten ([Abschnitt 7.2](#72-zahlungslink-und-abschluss-des-abos)). |
| „Noch kein Abo eingerichtet – bitte beim Betreiber melden." | Wie oben, aber der Link zur Zahlungsseite ist nicht bekannt. | Betreiber nach deinem Zahlungslink fragen. |
| „Bitte <N> Sekunden warten." | Zu viele Klicks kurz hintereinander. | Die Zeit abwarten, dann noch einmal. |
| „Server nicht erreichbar – bitte später erneut versuchen." | Keine Verbindung zum Server. | Internet prüfen, später erneut. |
| „Kundenportal gerade nicht erreichbar – bitte später erneut versuchen." | Der Server konnte das Portal gerade nicht öffnen, oder der Hintergrunddienst hat nicht geantwortet. | Später erneut. Bleibt es dauerhaft, Chrome komplett neu starten ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)), dann Betreiber fragen. |
| „Nicht angemeldet." | Du bist nicht (mehr) angemeldet. | Neu anmelden. |
| ein Text des Betreibers oder „Zugang gesperrt." | Zugang abgeschaltet oder Abo gesperrt. | [Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet) bzw. Betreiber fragen. |

**Ohne Dashboard ins Portal:** Öffnest du deinen Zahlungslink, während dein Abo läuft, gibt es dort den Knopf „Zahlungsart ändern, Rechnungen, kündigen". Dort meldest du dich über einen Link an, den du per E-Mail bekommst. Über „Abo verwalten" im Dashboard kommst du dagegen direkt hinein.

**Nicht im Kundenportal:** Shops hinzubuchen oder abbestellen. Das geht laut AGB per E-Mail beim Betreiber ([Abschnitt 7.7](#77-kündigen-shops-ändern-vertragsende)).

### 7.5 Warnungen bei offener Zahlung

Ist eine Zahlung offen oder droht eine Sperre, zeigt das Dashboard **oben unter der Überschrift eine farbige Warnleiste** und denselben Hinweis **als ersten Eintrag in der Glocke** oben rechts. Die Leiste hat einen Knopf, der deine Zahlungsseite in einem neuen Tab öffnet (nur wenn der Link bekannt ist). Ist der Link bekannt, führt auch der Eintrag in der Glocke per Klick dorthin.

| Titel | Text | Knopf |
|---|---|---|
| „Zahlung offen" | „Ohne Zahlung wird dein Zugang nach dem <Datum> gesperrt." bzw., wenn der Tag erreicht ist, „Die Sperre ist fällig – bitte jetzt bezahlen." | „Jetzt bezahlen" |
| „Zahlung überfällig" | „Die Abbuchung hat nicht geklappt." + derselbe Satz zur Sperre | „Jetzt bezahlen" |
| „Erste Zahlung fehlgeschlagen" | „Die erste Abbuchung hat nicht geklappt." + derselbe Satz zur Sperre | „Jetzt bezahlen" |
| „Abo gesperrt" | „Ein Shop deines Abos ist wegen einer offenen Zahlung gesperrt." | „Jetzt bezahlen" |
| „Noch kein Abo eingerichtet" bzw. „Abo beendet" | „Dein Zugang läuft bis <Datum>. Richte das Abo auf der Zahlungsseite ein, damit es weitergeht." bzw. „Dein Zugang ist abgelaufen. Richte das Abo …" | „Abo einrichten" |

Die Warnung „Noch kein Abo eingerichtet"/„Abo beendet" erscheint erst etwa eine Woche vor dem Ende deines Zugangs. Bei „Zahlung offen", „Noch kein Abo eingerichtet" und „Abo beendet" ist die Leiste zunächst orange und wird rot, wenn weniger als etwa zwei Tage bleiben. „Zahlung überfällig", „Erste Zahlung fehlgeschlagen" und „Abo gesperrt" sind immer rot.

**Wann wird gesperrt?** Laut AGB (§ 6) kann der Zugang gesperrt werden, wenn das Entgelt **drei Tage nach Fälligkeit** nicht bezahlt ist. Bei SEPA-Lastschrift wartet der Betreiber, solange der Einzug läuft und kein Fehlschlag bekannt ist, bis zu zwei weitere Wochen. Schlägt ein Einzug nach diesen drei Tagen fehl, kann sofort gesperrt werden. **Den Tag, ab dem gesperrt wird, nennt dir das Dashboard** („Ohne Zahlung wird dein Zugang nach dem <Datum> gesperrt.") und die Statuszeile der Karte „Dein Abo"; laut AGB zeigt ihn auch deine Zahlungsseite.

**So bezahlst du:**
1. In der Warnleiste auf „Jetzt bezahlen" klicken (oder in der Karte „Dein Abo" auf „Zahlungsseite").
2. Auf der Zahlungsseite den passenden Knopf nehmen, z. B. „Offene Rechnung bezahlen", falls er angezeigt wird.
3. Hat eine Abbuchung nicht geklappt, weil die Karte abgelaufen ist oder das Konto nicht gedeckt war: über „Abo verwalten" im Kundenportal die Zahlungsart prüfen bzw. ändern.
4. Zurück im Dashboard-Tab holt das Dashboard den Stand neu.

### 7.6 Abo-Sperre: was passiert und wie sie endet

**Was du bei einer Sperre siehst:**
- Unten in der Seitenleiste: roter Punkt, „Abo gesperrt", „Details im Dashboard", „Produkt-Vergabe aus". Alle Module außer Dashboard und Einstellungen sind grau.
- Im Dashboard: die Anmeldekarte mit der Überschrift **„Abo gesperrt"** und dem Text des Betreibers, z. B. „Abo abgelaufen – bitte die Zahlung erneuern oder beim Betreiber melden." (ohne eigenen Text: „Bitte die Zahlung erneuern oder beim Betreiber melden."). Ist dein Zahlungslink bekannt, steht darunter der Knopf **„Zur Zahlungsseite"** mit dem Hinweis „Nach der Zahlung hier wieder anmelden.".
- In der Zeile unter der Überschrift „… · Abo gesperrt", im Kontofeld „Abo gesperrt".
- Versuchst du dich anzumelden: „Anmeldung abgelehnt: Abo gesperrt.".
- In Modulen z. B. „Abo gesperrt – bitte im Dashboard nachsehen.". Der Browser-Lister beendet seinen Lauf mit einem Hinweis, Module lassen sich nicht mehr öffnen oder starten.
- Auch das Update-Programm kann sich während einer Sperre nicht anmelden (unter Windows erscheint dann „Server nicht erreichbar (…)", auf dem Mac „Anmeldung fehlgeschlagen (HTTP 402)."). Erst bezahlen, dann aktualisieren.

**Was erhalten bleibt (laut AGB § 6):** dein Benutzerkonto, deine gesicherten Einstellungen und die Zuteilungen der Produkte, die du schon bei eBay anbietest. Reservierte, noch nicht angebotene Produkte können bei einer längeren Sperre freigegeben werden (Einzelheiten in den AGB, § 6 und § 8). Deine Einstellungen in Chrome bleiben ohnehin unberührt. Das offene Entgelt bleibt geschuldet.

**So endet die Sperre:**
1. Im Dashboard auf „Zur Zahlungsseite" klicken (oder deinen Zahlungslink aus der Nachricht des Betreibers öffnen).
2. Die offene Zahlung erledigen.
3. Laut AGB hebt der Betreiber die Sperre nach Eingang der Zahlung unverzüglich auf, **in der Regel automatisch**.
4. Danach im Dashboard **neu anmelden** (Name und Passwort oder „Einrichtungsdatei einlesen").
5. Kommt beim Anmelden weiterhin „Anmeldung abgelehnt: Abo gesperrt.", ist die Zahlung noch nicht angekommen. Etwas später erneut versuchen. Bleibt es, Betreiber fragen.

**Nicht sicher belegt:** Wie schnell die Sperre nach einer Zahlung aufgehoben ist (bei Karte vermutlich schneller als bei Lastschrift). Frag im Zweifel den Betreiber.

Steht in der Sperr-Karte **kein** Knopf „Zur Zahlungsseite": Dann kennt die Extension deinen Link nicht. Nimm den Link aus der Nachricht des Betreibers oder frag ihn danach.

### 7.7 Kündigen, Shops ändern, Vertragsende

**Kündigen (laut AGB § 7):**
- Jederzeit zum **Ende des laufenden Abrechnungszeitraums**, in Textform.
- Am einfachsten über **„Abo verwalten"** im Dashboard (Kundenportal) oder per E-Mail an die Adresse im Impressum.
- Der Betreiber bestätigt die Kündigung mit dem Tag, an dem der Vertrag endet. Für den laufenden Zeitraum gezahlte Beträge werden bei einer normalen Kündigung nicht anteilig erstattet.
- Im Dashboard zeigt die Karte danach „gekündigt" und „Gekündigt zum <Datum>". Bis dahin arbeitest du normal weiter.

**Shops hinzubuchen oder abbestellen:** Laut AGB per E-Mail beim Betreiber. Für den Rest des laufenden Zeitraums wird anteilig verrechnet. Bestellst du alle Shops ab, gilt das als Kündigung.

**Nach dem Vertragsende:**
- Laut AGB sperrt der Betreiber dann den Zugang; die Software kann nicht mehr genutzt werden.
- Deine Einstellungen kannst du vorher jederzeit über „Einstellungen exportieren" sichern ([Abschnitt 10](#10-einstellungen-als-datei-exportieren-und-importieren)).
- Laut AGB kannst du während der Laufzeit und bis 30 Tage nach Vertragsende per E-Mail eine Kopie der Daten anfordern, die zu deinem Konto auf dem Server liegen (z. B. gesicherte Einstellungen und die Liste deiner zugeteilten Produkte). Danach werden sie gelöscht, soweit nichts aufbewahrt werden muss.

### 7.8 Webseite mit AGB, Datenschutz und Impressum

Die Webseite von Cash Lister ist **https://cash-lister.de**. Unten auf der Seite stehen die Links **„Impressum"**, **„Datenschutz"** und **„AGB"**. Dort findest du:
- die **AGB** (Allgemeine Geschäftsbedingungen, nur für Unternehmer) mit Preisen, Zahlung, Sperre, Kündigung und Produkt-Zuteilung,
- die **Datenschutzerklärung**,
- das **Impressum** mit den Kontaktangaben des Betreibers.

Die Fassung der AGB, die bei deinem Abschluss gilt, ist im Bestellvorgang verlinkt.

### Häufige Fragen zum Abo

**Was kostet Cash Lister?**
150 € pro Monat für den ersten Shop, 50 € für jeden weiteren, jeweils zzgl. 19 % USt ([Abschnitt 7.1](#71-preise-und-ablauf-im-überblick)). OpenAI und eBay-Gebühren kommen dazu.

**Ich sehe keine Karte „Dein Abo".**
Sie erscheint nur angemeldet und nur, wenn für dein Konto ein Abo abgerechnet wird. Direkt nach dem Öffnen kann sie einen Moment fehlen, bis der Stand geladen ist. Fehlt sie dauerhaft, obwohl du zahlst: Chrome komplett neu starten ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)), sonst Betreiber fragen.

**Wo bekomme ich meine Rechnungen?**
Als PDF per E-Mail oder im Kundenportal: Dashboard → Karte „Dein Abo" → „Abo verwalten".

**Wie ändere ich meine Karte oder mein Bankkonto?**
Dashboard → „Dein Abo" → „Abo verwalten" → im Kundenportal die Zahlungsart ändern.

**Wie kündige ich?**
Dashboard → „Dein Abo" → „Abo verwalten" → im Kundenportal kündigen. Oder per E-Mail an die Adresse im Impressum. Die Kündigung wirkt zum Ende des laufenden Abrechnungszeitraums.

**Kann ich das Abo pausieren?**
**Nicht sicher belegt:** Eine Pause ist weder in der Extension noch in den AGB beschrieben. Frag den Betreiber.

**Kann ich als Privatperson abschließen?**
Laut AGB nein, Cash Lister wird nur Unternehmern angeboten.

**Ich habe bezahlt, bin aber immer noch gesperrt.**
Siehe [Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet), Schritt 4 und 5: neu anmelden; geht es nicht, etwas warten und dann den Betreiber fragen.

**Ich habe den Zahlungslink verloren.**
Ist er dem Dashboard bekannt, findest du ihn in der Karte „Dein Abo" („Zahlungsseite"), in der Warnleiste oder in der Sperr-Karte („Zur Zahlungsseite"). Sonst den Betreiber fragen.

### Probleme und Lösungen beim Abo

| Problem | Lösung |
|---|---|
| „Abo verwalten" öffnet nichts | Meldung unter dem Knopf lesen (Tabelle in [Abschnitt 7.4](#74-abo-verwalten-das-kundenportal)). Wurde ein neuer Tab blockiert? Prüfe, ob Chrome den Tab im Hintergrund geöffnet hat. |
| „Kundenportal gerade nicht erreichbar …" kommt immer wieder | Chrome komplett neu starten ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)), dann erneut. Bleibt es: Betreiber. |
| Die Karte zeigt noch den alten Stand, obwohl ich gerade bezahlt habe | Das Dashboard neu laden (F5). Bei SEPA-Lastschrift steht erst nach einigen Werktagen fest, ob der Einzug geklappt hat („Zahlung unterwegs"). |
| Warnleiste „Zahlung offen", aber kein Knopf „Jetzt bezahlen" | Der Link ist dem Dashboard nicht bekannt. Link aus der Nachricht des Betreibers nehmen oder ihn fragen. |
| Anmelden geht nicht: „Anmeldung abgelehnt: Abo gesperrt." | [Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet). |
| `update.bat` meldet „Server nicht erreichbar", obwohl Internet geht | Auch ein gesperrtes Abo kann dahinterstecken. Im Dashboard nachsehen, ob „Abo gesperrt" steht. Sonst [Abschnitt 12](#12-updates-unter-windows). |

---

## 8. Produkt-Datenbank: jetzt je Konto auf dem Server

Die Bedienung der Produkt-Datenbank steht im Bereich Produkt-Datenbank (`references/produkte-finden-und-datenbank.md`). Hier nur, was mit Konto, Anmeldung und Sicherung zu tun hat:

- **Seit 46.0 liegt die Produkt-Datenbank auf dem Server, eine je Konto.** Alle Geräte und Chrome-Profile, die mit demselben Konto angemeldet sind, sehen dieselbe Liste. Produkte, die gerade ein Lister bearbeitet, stehen in der Spalte „In Arbeit"; jedes Gerät bekommt andere Produkte.
- **Erster Start nach dem Update:** Sobald du angemeldet bist, lädt die Extension die bisherige Liste dieses Chrome-Profils **automatisch** auf den Server hoch. Solange das läuft, steht in der Produkt-Datenbank „<N> Produkte werden noch auf den Server übertragen …" und im Dashboard „… werden noch auf den Server übertragen". Produkte, die laut deinen Google-Tabellen schon gelistet sind, und Produkte, die einem anderen Kunden gehören, werden dabei aussortiert. Bist du nicht angemeldet oder ist der Server nicht erreichbar, wartet der Rest und wird beim nächsten Anlass übertragen. Dann steht dort „<N> Produkte dieses Geräts warten darauf, nach der Anmeldung auf den Server übertragen zu werden." bzw. „… warten darauf, sobald der Server erreichbar ist, auf den Server übertragen zu werden.".
- **Ohne Anmeldung** gibt es keine Liste (im Dashboard „nach der Anmeldung sichtbar").
- **Ohne Server** nehmen die Lister keine Produkte aus der Datenbank: Ein laufender Browser-Lister pausiert („Server nicht erreichbar – Lister pausiert, macht von selbst weiter") und macht von selbst weiter, sobald der Server wieder antwortet. Willst du ihn ohne Server starten, kommt „Server nicht erreichbar - die Produkt-Datenbank liegt auf dem Server. Bitte später erneut starten.". Ein Import scheitert mit einer Meldung, z. B. „Nichts importiert – Server nicht erreichbar. Bitte später erneut versuchen.".
- **„Alle löschen"** in der Produkt-Datenbank fragt vorher „Wirklich ALLE Produkte aus der Datenbank löschen? Das gilt für alle Geräte deines Kontos – die Liste ist danach überall leer." Produkte, die gerade in Arbeit sind (auf diesem oder einem anderen Gerät), bleiben dabei stehen; das meldet die Seite z. B. mit „<N> Produkte sind gerade in Arbeit und bleiben stehen (einzeln mit ✕ löschbar).".
- **Abmelden, Neuinstallation, neuer PC:** Die Liste bleibt auf dem Server und ist nach der Anmeldung mit demselben Konto wieder da.
- **Export-Datei und Einstellungs-Sicherung enthalten die Produkt-Datenbank nicht mehr.** Sie liegt ohnehin auf dem Server.
- **Ältere Export-Datei mit Produkt-Datenbank importieren:** Steckt in einer älteren Export-Datei noch eine Produkt-Datenbank, lädt die Extension diese Produkte nach dem Import (und nach der Anmeldung) von selbst in deine Produkt-Datenbank auf dem Server hoch. Die vorhandene Liste wird dabei **nicht ersetzt**, sondern ergänzt; Doppelte, schon gelistete und anderweitig vergebene Produkte werden aussortiert.
- Die **Sortierung** der Produkt-Datenbank gilt je Gerät und wird nicht gesichert.

---

## 9. Einstellungs-Sicherung auf dem Server

Damit deine Einstellungen nicht verloren gehen, wenn die Extension aus Chrome verschwindet oder du ein neues Gerät einrichtest, legt Cash Lister **je Konto eine Kopie deiner Einstellungen auf dem Server** ab. Du musst dafür normalerweise nichts tun.

Bedient wird die Sicherung in den **Einstellungen → Reiter „Sicherung" → Karte „Auf dem Server"** (Zusatz „für dein Konto · nur mit Anmeldung"). Dort stehen der Text „Mit Anmeldung werden deine Einstellungen von selbst auf dem Server gesichert – ohne Schlüssel und Produkt-Datenbank.", die Knöpfe „Einstellungen vom Server holen" und (nur bei einem Konflikt) „Dieses Gerät auf den Server sichern", der Hinweis „„Einstellungen vom Server holen" ersetzt die Einstellungen auf diesem Gerät; Schlüssel und Produkt-Datenbank bleiben." und darunter die Statuszeile.

### Wie die automatische Sicherung läuft

- Solange du **angemeldet** bist, merkt die Extension jede Änderung an einer gesicherten Einstellung, egal auf welcher Seite du sie machst (Einstellungen, Module).
- Etwa **30 Sekunden nach der letzten Änderung** geht der ganze Satz an den Server, aber nur, wenn sich wirklich etwas geändert hat.
- Zusätzlich wird nach jeder Installation bzw. jedem Update (nach etwa 1 Minute), bei jedem Chrome-Start (nach etwa 2 Minuten) und direkt nach dem Anmelden einmal geprüft.
- Ist der Server nicht erreichbar, versucht es die Extension später automatisch noch einmal (alle 30 Minuten, höchstens etwa einen Tag lang, dazu bei jedem Chrome-Start).
- Abgemeldet wird nichts gesichert.

### Was gesichert wird und was nicht

**Gesichert (auf dem Server):**
- Reiter „Preise & Listing": Preise (Aufschläge, Preisspannen, „Neu: Sonstige"-Haken, „Preisendung" samt Schalter), „Domain", „Listing automatisch absenden", „Anzeigengebühr (%)", die beiden Schalter „Pflicht-Artikelmerkmale mit KI ausfüllen" und „Optionale Artikelmerkmale mit KI ausfüllen"
- Reiter „Produkt-Filter": „Nur FBA", „Nur chinesische Verkäufer", „GPSR-Angaben übernehmen", „Markenlos listen", „Bildabgleich gegen fremde Angebote", „Nur Verkauf durch Amazon", die **Zahlen** bei „Max. verlängerte Lieferzeit", „Preis ab" und „Preis bis", die Blacklist („Meine Liste")
- Reiter „eBay & Rahmenbedingungen": die Karte „Rahmenbedingungen" („Versand", „Zahlung", „Rücknahme", „Artikelstandort (Ort oder PLZ)"), „Auch mit Angebotsgebühr einstellen", „Nur ein Bild bei eBay einstellen", „Mehrwertsteuer im Angebot angeben", „Mehrwertsteuersatz", „Zustandsbeschreibung", eine ggf. eingetragene eigene „Server-Adresse", „Beenden-CSV für Duplikate erstellen"
- Reiter „Beschreibungsvorlage": die Vorlage
- Reiter „KI": nur die **Auswahl** bei „OpenAI-Modell", nicht der Schlüssel
- Einstellungen des Browser-Listers (z. B. Quelle, Zeitschaltung, Zielzahl, Threads)
- Einstellungen des Trackers (z. B. Dauerbetrieb, Zeitlimit, Threads, Export-Einstellungen) und die **Adressen deiner Google-Tabellen**
- Einstellungen der Verkaufs-Übersicht, des Konkurrenz-Scanners und des CSV-Listers
- dein Anmeldename (zur Anzeige)

**Nicht gesichert (bleibt nur auf dem Gerät):**
- **dein OpenAI-Schlüssel** und andere Schlüssel. Die gehen nie auf den Server. Nach einer Neuinstallation musst du den OpenAI-Schlüssel neu eintragen (oder aus deiner Export-Datei holen).
- dein Passwort und deine Anmeldung selbst
- die Filter „Mind. Sterne", „Mind. Bewertungen" und „Mind. Lagerbestand" (Zahl und Schalter) sowie die **Ein/Aus-Schalter aller Amazon-Filter**. Beim ersten Öffnen der Einstellungen nach einer Neuinstallation werden die fehlenden Schalter aus den Zahlen abgeleitet: Steht im Feld eine Zahl über 0, ist der Filter an. Das betrifft vor allem „Max. verlängerte Lieferzeit" (steht ohne gespeicherte Zahl auf 20 und ist dann an) sowie „Preis ab" und „Preis bis", wenn dort eine Zahl über 0 gesichert war. Prüfe diese Filter danach von Hand.
- die Karte „Server-Modus" (Reiter „eBay & Rahmenbedingungen"), also der Schalter „Dieses Gerät ist ein Server" und der „Gerätename". Sie gilt nur für das eine Gerät.
- die Sortierung der Produkt-Datenbank (gilt je Gerät)
- laufende Zustände (Fortschritt, Zähler, geöffnete Läufe) und die geladenen Daten der Module (z. B. eingelesene Berichte der Verkaufs-Übersicht, die geladene Datei im Tracker)
- die gemerkten Konkurrenten des Konkurrenz-Scanners
- die Liste, die sich die Extension auf diesem Gerät über bereits gelistete Produkte führt. Sie dient einer Doppel-Prüfung direkt vor dem Listen. Nach einer Neuinstallation ist sie leer. Schlägt sie an, steht beim Produkt „Produkt ist schon gelistet (Duplikat)". Unabhängig davon laufen weiter: die Produkt-Vergabe und der Abgleich mit deinen Google-Tabellen, der beim Übernehmen in die Produkt-Datenbank schon gelistete Produkte aussortiert.
  **Nicht sicher belegt:** Ob diese Prüfungen jedes früher gelistete Produkt sicher abfangen.

Die **Produkt-Datenbank** wird hier nicht gesichert, weil sie seit 46.0 selbst auf dem Server liegt ([Abschnitt 8](#8-produkt-datenbank-jetzt-je-konto-auf-dem-server)).

Gesichert wird **je Konto**, nicht je Gerät. Es gibt auf dem Server also genau **einen** Einstellungsstand für dein Konto.

### Größenbeschränkung

Der gesicherte Satz darf höchstens 512 KB groß sein. Ist er größer, wird nichts gesendet, und in der Statuszeile steht „ · Aktueller Stand zu groß für die Sicherung (<N> KB, erlaubt 512 KB) – Vorlagen oder Bild-Templates kürzen.". Am ehesten machen eine sehr lange Beschreibungsvorlage oder eine sehr lange Blacklist den Satz so groß.
**Nicht sicher belegt:** Welcher Teil bei dir die Größe verursacht.

### Die Statuszeile (Reiter „Sicherung")

Die Zeile wird aktualisiert, wenn du die Einstellungen öffnest, wenn du in ihren Tab zurückwechselst und wenn die Extension einen neuen Konflikt bemerkt.

| Text | Bedeutung |
|---|---|
| „Auf dem Server gesichert: <Datum, Uhrzeit>" | Letzte erfolgreiche Sicherung dieses Geräts. |
| „Noch nicht auf dem Server gesichert." | Von diesem Gerät liegt noch keine Sicherung vor (z. B. direkt nach der ersten Anmeldung, oder der Server war nicht erreichbar). Normalerweise erledigt sich das von selbst. |
| „ · Aktueller Stand zu groß für die Sicherung (…)" | Siehe oben „Größenbeschränkung". |
| „ · Vom Server übernommen: <Datum, Uhrzeit>" | Die Extension hat deine Einstellungen vom Server zurückgeholt. Wird einmal angezeigt. |
| „Achtung: Auf dem Server liegt eine Sicherung vom <Datum> mit <N> Einstellungen von einem anderen Gerät. Dieses Gerät hat <M> Einstellungen und wurde noch nicht gesichert. Bitte entscheiden: "Einstellungen vom Server holen" oder "Dieses Gerät auf den Server sichern"." | **Konflikt**, siehe unten. Bis du entscheidest, wird nichts gesendet und nichts überschrieben. (Der Zusatz „von einem anderen Gerät" fehlt, wenn nicht feststeht, von welchem Gerät die Sicherung stammt.) |
| (leer) | Du bist nicht angemeldet, oder der Hintergrunddienst hat nicht geantwortet. |

**Auch im Dashboard** siehst du den Stand: In der Karte „Heute" gibt es die Zeile „Einstellungen gesichert" mit z. B. „Zuletzt <Zeit> auf dem Server", „Noch nicht gesichert", „Server nicht erreicht – wird wiederholt", „Zu groß für die Sicherung (<N> KB)", „Erst nach der Anmeldung" oder „Ein anderes Gerät hat anders gesichert – unter Einstellungen → Sicherung entscheiden". Bei einem Konflikt erscheint außerdem in der Glocke „Einstellungen: zwei Geräte" („Ein anderes Gerät hat anders gesichert. Unter Einstellungen → Sicherung entscheiden, welcher Stand gilt."). Ein Klick darauf öffnet die Einstellungen; dort auf den Reiter „Sicherung" klicken. Bei „zu groß" steht in der Glocke „Einstellungen zu groß für die Sicherung".

### Neues Gerät oder Neuinstallation: automatisches Zurückholen

Wenn du die Extension neu installierst (neuer Computer, neues Chrome-Profil oder nach „Entfernen" und neu laden) und dich anmeldest, sieht die Extension beim Server nach:

1. Liegt dort eine Sicherung und dieses Gerät ist **frisch installiert** bzw. hat noch kaum eigene Einstellungen, werden die gesicherten Einstellungen **automatisch übernommen**. Beim nächsten Öffnen der Einstellungen steht im Reiter „Sicherung" „Vom Server übernommen: …".
2. Stimmen die Einstellungen auf beiden Seiten schon überein, passiert nichts weiter.
3. Hat dieses Gerät dagegen schon **eigene** Einstellungen, die sich von der Sicherung unterscheiden, wird **nichts automatisch überschrieben**. Es entsteht ein **Konflikt**, und du entscheidest.

Danach: offene Tabs von Cash Lister (Einstellungen, Module) neu laden, damit überall die übernommenen Werte angezeigt werden. Den OpenAI-Schlüssel neu eintragen und die Amazon-Filter prüfen (siehe „Nicht gesichert"). Die Produkt-Datenbank ist ohnehin auf dem Server.

### Konflikt lösen (zwei Geräte, ein Konto)

Ein Konflikt entsteht nur bei der **ersten** Sicherung eines Geräts für dein Konto, oder wenn dein Gerät deutlich weniger Einstellungen hat als die Sicherung eines anderen Geräts. (Damit soll ein fast leerer Stand eine volle Sicherung nicht still ersetzen.)

1. Einstellungen öffnen → Reiter **„Sicherung"**. Die Statuszeile zeigt den „Achtung: …"-Text mit beiden Ständen (Datum und Anzahl).
2. Entscheiden:
   - **Die Einstellungen auf dem Server sind die richtigen** → Knopf **„Einstellungen vom Server holen"** → Rückfrage bestätigen. Die Einstellungen dieses Geräts werden ersetzt.
   - **Die Einstellungen auf diesem Gerät sind die richtigen** → Knopf **„Dieses Gerät auf den Server sichern"** → Rückfrage „Die Sicherung auf dem Server (<N> Einstellungen vom <Datum>) wird durch die <M> Einstellungen dieses Geräts ersetzt. Fortfahren?" bestätigen. Während des Sicherns steht dort „Sichere …".
3. Danach verschwindet der Konflikt, und die automatische Sicherung läuft wieder.

### Wichtig bei zwei Geräten (oder zwei Chrome-Profilen) mit demselben Konto

- Nach der ersten Entscheidung gilt: **Was zuletzt gesichert wurde, gilt auf dem Server.** Änderst du auf Gerät A etwas, landet A's ganzer Einstellungssatz etwa 30 Sekunden später auf dem Server. Änderst du danach auf Gerät B etwas, ersetzt B's Satz den von A.
- **Die Einstellungen der Geräte gleichen sich nicht von selbst ab.** Gerät B bekommt Änderungen von A nur, wenn du auf B „Einstellungen vom Server holen" klickst. (Die Produkt-Datenbank ist dagegen immer für alle Geräte dieselbe.)
- Praktisch heißt das: Richte ein Gerät als „Haupt-Gerät" ein. Auf dem anderen holst du bei Bedarf die Einstellungen vom Server.
- **Verschiedene Shops mit demselben Konto in verschiedenen Chrome-Profilen:** Falls du das so nutzt, liegt auf dem Server trotzdem nur **ein** Stand, nämlich der zuletzt gesicherte, inklusive der **Google-Tabellen-Adressen** eines Shops. Holst du in einem Profil die Einstellungen vom Server, oder holt die Extension sie nach einer Neuinstallation automatisch, bekommst du womöglich die Einstellungen des **anderen** Shops. Prüfe danach unbedingt die Tabellen-Adressen im Tracker und deine Preise.
- Meldet sich im selben Chrome-Profil ein **anderes** Konto an, beginnt die Sicherung für dieses Konto von vorn (mit derselben Konflikt-Prüfung). Abmelden allein ändert an der Sicherung nichts.

### „Einstellungen vom Server holen": Ablauf und Meldungen

Den Knopf kannst du jederzeit benutzen, nicht nur bei einem Konflikt.

1. Einstellungen → Reiter „Sicherung" → Karte „Auf dem Server" → **„Einstellungen vom Server holen"**.
2. Die Statuszeile zeigt „Frage den Server …".
3. Liegt eine Sicherung vor, fragt ein Fenster:
   „Einstellungen vom Server übernehmen?
   Server: <Datum> (<N> Einstellungen)
   Dieses Gerät: <M> Einstellungen
   Die Einstellungen auf diesem Gerät werden ersetzt. Schlüssel (OpenAI usw.) und die Produkt-Datenbank bleiben."
4. Mit „OK" bestätigen. Danach steht dort „Übernommen (<N> Einstellungen). Lade offene Seiten von Cash Lister bitte neu."
5. Die Einstellungsseite und offene Modul-Tabs neu laden.

Wichtig: „Ersetzt" heißt wirklich ersetzt. Gesicherte Einstellungen, die in der Server-Sicherung **nicht** vorkommen, werden auf diesem Gerät gelöscht und stehen danach wieder auf ihrer Vorgabe.

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Auf dem Server liegt noch keine Sicherung für dieses Konto." | Für dein Konto wurde noch nie etwas gesichert | Nichts zu holen. Die Sicherung entsteht automatisch, sobald du angemeldet etwas änderst. |
| „Nicht möglich: Server nicht erreichbar" | Keine Verbindung | Internet prüfen, später erneut versuchen. |
| „Nicht möglich: nicht angemeldet" | Du bist nicht (mehr) angemeldet | Im Dashboard neu anmelden. |
| „Nicht möglich: HTTP …" | Der Server hat die Anfrage abgelehnt | Abmelden, neu anmelden, erneut versuchen. Bleibt es: Betreiber mit der Meldung informieren. Prüfe auch, ob dein Abo gesperrt ist. |
| „Nicht möglich: keine Antwort" oder „Nicht möglich: …" mit einem englischen Text, z. B. „A listener indicated an asynchronous response …" | Meist läuft der Hintergrunddienst der Extension noch mit einer alten Version (typisch nach einem Update ohne Chrome-Neustart) | Chrome komplett schließen und neu starten bzw. die Extension neu laden ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)), dann erneut versuchen. |
| „Übernehmen fehlgeschlagen." | Beim Schreiben in Chrome ging etwas schief | Chrome neu starten, erneut versuchen. |
| „Sichern fehlgeschlagen: …" (beim Knopf „Dieses Gerät auf den Server sichern") | Z. B. „Server nicht erreichbar", „zu gross", „nicht angemeldet", „HTTP …", „keine Antwort" | Je nach Grund: Verbindung prüfen, Satz verkleinern (siehe „Größenbeschränkung"), neu anmelden, bei „keine Antwort" Chrome komplett neu starten. |

### Häufige Fragen zur Sicherung

**Muss ich auf „Sichern" klicken?**
Nein. Die Sicherung läuft automatisch. Der Knopf „Dieses Gerät auf den Server sichern" ist nur für Konflikte da.

**Wo ist die Sicherung hin? Im Popup waren doch die Knöpfe.**
Das Popup gibt es seit 46.0 nicht mehr. Die Knöpfe stehen jetzt in den Einstellungen im Reiter „Sicherung".

**Ist mein OpenAI-Schlüssel auf dem Server?**
Nein, nie. Er bleibt nur auf deinem Gerät und steht zusätzlich in deiner Export-Datei, falls du eine erstellst.

**Ist meine Produkt-Datenbank gesichert?**
Sie liegt seit 46.0 selbst auf dem Server, je Konto ([Abschnitt 8](#8-produkt-datenbank-jetzt-je-konto-auf-dem-server)). In der Einstellungs-Sicherung und in der Export-Datei ist sie nicht enthalten. Eine eigene Kopie kannst du in der Produkt-Datenbank exportieren (siehe Bereich Produkt-Datenbank).

**Kann ich eine ältere Sicherung zurückholen?**
Auf dem Server liegt nur der letzte Stand.
**Nicht sicher belegt:** Ob der Betreiber ältere Stände aufbewahrt. Für eigene Zwischenstände: regelmäßig „Einstellungen exportieren".

**Werden die Adressen meiner Google-Tabellen gesichert?**
Ja, sie gehören zu den gesicherten Einstellungen. Damit musst du sie nach einer Neuinstallation nicht neu eintragen.

---

## 10. Einstellungen als Datei exportieren und importieren

Die Export-Datei ist deine **persönliche Sicherung**, z. B. für einen Rechnerwechsel oder als Notfall-Kopie. Sie ergänzt die Server-Sicherung, weil sie auch deine Schlüssel enthält.

Du findest Export und Import in den **Einstellungen → Reiter „Sicherung" → Karte „Als Datei"** (Zusatz „z. B. für einen Rechnerwechsel"). Dort steht ein Warnkasten „Enthält API-Schlüssel und Lizenz – nicht weitergeben.".

### Exportieren

1. Einstellungen → Reiter „Sicherung" → **„Einstellungen exportieren"**.
2. Chrome lädt die Datei `einstellungen-privat-<Datum>.json` herunter (Datum in der Form Jahr-Monat-Tag; sie landet dort, wo Chrome Downloads ablegt, normalerweise im Download-Ordner).
3. Datei an einem sicheren Ort aufbewahren.

**Inhalt:** alle gesicherten Einstellungen (siehe [Abschnitt 9](#9-einstellungs-sicherung-auf-dem-server)), **dazu deine Schlüssel (OpenAI usw.)** und einige Arbeitsdaten (z. B. die gemerkten Konkurrenten des Konkurrenz-Scanners).

**Nicht enthalten:** dein Passwort und deine Anmeldung, die Filter „Mind. Sterne", „Mind. Bewertungen", „Mind. Lagerbestand" und die Ein/Aus-Schalter der Amazon-Filter, der „Server-Modus" und **die Produkt-Datenbank**.

**Achtung, Abweichung:** Auf der Seite steht noch „Der Export enthält alle Einstellungen, die Schlüssel und die Produkt-Datenbank." Seit 46.0 ist die Produkt-Datenbank aber nicht mehr in der Datei, weil sie auf dem Server liegt ([Abschnitt 8](#8-produkt-datenbank-jetzt-je-konto-auf-dem-server)).

**Die Datei niemals weitergeben.** Sie enthält deinen OpenAI-Schlüssel. Wer ihn hat, kann auf deine Kosten KI nutzen.

Empfehlung: Exportiere regelmäßig, besonders vor größeren Änderungen und bevor du an der Chrome-Installation etwas machst. Nur so lässt sich der OpenAI-Schlüssel nach einem Verlust einfach zurückholen.

### Importieren

1. Einstellungen → Reiter „Sicherung" → **„Einstellungen importieren"**.
2. Die `.json`-Datei wählen.
3. Ein Fenster meldet „Einstellungen importiert (<N> Einträge). Lade offene Seiten von Cash Lister (z. B. den Tracker) bitte neu.".
4. Die Einstellungsseite und offene Modul-Tabs neu laden.

**Achtung:**
- Der Import **ersetzt** auf diesem Gerät alles, was in der Datei steht. Werte, die in der Datei nicht vorkommen, bleiben unverändert.
- Weil sich dabei Einstellungen ändern, geht der neue Stand etwa 30 Sekunden später automatisch auf den Server (siehe [Abschnitt 9](#9-einstellungs-sicherung-auf-dem-server)), wenn du angemeldet bist.
- Enthält die Datei noch eine **Produkt-Datenbank** (ältere Export-Dateien), werden diese Produkte nicht lokal eingespielt, sondern nach der Anmeldung zu deiner Produkt-Datenbank auf dem Server **hinzugefügt** ([Abschnitt 8](#8-produkt-datenbank-jetzt-je-konto-auf-dem-server)).
- Für die **Einrichtungsdatei** vom Betreiber (mit Name und Passwort) nimm „Einrichtungsdatei einlesen" im Dashboard ([Abschnitt 5.3](#53-anmelden-mit-der-einrichtungsdatei)), nicht diesen Import. Dieser Import meldet dich nicht an.
- Der Import funktioniert auch ohne Anmeldung (die Einstellungen sind auch dann erreichbar).

Meldungen:

| Meldung | Bedeutung |
|---|---|
| „Einstellungen importiert (<N> Einträge). Lade offene Seiten von Cash Lister (z. B. den Tracker) bitte neu." | Erfolgreich. |
| „Ungültige Einstellungsdatei." | Die Datei hat nicht den erwarteten Aufbau. |
| „Die Datei ist kein gültiges JSON." | Die Datei ist beschädigt oder keine Einstellungsdatei. |
| „Import fehlgeschlagen: …" | Chrome konnte nicht speichern. Chrome neu starten und erneut versuchen. |

### Rechnerwechsel Schritt für Schritt

1. Auf dem alten Rechner: Einstellungen → Reiter „Sicherung" → „Einstellungen exportieren".
2. Auf dem neuen Rechner: Extension installieren ([Abschnitt 2](#2-installation-unter-windows-ersteinrichtung) bzw. [3](#3-installation-auf-dem-mac)).
3. Im Dashboard mit der Einrichtungsdatei anmelden. Die Server-Sicherung holt deine Einstellungen dabei wahrscheinlich schon automatisch, und die Produkt-Datenbank ist ohnehin auf dem Server.
4. Einstellungen öffnen → Reiter „Sicherung" → „Einstellungen importieren" mit der Export-Datei, damit auch der OpenAI-Schlüssel mitkommt. (Oder den Schlüssel im Reiter „KI" einfach neu eintragen.)
5. Einstellungen neu laden und prüfen: Reiter „Preise & Listing" (Domain, Preise), Reiter „Produkt-Filter" (Amazon-Filter und ihre Schalter), Reiter „KI" (Schlüssel).
6. Läuft der alte Rechner weiter mit demselben Konto, lies „Wichtig bei zwei Geräten" in [Abschnitt 9](#9-einstellungs-sicherung-auf-dem-server).

---

## 11. Erste Schritte nach der Anmeldung (Checkliste)

1. **Einstellungen öffnen** (Seitenleiste → „Einstellungen"). War der Einstellungs-Tab schon offen, neu laden, damit eventuell vom Server zurückgeholte Einstellungen angezeigt werden.
2. **Reiter „Preise & Listing":**
   - Karte „Listing": **„Domain"** auf deinen Marktplatz stellen (z. B. „DE"). „Keine" nicht wählen. Nach einer Neuinstallation steht dort normalerweise „DE", wenn deine Einrichtungsdatei oder die Server-Sicherung nichts anderes mitgebracht hat – trotzdem prüfen.
   - Karte „Preise": **„% Aufschlag"** (nach einer Neuinstallation steht dort zunächst 120 – unbedingt prüfen!), „Fester Aufschlag (€)", ggf. Preisspannen und „Neu: Sonstige", „Preisendung" prüfen. Mindestens einen Wert einmal ändern, damit die Preis-Einstellungen gespeichert sind; vorher rechnet der Tracker ohne Aufschlag.
   - „Listing automatisch absenden" und „Anzeigengebühr (%)" nach Wunsch.
3. **Reiter „Produkt-Filter":** Karte „Amazon-Filter" prüfen, besonders „Preis ab" und „Preis bis" und ihre Schalter, außerdem „Beim Listen" (z. B. „Nur FBA").
4. **Reiter „KI":** **„OpenAI-API-Schlüssel (für die Titel-Generierung)"** eintragen und bei „OpenAI-Modell (für KI-Beschreibung & Generierung)" ein Modell wählen (Vorgabe „gpt-4o-mini — Standard, günstig"). Ohne Schlüssel kann der Browser-Lister nicht listen.
5. **Reiter „eBay & Rahmenbedingungen":** Willst du den CSV-Lister nutzen, oben die Karte „Rahmenbedingungen" ausfüllen (Einzelheiten im Bereich Einstellungen). In der Karte „Server & Produkt-Vergabe" muss „● Produkt-Vergabe: AN (über deine Anmeldung)" stehen. Mit „Verbindung prüfen" testen. Steht dort „● Produkt-Vergabe: AUS – keine Server-Adresse hinterlegt.", bist du nicht angemeldet ([Abschnitt 6](#6-zugang-freischaltung-kosten-produkt-vergabe)). Das Feld „Server-Adresse" bleibt leer. Außerdem „Zustandsbeschreibung" und die übrigen Angaben nach Wunsch.
6. **Reiter „Beschreibungsvorlage":** nach Wunsch (leer lassen = schlichte Beschreibung aus dem Produkttext).
7. **Reiter „Sicherung":** einmal „Einstellungen exportieren" und die Datei sicher ablegen.
8. **Dashboard:** Prüfe die Karte „Dein Abo" ([Abschnitt 7.3](#73-die-karte-dein-abo-im-dashboard)).
9. Danach mit den Modulen loslegen. Die Bedienung steht in den Bereichen Produkt-Datenbank, Listen auf eBay, Tracker usw.

---

## 12. Updates unter Windows

Die Extension aktualisiert sich **nicht von selbst** und zeigt auch keinen Hinweis auf neue Versionen an. Du startest das Update selbst mit `update.bat`. Gibt es nichts Neues, sagt dir das Programm das einfach.
**Nicht sicher belegt:** Auf welchem Weg der Betreiber neue Versionen ankündigt. Frag ihn.

### So aktualisierst du

1. **Chrome komplett schließen**: alle Fenster aller Profile, **und** im Infobereich unten rechts in der Taskleiste nachsehen (ggf. über den kleinen Pfeil „^"). Siehst du dort das Chrome-Symbol: Rechtsklick → „Beenden". Siehe [Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren).
   Läuft gerade ein Lauf des Browser-Listers oder des Trackers, warte, bis er fertig ist, oder halte ihn vorher an.
2. Im Programmordner auf **`update.bat`** doppelklicken.
3. Ein schwarzes Fenster öffnet sich und zeigt, was passiert:
   - „Frage beim Server nach ..."
   - „Server: … (aus der Zugangsdatei)" oder „Server: … (aus dem Update-Paket)". Diese Zeile zeigt nur, mit welchem Server gesprochen wird.
   - „Melde an ..."
   - „(beim ersten Mal nach einer neuen Version dauert das bis zu 3 Minuten)". Hier bitte wirklich warten, das ist normal.
   - „Deine Version : 45.x" und „Auf dem Server: 46.0" (Beispiel)
   - Gibt es eine neue Version: „Lade Version 46.0 (… MB) ...", dann „Aktualisiert auf Version 46.0." und „Die vorherige Fassung liegt als 'extension_alt_<Datum>_<Uhrzeit>' daneben."
4. Am Ende steht eines von drei Ergebnissen:
   - „Fertig. Chrome jetzt wieder starten." → Update eingespielt.
   - „Du hast bereits die neueste Version." → Nichts zu tun.
   - „Update fehlgeschlagen - Meldungen oben. Deine alte Fassung ist unveraendert." → Meldung weiter oben lesen (Tabelle unten).
5. Eine Taste drücken, das Fenster schließt sich.
6. **Chrome wieder starten.** Damit lädt Chrome auch den Hintergrunddienst neu (siehe [Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)).
7. **Kontrolle:** Auf das Cash-Lister-Symbol klicken. Es muss sich das **Dashboard** öffnen (nicht ein kleines Fenster), unten in der Seitenleiste muss die neue Versionsnummer stehen („Version 46.0" oder höher, z. B. „Version 46.3"), und oben muss dein Name stehen. Steht dort die alte Nummer, öffnet sich noch das kleine Fenster oder benimmt sich etwas seltsam: [Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren) (Chrome komplett neu starten bzw. Extension neu laden, in jedem Chrome-Profil).

Deine Einstellungen, Schlüssel und deine Anmeldung bleiben bei einem Update erhalten, weil sie in Chrome liegen, nicht im Ordner. Die Produkt-Datenbank liegt auf dem Server.

### Was beim Update im Hintergrund passiert (einfach erklärt)

1. Das Programm sucht deine Einrichtungsdatei (`zugang.json` oder eine `.json`-Datei mit „einrichtung" oder „zugang" im Namen) neben `update.bat` und meldet sich damit an. Die Datei selbst wird nie verändert.
2. Es vergleicht deine Version mit der auf dem Server. Getauscht wird nur, wenn die Server-Version wirklich **neuer** ist.
3. Es lädt das neue Paket herunter, entpackt es zuerst in einen temporären Ordner und prüft, ob wirklich eine Extension drin ist.
4. **Erst dann** wird dein bisheriger Ordner `extension` in `extension_alt_<Datum>_<Uhrzeit>` umbenannt und die neue Fassung als `extension` eingesetzt. Bricht vorher etwas ab, bleibt alles, wie es war.
5. Nur die **letzte** vorherige Fassung bleibt als `extension_alt_…` liegen, ältere werden gelöscht.
6. Das Update-Programm hält sich selbst aktuell: Bringt das neue Paket eine neuere Fassung des Updaters mit, ersetzt es seine eigene `update.ps1` (die alte bleibt als `update.ps1.alt` liegen). Meldung dazu: „Updater erneuert (neue Fassung aus dem Update-Paket, die vorherige liegt als update.ps1.alt daneben)." `update.bat` selbst wird dabei nie ersetzt.

### Wenn Chrome noch läuft

Das Programm prüft vorher, ob Chrome läuft. Wenn ja, steht dort:
„Chrome laeuft noch.
Bitte Chrome KOMPLETT schliessen (auch im Infobereich unten rechts)."
und darunter „Drücken Sie eine beliebige Taste . . .". Schließe Chrome vollständig und drücke dann eine Taste, das Programm prüft erneut. Hilft das nicht: Task-Manager öffnen (Strg+Umschalt+Esc) → Reiter „Details" → alle Einträge `chrome.exe` beenden.

Warum das sein muss: Windows hält die Dateien der geladenen Extension offen. Ein Tausch bei laufendem Chrome kann auf halber Strecke abbrechen.

Steht im Fenster „[i] Chrome-Pruefung ist in der Einrichtungsdatei abgeschaltet.", ist diese Prüfung in deiner Einrichtungsdatei bewusst abgeschaltet. Dann musst du selbst dafür sorgen, dass Chrome wirklich komplett zu ist. Das Abschalten ist nicht empfohlen. Frag den Betreiber, falls du das nicht selbst eingerichtet hast.

### Alle Meldungen des Windows-Updates

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „FEHLER: Die Einrichtungsdatei fehlt. …" bzw. „FEHLER: Keine Zugangsdatei gefunden. Lege die Datei vom Betreiber (zugang.json oder leck-atakan-einrichtung-*.json) neben diese update.bat." | Die Einrichtungsdatei liegt nicht neben `update.bat` | Datei in den Programmordner legen (neben `update.bat`, nicht in `extension`). Der Name muss „zugang" oder „einrichtung" enthalten und auf `.json` enden. |
| „FEHLER: Im Ordner "extension" liegt keine Extension. Erwartet wird: …\extension\manifest.json" | Der Ordner `extension` fehlt oder ist leer, oder `update.bat` liegt am falschen Platz | Prüfen, ob `update.bat` direkt neben dem Ordner `extension` liegt. Fehlt `extension`, aber es gibt `extension_alt_…`: siehe [Abschnitt 16](#16-zurück-zur-vorherigen-version). |
| „FEHLER: <Datei> ist nicht lesbar: …" | Die Einrichtungsdatei ist beschädigt | Neue Einrichtungsdatei beim Betreiber anfordern. Nicht mit einem Textprogramm bearbeiten. |
| „FEHLER: In der <Datei> fehlen Angaben (…)." | Name oder Passwort fehlen in der Datei (z. B. eine eigene Export-Datei statt der Einrichtungsdatei, oder eine andere `.json`-Datei mit „zugang" oder „einrichtung" im Namen liegt im Ordner) | Die richtige Einrichtungsdatei vom Betreiber verwenden. Andere `.json`-Dateien mit diesen Wörtern im Namen aus dem Ordner nehmen. |
| „FEHLER: Keine Serveradresse gefunden - …" | Weder Einrichtungsdatei noch Extension-Ordner nennen einen Server | Betreiber fragen (neue Einrichtungsdatei). |
| „Hinweis: … ist nicht lesbar (…) - nehme die Adresse aus der Zugangsdatei." | Nur ein Hinweis, das Update läuft weiter | Nichts. Scheitert es danach mit „Server nicht erreichbar", Betreiber fragen. |
| „FEHLER: Name oder Passwort stimmen nicht. Bitte beim Betreiber melden." | Die Zugangsdaten in der Einrichtungsdatei sind veraltet | Neue Einrichtungsdatei beim Betreiber anfordern. |
| „FEHLER: Dein Zugang ist abgeschaltet. Bitte beim Betreiber melden." | Zugang abgeschaltet | Betreiber kontaktieren. |
| „FEHLER: Zu viele Versuche. Bitte ein paar Minuten warten." | Kurzzeitige Sperre nach mehreren Fehlversuchen | Ein paar Minuten warten, erneut starten. |
| „FEHLER: Server nicht erreichbar (…). Internetverbindung pruefen." | Keine Verbindung zum Server – **oder dein Abo ist gesperrt** (das Update-Programm zeigt eine Abo-Sperre ebenfalls so an) | Internet prüfen, VPN/Firewall/Virenscanner prüfen, später erneut. Im Dashboard nachsehen, ob „Abo gesperrt" steht; dann erst bezahlen ([Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet)). Steht oben „Melde an bei …" statt einer Zeile „Server: …", hast du den alten Updater: [Abschnitt 14](#14-den-updater-einmalig-erneuern). |
| „FEHLER: Der Server hat kein Zugangs-Token geliefert." | Unerwartete Antwort | Später erneut versuchen, sonst Betreiber informieren. |
| „FEHLER: Konnte die Versionsinfo nicht abrufen: …" | Der Server hat zu lange gebraucht oder einen Fehler gemeldet | Ein paar Minuten warten und erneut starten. Kurz nach einem neuen Release kann der erste Abruf länger dauern. |
| „FEHLER: Download fehlgeschlagen: …" | Download abgebrochen | Internet prüfen, erneut starten. Dein Ordner ist unverändert. |
| „FEHLER: Die heruntergeladene Datei ist unbrauchbar (zu klein)." | Der Download war unvollständig | Erneut starten. Dein Ordner ist unverändert. |
| „FEHLER: Das Paket liess sich nicht entpacken: …" | Das Paket ist beschädigt, oder ein Virenscanner hat eingegriffen | Erneut starten. Bleibt es, Betreiber informieren. Dein Ordner ist unverändert. |
| „FEHLER: Im Paket ist keine manifest.json - Abbruch, dein Ordner bleibt unveraendert." | Das Paket war fehlerhaft | Betreiber informieren. |
| „FEHLER: Der Ordner 'extension' laesst sich nicht umbenennen. Laeuft Chrome doch noch? (…)" | Chrome oder ein anderes Programm (z. B. ein offenes Explorer-Fenster im Ordner, Virenscanner, Synchronisierung) hält den Ordner fest | Chrome komplett beenden (Task-Manager, `chrome.exe`), Explorer-Fenster in diesem Ordner schließen, erneut starten. |
| „FEHLER: Konnte die neue Fassung nicht einsetzen. Alte Fassung wiederhergestellt." | Der Tausch hat nicht geklappt | Prüfen, ob der Ordner `extension` noch da ist. Fehlt er, aber `extension_alt_…` existiert: `extension_alt_…` in `extension` umbenennen. Häufige Ursache: Der Programmordner liegt nicht auf Laufwerk C:. Dann den ganzen Ordner nach `C:\LeckAtakan` verschieben. **Vorsicht:** Danach muss die Extension in Chrome aus dem neuen Ort neu geladen werden. Vorher unbedingt „Einstellungen exportieren" und am besten den Betreiber fragen. |
| „Hinweis: Der Updater im Paket hat keine Kennzeile - der bisherige bleibt." / „WARNUNG: Der Updater im Paket ist fehlerhaft (…) - der bisherige bleibt." / „Hinweis: Der Updater konnte sich nicht erneuern (…) - das Update selbst ist davon nicht betroffen." | Die Selbst-Erneuerung des Updaters hat nicht geklappt, das eigentliche Update schon | Nichts tun. Bei Wiederholung Betreiber informieren. |
| Windows oder dein Virenscanner zeigt beim Start eine Warnung | – | Nichts einfach freigeben, was du nicht einordnen kannst. Frag den Betreiber. **Nicht sicher belegt:** Welche Warnungen auf welchen Systemen auftreten. |

### Häufige Fragen zu Updates (Windows)

**Gehen bei einem Update meine Einstellungen oder die Produkt-Datenbank verloren?**
Nein. Die Einstellungen liegen in Chrome, die Produkt-Datenbank auf dem Server. Getauscht wird nur der Programmordner `extension`.

**Muss ich nach dem Update etwas in Chrome klicken?**
Normalerweise nicht. Weil Chrome während des Updates geschlossen war, lädt es beim Start die neue Fassung samt Hintergrunddienst. Kontrolliere die Versionsnummer unten in der Seitenleiste. Stimmt sie nicht, die Extension in `chrome://extensions` neu laden ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)).

**Das Fenster hängt bei „(beim ersten Mal nach einer neuen Version dauert das bis zu 3 Minuten)".**
Warten. Das Programm wartet hier bis zu 5 Minuten, bevor es aufgibt.

**Kann ich `extension_alt_…` löschen?**
Ja, wenn die neue Version gut läuft. Das Programm räumt beim nächsten Update ohnehin auf und behält nur die letzte vorherige Fassung.

**Ich habe eine Meldung „veraltet" bekommen. Funktioniert das Update trotzdem?**
Ja. Das Update-Programm kann die neue Version auch dann holen, wenn die Extension selbst als veraltet abgewiesen wird ([Abschnitt 15](#15-mindestversion-wenn-deine-version-zu-alt-ist)).

**Funktioniert das Update, wenn mein Abo gesperrt ist?**
Nein. Das Update-Programm meldet sich mit deinem Konto an; bei einer Abo-Sperre klappt das nicht (Meldung „Server nicht erreichbar (…)"). Erst bezahlen, dann aktualisieren.

---

## 13. Updates auf dem Mac

### Einmalig: update.command startklar machen

1. **Datei an die richtige Stelle legen:** `update.command` in den Ordner ziehen, in dem auch `extension` liegt (neben `extension`, nicht hinein).
2. **Ausführbar machen** (nur nötig, wenn ein Doppelklick nichts tut oder „keine Berechtigung" meldet; kam die Datei in `update-mac.zip` und hast du sie per Doppelklick entpackt, ist das meist schon erledigt):
   - Terminal öffnen (Cmd+Leertaste, „Terminal" eingeben, Enter),
   - `chmod +x` eintippen, danach **ein Leerzeichen**,
   - `update.command` aus dem Finder in das Terminal-Fenster ziehen (der Pfad erscheint von allein),
   - Enter drücken. Es kommt keine Rückmeldung, das ist richtig so.
3. **Beim ersten Mal über Rechtsklick starten:** macOS meldet bei Dateien von außen „nicht verifizierter Entwickler". Rechtsklick (oder Ctrl+Klick) auf `update.command` → „Öffnen" → im Hinweisfenster noch einmal „Öffnen". Ab dem zweiten Mal genügt ein Doppelklick.
   **Nicht sicher belegt:** Bei neueren macOS-Versionen kann der Weg anders sein. Dort musst du die Datei eventuell unter Systemeinstellungen → „Datenschutz & Sicherheit" mit „Trotzdem öffnen" freigeben.

### So aktualisierst du

1. **Chrome komplett beenden: Cmd+Q**, nicht nur das Fenster schließen (der rote Punkt beendet Chrome auf dem Mac nicht).
2. `update.command` doppelklicken. Ein Terminal-Fenster öffnet sich. Oben steht „Cash Lister - Extension aktualisieren" (bei einer älteren Fassung des Updaters noch mit dem früheren Namen, das ist egal), darunter siehst du, was passiert:
   - „Melde an bei … ...", ggf. „(Adresse aus dem Extension-Ordner - die Zugangsdatei bleibt unveraendert)"
   - „(beim ersten Mal nach einer neuen Version dauert das bis zu 3 Minuten)"
   - „Deine Version : …" / „Auf dem Server: …"
   - neue Version: „Lade Version … (… MB) ...", „Aktualisiert auf Version ….", „Die vorherige Fassung liegt als "extension_alt_…" daneben.", „Chrome kann jetzt wieder gestartet werden."
   - keine neue Version: „Du hast bereits die aktuelle Fassung. Nichts zu tun."
   - ggf. „Der Updater selbst wurde ebenfalls auf den neuesten Stand gebracht."
3. „Zum Schliessen dieses Fensters Enter druecken." → Enter.
4. Chrome starten, auf das Cash-Lister-Symbol klicken: Das Dashboard muss sich öffnen, unten in der Seitenleiste muss die neue Versionsnummer stehen.

Anders als unter Windows wartet der Mac-Updater nicht, wenn Chrome noch läuft. Er bricht mit „Chrome laeuft noch. Bitte Chrome komplett beenden (Cmd+Q, nicht nur das Fenster schliessen) und diese Datei danach erneut anklicken." ab. Notfalls in der Aktivitätsanzeige nach „Google Chrome" suchen und beenden.

### Meldungen des Mac-Updates

| Meldung | Was tun |
|---|---|
| Doppelklick tut nichts, oder „keine Berechtigung" / „permission denied" | Schritt „Ausführbar machen" (chmod +x) fehlt. Alternative ohne chmod: Terminal öffnen, `bash ` (mit Leerzeichen) eintippen, Datei hineinziehen, Enter. |
| „bad interpreter: /bin/bash^M" | Die Datei wurde unterwegs verändert (Windows-Zeilenenden). Neue Fassung beim Betreiber anfordern und die Datei nicht mit einem Texteditor öffnen oder speichern. |
| „FEHLER: Keine Zugangsdatei gefunden. Lege die Datei vom Betreiber (zugang.json oder leck-atakan-einrichtung-*.json) neben diese Datei." | Einrichtungsdatei neben `update.command` legen. |
| „FEHLER: In <Datei> fehlen Angaben (…)." | Name oder Passwort fehlen in der Datei. Richtige Einrichtungsdatei verwenden bzw. neue anfordern. |
| „FEHLER: Keine Serveradresse: …" | Betreiber fragen. |
| „FEHLER: Name oder Passwort stimmen nicht. Bitte beim Betreiber melden." | Neue Einrichtungsdatei anfordern. |
| „FEHLER: Dein Zugang ist abgeschaltet. Bitte beim Betreiber melden." | Betreiber kontaktieren. |
| „FEHLER: Zu viele Versuche. Bitte ein paar Minuten warten." | Warten, erneut starten. |
| „FEHLER: Server nicht erreichbar (…). Internetverbindung pruefen." | Internet prüfen, später erneut. |
| „FEHLER: Anmeldung fehlgeschlagen (HTTP 402)." | Dein Abo ist gesperrt. Erst bezahlen ([Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet)), dann erneut aktualisieren. |
| „FEHLER: Anmeldung fehlgeschlagen (HTTP …)." mit einer anderen Zahl | Später erneut, sonst Betreiber informieren. |
| „FEHLER: Der Server hat kein Zugangs-Token geliefert." | Später erneut, sonst Betreiber informieren. |
| „FEHLER: Konnte die Versionsinfo nicht abrufen (HTTP …)." | Ein paar Minuten warten, erneut starten. |
| „FEHLER: Neben dieser Datei fehlt der Ordner 'extension'. Liegt sie am richtigen Platz?" | `update.command` liegt falsch. Sie muss **neben** dem Ordner `extension` liegen. |
| „FEHLER: Download fehlgeschlagen (HTTP …)." / „FEHLER: Die heruntergeladene Datei ist unbrauchbar (zu klein)." / „FEHLER: Das Paket liess sich nicht entpacken." | Erneut starten. Dein Ordner ist unverändert. |
| „FEHLER: Im Paket ist keine manifest.json - Abbruch, dein Ordner bleibt unveraendert." | Betreiber informieren. |
| „FEHLER: Kein Arbeitsverzeichnis anlegbar." / „FEHLER: Kein Zielverzeichnis anlegbar." | Mac neu starten, erneut versuchen. Bleibt es: Betreiber informieren. |
| „FEHLER: Der Ordner 'extension' laesst sich nicht zur Seite legen." | Chrome mit Cmd+Q beenden, Finder-Fenster in diesem Ordner schließen, erneut starten. |
| „FEHLER: Konnte die neue Fassung nicht einsetzen. Alte Fassung wiederhergestellt." | Prüfen, ob `extension` da ist. Sonst `extension_alt_…` zurückbenennen ([Abschnitt 16](#16-zurück-zur-vorherigen-version)). |
| „[i] Chrome-Pruefung ist in der Einrichtungsdatei abgeschaltet. …" | Selbst sicherstellen, dass Chrome mit Cmd+Q beendet ist. |

---

## 14. Den Updater einmalig erneuern

Ältere Kunden haben noch eine erste Fassung des Update-Programms. Diese kann sich nicht selbst aktualisieren. Die neue Fassung hält sich bei jedem Update selbst aktuell.

**Woran du erkennst, welche Fassung du hast (Windows):** Steht im Update-Fenster eine Zeile „Server: … (aus der Zugangsdatei)" oder „Server: … (aus dem Update-Paket)", hast du die neue Fassung, und du musst nichts tun. Steht dort stattdessen „Melde an bei … ...", ist es die alte.

**Wann du das brauchst:** wenn der Betreiber es dir sagt, oder wenn das alte Update-Programm „Server nicht erreichbar" meldet, obwohl dein Internet funktioniert (und dein Abo nicht gesperrt ist).

### Windows

1. Öffne im Programmordner den Ordner `extension\kunden-updater\`.
2. Doppelklicke **`Updater-erneuern.bat`**. Oben im Fenster steht „Cash Lister - Updater erneuern".
3. Mögliche Meldungen:
   - „Fertig - der Updater ist erneuert. … Diese Datei brauchst du nicht noch einmal. Die bisherige Fassung liegt als update.ps1.alt daneben." → erledigt.
   - „Der Updater ist schon auf dem neuesten Stand - nichts zu tun." → erledigt.
   - „FEHLER: Diese Datei liegt nicht an der richtigen Stelle. …" → Die Datei muss im Ordner `extension\kunden-updater\` gestartet werden, und neben `extension` muss `update.ps1` liegen. Es wurde nichts verändert.
   - „FEHLER: Neben dieser Datei fehlt der neue Updater update.ps1." / „FEHLER: Die update.ps1 neben dieser Datei ist kein Cash-Lister-Updater." → Erst mit dem bisherigen Updater aktualisieren oder beim Betreiber melden. Es wurde nichts verändert.
   - „FEHLER: Konnte die bisherige update.ps1 nicht sichern." / „FEHLER: Konnte den neuen Updater nicht kopieren." / „FEHLER: Konnte die update.ps1 nicht ersetzen." → Es wurde nichts verändert. Ordner schreibgeschützt oder von einem anderen Programm geöffnet? Erneut versuchen.
   - „FEHLER: Die Kontrolle nach dem Kopieren ist fehlgeschlagen. Die bisherige update.ps1 wurde wiederhergestellt." → Erneut versuchen, sonst Betreiber informieren.
4. Ab jetzt wie gewohnt `update.bat` benutzen. `update.bat` selbst wird dabei nicht ersetzt, und die Einrichtungsdatei wird nicht angefasst.

### Mac

1. Öffne im Programmordner `extension/kunden-updater/`.
2. Doppelklicke **`Updater-erneuern.command`** (falls nötig: Rechtsklick → „Öffnen").
3. Mögliche Meldungen (Fenstertitel „Cash Lister - neuen Updater einrichten (einmalig)"):
   - „Fertig. Der neue Updater liegt jetzt hier: … Ab jetzt wie gewohnt: Chrome beenden (Cmd+Q), dann update.command doppelklicken. …" → erledigt.
   - „Der neue Updater ist schon eingerichtet. Nichts zu tun."
   - „FEHLER: Diese Datei muss im Ordner extension/kunden-updater liegen - …" → von dort aus starten.
   - „FEHLER: Hier fehlt die neue update.command. Bitte zuerst mit dem bisherigen Updater aktualisieren." / „FEHLER: Die update.command hier ist nicht der neue Updater. Bitte zuerst aktualisieren."
   - „FEHLER: Die neue update.command hat Windows-Zeilenenden …" / „FEHLER: Die neue update.command ist beschaedigt. …" → beim Betreiber melden.
   - „FEHLER: Kann im Ordner … nicht schreiben." / „FEHLER: Kann das Ausfuehrungsrecht nicht setzen." / „FEHLER: Kann … nicht ersetzen." / „FEHLER: Der Ordner ueber "extension" ist nicht erreichbar." → Finder-Fenster in diesem Ordner schließen, Mac neu starten und erneut versuchen. Bleibt es: Betreiber informieren.
   - Nach jedem Fehler: „An deinem bisherigen Updater wurde nichts geaendert."
   - Tut der Doppelklick nichts oder kommt „keine Berechtigung": derselbe Weg wie bei `update.command` ([Abschnitt 13](#13-updates-auf-dem-mac), „Ausführbar machen", oder im Terminal `bash ` eintippen und die Datei hineinziehen).
   - Hinweise am Ende: wenn neben `extension` keine Einrichtungsdatei liegt, oder wenn dort weitere `.command`-Dateien liegen (alte Updater, die du löschen kannst).

---

## 15. Mindestversion: wenn deine Version zu alt ist

Der Betreiber kann eine **Mindestversion** festlegen. Versionen darunter können sich **nicht mehr anmelden**.

So merkst du es:
- Bei der regelmäßigen Prüfung der Anmeldung (regelmäßig im Hintergrund, beim Chrome-Start, beim Öffnen des Dashboards) wird eine zu alte Version **still abgemeldet**. Im Dashboard steht dann „Nicht angemeldet".
- Beim nächsten Anmeldeversuch erscheint: „Deine Version der Extension ist veraltet und wird nicht mehr unterstuetzt. Bitte melde dich beim Betreiber - du bekommst dann die neue Version."

Das Update-Programm ist davon ausgenommen: Es kann die neue Version auch dann holen.

**Nicht sicher belegt:** Welche Version gerade die Mindestversion ist. Frag den Betreiber.

Vorgehen bei „veraltet":
1. Versionsnummer unten in der Seitenleiste ansehen (bzw. bei einer sehr alten Fassung oben im kleinen Fenster).
2. **Ist sie alt:** Update machen ([Abschnitt 12](#12-updates-unter-windows) bzw. [13](#13-updates-auf-dem-mac)). Danach Chrome starten und im Dashboard neu anmelden.
3. **Ist sie schon neu, die Meldung kommt aber trotzdem:** Dann läuft noch der alte Hintergrunddienst. Chrome komplett schließen (auch Infobereich bzw. Cmd+Q) und neu starten, oder die Extension in `chrome://extensions` neu laden, und zwar in **jedem** Chrome-Profil ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)). Dann neu anmelden.
4. Hilft beides nicht: Betreiber kontaktieren.

---

## 16. Zurück zur vorherigen Version

Nach jedem erfolgreichen Update liegt die vorherige Fassung als Ordner `extension_alt_<Datum>_<Uhrzeit>` neben `extension`.

1. Chrome komplett schließen ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)).
2. Ordner `extension` umbenennen, z. B. in `extension_neu`.
3. Ordner `extension_alt_…` in **`extension`** umbenennen (genau dieser Name, am selben Ort).
4. Chrome starten. Jetzt läuft die vorherige Version. Deine Einstellungen sind weiterhin da.

Hinweise:
- Es gibt nur **eine** vorherige Fassung, ältere werden beim Update gelöscht.
- Ist die vorherige Fassung zu alt, kann der Server sie mit „Deine Version der Extension ist veraltet …" abweisen ([Abschnitt 15](#15-mindestversion-wenn-deine-version-zu-alt-ist)). Zurückgehen hilft dann nicht dauerhaft. Sag dem Betreiber Bescheid, was mit der neuen Version nicht stimmt.
- **Achtung beim Zurückgehen von 46.0 auf 45.x:** Version 46.0 hat deine Produkt-Datenbank auf den Server übertragen und die Liste in Chrome danach geleert. Eine 45er-Fassung kennt die Datenbank auf dem Server nicht und zeigt deshalb eine **leere Produkt-Datenbank**; dazu kommt dort wieder das alte kleine Fenster statt des Dashboards. Die Produkte sind nicht weg, sie liegen auf dem Server und sind mit 46.0 wieder da. Geh nur nach Rücksprache mit dem Betreiber zurück.
- Beim nächsten `update.bat` wird wieder die neueste Version geholt.

---

## 17. Chrome richtig schließen und den Hintergrunddienst aktualisieren

### Chrome komplett schließen (Windows)

1. Alle Chrome-Fenster schließen, **auch die anderer Chrome-Profile**.
2. Im Infobereich unten rechts in der Taskleiste nachsehen, ggf. auf den Pfeil „^" klicken. Ist dort ein Chrome-Symbol: Rechtsklick → „Beenden".
3. Alternativ im Chrome-Menü (drei Punkte oben rechts) „Beenden" wählen. Das schließt alle Fenster auf einmal.
4. Notfalls: Task-Manager (Strg+Umschalt+Esc) → Reiter „Details" → alle `chrome.exe` beenden.

Chrome läuft oft im Hintergrund weiter, wenn in den Chrome-Einstellungen unter „System" die Option zum Weiterlaufen von Apps im Hintergrund an ist. Das kannst du dort abschalten, wenn es dich stört. Die genaue Beschriftung hängt von deiner Chrome-Version ab.

### Chrome komplett beenden (Mac)

Cmd+Q in Chrome, oder im Menü „Chrome" → „Google Chrome beenden". Notfalls Aktivitätsanzeige → „Google Chrome" → beenden.

### Warum ein kompletter Neustart wichtig ist

Die Extension hat einen **Hintergrunddienst**, der dauerhaft läuft. Er erledigt unsichtbar Anmeldung, Abo-Stand, Listen, Tracker, Sicherung und die Verbindung zum Server. Nach jedem Update muss der **Hintergrunddienst aktualisiert** werden, sonst arbeitet er mit der alten Version weiter. Chrome lädt ihn erst bei einem kompletten Neustart oder beim Neuladen der Extension neu, und zwar **für jedes Chrome-Profil einzeln**. Die Seiten (Dashboard, Einstellungen, Browser-Lister, Tracker …) kommen dagegen jedes Mal frisch von der Festplatte. Wird Chrome nach einem Update nicht richtig neu gestartet, läuft eine **neue Oberfläche mit einem alten Hintergrunddienst**. Das sieht aus wie ein Programmfehler. Typische Zeichen:
- Beim Klick auf das Symbol öffnet sich noch das alte kleine Fenster statt des Dashboards,
- „Anmelden" im Dashboard tut nichts, nach etwa 30 Sekunden kommt „Keine Antwort vom Hintergrunddienst – bitte noch einmal versuchen.",
- Knöpfe in den Modulen tun nichts (z. B. „Starten" im Browser-Lister),
- die Karte „Dein Abo" fehlt, oder „Abo verwalten" meldet immer wieder „Kundenportal gerade nicht erreichbar …",
- „Deine Version der Extension ist veraltet …", obwohl die Seitenleiste die neue Versionsnummer zeigt,
- „Nicht möglich: keine Antwort" oder „Nicht möglich: A listener indicated an asynchronous response …" bei „Einstellungen vom Server holen",
- Profile verhalten sich unterschiedlich, obwohl sie denselben Ordner nutzen.

**Merksatz für jedes Update:** Erst wenn Chrome komplett neu gestartet bzw. die Extension neu geladen wurde, ist der Hintergrunddienst aktualisiert, und erst dann wirkt das Update vollständig.

### Extension neu laden (löscht nichts, aktualisiert den Hintergrunddienst)

1. In Chrome `chrome://extensions` öffnen.
2. Bei der Karte „Cash Lister" auf das **Kreispfeil-Symbol** (Neu laden) klicken.
3. Bei mehreren Chrome-Profilen: in **jedem** Profil, das Cash Lister benutzt, wiederholen.

Neu laden behält Einstellungen, Schlüssel und Anmeldung (die Produkt-Datenbank liegt ohnehin auf dem Server). **Aber:** Laufende Läufe des Browser-Listers oder Trackers werden dabei unterbrochen. Lade die Extension also nicht mitten in einem Lauf neu. Danach offene Tabs von Cash Lister neu laden bzw. die Module über die Seitenleiste neu öffnen.

**Nicht verwechseln:** „Entfernen" auf derselben Karte löscht alle Daten der Extension in Chrome.

---

## 18. Probleme und Lösungen (Sammelstelle)

### Klick auf das Symbol tut nichts

1. Ist das Dashboard schon offen, vielleicht in einem anderen Chrome-Fenster? Der Klick springt dann dorthin. Schau in deinen anderen Fenstern nach.
2. Steht in `chrome://extensions` auf der Cash-Lister-Karte ein Knopf „Fehler" oder ist die Karte grau: siehe „Extension verschwunden" unten.
3. Extension neu laden bzw. Chrome komplett neu starten ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)).
4. Hilft das nicht: Betreiber mit Versionsnummer und Betriebssystem kontaktieren.

### Statt des Dashboards öffnet sich ein kleines Fenster

Chrome hat noch eine ältere Fassung (vor 46.0) geladen, z. B. weil Chrome nach dem Update nicht komplett geschlossen war. Chrome komplett neu starten oder in `chrome://extensions` neu laden, in jedem Profil ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)). Zeigt die Seitenleiste danach immer noch eine alte Nummer, war das Update nicht erfolgreich: `update.bat` noch einmal ausführen und die Meldungen lesen.

### Anmelden tut nichts

1. **Bis zu 30 Sekunden warten.** Nach etwa 20 Sekunden kommt ggf. „Server nicht erreichbar (…)", nach etwa 30 Sekunden „Keine Antwort vom Hintergrunddienst – bitte noch einmal versuchen.".
2. Kommt „Keine Antwort vom Hintergrunddienst …": Der Hintergrunddienst der Extension antwortet nicht.
   - Chrome **komplett** schließen und neu starten ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)), oder
   - `chrome://extensions` → bei „Cash Lister" auf den Kreispfeil.
   - Danach das Dashboard neu öffnen und erneut anmelden.
3. Erscheint eine andere rote Meldung unter dem Formular: Bedeutung in der Tabelle in [Abschnitt 5.5](#55-alle-meldungen-beim-anmelden).
4. Kommt „Server nicht erreichbar (…)", obwohl dein Internet funktioniert: In den Einstellungen im Reiter „eBay & Rahmenbedingungen", Karte „Server & Produkt-Vergabe", nachsehen, ob im Feld „Server-Adresse" etwas steht. Hat der Betreiber dir keine Adresse genannt: Feld leeren, in ein anderes Feld klicken, im Dashboard erneut anmelden ([Abschnitt 5.4](#54-das-feld-server-adresse)). Das Feld im Dashboard zeigt eine gespeicherte Adresse nicht an.
5. Steht in `chrome://extensions` auf der Cash-Lister-Karte ein Knopf „Fehler": Inhalt abfotografieren und dem Betreiber schicken.
6. Erst wenn das alles nicht hilft: Betreiber mit genauer Meldung, Versionsnummer und Betriebssystem kontaktieren.

### Meldung veraltet

Text: „Deine Version der Extension ist veraltet und wird nicht mehr unterstuetzt. Bitte melde dich beim Betreiber - du bekommst dann die neue Version."

Bedeutung: Der Server akzeptiert die Version nicht mehr, die gerade **im Hintergrund** von Chrome läuft. Meist wurdest du vorher schon still abgemeldet (im Dashboard „Nicht angemeldet"), und die Meldung erscheint, sobald du dich neu anmelden willst. Vorgehen: [Abschnitt 15](#15-mindestversion-wenn-deine-version-zu-alt-ist).

### Abo gesperrt

Siehe [Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet): bezahlen, dann im Dashboard neu anmelden.

### Die Module in der Seitenleiste sind grau

Du bist nicht angemeldet, dein Zugang ist abgeschaltet oder dein Abo ist gesperrt. Was zutrifft, steht unten im Kasten der Seitenleiste und im Dashboard ([Abschnitt 5.6](#56-wo-du-siehst-ob-du-angemeldet-bist)). Nur Dashboard und Einstellungen bleiben immer anklickbar.

### Extension verschwunden

Gemeldet wurde: „Die Extension ist plötzlich weg" bzw. „grau / ausgeschaltet", teils mit verlorenen Einstellungen. Die Extension kann sich nicht selbst entfernen. Die Ursache liegt bei Chrome oder beim Ordner.
**Nicht sicher belegt:** Warum das bei manchen Kunden passiert. Mögliche, aber nicht bewiesene Ursachen: Der Entwicklermodus wurde ausgeschaltet. Der Ordner `extension` wurde verschoben, umbenannt oder gelöscht (auch durch Synchronisierungsprogramme wie OneDrive, Virenscanner oder ein abgebrochenes Update). Chrome hat die entpackte Erweiterung beim Start deaktiviert.

**Ganz wichtig: Nicht vorschnell auf „Entfernen" klicken.** Solange die Karte noch da ist, sind deine Daten in Chrome meist noch da.

1. `chrome://extensions` öffnen. Ist der **„Entwicklermodus"** oben rechts an? Wenn nicht: einschalten.
2. **Fall A: Die Karte „Cash Lister" ist da, aber grau/ausgeschaltet.**
   - Schalter auf der Karte einschalten.
   - Steht dort ein Fehler, z. B. dass Dateien oder die Manifestdatei fehlen: Prüfe, ob der Ordner `extension` noch an seinem alten Ort liegt und `manifest.json` enthält. Ggf. wiederherstellen (Papierkorb, `extension_alt_…` zurückbenennen, aus dem Paket neu entpacken **an denselben Ort**), dann auf der Karte den Kreispfeil klicken.
   - Deine Einstellungen sollten dann wieder da sein.
3. **Fall B: Die Karte ist ganz weg.** Dann wurde die Extension aus Chrome entfernt, und Chrome hat dabei auch ihre Daten in Chrome gelöscht.
   - Prüfe, ob der Ordner `extension` mit `manifest.json` im Programmordner noch existiert. Fehlt er: aus `extension_alt_…` zurückbenennen oder das Paket neu entpacken (am besten nach `C:\LeckAtakan`).
   - In `chrome://extensions` → „Entpackte Erweiterung laden" → Ordner `extension` wählen.
   - Auf das Symbol klicken und im Dashboard anmelden (am besten mit „Einrichtungsdatei einlesen"). **Die Server-Sicherung holt deine Einstellungen jetzt automatisch zurück** ([Abschnitt 9](#9-einstellungs-sicherung-auf-dem-server)). In den Einstellungen im Reiter „Sicherung" sollte „Vom Server übernommen: …" stehen.
   - **Deine Produkt-Datenbank ist nicht verloren.** Sie liegt auf dem Server und ist nach der Anmeldung wieder da.
   - **Von Hand nachholen:** OpenAI-Schlüssel im Reiter „KI" eintragen (oder die eigene Export-Datei im Reiter „Sicherung" importieren). Im Reiter „Produkt-Filter" die Filter „Mind. Sterne", „Mind. Bewertungen", „Mind. Lagerbestand" und die Schalter aller Amazon-Filter prüfen. War das Gerät als Server eingetragen, in der Karte „Server-Modus" im Reiter „eBay & Rahmenbedingungen" den Schalter „Dieses Gerät ist ein Server" wieder einschalten.
4. Vorbeugen: Ordner nach `C:\LeckAtakan` legen und dort lassen. Entwicklermodus anlassen. Regelmäßig „Einstellungen exportieren".

### Einstellungen weg (Extension ist aber noch da)

Mögliche Ursachen:
- Die Extension wurde entfernt und neu geladen. Das ist für Chrome eine Neuinstallation mit leerem Speicher.
- Du bist in einem **anderen Chrome-Profil**. Jedes Profil hat eigene Einstellungen. Oben rechts in Chrome prüfen, welches Profil offen ist.
- Ein „Einstellungen importieren", „Einrichtungsdatei einlesen" oder „Einstellungen vom Server holen" hat die Werte ersetzt.
- Auf einem zweiten Gerät mit demselben Konto wurde zuletzt gesichert, und du hast dessen Stand geholt ([Abschnitt 9](#9-einstellungs-sicherung-auf-dem-server)).

Lösung:
1. Prüfen, ob du angemeldet bist (Dashboard). Wenn nicht: anmelden. Bei einer frischen Installation werden die Einstellungen dabei automatisch zurückgeholt.
2. Einstellungen öffnen → Reiter „Sicherung" → Statuszeile lesen:
   - Konflikt-Text → entscheiden ([Abschnitt 9](#9-einstellungs-sicherung-auf-dem-server)).
   - Sonst: „Einstellungen vom Server holen" klicken und bestätigen.
3. Zusätzlich deine letzte Export-Datei importieren, wenn du den OpenAI-Schlüssel zurückhaben willst.
4. Offene Tabs von Cash Lister neu laden.

Nicht wiederherstellbar ohne eigene Export-Datei: der OpenAI-Schlüssel (musst du neu eintragen) und die gemerkten Konkurrenten des Konkurrenz-Scanners. Die Produkt-Datenbank liegt auf dem Server und ist davon nicht betroffen.

### Produkt-Datenbank leer oder „nach der Anmeldung sichtbar"

- Nicht angemeldet → im Dashboard anmelden.
- „Server nicht erreichbar" → Internet prüfen, später erneut; die Daten liegen auf dem Server.
- Direkt nach dem Update auf 46.0: Die bisherige Liste wird noch übertragen („… werden noch auf den Server übertragen …"). Warten.
- Mit einem anderen Konto angemeldet? Jedes Konto hat seine eigene Produkt-Datenbank.
- Läuft eine Version vor 46.0? Siehe [Abschnitt 16](#16-zurück-zur-vorherigen-version), „Achtung beim Zurückgehen".

### Update meldet einen Fehler

- Windows: Tabelle in [Abschnitt 12](#12-updates-unter-windows). Mac: Tabelle in [Abschnitt 13](#13-updates-auf-dem-mac).
- Grundsatz: Bei Fehlern vor dem Tausch bleibt dein Ordner unverändert. Du kannst es einfach noch einmal versuchen.
- Ist nach einem Fehler der Ordner `extension` weg, aber `extension_alt_…` da: zurückbenennen ([Abschnitt 16](#16-zurück-zur-vorherigen-version)).
- Häufigste Ursachen: Chrome lief noch, die Einrichtungsdatei fehlt oder ist veraltet, der Ordner liegt nicht auf C:, keine Internetverbindung, alter Updater ([Abschnitt 14](#14-den-updater-einmalig-erneuern)), Abo gesperrt ([Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet)).

### Mac-spezifische Probleme

| Problem | Lösung |
|---|---|
| Doppelklick auf `update.command` tut nichts / „keine Berechtigung" | `chmod +x` ([Abschnitt 13](#13-updates-auf-dem-mac)) oder per `bash ` im Terminal starten. |
| „nicht verifizierter Entwickler" | Rechtsklick → „Öffnen" → „Öffnen". Bei neueren macOS ggf. Systemeinstellungen → „Datenschutz & Sicherheit" → „Trotzdem öffnen" (**Nicht sicher belegt**, hängt von der macOS-Version ab). |
| „bad interpreter: /bin/bash^M" | Neue Datei beim Betreiber anfordern, nicht im Texteditor öffnen. |
| „Chrome laeuft noch" | Cmd+Q, notfalls Aktivitätsanzeige. |
| „Anmeldung fehlgeschlagen (HTTP 402)." | Abo gesperrt ([Abschnitt 7.6](#76-abo-sperre-was-passiert-und-wie-sie-endet)). |
| Update lief, aber die Seitenleiste zeigt die alte Version oder es öffnet sich das kleine Fenster | Chrome mit Cmd+Q beenden und neu starten, ggf. Extension neu laden. |
| `update.bat` auf dem Mac | Tut nichts. Auf dem Mac ist `update.command` zuständig. |

### Seiten zeigen alte Werte

- Nach „Einstellungen vom Server holen", einem Import, „Einrichtungsdatei einlesen" oder der automatischen Wiederherstellung: offene Tabs von Cash Lister (Einstellungen, Module) neu laden.
- Nach einem Update: Versionsnummer unten in der Seitenleiste prüfen, ggf. Chrome komplett neu starten bzw. Extension neu laden.

### Tracker zeigt „Für den Tracker brauchst du die Ultimate-Mitgliedschaft." und eine leere Seite

Du bist nicht angemeldet, dein Zugang ist nicht aktiv oder dein Abo ist gesperrt. Im Dashboard anmelden (bzw. Abo klären), dann den Tracker über die Seitenleiste neu öffnen. Eine zusätzliche Buchung ist nicht nötig.

### Viele Produkte scheitern mit „Amazon-Preis zu hoch (Filter „Preis bis")"

(Früher lautete die Meldung „Price is too high".) Einstellungen → Reiter „Produkt-Filter" → Karte „Amazon-Filter" → „Preis bis" und seinen Schalter prüfen. Ältere Installationen haben dort oft noch eine Obergrenze von 100 stehen. Einzelheiten im Bereich Einstellungen.

---

## 19. Was diese Hilfe nicht sicher weiß

Bei diesen Fragen offen sagen, dass es nicht sicher bekannt ist, und an den Betreiber verweisen:

- Warum die Extension bei manchen Kunden aus Chrome verschwindet. Es gibt nur Vermutungen (Entwicklermodus, verschobener Ordner, OneDrive/Virenscanner, abgebrochenes Update).
- Ob und ab welcher Chrome-Version Chrome entpackte Erweiterungen abschaltet, wenn der Entwicklermodus aus ist.
- Welche Version gerade die Mindestversion ist.
- Nach welcher Zeit ohne Nutzung eine Anmeldung (Sitzung) abläuft.
- Ob der Betreiber die Zahl der Geräte oder Chrome-Profile je Konto begrenzt (in der Extension ist keine Grenze zu sehen).
- Der genaue Tag der ersten Abbuchung (maßgeblich ist die eigene Zahlungsseite).
- Wie schnell eine Abo-Sperre nach einer Zahlung aufgehoben ist.
- Ob man das Abo pausieren kann.
- Ob ältere Stände der Einstellungs-Sicherung beim Betreiber aufbewahrt werden.
- Welcher Teil bei „zu groß für die Sicherung" die Größe verursacht.
- Ob Produkt-Vergabe und Sheet-Abgleich nach einer Neuinstallation jedes früher gelistete Produkt sicher als „schon gelistet" erkennen.
- Welche Warnungen Windows, macOS oder Virenscanner beim Start der Update-Programme zeigen, und den genauen Freigabe-Weg bei neueren macOS-Versionen.
- Auf welchem Weg der Betreiber neue Versionen ankündigt.
- Zur Prüfung Auktion/Sofort-Kaufen gibt es keine Beschreibung. Bei Fragen dazu an den Betreiber wenden.

---

## 20. Neu in Version 46.0

Was Kunden der bisherigen Version (45.4/45.5) in diesem Bereich jetzt anders finden:

- **Neuer Name und neues Logo:** Die Extension heißt überall „Cash Lister", alle Seiten haben ein neues Design mit einer Seitenleiste links.
- **Das kleine Fenster beim Klick aufs Symbol gibt es nicht mehr.** Es öffnet sich das **Dashboard** in einem eigenen Tab. Ist es schon offen, springt der Klick dorthin.
- **Anmelden und Abmelden im Dashboard.** Die Anmeldekarte erscheint, solange du nicht angemeldet bist. Abmelden geht über das Kontofeld oben rechts → „Abmelden"; läuft gerade etwas, fragt Cash Lister vorher nach.
- **Einrichtungsdatei:** Der Knopf heißt jetzt „Einrichtungsdatei einlesen" (früher „Einstellungen importieren" im Anmeldefenster).
- **Die Einstellungen aus dem kleinen Fenster stehen jetzt in den Einstellungen, Reiter „Preise & Listing":**

  | Früher im kleinen Fenster | Jetzt |
  |---|---|
  | Karte „Preise" („% Aufschlag:", „Fester Aufschlag (€):", „Neu: Sonstige"-Haken, „Variable Preise (nach Preis-Range):") | Reiter „Preise & Listing", Karte „Preise" („Variable Preise (nach Preisspanne)") |
  | „Eigene Preise für „Neu: Sonstige"" (zweite Preistafel) | gibt es nicht mehr – eine Preistafel für alle Zustände |
  | „End Price:" mit Knopf „End Price: An/Aus" | „Preisendung" mit Schalter |
  | „Domain:" | Karte „Listing", „Domain" („None" heißt jetzt „Keine") |
  | „Auto Submit Listing" | „Listing automatisch absenden" |
  | „Promoted Listing Ad Rate:" | „Anzeigengebühr (%)" |
  | „Min Price (AutoList):" / „Max Price (AutoList):" | Reiter „Produkt-Filter", Karte „Amazon-Filter": „Preis ab" / „Preis bis" (mit eigenem Schalter) |
  | „Schedule Listing Time:" | entfernt |
  | „Fill Required Item Specifics with AI" / „Fill Optional Item Specifics with AI" | Karte „Artikelmerkmale (KI)": „Pflicht-Artikelmerkmale mit KI ausfüllen" / „Optionale Artikelmerkmale mit KI ausfüllen" |
  | Knöpfe für die Module | Seitenleiste bzw. Karten im Dashboard |
  | „Einstellungen exportieren" / „Einstellungen importieren", „Einstellungen vom Server holen", „Dieses Gerät auf den Server sichern" | Reiter „Sicherung" |

  Genaueres zu jeder Einstellung steht im Bereich Einstellungen (`references/einstellungen.md`).
- **Versionsnummer:** steht jetzt unten in der Seitenleiste („Version 46.0"), nicht mehr oben im kleinen Fenster.
- **Umbenannt:** „Bulk Lister" heißt jetzt **„Browser-Lister"**, „CSV Tracker" heißt jetzt **„Tracker"**. Der Browser-Lister hat nur noch den Knopf „Starten" (Titel immer per KI).
- **CSV-Lister für alle:** Früher sahen nur freigeschaltete Tester den „CSV-Lister (neu)". Jetzt steht „CSV-Lister" bei allen Kunden in der Seitenleiste und im Dashboard, und der Reiter heißt bei allen „eBay & Rahmenbedingungen".
- **Meldungen sagen jetzt „im Dashboard anmelden"** statt „im Popup anmelden". Die Tracker-Meldung bei fehlender Anmeldung lautet jetzt „Für den Tracker brauchst du die Ultimate-Mitgliedschaft.".
- **Produkt-Datenbank je Konto auf dem Server:** Alle Geräte mit demselben Konto sehen dieselbe Liste, mit Spalte „In Arbeit". Beim ersten Start wird die bisherige Liste automatisch hochgeladen. Sie ist nicht mehr in der Export-Datei und geht bei „Entfernen" der Extension nicht mehr verloren ([Abschnitt 8](#8-produkt-datenbank-jetzt-je-konto-auf-dem-server)).
- **Neu: Abo und Zahlung.** Karte „Dein Abo" im Dashboard mit „Abo verwalten" (Kundenportal), Warnungen bei offener Zahlung, Sperre bei Nichtzahlung ([Abschnitt 7](#7-abo-und-zahlung)).
- **Nach dem Update auf 46.0 ist der komplette Chrome-Neustart Pflicht** (bzw. „Neu laden" in `chrome://extensions`, in jedem Chrome-Profil). Öffnet sich danach noch das kleine Fenster, läuft noch die alte Fassung ([Abschnitt 17](#17-chrome-richtig-schließen-und-den-hintergrunddienst-aktualisieren)).
- **Zurück auf 45.x** zeigt eine leere Produkt-Datenbank ([Abschnitt 16](#16-zurück-zur-vorherigen-version)).
- Unverändert: das Update-Programm (`update.bat`, `update.ps1`, `update.command`, `Updater-erneuern`), die Einrichtungsdatei, die Regeln der Einstellungs-Sicherung (Konflikt, „zuletzt gesichert gilt", 512 KB) und die Meldungen beim Anmelden (einige jetzt mit echten Umlauten; neu dazu kommen „Anmeldung abgelehnt: Abo gesperrt." und „Keine Antwort vom Hintergrunddienst – bitte noch einmal versuchen.").

Weitere Änderungen in anderen Bereichen (z. B. Dashboard, Browser-Lister, Tracker, Produkt-Datenbank, Einstellungen) stehen in den jeweiligen Bereichen dieser Hilfe.
