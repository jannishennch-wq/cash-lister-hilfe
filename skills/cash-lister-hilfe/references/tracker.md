# Tracker: Preise und Bestand mit Amazon abgleichen

Der Tracker (früher „CSV Tracker“) prüft deine laufenden eBay-Angebote der Reihe nach bei Amazon. Danach passt er bei eBay Preis und Menge an oder setzt Angebote, deren Amazon-Produkt nicht mehr kaufbar ist, auf Menge 0 bzw. beendet sie. Hochgeladen wird automatisch, sobald ein Lauf vollständig durchgelaufen ist.

> Hinweis für den Assistenten: Stellen, die mit **Nicht sicher belegt:** markiert sind, sind offen. Sag dem Kunden ehrlich „Das weiß ich nicht sicher“ und verweise an den Betreiber, statt zu raten. Beschriftungen stehen hier genau so, wie sie auf der Seite stehen. Die Tracker-Seite ist seit Version 46.0 deutsch beschriftet. Einige Status-Texte enthalten trotzdem englische Teile (z. B. „Success“, „Skipped“, „ERROR_503“, „Tab failed to load“), weil sie aus Chrome oder aus festen Kennzeichen stammen. Kunden mit älteren Versionen kennen noch englische Knöpfe wie „Get Listings From Ebay“ – die Zuordnung steht in [Abschnitt 26](#26-neu-in-version-460).

## Inhalt

1. [Wozu der Tracker da ist](#1-wozu-der-tracker-da-ist)
2. [Begriffe kurz erklärt](#2-begriffe-kurz-erklärt)
3. [Tracker öffnen und Voraussetzungen](#3-tracker-öffnen-und-voraussetzungen)
4. [Die Seite von oben nach unten](#4-die-seite-von-oben-nach-unten)
5. [Angebote laden: von eBay oder als eigene Datei](#5-angebote-laden-von-ebay-oder-als-eigene-datei)
6. [Die Karte „Filter“](#6-die-karte-filter)
7. [Ein Lauf: starten, pausieren, fortsetzen, abbrechen](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)
8. [„Gleichzeitig“: wie viele Artikel gleichzeitig geprüft werden](#8-gleichzeitig-wie-viele-artikel-gleichzeitig-geprüft-werden)
9. [Die Tabelle „Verarbeitete Artikel“ und die Status-Texte](#9-die-tabelle-verarbeitete-artikel-und-die-status-texte)
10. [Preise und Mengen: so rechnet der Tracker](#10-preise-und-mengen-so-rechnet-der-tracker)
11. [Das Fenster „Upload-Einstellungen“](#11-das-fenster-upload-einstellungen)
12. [Hochladen zu eBay](#12-hochladen-zu-ebay)
13. [Die Dateien des Trackers](#13-die-dateien-des-trackers)
14. [Die eBay-Berichtsseiten (Downloads und Uploads)](#14-die-ebay-berichtsseiten-downloads-und-uploads)
15. [Automatik: „Dauerhaft wiederholen“ (24/7)](#15-automatik-dauerhaft-wiederholen-247)
16. [Schutz bei Sperren und Fehlern: „Kurz warten!“ und Notbremse](#16-schutz-bei-sperren-und-fehlern-kurz-warten-und-notbremse)
17. [Die Karte „Google Sheets“ (Duplikat-Abgleich)](#17-die-karte-google-sheets-duplikat-abgleich)
18. [Produkt-Vergabe beim Laden der Angebote](#18-produkt-vergabe-beim-laden-der-angebote)
19. [Der Tracker im Dashboard](#19-der-tracker-im-dashboard)
20. [Alle Meldungen des Trackers](#20-alle-meldungen-des-trackers)
21. [Typische Abläufe Schritt für Schritt](#21-typische-abläufe-schritt-für-schritt)
22. [Häufige Fragen (allgemein)](#22-häufige-fragen-allgemein)
23. [Probleme und Lösungen (allgemein)](#23-probleme-und-lösungen-allgemein)
24. [Standardwerte auf einen Blick](#24-standardwerte-auf-einen-blick)
25. [Was hier nicht sicher belegt ist](#25-was-hier-nicht-sicher-belegt-ist)
26. [Neu in Version 46.0](#26-neu-in-version-460)
27. [Neu in Version 46.1 bis 46.3](#27-neu-in-version-461-bis-463)

---

## 1. Wozu der Tracker da ist

Der Tracker hält Preis und Bestand deiner eBay-Angebote passend zu Amazon. Ist ein Produkt bei Amazon teurer geworden oder nicht mehr lieferbar, passt er dein Angebot an, damit du nicht mit Verlust oder ohne lieferbare Ware verkaufst.

**So läuft es grob ab:**

1. Der Tracker holt sich eine Liste deiner aktiven eBay-Angebote (einen „Bericht“ von eBay als CSV-Datei).
2. Er erkennt an der SKU (Bestandseinheit) jedes Angebots, welches Amazon-Produkt dazugehört.
3. Für jedes Angebot öffnet er die Amazon-Produktseite in einem Hintergrund-Tab und liest ab: Ist es lieferbar? Wird es von Amazon versendet (Prime)? Gibt es kostenlosen Versand? Was kostet es?
4. Daraus berechnet er deinen eBay-Preis (mit den Aufschlägen aus den Einstellungen, Reiter „Preise & Listing“) und die Menge.
5. Ist der Lauf **vollständig** durchgelaufen, lädt er die Änderungen **automatisch** bei eBay hoch. Angebote, deren Amazon-Produkt nicht mehr kaufbar ist, setzt er auf Menge 0 oder beendet sie (das stellst du ein, [Abschnitt 11](#11-das-fenster-upload-einstellungen)).

**Was der Tracker ändert und was nicht:**

- Er ändert bei eBay nur **Preis** und **Menge** und beendet bei Bedarf Angebote. Titel, Beschreibung, Bilder, Versand usw. fasst er **nicht** an.
- Er bearbeitet nur Angebote, die Cash Lister selbst eingestellt hat (erkennbar an der SKU, siehe [Abschnitt 2](#2-begriffe-kurz-erklärt)). Angebote, die du von Hand oder mit einem anderen Werkzeug eingestellt hast, lässt er in Ruhe.
- Er liest bei Amazon **keine Stückzahl**. Ist ein Produkt lieferbar, bekommt das eBay-Angebot die feste Menge aus dem Feld „Feste Menge“ ([Abschnitt 11.4](#11-das-fenster-upload-einstellungen)).
- Er lädt **nur** am Ende eines vollständigen Laufs hoch. Einen Knopf zum Hochladen von Hand gibt es nicht mehr (schon seit Version 45.5), und seit Version 46.0 lässt sich das automatische Hochladen auch nicht mehr abschalten ([Abschnitt 12](#12-hochladen-zu-ebay)).

Der Tracker arbeitet im Browser: Der Tracker-Tab muss offen bleiben, solange er arbeitet, Chrome muss laufen, und du musst in diesem Chrome-Profil bei eBay angemeldet sein.

---

## 2. Begriffe kurz erklärt

- **ASIN**: Amazons Artikelnummer, 10 Zeichen, z. B. `B0ABCDEFGH`. Steht in der Adresse einer Amazon-Produktseite hinter `/dp/`.
- **SKU / Bestandseinheit / Custom Label**: deine eigene Artikelnummer in einem eBay-Angebot. Im eBay-Bericht heißt die Spalte „Custom label (SKU)“. Cash Lister trägt dort beim Listen eine eigene Kennung ein (sie endet auf „==“). **Daran erkennt der Tracker das Amazon-Produkt. Ändere diese SKU nicht.** Wie eBay das Feld in deinem Verkäuferkonto genau beschriftet, ist von eBay abhängig.
- **Artikelnummer (ItemID)**: die Nummer deines eBay-Angebots (im eBay-Bericht „Item number“).
- **Bericht (Angebotsbericht)**: eine CSV-Datei, die eBay im Verkäufer-Bereich (Seller Hub) erstellt. Der Tracker nutzt den Bericht über **alle aktiven Angebote**.
- **CSV-Datei**: eine einfache Tabellen-Datei (lässt sich mit Excel oder Google Tabellen öffnen).
- **Buybox**: der Kaufkasten rechts auf einer Amazon-Produktseite mit „In den Einkaufswagen“.
- **FBA / Versand durch Amazon / Prime**: Die Ware liegt in einem Amazon-Lager, Amazon verschickt sie. Der Tracker prüft, ob ein Produkt als von Amazon versendet bzw. als Prime erkannt wird.
- **Revise**: eBay-Befehl „Angebot ändern“ (hier: Preis und/oder Menge). Taucht in der Vorschau und in der Upload-Datei auf.
- **EndItem / End**: eBay-Befehl „Angebot beenden“.
- **„Gleichzeitig“** (früher „Threads“): so viele Amazon-Seiten prüft der Tracker zur selben Zeit, jede in einem eigenen Tab ([Abschnitt 8](#8-gleichzeitig-wie-viele-artikel-gleichzeitig-geprüft-werden)).
- **Lauf**: einmal alle geladenen Angebote von vorne (bzw. ab „Ab Artikel“) bis hinten prüfen.
- **Dauerbetrieb (24/7)**: Nach jedem Lauf und einer Pause startet der nächste von selbst ([Abschnitt 15](#15-automatik-dauerhaft-wiederholen-247)).
- **Produkt-Vergabe**: Ein zentraler Vergabe-Dienst merkt sich, welcher Kunde welches Amazon-Produkt listet, damit nicht zwei Kunden dasselbe Produkt anbieten ([Abschnitt 18](#18-produkt-vergabe-beim-laden-der-angebote)).
- **Hintergrunddienst**: der unsichtbare Teil der Extension in Chrome, der u. a. die Amazon- und eBay-Tabs für den Tracker öffnet. Nach einem Update muss er aktualisiert werden (Chrome komplett neu starten, siehe `konto-und-installation.md`, Abschnitt 17 „Chrome richtig schließen und den Hintergrunddienst aktualisieren“).

---

## 3. Tracker öffnen und Voraussetzungen

### So öffnest du den Tracker

1. Klick oben in der Chrome-Leiste auf das Cash-Lister-Symbol. Es öffnet sich das **Dashboard** (das frühere kleine Fenster gibt es nicht mehr).
2. Klick in der **Seitenleiste** links unter „Arbeiten“ auf „**Tracker**“ – oder im Dashboard unter „Vorgänge“ auf die Karte „**Tracker**“ („Preise und Bestand der aktiven Angebote mit Amazon abgleichen und zu eBay hochladen.“).
3. Der Tracker öffnet sich in einem **eigenen Tab**. Der Tab heißt „Cash Lister – Tracker“, oben auf der Seite steht „Tracker“ und darunter „Preise & Bestand mit Amazon abgleichen“.

**Ist der Tracker schon offen**, öffnet ein Klick keinen zweiten Tab, sondern **springt** zum offenen Tracker-Tab (auch in einem anderen Chrome-Fenster). Das ist Absicht: Ein Lauf lebt nur in seinem Tab, und zwei Tracker-Tabs würden sich gegenseitig den gespeicherten Stand überschreiben.

Ist der Eintrag „Tracker“ in der Seitenleiste oder die Karte im Dashboard **grau**, bist du nicht angemeldet, dein Zugang ist abgeschaltet oder dein Abo ist gesperrt (siehe `konto-und-installation.md`, Abschnitte 5 und 7).

### Voraussetzungen

| Voraussetzung | Warum | Wo einstellen |
|---|---|---|
| Du bist **im Dashboard angemeldet**, dein Zugang ist aktiv und dein Abo nicht gesperrt. | Sonst kommt beim Öffnen „Für den Tracker brauchst du die Ultimate-Mitgliedschaft.“ und die Seite wird leer. | Dashboard → Anmeldung (`konto-und-installation.md`, Abschnitt 5; Abo: Abschnitt 7) |
| Deine Version ist nicht älter als die Mindestversion. | Mit einer zu alten Version kannst du dich nicht anmelden – und ohne Anmeldung öffnet sich der Tracker nicht. | Update mit `update.bat` (`konto-und-installation.md`, Abschnitte 12 und 15) |
| Du bist im **selben Chrome-Profil bei eBay** angemeldet. | Der Tracker holt den Bericht und lädt Änderungen über deine eBay-Sitzung hoch. | einfach bei eBay einloggen |
| In den Einstellungen ist bei „**Domain**“ dein eBay-Land eingestellt. | „Angebote von eBay laden“ holt den Bericht von dieser eBay-Seite. | Einstellungen → Reiter „Preise & Listing“ → Karte „Listing“ → „Domain“ |
| Im Tracker steht bei „**eBay-Seite**“ derselbe Marktplatz. | Danach richtet sich, auf welcher Amazon-Seite geprüft und zu welcher eBay-Seite hochgeladen wird ([Abschnitt 6.2](#6-die-karte-filter)). | Tracker → Karte „Filter“ → „eBay-Seite“ |
| Deine Preise sind eingestellt **und gespeichert**. | Der Tracker rechnet mit denselben Aufschlägen wie beim Listen ([Abschnitt 10](#10-preise-und-mengen-so-rechnet-der-tracker)). | Einstellungen → Reiter „Preise & Listing“ → Karte „Preise“ |
| Deine Upload-Einstellungen passen. | Am Ende jedes vollständigen Laufs wird **automatisch** hochgeladen. | Tracker → Knopf „Upload-Einstellungen“ ([Abschnitt 11](#11-das-fenster-upload-einstellungen)) |

Den Server von Cash Lister braucht der Tracker nur für den Abgleich der Produkt-Vergabe ([Abschnitt 18](#18-produkt-vergabe-beim-laden-der-angebote)). Zeigt die Seitenleiste „Server nicht erreicht“, prüft der Tracker trotzdem und lädt trotzdem hoch; nur der Vergabe-Abgleich meldet dann einen Fehler.

### Häufige Fragen

- **„Muss die Tracker-Seite offen bleiben?“** – Ja. Der Tracker arbeitet nur, solange sein Tab offen ist und Chrome läuft. Schließt du den Tab, hört er auf. Das Dashboard muss dagegen **nicht** offen sein.
- **„Kann ich den Tracker zweimal öffnen?“** – Über Dashboard und Seitenleiste nicht: Der Klick springt immer zum offenen Tracker-Tab. Öffne auch keinen zweiten Tracker auf anderem Weg (z. B. Tab duplizieren). Beide würden dieselben gespeicherten Einstellungen und Ergebnisse benutzen und sich gegenseitig überschreiben.
- **„Wo stelle ich die Preise für den Tracker ein?“** – Nicht im Tracker, sondern in den Einstellungen, Reiter „Preise & Listing“, Karte „Preise“ (Hinweis dort: „gilt beim Listen und im Tracker“).

### Probleme und Lösungen

| Problem | Lösung |
|---|---|
| Fenster „Für den Tracker brauchst du die Ultimate-Mitgliedschaft.“, nach „OK“ ist die Seite leer | Trotz des Wortlauts kein Hinweis auf eine Zusatzbuchung. Es heißt: nicht angemeldet, Zugang abgeschaltet oder Abo gesperrt. Im Dashboard nachsehen (Anmeldung, Karte „Dein Abo“), anmelden, dann den Tracker-Tab schließen und über die Seitenleiste neu öffnen. Hilft das nicht: Hintergrunddienst aktualisieren (Chrome komplett neu starten oder in `chrome://extensions` bei Cash Lister auf den Kreispfeil „Neu laden“ klicken, `konto-und-installation.md`, Abschnitt 17). Bleibt es so: Betreiber fragen. |
| Im Fenster „Upload-Einstellungen“ stehen „Angebot beenden“ und bei „Feste Menge“ eine „5“, obwohl du etwas anderes eingestellt hast | Die Seite hat beim Öffnen keine Antwort vom Hintergrunddienst bekommen und deine gespeicherten Upload-Einstellungen deshalb nicht angezeigt. In diesem Zustand werden Änderungen im Fenster **nicht gespeichert**, und die Vorschau zeigt nicht das, was wirklich hochgeladen würde. Hintergrunddienst aktualisieren (siehe Zeile darüber), Tracker neu öffnen und erst einen Lauf starten, wenn im Fenster deine Werte stehen. |
| „Tracker“ in der Seitenleiste ist grau | Nicht angemeldet, Zugang abgeschaltet oder Abo gesperrt. Unten in der Seitenleiste steht, was los ist („Nicht angemeldet“, „Zugang abgeschaltet“, „Abo gesperrt“). Im Dashboard klären. |

---

## 4. Die Seite von oben nach unten

| Bereich | Was du dort siehst | Mehr dazu |
|---|---|---|
| Seitenleiste links | „Cash Lister“, die Module (Eintrag „Tracker“ ist markiert), unten Server-Stand und Version (z. B. „Version 46.0“) | `dashboard.md` |
| Kopf | „Tracker“ / „Preise & Bestand mit Amazon abgleichen“, rechts der Knopf „**Upload-Einstellungen**“ | [Abschnitt 11](#11-das-fenster-upload-einstellungen) |
| Lauf-Karte, erste Zeile | Knopf „**Angebote von eBay laden**“, „oder“, ein Dateifeld, rechts die Anzeige „**Bericht:** …“ mit einem Papierkorb (Hinweis beim Drüberfahren: „Geladene Zeilen leeren“) | [Abschnitt 5](#5-angebote-laden-von-ebay-oder-als-eigene-datei) |
| Lauf-Karte, zweite Zeile | „**Laufzeit:** 00:00“, „**Verarbeitet:** 0“ (Hinweis: „In diesem Lauf verarbeitete Artikel“), rechts „**Gleichzeitig**“, „**Ab Artikel**“, „**Pausieren**“, „**Lauf starten**“ | [Abschnitte 7](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen) und [8](#8-gleichzeitig-wie-viele-artikel-gleichzeitig-geprüft-werden) |
| Lauf-Karte, dritte Zeile | Haken „**Dauerhaft wiederholen**“, Feld „**Pause** … **Minuten**“ | [Abschnitt 15](#15-automatik-dauerhaft-wiederholen-247) |
| Karte „**Filter**“ („Welche Angebote aus dem Bericht geprüft werden“) | „Lieferant“, „eBay-Seite“, „Preis endet auf (Cent, mit Komma getrennt)“ | [Abschnitt 6](#6-die-karte-filter) |
| Karte „**Google Sheets**“ („Duplikat-Abgleich mit deinen Shop-Sheets“) | drei Felder für Google Sheets | [Abschnitt 17](#17-die-karte-google-sheets-duplikat-abgleich) |
| Karte „**Verarbeitete Artikel**“ mit Anzahl in Klammern, rechts „neueste oben · „Status“ anklicken sortiert“ | die Ergebnistabelle; leer steht dort „Noch keine Artikel verarbeitet.“ | [Abschnitt 9](#9-die-tabelle-verarbeitete-artikel-und-die-status-texte) |
| Meldungen unten rechts | kleine Kästchen mit Uhrzeit, dunkelblau = Information, rot = Problem | [Abschnitt 20](#20-alle-meldungen-des-trackers) |

Dazu kommen drei Einblendungen, die nur bei Bedarf erscheinen:
- das Fenster „Upload-Einstellungen“ ([Abschnitt 11](#11-das-fenster-upload-einstellungen)),
- das Fenster „⏳ Kurz warten!“ bei einer Amazon-Sperre ([Abschnitt 16](#16-schutz-bei-sperren-und-fehlern-kurz-warten-und-notbremse)),
- „Bericht wird eingelesen … (Anzahl)“ über der ganzen Seite, während ein Bericht eingelesen wird ([Abschnitt 5](#5-angebote-laden-von-ebay-oder-als-eigene-datei)).

**Gespeichert wird automatisch.** Einen Speichern-Knopf für die Hauptseite gibt es nicht:
- „Lieferant“, „eBay-Seite“ und „Dauerhaft wiederholen“ werden sofort beim Ändern gespeichert, „Pause … Minuten“ schon beim Tippen.
- „Gleichzeitig“, „Preis endet auf …“ und „Ab Artikel“ werden gespeichert, sobald du das Feld verlässt (bei „Gleichzeitig“ auch sofort beim Klick auf die kleinen Pfeile im Feld).
- Ausnahme: „Keiner“ bei „Lieferant“ und „Keine“ bei „eBay-Seite“ gelten nur, solange die Seite offen ist. Beim nächsten Öffnen stehen dort wieder „Amazon“ bzw. das Land aus „Domain“ ([Abschnitt 6](#6-die-karte-filter)).
- Die drei Google-Sheet-Felder werden beim Tippen gespeichert.
- Die Upload-Einstellungen werden im Fenster sofort gespeichert ([Abschnitt 11](#11-das-fenster-upload-einstellungen)).
- Die Ergebnistabelle und die Position („Ab Artikel“) bleiben nach dem Schließen erhalten.
- **Nicht** erhalten bleibt der geladene Bericht. Nach dem Schließen oder Neuladen der Tracker-Seite steht wieder „Bericht: keine geladen“, und du musst die Angebote neu laden.

---

## 5. Angebote laden: von eBay oder als eigene Datei

Bevor der Tracker etwas prüfen kann, braucht er die Liste deiner aktiven eBay-Angebote. Dafür gibt es zwei Wege. Erst danach wird „Lauf starten“ klickbar.

### 5.1 Automatisch: „Angebote von eBay laden“

**Was passiert, wenn du klickst:**

1. Im Hintergrund öffnet sich ein Tab mit der eBay-Berichtsseite für Downloads (Adresse `ebay.<dein Land>/sh/reports/downloads`). Welches eBay-Land, richtet sich nach „Domain“ in den Einstellungen (Reiter „Preise & Listing“).
2. Die Extension schließt ein eventuelles Willkommens-Fenster von eBay, wählt als Berichtsart die Angebote, und zwar **alle aktiven**, und lässt eBay einen neuen Bericht erstellen. Der Tab-Titel zeigt dabei „Bericht wird erstellt…“, am Ende „Bericht fertig“.
3. Sie wartet, bis eBay den Bericht fertig hat – **bis zu 10 Minuten**. Bei vielen Angeboten kann das dauern.
4. Der Bericht wird direkt in den Tracker übernommen. Im Dateifeld steht dann ein Name wie „eBay_active_listings_2026-10-26.csv“. Er wird **nicht** in deinem Download-Ordner gespeichert.
5. Der Hilfs-Tab schließt sich wieder – auch wenn etwas schiefging.
6. Der Tracker liest die Datei ein: Über der ganzen Seite steht „Bericht wird eingelesen … (Anzahl)“, über der Anzeige „Bericht:“ dreht sich ein Ladekreis. Danach steht dort z. B. „Bericht: 1.234 Zeilen geladen“, und „Lauf starten“ und „Pausieren“ werden klickbar.
7. Gleichzeitig passiert beim Laden: Google-Sheet-Abgleich ([Abschnitt 17](#17-die-karte-google-sheets-duplikat-abgleich)), Abgleich der Produkt-Vergabe ([Abschnitt 18](#18-produkt-vergabe-beim-laden-der-angebote)), und die Vergleichswerte für „nur Änderungen hochladen“ werden gesetzt ([Abschnitt 12.2](#12-hochladen-zu-ebay)). Dazu erscheinen Meldungen unten rechts. Das Dashboard merkt sich außerdem Größe und Zeitpunkt des Berichts ([Abschnitt 19](#19-der-tracker-im-dashboard)).

Wichtig:
- Du musst im selben Chrome-Profil bei eBay angemeldet sein.
- Jeder Klick lässt eBay einen **neuen** Bericht erstellen. In deiner eBay-Berichtsliste (Downloads) erscheint dann jeweils ein neuer Eintrag – das ist normal.
- Klick nicht mehrmals hintereinander. Warte die Meldungen ab.
- Klick nicht, **während ein Lauf läuft** (vorher „Pausieren“). Das Neu-Einlesen ersetzt die Liste, die der Lauf gerade abarbeitet, und kann ihn vorzeitig beenden – dann wird mit einem Teilergebnis hochgeladen.

### 5.2 Von Hand: eigene CSV-Datei wählen

Neben „oder“ steht ein Dateifeld (nimmt nur `.csv`). Damit kannst du einen Bericht wählen, den du selbst bei eBay heruntergeladen hast.

1. Bei eBay im Seller Hub unter Berichte → Downloads einen Bericht über **alle aktiven Angebote** erstellen und herunterladen ([Abschnitt 14.2](#14-die-ebay-berichtsseiten-downloads-und-uploads)).
2. Im Tracker auf das Dateifeld klicken und die Datei wählen.
3. Der Tracker liest sie sofort ein (wie oben ab Schritt 6).

Der Tracker sucht in der Datei diese Spalten (Überschriften genau so geschrieben):
- „Item number“ (eBay-Artikelnummer) – ohne sie kann nichts geändert werden
- „Custom label (SKU)“ (SKU) – ohne sie wird kein Angebot übernommen
- „Start price“ (aktueller Preis) – für den Vergleich „nur Änderungen hochladen“ und den Filter „Preis endet auf …“
- „Listing site“ (Marktplatz) – für den Filter „eBay-Seite“
- eine Spalte mit „Quantity“ im Namen (Menge) – für den Vergleich „nur Änderungen hochladen“

Ob die Spalten mit Komma oder Semikolon getrennt sind, erkennt der Tracker selbst.

**Nicht sicher belegt:** wie der passende Bericht in der eBay-Oberfläche genau heißt und ob eBay die Spaltenüberschriften in jedem Konto genau so benennt. Am sichersten ist „Angebote von eBay laden“ – damit bekommst du automatisch den richtigen Bericht.

### 5.3 Welche Angebote übernommen werden

Beim Einlesen filtert der Tracker. Übernommen werden nur Angebote, die **alle** diese Bedingungen erfüllen:

1. **Lieferant passt:** Bei „Lieferant“ = „Amazon“ muss die SKU wie eine Cash-Lister-SKU aussehen (endet auf „==“). Angebote mit anderer oder leerer SKU fallen raus – sie werden weder geprüft noch geändert.
2. **Marktplatz passt:** Die Spalte „Listing site“ muss zur Auswahl bei „eBay-Seite“ passen. Bei „Keine“ wird nicht nach Marktplatz gefiltert (aber siehe Warnung in [Abschnitt 6.2](#6-die-karte-filter)).
3. **Preisendung passt:** nur wenn bei „Preis endet auf …“ etwas eingetragen ist ([Abschnitt 6.3](#6-die-karte-filter)).

Änderst du „Lieferant“, „eBay-Seite“ oder „Preis endet auf …“, liest der Tracker die zuletzt geladene Datei sofort neu ein – mit den neuen Filtern. Dabei laufen auch Sheet- und Vergabe-Abgleich noch einmal (du siehst die Meldungen erneut). Ändere die Filter deshalb nur, wenn gerade **kein Lauf** läuft.

### 5.4 Die Anzeige „Bericht“ und der Papierkorb

- Zeigt, wie viele Angebote nach den Filtern übrig sind: „Bericht: 1.234 Zeilen geladen“ oder „Bericht: keine geladen“.
- Der Papierkorb daneben (Hinweis: „Geladene Zeilen leeren“) leert die geladene Liste und setzt „Ab Artikel“ auf 0. Es gibt **keine Rückfrage**. Die Ergebnistabelle bleibt dabei erhalten. Nicht während eines Laufs benutzen.
- War „Lauf starten“ vor dem Leeren klickbar, bleibt der Knopf klickbar. Klickst du darauf, kommt „Keine Zeilen zum Verarbeiten – lade zuerst einen Angebotsbericht.“ Ausnahme: Stehen in der Tabelle noch Zeilen mit „ERROR_503“, prüft der Klick nur diese Zeilen noch einmal und lädt danach hoch ([Abschnitt 7.5](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)).
- Der geladene Bericht wird **nicht** gespeichert. Nach dem Schließen oder Neuladen der Tracker-Seite steht wieder „keine geladen“.

### Häufige Fragen

- **„Wie lange dauert ‚Angebote von eBay laden‘?“** – Das hängt davon ab, wie schnell eBay den Bericht erstellt. Der Tracker wartet bis zu 10 Minuten.
- **„Warum steht bei ‚Bericht‘ eine kleinere Zahl, als ich Angebote bei eBay habe?“** – Weil nur Angebote übernommen werden, die von Cash Lister gelistet wurden (SKU endet auf „==“) und zum Marktplatz (und ggf. zur Preisendung) passen. Von Hand eingestellte Angebote fehlen absichtlich. Das Dashboard zählt dagegen alle Zeilen des Berichts ([Abschnitt 19](#19-der-tracker-im-dashboard)).
- **„Muss ich vor jedem Lauf neu laden?“** – Für aktuelle Zahlen ja: Der Tracker vergleicht mit den Mengen und Preisen aus dem Bericht. Ein alter Bericht kennt neue Verkäufe nicht. Im Dauerbetrieb holt der Tracker den Bericht vor jedem Lauf selbst neu ([Abschnitt 15](#15-automatik-dauerhaft-wiederholen-247)).

### Probleme und Lösungen

Alle Fehler beim Laden erscheinen als rote Meldung, die mit „Fehler beim CSV-Download:“ beginnt. Dahinter steht der Grund:

| Grund nach „Fehler beim CSV-Download:“ | Ursache und Lösung |
|---|---|
| „Keine eBay-Domain eingestellt (Einstellungen → Preise & Listing → „Domain“).“ | In den Einstellungen, Reiter „Preise & Listing“, Karte „Listing“, bei „Domain“ dein eBay-Land wählen (nicht „Keine“). |
| „eBay hat auf eine andere Seite umgeleitet (…) - vermutlich bist du dort nicht angemeldet.“ | Bei eBay (im selben Chrome-Profil) anmelden, dann erneut klicken. Stimmt die „Domain“? Bei falschem Land bist du dort evtl. nicht angemeldet. |
| „eBay lieferte eine HTML-Seite statt des Berichts (Anmeldung abgelaufen?)“ | eBay-Anmeldung abgelaufen. Bei eBay neu anmelden, erneut klicken. |
| „Zeitüberschreitung beim Warten auf: neue Berichtszeile“ | eBay hat den Bericht nicht innerhalb von 10 Minuten fertig gemeldet. Später noch einmal versuchen. Auf der eBay-Seite Berichte → Downloads nachsehen, ob der Bericht doch noch fertig wurde – dann kannst du ihn herunterladen und über das Dateifeld laden. |
| „Zeitüberschreitung beim Warten auf: …“ mit „Knopf „Herunterladen“ im Banner“, „Auswahl „Quelle““, „Option „Quelle: Angebote““, „Auswahl „Typ““, „Option „Alle Angebote““, „Berichtstabelle“ oder „Knopf „Bericht erstellen““ | Die Extension hat auf der eBay-Berichtsseite einen Knopf nicht gefunden. Häufig: nicht angemeldet, oder eBay zeigt gerade eine andere Seite oder einen Hinweis. Selbst `ebay.<Land>/sh/reports/downloads` öffnen und schauen, was dort steht. Tritt es dauerhaft auf, hat eBay vermutlich die Seite geändert → Betreiber informieren (mit Screenshot). |
| „Abruf des Berichts fehlgeschlagen, Status <Nummer>“, „Der Bericht von eBay kam leer zurueck“ oder „Der Bericht kam ohne Inhalt zurueck (kein CSV in der Antwort der eBay-Seite).“ | eBay hat den Bericht nicht ausgeliefert. Erneut versuchen; sonst den Bericht von Hand herunterladen und über das Dateifeld laden. |
| „Die eBay-Berichtsseite meldet sich nicht (…).“, „Keine Antwort von der eBay-Seite innerhalb von … s“ oder „Die eBay-Seite hat leer geantwortet“ | Die eBay-Seite hat nicht reagiert. Erneut versuchen. Wiederholt es sich: Hintergrunddienst aktualisieren (Chrome komplett neu starten). |
| „… (keine Antwort vom Hintergrund)“ oder „Der Hintergrund hat geantwortet, aber ohne Ergebnis: …“ | Der Hintergrunddienst der Extension hat nicht geantwortet. Chrome komplett neu starten bzw. in `chrome://extensions` bei Cash Lister „Neu laden“ klicken, Tracker neu öffnen. |

| Problem | Ursache und Lösung |
|---|---|
| Nach dem Laden steht „Bericht: keine geladen“ | Kein Angebot hat die Filter überstanden. Prüfen: „Lieferant“ auf „Amazon“? „eBay-Seite“ richtig? Steht bei „Preis endet auf …“ etwas (dann leeren)? Hast du die richtige Datei gewählt? **Nicht sicher belegt:** welche Werte eBay in der Spalte „Listing site“ genau einträgt – passt dort nichts zu deiner Auswahl, bleibt die Liste leer. |
| „Lauf starten“ bleibt grau | Es sind keine Angebote geladen, oder ein Lauf ist gerade fertig geworden ([Abschnitt 7.7](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)). „Angebote von eBay laden“ oder eine Datei wählen. |

---

## 6. Die Karte „Filter“

Die Karte „Filter“ steht unter der Lauf-Karte. Untertitel: „Welche Angebote aus dem Bericht geprüft werden“.

### 6.1 „Lieferant“

| | |
|---|---|
| **Was es macht** | Legt fest, von welchem Lieferanten die Produkte stammen. Danach erkennt der Tracker, welche Angebote zu Cash Lister gehören. |
| **Auswahl** | „Keiner“, „Amazon“ |
| **Standard** | „Amazon“ |
| **Sinnvoll** | Immer „Amazon“. |
| **Typischer Fehler** | „Keiner“ gewählt: Dann wird beim Laden nicht gefiltert, aber beim Lauf bekommt **jedes** Angebot den Status „Skipped“ (übersprungen) – es wird nichts geprüft und nichts geändert. |
| **Wird gemerkt** | „Amazon“ ja. „Keiner“ gilt nur, solange die Tracker-Seite offen ist: Beim nächsten Öffnen steht wieder „Amazon“. |

### 6.2 „eBay-Seite“

| | |
|---|---|
| **Was es macht** | Der eBay-Marktplatz, um den es geht. Davon hängen vier Dinge ab: (1) welche Angebote aus dem Bericht übernommen werden (Spalte „Listing site“), (2) **auf welcher Amazon-Seite** geprüft wird, (3) **zu welcher eBay-Seite** hochgeladen wird, (4) wohin die Links in der Ergebnistabelle führen. |
| **Auswahl** | „Keine“, „USA“, „Kanada“, „Großbritannien“, „Australien“, „Deutschland“, „Frankreich“, „Italien“, „Spanien“ |
| **Standard** | Wurde noch nie etwas gewählt, nimmt der Tracker das Land aus „Domain“ in den Einstellungen; passt das nicht, „USA“. |
| **Wird gemerkt** | Ein Land ja. „Keine“ gilt nur, solange die Tracker-Seite offen ist: Beim nächsten Öffnen steht wieder das Land aus „Domain“ (bzw. „USA“). |
| **Zuordnung** | USA → amazon.com / ebay.com · Kanada → amazon.ca / ebay.ca · Großbritannien → amazon.co.uk / ebay.co.uk · Australien → amazon.com.au / ebay.com.au · Deutschland → amazon.de / ebay.de · Frankreich → amazon.fr / ebay.fr · Italien → amazon.it / ebay.it · Spanien → amazon.es / ebay.es |
| **Wechselwirkung** | Sollte zu „Domain“ in den Einstellungen passen. „Angebote von eBay laden“ holt den Bericht vom Land aus „Domain“, hochgeladen wird aber zum Land aus „eBay-Seite“. Stehen dort verschiedene Länder, landen die Änderungen auf der falschen eBay-Seite. |
| **Typischer Fehler** | **„Keine“ nicht verwenden.** Bei „Keine“ prüft der Tracker auf amazon.com und lädt zu ebay.com hoch. Für eBay Niederlande gibt es im Tracker keine Auswahl: Steht in den Einstellungen „Domain“ auf „NL“, zeigt „eBay-Seite“ beim ersten Öffnen „USA“ an. |

### 6.3 „Preis endet auf (Cent, mit Komma getrennt)“

| | |
|---|---|
| **Was es macht** | Übernimmt nur Angebote, deren aktueller eBay-Preis (Spalte „Start price“ im Bericht) auf eine der eingetragenen Cent-Endungen endet. Mehrere Endungen mit Komma trennen, z. B. „99,95“ (heißt: Endung ,99 oder ,95). Im leeren Feld steht als Beispiel „99,97,95,00,95,49“. |
| **Standard** | leer = kein Filter (alle Angebote) |
| **Wann gilt es** | Sobald du das Feld verlässt; die zuletzt geladene Datei wird dann sofort neu eingelesen. |
| **Wann sinnvoll** | Wenn du nur einen Teil deines Bestands prüfen willst und deine Cash-Lister-Angebote an einer besonderen Preisendung erkennbar sind. |
| **Typischer Fehler** | Etwas eingetragen und vergessen → es werden plötzlich viel weniger oder gar keine Angebote geladen. Im Zweifel leer lassen. |

**Endungen mit einer Null am Ende greifen nicht.** Der Tracker liest den Preis als Zahl ein, dabei fällt eine Null am Ende weg: aus 19.90 wird 19.9, aus 20.00 wird 20. Endungen wie „90“, „50“ oder „00“ (auch die „00“ aus dem Beispiel im Feld) finden deshalb kein Angebot. Endungen wie „99“, „95“ oder „49“ funktionieren. Rein rechnerisch passt für die Endung ,90 die Eingabe „9“ und für ,50 die Eingabe „5“ (weil aus 19.90 die Zahl 19.9 wird). Für glatte Preise (,00) gibt es keine passende Eingabe.
Steht der Preis im Bericht mit Komma statt Punkt (z. B. „19,99“), greift **keine** Endung, und es wird gar nichts geladen.
**Nicht sicher belegt:** ob eBay im Bericht Preise mit Punkt oder mit Komma schreibt. Probier den Filter deshalb einmal aus und schau, ob bei „Bericht:“ die erwartete Zahl steht.

---

## 7. Ein Lauf: starten, pausieren, fortsetzen, abbrechen

### 7.1 Einen Lauf starten

1. Angebote laden ([Abschnitt 5](#5-angebote-laden-von-ebay-oder-als-eigene-datei)).
2. In der Karte „Filter“ prüfen: „Lieferant“ = „Amazon“, „eBay-Seite“ = dein Marktplatz.
3. „Gleichzeitig“ einstellen (Standard 5).
4. „Ab Artikel“ prüfen – für einen kompletten Lauf „0“ ([Abschnitt 7.4](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)).
5. Knopf „Upload-Einstellungen“: prüfen, ob „Menge auf 0 setzen“ oder „Angebot beenden“ gewählt ist und ob „Feste Menge“ stimmt. **Am Ende des Laufs wird automatisch hochgeladen.**
6. „Lauf starten“ klicken.

**Achtung:** Ein neuer Lauf **leert die Tabelle „Verarbeitete Artikel“**. Die Tabelle bleibt nur in diesen Fällen stehen:
- Fortsetzen nach „Pausieren“, nach dem Fenster „⏳ Kurz warten!“ oder nach der Notbremse (der Lauf steht mitten in der Liste),
- „Lauf starten“ nach einem fertigen Lauf, wenn in der Tabelle noch Zeilen mit „ERROR_503“ stehen – dann werden nur diese Zeilen erneut geprüft ([Abschnitt 7.5](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)).

Eine Möglichkeit, die Ergebnistabelle als Datei zu speichern, gibt es auf der Tracker-Seite nicht mehr (schon seit Version 45.5).

### 7.2 Was bei jedem Artikel passiert

1. Der Tracker nimmt das nächste Angebot aus der Liste.
2. Er öffnet die Amazon-Produktseite (Adresse wie `amazon.de/dp/ASIN`) in einem **Hintergrund-Tab direkt neben dem Tracker-Tab**. Dieser Arbeits-Tab lädt nur den Text der Seite, ohne Bilder und Gestaltung – deshalb sieht er „kaputt“ aus. Das ist gewollt und spart Zeit und Speicher.
3. Der Tracker wartet bis zu 45 Sekunden, bis die Seite geladen ist, und dann bis zu 30 Sekunden auf die gelesenen Daten.
4. Er liest: lieferbar?, Lieferzeit, Versand durch Amazon/Prime, kostenloser Versand, Preis, Marke und ob die Seite wirklich zur ASIN gehört.
5. Der Tab bleibt nach dem Auslesen noch einen kurzen Moment offen (fest, unter einer Sekunde, nicht einstellbar) und schließt sich dann. (Bleibt doch einmal einer hängen, räumt die Extension ihn nach etwa 5 bis 8 Minuten selbst weg.)
6. Eine Zeile mit dem Ergebnis erscheint oben in der Tabelle „Verarbeitete Artikel“ (kurz farbig hervorgehoben).
7. Der Tracker nimmt das nächste Angebot.

So viele Artikel, wie bei „Gleichzeitig“ steht, laufen dabei parallel ([Abschnitt 8](#8-gleichzeitig-wie-viele-artikel-gleichzeitig-geprüft-werden)).

Sind alle Angebote geprüft, ist der Lauf fertig. Dann lädt der Tracker die Änderungen hoch ([Abschnitt 12](#12-hochladen-zu-ebay)) und plant – wenn „Dauerhaft wiederholen“ an ist – den nächsten Lauf ([Abschnitt 15](#15-automatik-dauerhaft-wiederholen-247)).

### 7.3 Die Anzeigen während des Laufs

- **„Laufzeit:“** zählt die Laufzeit des Laufs, z. B. „Laufzeit: 12:34“ (Minuten:Sekunden; Minuten können über 60 gehen, z. B. „Laufzeit: 125:30“).
- **„Verarbeitet:“** zählt die Artikel, die seit dem letzten Klick auf „Lauf starten“ geprüft wurden.
- **„Ab Artikel“** zeigt die aktuelle Position in der Liste.
- **„Verarbeitete Artikel (Anzahl)“** zeigt, wie viele Ergebnisse in der Tabelle stehen.

Bei **jedem** Start beginnen „Laufzeit“ und „Verarbeitet“ wieder bei 0 – also auch, wenn du nach „Pausieren“ mit „Lauf starten“ fortsetzt, und nach einer automatischen Sperr-Pause ([Abschnitt 16.1](#16-schutz-bei-sperren-und-fehlern-kurz-warten-und-notbremse)). Das ist normal, die Ergebnisse in der Tabelle bleiben erhalten. Wie viel insgesamt geschafft ist, siehst du an „Ab Artikel“ und an der Anzahl bei „Verarbeitete Artikel“.

**Die Laufzeit bleibt am Ende nicht stehen.** Nach einem fertigen Lauf und nach der Notbremse zählt „Laufzeit“ weiter, bis du den nächsten Lauf startest (oder „Pausieren“ klickst). Ob ein Lauf fertig ist, erkennst du an anderen Zeichen ([Abschnitt 7.7](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)). Bei „Pausieren“ und bei „⏳ Kurz warten!“ bleibt die Laufzeit stehen.

### 7.4 „Ab Artikel“: wo der Lauf beginnt

| | |
|---|---|
| **Wo** | Lauf-Karte, zweite Zeile, direkt neben „Pausieren“ und „Lauf starten“ (farbig hinterlegt). |
| **Was es macht** | Position in der geladenen Liste, ab der der nächste Lauf beginnt. Gezählt wird ab 0: „0“ = erstes Angebot, „500“ = ab dem 501. Angebot. |
| **Standard** | 0 |
| **Verhalten** | Das Feld zählt während des Laufs mit und zeigt immer, wo der Tracker gerade ist. Der Wert wird gespeichert. Ein eingetippter Wert gilt, sobald du das Feld verlässt (z. B. auf „Lauf starten“ klickst). |
| **Wann sinnvoll** | Wenn ein Lauf mittendrin abgebrochen wurde und du an einer bestimmten Stelle weitermachen willst. |
| **Typischer Fehler 1** | Nach einer Pause oder einem Abbruch steht hier eine Zahl mitten im Bestand. Lädst du neue Angebote und drückst „Lauf starten“, macht der Tracker **an dieser Stelle weiter** statt von vorne. |
| **Typischer Fehler 2** | Auch nach einem **vollständig beendeten** Lauf bleibt hier die Zahl stehen (die Anzahl der zuletzt geprüften Angebote, z. B. „1000“). Lädst du danach einen neuen Bericht, der **mehr** Angebote enthält (z. B. 1010), beginnt der nächste Lauf an dieser Stelle – geprüft werden dann nur die letzten 10 Angebote. Nur wenn die neue Liste gleich lang oder kürzer ist, fängt „Lauf starten“ von selbst wieder bei 0 an. |
| **Darum** | **Vor jedem kompletten Lauf von Hand „0“ eintragen** (und das Feld verlassen, z. B. auf „Lauf starten“ klicken). Im Dauerbetrieb musst du das nicht: Dort beginnt jeder automatische Lauf selbst bei 0 ([Abschnitt 15](#15-automatik-dauerhaft-wiederholen-247)). |
| **Wechselwirkung** | Die Position bezieht sich auf die gefilterte Liste. Änderst du Filter, ändert sich auch, welches Angebot an Position 500 steht. Liegt die eingetragene Zahl hinter dem Ende der neu geladenen Liste, setzt der Tracker sie beim Start auf 0 – außer es stehen noch Zeilen mit „ERROR_503“ in der Tabelle (dann siehe [Abschnitt 7.5](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)). |

### 7.5 Pausieren und fortsetzen

- **„Pausieren“** hält den Lauf an. Artikel, die gerade geprüft werden, werden noch fertig, dann stoppt der Tracker. Die Laufzeit bleibt stehen. Ein geplanter Lauf im Dauerbetrieb wird ebenfalls abgesagt.
- Beim Pausieren wird **nichts hochgeladen**.
- **„Lauf starten“** setzt an der aktuellen Position („Ab Artikel“) fort (Hinweis beim Drüberfahren: „Nach einer Pause geht der Lauf an derselben Stelle weiter“). Die Tabelle bleibt erhalten. Artikel, die zuvor wegen einer Amazon-Sperre nicht geprüft werden konnten (Status mit „ERROR_503“), werden dabei zuerst noch einmal geprüft. „Laufzeit“ und „Verarbeitet“ beginnen dabei wieder bei 0.
- Eine Änderung bei „Gleichzeitig“ wirkt erst beim nächsten „Lauf starten“.
- Läuft der fortgesetzte Lauf bis zum Ende, wird ganz normal hochgeladen – mit allen Ergebnissen der Tabelle, auch denen von vor der Pause.
- **Sonderfall nach einem fertigen Lauf** (sobald „Lauf starten“ wieder klickbar ist, [Abschnitt 7.7](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)): Stehen in der Tabelle noch Zeilen mit „ERROR_503“, startet „Lauf starten“ **keinen neuen Lauf**, sondern prüft nur diese Zeilen noch einmal. Danach wird hochgeladen. Willst du stattdessen einen ganz neuen Lauf: vor dem Klick bei „Ab Artikel“ „0“ eintragen.
- Das gilt auch direkt nach dem Öffnen der Seite: Stehen gespeicherte Ergebnisse mit „ERROR_503“ in der Tabelle, ist „Lauf starten“ schon klickbar, bevor du Angebote geladen hast, und prüft dann nur diese Zeilen. Anschließend wird die **ganze gespeicherte Tabelle** hochgeladen (ohne geladenen Bericht gibt es keine Vergleichswerte, alle Zeilen gelten als geändert, [Abschnitt 12.2](#12-hochladen-zu-ebay)). Lade deshalb vorher lieber mit „Angebote von eBay laden“ einen frischen Bericht.

### 7.6 Abbrechen

Einen eigenen Stopp-Knopf gibt es nicht. So brichst du einen Lauf ab:

1. „Pausieren“ klicken und warten, bis keine Amazon-Tabs mehr aufgehen.
2. Willst du beim nächsten Mal von vorne beginnen: bei „Ab Artikel“ „0“ eintragen.

Die Ergebnistabelle lässt sich nicht von Hand leeren. Sie wird beim nächsten **neuen** Lauf automatisch geleert.

Auch das Schließen des Tracker-Tabs beendet die Arbeit. Bereits geprüfte Ergebnisse und die Position bleiben gespeichert (gespeichert wird alle paar Sekunden, die allerletzten Ergebnisse können fehlen). Hochgeladen wird dann nichts. Wie du danach weitermachst, steht in [Abschnitt 7.8](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen).

### 7.7 Nach dem Lauf: woran du das Ende erkennst

Ist ein Lauf vollständig fertig, siehst du:
- unten rechts eine Meldung zum Hochladen: „✅ <Anzahl> geänderte Zeilen zu eBay hochgeladen.“, „Keine Preis-/Bestandsänderungen – Upload übersprungen.“ oder „Upload zu eBay fehlgeschlagen: …“ ([Abschnitt 12](#12-hochladen-zu-ebay)),
- bei eingeschaltetem „Dauerhaft wiederholen“ zusätzlich „Dauerbetrieb aktiv – nächster Lauf um HH:MM Uhr.“,
- „Verarbeitet“ steigt nicht mehr, „Ab Artikel“ steht auf der Zahl der geladenen Angebote,
- „Lauf starten“ ist **grau**, „Pausieren“ ist klickbar,
- im Dashboard auf der Karte „Tracker“: „fertig“ bzw. „nächster Lauf HH:MM“ ([Abschnitt 19](#19-der-tracker-im-dashboard)).

Dass „Lauf starten“ grau bleibt, ist kein Bedienfehler von dir. So geht es weiter:

1. **Empfohlen:** „Angebote von eBay laden“ klicken (oder eine Datei wählen). Danach ist „Lauf starten“ wieder klickbar – und du hast gleich frische Zahlen von eBay.
2. Bei „Ab Artikel“ „0“ eintragen ([Abschnitt 7.4](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)).
3. „Lauf starten“.

Alternativ macht ein Klick auf „Pausieren“ den Knopf „Lauf starten“ wieder klickbar. **Im Dauerbetrieb aber nicht „Pausieren“ klicken:** „Pausieren“ sagt den schon geplanten nächsten Lauf ab ([Abschnitt 15.3](#15-automatik-dauerhaft-wiederholen-247)).

**Nicht sicher belegt:** ob das Grau-Bleiben von „Lauf starten“ und das Weiterzählen der „Laufzeit“ nach einem fertigen Lauf Absicht sind. Belegt ist nur, dass es so passiert.

### 7.8 Fortsetzen nach geschlossenem Tab oder Absturz

Wurde der Tracker-Tab geschlossen, Chrome beendet oder der PC neu gestartet, **während ein Lauf lief**, zeigt das Dashboard „unterbrochen“ (z. B. „Unterbrochen bei 370 von 1.000 – im Tracker fortsetzen“). Ergebnisse und Position sind gespeichert, der geladene Bericht nicht.

**Weitermachen und die bisherigen Ergebnisse behalten:**

1. Tracker öffnen (Seitenleiste oder Dashboard-Karte „Tracker“). Die Tabelle zeigt die gespeicherten Ergebnisse, „Ab Artikel“ die gespeicherte Position.
2. „Angebote von eBay laden“ klicken (oder dieselbe Datei wie vorher wählen) und warten, bis bei „Bericht:“ die Zahl steht.
3. „Ab Artikel“ prüfen. Dort sollte noch die gespeicherte Position stehen.
4. **Einmal „Pausieren“ klicken.** Das ist wichtig: Der Lauf war beim Schließen nicht pausiert. Ohne diesen Klick gilt der nächste Start als **neuer** Lauf – er macht zwar an der gespeicherten Position weiter, **leert aber vorher die Ergebnistabelle**, und die früheren Ergebnisse werden nicht mit hochgeladen.
5. „Lauf starten“. Der Tracker prüft zuerst die Zeilen mit „ERROR_503“ noch einmal und macht dann an der Position weiter. Am Ende zählen alle Ergebnisse der Tabelle, auch die von vor dem Absturz. Hochgeladen wird wie immer nur, was sich gegenüber dem frisch geladenen Bericht geändert hat ([Abschnitt 12.2](#12-hochladen-zu-ebay)).

Hinweise:
- Die Artikel, die beim Schließen gerade in Arbeit waren (bis zu so viele, wie bei „Gleichzeitig“ steht), und die Ergebnisse der letzten Sekunden können fehlen. Sie werden beim nächsten vollständigen Lauf wieder geprüft.
- Hat sich die Angebotsliste seitdem geändert (neue oder beendete Angebote), stimmt die Position nicht mehr genau mit vorher überein.

**Einfacher, wenn dir die alten Ergebnisse egal sind:** „Angebote von eBay laden“, bei „Ab Artikel“ „0“ eintragen, „Lauf starten“ – ein ganz neuer Lauf.

War der Lauf beim Schließen **pausiert** oder von der Notbremse angehalten (Dashboard: „pausiert“ bzw. „angehalten“), brauchst du Schritt 4 nicht: Bericht laden, „Ab Artikel“ prüfen, „Lauf starten“.

### Häufige Fragen

- **„Wie lange dauert ein Lauf?“** – Hängt von der Zahl der Angebote, „Gleichzeitig“, deinem Rechner und Amazon ab. **Nicht sicher belegt:** eine verlässliche Zeit pro Artikel.
- **„Kann ich nebenbei am PC arbeiten?“** – Ja. Die Amazon-Tabs gehen ständig im Fenster des Trackers auf und zu, direkt neben dem Tracker-Tab. Ziehst du gerade einen Tab mit der Maus, kann Chrome kurz keine neuen Tabs öffnen – der Artikel bekommt dann einen vorübergehenden Fehler („Tabs cannot be edited right now …“) und wird beim nächsten Mal wieder geprüft. Tipp: Den Tracker-Tab in ein eigenes Chrome-Fenster ziehen, dann gehen die Arbeits-Tabs dort auf und nicht in dem Fenster, in dem du arbeitest.
- **„Läuft der Tracker auch, wenn das Fenster minimiert ist?“** – **Nicht sicher belegt.** Am sichersten: Fenster offen lassen, PC nicht in den Ruhezustand gehen lassen.
- **„Warum steht der Tab-Titel auf ‚⛔ Tracker angehalten – … % ohne Ergebnis‘ oder ‚⛔ Tracker angehalten – 200 Artikel in Folge nicht kaufbar‘?“** – Die Notbremse hat ausgelöst ([Abschnitt 16.2](#16-schutz-bei-sperren-und-fehlern-kurz-warten-und-notbremse)). Der Titel bleibt, bis du die Seite neu lädst.
- **„Kann ich einen Lauf erst ansehen, bevor hochgeladen wird?“** – Ja: Lauf starten, nach einigen Dutzend Artikeln „Pausieren“ klicken, Tabelle und Vorschau („Upload-Einstellungen“) ansehen, dann mit „Lauf starten“ fortsetzen. Hochgeladen wird erst am Ende des vollständigen Laufs.

### Probleme und Lösungen

| Problem | Lösung |
|---|---|
| Meldung „Keine Zeilen zum Verarbeiten – lade zuerst einen Angebotsbericht.“ | Erst Angebote laden ([Abschnitt 5](#5-angebote-laden-von-ebay-oder-als-eigene-datei)). |
| Der Lauf beginnt mitten im Bestand oder prüft nur wenige Angebote am Ende | „Ab Artikel“ stand nicht auf 0 (auch nach einem fertigen Lauf möglich, [Abschnitt 7.4](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)). „Pausieren“, „0“ eintragen, „Lauf starten“. Achtung: Ein zu früh beendeter Lauf lädt am Ende trotzdem hoch, was er geprüft hat. |
| „Lauf starten“ ist nach einem fertigen Lauf grau | Normal, siehe [Abschnitt 7.7](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen): „Angebote von eBay laden“ klicken, dann ist der Knopf wieder klickbar. |
| „Lauf starten“ prüft nur ein paar Zeilen und hört dann auf | In der Tabelle standen noch Zeilen mit „ERROR_503“; „Lauf starten“ hat nur diese erneut geprüft ([Abschnitt 7.5](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)). Für einen ganzen Lauf: „Angebote von eBay laden“, „Ab Artikel“ auf „0“, „Lauf starten“. |
| Nach einem Absturz ist die Tabelle beim neuen Start leer | Der Lauf war vor dem Schließen nicht pausiert. Beim nächsten Mal die Schritte in [Abschnitt 7.8](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen) befolgen (vor „Lauf starten“ einmal „Pausieren“). |
| Der Lauf hört nach dem Pausieren nicht sofort auf | Normal: laufende Artikel werden noch fertig geprüft (je Artikel höchstens etwa 75 Sekunden: bis 45 Sekunden Laden plus bis 30 Sekunden Lesen). |
| „Laufzeit“ zählt weiter, obwohl der Lauf fertig ist | Bekanntes Verhalten, kein Fehler im Lauf ([Abschnitt 7.3](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)). |
| Viele Amazon-Tabs gehen auf und zu | Normal. Pro gleichzeitig geprüftem Artikel ist ein Tab offen. Weniger bei „Gleichzeitig“ = weniger Tabs. |
| Die Amazon-Tabs sehen kaputt aus (keine Bilder, keine Gestaltung) | Normal – sie laden nur den Text der Seite. |
| Rechner wird langsam | „Gleichzeitig“ verringern. Die Tabelle zeigt während eines Laufs ohnehin nur die neuesten 300 Zeilen. |

---

## 8. „Gleichzeitig“: wie viele Artikel gleichzeitig geprüft werden

| | |
|---|---|
| **Wo** | Lauf-Karte, zweite Zeile, „Gleichzeitig“ (hieß früher „Threads“) |
| **Was es macht** | So viele Artikel prüft der Tracker gleichzeitig – jeder in einem eigenen Amazon-Tab. Bei 5 sind also bis zu 5 Amazon-Tabs gleichzeitig offen. |
| **Erlaubt** | 1 bis 10 |
| **Standard** | 5 |
| **Mehr** | schneller, aber mehr Last für deinen Rechner und mehr Anfragen an Amazon – Amazon reagiert dann eher mit Sperrseiten oder Sicherheitsabfragen. |
| **Weniger** | langsamer, aber schonender. |
| **Wann es wirkt** | beim nächsten „Lauf starten“ (auch nach „Pausieren“). |
| **Wird gemerkt** | Ja. Beim nächsten Öffnen steht der Wert wieder im Feld (höchstens 10). |
| **Wechselwirkung** | Derselbe Wert bestimmt auch, wie viele Prüf-Tabs der Produkt-Grabber mit „Nur Verkauf durch Amazon“ gleichzeitig öffnet (siehe `produkte-finden-und-datenbank.md` und `einstellungen.md`). Dort wirkt eine Änderung sofort. |

**Tipp (keine feste Regel):** Bekommst du oft das Fenster „⏳ Kurz warten!“ oder viele Status mit „ERROR_503“, stell weniger ein, z. B. 2 oder 3. **Nicht sicher belegt:** ein „bester“ Wert – der hängt von deinem Rechner, deiner Internetverbindung und Amazon ab.

Trag nur Zahlen von 1 bis 10 ein.

---

## 9. Die Tabelle „Verarbeitete Artikel“ und die Status-Texte

### 9.1 Die Spalten

Neueste Ergebnisse stehen oben. Neben der Überschrift steht in Klammern die Anzahl der Ergebnisse.

| Spalte | Inhalt |
|---|---|
| „Aktion“ | In der Tabelle immer „Revise“. Was beim Hochladen wirklich passiert (ändern, Menge 0, beenden, auslassen), siehst du in der Vorschau im Fenster „Upload-Einstellungen“ ([Abschnitt 11.5](#11-das-fenster-upload-einstellungen)). |
| „Artikelnummer“ | deine eBay-Artikelnummer. Ein Klick öffnet bei eBay deine aktiven Angebote, gesucht nach dieser Nummer. |
| „SKU“ | die SKU des Angebots (die Kennung von Cash Lister, endet auf „==“). Ein Klick öffnet die Amazon-Produktseite. |
| „Preis“ | **der Amazon-Preis**, nicht dein eBay-Preis! Den eBay-Preis berechnet der Tracker erst beim Hochladen ([Abschnitt 10](#10-preise-und-mengen-so-rechnet-der-tracker)). |
| „Menge“ | bei Erfolg „1“ (der Tracker liest keine Stückzahl). Die tatsächliche eBay-Menge kommt aus „Feste Menge“. |
| „Marke“ | die bei Amazon gelesene Marke |
| „Status ⬍“ | Ergebnis der Prüfung (siehe 9.2). Ein Klick auf die Überschrift sortiert ([Abschnitt 9.3](#9-die-tabelle-verarbeitete-artikel-und-die-status-texte)). |

Während eines Laufs zeigt die Tabelle nur die **neuesten 300 Zeilen**, damit die Seite flüssig bleibt. Alle Ergebnisse bleiben trotzdem erhalten und werden alle hochgeladen. Nach dem Sortieren oder Neuöffnen siehst du wieder alle Zeilen.

Lädt der Tracker gespeicherte Ergebnisse beim Öffnen, steht jede Artikelnummer nur einmal in der Tabelle (bei doppelten bleibt die neueste).

### 9.2 Die Status-Texte und was beim Hochladen passiert

Jeder Status gehört zu einer von drei Gruppen. Das entscheidet, was der Tracker bei eBay macht.

**Gruppe 1 – Erfolg**

| Status | Bedeutung | Beim Hochladen |
|---|---|---|
| „Success“ | Produkt bei Amazon lieferbar, Preis gelesen | Preis wird neu berechnet, Menge auf „Feste Menge“ gesetzt (Revise) |

**Gruppe 2 – vorübergehend (Abruf-Problem, kein Urteil über das Produkt)**

Hier konnte der Tracker die Amazon-Seite nicht sauber lesen. Er weiß also nicht, ob das Produkt lieferbar ist. Deshalb **ändert er bei eBay nichts** an diesem Angebot – es wird beim Hochladen ausgelassen und beim nächsten Lauf neu geprüft.

| Status (Beispiele) | Bedeutung |
|---|---|
| „Error: ERROR_503: IP bei Amazon gesperrt“ | Amazon hat statt der Produktseite eine Sperr- oder Fehlerseite gezeigt (z. B. Fehler 503, Seite ohne Produkt mit Amazon-Hinweis zu automatisierten Zugriffen). Auch wenn Amazon auf der Seite statt eines Preises einen Hinweis zeigt, dass kein Preis verfügbar ist, wertet der Tracker das so. |
| „Error: ERROR_503: Zeitüberschreitung beim Abruf der Produktdaten (Lieferant amazon, ASIN …)“ | Die Seite hat nicht rechtzeitig Daten geliefert. |
| „Error: ERROR_503: Tab failed to load: net::ERR_…“ | Der Tab konnte die Seite nicht laden – Internet kurz weg, Router-Neuverbindung o. Ä. |
| „Error: Zeitüberschreitung (timeout): Seite im Tab nicht fertig geladen“ | Die Seite hat länger als 45 Sekunden zum Laden gebraucht. |
| „Error: Zeitüberschreitung (timeout): keine Antwort von der Seite im Tab.“ | Die Seite hat innerhalb von 30 Sekunden keine Daten geliefert, z. B. weil Amazon eine Sicherheitsabfrage (Captcha) zeigt. |
| „Error: Netzwerkfehler beim Abruf der Amazon-Daten“ | Netzwerkproblem. Kommt im heutigen Ablauf praktisch nicht vor. |
| „Error: Tabs cannot be edited right now (user may be dragging a tab).“ | Du hast gerade einen Tab gezogen; Chrome konnte keinen neuen öffnen. |
| „The message port closed before a response was received.“, „Could not establish connection. Receiving end does not exist.“, „Unknown error“ u. Ä. | Verbindung zum Hintergrunddienst der Extension kurz abgerissen. Tritt das bei sehr vielen Zeilen auf: Hintergrunddienst aktualisieren (Chrome komplett neu starten). |
| „Skipped“ | Übersprungen, weil das Angebot nicht zum gewählten Lieferanten passt (praktisch nur, wenn „Lieferant“ auf „Keiner“ steht). Wird nicht hochgeladen. |

Nur die Status mit „**ERROR_503**“ zählen für die Sperr-Pause „⏳ Kurz warten!“ und werden beim Fortsetzen als Erstes noch einmal geprüft ([Abschnitte 7.5](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen) und [16.1](#16-schutz-bei-sperren-und-fehlern-kurz-warten-und-notbremse)). Die übrigen vorübergehenden Fehler werden beim nächsten vollständigen Lauf wieder geprüft.

**„ERROR_503: Zeitüberschreitung beim Abruf der Produktdaten …“ oder „Zeitüberschreitung (timeout): keine Antwort von der Seite im Tab.“?** Beide entstehen in derselben Lage: Die Amazon-Seite ist geladen, liefert aber innerhalb von 30 Sekunden keine Daten. Der Tracker wartet dabei auf zwei Dinge gleichzeitig, die beide nach 30 Sekunden aufgeben. Welcher der beiden Texte erscheint, hängt nur davon ab, welche Wartezeit zuerst abläuft – darauf hast du keinen Einfluss. Für dich bedeuten beide dasselbe: Das Angebot bleibt unverändert und wird beim nächsten Mal neu geprüft. Einziger Unterschied: Nur der Text mit „ERROR_503“ zählt für die Sperr-Pause und wird beim Fortsetzen zuerst wiederholt.

**Gruppe 3 – endgültig (Produkt ist nicht kaufbar)**

Der Tracker hat die Seite gelesen und festgestellt, dass das Produkt so nicht mehr zu deinen Regeln passt. Beim Hochladen wird das Angebot – je nach Einstellung „Ausverkaufte / fehlgeschlagene Artikel“ ([Abschnitt 11.3](#11-das-fenster-upload-einstellungen)) – auf **Menge 0** gesetzt oder **beendet**.

| Status | Bedeutung |
|---|---|
| „Error: Artikel bei Amazon nicht verfügbar“ | Amazon zeigt das Produkt nicht als lieferbar an. Dazu zählen auch: kein Preis lesbar, Amazon-Seite „nicht gefunden“ (Produkt gibt es nicht mehr), unbekannter Verfügbarkeitstext und **zu lange Lieferzeit** (später als „Max. verlängerte Lieferzeit“, siehe unten). |
| „Error: Lieferzeit bei Amazon verlängert“ | Lieferzeit zu lang. Kommt praktisch nicht vor: Bei zu langer Lieferzeit meldet der Tracker schon „Artikel bei Amazon nicht verfügbar“. |
| „Error: Artikel bei Amazon nicht Prime-fähig“ | Das Produkt wird nach der Prüfung nicht von Amazon versendet bzw. nicht als Prime erkannt. |
| „Error: Artikel bei Amazon ohne kostenlosen Versand“ | Im Kaufkasten steht kein kostenloser Versand. |
| „Error: ASIN passt nicht: erwartet …, erhalten …“ | Unter der Adresse zeigt Amazon ein **anderes** Produkt (andere ASIN), z. B. weil Amazon Produkte zusammengelegt oder umgeleitet hat. |
| jeder andere, hier nicht genannte Text | **Achtung:** Unbekannte Fehlertexte behandelt der Tracker ebenfalls als endgültig. Prüfe die Vorschau ([Abschnitt 11.5](#11-das-fenster-upload-einstellungen)) und melde unbekannte Texte dem Betreiber. |

Ergebnisse, die noch von einer älteren Version gespeichert sind, können englische Texte haben (z. B. „Error: Item is not available on Amazon“ oder „Error: ERROR_503: IP is blocked on Amazon“). Sie werden genauso eingeordnet wie die deutschen. Mit dem nächsten neuen Lauf verschwinden sie.

**Lieferzeit-Grenze:** Wie viele Tage Lieferzeit noch in Ordnung sind, steht in den Einstellungen, Reiter „Produkt-Filter“, Karte „Amazon-Filter“, im Feld „**Max. verlängerte Lieferzeit**“ (in Tagen, Standard 20). Der Tracker benutzt diese Zahl **immer** – auch wenn der Schalter daneben ausgeschaltet ist (der Schalter wirkt nur beim Grabber). Ist der Schalter aus, ist das Zahlenfeld ausgegraut; zum Ändern der Zahl den Schalter kurz einschalten, Zahl ändern, Schalter wieder so stellen, wie du ihn haben willst. Ein zu kleiner Wert lässt viele deiner Angebote als „nicht verfügbar“ enden. Details in `einstellungen.md`.

Belegt ist nur grob: „lieferbar“ erkennt der Tracker am Verfügbarkeitstext auf der Produktseite. Er vergleicht ihn mit einer Liste bekannter „Auf Lager“-Texte in Englisch, Deutsch, Italienisch, Spanisch und Niederländisch; eine eigene französische Liste gibt es nicht. „Kostenloser Versand“ erkennt er an bestimmten Wörtern im Kaufkasten (Buybox).
**Nicht sicher belegt:** ob diese Erkennung auf jeder Amazon-Seite und bei jedem Seitenaufbau stimmt, die genauen Merkmale für „Versand durch Amazon/Prime“ und welche Verfügbarkeitstexte von Amazon der Tracker nicht kennt. Wenn ein Produkt bei Amazon eindeutig lieferbar ist, der Tracker aber „nicht verfügbar“ meldet: Link und Status an den Betreiber schicken.

**Sicherheitsabfrage (Captcha) bei Amazon:** Zeigt Amazon eine Sicherheitsabfrage, kann der Tracker die Seite meist nicht lesen. Der Artikel läuft dann in der Regel in eine Zeitüberschreitung und zählt als vorübergehender Fehler (Gruppe 2). Stell bei häufigen Abfragen weniger bei „Gleichzeitig“ ein und mach längere Pausen.

### 9.3 Sortieren

- Klick auf die Spaltenüberschrift „Status ⬍“: Daneben dreht sich kurz ein Ladekreis, dann ist die **ganze** Tabelle nach Status sortiert.
- Ein weiterer Klick dreht die Reihenfolge um.
- So siehst du schnell, welche Status vorherrschen (z. B. nach einer Notbremse).
- Während eines Laufs kommen neue Ergebnisse trotzdem oben dazu.

### Häufige Fragen

- **„Warum steht bei ‚Preis‘ ein viel kleinerer Preis als bei eBay?“** – Das ist der Amazon-Preis. Dein eBay-Preis wird erst beim Hochladen berechnet. Schau in die Vorschau im Fenster „Upload-Einstellungen“.
- **„Was zählt ‚Fehlgeschlagen / ausverkauft insgesamt‘?“** – Diese Zahl im Fenster „Upload-Einstellungen“ zählt alle Zeilen mit „Error“ im Status oder Menge 0 – also vorübergehende **und** endgültige. Hochgeladen (als Menge 0 oder Beenden) werden davon nur die endgültigen.
- **„Werden ‚ERROR_503‘-Artikel beendet?“** – Nein. Vorübergehende Fehler ändern bei eBay nichts.
- **„Wie prüfe ich nur die fehlgeschlagenen Artikel noch einmal?“** – Einen eigenen Knopf dafür gibt es nicht mehr (schon seit Version 45.5). Zeilen mit „ERROR_503“ prüft der Tracker beim Fortsetzen und nach der Sperr-Pause von selbst zuerst. Alle anderen werden beim nächsten vollständigen Lauf geprüft.

### Probleme und Lösungen

| Problem | Lösung |
|---|---|
| Fast alle Zeilen „IP bei Amazon gesperrt“ oder „Zeitüberschreitung“ | Amazon bremst dich. „Pausieren“, weniger bei „Gleichzeitig“, später erneut. Siehe [Abschnitt 16](#16-schutz-bei-sperren-und-fehlern-kurz-warten-und-notbremse). |
| Viele „nicht verfügbar“, obwohl die Produkte bei Amazon lieferbar sind | 1. „eBay-Seite“ prüfen – bei falschem Land wird auf der falschen Amazon-Seite geprüft. 2. „Max. verlängerte Lieferzeit“ in den Einstellungen prüfen (zu kleiner Wert). 3. Einen betroffenen Link selbst öffnen (Klick auf die SKU). 4. Bleibt es unklar: Beispiele (Link + Status) an den Betreiber. Bis dahin den Lauf **pausieren**, damit nichts hochgeladen wird, oder in den Upload-Einstellungen „Menge auf 0 setzen“ wählen, damit nichts endgültig beendet wird. |
| Alle Zeilen „Skipped“ | „Lieferant“ steht auf „Keiner“. Auf „Amazon“ stellen, Bericht neu laden, „Ab Artikel“ 0, „Lauf starten“. |
| Ein Artikel steht bei jedem Lauf auf „IP bei Amazon gesperrt“, obwohl andere klappen | Möglich, dass Amazon auf dieser Seite statt eines Preises einen Hinweis zeigt, dass kein Preis verfügbar ist – das wertet der Tracker wie eine Sperre und lässt das Angebot unverändert. Seite selbst öffnen und prüfen; das Angebot ggf. von Hand bei eBay anpassen oder beenden. |
| „ASIN passt nicht“ | Amazon leitet die ASIN auf ein anderes Produkt um. Link öffnen und prüfen, ob es noch dasselbe Produkt ist. Der Tracker behandelt das als endgültig. |
| Status „Success“, aber bei „Preis“ steht eine negative Zahl (z. B. „-99999“) | Amazon hat keinen normalen Preis im Kaufkasten gezeigt (z. B. nur einen Knopf zu allen Kaufoptionen). Solche Zeilen lädt der Tracker wegen des Preis-Schutzes nicht hoch ([Abschnitt 10.5](#10-preise-und-mengen-so-rechnet-der-tracker)) – das Angebot bleibt bei eBay unverändert. Bei Bedarf selbst prüfen und von Hand anpassen. |

---

## 10. Preise und Mengen: so rechnet der Tracker

### 10.1 Woher die Preise kommen

Der Tracker hat **keine eigenen Preiseinstellungen**. Er nimmt die Preise aus den **Einstellungen, Reiter „Preise & Listing“, Karte „Preise“** (Hinweis dort: „gilt beim Listen und im Tracker“) – dieselben, mit denen auch gelistet wird:
- „% Aufschlag“
- „Fester Aufschlag (€)“
- „Variable Preise (nach Preisspanne)“ mit Regeln (Knopf „Regel“; je Regel „ab € … bis € … → …% + € …“)
- „Preisendung“ mit Schalter

Die Schalter „Als „Neu: Sonstige“ listen (Standard)“ und „NUR „Neu: Sonstige“ listen“ und der Haken „Neu: Sonstige“ in den Regeln betreffen nur das Listen, nicht den Tracker.

Änderst du dort einen Preis, nimmt ein offener Tracker die neue Einstellung sofort für die nächste Berechnung. Ausführlich zu allen Feldern: `einstellungen.md`.

### 10.2 Die Rechnung

Nur für Zeilen mit Status „Success“:

1. **Aufschlag:** Verkaufspreis = Amazon-Preis + (Amazon-Preis × „% Aufschlag“ ÷ 100) + „Fester Aufschlag (€)“
   - Ist „Variable Preise (nach Preisspanne)“ an und liegt der Amazon-Preis in einer Regel („ab“ bis „bis“, Grenzen eingeschlossen), gelten Prozent und fester Betrag dieser Regel (die erste passende Regel zählt). Passt keine Regel, gelten die normalen Werte darüber.
2. **Endung:** Ist der Schalter bei „Preisendung“ an, wird auf den nächsten vollen Euro **aufgerundet** und dann so viel abgezogen, dass die gewünschte Endung entsteht. Bei Preisendung 0 bleibt der aufgerundete volle Euro-Betrag. Ist der Schalter aus, bleibt der Preis aus Schritt 1 (auf Cent gerundet).

**Beispiel:** Amazon-Preis 18,40 €, „% Aufschlag“ 30, „Fester Aufschlag (€)“ 2, „Preisendung“ 0,99 (an):
- 18,40 + 5,52 + 2,00 = 25,92
- aufrunden → 26,00 → Endung 0,99 → **25,99 €**

Mit Preisendung 0,49 würde daraus **25,49 €** – also etwas *unter* dem errechneten Preis. Wie weit es darunter gehen kann, hängt von der Endung ab: bei 0,99 höchstens 1 Cent, bei 0,49 bis zu 0,51 €, bei sehr kleinen Endungen bis knapp 1 €. Nach oben sind es bis knapp 1 €.

**Achtung beim Feld „Preisendung“ (Einstellungen):**
- Trag die Endung als Euro-Betrag unter 1 ein, z. B. „0,99“ – **nicht** „99“. Das Feld nimmt beim Tippen auch größere Zahlen an. Der Tracker rechnet dann aber falsch nach oben: Bei „99“ landet der Preis rund 98 € über dem aufgerundeten Betrag.
- Ist das Feld leer und der Schalter daneben an, kann der Tracker keinen gültigen eBay-Preis ausrechnen. In der Vorschau steht dann bei „Preis“ „NaN“, und – solange „Preis aktualisieren“ an ist – werden alle erfolgreich geprüften Angebote beim Hochladen weggelassen (weder Preis noch Menge werden geändert). Eine eigene Meldung dazu gibt es nicht. Lösung: eine Endung eintragen oder den Schalter ausschalten (siehe `einstellungen.md`).

### 10.3 Eine Preistafel für alle Zustände

Seit Version 46.0 gibt es nur noch **eine** Preistafel. Der Tracker rechnet Angebote im Zustand „Neu“ und „Neu: Sonstige“ gleich. Die frühere zweite Preistafel „Eigene Preise für „Neu: Sonstige““ gibt es nicht mehr.

### 10.4 Menge

Der Tracker liest bei Amazon keine Stückzahl. Für lieferbare Produkte setzt er die Menge aus „Feste Menge“ (Fenster „Upload-Einstellungen“, Standard 1). Hat jemand bei eBay gekauft und die Menge ist gesunken, füllt der nächste Lauf sie wieder auf diesen Wert auf – vorausgesetzt, der geladene Bericht ist aktuell.

### 10.5 Preis-Schutz

Zeilen, bei denen ein Preis von 0 € oder weniger herauskäme (oder gar keine Zahl, siehe „Preisendung“ oben), lädt der Tracker **nie** hoch. Sie fehlen dann einfach in der Upload-Datei, das Angebot bleibt bei eBay unverändert.

Dieser Schutz prüft nur den Preis, der mitgeschickt wird. Ist „Preis aktualisieren“ aus, wird kein Preis mitgeschickt – dann geht so eine Zeile trotzdem mit der Menge hinaus.

### Häufige Fragen

- **„Kann ich im Tracker einen anderen Aufschlag als beim Listen nehmen?“** – Nein. Der Tracker nutzt immer die Preise aus den Einstellungen. Im Fenster „Upload-Einstellungen“ gibt es keine eigenen Preisfelder.
- **„Ändert der Tracker den Preis, wenn ich die Aufschläge in den Einstellungen ändere?“** – Ja, beim nächsten Hochladen bekommen alle erfolgreich geprüften Angebote den Preis nach der neuen Rechnung. Der Preis wird erst beim Hochladen berechnet – auch Zeilen, die schon in der Tabelle stehen, bekommen dann die neuen Werte.

### Probleme und Lösungen

| Problem | Lösung |
|---|---|
| In der Vorschau entsprechen die Preise fast genau dem Amazon-Preis (kein Aufschlag) | Die Preis-Einstellungen sind evtl. nie gespeichert worden. Bei einer frischen Installation zeigt die Karte „Preise“ bei „% Aufschlag“ zwar einen Wert an (z. B. „120“), für den Tracker gespeichert wird die Preistafel aber erst, wenn du in der Karte „Preise“ etwas änderst (oder Einstellungen aus einer Datei bzw. vom Server zurückholst). Bis dahin rechnet der Tracker **ohne Aufschlag** (nur Amazon-Preis plus Preisendung). So geht's: Einstellungen → Reiter „Preise & Listing“ → Karte „Preise“ → bei „% Aufschlag“ den Wert neu eintippen (z. B. löschen und wieder eingeben). Danach im Tracker die Vorschau ansehen (Knopf „Upload-Einstellungen“). Erst einen vollständigen Lauf zulassen, wenn die Preise stimmen. |
| Preise liegen knapp unter dem errechneten Wert | Wirkung der „Preisendung“ (siehe Beispiel oben). |
| In der Vorschau steht bei „Preis“ „NaN“ | Das Feld „Preisendung“ in den Einstellungen ist leer, der Schalter aber an. Endung eintragen (z. B. „0,99“) oder Schalter aus ([Abschnitt 10.2](#10-preise-und-mengen-so-rechnet-der-tracker)). Bis dahin werden erfolgreich geprüfte Angebote nicht aktualisiert. |
| Preise sind viel zu hoch (rund 98 € zu viel) | Bei „Preisendung“ steht vermutlich „99“ statt „0,99“. Korrigieren und die Vorschau prüfen, bevor ein Lauf zu Ende läuft. |
| Eine Preis-Regel greift nicht | Liegt der Amazon-Preis wirklich zwischen „ab“ und „bis“ der Regel? Ist „Variable Preise (nach Preisspanne)“ eingeschaltet? Steht bei „bis“ wirklich eine Zahl? Mehr in `einstellungen.md`. |

---

## 11. Das Fenster „Upload-Einstellungen“

**Öffnen:** oben rechts mit dem Knopf „**Upload-Einstellungen**“. **Schließen:** mit „×“ oben rechts (Hinweis „Schließen“) oder mit „Einstellungen speichern“.

**Gespeichert wird sofort** bei jeder Änderung. „Einstellungen speichern“ schließt nur das Fenster.

Die Einstellungen hier gelten für das **automatische Hochladen** am Ende jedes vollständigen Laufs. Einen Knopf zum Hochladen oder Exportieren gibt es im Fenster nicht mehr (schon seit Version 45.5).

### 11.1 „Bestand aktualisieren“

| | |
|---|---|
| **Was es macht** | An: Die Menge wird mit hochgeladen. Aus: Die Spalte Menge bleibt in der Upload-Datei leer – gedacht ist, dass eBay die Menge dann nicht ändert. **Nicht sicher belegt:** wie eBay ein leeres Feld genau behandelt. |
| **Standard** | an |
| **Wechselwirkung** | Ist es aus, wirkt auch „Menge auf 0 setzen“ nicht (die Menge wird ja nicht übertragen). „Angebot beenden“ wirkt trotzdem. |

### 11.2 „Preis aktualisieren“

| | |
|---|---|
| **Was es macht** | An: Der neu berechnete Preis wird hochgeladen. Aus: Die Spalte Preis bleibt in der Upload-Datei leer – gedacht ist, dass eBay den Preis dann nicht ändert (**nicht sicher belegt**, wie oben). |
| **Standard** | an |

**Wichtig:** Beide Haken aus ist **kein Testmodus**. Ist „Angebot beenden“ gewählt, beendet der Tracker nicht kaufbare Angebote trotzdem. Und die übrigen Zeilen werden dann als leere Änderungszeilen an eBay geschickt. **Nicht sicher belegt:** wie eBay leere Änderungszeilen behandelt. Wer nur ansehen will, hält den Lauf vor dem Ende mit „Pausieren“ an ([Abschnitt 12.1](#12-hochladen-zu-ebay)).

### 11.3 „Ausverkaufte / fehlgeschlagene Artikel“

Was mit Angeboten passiert, deren Amazon-Produkt **endgültig** nicht kaufbar ist (Gruppe 3 in [Abschnitt 9.2](#9-die-tabelle-verarbeitete-artikel-und-die-status-texte)). Vorübergehende Fehler sind davon **nie** betroffen.

| Auswahl | Wirkung bei eBay |
|---|---|
| „Menge auf 0 setzen“ | Das Angebot bekommt Menge 0 (der Preis wird nicht geändert). |
| „Angebot beenden“ | Das Angebot wird beendet (Grund „NotAvailable“). |

- **Standard:** „Menge auf 0 setzen“ (sofern nichts anderes gespeichert ist, z. B. durch „Einstellungen importieren“ oder die Server-Sicherung).
- Darunter: **„Fehlgeschlagen / ausverkauft insgesamt: Anzahl“** – zählt alle Zeilen mit „Error“ im Status oder Menge 0 (enthält auch vorübergehende Fehler, die gar nicht hochgeladen werden).

**Was ist besser?** Das ist deine Entscheidung. Belegt ist nur: Bei „Angebot beenden“ ist das Angebot weg, und der Tracker kann es später nicht wieder auffüllen. Bei „Menge auf 0 setzen“ bleibt die Möglichkeit, dass der Tracker die Menge wieder hochsetzt, wenn das Produkt erneut lieferbar ist.
**Nicht sicher belegt (eBay-Regeln, bitte bei eBay nachlesen):** was eBay mit einem Angebot mit Menge 0 macht – ob es ausgeblendet aktiv bleibt oder beendet wird, hängt nach allgemeinem Wissen von deiner eBay-Einstellung für nicht vorrätige Artikel ab – und ob solche Angebote im eBay-Bericht „alle aktiven Angebote“ weiterhin auftauchen und damit vom Tracker wieder aufgefüllt werden können.

### 11.4 „Menge“ → „Feste Menge“

| | |
|---|---|
| **Was es macht** | Diese Menge bekommt jedes erfolgreich geprüfte Angebot bei eBay. |
| **Standard** | 1 (sofern nichts anderes gespeichert ist) |
| **Sinnvolle Werte** | Ganze Zahl ab 1. Eine leere Eingabe und auch „0“ werden als 1 gespeichert. |
| **Hinweis** | Eine Option „echte Menge übernehmen“ gibt es nicht – der Tracker liest bei Amazon keine Stückzahl. |

**Nicht sicher belegt (eBay-Regeln):** ob und wie höhere Mengen bei eBay gegen dein Verkaufslimit zählen ([Abschnitt 12.5](#12-hochladen-zu-ebay)).

### 11.5 „Vorschau (erste 3 Artikel)“

Zeigt für die **ersten drei Zeilen** der Ergebnisliste (die zuerst geprüften – die Haupttabelle zeigt die neuesten oben), was hochgeladen würde. Spalten: „Aktion“, „Artikelnummer“, „SKU“, „Preis“, „Menge“, „Status“.

| „Aktion“ in der Vorschau | Bedeutung |
|---|---|
| „Revise“ mit Preis und Menge | Angebot wird geändert |
| „Revise“ mit Menge 0 und leerem Preis | endgültig nicht kaufbar, Einstellung „Menge auf 0 setzen“ |
| „End“ | endgültig nicht kaufbar, Einstellung „Angebot beenden“ |
| „Auslassen (Abruf)“ | vorübergehender Fehler oder „Skipped“ – wird nicht hochgeladen |

Bei „Preis“ siehst du hier den **berechneten eBay-Preis**. Ist „Preis aktualisieren“ oder „Bestand aktualisieren“ aus, bleibt die jeweilige Spalte leer. Ohne Ergebnisse steht dort „Noch keine verarbeiteten Artikel.“

Die Vorschau wird beim Öffnen des Fensters und bei jeder Änderung im Fenster neu berechnet. Sie zeigt alle drei Zeilen, auch wenn sich bei ihnen nichts geändert hat. Ob eine Zeile beim Hochladen wirklich dabei ist, hängt zusätzlich von „nur Änderungen“ ab ([Abschnitt 12.2](#12-hochladen-zu-ebay)).

Tipp: Weil die Vorschau die **ersten** Ergebnisse zeigt, kannst du sie schon kurz nach dem Start eines Laufs ansehen.

### Häufige Fragen

- **„Muss ich auf ‚Einstellungen speichern‘ klicken?“** – Nein, alles ist schon beim Ändern gespeichert.
- **„Wo ist ‚Update Listings To Ebay‘ bzw. ‚Export CSV‘?“** – Beide Knöpfe gibt es nicht mehr. Hochgeladen wird automatisch am Ende jedes vollständigen Laufs ([Abschnitt 12](#12-hochladen-zu-ebay)).
- **„Warum zeigt die Vorschau nur drei Zeilen?“** – Sie ist nur eine Stichprobe. Alle Zeilen siehst du in der Tabelle „Verarbeitete Artikel“; was eBay mit jeder Zeile gemacht hat, steht in der Ergebnisdatei bei eBay ([Abschnitt 14.4](#14-die-ebay-berichtsseiten-downloads-und-uploads)).

### Probleme und Lösungen

| Problem | Lösung |
|---|---|
| Im Fenster stehen „Angebot beenden“ und „5“, obwohl du anderes eingestellt hast; Änderungen bleiben nicht erhalten | Die Seite hat deine gespeicherten Einstellungen beim Öffnen nicht geladen (keine Antwort vom Hintergrunddienst). Hintergrunddienst aktualisieren, Tracker neu öffnen ([Abschnitt 3](#3-tracker-öffnen-und-voraussetzungen), Probleme). |
| Vorschau zeigt „Noch keine verarbeiteten Artikel.“ | Die Ergebnistabelle ist leer. Erst einen Lauf starten. |
| In der Vorschau steht bei „Menge“ nichts oder „NaN“ | Bei „Feste Menge“ steht keine gültige Zahl, oder „Bestand aktualisieren“ ist aus. Eine ganze Zahl ab 1 eintragen bzw. den Haken setzen. |

---

## 12. Hochladen zu eBay

### 12.1 Wann hochgeladen wird

- **Automatisch**, sobald ein Lauf **vollständig** fertig ist – also bis zum letzten Angebot durchgelaufen. Das gilt auch für den Sonderfall, in dem „Lauf starten“ nur die „ERROR_503“-Zeilen erneut prüft ([Abschnitt 7.5](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)).
- **Nicht**, solange der Lauf angehalten ist (durch „Pausieren“ oder die Notbremse) und nicht, wenn der Tab vorher geschlossen wird.
- Nach der Sperr-Pause „⏳ Kurz warten!“ geht der Lauf von selbst weiter und lädt am Ende ganz normal hoch.
- Setzt du einen pausierten Lauf mit „Lauf starten“ fort und läuft er dann bis zum Ende, wird hochgeladen – mit allen Ergebnissen der Tabelle.

Einen Schalter, um das Hochladen auszuschalten, gibt es seit Version 46.0 nicht mehr, einen Knopf, um von Hand hochzuladen, schon seit Version 45.5 nicht. Willst du nicht hochladen, halte den Lauf vor dem Ende mit „Pausieren“ an.

### 12.2 „Nur Änderungen“

Der Tracker schickt nur Zeilen, die sich wirklich ändern:
- „Revise“-Zeilen nur, wenn Preis oder Menge **anders** sind als im zuletzt geladenen eBay-Bericht bzw. als beim letzten Hochladeversuch seitdem.
- Beenden-Zeilen immer.
- Zeilen, für die es keinen Vergleichswert gibt, immer.

Ändert sich nichts: Meldung „Keine Preis-/Bestandsänderungen – Upload übersprungen.“

Wurde seit dem Öffnen der Tracker-Seite noch kein Bericht geladen, gibt es keine Vergleichswerte – dann gelten alle Zeilen als geändert.

**Wichtig:** Die Vergleichswerte merkt sich der Tracker schon beim Zusammenstellen der Upload-Datei – auch dann, wenn das Hochladen danach scheitert. Prüfst du danach erneut, **ohne** vorher einen frischen Bericht zu laden, hält der Tracker diese Änderungen für schon geschickt und lässt sie weg. Deshalb vor einem neuen Lauf immer „Angebote von eBay laden“ klicken – das setzt die Vergleichswerte auf den echten Stand bei eBay zurück.

### 12.3 Was beim Hochladen passiert

1. Der Tracker baut die Datei „update_<Datum>.csv“ (wird nicht in deinem Download-Ordner gespeichert).
2. Ein eBay-Tab öffnet sich **im Vordergrund** mit der eBay-Berichtsseite für Uploads (Adresse `ebay.<Land>/sh/reports/uploads`). Das Land richtet sich nach „eBay-Seite“ im Tracker. Die Seite muss innerhalb von 60 Sekunden laden.
3. Die Extension klickt dort „Vorlage hochladen“ (englische eBay-Seite: „Upload template“, italienische: „Carica modello“), wartet auf „Datei auswählen“ („Choose file“, „Scegli il file“) und gibt die Datei hinein.
4. Im Tab-Titel siehst du den Fortschritt: „🔍 Suche Knopf „Vorlage hochladen““, „🔍 Warte auf das Dateifeld“, „⚙️ Bereite CSV vor…“, „📤 Setze CSV ein…“, „📤 Lade Datei hoch…“, „🔍 Warte auf neue Zeile“, dann „Warte auf Ergebnisse“ mit wechselndem Symbol davor (🔄, ⏳, ⌛). („⏳ Hochladen startet“ und „📂 Öffne Dialog…“ stehen nur für einen Augenblick da.)
5. Die Extension wartet, bis eBay die Datei in der Liste zeigt (bis etwa 6 Minuten) und bis eBay fertig ist und „Ergebnisse herunterladen“ („Download results“) anbietet (bis etwa 18 Minuten).
6. Fertig: Titel „✅ Hochladen fertig!“.
   - Kam das innerhalb von etwa 90 Sekunden, schließt sich der Tab kurz danach von selbst, und im Tracker erscheint „✅ <Anzahl> geänderte Zeilen zu eBay hochgeladen.“
   - Dauert es länger, hat der Tracker schon vorher „Upload zu eBay fehlgeschlagen: unbekannt“ gemeldet, obwohl der Upload weiterläuft ([Abschnitt 12.4](#12-hochladen-zu-ebay)).
7. Fehler: Titel „❌ Hochladen fehlgeschlagen“. Der Tab **bleibt offen**, damit du siehst, was eBay anzeigt (die Extension räumt ihn erst etwa 25 bis 28 Minuten nach dem Öffnen von selbst weg). Passiert der Fehler in den ersten 90 Sekunden, erscheint im Tracker „Upload zu eBay fehlgeschlagen: …“ mit dem Grund; bei späteren Fehlern hat der Tracker schon „… unbekannt“ gemeldet.
   - Sonderfall: Bietet eBay auch nach etwa 18 Minuten kein „Ergebnisse herunterladen“ an, zeigt der Titel nur ganz kurz „❌ Hochladen fehlgeschlagen“ und springt dann zurück auf „Warte auf Ergebnisse“. Steht dort also länger als etwa 18 Minuten „Warte auf Ergebnisse“, wartet die Extension nicht mehr wirklich – sieh selbst auf der eBay-Upload-Seite nach ([Abschnitt 14.4](#14-die-ebay-berichtsseiten-downloads-und-uploads)).

**Wichtig:** „✅ … geänderte Zeilen zu eBay hochgeladen.“ heißt: Die Datei ist bei eBay angekommen und verarbeitet. Ob eBay **jede einzelne Zeile** angenommen hat, prüft der Tracker **nicht**. Das siehst du nur in der Ergebnisdatei von eBay ([Abschnitt 14.4](#14-die-ebay-berichtsseiten-downloads-und-uploads)).

### 12.4 „Upload zu eBay fehlgeschlagen: unbekannt“ – oft kein echter Fehler

Der Tracker wartet nur **90 Sekunden** auf die Bestätigung vom eBay-Tab. Der eBay-Tab meldet sich aber erst, wenn eBay die Datei komplett verarbeitet hat („Ergebnisse herunterladen“ ist da). Braucht eBay dafür länger, meldet der Tracker „Upload zu eBay fehlgeschlagen: unbekannt“ – der eBay-Tab arbeitet aber weiter, und der Upload läuft meist trotzdem durch. Erkennbar daran, dass der eBay-Tab später „✅ Hochladen fertig!“ zeigt. Er bleibt dann offen und wird von der Extension etwa 25 bis 28 Minuten nach dem Öffnen automatisch geschlossen (du kannst ihn auch selbst schließen). Das Dashboard zeigt in diesem Fall „nicht hochgeladen“, weil die Bestätigung fehlt.

So prüfst du es:
1. Den eBay-Tab ansehen: Steht „Warte auf Ergebnisse“ (mit 🔄, ⏳ oder ⌛ davor) oder „✅ Hochladen fertig!“ im Titel? Dann warten bzw. es hat geklappt. Steht dort „❌ Hochladen fehlgeschlagen“, im Tab nachsehen, was eBay anzeigt.
2. Oder selbst `ebay.<Land>/sh/reports/uploads` öffnen: Steht dort eine neue Zeile mit einer Datei „update_<Datum>.csv“? Dann ist die Datei angekommen.
3. Nur wenn dort nichts angekommen ist: siehe [Abschnitt 12.6](#12-hochladen-zu-ebay).

### 12.5 eBay lehnt Zeilen ab (z. B. Verkaufslimit erreicht)

**Nicht sicher belegt (eBay-Regeln, bitte bei eBay nachlesen):** Nach allgemeinem Wissen begrenzt eBay bei vielen Konten, wie viele Artikel bzw. welchen Gesamtwert du anbieten darfst (Verkaufslimits), und lehnt bei erreichtem Limit Änderungen ab, die mehr Menge oder Wert bedeuten würden. Die genauen Regeln und deine aktuellen Limits stehen bei eBay.

Belegt ist, was der Tracker dabei macht:
- Der Tracker erkennt ein Verkaufslimit **nicht** und zeigt dazu **keine** Meldung. Die Datei gilt als hochgeladen.
- Welche Zeilen eBay abgelehnt hat und warum, steht in der eBay-Ergebnisdatei („Ergebnisse herunterladen“ auf der Upload-Seite, [Abschnitt 14.4](#14-die-ebay-berichtsseiten-downloads-und-uploads)).
- **Nicht sicher belegt:** der genaue Wortlaut, mit dem eBay ein erreichtes Verkaufslimit in der Ergebnisdatei meldet.
- Möglicher Ausweg (deine Entscheidung): „Feste Menge“ niedriger einstellen, damit weniger Menge gegen das Limit zählt, oder bei eBay eine Limiterhöhung anfragen.

### 12.6 Wenn das Hochladen gescheitert ist

Den letzten Upload kann man auf der Tracker-Seite nicht von Hand wiederholen. Die Änderungen gehen aber nicht verloren:

- **Im Dauerbetrieb:** Der nächste Lauf holt einen frischen Bericht, rechnet alle Änderungen neu und lädt sie hoch. Du musst nichts tun. Ausnahme: Klappt vor diesem Lauf der Bericht nicht („Dauerbetrieb: Bericht nicht abrufbar – Lauf mit dem letzten Stand.“), hält der Tracker die gescheiterten Änderungen für schon geschickt und lässt sie weg ([Abschnitt 12.2](#12-hochladen-zu-ebay)). Sie kommen erst wieder mit, sobald ein frischer Bericht geladen ist.
- **Von Hand:** Zuerst auf `ebay.<Land>/sh/reports/uploads` nachsehen, ob die Datei nicht doch angekommen ist ([Abschnitt 12.4](#12-hochladen-zu-ebay)). Wenn nicht: „Angebote von eBay laden“ (wichtig, siehe 12.2), bei „Ab Artikel“ „0“ eintragen, „Lauf starten“. Am Ende dieses neuen Laufs wird wieder hochgeladen.

### Häufige Fragen

- **„Werden Angebote beendet, die gerade nicht geprüft werden konnten?“** – Nein. Nur endgültige Ergebnisse (Gruppe 3) führen zu Menge 0 oder Beenden.
- **„Kann ich hochladen, ohne einen Lauf zu machen?“** – Nein. Hochgeladen wird nur am Ende eines vollständigen Laufs.
- **„Kann ich das automatische Hochladen ausschalten?“** – Nein, nicht mehr. Halte den Lauf vor dem Ende mit „Pausieren“ an, wenn du (noch) nicht hochladen willst.
- **„Warum öffnet sich plötzlich ein eBay-Tab?“** – Das ist das Hochladen nach einem fertigen Lauf. Nicht schließen, solange im Tab-Titel noch gearbeitet wird („… Warte auf Ergebnisse“ usw.). Steht dort „✅ Hochladen fertig!“, ist er fertig: Er schließt sich dann selbst, oder du schließt ihn.

### Probleme und Lösungen

| Problem | Lösung |
|---|---|
| „Upload zu eBay fehlgeschlagen: unbekannt“ | Siehe [Abschnitt 12.4](#12-hochladen-zu-ebay) – meist lief es trotzdem durch. |
| „Upload zu eBay fehlgeschlagen: Zeitüberschreitung beim Warten auf: Knopf „Vorlage hochladen““ | Die Extension hat auf der eBay-Upload-Seite den Knopf „Vorlage hochladen“/„Upload template“ nicht gefunden. Bist du bei eBay angemeldet? Den offenen Tab ansehen. **Nicht sicher belegt:** ob das Hochladen auf eBay-Seiten in anderen Sprachen klappt – die Extension sucht den Knopf nur auf Deutsch, Englisch und Italienisch. Auf eBay Frankreich oder Spanien kann das automatische Hochladen deshalb scheitern → Betreiber fragen. |
| „Upload zu eBay fehlgeschlagen: Zeitüberschreitung beim Warten auf: verstecktes Dateifeld“ oder „… Knopf „Datei auswählen““ | Das Hochlade-Fenster von eBay hat sich nicht wie erwartet geöffnet (auch „Datei auswählen“/„Choose file“ sucht die Extension nur auf Deutsch, Englisch und Italienisch). Tab ansehen, Screenshot an den Betreiber. |
| „Upload zu eBay fehlgeschlagen: Error: Zeitüberschreitung (timeout): Seite im Tab nicht fertig geladen“ | Die eBay-Upload-Seite wurde nicht innerhalb von 60 Sekunden als fertig geladen erkannt. Den offenen eBay-Tab ansehen, Internet und eBay-Anmeldung prüfen. Beim nächsten Lauf wird erneut hochgeladen ([Abschnitt 12.6](#12-hochladen-zu-ebay)). |
| „Upload zu eBay fehlgeschlagen: …“ (anderer Text) | Die eBay-Seite sah anders aus als erwartet oder der Tab ließ sich nicht öffnen. Tab ansehen, Screenshot an den Betreiber. |
| eBay-Tab bleibt mit „❌ Hochladen fehlgeschlagen“ offen | Im Tab sehen, was eBay anzeigt. Dann [Abschnitt 12.6](#12-hochladen-zu-ebay). |
| eBay-Tab bleibt mit „✅ Hochladen fertig!“ offen | Upload hat geklappt, nur die Bestätigung kam zu spät beim Tracker an ([Abschnitt 12.4](#12-hochladen-zu-ebay)). Tab kann geschlossen werden. |
| „Keine Preis-/Bestandsänderungen – Upload übersprungen.“, obwohl du Änderungen erwartest | Entweder ändert sich wirklich nichts, oder der Bericht ist nicht aktuell. Vorschau ansehen. Wurden die Preise in den Einstellungen nie gespeichert? ([Abschnitt 10](#10-preise-und-mengen-so-rechnet-der-tracker), Probleme) |

---

## 13. Die Dateien des Trackers

### 13.1 Der Angebotsbericht „eBay_active_listings_<Datum>.csv“

So heißt der Bericht, den „Angebote von eBay laden“ holt. Der Name steht im Dateifeld. Die Datei wird **nicht** in deinem Download-Ordner gespeichert. Wählst du selbst eine Datei, steht dort deren Name.

### 13.2 Die Upload-Datei „update_<Datum>.csv“

Das ist die Datei im eBay-Upload-Format, die der Tracker am Ende eines Laufs hochlädt (nur die geänderten Zeilen). Sie wird nicht in deinem Download-Ordner gespeichert, du siehst sie aber auf der eBay-Upload-Seite.

| Spalte | Inhalt |
|---|---|
| „Action“ | „Revise“ (ändern) oder „EndItem“ (beenden) |
| „ItemID“ | eBay-Artikelnummer |
| „StartPrice“ | neuer eBay-Preis; leer bei Beenden, bei Menge 0 und wenn „Preis aktualisieren“ aus ist |
| „Quantity“ | neue Menge („Feste Menge“ oder 0); leer bei Beenden und wenn „Bestand aktualisieren“ aus ist |
| „EndingReason“ | „NotAvailable“ bei Beenden, sonst leer |

Nicht enthalten: Zeilen mit vorübergehenden Fehlern, „Skipped“-Zeilen und Zeilen mit einem Preis von 0 € oder weniger.

### 13.3 Beenden-Datei für Duplikate „doppelte_beenden_<Datum>.csv“

Entsteht nur, wenn in den Einstellungen, Reiter „eBay & Rahmenbedingungen“, Karte „Server & Produkt-Vergabe“ der Schalter „**Beenden-CSV für Duplikate erstellen**“ an ist (Standard aus). Gleiche Spalten wie 13.2, alle Zeilen „EndItem“ mit „NotAvailable“. Sie landet in deinem **Download-Ordner** und wird **nicht** automatisch hochgeladen – du lädst sie selbst bei eBay hoch ([Abschnitt 14.3](#14-die-ebay-berichtsseiten-downloads-und-uploads)). Mehr in [Abschnitt 18](#18-produkt-vergabe-beim-laden-der-angebote).

### 13.4 Die Ergebnisdatei von eBay

Nach jedem Upload bietet eBay auf der Upload-Seite „Ergebnisse herunterladen“ („Download results“) an. Darin steht pro Zeile, ob eBay sie angenommen hat. Diese Datei stammt von eBay; der Tracker wertet sie nicht aus. **Nicht sicher belegt:** wie die Spalten dieser eBay-Datei heißen.

### 13.5 Was es nicht mehr gibt

Die früheren Dateien „processed_items_<Datum>.csv“ (Ergebnistabelle speichern) und „eBay_update_<Datum>.csv“ (Knopf „Export CSV“) erzeugt der Tracker nicht mehr (schon seit Version 45.5).

---

## 14. Die eBay-Berichtsseiten (Downloads und Uploads)

Der Tracker arbeitet mit zwei Berichtsseiten aus dem eBay-Verkäufer-Bereich (Seller Hub). Du kannst beide auch selbst öffnen – am einfachsten, indem du die Adresse aus der Tabelle in die Adresszeile eingibst.

**Nicht sicher belegt:** wie die Menüpunkte zu diesen Seiten im Seller Hub genau heißen (eBay ändert seine Menüs gelegentlich). Die Adressen funktionieren direkt.

| Seite | Adresse | Was der Tracker dort macht | Was du dort selbst machen kannst |
|---|---|---|---|
| Downloads | `ebay.<Land>/sh/reports/downloads` | lässt bei „Angebote von eBay laden“ einen Bericht über alle aktiven Angebote erstellen und holt ihn ab (Hintergrund-Tab, schließt sich) | Berichte selbst erstellen/herunterladen; sehen, ob ein Bericht fertig ist |
| Uploads | `ebay.<Land>/sh/reports/uploads` | lädt am Ende eines Laufs die Änderungsdatei hoch (Tab im Vordergrund, schließt sich bei rechtzeitiger Bestätigung) | Dateien selbst hochladen („Vorlage hochladen“); Ergebnisse jedes Uploads ansehen („Ergebnisse herunterladen“) |

`<Land>` ist z. B. `de` für eBay.de.

### 14.1 Welches eBay-Land wofür

- Downloads: Land aus „Domain“ in den Einstellungen (Reiter „Preise & Listing“).
- Uploads: Land aus „eBay-Seite“ im Tracker (Karte „Filter“).

Beides sollte dasselbe Land sein.

### 14.2 Bericht selbst holen

1. `ebay.<Land>/sh/reports/downloads` öffnen.
2. Einen Bericht über alle aktiven Angebote erstellen lassen und warten, bis er fertig ist.
3. Herunterladen.
4. Im Tracker über das Dateifeld neben „oder“ wählen.

### 14.3 Datei selbst hochladen

Für „doppelte_beenden_<Datum>.csv“:
1. Bei eBay im selben Land anmelden.
2. `ebay.<Land>/sh/reports/uploads` öffnen.
3. „Vorlage hochladen“ (englisch „Upload template“) klicken und die Datei wählen.
4. Warten, bis die Datei in der Liste erscheint und eBay fertig ist.
5. Bei der Zeile „Ergebnisse herunterladen“ („Download results“) prüfen, ob alles angenommen wurde.

**Nicht sicher belegt:** wie die Schritte im eBay-Hochlade-Fenster im Einzelnen aussehen (das gestaltet eBay und kann sich ändern).

### 14.4 Ergebnis eines Uploads prüfen

1. `ebay.<Land>/sh/reports/uploads` öffnen.
2. Die neueste Zeile suchen (Dateiname „update_<Datum>.csv“ bei Uploads des Trackers).
3. „Ergebnisse herunterladen“ / „Download results“ klicken.
4. In der Datei nach Zeilen mit Fehlern suchen. Typische Gründe kommen von eBay selbst (z. B. Verkaufslimits, Angebot schon beendet).

---

## 15. Automatik: „Dauerhaft wiederholen“ (24/7)

**Wo:** Lauf-Karte, dritte Zeile.

| Bedienelement | Was es macht | Standard |
|---|---|---|
| Haken „Dauerhaft wiederholen“ (Hinweis: „Nach jedem Lauf und der Pause startet der nächste von selbst (24/7)“) | Nach jedem fertigen Lauf plant der Tracker automatisch den nächsten. Vor jedem neuen Lauf holt er einen frischen eBay-Bericht. | aus |
| „Pause … Minuten“ | **Pause in Minuten zwischen dem Ende eines Laufs und dem Start des nächsten** (nicht der Abstand von Start zu Start). Mindestens 1. Ein leeres Feld oder „0“ zählt als 60 Minuten. Nicht verwechseln mit dem Knopf „Pausieren“. | 60 |

### 15.1 Was beim Einschalten passiert

- Es startet **noch kein** Lauf. Den ersten Lauf startest du selbst mit „Lauf starten“.
- Hochgeladen wird ohnehin nach jedem vollständigen Lauf. Einen eigenen Upload-Haken gibt es nicht mehr.

### 15.2 Ablauf im Dauerbetrieb

1. Du startest den ersten Lauf (Angebote laden, „Lauf starten“).
2. Lauf fertig → Änderungen werden hochgeladen.
3. Meldung „Dauerbetrieb aktiv – nächster Lauf um HH:MM Uhr.“
4. Nach der Pause: „Dauerbetrieb: hole aktuellen Angebotsbericht …“ – der Tracker macht dasselbe wie „Angebote von eBay laden“.
5. „Dauerbetrieb: neuer Lauf startet (<Anzahl> Zeilen).“ – die Ergebnistabelle wird geleert, der Lauf beginnt bei Artikel 0.
6. Klappt der Bericht nicht: Erst kommt „Fehler beim CSV-Download: …“ mit dem Grund, dann „Dauerbetrieb: Bericht nicht abrufbar – Lauf mit dem letzten Stand.“ – der Tracker prüft dann mit dem zuletzt geladenen Bericht weiter, statt stehen zu bleiben. (Ohne jeden früheren Bericht in dieser Sitzung versucht er es nach der nächsten Pause erneut.)
7. Weiter bei Schritt 2.

Durch den frischen Bericht vor jedem Lauf bemerkt der Tracker neue Verkäufe und füllt die Menge wieder auf „Feste Menge“ auf.

### 15.3 Was die Automatik unterbricht

| Ereignis | Folge |
|---|---|
| „Pausieren“ geklickt | Der geplante Lauf wird abgesagt. Weiter mit „Lauf starten“. |
| Haken „Dauerhaft wiederholen“ aus | Der geplante Lauf wird abgesagt. |
| Notbremse ([Abschnitt 16.2](#16-schutz-bei-sperren-und-fehlern-kurz-warten-und-notbremse)) | Kein Upload, **kein** nächster Lauf. Erst nach deinem „Lauf starten“ geht es weiter. |
| Sperr-Pause „⏳ Kurz warten!“ | Nur kurze Unterbrechung, danach geht es von selbst weiter. Schließt du das Fenster mit „×“, bleibt der Lauf pausiert – und es wird auch kein nächster Lauf geplant, bis du mit „Lauf starten“ fortsetzt und der Lauf zu Ende kommt. |
| Tracker-Tab geschlossen, Chrome beendet, PC aus oder im Ruhezustand | Alles steht. Nach dem Neuöffnen ist der Haken zwar noch gesetzt, aber es läuft nichts, bis du Angebote lädst und „Lauf starten“ klickst. |
| Upload fehlgeschlagen | Der nächste Lauf wird trotzdem geplant. |

Änderst du „Pause … Minuten“ während der Automatik, gilt der neue Wert ab der nächsten Planung, also nach dem nächsten fertigen Lauf.

### Häufige Fragen

- **„Läuft der Dauerbetrieb auch, wenn Chrome zu ist?“** – Nein. Die Tracker-Seite muss offen sein, Chrome muss laufen, der PC muss an sein.
- **„Welche Pause ist sinnvoll?“** – **Nicht sicher belegt:** eine Empfehlung. Kürzer = aktuellere Preise, aber mehr Anfragen an Amazon und eBay. Frag bei Bedarf den Betreiber.
- **„Startet der Dauerbetrieb nach einem Neustart von selbst?“** – Nein. Nach dem Neuöffnen einmal „Angebote von eBay laden“ klicken, bei „Ab Artikel“ „0“ eintragen und „Lauf starten“ klicken ([Abschnitt 21.3](#21-typische-abläufe-schritt-für-schritt), Schritt 6).
- **„Warum ist die Ergebnistabelle plötzlich leer?“** – Jeder neue automatische Lauf beginnt mit leerer Tabelle.
- **„Kann ich den Tracker auf einem eigenen Rechner (z. B. einem gemieteten Server) rund um die Uhr laufen lassen und von meinem PC aus sehen?“** – Ja, dafür gibt es in den Einstellungen den „Server-Modus“ (Reiter „eBay & Rahmenbedingungen“, Karte „Server-Modus“, Schalter „Dieses Gerät ist ein Server“ – auf dem Rechner einschalten, auf dem der Tracker läuft). Das Dashboard deiner anderen Geräte zeigt dann den Stand dieses Rechners. Steuern musst du den Tracker dort selbst. Siehe `dashboard.md` und `einstellungen.md`.

### Probleme und Lösungen

| Problem | Lösung |
|---|---|
| Nach der angekündigten Uhrzeit passiert nichts | Ist der Tracker-Tab noch offen? Wurde zwischendurch „Pausieren“ geklickt? Hat die Notbremse ausgelöst (Tab-Titel „⛔ Tracker angehalten …“)? War der PC im Ruhezustand? |
| Jeder automatische Lauf meldet „Bericht nicht abrufbar“ | eBay-Anmeldung prüfen (vermutlich abgelaufen). Einmal von Hand „Angebote von eBay laden“ klicken und die Fehlermeldung lesen ([Abschnitt 5](#5-angebote-laden-von-ebay-oder-als-eigene-datei)). |
| Meldung „Dauerbetrieb aktiv …“ erscheint nicht | Sie erscheint erst nach dem Ende eines Laufs, und nur wenn der Lauf nicht pausiert oder von der Notbremse gestoppt wurde und „Dauerhaft wiederholen“ an ist. |
| „Dauerbetrieb: neuer Lauf startet (0 Zeilen).“, danach „Keine Zeilen zum Verarbeiten – lade zuerst einen Angebotsbericht.“ – und dann passiert nichts mehr | Im frischen Bericht hat kein Angebot die Filter überstanden. In diesem Fall plant der Tracker **keinen** weiteren Lauf, der Dauerbetrieb steht. Filter prüfen ([Abschnitt 5](#5-angebote-laden-von-ebay-oder-als-eigene-datei), Probleme), dann von Hand „Angebote von eBay laden“ und „Lauf starten“. |

---

## 16. Schutz bei Sperren und Fehlern: „Kurz warten!“ und Notbremse

### 16.1 Sperr-Pause „⏳ Kurz warten!“

**Wann:** Wenn mehr als 10 Artikel einen Fehler mit „**ERROR_503**“ bekommen (Sperrseite, „Zeitüberschreitung beim Abruf der Produktdaten“, Tab-Ladefehler), **ohne dass dazwischen ein Artikel erfolgreich war**. Nur ein „Success“ setzt die Zählung zurück (ebenso jeder Klick auf „Lauf starten“); andere Ergebnisse dazwischen, z. B. „nicht verfügbar“, setzen sie nicht zurück. Zeitüberschreitungen ohne „ERROR_503“ (z. B. „… keine Antwort von der Seite im Tab.“) zählen hier nicht mit – gegen viele solcher Fehler schützt nur der zweite Fall der Notbremse (mehr als 70 % ohne „Success“, 16.2); bei „200 Artikel hintereinander nicht kaufbar“ zählen sie nicht mit.

**Was du siehst:** ein dunkles Fenster über der ganzen Seite mit
- „⏳ Kurz warten!“
- „Amazon hat deine IP wegen zu vieler Anfragen vorübergehend gesperrt.“
- „Der Tracker wartet kurz und versucht es dann von selbst weiter.“
- „noch <Zahl> Sekunden …“ – Countdown, 120 Sekunden.

**Was passiert:**
1. Der Lauf wird angehalten.
2. Nach dem Countdown geht es **von selbst** weiter – an derselben Stelle. Die Artikel mit „ERROR_503“ werden dabei zuerst noch einmal geprüft.
3. „Laufzeit“ und „Verarbeitet“ beginnen wieder bei 0, die Ergebnisse bleiben.

**„×“ (oben rechts, Hinweis „Schließen“):** schließt das Fenster und stoppt den Countdown. Der Lauf bleibt **pausiert**, bis du „Lauf starten“ klickst.

Während des Countdowns verdeckt das Fenster die ganze Tracker-Seite; darunter kannst du nichts bedienen (nur „×“). Die kleinen Meldungen unten rechts bleiben sichtbar. Das Dashboard zeigt in dieser Zeit „wartet (Amazon-Sperre)“.

Wichtig: Ein Tab-Ladefehler (z. B. Internet kurz weg) zählt hier genauso mit. Fällt dein Internet für längere Zeit aus, erscheint also ebenfalls „⏳ Kurz warten!“, obwohl Amazon gar nicht sperrt. Gesperrte oder nicht geladene Artikel werden **nie** beendet oder auf 0 gesetzt.

### 16.2 Notbremse

**Wann:** in zwei Fällen. (1) 200 Artikel **hintereinander** gelten als nicht kaufbar (z. B. „nicht verfügbar“). Ein „Success“ setzt diese Zählung zurück; „Skipped“ und vorübergehende Fehler (z. B. „ERROR_503“, Zeitüberschreitungen) zählen nicht mit und setzen sie auch nicht zurück. (2) Mindestens 200 Artikel sind bewertet und davon haben **mehr als 70 %** kein „Success“; hier zählt „Skipped“ nicht mit, alle anderen Nicht-Erfolge schon (auch endgültige wie „nicht verfügbar“). Für beide Fälle gilt: Gezählt wird ab jedem „Lauf starten“ (auch der automatische Neustart nach „⏳ Kurz warten!“ beginnt die Zählung neu), und erneut geprüfte „ERROR_503“-Zeilen zählen nicht mit.

**Was passiert:**
- Der Lauf wird angehalten.
- Es wird **nichts hochgeladen** und **kein** nächster Lauf geplant.
- Meldung (rot), je nach Fall: „⛔ Notbremse: 200 Artikel hintereinander als nicht kaufbar gewertet. Lauf angehalten, nichts hochgeladen.“ (Fall 1) bzw. „⛔ Notbremse: <X> von <Y> Artikeln ohne verwertbares Ergebnis (<Z> %). Lauf angehalten, nichts hochgeladen.“ (Fall 2)
- Tab-Titel: „⛔ Tracker angehalten – 200 Artikel in Folge nicht kaufbar“ (Fall 1) bzw. „⛔ Tracker angehalten – <Z> % ohne Ergebnis“ (Fall 2); bleibt bis zum Neuladen der Seite.
- Im Dashboard: „angehalten“, in der Glocke „Tracker angehalten“.

**Wozu:** Wenn Amazon still sperrt oder die Seiten anders aussehen, würden sonst massenhaft gesunde Angebote auf 0 gesetzt oder beendet.

**Was du tun solltest:**
1. In der Tabelle nachsehen, welche Status vorherrschen (Klick auf „Status ⬍“ sortiert).
2. Viele „ERROR_503“/„Zeitüberschreitung“ → Amazon bremst: warten, weniger bei „Gleichzeitig“, später neu.
3. Viele „nicht verfügbar“ → „eBay-Seite“ und „Max. verlängerte Lieferzeit“ prüfen, einige Links selbst öffnen.
4. Erst wenn klar ist, dass die Ergebnisse stimmen, mit „Lauf starten“ fortsetzen (macht an der Stelle weiter und zählt neu).
5. Ist dein Bestand wirklich zu mehr als 70 % nicht lieferbar, löst die Notbremse bei jedem Lauf aus – und nach jedem „Lauf starten“ wieder, sobald erneut 200 Artikel bewertet sind. Hochgeladen wird erst, wenn ein Lauf ohne Notbremse bis zum Ende kommt. **Nicht sicher belegt:** ein bequemerer Weg für diesen Fall – Betreiber fragen.

Bei weniger als 200 bewerteten Artikeln (kleiner Bestand) greift die Notbremse nie.

### Häufige Fragen

- **„Ist meine IP jetzt dauerhaft gesperrt?“** – Die Meldung kommt von der Extension, nicht von Amazon. Sie bedeutet, dass Amazon gerade keine verwertbaren Seiten liefert. **Nicht sicher belegt:** wie lange Amazon jeweils bremst. Versuch es mit Warten und weniger bei „Gleichzeitig“.
- **„Was kann ich gegen die Sperren tun?“** – Weniger bei „Gleichzeitig“ einstellen und längere Pausen zwischen den Läufen („Pause … Minuten“). Tipps zum Umgehen von Amazon-Sperren gibt es nicht.

---

## 17. Die Karte „Google Sheets“ (Duplikat-Abgleich)

**Wo:** Karte „Google Sheets“ neben der Karte „Filter“ (Untertitel „Duplikat-Abgleich mit deinen Shop-Sheets“). Alle Felder werden beim Tippen gespeichert.

Wofür das Ganze? Damit du keine Produkte doppelt listest – weder in diesem Shop noch in deinen anderen Shops. Dazu führt der Tracker eine Liste deiner gelisteten Produkte in einem Google Sheet, und die Produkt-Datenbank nimmt Produkte, die in deinen Sheets stehen, gar nicht erst auf.

### 17.1 Die Felder

| Feld | Was es macht |
|---|---|
| „Haupt-Sheet dieses Shops – Web-App-URL“ (Beispiel im Feld: `https://script.google.com/macros/s/.../exec`) | Adresse eines Google-Apps-Script, das in dein Haupt-Sheet schreibt. Nach jedem Laden der Angebote schickt der Tracker dorthin die Liste deiner Angebote: je Zeile eBay-Artikelnummer und Amazon-Link, zusammen mit der Anweisung, das Sheet **vorher zu leeren** und dann neu zu befüllen. Was genau im Sheet passiert, bestimmt dein Script. |
| „Haupt-Sheet – Lese-Link“ (Beispiel: `https://docs.google.com/spreadsheets/d/.../edit`) | Der normale Link zu deinem Haupt-Sheet. Darüber liest die Extension beim Hinzufügen von Produkten zur Produkt-Datenbank, welche Produkte du schon gelistet hast. Darunter steht: „Freigabe: „Jeder mit dem Link – Betrachter“.“ |
| „Weitere Shop-Sheets (eine pro Zeile)“ | Links zu den Sheets deiner anderen Shops, je Zeile einer. Produkte aus diesen Sheets kommen ebenfalls nicht in die Produkt-Datenbank. Freigabe ebenfalls „Jeder mit dem Link – Betrachter“. |

Gelesen wird aus jedem Sheet das Tabellenblatt, das im Link angegeben ist (die Angabe „gid=…“ in der Adresse); steht keines im Link, das Blatt mit der Nummer 0 – meist das erste. Ohne Lese-Link versucht die Extension, über die Web-App-Adresse zu lesen. **Nicht sicher belegt:** ob das mit deinem Script klappt – trag am besten den Lese-Link ein. Lässt sich ein Sheet nicht lesen (nicht freigegeben, keine Antwort), wird es beim Abgleich übergangen – die Produkte daraus gelten dann nicht als doppelt.

Ob deine Sheets gelesen werden können, prüfst du in der **Produkt-Datenbank** mit dem Knopf „Sheet-Abgleich prüfen“ (siehe `produkte-finden-und-datenbank.md`).

Die Sheet-Adressen werden mit deinen Einstellungen gesichert (Datei-Export und Server-Sicherung, siehe `einstellungen.md`).

### 17.2 Was beim Laden der Angebote passiert

Nach jedem Laden (Knopf, Datei, automatischer Lauf im Dauerbetrieb und auch nach dem Ändern von „Lieferant“, „eBay-Seite“ oder „Preis endet auf …“):
1. Der Tracker nimmt die geladenen Angebote (nach den Filtern).
2. Er schickt für jedes Angebot mit lesbarer SKU eine Zeile „Artikelnummer + Amazon-Link“ an die Web-App.
3. Die Links zeigen immer auf amazon.de – auch bei anderen Marktplätzen.
4. Gibt es keine einzige gültige Zeile, schickt er **nichts** (damit das Sheet nicht leer gemacht wird).

### 17.3 Einrichtung

**Nicht sicher belegt:** wie das Google Sheet und das Apps-Script dafür eingerichtet werden. Das Script selbst ist nicht Teil der Extension – frag den Betreiber danach. Belegt sind nur die Hinweise, die der Tracker bei Fehlern gibt:
- In Apps Script unter „Bereitstellen → Bereitstellungen verwalten“ beim Stiftsymbol „Ausführen als: Ich“ und „Zugriff: Jeder“ (nicht „Jeder mit Google-Konto“) setzen und speichern; die /exec-Adresse bleibt dabei gleich.
- Bei veralteter Bereitstellung: in Apps Script „Neue Bereitstellung“ (Zugriff: Jeder) und die frische /exec-Adresse eintragen.
- Die Lese-Links brauchen die Freigabe „Jeder mit dem Link – Betrachter“.

### 17.4 Meldungen

| Meldung | Bedeutung / Lösung |
|---|---|
| „Sheet-Sync übersprungen: kein Haupt-Sheet (Web-App-URL) hinterlegt.“ (rot) | Es ist keine Web-App-Adresse eingetragen. Harmlos, wenn du keine Google Sheets nutzt – die Meldung kommt dann bei jedem Laden. |
| „Sheet-Sync: die Haupt-Sheet-URL sieht ungültig aus (muss mit http/https beginnen).“ | Adresse prüfen, vollständig mit `https://` einfügen. |
| „Sheet-Sync: 0 gültige Zeilen aus <N> Listings (<M> mit nicht-dekodierbarer SKU). Nichts gesendet, damit das Sheet nicht geleert wird.“ | Keines der geladenen Angebote hat eine Cash-Lister-SKU. Filter und Datei prüfen. |
| „✅ Sheet aktualisiert: <N> Zeilen gesendet. Script meldet: …“ | Hat geklappt. |
| „Sheet NICHT aktualisiert: HTTP <Nummer>. Antwort: …“ | Google hat einen Fehler zurückgegeben. Adresse und Bereitstellung prüfen. |
| „Sheet NICHT aktualisiert: Google verlangt eine Anmeldung bzw. Autorisierung. …“ | Die Web-App ist nicht für alle freigegeben. Schritte siehe 17.3 (der Text in der Meldung beschreibt sie). |
| „Sheet NICHT aktualisiert – das Script meldet: …“ | Dein Script hat einen Misserfolg gemeldet. Text lesen; bei Unklarheit Betreiber fragen. |
| „Sheet NICHT aktualisiert: Google hat eine Webseite zurückgegeben statt einer Script-Antwort. …“ | Meist veraltete oder nicht freigegebene Bereitstellung. Neu bereitstellen (17.3) und die neue /exec-Adresse eintragen. |
| „Sheet-Update abgeschickt: das Script lief, antwortet aber mit einer HTML-Seite …“ | Ob die Zeilen ankamen, ist unklar. Im Sheet nachsehen. |
| „Sheet-Update abgeschickt, aber das Script hat nichts zurückgemeldet – …“ | Ob die Zeilen ankamen, ist unklar. Im Sheet nachsehen. |
| „Sheet NICHT aktualisiert – das Script meldet einen Fehler: …“ | Dein Script hat einen Fehler. Betreiber fragen. |
| „Sheet-Update fehlgeschlagen: …“ | Keine Verbindung, oder nach 60 Sekunden keine Antwort. Später erneut (z. B. „Angebote von eBay laden“). |

### Häufige Fragen

- **„Brauche ich Google Sheets für den Tracker?“** – Nein. Preise und Bestand gleicht der Tracker auch ohne ab. Die Sheets dienen nur dem Schutz vor doppelten Produkten.
- **„Was trage ich bei mehreren Shops ein?“** – In jedem Shop sein eigenes Haupt-Sheet (Web-App-URL und Lese-Link) und bei „Weitere Shop-Sheets“ die Lese-Links der anderen Shops.

---

## 18. Produkt-Vergabe beim Laden der Angebote

**Was das ist:** Cash Lister hat einen Vergabe-Dienst, der verhindert, dass zwei Kunden dasselbe Amazon-Produkt listen. Produkte werden schon beim Hinzufügen zur Produkt-Datenbank für dich reserviert (siehe `produkte-finden-und-datenbank.md`).

**Was der Tracker dazu beiträgt:** Nach jedem Laden der Angebote meldet er dem Vergabe-Dienst, welche Produkte du **tatsächlich bei eBay anbietest** – und zwar aus **allen** Angeboten des Berichts, unabhängig von den Filtern. Dadurch
- werden deine Reservierungen **bestätigt**,
- werden Produkte, die du nicht mehr anbietest, für andere **freigegeben**.

Voraussetzung: Du bist angemeldet. Ohne Anmeldung findet kein Abgleich statt – ohne Meldung.

**Regelmäßig „Angebote von eBay laden“ (oder den Dauerbetrieb) nutzen hält deine Reservierungen aktuell.** **Nicht sicher belegt:** wie lange eine unbestätigte Reservierung hält – das legt der Betreiber fest. Frag ihn bei Bedarf.

### Meldungen

| Meldung | Bedeutung / was tun |
|---|---|
| „✅ Produkt-Vergabe abgeglichen: <N> Artikel · <X> bestätigt · <Y> neu · <Z> freigegeben“ | Hat geklappt. „bestätigt“ = deine Reservierungen gelten jetzt als gelistet, „neu“ = Produkte, die noch nicht für dich eingetragen waren, „freigegeben“ = Produkte, die du nicht mehr anbietest. |
| … „(Sicherung aktiv – nichts freigegeben)“ | Der Vergabe-Dienst hat vorsichtshalber nichts freigegeben. **Nicht sicher belegt:** wann genau das passiert. Kein Handlungsbedarf. |
| „Hinweis zur Produkt-Vergabe: <N> von <M> Angeboten haben keine lesbare ASIN in der SKU und waren im Abgleich NICHT dabei. Deren Reservierungen bleiben unbestätigt und laufen ab.“ | Manche Angebote haben eine fremde, geänderte oder gar keine SKU (z. B. von Hand eingestellte Angebote). Die gehören für den Vergabe-Dienst nicht zu dir. Bei eigenen Handangeboten ist der Hinweis normal. Wenn das Angebote von Cash Lister sind: SKU bei eBay nicht ändern. |
| „Produkt-Vergabe: KEIN Abgleich – <Angaben>. Es wurde nichts bestätigt!“ | Im Bericht war keine einzige lesbare Cash-Lister-SKU. Die Angaben nennen, wie viele Angebote geladen wurden und warum keines passte („ohne SKU“, „SKU nicht lesbar“, „keine ASIN“). Richtige Datei? Angebote mit Cash Lister gelistet? |
| „Produkt-Vergabe: API-Key ungültig.“ | Deine Anmeldung wurde nicht angenommen. Im Dashboard nachsehen (Anmeldung, Karte „Dein Abo“), ab- und wieder anmelden. Hilft das nicht: Betreiber fragen. |
| „Produkt-Vergabe: Abgleich fehlgeschlagen (HTTP <Nummer>).“ | Der Vergabe-Dienst hatte ein Problem oder hat die Anfrage abgelehnt. Im Dashboard prüfen, ob du angemeldet bist und dein Abo aktiv ist. Später erneut („Angebote von eBay laden“). Bleibt es: Betreiber informieren. |
| „Produkt-Vergabe: Server nicht erreichbar.“ | Keine Verbindung zum Vergabe-Dienst (oder 60 Sekunden ohne Antwort). Internet prüfen, später erneut. Bleibt es: Betreiber informieren. Prüfen und Hochladen funktionieren trotzdem. |
| „⚠️ <N> Produkt(e) bereits von einem anderen Nutzer belegt. Beenden-Datei mit <M> Angebot(en) heruntergeladen – bei eBay hochladen.“ | Ein anderer Kunde hatte diese Produkte vor dir. Die Datei „doppelte_beenden_<Datum>.csv“ liegt in deinem Download-Ordner. Bei eBay hochladen ([Abschnitt 14.3](#14-die-ebay-berichtsseiten-downloads-und-uploads)), damit deine doppelten Angebote enden. Kommt nur, wenn „Beenden-CSV für Duplikate erstellen“ an ist. |
| „⚠️ <N> doppelte Produkt(e) gefunden, aber keine ItemID dazu gefunden.“ | Doppelte Produkte gemeldet, aber zu keinem davon steht im geladenen Bericht eine eBay-Artikelnummer – z. B., weil in einer selbst gewählten Datei die Spalte „Item number“ fehlt oder leer ist. Deshalb konnte keine Beenden-Datei erstellt werden. Lade die Angebote mit „Angebote von eBay laden“ neu. Kommt die Meldung dann immer noch: Betreiber fragen. |

Ist „Beenden-CSV für Duplikate erstellen“ aus (Standard), gibt es bei Dopplungen **weder Datei noch Meldung**. Der Vergabe-Dienst meldet Dopplungen bei jedem Abgleich erneut – mit eingeschaltetem Schalter bekommst du deshalb bei jedem Laden dieselbe Datei.

Der Schalter steht in den Einstellungen, Reiter „eBay & Rahmenbedingungen“, Karte „Server & Produkt-Vergabe“ („wenn ein anderer Nutzer das Produkt zuerst hatte“). Mehr in `einstellungen.md`.

---

## 19. Der Tracker im Dashboard

Das Dashboard zeigt den Stand des Trackers an, steuert ihn aber nicht. Starten, pausieren und fortsetzen kannst du nur im Tracker selbst. Ausführlich: `dashboard.md`.

**Wo der Tracker im Dashboard auftaucht:**
- Kachel „**Tracker, letzter Lauf**“ mit Fortschrittsbalken:
  - während des Laufs z. B. „37 %“ / „370 von 1.000 geprüft“ (in der Sperr-Pause mit „· wartet“ dahinter),
  - nach dem Lauf mit Upload z. B. „25“ / „geändert hochgeladen · heute 06:12“ (die Zahl = so viele Zeilen gingen an eBay),
  - nach dem Lauf ohne bestätigten Upload z. B. „1.000“ / „geprüft, nicht hochgeladen · heute 06:12“,
  - angehalten z. B. „37 %“ / „pausiert bei 370 von 1.000“ (ebenso „angehalten …“ bzw. „unterbrochen …“),
  - vor dem ersten Lauf „–“ / „noch kein Lauf seit dem Update“.
- Karte „**Tracker**“ unter „Vorgänge“ mit einem Marker und einer Stand-Zeile (z. B. „Fertig heute 06:12 · 25 geändert hochgeladen“). Ein Klick öffnet den Tracker bzw. springt in den offenen Tab. Die Zeile darunter sagt, was der Klick tut: „Tracker ist offen – Klick springt hin“ oder „Klick öffnet: Tracker“. (Hast du Server-Geräte, steht dort stattdessen, von welchem Gerät der Stand kommt, z. B. „Dieser PC · …“ oder „<Gerätename> · letzte Meldung …“.)
- Checkliste „Heute“, Punkt „**Preise & Bestand abgeglichen**“.
- Glocke mit Hinweisen: „Tracker angehalten“, „Lauf des Trackers unterbrochen“, „Tracker wartet“.
- Kachel „Aktive Angebote“: „laut Tracker · Bericht …“ – zählt **alle** Zeilen des zuletzt eingelesenen Berichts, egal welcher Filter im Tracker eingestellt ist.

**Was die Anzeigen bedeuten und was du im Tracker tust:**

| Dashboard zeigt (Karte „Tracker“) | Bedeutung | Was du im Tracker tust |
|---|---|---|
| „läuft · 37 %“ | Ein Lauf prüft gerade. | nichts; Tab offen lassen |
| „wartet (Amazon-Sperre)“ | Das Fenster „⏳ Kurz warten!“ zählt herunter ([Abschnitt 16.1](#16-schutz-bei-sperren-und-fehlern-kurz-warten-und-notbremse)). | nichts; es geht von selbst weiter |
| „pausiert“ | Du hast „Pausieren“ geklickt (oder „×“ im Fenster „⏳ Kurz warten!“). | „Lauf starten“ (macht an derselben Stelle weiter). War der Tab zwischendurch zu: erst den Bericht laden ([Abschnitt 7.8](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)). |
| „angehalten“ | Die Notbremse hat ausgelöst ([Abschnitt 16.2](#16-schutz-bei-sperren-und-fehlern-kurz-warten-und-notbremse)). | Status prüfen, Ursache beheben, dann „Lauf starten“ |
| „unterbrochen“ | Der Lauf lief noch, aber der Tracker-Tab ist zu (Tab geschlossen, Chrome beendet, Neustart). | [Abschnitt 7.8](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen) |
| „fertig“ | Der letzte Lauf ist fertig. Die Stand-Zeile sagt, ob hochgeladen wurde („… geändert hochgeladen“ bzw. „nicht hochgeladen“). | nichts; nächsten Lauf bei Bedarf von Hand starten |
| „nächster Lauf 18:30“ | Lauf fertig, „Dauerhaft wiederholen“ ist an, der Tracker-Tab ist offen. | nichts; Tab offen lassen |
| „bereit“ | Seit dem Update noch kein Lauf. | ersten Lauf starten |
| „meldet sich nicht“ | Nur bei einem Server-Gerät (Server-Modus): Es lief dort ein Lauf, aber das Gerät hat sich länger nicht gemeldet. | auf dem Server-Gerät nachsehen (läuft Chrome, ist der Tracker-Tab offen, gibt es Internet?) |

„nicht hochgeladen“ nach einem fertigen Lauf heißt: Das Hochladen ist gescheitert oder die Bestätigung kam nicht rechtzeitig ([Abschnitt 12.4](#12-hochladen-zu-ebay)). Kommt der Stand von einem Server-Gerät („auf <Gerätename>“), musst du den Tracker **dort** bedienen, nicht auf diesem PC.

Meldest du dich im Dashboard ab, während der Tracker auf diesem PC läuft (oder in der Sperr-Pause wartet), fragt das Dashboard vorher nach: „Gerade läuft auf diesem PC: Tracker.“ und „Nach dem Abmelden sperren sich die Module. Trotzdem abmelden?“ (siehe `dashboard.md`). Nach dem Abmelden lässt sich der Tracker nicht mehr öffnen.

---

## 20. Alle Meldungen des Trackers

Meldungen erscheinen unten rechts als kleine Kästchen mit Uhrzeit davor (z. B. „14:05  …“). Dunkelblau = Information (verschwindet nach etwa 12 Sekunden), rot = Problem (etwa 30 Sekunden). Höchstens 6 stehen gleichzeitig da; kommt eine siebte, verschwindet die älteste. Eine verpasste Meldung lässt sich auf der Seite nicht mehr aufrufen. Diese Meldungen halten nichts an – auch der Dauerbetrieb läuft weiter.

Ein einziges Fenster mit „OK“ gibt es noch: „Für den Tracker brauchst du die Ultimate-Mitgliedschaft.“ beim Öffnen ([Abschnitt 3](#3-tracker-öffnen-und-voraussetzungen)).

| Meldung | Wo/wann | Bedeutung | Abschnitt |
|---|---|---|---|
| Fenster „Für den Tracker brauchst du die Ultimate-Mitgliedschaft.“ | beim Öffnen | nicht angemeldet / Zugang abgeschaltet / Abo gesperrt | 3 |
| „Bericht wird eingelesen … (<N>)“ (über der ganzen Seite) | beim Laden einer Datei oder eines Berichts | Datei wird eingelesen | 5 |
| „Fehler beim CSV-Download: …“ | „Angebote von eBay laden“ | Bericht nicht bekommen | 5 |
| „Keine Zeilen zum Verarbeiten – lade zuerst einen Angebotsbericht.“ | „Lauf starten“ | keine Angebote geladen | 5.4, 7 |
| Fenster „⏳ Kurz warten!“ | während des Laufs | Amazon-Sperre, automatische Pause | 16.1 |
| „⛔ Notbremse: … Lauf angehalten, nichts hochgeladen.“ | während des Laufs | zu viele unbrauchbare Ergebnisse | 16.2 |
| „Keine Preis-/Bestandsänderungen – Upload übersprungen.“ | Ende des Laufs | nichts geändert | 12 |
| „✅ <N> geänderte Zeilen zu eBay hochgeladen.“ | Ende des Laufs | Datei bei eBay verarbeitet | 12 |
| „Upload zu eBay fehlgeschlagen: …“ | Ende des Laufs | siehe 12.4 und Tabelle in 12 | 12 |
| „Dauerbetrieb aktiv – nächster Lauf um HH:MM Uhr.“ | Ende des Laufs | nächster Lauf geplant | 15 |
| „Dauerbetrieb: hole aktuellen Angebotsbericht …“ | Dauerbetrieb | holt Bericht | 15 |
| „Dauerbetrieb: neuer Lauf startet (<N> Zeilen).“ | Dauerbetrieb | Lauf beginnt | 15 |
| „Dauerbetrieb: Bericht nicht abrufbar – Lauf mit dem letzten Stand.“ | Dauerbetrieb | Bericht fehlgeschlagen, alter Stand wird benutzt | 15 |
| Meldungen mit „Sheet“ | nach dem Laden | Google-Sheet-Abgleich | 17.4 |
| Meldungen mit „Produkt-Vergabe“ / „belegt“ / „doppelte“ | nach dem Laden | Vergabe-Abgleich | 18 |
| Tab-Titel „⛔ Tracker angehalten – <Z> % ohne Ergebnis“ bzw. „⛔ Tracker angehalten – 200 Artikel in Folge nicht kaufbar“ | nach der Notbremse | bleibt bis zum Neuladen | 16.2 |

Die Status-Texte in der Tabelle stehen in [Abschnitt 9.2](#9-die-tabelle-verarbeitete-artikel-und-die-status-texte), die Tab-Titel des eBay-Upload-Tabs in [Abschnitt 12.3](#12-hochladen-zu-ebay).

---

## 21. Typische Abläufe Schritt für Schritt

### 21.1 Der allererste Lauf (vorsichtig)

Weil am Ende jedes vollständigen Laufs automatisch hochgeladen wird, prüfst du beim ersten Mal zwischendurch:

1. Dashboard: angemeldet? Einstellungen → Reiter „Preise & Listing“: „Domain“ = dein eBay-Land, Preise in der Karte „Preise“ eingestellt (einen Wert einmal neu eintippen, damit die Preistafel sicher gespeichert ist).
2. Seitenleiste → „Tracker“.
3. Karte „Filter“: „Lieferant“ = „Amazon“, „eBay-Seite“ = dein Land, „Preis endet auf …“ leer.
4. „Dauerhaft wiederholen“ **aus**.
5. „Upload-Einstellungen“ klicken: „Ausverkaufte / fehlgeschlagene Artikel“ wählen (für den Anfang ist „Menge auf 0 setzen“ vorsichtiger), „Feste Menge“ eintragen, „Bestand aktualisieren“ und „Preis aktualisieren“ an, „Einstellungen speichern“.
6. „Angebote von eBay laden“ klicken, Meldungen abwarten, bis bei „Bericht:“ eine Zahl steht.
7. „Gleichzeitig“ z. B. 5, „Ab Artikel“ 0.
8. „Lauf starten“.
9. Nach einigen Dutzend Artikeln „**Pausieren**“ klicken.
10. Tabelle nach „Status ⬍“ sortieren und anschauen. „Upload-Einstellungen“ öffnen → Vorschau: Stimmen die Preise (eBay-Preis, nicht Amazon-Preis)?
11. Stimmt alles: „Lauf starten“ (macht weiter). Am Ende wird automatisch hochgeladen.
12. Stimmt etwas nicht: Lauf **pausiert lassen**, Einstellungen korrigieren, dann neu beginnen („Ab Artikel“ 0, „Lauf starten“ – die Tabelle wird dabei geleert).
13. Später auf `ebay.<Land>/sh/reports/uploads` bei der neuesten Zeile „Ergebnisse herunterladen“ prüfen.

### 21.2 Täglicher Lauf von Hand

1. Tracker öffnen (oder den schon offenen Tracker-Tab nehmen).
2. „Angebote von eBay laden“ klicken und warten, bis bei „Bericht:“ die Zahl steht. (Damit wird „Lauf starten“ auch nach einem früheren Lauf wieder klickbar, [Abschnitt 7.7](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen).)
3. Bei „Ab Artikel“ **„0“ eintragen** – auch wenn dort schon eine Zahl steht ([Abschnitt 7.4](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)).
4. „Lauf starten“.
5. Am Ende öffnet sich der eBay-Tab und lädt hoch. Erscheint „✅ … hochgeladen“, ist alles erledigt. Erscheint „Upload zu eBay fehlgeschlagen: unbekannt“, siehe [Abschnitt 12.4](#12-hochladen-zu-ebay).

### 21.3 Dauerbetrieb (24/7) einrichten

1. Ersten Lauf wie 21.1 machen und prüfen, dass die Ergebnisse stimmen.
2. Lauf-Karte: „Dauerhaft wiederholen“ einschalten.
3. „Pause … Minuten“ einstellen (Pause zwischen den Läufen).
4. „Angebote von eBay laden“, „Ab Artikel“ 0, „Lauf starten“.
5. Tracker-Tab offen lassen, PC nicht in den Ruhezustand gehen lassen. Tipp: Tracker in ein eigenes Chrome-Fenster ziehen. Im Dauerbetrieb nicht auf „Pausieren“ klicken, wenn du nicht anhalten willst (das sagt den nächsten geplanten Lauf ab).
6. Nach einem Neustart von Chrome oder PC: Tracker öffnen, „Angebote von eBay laden“, „Ab Artikel“ 0, „Lauf starten“. Der Haken „Dauerhaft wiederholen“ ist noch gesetzt, der Dauerbetrieb geht nach diesem Lauf von selbst weiter.

### 21.4 Nach einer Notbremse

1. Tabelle nach Status sortieren, Ursache suchen ([Abschnitt 16.2](#16-schutz-bei-sperren-und-fehlern-kurz-warten-und-notbremse)).
2. Ursache beheben (warten, weniger bei „Gleichzeitig“ bzw. Einstellungen korrigieren).
3. Entweder mit „Lauf starten“ fortsetzen (macht an der Stelle weiter, Tabelle bleibt) oder neu beginnen: „Angebote von eBay laden“, „Ab Artikel“ 0, „Lauf starten“ (Tabelle wird geleert).

### 21.5 Fehlgeschlagene Artikel noch einmal prüfen

Einen eigenen Knopf dafür gibt es nicht mehr.
- Zeilen mit „ERROR_503“ prüft der Tracker beim Fortsetzen nach „Pausieren“ und nach „⏳ Kurz warten!“ von selbst zuerst. Nach einem fertigen Lauf prüft „Lauf starten“ (sobald klickbar) nur diese Zeilen und lädt danach hoch ([Abschnitt 7.5](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)).
- Alle anderen fehlgeschlagenen Artikel werden beim nächsten vollständigen Lauf wieder geprüft.

### 21.6 Lauf fortsetzen nach Absturz oder geschlossenem Tab

Siehe [Abschnitt 7.8](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen). Kurz: Tracker öffnen, „Angebote von eBay laden“, „Ab Artikel“ prüfen, einmal „Pausieren“, dann „Lauf starten“.

### 21.7 Hochladen hat nicht geklappt

1. Auf `ebay.<Land>/sh/reports/uploads` nachsehen, ob die Datei doch angekommen ist ([Abschnitt 12.4](#12-hochladen-zu-ebay)).
2. Wenn nicht: im Dauerbetrieb einfach den nächsten Lauf abwarten; sonst „Angebote von eBay laden“, „Ab Artikel“ 0, „Lauf starten“ ([Abschnitt 12.6](#12-hochladen-zu-ebay)).

### 21.8 Rund um ein Update

1. Vor dem Update im Tracker „Pausieren“ klicken (ein Neustart von Chrome beendet den Lauf sowieso).
2. Update mit `update.bat` (bzw. auf dem Mac `update.command`) ausführen, siehe `konto-und-installation.md`, Abschnitte 12 und 13.
3. Chrome **komplett** neu starten oder in `chrome://extensions` bei Cash Lister auf „Neu laden“ klicken (Hintergrunddienst aktualisieren, `konto-und-installation.md`, Abschnitt 17).
4. Tracker über die Seitenleiste neu öffnen. Prüfen, ob Filter und Upload-Einstellungen noch stimmen.
5. „Angebote von eBay laden“, „Ab Artikel“ prüfen bzw. „0“, „Lauf starten“.

---

## 22. Häufige Fragen (allgemein)

**„Was genau ändert der Tracker bei eBay?“**
Nur Preis und Menge – und er beendet Angebote, wenn du „Angebot beenden“ gewählt hast. Titel, Beschreibung, Bilder, Versand bleiben unverändert.

**„Fasst der Tracker auch Angebote an, die ich selbst eingestellt habe?“**
Nein. Er bearbeitet nur Angebote mit einer Cash-Lister-SKU (endet auf „==“).

**„Kann ich die SKU meiner Angebote ändern?“**
Nicht machen. Ohne die SKU erkennt der Tracker das Amazon-Produkt nicht mehr, und die Produkt-Vergabe zählt das Angebot nicht mehr zu dir.

**„Liest der Tracker, wie viele Stück Amazon auf Lager hat?“**
Nein. Lieferbar → feste Menge aus „Feste Menge“. Nicht lieferbar → Menge 0 oder beenden.

**„Was passiert, wenn bei eBay etwas verkauft wurde?“**
Beim nächsten Lauf mit frischem Bericht setzt der Tracker die Menge wieder auf „Feste Menge“ (falls das Produkt bei Amazon lieferbar ist).

**„Wird ein Angebot beendet, wenn Amazon gerade nicht erreichbar ist?“**
Nein. Abruf-Probleme (Sperre, Zeitüberschreitung, Internet weg) ändern nichts. Nur wenn der Tracker die Seite gelesen und „nicht kaufbar“ festgestellt hat.

**„Warum steht bei ‚Preis‘ der Amazon-Preis?“**
Die Tabelle zeigt, was bei Amazon gelesen wurde. Den eBay-Preis siehst du in der Vorschau im Fenster „Upload-Einstellungen“.

**„Wird automatisch hochgeladen?“**
Ja, immer am Ende eines vollständigen Laufs. Einen Haken zum Abschalten gibt es seit Version 46.0 nicht mehr, einen Knopf zum Hochladen von Hand schon seit Version 45.5 nicht.

**„Kann ich die Ergebnisse als Datei speichern?“**
Auf der Tracker-Seite nicht mehr. Was eBay mit jeder hochgeladenen Zeile gemacht hat, steht in der Ergebnisdatei auf der eBay-Upload-Seite ([Abschnitt 14.4](#14-die-ebay-berichtsseiten-downloads-und-uploads)).

**„Kann ich mehrere eBay-Länder tracken?“**
Pro Lauf nur ein Land („eBay-Seite“). **Nicht sicher belegt:** der empfohlene Weg für mehrere Länder oder mehrere eBay-Konten. Der Tracker arbeitet mit dem eBay-Konto, mit dem du in diesem Chrome-Profil angemeldet bist. Frag den Betreiber, wie du mehrere Shops am besten trennst.

**„Kann ich Tracker und Browser-Lister gleichzeitig laufen lassen?“**
**Nicht sicher belegt.** Beide öffnen Amazon-Tabs; mehr gleichzeitige Anfragen machen Sperren wahrscheinlicher und belasten den Rechner.

**„Wie oft sollte ich tracken?“**
**Nicht sicher belegt:** eine Empfehlung. Frag den Betreiber.

**„Werden meine Tracker-Einstellungen gesichert?“**
Ja. Lieferant, eBay-Seite, „Gleichzeitig“, „Dauerhaft wiederholen“ und „Pause … Minuten“, die Upload-Einstellungen, die Sheet-Adressen und „Preis endet auf …“ sind in „Einstellungen exportieren“ und in der Server-Sicherung enthalten (Einstellungen, Reiter „Sicherung“, siehe `einstellungen.md`). **Nicht** enthalten sind die Ergebnistabelle und die Position. Nach dem Einspielen von Einstellungen offene Tracker-Seiten neu laden.

**„Muss ich etwas speichern?“**
Nein. Alles im Tracker wird beim Ändern bzw. beim Verlassen des Feldes gespeichert.

**„Was bedeutet ‚Skipped‘?“**
Übersprungen, weil das Angebot nicht zum Lieferanten passt – praktisch nur bei „Lieferant“ = „Keiner“. Es wird nichts geändert.

**„Wieso gibt es keinen Stopp-Knopf?“**
„Pausieren“ übernimmt das. Siehe [Abschnitt 7.6](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen).

**„Die Seitenleiste zeigt ‚Server nicht erreicht‘ – läuft der Tracker trotzdem?“**
Ja. Prüfen und Hochladen laufen weiter. Nur der Abgleich der Produkt-Vergabe meldet dann „Produkt-Vergabe: Server nicht erreichbar.“

**„Wo finde ich die Versionsnummer?“**
Unten in der Seitenleiste, z. B. „Version 46.0“.

---

## 23. Probleme und Lösungen (allgemein)

**Erst das Wichtigste:** Kurz nach einem Update der Extension verhält sich der Tracker seltsam (Knöpfe tun nichts, alle Zeilen mit „Could not establish connection …“ oder „message port closed“, „Angebote von eBay laden“ meldet „keine Antwort vom Hintergrund“, im Fenster „Upload-Einstellungen“ stehen „Angebot beenden“ und „5“)? → **Hintergrunddienst aktualisieren:** Chrome komplett schließen (auch unten rechts im Infobereich) und neu starten; hilft das nicht, in `chrome://extensions` bei Cash Lister auf das Kreispfeil-Symbol (Neu laden) klicken (Schritte in `konto-und-installation.md`, Abschnitt 17). Beides unterbricht einen laufenden Tracker-Lauf – vorher „Pausieren“ klicken. Danach den Tracker neu öffnen.

| Problem | Mögliche Ursache | Lösung |
|---|---|---|
| Fenster „Für den Tracker brauchst du die Ultimate-Mitgliedschaft.“, danach leere Seite | nicht angemeldet, Zugang abgeschaltet oder Abo gesperrt | [Abschnitt 3](#3-tracker-öffnen-und-voraussetzungen) |
| „Tracker“ in der Seitenleiste grau | dasselbe | im Dashboard klären |
| „Lauf starten“ grau | keine Angebote geladen, oder ein Lauf ist gerade fertig geworden | „Angebote von eBay laden“ ([Abschnitte 5](#5-angebote-laden-von-ebay-oder-als-eigene-datei) und [7.7](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)) |
| Lauf prüft nur die letzten Angebote der Liste | „Ab Artikel“ stand noch auf der Zahl vom letzten Lauf | vor jedem Lauf „0“ eintragen ([Abschnitt 7.4](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)) |
| Ergebnistabelle nach Absturz und neuem Start leer | Lauf war vor dem Schließen nicht pausiert | [Abschnitt 7.8](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen) |
| „Upload-Einstellungen“ zeigt „Angebot beenden“ und „5“ statt deiner Werte | Einstellungen beim Öffnen nicht geladen | Hintergrunddienst aktualisieren ([Abschnitt 3](#3-tracker-öffnen-und-voraussetzungen)) |
| „Bericht: keine geladen“ nach dem Laden | Filter („Lieferant“, „eBay-Seite“, „Preis endet auf …“), falsche Datei, keine Cash-Lister-Angebote | [Abschnitt 5](#5-angebote-laden-von-ebay-oder-als-eigene-datei), Probleme |
| Alle Zeilen „Skipped“ | „Lieferant“ = „Keiner“ | auf „Amazon“ stellen |
| Viele „nicht verfügbar“ trotz Lieferbarkeit | falsche „eBay-Seite“, zu kleine „Max. verlängerte Lieferzeit“, unbekannter Amazon-Text | [Abschnitt 9](#9-die-tabelle-verarbeitete-artikel-und-die-status-texte), Probleme |
| Ständig „⏳ Kurz warten!“ | Amazon bremst, oder Internet instabil | weniger bei „Gleichzeitig“, längere Pausen, Internet prüfen |
| Notbremse | Sperre oder falsche Einstellungen, oder wirklich viele nicht lieferbare Produkte | [Abschnitt 16.2](#16-schutz-bei-sperren-und-fehlern-kurz-warten-und-notbremse) |
| Preise ohne Aufschlag | Preistafel in den Einstellungen nie gespeichert | [Abschnitt 10](#10-preise-und-mengen-so-rechnet-der-tracker), Probleme |
| Änderungen landen auf der falschen eBay-Seite | „eBay-Seite“ ≠ „Domain“, oder „eBay-Seite“ = „Keine“ | beides auf dasselbe Land |
| „Upload zu eBay fehlgeschlagen: unbekannt“ | eBay brauchte länger als 90 Sekunden | [Abschnitt 12.4](#12-hochladen-zu-ebay) |
| Upload gescheitert, wie wiederholen? | kein Knopf mehr dafür | [Abschnitt 12.6](#12-hochladen-zu-ebay) |
| eBay lehnt Zeilen ab | eBay-Regeln, z. B. Verkaufslimit | [Abschnitt 12.5](#12-hochladen-zu-ebay), Ergebnisdatei prüfen |
| Dauerbetrieb läuft nicht weiter | Tab zu, „Pausieren“, Notbremse, Ruhezustand, Neustart | [Abschnitt 15.3](#15-automatik-dauerhaft-wiederholen-247) |
| Ergebnistabelle plötzlich leer | neuer Lauf oder automatischer Lauf leert die Tabelle | normal |
| Laufzeit und „Verarbeitet“ springen auf 0 | jeder Start setzt sie zurück – auch das Fortsetzen nach „Pausieren“ und der automatische Neustart nach der Sperr-Pause | normal, [Abschnitt 7.3](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen) |
| Laufzeit zählt nach dem Ende weiter | Anzeige wird erst beim nächsten Start bzw. bei „Pausieren“ angehalten | normal, [Abschnitt 7.3](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen) |
| Tab-Titel „⛔ Tracker angehalten …“ bleibt | Notbremse; der Titel bleibt bis zum Neuladen der Seite | Zum Weitermachen musst du nicht neu laden – „Lauf starten“ genügt. Lädst du die Seite neu, bleiben Ergebnisse und Position erhalten, der geladene Bericht aber nicht (danach „Angebote von eBay laden“). |
| Lauf endet viel zu früh und lädt nur einen Teil hoch | während des Laufs Filter geändert, Bericht neu geladen oder Papierkorb bei „Bericht“ geklickt | Diese Bedienelemente nur benutzen, wenn kein Lauf läuft (vorher „Pausieren“). Danach einen neuen vollständigen Lauf machen. |
| Viele rote Sheet-Meldungen | Web-App-URL fehlt oder Script nicht freigegeben | [Abschnitt 17.4](#17-die-karte-google-sheets-duplikat-abgleich) |
| Bei jedem Laden kommt eine Datei „doppelte_beenden_…“ | „Beenden-CSV für Duplikate erstellen“ ist an | Datei bei eBay hochladen; Schalter bei Bedarf ausschalten |
| Ein unbekannter Status-Text | – | wird als endgültig behandelt; Vorschau prüfen, Text an den Betreiber melden |
| Knöpfe „Get Listings From Ebay“, „Retry Failed Listings“, „Update Listings“, „Export CSV“ nicht zu finden | „Get Listings From Ebay“ heißt seit Version 46.0 „Angebote von eBay laden“; die anderen gibt es schon seit Version 45.5 nicht mehr | [Abschnitt 26](#26-neu-in-version-460) |
| Vorschau zeigt bei „Preis“ „NaN“, oder die Preise sind rund 98 € zu hoch | „Preisendung“ in den Einstellungen leer (Schalter an) bzw. „99“ statt „0,99“ | [Abschnitt 10.2](#10-preise-und-mengen-so-rechnet-der-tracker) |
| Dauerbetrieb steht nach „Dauerbetrieb: neuer Lauf startet (0 Zeilen).“ | kein Angebot hat die Filter überstanden | [Abschnitt 15](#15-automatik-dauerhaft-wiederholen-247), Probleme |

Wenn nichts davon hilft: an den Betreiber wenden und mitschicken: Version (unten in der Seitenleiste), was du gemacht hast, den genauen Wortlaut der Meldung bzw. einen Screenshot (ohne Passwörter), betroffene Status-Texte mit ein, zwei Beispiel-Links, ob der Hintergrunddienst schon aktualisiert wurde.

---

## 24. Standardwerte auf einen Blick

| Einstellung | Standard | Erlaubt / Hinweis |
|---|---|---|
| „Lieferant“ | „Amazon“ | immer „Amazon“ benutzen |
| „eBay-Seite“ | aus „Domain“ in den Einstellungen, sonst „USA“ | nicht „Keine“ |
| „Gleichzeitig“ | 5 | 1–10 |
| „Ab Artikel“ | 0 | ab 0 |
| „Dauerhaft wiederholen“ | aus | – |
| „Pause … Minuten“ | 60 | mindestens 1; leer oder 0 zählt als 60 |
| „Preis endet auf (Cent, mit Komma getrennt)“ | leer | – |
| Google-Sheet-Felder | leer | – |
| „Bestand aktualisieren“ | an | – |
| „Preis aktualisieren“ | an | – |
| „Ausverkaufte / fehlgeschlagene Artikel“ | „Menge auf 0 setzen“ | sofern nicht anders gespeichert |
| „Feste Menge“ | 1 | sofern nicht anders gespeichert |
| Hochladen | automatisch nach jedem vollständigen Lauf | nicht abschaltbar |
| Wartezeit pro Amazon-Seite | bis 45 s laden, dann bis 30 s lesen | fest |
| Wartezeit Bericht | bis 10 Minuten | fest |
| Wartezeit Upload-Bestätigung im Tracker | 90 Sekunden | fest |
| eBay-Upload-Seite laden | bis 60 Sekunden | fest |
| Sperr-Pause „⏳ Kurz warten!“ | nach mehr als 10 „ERROR_503“-Fehlern ohne „Success“ dazwischen, 120 s | fest |
| Hängengebliebene Amazon-Arbeits-Tabs | werden nach etwa 5 bis 8 Minuten von selbst geschlossen | fest |
| eBay-Upload-Tab | schließt sich bei rechtzeitiger Bestätigung selbst, sonst nach etwa 25 bis 28 Minuten | fest |
| Notbremse | 200 Artikel hintereinander nicht kaufbar, oder ab 200 bewerteten Artikeln mehr als 70 % ohne Erfolg | fest |
| Tabelle während des Laufs | neueste 300 Zeilen sichtbar | alle bleiben gespeichert |
| „Max. verlängerte Lieferzeit“ (Einstellungen, Reiter „Produkt-Filter“) | 20 Tage | wirkt im Tracker immer, auch bei ausgeschaltetem Schalter |
| „Beenden-CSV für Duplikate erstellen“ (Einstellungen, Reiter „eBay & Rahmenbedingungen“) | aus | – |

---

## 25. Was hier nicht sicher belegt ist

- Wie der eBay-Bericht „alle aktiven Angebote“ in der eBay-Oberfläche genau heißt und ob eBay die Spaltenüberschriften („Item number“, „Custom label (SKU)“, „Start price“, „Listing site“) in jedem Konto genau so benennt.
- Welche Werte eBay in der Spalte „Listing site“ einträgt (wichtig für den Filter „eBay-Seite“).
- Ob eBay im Bericht Preise mit Punkt oder Komma schreibt (davon hängt ab, ob „Preis endet auf …“ überhaupt greift; Endungen mit Null am Ende greifen nie).
- Ob das Grau-Bleiben von „Lauf starten“ und das Weiterzählen der „Laufzeit“ nach einem fertigen Lauf Absicht sind.
- Eine verlässliche Dauer pro Artikel bzw. pro Lauf.
- Ob der Tracker bei minimiertem Fenster langsamer wird.
- Ein „bester“ Wert für „Gleichzeitig“ und eine empfohlene Pause zwischen Läufen im Dauerbetrieb.
- Ob die Erkennung von „lieferbar“, „Versand durch Amazon/Prime“ und „kostenloser Versand“ auf jeder Amazon-Seite stimmt, und welche Amazon-Verfügbarkeitstexte der Tracker nicht kennt.
- In welchen Fällen Amazon statt eines Preises einen Hinweis zeigt, dass kein Preis verfügbar ist (den der Tracker wie eine Sperre wertet).
- Wie die Menüpunkte zu den eBay-Berichtsseiten (Downloads, Uploads) im Seller Hub genau heißen.
- Der genaue Wortlaut, mit dem eBay ein erreichtes Verkaufslimit in der Ergebnisdatei meldet, und die Spalten der eBay-Ergebnisdatei.
- Wie eBay leere Felder in der Upload-Datei behandelt (leere Menge bei ausgeschaltetem „Bestand aktualisieren“, leerer Preis bei ausgeschaltetem „Preis aktualisieren“) und ganz leere Änderungszeilen (beide Haken aus).
- Ob das automatische Hochladen auf eBay-Seiten in Französisch oder Spanisch funktioniert.
- Wie die Schritte im eBay-Hochlade-Fenster im Einzelnen aussehen.
- Wie das Google Sheet und das Apps-Script eingerichtet werden (Script ist nicht Teil der Extension) und ob das Lesen über die Web-App-Adresse klappt.
- Wie lange eine Reservierung der Produkt-Vergabe hält und wann „Sicherung aktiv – nichts freigegeben“ vorkommt (das entscheidet der Betreiber bzw. der Vergabe-Dienst).
- Was eBay mit Angeboten mit Menge 0 macht, ob sie im Bericht weiter auftauchen und wie Verkaufslimits genau wirken (eBay-Regeln).
- Wie lange Amazon jeweils bremst.
- Empfehlungen für mehrere eBay-Konten/Länder und für gleichzeitigen Betrieb von Tracker und Browser-Lister.
- Ein bequemerer Weg, wenn die Notbremse bei einem wirklich zu mehr als 70 % nicht lieferbaren Bestand bei jedem Lauf auslöst.

---

## 26. Neu in Version 46.0

Für Kunden, die den Tracker aus Version 45.x kennen (die Versionsnummer steht jetzt unten in der Seitenleiste). Einiges davon fehlte schon in Version 45.5.

1. **Neuer Name und neuer Weg dorthin.** Aus „CSV Tracker“ wurde „**Tracker**“. Das kleine Fenster beim Klick auf das Symbol gibt es nicht mehr – es öffnet sich das Dashboard. Den Tracker öffnest du über die Seitenleiste („Tracker“) oder die Dashboard-Karte „Tracker“. Ist er schon offen, springt der Klick in den offenen Tab.
2. **Neues Design, alles deutsch.** Die wichtigsten Umbenennungen:

   | Früher | Jetzt |
   |---|---|
   | Seitentitel „eBay CSV Processor“ | „Tracker“ / „Preise & Bestand mit Amazon abgleichen“ |
   | „Get Listings From Ebay“ / „or“ | „Angebote von eBay laden“ / „oder“ |
   | „📄 Raw Items:“ | „Bericht:“ |
   | „Importing... (Anzahl)“ | „Bericht wird eingelesen … (Anzahl)“ |
   | „Settings“ / Fenster „Export Settings“ | „Upload-Einstellungen“ |
   | „▶ Running Time:“ / „Processed Items During Runtime:“ | „Laufzeit:“ / „Verarbeitet:“ |
   | „Supplier:“ („None“, „Amazon“) | „Lieferant“ („Keiner“, „Amazon“) |
   | „Listing Site:“ („Germany“ usw.) | „eBay-Seite“ („Deutschland“ usw.) |
   | „Threads:“ | „Gleichzeitig“ |
   | „Start“ / „Pause“ | „Lauf starten“ / „Pausieren“ |
   | „Enable continuous tracking (24/7)“ / „Timeout (min):“ | „Dauerhaft wiederholen“ / „Pause … Minuten“ |
   | „Price ends with …“ (in „➕ Sonstiges“) | „Preis endet auf (Cent, mit Komma getrennt)“ in der Karte „Filter“ |
   | „Processed Items“ (Spalten Action, ItemID, CustomLabel, StartPrice, Quantity, Brand, Status) | „Verarbeitete Artikel“ (Spalten Aktion, Artikelnummer, SKU, Preis, Menge, Marke, Status) |
   | „Update Stock Quantity“ / „Update Price“ | „Bestand aktualisieren“ / „Preis aktualisieren“ |
   | „Out of Stock/Failed Items“: „Set Quantity to 0“ / „End Item“ | „Ausverkaufte / fehlgeschlagene Artikel“: „Menge auf 0 setzen“ / „Angebot beenden“ |
   | „Total Failed / Out of Stock:“ | „Fehlgeschlagen / ausverkauft insgesamt:“ |
   | „Fixed Quantity“ / „Preview (First 3 Items)“ / „Save Settings“ | „Feste Menge“ / „Vorschau (erste 3 Artikel)“ / „Einstellungen speichern“ |
   | Fenster „⏳ Hold Tight!“ | Fenster „⏳ Kurz warten!“ |
   | Meldungen „Continuous Tracking …“ | Meldungen „Dauerbetrieb …“ |

   Auch die Status-Texte sind deutsch, z. B. „Error: Artikel bei Amazon nicht verfügbar“ statt „Error: Item is not available on Amazon“ ([Abschnitt 9.2](#9-die-tabelle-verarbeitete-artikel-und-die-status-texte)), ebenso die Tab-Titel beim Hochladen zu eBay.
3. **Hochladen nur noch automatisch.** Der Haken „Upload to eBay after processing“ ist weg (neu in 46.0): Nach jedem vollständigen Lauf wird immer hochgeladen. Die Knöpfe „Update Listings“, „Update Listings To Ebay“ und „Export CSV“ gibt es schon seit Version 45.5 nicht mehr.
4. **Schon in Version 45.5 entfernt:** „Retry Failed Listings“, „Total Errors in Table:“ und die Symbol-Knöpfe 📥 📤 🗑️ unter der Tabelle (Ergebnisse importieren, als CSV speichern, leeren). „ERROR_503“-Zeilen prüft der Tracker beim Fortsetzen von selbst noch einmal.
5. **Preise kommen aus den Einstellungen.** Statt aus dem Popup (Karte „💶 Preise“) kommen die Aufschläge jetzt aus Einstellungen → Reiter „Preise & Listing“ → Karte „Preise“; die eBay-Domain für den Bericht aus derselben Seite, Karte „Listing“. Die zweite Preistafel für „Neu: Sonstige“ gibt es nicht mehr – eine Tafel für alle Zustände.
6. **Dashboard zeigt den Tracker.** Fortschritt, „pausiert“, „angehalten“, „unterbrochen“ und den nächsten geplanten Lauf siehst du jetzt auch im Dashboard ([Abschnitt 19](#19-der-tracker-im-dashboard)).

Unverändert geblieben sind das Prüfen bei Amazon, die Preisrechnung, „nur Änderungen hochladen“, der Dauerbetrieb, die Sperr-Pause, die Notbremse, Google Sheets und der Abgleich der Produkt-Vergabe. Was sich danach in 46.1 bis 46.3 an Notbremse und Prüfen bei Amazon geändert hat, steht in Abschnitt 27.

---

## 27. Neu in Version 46.1 bis 46.3

Kleine Änderungen nach 46.0 im Tracker:

1. **Kurze Pause je Amazon-Tab.** Nach dem Auslesen bleibt jeder Amazon-Tab noch einen kurzen Moment offen (fest, unter einer Sekunde, nicht einstellbar), bevor er sich schließt ([Abschnitt 7.2](#7-ein-lauf-starten-pausieren-fortsetzen-abbrechen)). Ein Lauf dauert dadurch etwas länger. Das Feld „Pause (s)“, das es nur in Version 46.1 gab, ist seit 46.2 wieder weg; ein dort eingetragener Wert wirkt nicht mehr.
2. **Zweiter Auslöser der Notbremse.** Die Notbremse hält den Lauf jetzt auch an, wenn 200 Artikel hintereinander als nicht kaufbar gelten, mit eigener Meldung und eigenem Tab-Titel ([Abschnitt 16.2](#16-schutz-bei-sperren-und-fehlern-kurz-warten-und-notbremse)).
