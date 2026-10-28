# Verkaufs-Übersicht (Produktübersicht) und CSV-Lister

Dieser Bereich erklärt zwei Werkzeuge von Cash Lister:

- die **Verkaufs-Übersicht**: Damit findest du aus deinen eBay-Berichten Ladenhüter, erzeugst eine Beenden-Datei für eBay und siehst, wie lange neue Angebote bis zum ersten Verkauf brauchen.
- den **CSV-Lister**: ein Lister, der Produkte aus deiner Produkt-Datenbank als **eine Datei** zu eBay hochlädt. Seit Version 46.0 steht er allen Kunden zur Verfügung. Oben auf seiner Seite steht weiterhin „neu · im Test“.

Manche Kunden sagen zur Verkaufs-Übersicht auch „Produktübersicht“. In der Oberfläche heißt sie überall „Verkaufs-Übersicht“. Meint jemand mit „Produktübersicht“ dagegen die Liste der Produkte, die noch auf das Listen warten, ist die **Produkt-Datenbank** gemeint (siehe produkte-finden-und-datenbank.md). Im Zweifel kurz nachfragen: „Meinst du die Auswertung deiner eBay-Verkäufe (Verkaufs-Übersicht) oder die Liste deiner noch nicht gelisteten Produkte (Produkt-Datenbank)?“

**Wo alles ist (Kurzfassung):** Beide Werkzeuge öffnest du über die **Seitenleiste** links, die auf jeder Seite von Cash Lister steht: die Verkaufs-Übersicht unter „Auswerten“, den CSV-Lister unter „Arbeiten“. Den CSV-Lister erreichst du zusätzlich über das **Dashboard** (Abschnitt „Vorgänge“). Das Dashboard öffnet sich, wenn du in Chrome auf das Symbol von Cash Lister klickst (siehe dashboard.md).

## Inhalt

- [Teil A: Verkaufs-Übersicht](#teil-a-verkaufs-übersicht)
  - [A1. Wozu und wo du sie findest](#a1-wozu-und-wo-du-sie-findest)
  - [A2. Woher die Daten kommen](#a2-woher-die-daten-kommen)
  - [A3. Aufbau der Seite](#a3-aufbau-der-seite)
  - [A4. Berichte einlesen – Schritt für Schritt](#a4-berichte-einlesen--schritt-für-schritt)
  - [A5. Was beim Einlesen passiert (die Regeln)](#a5-was-beim-einlesen-passiert-die-regeln)
  - [A6. Reiter „Wann zuletzt verkauft“](#a6-reiter-wann-zuletzt-verkauft)
  - [A7. Beenden-CSV erstellen und bei eBay hochladen](#a7-beenden-csv-erstellen-und-bei-ebay-hochladen)
  - [A8. Reiter „Wann zum ersten Mal verkauft“](#a8-reiter-wann-zum-ersten-mal-verkauft)
  - [A9. Gespeicherten Verlauf löschen](#a9-gespeicherten-verlauf-löschen)
  - [A10. Wo die Daten liegen](#a10-wo-die-daten-liegen)
  - [A11. Häufige Fragen zur Verkaufs-Übersicht](#a11-häufige-fragen-zur-verkaufs-übersicht)
  - [A12. Probleme und Lösungen zur Verkaufs-Übersicht](#a12-probleme-und-lösungen-zur-verkaufs-übersicht)
- [Teil B: CSV-Lister](#teil-b-csv-lister)
  - [B1. Was der CSV-Lister ist](#b1-was-der-csv-lister-ist)
  - [B2. Wer den CSV-Lister sieht und wie du ihn öffnest](#b2-wer-den-csv-lister-sieht-und-wie-du-ihn-öffnest)
  - [B3. Die gemeinsame Produkt-Datenbank und „in Arbeit“](#b3-die-gemeinsame-produkt-datenbank-und-in-arbeit)
  - [B4. Voraussetzungen](#b4-voraussetzungen)
  - [B5. Einstellungen, die der CSV-Lister benutzt](#b5-einstellungen-die-der-csv-lister-benutzt)
  - [B6. Aufbau der CSV-Lister-Seite](#b6-aufbau-der-csv-lister-seite)
  - [B7. Der CSV-Lister im Dashboard und in der Seitenleiste](#b7-der-csv-lister-im-dashboard-und-in-der-seitenleiste)
  - [B8. Tageskontingent](#b8-tageskontingent)
  - [B9. Was bei einem Lauf passiert](#b9-was-bei-einem-lauf-passiert)
  - [B10. Was im Angebot steht (Aufbau der CSV-Datei)](#b10-was-im-angebot-steht-aufbau-der-csv-datei)
  - [B11. Gebührenprüfung bei „NUR Neu: Sonstige“](#b11-gebührenprüfung-bei-nur-neu-sonstige)
  - [B12. Bilder](#b12-bilder)
  - [B13. Upload zu eBay und das Ergebnis](#b13-upload-zu-ebay-und-das-ergebnis)
  - [B14. Wartende Produkte: abholen oder vergessen](#b14-wartende-produkte-abholen-oder-vergessen)
  - [B15. Was mit jedem Produkt passiert (Übersicht)](#b15-was-mit-jedem-produkt-passiert-übersicht)
  - [B16. Abbrechen, Anhalten, Seite geschlossen](#b16-abbrechen-anhalten-seite-geschlossen)
  - [B17. Meldungen an den Betreiber](#b17-meldungen-an-den-betreiber)
  - [B18. Schritt für Schritt: dein erster Lauf](#b18-schritt-für-schritt-dein-erster-lauf)
  - [B19. Häufige Fragen zum CSV-Lister](#b19-häufige-fragen-zum-csv-lister)
  - [B20. Probleme und Lösungen zum CSV-Lister](#b20-probleme-und-lösungen-zum-csv-lister)
- [Neu in Version 46.0](#neu-in-version-460)
- [Was dieser Bereich nicht sicher weiß](#was-dieser-bereich-nicht-sicher-weiß)

---

## Teil A: Verkaufs-Übersicht

### A1. Wozu und wo du sie findest

Die Verkaufs-Übersicht beantwortet zwei Fragen zu deinen **aktuell aktiven** eBay-Angeboten:

1. **„Wann zuletzt verkauft?“** – Welche Angebote haben schon länger nichts mehr verkauft (Ladenhüter)? Die kannst du markieren und als **Beenden-CSV** herunterladen, um sie bei eBay auf einen Schlag zu beenden.
2. **„Wann zum ersten Mal verkauft?“** – Wie viele Tage dauert es im Schnitt, bis ein neues Angebot seinen ersten Verkauf hat (Anlaufzeit)?

**So öffnest du sie:**

1. Klicke in Chrome auf das Symbol von Cash Lister. Es öffnet sich das Dashboard.
2. Melde dich an, falls noch nicht geschehen (Anmeldung im Dashboard, siehe konto-und-installation.md). Ohne Anmeldung sind die Einträge in der Seitenleiste – außer „Dashboard“ und „Einstellungen“ – ausgegraut und nicht anklickbar.
3. Klicke in der **Seitenleiste** links in der Gruppe „Auswerten“ auf „Verkaufs-Übersicht“.
4. Die Seite öffnet sich in einem **eigenen Tab**. Der Tab heißt „Cash Lister – Verkaufs-Übersicht“, oben auf der Seite steht „Verkaufs-Übersicht“ und darunter „Ladenhüter erkennen und Anlaufzeit messen“.
5. Ist die Verkaufs-Übersicht schon in einem Tab offen, springt der Klick in diesen Tab, statt einen zweiten zu öffnen.

Gut zu wissen:

- Die Verkaufs-Übersicht ist für alle angemeldeten Kunden da, eine besondere Freischaltung braucht es nicht.
- Im Dashboard gibt es **keine** eigene Karte für die Verkaufs-Übersicht. Der Weg führt immer über die Seitenleiste.
- Ist dein Abo gesperrt oder dein Zugang abgeschaltet, ist der Eintrag ebenfalls ausgegraut (unten in der Seitenleiste steht dann z. B. „Abo gesperrt“). Siehe konto-und-installation.md.

### A2. Woher die Daten kommen

Die Verkaufs-Übersicht holt sich **nichts selbst** bei eBay. Sie wertet nur zwei Berichte aus, die du vorher bei eBay herunterlädst und hier einliest:

| Bericht | Feld auf der Seite | Woran die Seite ihn erkennt (Spaltennamen in der Kopfzeile) |
|---|---|---|
| **Angebotsbericht** (aktive Angebote) | „Aktive Angebote“ (klein daneben „Active-Listings-CSV“) | „Item number“, „Custom label“, „Available quantity“, „Sold quantity“, „Start date“ |
| **Bestellbericht** (Verkäufe) | „Bestellbericht“ (klein daneben „Orders-CSV“) | „Artikelnummer“, „Bestandseinheit“, „Verkauft am“ |

Wichtig dabei:

- Die Seite erkennt den Bericht **am Inhalt (an der Kopfzeile)**, nicht am Dateinamen und nicht daran, in welches Feld du ihn ziehst. Ziehst du den Bestellbericht aus Versehen in das Feld für aktive Angebote, wird er trotzdem richtig als Bestellbericht eingelesen.
- Der Angebotsbericht wird mit **englischen** Spaltennamen erwartet, der Bestellbericht mit **deutschen** Spaltennamen. Ein Bestellbericht mit englischen Spaltennamen wird nicht erkannt.
- eBays **Änderungsvorlagen** (z. B. für Preis und Menge) haben zwar ähnliche Spalten, werden aber bewusst **nicht** als Angebotsbericht angenommen – sonst würden sie deine gespeicherten Angebote ersetzen.
- Die Datei muss eine CSV-Datei mit **Semikolon** als Trennzeichen sein (so, wie eBay sie liefert). Öffne und speichere die Berichte **nicht** vorher in Excel – Excel kann das Trennzeichen oder die Zeichenkodierung ändern, dann erkennt die Seite die Datei nicht mehr.
- Aus dem Angebotsbericht liest die Seite je Angebot: Artikelnummer, Titel, Custom Label, verfügbare Menge, aktuellen Preis, Startdatum und die Gesamtzahl verkaufter Stück („Sold quantity“).
- Aus dem Bestellbericht liest die Seite je verkaufter Position: Transaktionsnummer, Verkaufsprotokollnummer, Bestellnummer, Artikelnummer, Bestandseinheit, Anzahl und das Datum „Verkauft am“ (ersatzweise das Zahlungsdatum).
- Zugeordnet werden Verkäufe und Angebote über die **eBay-Artikelnummer** (nicht über das Custom Label / die Bestandseinheit).

**Custom Label** (auch „SKU“ oder „Bestandseinheit“ genannt) ist deine eigene Kennung für ein Angebot. **Artikelnummer** ist die Nummer, die eBay jedem Angebot gibt.

**Wo du die Berichte bekommst:** Beide Berichte lädst du selbst bei eBay herunter. Belegt ist: Den Bericht über alle aktiven Angebote erzeugt eBay im Seller Hub auf der Seite für Berichte zum Herunterladen (Adresse **www.ebay.de/sh/reports/downloads**) – von dort holt sich auch der Tracker seine Angebotsliste.

**Nicht sicher belegt:** die genauen Beschriftungen der Auswahlfelder und Knöpfe auf dieser eBay-Seite und auf welchem Weg genau du den **Bestellbericht** erzeugst. Die Extension schreibt das nicht vor, und eBay ändert seine Seiten ab und zu. Wenn du einen Bericht nicht findest, frag den Betreiber.

### A3. Aufbau der Seite

Links steht die Seitenleiste (wie auf allen Seiten von Cash Lister). Rechts davon, von oben nach unten:

#### Karte „Berichte einlesen“

- **Überschrift** „Berichte einlesen“ mit dem Hinweis „eBay-Berichte als CSV – einzeln oder beide auf einmal, Reihenfolge egal“.
- **Knopf „Berichte aktualisieren“** (rechts oben in der Karte) – öffnet eine Dateiauswahl, in der du **einen oder mehrere** Berichte auf einmal auswählen kannst (z. B. Angebotsbericht und Bestellbericht zusammen). Die Reihenfolge ist egal.
- **Feld „Aktive Angebote“** (klein daneben „Active-Listings-CSV“) – darunter steht „— Datei wählen oder hierher ziehen —“. Ein Klick auf das Feld öffnet die Dateiauswahl; du kannst die Datei auch hineinziehen. Nach dem Einlesen wird das Feld grün und zeigt z. B. den Dateinamen mit „✓“, die Zahl der Angebote und „eingelesen am …“ mit Datum und Uhrzeit. Diese Anzeige bleibt auch nach dem Schließen und erneuten Öffnen der Seite stehen – so siehst du immer, welcher Stand drin ist.
- **Feld „Bestellbericht“** (klein daneben „Orders-CSV“) – genauso. Nach dem Einlesen zeigt es die Zahl der Bestellungen, „neueste vom …“ (das Datum der neuesten Bestellung) und „eingelesen am …“.
- **Ziehen und Ablegen überall:** Du kannst Berichte auch irgendwo auf die Seite ziehen (nicht nur in die Felder, auch auf den Knopf). Die Seite erkennt selbst, welcher Bericht es ist.
- **Statuszeile** unter den Feldern: zeigt während des Einlesens „Wird eingelesen …“ und danach das Ergebnis, z. B.
  - „Angebote: … aktiv“ (bei Bedarf mit „· … Bestellungen zu nicht aktiven Angeboten aussortiert“)
  - „Bestellungen: … gelesen, davon … zu aktiven Angeboten · neueste vom …“
  - „Nichts eingelesen.“
  - Beim Öffnen der Seite steht dort kurz „Gespeicherter Stand wird geladen …“ – bei großen Shops kann das ein, zwei Sekunden dauern.
- **Fehlerzeile** (rot) – Fehler beim Einlesen beginnen mit „Fehler:“, meist gefolgt vom Dateinamen. Siehe [A12](#a12-probleme-und-lösungen-zur-verkaufs-übersicht).
- **Kurzübersicht** mit drei Angaben:
  - „… aktive Angebote“
  - „… Bestellungen im Verlauf“ (nur Bestellungen, die zu aktuell aktiven Angeboten gehören)
  - „Verkäufe vom … bis …“ (Zeitraum der gespeicherten Verkäufe; das Enddatum ist der „Stand der Verkaufsdaten“, siehe [A6](#a6-reiter-wann-zuletzt-verkauft)). Vor dem ersten Einlesen stehen dort Nullen bzw. „–“.
- **Fußzeile der Karte:** links der Hinweis „Gespeichert wird immer nur **ein Shop**.“, rechts der kleine rote Knopf **„Gespeicherten Verlauf löschen“** (siehe [A9](#a9-gespeicherten-verlauf-löschen)). Daneben erscheint nach dem Löschen „Verlauf gelöscht.“.

#### Reiter

Sobald Daten da sind, erscheinen unter der Karte zwei Reiter (runde Knöpfe):

- „Wann zuletzt verkauft“ (vorausgewählt, dunkel hinterlegt)
- „Wann zum ersten Mal verkauft“

Beim allerersten Öffnen (noch nichts eingelesen) gibt es keine Reiter; die Karte „Wann zuletzt verkauft“ steht aber schon da – mit Schwelle und Knopf, jedoch ohne Tabelle. Nach „Gespeicherten Verlauf löschen“ verschwinden Reiter und Karten, bis wieder etwas eingelesen ist.

### A4. Berichte einlesen – Schritt für Schritt

**Erstes Einlesen:**

1. Lade bei eBay den aktuellen Angebotsbericht (aktive Angebote) und den Bestellbericht herunter. Ändere die Dateien nicht.
2. Öffne die Verkaufs-Übersicht (Seitenleiste → „Auswerten“ → „Verkaufs-Übersicht“).
3. Klicke auf „Berichte aktualisieren“ und wähle **beide** Dateien gleichzeitig aus (oder ziehe beide auf die Seite).
4. Warte, bis in der Statuszeile das Ergebnis steht (statt „Wird eingelesen …“).
5. Prüfe die Kurzübersicht: Stimmen die Zahl der aktiven Angebote und der Zeitraum der Verkäufe ungefähr?
6. Wechsle in den Reiter „Wann zuletzt verkauft“.

**Später aktualisieren (empfohlen):**

1. Lade bei eBay einen **frischen** Angebotsbericht und einen **frischen** Bestellbericht herunter – möglichst am selben Tag.
2. Lies beide über „Berichte aktualisieren“ ein.
3. Der Verkaufsverlauf wird dabei **ergänzt**, nicht ersetzt (siehe [A5](#a5-was-beim-einlesen-passiert-die-regeln)).

**Regeln beim Auswählen mehrerer Dateien:**

- Höchstens **ein** Angebotsbericht auf einmal. Sonst kommt: „Bitte nur einen Angebotsbericht auf einmal – sonst ist unklar, welcher der aktuelle ist.“
- **Mehrere Bestellberichte** auf einmal sind erlaubt (z. B. mehrere Zeiträume). Überschneiden sie sich, wird nichts doppelt gezählt.
- Erst werden **alle** gewählten Dateien geprüft, dann gespeichert. Ist eine Datei kaputt, wird gar nichts gespeichert – du bekommst eine Fehlermeldung mit dem Dateinamen.
- Während eingelesen wird, ist der Knopf gesperrt. Wählst du in der Zeit weitere Dateien, steht dort: „Es wird gerade noch eingelesen – bitte … danach noch einmal wählen.“
- Dieselbe Datei kannst du jederzeit noch einmal wählen – sie wird dann erneut eingelesen.

### A5. Was beim Einlesen passiert (die Regeln)

**Grundregel: Angezeigt werden nur die aktuell aktiven Angebote.**

- **Angebotsbericht:** Er ist eine Momentaufnahme. Die gespeicherten Angebote werden bei jedem Einlesen **komplett ersetzt**. Gespeicherte Bestellungen zu Angeboten, die im neuen Bericht nicht mehr vorkommen (also bei eBay beendet sind), werden dabei entfernt. Das meldet die Statuszeile als „… Bestellungen zu nicht aktiven Angeboten aussortiert“.
- **Bestellbericht:** Alle Bestellungen werden gespeichert – auch die zu Angeboten, die (noch) nicht im gespeicherten Angebotsbericht stehen. Ausgewertet werden aber nur die zu aktiven Angeboten. Den Rest räumt der nächste Angebotsbericht weg.
- **Reihenfolge egal:** Du kannst erst den Bestellbericht und dann den Angebotsbericht einlesen oder umgekehrt.
- **Nichts wird doppelt gezählt:** Jede verkaufte Position hat bei eBay eine eigene Transaktionsnummer. Liest du denselben Bericht zweimal ein oder überschneiden sich zwei Berichte, zählt jede Position nur einmal. Eine Sammelbestellung mit mehreren Produkten bleibt dabei vollständig.
- **Der Verlauf wächst weiter:** Für aktive Angebote behält die Seite auch ältere Verkäufe, die in einem neuen Bestellbericht nicht mehr drinstehen. Der gespeicherte Verlauf kann also weiter zurückreichen als eBays Bericht. Folge: Wenn du den Verlauf löschst und neu einliest, hast du danach eventuell **weniger** Daten als vorher.
- **Nur ein Shop:** Die Übersicht speichert immer nur einen Shop. Liest du einen Angebotsbericht ein, in dem **keine einzige** der gespeicherten Artikelnummern vorkommt, fragt die Seite nach (das passiert nur, wenn schon Bestellungen gespeichert sind – sonst gibt es nichts zu verlieren, und der neue Bericht wird ohne Rückfrage übernommen):

  > Keines der … gespeicherten Angebote steht in diesem Angebotsbericht – das ist ein anderer Shop.
  >
  > Die Übersicht speichert immer nur einen Shop. Beim Einlesen fällt der gespeicherte Verkaufsverlauf des bisherigen Shops weg.
  >
  > Trotzdem einlesen?

  - „Abbrechen“ → es wird nichts eingelesen („Nichts eingelesen.“).
  - „OK“ → der neue Shop ersetzt den alten; der Verkaufsverlauf des alten Shops ist danach weg. Bleibt dabei keine einzige Bestellung übrig, zeigt das Feld „Bestellbericht“ wieder „— Datei wählen oder hierher ziehen —“. Lies dann den Bestellbericht des neuen Shops ein.
  - Schon **eine** gemeinsame Artikelnummer reicht, damit die Seite den Bericht als denselben Shop ansieht (auch nach großem Aufräumen).
- **Bestellbericht ohne Treffer:** Ist schon ein Angebotsbericht gespeichert und gehört keine einzige Bestellung aus einem Bestellbericht zu diesen Angeboten, erscheint (rot):

  > Achtung: Keine Bestellung aus … gehört zu den gespeicherten Angeboten. Ist der Bestellbericht von einem anderen Shop? Dann den passenden Angebotsbericht dazu einlesen.

  Die Bestellungen sind trotzdem gespeichert.
- **Nach jedem erfolgreichen Einlesen** verfallen Haken, die du von Hand **gesetzt** hast (ein damals abgehaktes Angebot kann inzwischen wieder verkauft haben). Haken, die du von Hand **entfernt** hast, bleiben entfernt. Siehe [A6](#a6-reiter-wann-zuletzt-verkauft).

### A6. Reiter „Wann zuletzt verkauft“

Hier findest du Ladenhüter: Angebote, die schon mindestens einmal verkauft haben, aber seit einer bestimmten Zahl von Tagen nicht mehr.

#### Bedienelemente

- **Überschrift** „Wann zuletzt verkauft“, daneben die **Zählzeile**, z. B. „12 von 340 Angeboten ab 30 Tagen ohne Verkauf (gezählt bis 20.09.2026, Stand der Verkaufsdaten)“.
- **„Vorschlag ab [Zahl] Tagen ohne Verkauf“** – die Schwelle.
  - Standardwert: **30**. Vorgesehen: 1 bis 365.
  - Die Zahl wird gespeichert und ist beim nächsten Öffnen wieder da. Sie gehört auch zu den Einstellungen, die beim Export und bei der Einstellungs-Sicherung auf dem Server mitgehen.
  - Änderst du die Zahl, wird die Tabelle sofort neu berechnet.
- **Knopf „Beenden-CSV für markierte erstellen“** – siehe [A7](#a7-beenden-csv-erstellen-und-bei-ebay-hochladen).
- **„… markiert“** – wie viele Zeilen gerade einen Haken haben.
- Darunter ggf. der orange Warnkasten (siehe unten) und nach dem Erstellen der Datei eine graue Hinweiszeile.

#### Die Tabelle

| Spalte | Bedeutung |
|---|---|
| „✓“ | Haken: soll dieses Angebot in die Beenden-CSV? |
| „Titel“ | Titel des Angebots aus dem Angebotsbericht |
| „Artikelnr.“ | eBay-Artikelnummer; ein Klick öffnet das Angebot auf ebay.de in einem neuen Tab |
| „Start“ | Startdatum des Angebots |
| „Letzter Verkauf“ | Datum des letzten gespeicherten Verkaufs |
| „Tage ohne Verkauf“ | Tage zwischen dem letzten Verkauf und dem **Stand der Verkaufsdaten** (siehe unten). Ab der Schwelle als rote Marke hervorgehoben. „Datum unbekannt“ (orange Marke), wenn Verkäufe da sind, aber kein lesbares Datum. |
| „Verkäufe“ | Anzahl verkaufter Stück im **gespeicherten** Verlauf (nicht eBays Gesamtzahl) |
| „Bestand“ | verfügbare Menge laut Angebotsbericht; „0“ wird als orange Marke hervorgehoben |

- **Sortieren:** Klick auf eine Spaltenüberschrift sortiert nach dieser Spalte, ein zweiter Klick dreht die Richtung um. Standard: „Tage ohne Verkauf“, längste zuerst. Angebote mit „Datum unbekannt“ stehen dabei ganz oben, damit du sie nachsehen kannst. Die Spalte „✓“ ist nicht sortierbar.
- **Rötlich hinterlegte Zeilen** sind die Vorschläge: Angebote mit mindestens so vielen Tagen ohne Verkauf wie die Schwelle. Sie haben automatisch einen Haken.
- **Wer fehlt in der Tabelle?** Angebote, die im gespeicherten Verlauf **noch nie** verkauft haben. „Seit wann nicht mehr verkauft“ ergibt bei null Verkäufen keinen Sinn – solche Angebote musst du direkt bei eBay prüfen.
- **„Datum unbekannt“** wird nie vorgeschlagen (kein automatischer Haken), damit nicht aus Versehen ein frisch verkauftes Angebot beendet wird.
- Lange Tabellen scrollen in ihrem eigenen Bereich; die Spaltenüberschriften bleiben dabei oben stehen.

#### Haken von Hand

- Du kannst jeden Haken setzen oder entfernen. Deine Änderungen werden gespeichert und bleiben auch nach Sortieren, Ändern der Schwelle, Schließen der Seite und Neustart des Browsers erhalten.
- Setzt du einen Haken wieder auf den Vorschlag zurück, gilt er nicht mehr als Hand-Entscheidung.
- Nach dem nächsten erfolgreichen Einlesen eines Berichts verfallen von Hand **gesetzte** Haken; von Hand **entfernte** bleiben entfernt.

#### „Tage ohne Verkauf“ zählen bis zum Stand der Verkaufsdaten – nicht bis heute

Das ist der häufigste Grund für Verwunderung, deshalb genau:

- Der **Stand der Verkaufsdaten** ist das Datum der neuesten gespeicherten Bestellung – oder das Datum im Dateinamen des Bestellberichts, falls das später ist. eBay schreibt bei Bestellberichten das Ende des Berichtszeitraums in den Dateinamen. Hast du die Datei umbenannt, kann die Seite dieses Datum nicht lesen; dann zählt nur die neueste Bestellung.
- Beispiel: Bestellbericht vom 20.09., letzte Bestellung am 15.09. → gezählt wird bis zum 20.09. (bis dahin wurde nachweislich nichts mehr verkauft).
- Warum nicht bis heute? Sonst würde die Zahl jeden Tag wachsen, an dem du keinen neuen Bestellbericht einliest, und Angebote, die zwischendurch verkauft haben, sähen wie Ladenhüter aus.
- In der Zählzeile steht immer „(gezählt bis …, Stand der Verkaufsdaten)“.

#### Warnung: Verkaufsdaten älter als der Angebotsbericht

Ist der Angebotsbericht **mehr als 2 Tage neuer** als der Stand der Verkaufsdaten, erscheint ein oranger Kasten:

> Die Verkaufsdaten reichen nur bis …, der Angebotsbericht ist vom …. Verkäufe dazwischen fehlen – bitte den aktuellen Bestellbericht einlesen. Bis dahin wird nichts zum Beenden vorgeschlagen.

Solange dieser Kasten da ist, bekommt **keine** Zeile automatisch einen Haken (auch wenn die Tage-Zahl rot markiert ist). Grund: Sonst würden laufende Angebote beendet, die in der fehlenden Zeit verkauft haben. Lösung: aktuellen Bestellbericht einlesen.

Das Datum des Angebotsberichts nimmt die Seite aus dem Dateinamen; bei umbenannter Datei nimmt sie den Zeitpunkt des Einlesens (nur wenn der Angebotsbericht nach dem Bestellbericht eingelesen wurde).

### A7. Beenden-CSV erstellen und bei eBay hochladen

Die Beenden-CSV ist eine Datei, mit der eBay alle darin genannten Angebote beendet, sobald du sie im Seller Hub hochlädst. **Die Verkaufs-Übersicht beendet selbst nichts.**

**Schritt für Schritt:**

1. Stelle sicher, dass beide Berichte frisch eingelesen sind und kein oranger Warnkasten zu sehen ist.
2. Stelle im Reiter „Wann zuletzt verkauft“ die Schwelle ein (z. B. 30 Tage).
3. Prüfe die rötlichen, vorgehakten Zeilen. Entferne Haken bei Angeboten, die du behalten willst; setze Haken bei weiteren, die weg sollen.
4. Klicke auf „Beenden-CSV für markierte erstellen“.
5. Chrome lädt die Datei `beenden_JJJJ-MM-TT.csv` (mit dem heutigen Datum) herunter. Auf der Seite steht: „Beenden-Datei mit … Angebot(en) heruntergeladen – bei eBay hochladen, erst dann werden sie beendet.“
6. Öffne im eBay Seller Hub die Seite für Uploads (Adresse **www.ebay.de/sh/reports/uploads**; dort gibt es den Knopf „Vorlage hochladen“) und lade die Datei dort hoch.
7. Warte, bis eBay die Datei verarbeitet hat. Erst dann sind die Angebote beendet.
8. Lade danach bei eBay einen **neuen Angebotsbericht** herunter und lies ihn ein. Erst dann verschwinden die beendeten Angebote auch aus der Verkaufs-Übersicht (samt ihren gespeicherten Bestellungen).

**Was in der Datei steht:** je markiertem Angebot eine Zeile mit der Aktion „Beenden“ (EndItem), der Artikelnummer und dem Beendigungsgrund „nicht mehr verfügbar“ (NotAvailable). Es ist dasselbe Format wie bei den Beenden-Dateien des Trackers.

**Hinweise:**

- Ist nichts markiert, kommt die Meldung „Nichts markiert.“ und es wird keine Datei erzeugt.
- In die Datei kommen nur echte eBay-Artikelnummern (nur Ziffern); jede Nummer nur einmal.
- Die Beenden-CSV ändert nichts an deiner Produkt-Datenbank und nichts an der Produktvergabe.

Die Adresse der Upload-Seite ist belegt (dieselbe Seite benutzt auch der CSV-Lister). **Nicht sicher belegt:** über welche Menüpunkte du im Seller Hub dorthin klickst und was dort nach dem Hochladen genau angezeigt wird – das ist eBays Seite, nicht die der Extension.

### A8. Reiter „Wann zum ersten Mal verkauft“

Hier siehst du, wie lange neue Angebote bis zum ersten Verkauf brauchen.

- **Kennzahlen oben:**
  - „Ø … Tage bis zum ersten Verkauf“ (Durchschnitt, mit einer Nachkommastelle, z. B. „Ø 12,4 Tage“)
  - „Median …“ (der mittlere Wert: die Hälfte der Angebote war schneller, die Hälfte langsamer – weniger anfällig für Ausreißer als der Durchschnitt)
  - „Basis: … Angebote“ (wie viele Angebote in die Rechnung eingehen)
  - Gibt es noch keine verlässlichen Fälle: „Noch keine verlässliche Anlaufzeit.“
- **Tabelle:** „Titel“, „Artikelnr.“ (Link zum Angebot), „Start“, „Erster Verkauf“, „Tage bis Erstverkauf“. Sortiert nach den Tagen, schnellste zuerst. Diese Tabelle lässt sich nicht umsortieren und hat keine Haken.

**Welche Angebote zählen?** Nur verlässliche Fälle:

- Die Seite muss **alle** Verkäufe des Angebots kennen. Das prüft sie so: eBays „Sold quantity“ (Gesamtzahl über die ganze Laufzeit) darf nicht größer sein als die Zahl der gespeicherten Verkäufe. Ist sie größer, gab es Verkäufe vor deinem gespeicherten Zeitraum – dann ist der früheste gespeicherte Verkauf nicht sicher der erste, und das Angebot wird weggelassen.
- Der erste Verkauf darf nicht vor dem Startdatum liegen.
- Unsichere Fälle werden weder angezeigt noch mitgerechnet.

Deshalb kann die Basis deutlich kleiner sein als die Zahl deiner Angebote, besonders bei alten Angeboten.

### A9. Gespeicherten Verlauf löschen

- Kleiner roter Knopf „Gespeicherten Verlauf löschen“ unten rechts in der Karte „Berichte einlesen“.
- Rückfrage: „Den kompletten gespeicherten Verlauf löschen? Angebote und Bestellungen werden entfernt.“
- Nach „OK“: alle gespeicherten Angebote, Bestellungen und Einlese-Stände sind weg, ebenso alle deine Haken-Entscheidungen (gesetzte und entfernte). Neben dem Knopf steht „Verlauf gelöscht.“, die beiden Felder zeigen wieder „— Datei wählen oder hierher ziehen —“.
- Die Schwelle (z. B. 30 Tage) bleibt.
- Während gerade eingelesen wird, geht das nicht: „Es wird gerade eingelesen – bitte danach löschen.“
- **Achtung:** Der gespeicherte Verlauf kann weiter zurückreichen als eBays Bestellbericht. Nach dem Löschen und Neu-Einlesen hast du unter Umständen weniger Verkaufsdaten als vorher. Lösche nur, wenn du wirklich neu anfangen willst (z. B. Wechsel des Shops).

### A10. Wo die Daten liegen

- Angebote, Bestellungen und deine Haken liegen **nur in diesem Chrome-Profil auf deinem Rechner**. Anders als die Produkt-Datenbank liegen sie **nicht** auf dem Server.
- Sie werden **nicht** mit „Einstellungen exportieren“ gesichert und **nicht** über die Einstellungs-Sicherung auf dem Server. Nur die Schwelle („Vorschlag ab … Tagen ohne Verkauf“) geht mit.
- Auf einem anderen Rechner oder in einem anderen Chrome-Profil ist die Verkaufs-Übersicht leer, bis du dort die Berichte einliest.
- **Verbindung zum Dashboard:** Die Kennzahl „Aktive Angebote“ im Dashboard nimmt den jüngeren Stand aus Tracker und Verkaufs-Übersicht. Stammt er aus der Verkaufs-Übersicht, steht darunter „laut Verkaufs-Übersicht · Stand …“ mit dem Datum deines zuletzt eingelesenen Angebotsberichts (siehe dashboard.md).

### A11. Häufige Fragen zur Verkaufs-Übersicht

**Wo finde ich die Verkaufs-Übersicht jetzt?**
In der Seitenleiste links unter „Auswerten“ → „Verkaufs-Übersicht“. Das kleine Fenster beim Klick auf das Symbol gibt es seit Version 46.0 nicht mehr.

**Warum kann ich „Verkaufs-Übersicht“ in der Seitenleiste nicht anklicken?**
Du bist nicht angemeldet, dein Zugang ist abgeschaltet oder dein Abo ist gesperrt. Was gilt, steht ganz unten in der Seitenleiste. Melde dich im Dashboard an (siehe konto-und-installation.md).

**Muss ich beide Berichte einlesen?**
Für sinnvolle Ergebnisse ja. Ohne Angebotsbericht weiß die Seite nicht, welche Angebote aktiv sind; ohne Bestellbericht kennt sie keine Verkäufe.

**Ist die Reihenfolge wichtig?**
Nein. Du kannst beide Dateien auch gleichzeitig über „Berichte aktualisieren“ auswählen.

**Werden Verkäufe doppelt gezählt, wenn ich einen Bericht zweimal einlese?**
Nein. Jede Position zählt über ihre Transaktionsnummer nur einmal.

**Warum fehlt ein Angebot in „Wann zuletzt verkauft“?**
Es hat im gespeicherten Verlauf noch keinen einzigen Verkauf – oder es ist im zuletzt eingelesenen Angebotsbericht nicht mehr aktiv.

**Warum zeigt „Tage ohne Verkauf“ weniger Tage, als seit dem letzten Verkauf bis heute vergangen sind?**
Weil bis zum Stand der Verkaufsdaten gezählt wird, nicht bis heute. Lies einen aktuellen Bestellbericht ein, dann rückt der Stand nach vorn.

**Warum ist nichts vorgehakt?**
Entweder hat kein Angebot die Schwelle erreicht, oder der orange Kasten „Die Verkaufsdaten reichen nur bis …“ ist zu sehen. Dann zuerst den aktuellen Bestellbericht einlesen.

**Kann ich mehrere Shops auswerten?**
Nicht gleichzeitig. Gespeichert wird immer nur ein Shop. Wechselst du den Shop, fällt der Verlauf des alten Shops weg (mit Rückfrage). **Nicht sicher belegt:** ob die Nutzung getrennter Chrome-Profile je Shop mit deiner Anmeldung vorgesehen ist – frag im Zweifel den Betreiber.

**Beendet die Seite meine Angebote?**
Nein. Sie erzeugt nur die Beenden-CSV. Beendet wird erst, wenn du die Datei bei eBay hochlädst.

**Was bedeutet „Median“?**
Der mittlere Wert aller verlässlichen Anlaufzeiten. Ein paar extrem langsame Angebote verzerren ihn weniger als den Durchschnitt.

**Warum ist die „Basis“ bei der Anlaufzeit so klein?**
Weil nur Angebote zählen, deren Verkäufe vollständig im gespeicherten Verlauf liegen (siehe [A8](#a8-reiter-wann-zum-ersten-mal-verkauft)).

**Bleiben meine Haken erhalten, wenn ich die Seite schließe?**
Ja. Nach dem nächsten Einlesen verfallen aber die von Hand gesetzten Haken (die entfernten bleiben entfernt).

**Sind meine Daten nach dem Update auf 46.0 noch da?**
Die Verkaufs-Übersicht speichert in deinem Chrome-Profil; am Speicher hat sich mit 46.0 nichts geändert. **Nicht sicher belegt:** ob das in jedem Einzelfall so ist (z. B. wenn die Extension bei dir neu installiert statt aktualisiert wurde – dann können lokale Daten fehlen). Lies die Berichte im Zweifel einfach neu ein.

**Zeigt mir die Verkaufs-Übersicht auch Angebote, die nie verkauft haben?**
Nein, nur Angebote mit mindestens einem gespeicherten Verkauf.

### A12. Probleme und Lösungen zur Verkaufs-Übersicht

Fehler beim Einlesen stehen rot unter den Feldern und beginnen mit „Fehler:“, meistens gefolgt vom Dateinamen, z. B. „Fehler: bericht.csv: weder Angebots- noch Bestellbericht erkannt.“ In der Statuszeile steht dann „Nichts eingelesen.“ In der Tabelle unten ist der Teil nach dem Dateinamen aufgeführt.

| Meldung / Problem | Bedeutung | Lösung |
|---|---|---|
| „Fehler: …: weder Angebots- noch Bestellbericht erkannt.“ | Die Kopfzeile der Datei passt zu keinem der beiden Berichte. Häufige Ursachen: falsche Datei, in Excel geöffnet und neu gespeichert, Bestellbericht mit englischen Spaltennamen, eine eBay-Änderungsvorlage (z. B. für Preis/Menge) statt eines Berichts. | Den Bericht frisch bei eBay herunterladen und unverändert einlesen. |
| „Angebotsbericht: Kopfzeile nicht gefunden (erwarte 'Item number', 'Custom label', 'Available quantity', 'Sold quantity', 'Start date').“ | Der Angebotsbericht hat nicht die erwarteten Spalten. | Unveränderten Angebotsbericht verwenden. |
| „Bestellbericht: Kopfzeile nicht gefunden (erwarte 'Artikelnummer', 'Bestandseinheit', 'Verkauft am').“ | Der Bestellbericht hat nicht die erwarteten (deutschen) Spalten. | Unveränderten deutschen Bestellbericht verwenden. |
| „Angebotsbericht: keine Datenzeilen gefunden.“ | Der Angebotsbericht enthält keine Angebote. | Prüfen, ob der richtige Bericht heruntergeladen wurde. |
| „Bestellbericht: keine Bestellzeilen gefunden.“ | Keine Zeile mit gültiger Artikelnummer. | Zeitraum des Berichts prüfen; anderen Bericht herunterladen. |
| „Bitte nur einen Angebotsbericht auf einmal – sonst ist unklar, welcher der aktuelle ist.“ | Du hast zwei Angebotsberichte gleichzeitig gewählt. | Nur den neuesten einlesen. |
| Rückfrage „Keines der … gespeicherten Angebote steht in diesem Angebotsbericht – das ist ein anderer Shop.“ | Der Bericht gehört zu einem anderen Shop. | „Abbrechen“, wenn du aus Versehen den falschen Shop gewählt hast. „OK“ nur, wenn du wirklich wechseln willst. |
| „Achtung: Keine Bestellung aus … gehört zu den gespeicherten Angeboten. …“ | Bestellbericht und Angebotsbericht passen nicht zusammen (anderer Shop?). | Den passenden Angebotsbericht einlesen. |
| Oranger Kasten „Die Verkaufsdaten reichen nur bis …“ | Bestellbericht zu alt im Vergleich zum Angebotsbericht; es wird nichts vorgeschlagen. | Aktuellen Bestellbericht einlesen. |
| „Es wird gerade noch eingelesen – bitte … danach noch einmal wählen.“ | Ein Einlesen läuft noch. | Warten und die Datei danach erneut wählen. |
| „Es wird gerade eingelesen – bitte danach löschen.“ | Löschen während des Einlesens. | Warten, dann erneut löschen. |
| „Datenbank: …“ | Der Speicher im Browser ist nicht lesbar oder schreibbar. | Seite neu laden. Bleibt es, Chrome neu starten. **Nicht sicher belegt:** weitere Ursachen – dann den Betreiber mit dem genauen Text fragen. |
| „Nichts markiert.“ | Beim Beenden-CSV ist keine Zeile angehakt. | Haken setzen, dann erneut klicken. |
| Ein Angebot steht noch drin, obwohl ich es beendet habe | Die Übersicht kennt nur den zuletzt eingelesenen Angebotsbericht. | Neuen Angebotsbericht einlesen. |
| Zahlen sehen nach dem Einlesen „komisch“ aus | Oft: Verkaufsdaten und Angebotsbericht von verschiedenen Tagen oder verschiedenen Shops. | Beide Berichte frisch am selben Tag herunterladen und zusammen einlesen. |
| Eintrag „Verkaufs-Übersicht“ in der Seitenleiste ist ausgegraut | Nicht angemeldet, Zugang abgeschaltet oder Abo gesperrt. | Im Dashboard anmelden; bei „Abo gesperrt“ siehe konto-und-installation.md. |
| Ich finde den Knopf „Verkaufs-Übersicht“ unter „Werkzeuge“ nicht mehr | Den Bereich „Werkzeuge“ im kleinen Fenster gibt es seit 46.0 nicht mehr. | Seitenleiste → „Auswerten“ → „Verkaufs-Übersicht“. |

---

## Teil B: CSV-Lister

### B1. Was der CSV-Lister ist

Der CSV-Lister stellt Produkte aus deiner **Produkt-Datenbank** auf eBay ein – aber anders als der Browser-Lister (früher „Bulk-Lister“):

- Der **Browser-Lister** füllt für jedes Produkt das eBay-Formular im Browser aus.
- Der **CSV-Lister** sammelt alle Produkte eines Laufs, baut daraus **eine Datei** im eBay-Upload-Format (CSV) und lädt sie **selbst** im eBay Seller Hub hoch. Danach holt er eBays Ergebnisdatei und sieht für jedes Produkt einzeln nach, ob es gelistet oder abgelehnt wurde.

**Du musst keine CSV-Datei selbst bauen oder hochladen.** Die Produkte kommen aus deiner Produkt-Datenbank (dorthin kommen sie über den Import, siehe produkte-finden-und-datenbank.md). Die Produkt-Datenbank liegt seit Version 46.0 für dein Konto auf dem Server – wie der CSV-Lister damit umgeht, steht in [B3](#b3-die-gemeinsame-produkt-datenbank-und-in-arbeit).

Der CSV-Lister ist auf **eBay.de** ausgelegt: Die Datei ist für Deutschland und Euro angelegt, und die Kategorien kommen aus dem deutschen eBay-Kategoriebaum.

Die Seite trägt oben den Hinweis „CSV-Lister **neu · im Test**“ und darunter „Angebote aus der Datenbank bauen und als Datei bei eBay hochladen“. Browser-Lister und CSV-Lister gibt es nebeneinander; du kannst wählen, welchen du benutzt, oder beide gleichzeitig laufen lassen (siehe [B3](#b3-die-gemeinsame-produkt-datenbank-und-in-arbeit)).

### B2. Wer den CSV-Lister sieht und wie du ihn öffnest

**Seit Version 46.0 steht der CSV-Lister allen Kunden zur Verfügung.** Einen Zugangscode brauchst du nicht mehr.

**So öffnest du ihn:**

1. Klicke in Chrome auf das Symbol von Cash Lister – das Dashboard öffnet sich.
2. Melde dich an, falls noch nicht geschehen.
3. Entweder: in der **Seitenleiste** links in der Gruppe „Arbeiten“ auf „CSV-Lister“ klicken.
   Oder: im **Dashboard** im Abschnitt „Vorgänge“ auf die Karte „CSV-Lister“ klicken.
4. Die Seite öffnet sich in einem **eigenen Tab** mit dem Titel „Cash Lister – CSV-Lister“. Ist sie schon offen, springt der Klick in diesen Tab.

**Wenn du den CSV-Lister nicht anklicken kannst oder nicht findest:**

- **Eintrag ausgegraut:** Du bist nicht angemeldet, dein Zugang ist abgeschaltet oder dein Abo ist gesperrt. Was gilt, steht ganz unten in der Seitenleiste („Nicht angemeldet“, „Zugang abgeschaltet“ oder „Abo gesperrt“). Siehe konto-und-installation.md.
- **Eintrag fehlt ganz:** Öffnet sich beim Klick auf das Symbol noch das kleine Fenster statt des Dashboards, oder gibt es gar keine Seitenleiste, läuft bei dir noch eine ältere Version (die Seitenleiste gibt es erst seit 46.0). Sonst schau ganz unten in der Seitenleiste nach der Version: Dort muss „Version 46.0“ (oder höher) stehen. Aktualisiere mit `update.bat`, starte Chrome danach **komplett** neu (alle Chrome-Fenster schließen) bzw. klicke unter `chrome://extensions` bei Cash Lister auf „Neu laden“. Fehlt er danach immer noch, frag den Betreiber.
- **Die Seite zeigt nur „Dieses Modul ist noch im Test“** mit dem Text „Der CSV-Lister wird gerade mit einigen Testern erprobt. Zum Öffnen brauchst du einen Zugangscode.“ und einem Feld „Zugangscode“ mit dem Knopf „Freischalten“: In Version 46.0 erscheint diese Sperre nicht mehr. Siehst du sie, ist bei dir noch der alte Stand geladen – wie oben aktualisieren und Chrome neu starten. Bleibt sie, frag den Betreiber.

### B3. Die gemeinsame Produkt-Datenbank und „in Arbeit“

Seit Version 46.0 liegt die Produkt-Datenbank **je Konto auf dem Server**. Alle deine Geräte (alle Chrome-Profile, in denen du mit deinem Zugang angemeldet bist) sehen dieselbe Liste. Für den CSV-Lister heißt das:

**Produkte nehmen statt nur lesen.** Beim Start eines Laufs **nimmt** der CSV-Lister die Produkte für diesen Lauf aus der Datenbank und markiert sie als **„in Arbeit“** für dieses Gerät. Solange sie so markiert sind:

- bekommt sie **kein anderes Gerät** und **nicht der Browser-Lister** – jeder Lister und jedes Gerät bekommt andere Produkte. Du kannst deshalb den CSV-Lister auf mehreren Geräten oder Browser-Lister und CSV-Lister auf demselben PC **gleichzeitig** laufen lassen.
- stehen sie in der Produkt-Datenbank weiter in der Liste, mit einem Eintrag in der Spalte „In Arbeit“, z. B. „CSV-Lister (dieses Gerät) bis 14:32“. Läuft der CSV-Lister auf einem Gerät mit Gerätenamen (Server-Modus), steht dort z. B. „Server-1 · CSV-Lister bis 14:32“.
- zählen sie im Dashboard bei „Produkte in der Datenbank“ als „in Arbeit“ (z. B. „250 bereit · 30 in Arbeit“).

**Welche Produkte ein Lauf bekommt:** nur freie Produkte (nicht in Arbeit), und zwar in der Reihenfolge, die du in der Produkt-Datenbank bei „Sortierung“ eingestellt hast („Älteste zuerst“ oder „Neuste zuerst“). Diese Sortierung gilt nur für das Gerät, auf dem du sie einstellst (siehe produkte-finden-und-datenbank.md).

**Wie lange „in Arbeit“ gilt:**

- Produkte, an denen der Lauf noch arbeitet, hält die Extension nur **kurz** fest (etwa eine Stunde) und verlängert das laufend, solange der Lauf lebt.
- Ein Produkt, für das eine fertige Zeile entstanden ist, wartet auf den Upload und auf eBays Ergebnis. Es bleibt **bis zu 7 Tage** „in Arbeit“ – so lange darf eBay die Datei verarbeiten, ohne dass ein anderes Gerät das Produkt ein zweites Mal listet. Sobald das Ergebnis verbucht ist, verlässt das Produkt die Datenbank (gelistet oder abgelehnt).

**Was nach dem Lauf mit den Produkten passiert** (Einzelheiten in [B15](#b15-was-mit-jedem-produkt-passiert-übersicht)):

- **gelistet**, **von eBay abgelehnt** oder **übersprungen** → das Produkt verlässt die Datenbank.
- **nicht fertig geworden** (zurückgestellt, abgebrochen, nicht mehr drangekommen, Lauf angehalten, Upload sicher nicht bei eBay angekommen, Seite oder Browser abgestürzt) → das Produkt geht **zurück in die Datenbank**: Die Markierung „in Arbeit“ fällt weg, es ist wieder frei für jedes deiner Geräte und beide Lister. Seine Reservierung aus dem Import bleibt dabei bestehen.

**Ohne Server kein Lauf.** Weil die Datenbank auf dem Server liegt, startet der CSV-Lister keinen Lauf, wenn der Server nicht erreichbar ist. Meist scheitert der Start dann schon beim Prüfen des Tageskontingents („Nicht gestartet: Tageskontingent nicht abrufbar: Claims-Server nicht erreichbar …“), sonst beim Nehmen der Produkte („Server nicht erreichbar – Lauf nicht gestartet. …“); siehe [B20](#b20-probleme-und-lösungen-zum-csv-lister). Anders als der Browser-Lister wartet er nicht, bis der Server wieder da ist – du startest einfach später neu. Unten in der Seitenleiste steht in diesem Fall „Server nicht erreicht“ und „Lister nehmen keine Produkte“.

**Fällt der Server mitten im Lauf aus:** Die Produkte des Laufs hat der CSV-Lister schon beim Start genommen. Der Lauf hält aber spätestens bei der nächsten eBay-Abfrage an, weil die auch über den Server laufen (Meldung beginnt meist mit „Claims-Server nicht erreichbar“). Konnte die Seite Produkte nicht zurückgeben, merkt sie sich das und holt es beim nächsten Öffnen der Seite oder beim nächsten Start von selbst nach.

**Direkt nach dem Update auf 46.0:** Die Extension überträgt deine bisherige (lokale) Produkt-Datenbank automatisch auf den Server. Bei einer großen Liste dauert das eine Weile; im Dashboard steht dann bei „Produkte in der Datenbank“ z. B. „… werden noch auf den Server übertragen“. Solange nimmt der CSV-Lister nur die Produkte, die schon auf dem Server liegen.

**Wenn dir ein Produkt „weggenommen“ wird:** Löschst du in der Produkt-Datenbank ein Produkt, das gerade in Arbeit ist (das geht nur nach einer Rückfrage), oder war die CSV-Lister-Seite so lange angehalten (z. B. Ruhezustand), dass ihre Markierung abgelaufen ist und ein anderes Gerät das Produkt genommen hat, bearbeitet der CSV-Lister es nicht weiter. In der Tabelle steht dann „nicht mehr dran“ bzw. „verworfen (anderes Gerät)“ mit dem Grund „nicht mehr dran – die Seite war angehalten, inzwischen hat ein anderes Gerät das Produkt (oder es wurde gelöscht)“. Eine schon fertige Zeile für so ein Produkt wird nicht hochgeladen – so wird es nicht doppelt gelistet.

**„Alle löschen“ in der Produkt-Datenbank** lässt Produkte, die gerade in Arbeit sind, stehen (siehe produkte-finden-und-datenbank.md). Ein laufender CSV-Lister verliert dadurch also nicht seine Produkte.

### B4. Voraussetzungen

Bevor ein Lauf startet, muss alles hier erfüllt sein. Die Punkte 1 bis 3 prüft die Statuszeile oben auf der Seite (rote Punkte, siehe [B6](#b6-aufbau-der-csv-lister-seite)). Alles ab Punkt 4 prüft die Statuszeile **nicht** – Fehler dort merkst du erst beim Start, im Lauf oder beim Upload:

1. **Angemeldet** in Cash Lister (Anmeldung im Dashboard). Ohne Anmeldung keine eBay-Abfragen, keine Produkt-Datenbank, keine Produktvergabe, kein Tageskontingent.
2. **Namen deiner drei Rahmenbedingungen** (Versand, Zahlung, Rücknahme) in den Einstellungen – Buchstabe für Buchstabe wie im Seller Hub (siehe [B5](#b5-einstellungen-die-der-csv-lister-benutzt)).
3. **Artikelstandort** (Ort oder PLZ) in den Einstellungen.
4. **Server erreichbar** und Abo aktiv. Die Produkt-Datenbank, das Tageskontingent und die eBay-Abfragen laufen über den Server des Betreibers.
5. **Bei eBay angemeldet** – im Seller Hub, **im selben Chrome-Profil**. Der Upload läuft über deinen Seller Hub.
6. **Domain „DE“** in den Einstellungen: Reiter „Preise & Listing“ → Karte „Listing“ → „Domain“ (darunter steht „eBay-Seite, z. B. DE = ebay.de“). Nach einer frischen Installation steht dort normalerweise „DE“; wurden deine Einstellungen vom Server zurückgeholt oder importiert, steht dort der übernommene Wert. Prüfe es vor dem ersten Lauf trotzdem. Die Domain bestimmt zwei Dinge: auf welcher eBay-Seite der Upload stattfindet (bei „DE“ im Seller Hub von ebay.de) und in welcher Sprache die KI den Titel schreibt (bei „DE“ deutsch, bei „USA“ englisch). Steht dort „Keine“, kommt beim Upload „Keine eBay-Domain eingestellt (Einstellungen → Preise & Listing → „Domain“).“
7. **Seller Hub auf Deutsch, Englisch oder Italienisch.** Der Upload sucht im Seller Hub den Knopf „Vorlage hochladen“ (bzw. „Upload template“ / „Carica modello“) und „Datei auswählen“ (bzw. „Choose file“ / „Scegli il file“). In anderen Sprachen findet er ihn nicht.
8. **Eigener OpenAI-Schlüssel mit Guthaben** in den Einstellungen: Reiter „KI“ → Karte „KI (OpenAI)“ → „OpenAI-API-Schlüssel (für die Titel-Generierung)“. Die KI erzeugt den Titel und füllt die Artikelmerkmale. **Achtung:** Die Statuszeile prüft den Schlüssel **nicht** – „Bereit zum Listen“ kann grün sein, obwohl er fehlt. Fehlt er, ist er ungültig oder ist das Guthaben leer, scheitert der KI-Titel bei jedem Produkt; die Produkte werden dann zurückgestellt (siehe [B20](#b20-probleme-und-lösungen-zum-csv-lister)).
9. **Freie Produkte in der Produkt-Datenbank.** Ist sie leer, kommt „Die Produkt-Datenbank ist leer.“; sind alle in Arbeit, kommt „Alle … Produkte der Datenbank sind gerade in Arbeit – auf diesem oder einem anderen Gerät, oder sie warten auf ein eBay-Ergebnis.“
10. **Tageskontingent nicht aufgebraucht** (siehe [B8](#b8-tageskontingent)).
11. **Preis-Einstellungen** im Reiter „Preise & Listing“ (Karte „Preise“) – daraus entsteht der Verkaufspreis. Ergibt sich kein Preis, wird das Produkt übersprungen („kein Verkaufspreis aus der Preisstaffelung“).

### B5. Einstellungen, die der CSV-Lister benutzt

Alle Einstellungen stehen auf der Einstellungsseite („Cash Lister – Einstellungen“). Du erreichst sie über die Seitenleiste („System“ → „Einstellungen“) oder über den Knopf „Einstellungen“ oben rechts auf der CSV-Lister-Seite. Die Einstellungsseite öffnet mit dem ersten Reiter „Preise & Listing“ (war sie schon in einem Tab offen, springt Chrome in diesen Tab) – für die Rahmenbedingungen musst du auf den Reiter „eBay & Rahmenbedingungen“ klicken. Jede Änderung wird gespeichert, sobald du das Feld verlässt; der Knopf „Speichern“ unten zeigt nur „Einstellungen gespeichert“ an. Ausführlich erklärt sind alle Felder in einstellungen.md.

#### Eigene Felder: Reiter „eBay & Rahmenbedingungen“ → Karte „Rahmenbedingungen“

Die Karte trägt neben der Überschrift den Hinweis „CSV-Lister (neuer Lister, im Test)“. Über den Feldern steht: „Die Namen müssen **Buchstabe für Buchstabe** so lauten wie im Seller Hub. Solange einer fehlt, startet der CSV-Lister keinen Lauf.“

| Feld | Was hinein muss | Standard | Typische Fehler |
|---|---|---|---|
| „Versand“ | Name deiner Versand-Rahmenbedingung, genau wie im Seller Hub (Platzhalter im Feld: „genau wie in den Rahmenbedingungen“) | leer | Tippfehler, andere Groß-/Kleinschreibung, anderer Name als im Seller Hub |
| „Zahlung“ | Name deiner Zahlungs-Rahmenbedingung | leer | wie oben |
| „Rücknahme“ | Name deiner Rücknahme-Rahmenbedingung | leer | wie oben |
| „Artikelstandort (Ort oder PLZ)“ | Ort oder Postleitzahl, z. B. „78315“ | leer | leer gelassen |

**Rahmenbedingungen** sind bei eBay gespeicherte Vorlagen für Versand, Zahlung und Rücknahme. Der CSV-Lister trägt nur deren **Namen** in die Datei ein; Versandart, Versandkosten, Bearbeitungszeit und Rücknahmefrist kommen bei eBay aus diesen Vorlagen. Leerzeichen am Anfang und Ende entfernt der CSV-Lister selbst.

**Wenn ein Name nicht passt** (Tippfehler, andere Schreibweise): Der CSV-Lister merkt das nicht, er prüft nur, ob etwas eingetragen ist. Erst eBay lehnt die Zeilen ab (Angabe des Betreibers), und abgelehnte Produkte sind danach **nicht mehr in der Produkt-Datenbank** (siehe [B15](#b15-was-mit-jedem-produkt-passiert-übersicht)). Ein falscher Name kostet also alle Produkte eines Laufs. Darum den **ersten Lauf mit nur 1 Produkt** machen (siehe [B18](#b18-schritt-für-schritt-dein-erster-lauf)). **Nicht sicher belegt:** eBays genauer Wortlaut dazu – er steht in der Spalte „Titel / Grund“ mit „eBay: …“.

#### Weitere Einstellungen, die wirken

| Wo (Reiter → Karte) | Einstellung | Wirkung im CSV-Lister |
|---|---|---|
| „Preise & Listing“ → „Preise“ | „% Aufschlag“, „Fester Aufschlag (€)“, „Variable Preise (nach Preisspanne)“ mit ihren Regeln („ab € … bis € … → …% + € …“), „Preisendung“ | ergeben den Verkaufspreis, genau wie beim Browser-Lister |
| „Preise & Listing“ → „Preise“ | „Als „Neu: Sonstige“ listen (Standard)“ und der Haken „Neu: Sonstige“ in jeder Preisregel | bestimmen, ob ein Produkt als „Neu: Sonstige“ gelistet werden soll (siehe [B10](#b10-was-im-angebot-steht-aufbau-der-csv-datei), Zustand) |
| „Preise & Listing“ → „Preise“ | „NUR „Neu: Sonstige“ listen“ | Soll ein Produkt „Neu: Sonstige“ werden und bietet die Kategorie diesen Zustand nicht an, wird es übersprungen statt als „Neu“ gelistet. Außerdem läuft dann für **jedes** Produkt die Gebührenprüfung (siehe [B11](#b11-gebührenprüfung-bei-nur-neu-sonstige)). |
| „Preise & Listing“ → „Listing“ | „Domain“ | muss „DE“ sein; daraus entstehen die Seller-Hub-Adresse für den Upload und die Sprache des KI-Titels |
| „Produkt-Filter“ → „Beim Listen“ (Hinweis „gilt im Browser-Lister und im CSV-Lister“) | „Nur FBA“ („Amazon muss der Versender sein“, Standard an), „Nur chinesische Verkäufer“ („sortiert alle anderen aus“, Standard aus), „GPSR-Angaben übernehmen“ („Produkte ohne diese Angaben werden übersprungen“, Standard aus) | Vorfilter auf der Amazon-Seite. **Übersprungene Produkte löscht der CSV-Lister aus der Produkt-Datenbank.** Mit „GPSR-Angaben übernehmen“ werden zusätzlich Hersteller und EU-Verantwortlicher eingetragen. |
| „Produkt-Filter“ → „Beim Listen“ | „Markenlos listen“ | Standard **an**: als Marke steht „Markenlos“. Aus: echte Marke (siehe [B10](#b10-was-im-angebot-steht-aufbau-der-csv-datei)). Gilt nur für den CSV-Lister. |
| „Produkt-Filter“ → „Amazon-Filter“ | „Preis ab“ / „Preis bis“ (je mit eigenem Schalter) | Liegt der Amazon-Preis außerhalb, wird das Produkt übersprungen – und beim CSV-Lister damit aus der Produkt-Datenbank gelöscht: „Amazon: Amazon-Preis zu niedrig (Filter „Preis ab“)“ bzw. „Amazon: Amazon-Preis zu hoch (Filter „Preis bis“)“. **Achtung:** Hattest du aus einer älteren Version noch „100“ als Höchstpreis gespeichert, ist der Filter an, und teurere Produkte fallen heraus. |
| „Produkt-Filter“ → „Amazon-Filter“ | „Max. verlängerte Lieferzeit“ (in Tagen) | Zeigt Amazon eine Lieferung, die weiter in der Zukunft liegt als diese Zahl an Tagen, gilt das Produkt als nicht lieferbar: „Amazon: Produkt ist nicht auf Lager“. Beim Listen zählt nur die Zahl (leer = 20), der Schalter daneben wirkt hier nicht (Einzelheiten in einstellungen.md). |
| „Produkt-Filter“ → „Blacklist“ | „Meine Liste“ (ein Wort oder Begriff je Zeile) | Ein Produkt mit einem Wort aus deiner Liste wird übersprungen („Amazon: Produkt enthält ein Wort aus der Blacklist: …“) |
| „eBay & Rahmenbedingungen“ → „Beim Einstellen“ | „Mehrwertsteuer im Angebot angeben“ + „Mehrwertsteuersatz … %“ | Ist der Schalter an, wird der Satz als MwSt. eingetragen (Feld-Standard 19) |
| „eBay & Rahmenbedingungen“ → „Neu: Sonstige“ | „Zustandsbeschreibung“ | wird als Zustandsbeschreibung eingetragen – nur bei „Neu: Sonstige“. Höchstens 1000 Zeichen werden übernommen. Vorbelegt (sobald die Einstellungsseite einmal geöffnet wurde) mit: „Neuware. Die Originalverpackung wurde ggf. zur Prüfung geöffnet. Der Artikel ist unbenutzt, vollständig und voll funktionsfähig, ohne Gebrauchsspuren.“ |
| „Beschreibungsvorlage“ → „Beschreibungsvorlage (HTML)“ | deine eigene Vorlage (Hinweis: „leer lassen = schlichte Beschreibung aus dem Produkttext“) | leer = schlichte Beschreibung (siehe [B10](#b10-was-im-angebot-steht-aufbau-der-csv-datei)) |
| „KI“ → „KI (OpenAI)“ | „OpenAI-API-Schlüssel (für die Titel-Generierung)“ | nötig für KI-Titel und KI-Merkmale |
| „KI“ → „KI (OpenAI)“ | „OpenAI-Modell (für KI-Beschreibung & Generierung)“ | gilt für das Ausfüllen der Artikelmerkmale und die Spielzeug-Frage; der Titel läuft immer mit dem Standardmodell „gpt-4o-mini“ |

**FBA** heißt „Fulfillment by Amazon“: Amazon lagert und versendet das Produkt selbst. **GPSR** ist die EU-Produktsicherheitsverordnung; dazu gehören Angaben zum Hersteller und zur verantwortlichen Person in der EU.

#### Was der CSV-Lister **nicht** benutzt

Diese Einstellungen gelten für den Browser-Lister bzw. andere Teile, der CSV-Lister liest sie nicht:

- „Anzeigengebühr (%)“ und „Listing automatisch absenden“ (Reiter „Preise & Listing“) – der CSV-Lister setzt keine Werbung und hat kein „Absenden“.
- „Pflicht-Artikelmerkmale mit KI ausfüllen“ / „Optionale Artikelmerkmale mit KI ausfüllen“ (Reiter „Preise & Listing“ → Karte „Artikelmerkmale (KI)“) – der CSV-Lister lässt die Merkmale immer von der KI füllen und füllt leere Pflichtmerkmale nach festen Regeln auf (siehe [B10](#b10-was-im-angebot-steht-aufbau-der-csv-datei)).
- „Auch mit Angebotsgebühr einstellen“ und „Nur ein Bild bei eBay einstellen“ (Reiter „eBay & Rahmenbedingungen“ → „Beim Einstellen“).
- „Bildabgleich gegen fremde Angebote“ (Reiter „Produkt-Filter“).
- „Mind. Sterne“, „Mind. Bewertungen“, „Mind. Lagerbestand“ und „Nur Verkauf durch Amazon“ (Reiter „Produkt-Filter“ → „Amazon-Filter“) – die prüft der CSV-Lister beim Listen nicht.
- Thread-Zahl, Erfolgsgrenze und Zeitschaltung des Browser-Listers. Der CSV-Lister hat dafür seine eigene Auswahl „gleichzeitig“ auf seiner Seite.

**Menge je Angebot:** Dafür gibt es in der Oberfläche keine Einstellung. Ohne einen früher gespeicherten Wert wird jedes Angebot mit **Menge 1** eingestellt. **Nicht sicher belegt:** ob bei dir noch ein Wert aus einer älteren Version gespeichert ist, der stattdessen gilt.

### B6. Aufbau der CSV-Lister-Seite

Links steht die Seitenleiste. Oben rechts daneben die Überschrift „CSV-Lister“ mit dem Abzeichen „neu · im Test“ und der Zeile „Angebote aus der Datenbank bauen und als Datei bei eBay hochladen“.

Die Seite ist bewusst schlicht: Sichtbar ist nur, was du zum Starten und Mitverfolgen brauchst. Technisches steckt in zugeklappten Bereichen.

#### 1. Statuskarte (oben)

Eine Zeile mit farbigem Punkt:

- „Wird geprüft …“ (beim Öffnen)
- grün „Bereit zum Listen“
- rot „Fehlt noch: Anmeldung, Rahmenbedingungen, Artikelstandort“ (nur die Punkte, die wirklich fehlen)
- rot „Noch nicht bereit“ (wenn etwas anderes fehlt, z. B. die eingebaute Muster-CSV)

Daneben:

- **„Details“** / **„Weniger“** – klappt die sieben Prüfpunkte auf und zu. Fehlt etwas, klappt die Liste von selbst auf.
- **„Einstellungen“** (rechts) – öffnet die Einstellungsseite (Reiter „Preise & Listing“; die Rahmenbedingungen stehen im Reiter „eBay & Rahmenbedingungen“).
- **„Neu prüfen“** – erscheint bei aufgeklappten Details; prüft alles erneut. Änderst du eine der geprüften Einstellungen oder meldest du dich an, prüft die Seite ohnehin von selbst neu.

**Die sieben Prüfpunkte** (grünes ✓, rotes ✕ oder gelbes !):

| Punkt | Grün | Rot / Gelb |
|---|---|---|
| „eBay-Abfragen (laufen über den Server)“ | „Anmeldung vorhanden – die eBay-Schlüssel liegen auf dem Server, nicht in der Extension“ | rot: „nicht angemeldet – ohne Anmeldung keine eBay-Abfragen (Dashboard → Anmelden)“ |
| „Rahmenbedingungen (Versand, Zahlung, Rücknahme)“ | zeigt deine drei Namen, getrennt mit „ · “ | rot: „fehlt: Versand, Zahlung, Rücknahme – ohne die drei Namen startet kein Lauf“ (nur die fehlenden) |
| „Artikelstandort“ | zeigt deinen Standort | rot: „fehlt – Ort oder Postleitzahl für die Spalte *Location“ |
| „Anmeldung (Produkt-Vergabe, Server)“ | „angemeldet als …“ | gelb: „nicht angemeldet – Produkt-Vergabe und Lister-Log sind aus“ |
| „Muster-CSV“ | z. B. „201 Spalten, davon 134 Merkmalspalten“ | rot, wenn die eingebaute Vorlage nicht lesbar ist |
| „Produkt-Filter (Einstellungen)“ | z. B. „nur FBA an · nur chinesische Verkäufer aus · GPSR aus (ändern: Einstellungen)“ | gelb, wenn „nur chinesische Verkäufer“ oder „GPSR“ an ist, mit dem Zusatz „– Produkte ohne passenden Verkäufer bzw. ohne GPSR-Angaben werden aussortiert und gelöscht“ |
| „Alter Browser-Lister“ | „läuft nicht“ oder „läuft gerade – geht gleichzeitig, jeder Lister bekommt andere Produkte“ | – (dieser Punkt ist immer grün) |

Gelbe Punkte sind nur Hinweise und **verhindern keinen Start**. Rote Punkte verhindern den Start. Steht etwas Rotes da, zeigt die Seite „Erst die offenen Punkte oben beheben.“ und beim Klick auf Start „Rote Punkte oben zuerst beheben.“

Die „Muster-CSV“ ist eine fest eingebaute Vorlage im eBay-Format. Du kannst und musst daran nichts ändern. Ist der Punkt rot, ist die Installation beschädigt – Extension neu installieren oder den Betreiber fragen.

**Was die Statuszeile nicht prüft:** OpenAI-Schlüssel, Domain, eBay-Anmeldung im Seller Hub, Server-Erreichbarkeit, freie Produkte, Tageskontingent (siehe [B4](#b4-voraussetzungen)).

#### 2. Startbereich

| Element | Bedeutung | Standard |
|---|---|---|
| „Produkte“ (Zahlenfeld) | wie viele Produkte aus der Produkt-Datenbank dieser Lauf nimmt | 5, mindestens 1; höchstens der Tagesrest |
| Kontingent-Anzeige rechts daneben | z. B. „Heute noch 300 von …“ (siehe [B8](#b8-tageskontingent)) | leer, wenn es keine Grenze gibt |
| „alle“ (Haken) | alle freien Produkte der Datenbank, aber höchstens der Tagesrest; graut das Feld „Produkte“ aus | aus |
| „gleichzeitig“ (Auswahl 1–10) | wie viele Produkte parallel bearbeitet werden (Threads); jeder Thread öffnet seinen eigenen Amazon-Tab im Hintergrund. Die Wahl wird gespeichert. | 1 |
| „Abbrechen“ (rot) | erscheint nur während eines Laufs; Hinweis beim Darüberfahren: „Lauf abbrechen – fertige Zeilen werden verworfen, die Produkte bleiben in der Datenbank“ | – |
| „Lauf starten“ | startet den Lauf | – |

**Threads („gleichzeitig“):** Mehr Threads machen den Lauf schneller, belasten aber Rechner und Internetleitung stärker. Bei langsamer Leitung kann der Bild-Upload zu lange dauern (Meldung „… bei „gleichzeitig“ eine kleinere Zahl wählen“). Läuft ein Thread auf einen technischen Fehler, halten **alle** an.

**„alle“ und andere Geräte:** Mit „alle“ nimmt der Lauf alle freien Produkte (höchstens den Tagesrest). Solange er läuft, bekommen deine anderen Geräte und der Browser-Lister diese Produkte nicht.

Während eines Laufs sind „Produkte“, „alle“, „gleichzeitig“, „Lauf starten“, „Ergebnisse bei eBay abholen“ und „Wartende vergessen“ gesperrt.

#### 3. Fortschritt

- **Balken.** Solange noch kein Produkt fertig ist, läuft er gestreift durch (damit die Seite nicht eingefroren wirkt). Grün = fertig, orange = abgebrochen.
- **Text links:** „Produkt … von …“, „Datei wird zu eBay hochgeladen …“, „Wird abgebrochen – das laufende Produkt wird noch fertig“, „Läuft in einem anderen Tab“, „Abgebrochen“ oder „Fertig“.
- **Wichtig:** Auch ein Lauf, der wegen eines technischen Fehlers von selbst angehalten hat, endet mit orangem Balken und „Abgebrochen“ – obwohl du nichts abgebrochen hast. Den Grund zeigt dann die rote Box (siehe unten). In diesem Fall wurden die fertigen Zeilen trotzdem hochgeladen (siehe [B16](#b16-abbrechen-anhalten-seite-geschlossen)).
- **Zahl rechts:** „fertig / gesamt · … %“.

#### 4. Ergebnis-Kapseln

Sobald das erste Produkt fertig ist:

- grün „… Zeilen“ – Produkte, für die eine fertige Zeile in der Datei entstanden ist
- orange „… übersprungen“ – aussortiert (siehe [B15](#b15-was-mit-jedem-produkt-passiert-übersicht))
- rot „… offen“ bzw. „… offen, … zurückgestellt“
- nach dem Upload grün „… gelistet“ und rot „… abgelehnt“
- orange „… mit eBay-Warnung“ – gelistet, aber eBay hat etwas geändert
- grau „… mit Hinweis“ – z. B. Vergabe noch nicht bestätigt, Gebühr unbekannt, Merkmal ohne Spalte weggelassen

Darunter stehen bis zu drei Warnungen/Hinweise im Klartext („ASIN: …“), bei mehr: „… und … weitere (siehe Produkte dieses Laufs)“.

**ASIN** ist die Amazon-Standard-Identifikationsnummer, die zehnstellige Kennung eines Produkts bei Amazon.

#### 5. Hinweiszeile und rote Fehlerbox

- Die **Hinweiszeile** (grau) zeigt das Ergebnis des letzten Klicks (Start, Abholen, Vergessen), z. B. „csv-lister-….csv hochgeladen: 12 gelistet · 1 abgelehnt.“ oder „Prüfe das Tageskontingent …“.
- Die **rote Box** zeigt, warum ein Lauf angehalten wurde oder unterbrochen war (siehe [B20](#b20-probleme-und-lösungen-zum-csv-lister)).

#### 6. Wartende Produkte

Nur sichtbar, wenn Produkte auf ein eBay-Ergebnis warten oder Vergaben noch nicht bestätigt sind:

- Text „… Produkt(e) warten auf ein eBay-Ergebnis“ und/oder „… Vergabe(n) noch nicht bestätigt“
- Knopf „Ergebnisse bei eBay abholen“ (nur, wenn Produkte auf ein eBay-Ergebnis warten)
- roter Knopf „Wartende vergessen“ (ebenfalls nur dann)

Siehe [B14](#b14-wartende-produkte-abholen-oder-vergessen).

#### 7. Zugeklappt: „Produkte dieses Laufs“

Erscheint, sobald ein Lauf Produkte hat. Oben eine Bilanzzeile, z. B. „Fertig: 20 / 20 bearbeitet · 17 Zeilen · 3 übersprungen · 2 gleichzeitig · Datei: csv-lister-….csv · gestartet …“. Am Anfang steht je nach Zustand „Läuft:“, „Upload läuft:“, „Wird abgebrochen:“, „Abgebrochen:“, „Fertig:“ oder „Läuft in einem anderen Tab:“. Gibt es offene Produkte, kommt „· … offen“ dazu, ggf. mit „(davon … zurückgestellt, gehen nach dem Lauf zurück in die Datenbank)“. Die Zahl bei „gleichzeitig“ steht nur da, wenn mehr als ein Thread lief.

Darunter eine Tabelle:

| Spalte | Inhalt |
|---|---|
| „#“ | laufende Nummer |
| „ASIN“ | Amazon-Kennung |
| „Schritt“ | woran gerade gearbeitet wird bzw. das Ende (siehe [B9](#b9-was-bei-einem-lauf-passiert)) |
| „Kategorie“ | eBay-Kategorienummer und -name |
| „Zustand“ | eBay-Zustandsnummer und -name, z. B. 1000 (Neu) oder 1500 (Neu: Sonstige) |
| „eBay“ | „in Arbeit“ (Zeile fertig, eBay-Ergebnis fehlt noch), „gelistet“ mit eBay-Artikelnummer, „abgelehnt“ oder „vergessen“ |
| „Titel / Grund“ | bei fertigen Zeilen der Titel und „… Merkmale“; sonst der Grund (z. B. warum übersprungen) und Hinweise |

Farbiger Rand links: grün = Zeile fertig, orange = übersprungen, rot = offen oder von eBay abgelehnt, blau = wird gerade bearbeitet.

#### 8. Zugeklappt ganz unten: „Technik“

Daneben steht „für die Fehlersuche: eBay-Zugang, Kategorie-Abfrage“. Im Alltag brauchst du diesen Bereich nicht.

- **„Letztes eBay-Ergebnis“** – „Noch keins.“ oder z. B. „eBay-Ergebnis (Upload …, Datum Uhrzeit): 12 gelistet · 1 abgelehnt …“. Nach dem Abholen steht statt „Upload …“ „… Datei(en) bei eBay abgeholt“. Ist ein Upload gescheitert, steht hier dessen Meldung.
- **„Verbindung zu eBay“** mit Knopf „Server und eBay-Zugang prüfen“ – prüft, ob der Server des Betreibers gerade Zugang zu eBay hat. Ausgabe vorher „Noch nicht geprüft.“, während der Prüfung „Server wird gefragt …“. Ist alles in Ordnung, endet die Zeile zum Kategoriebaum mit „– wie erwartet.“ und die Zeile zu den Bildadressen mit „– HTTPS, in Ordnung.“; ganz unten steht „Dauer: … ms“. Die Ausgabe enthält technische Angaben für den Betreiber – du musst sie nicht verstehen. Steht dort „ACHTUNG“ oder „KEIN HTTPS“, beginnt eine Zeile mit „Server hat keinen eBay-Zugang“ oder „Auf dem Server sind keine eBay-Schlüssel eingerichtet“, oder ist die Ausgabe rot: Kopiere den Text und schick ihn dem Betreiber – das kannst du nicht selbst beheben.
- **„Kategorie und Merkmale zu einem Titel“** – Feld „Produkttitel eingeben“ und Knopf „Abfragen“ (oder Enter). Ausgabe vorher „Noch nicht geprüft.“, dann „Kategorievorschlag wird geholt …“ und „Merkmale und Zustände werden geholt …“. Ergebnis: „Kategorie <Nummer>: <Kategoriepfad>“, „Merkmale: … (davon Pflicht: …)“ und „Zustände: …“ (z. B. „1000 = Neu | 1500 = Neu: Sonstige“; „(Pflicht)“, wenn die Kategorie eine Zustandsangabe verlangt). Darunter eine Tabelle mit „Merkmal“, „Art“ („Pflicht“/„empfohlen“/„optional“), „Eingabe“ („nur Auswahl“ oder „frei“, ggf. „, mehrere“, „, max. …“) und „Erlaubte Werte“ (die ersten 12, bei mehr mit „… (Anzahl)“). Ohne Titel: „Bitte einen Titel eingeben.“ Ohne Vorschlag: „eBay schlägt zu diesem Titel keine Kategorie vor – so ein Produkt würde übersprungen.“ Bei Problemen (z. B. nicht angemeldet) steht rot „Fehler: …“. Praktisch, um vorab zu sehen, wo ein Produkt landen würde. Diese Abfrage verbraucht kein Tageskontingent und nimmt kein Produkt aus der Datenbank.

Ein Protokoll ist auf der Seite in Version 46.0 nicht mehr zu sehen. Was in einem Lauf passiert ist, steht in „Produkte dieses Laufs“, in der Hinweiszeile, in der roten Box und unter „Letztes eBay-Ergebnis“.

### B7. Der CSV-Lister im Dashboard und in der Seitenleiste

Auch ohne die CSV-Lister-Seite zu öffnen, siehst du einiges (Einzelheiten in dashboard.md):

- **Dashboard → „Vorgänge“ → Karte „CSV-Lister“:** eine Marke mit dem Zustand („bereit“, „läuft · … von …“, „lädt zu eBay hoch“, „unterbrochen“, „fertig“ oder „abgebrochen“) und eine Zeile wie „Noch kein Lauf“, „Läuft seit …“, „Lauf von … unterbrochen – der Tab wurde geschlossen“ oder „Zuletzt … · … Zeilen, … übersprungen · … gelistet, … abgelehnt“. Die unterste Zeile der Karte sagt „CSV-Lister ist offen – Klick springt hin“ oder „Klick öffnet: CSV-Lister“. Ein Klick öffnet den CSV-Lister bzw. springt in seinen Tab. Die Karte zeigt nur den Stand dieses PCs (Chrome-Profils).
- **Glocke im Dashboard:** Hinweise wie „CSV-Lister-Lauf unterbrochen“, „CSV-Lister: Hochladen fehlgeschlagen“, „CSV-Lister angehalten“ oder „… Produkte warten auf das eBay-Ergebnis“ („Im CSV-Lister „Ergebnisse bei eBay abholen“.“). Diese Hinweise betreffen nur den PC, an dem du gerade sitzt.
- **Kennzahl „Heute gelistet“:** In der kleinen Zeile darunter steht „CSV-Lister …“ mit der Zahl der heute mit dem CSV-Lister gelisteten Angebote; von eBay abgelehnte Zeilen zählen bei „… fehlgeschlagen“ mit.
- **Kennzahl „Produkte in der Datenbank“:** zeigt, wie viele Produkte gerade „in Arbeit“ sind – auch die, die der CSV-Lister genommen hat.
- **Seitenleiste unten:** „Server verbunden“ / „Produkt-Vergabe aktiv“ heißt, der CSV-Lister kann Produkte nehmen. Bei „Server nicht erreicht“ steht darunter „Lister nehmen keine Produkte“ – dann startet kein Lauf.

### B8. Tageskontingent

Der Betreiber legt für dein Konto fest, **wie viele Produkte du pro Tag mit dem CSV-Lister bearbeiten darfst**. Die genaue Zahl siehst du neben dem Feld „Produkte“. Das Kontingent gilt für dein Konto, also für alle deine Geräte zusammen.

**Anzeigen neben dem Feld „Produkte“:**

- „Heute noch … von …“ – so viele Produkte darfst du heute noch bearbeiten.
- „Tageskontingent erreicht – ab Mitternacht wieder frei“ (orange) – heute geht nichts mehr; der Knopf „Lauf starten“ ist gesperrt.
- „Rückgabe von … Produkt(en) ausstehend – wird nachgeholt“ – ein früherer Lauf hat nicht verbrauchtes Kontingent noch nicht zurückgebucht; das passiert automatisch. Der Start bleibt möglich.
- „Heute noch 0 von … – der Rest ist für den laufenden Lauf gebucht“ – ein Lauf läuft gerade (hier oder in einem anderen Tab).
- **leer** – es gibt für dich keine Grenze, oder der Stand ist gerade nicht abrufbar (dann prüft der Start selbst).

**Regeln:**

1. Das Feld „Produkte“ wird automatisch auf den Tagesrest begrenzt. Tippst du eine größere Zahl ein, wird sie auf den Rest gesetzt.
2. „alle“ nimmt höchstens den Tagesrest.
3. Beim Start bucht der Lauf genau so viele Produkte, wie er aus der Datenbank bekommen hat (gibt es weniger freie Produkte als gewünscht, nur diese). **Ein laufender Lauf hält normalerweise nie wegen des Kontingents an.** Einzige Ausnahme: die CSV-Lister-Seite ist in zwei Tabs offen und die beiden kommen sich in die Quere – dann kann ein Lauf mit „Das Tageskontingent dieses Laufs wurde von einer anderen Lister-Seite zurückgegeben – Lauf angehalten, bitte erneut starten.“ oder „Tageskontingent dieses Laufs aufgebraucht (… gebucht) – Lauf angehalten.“ stehen bleiben. Deshalb immer nur **einen** CSV-Lister-Tab benutzen.
4. **Jedes Produkt, das der Lauf anfängt, zählt als verbraucht** – auch wenn es danach übersprungen, zurückgestellt oder beim Abbrechen verworfen wird.
5. Was der Lauf nicht mehr anfängt (z. B. nach „Abbrechen“ oder einem technischen Halt), wird am Ende automatisch zurückgebucht. Klappt das nicht sofort, holt die Seite es von selbst nach.
6. Nach Mitternacht wird das Kontingent wieder frei. Die Seite merkt das von selbst (beim Zurückkehren in den Tab oder spätestens nach 10 Minuten) – du musst sie nicht neu laden.

**Meldungen beim Start** (in der Hinweiszeile, meist mit „Nicht gestartet: “ davor):

- „Prüfe das Tageskontingent …“
- „Nicht gestartet: Tageskontingent erreicht – ab Mitternacht wieder frei.“
- „Nicht gestartet: Tageskontingent erreicht – Rückgabe von … ausstehend – wird nachgeholt. Bitte in ein paar Minuten erneut starten.“
- „Nicht gestartet: Tageskontingent erreicht (… Produkte heute) – ab Mitternacht wieder frei.“ bzw. „… – Rückgabe von … ausstehend, wird nachgeholt. Bitte in ein paar Minuten erneut starten.“ – dieselbe Lage, erst im Lauf-Start bzw. beim Buchen festgestellt (z. B. weil ein anderes Gerät kurz vorher gebucht hat); in Klammern steht deine Tagesmenge.
- „Nicht gestartet: Tageskontingent reicht nicht – heute noch … von … Produkten frei. Bitte erneut starten.“ – zwischen Prüfung und Buchung wurde von anderer Stelle gebucht (z. B. an einem zweiten Gerät). Einfach erneut starten; das Feld „Produkte“ passt sich an.
- „Nicht gestartet: Tageskontingent nicht abrufbar: …“ – z. B. weil der Server nicht erreichbar ist (dahinter „Claims-Server nicht erreichbar …“) oder deine Anmeldung abgelaufen ist („nicht angemeldet oder Sitzung abgelaufen – bitte im Dashboard neu anmelden“, „dieser Zugang ist abgeschaltet“).
- „Nicht gestartet: Tageskontingent nicht buchbar: … – Lauf nicht gestartet, bitte später erneut starten.“ – die Buchung kam wegen einer Verbindungsstörung nicht sicher an. Später erneut starten; eine eventuell doch gebuchte Menge bucht die Seite von selbst zurück.
- „Tageskontingent: die Buchung dieses Laufs wurde inzwischen von einer anderen Lister-Seite zurückgegeben (galt als unbeantwortet) – Lauf nicht gestartet, bitte erneut starten.“ – kommt vor, wenn die CSV-Lister-Seite in zwei Tabs offen ist. Einfach erneut starten (und nur einen Tab benutzen).
- Andere Meldungen der Form „Tageskontingent: … – Lauf nicht gestartet.“ (z. B. „Tageskontingent: Server meldet keine nutzbare Menge – Lauf nicht gestartet.“) – der Server hat die Buchung nicht angenommen. Später erneut starten; bleibt es, den Betreiber mit dem genauen Text fragen.

Schlägt der Start nach dem Nehmen der Produkte fehl (z. B. beim Buchen), gibt die Seite die genommenen Produkte sofort an die Datenbank zurück.

**Tipp:** Weil jedes angefangene Produkt zählt, lohnt sich „Abbrechen“ nicht, um Kontingent zu sparen – die bereits angefangenen Produkte sind verbraucht, und ihre fertigen Zeilen werden beim Abbrechen verworfen (siehe [B16](#b16-abbrechen-anhalten-seite-geschlossen)).

**Wie hoch ist mein Kontingent und kann es erhöht werden?** Das entscheidet der Betreiber. Die aktuelle Zahl steht hinter „von“ in der Anzeige.

### B9. Was bei einem Lauf passiert

#### Vor dem ersten Produkt

1. Die Seite prüft die Voraussetzungen und das Tageskontingent.
2. Unbestätigte Produktvergaben früherer Läufe werden nachgeholt.
3. Warten noch Produkte früherer Läufe auf ein eBay-Ergebnis, holt der Lauf zuerst die Ergebnisdateien aus dem Seller Hub ab (in einem Hintergrund-Tab). Klappt das nicht, läuft der Lauf trotzdem; die wartenden Produkte bleiben „in Arbeit“. Am Ende steht dann in der Hinweiszeile in Klammern „(Ergebnisdateien nicht abgeholt: …)“. Hat das Abholen etwas gebracht, steht dort „Vor dem Lauf: … Ergebnisdatei(en) abgeholt: …“.
4. Er prüft, ob die Rahmenbedingungen und der Artikelstandort eingetragen sind („Einstellungen fehlen: …“).
5. Er fragt beim Server nach, ob die Bilder über eine sichere Adresse (HTTPS) bereitgestellt werden können. Wenn nicht, startet er nicht („Der Claims-Server liefert Bildadressen ohne HTTPS …“ – das liegt am Server, nicht an dir).
6. Er holt Rückgaben an die Datenbank nach, die früher nicht geklappt haben.
7. Er **nimmt** die Produkte für den Lauf aus der Produkt-Datenbank – nur freie, mit der Markierung „in Arbeit“ für dieses Gerät (siehe [B3](#b3-die-gemeinsame-produkt-datenbank-und-in-arbeit)).
8. Er bucht das Kontingent für genau diese Menge. Was über den nutzbaren Rest hinausgeht, geht sofort an die Datenbank zurück.

#### Je Produkt (Spalte „Schritt“)

| Schritt in der Tabelle | Was passiert |
|---|---|
| „wartet“ | noch nicht dran |
| „Vergabe prüfen“ | Ist das Produkt noch dir zugeteilt? Die **Produktvergabe** verhindert, dass zwei Kunden dasselbe Produkt listen. Beim Import in die Produkt-Datenbank wurde es für dich reserviert; hier wird das noch einmal geprüft. Ist es inzwischen einem anderen Kunden zugeteilt, wird es übersprungen („bereits von einem anderen Nutzer vergeben“). |
| „Amazon“, „Amazon: Verkäufer prüfen (… s)“, „Amazon: KI-Titel (… s)“, „Amazon: GPSR-Angaben (… s)“, „Amazon: Produktdaten (… s)“, „Amazon: arbeitet (… s)“ | Die Amazon-Produktseite wird im Hintergrund geöffnet. Dort laufen dieselben Prüfungen wie beim Browser-Lister (Vorfilter, Blacklist usw.), es werden Titel, Bilder und Produktinfos gelesen, der KI-Titel erzeugt und der Verkaufspreis nach deinen Preis-Einstellungen berechnet. Die Sekunden zeigen, wie lange der Zwischenschritt schon dauert. |
| „Kategorie“ | eBay schlägt zum Titel eine Kategorie vor. |
| „Merkmale + Zustände“ | Welche Artikelmerkmale und Zustände erlaubt die Kategorie? Der Zustand wird gewählt. |
| „KI-Merkmale“ | Die KI füllt die Artikelmerkmale aus dem Produkttext (bis zu 5 Versuche). |
| „Bilder“ | Die Bilder werden von Amazon geladen und für eBay bereitgestellt (siehe [B12](#b12-bilder)). Dieser Schritt kommt bewusst zuletzt, wenn alles andere geklappt hat. |
| „CSV-Zeile“ | Die Beschreibung wird gebaut und die Zeile für die Datei zusammengesetzt. |
| „fertig“ | Zeile fertig. Das Produkt bleibt jetzt bis zum eBay-Ergebnis „in Arbeit“. |
| „wird aussortiert“ → „übersprungen“ | Das Produkt passt nicht; Grund in „Titel / Grund“. Es verlässt die Datenbank. |
| „zurückgestellt“ | Technisches Problem nur bei diesem Produkt; es geht nach dem Lauf zurück in die Datenbank, der Lauf geht weiter. |
| „Fehler“ | Technisches Problem, das alle Produkte treffen würde; der Lauf hält an. |
| „Server bremst – warte … s“ | Zu viele eBay-Abfragen pro Minute; der Lauf wartet so lange, wie der Server sagt (höchstens 2 Minuten je Wartezeit), und macht dann mit demselben Produkt weiter. Nach 20 Wartezeiten hintereinander hält der Lauf an. |
| „eBay-Rate-Limit – Pause …/3“ | eBay selbst bremst; der Lauf wartet je eine Minute, höchstens dreimal. |
| „abgebrochen“, „nicht bearbeitet“, „verworfen (Abbruch)“, „verworfen (Upload nicht gelungen)“, „Lauf unterbrochen (zurückgegeben)“ | siehe [B16](#b16-abbrechen-anhalten-seite-geschlossen) und [B13](#b13-upload-zu-ebay-und-das-ergebnis) |
| „nicht mehr dran“, „verworfen (anderes Gerät)“ | Das Produkt gehört nicht mehr zu diesem Lauf (anderes Gerät hat es oder es wurde gelöscht), siehe [B3](#b3-die-gemeinsame-produkt-datenbank-und-in-arbeit) |

Der Amazon-Schritt wird überwacht: Hängt ein Zwischenschritt zu lange (je nach Schritt 1,5 bis 4 Minuten ohne Fortschritt), wird das Produkt zurückgestellt („Amazon-Skript hängt seit … s im Schritt „…““). Zusätzlich gibt es zwei äußere Grenzen: 240 Sekunden, bis die Amazon-Seite geladen ist, und 300 Sekunden für die Antwort des Amazon-Schritts.

#### Nach dem letzten Produkt

1. Nicht verbrauchtes Kontingent wird zurückgebucht.
2. Amazon-Tabs des Laufs, die noch offen sind, werden geschlossen.
3. Alle nicht fertigen Produkte gehen zurück in die Produkt-Datenbank.
4. Alle fertigen Zeilen werden zu **einer** Datei zusammengefügt. Sie heißt `csv-lister-<Datum>-<Uhrzeit>.csv`, z. B. `csv-lister-2026-10-24-13-05-22.csv`. **Achtung:** Die Uhrzeit im Namen ist Weltzeit (UTC) – im Winter eine Stunde, im Sommer zwei Stunden früher als deine Uhr. Das ist wichtig, wenn du die Datei im Seller Hub suchst.
5. Die Datei wird automatisch im Seller Hub hochgeladen (siehe [B13](#b13-upload-zu-ebay-und-das-ergebnis)).
6. eBays Ergebnis wird je Produkt verbucht.

**Die Seite muss während des ganzen Laufs offen bleiben.** Der Lauf läuft in dieser Seite. Schließt du sie mitten im Lauf, fragt Chrome nach, ob du die Seite wirklich verlassen willst. Lass den Rechner auch nicht in den Ruhezustand gehen – solange die Seite angehalten ist, läuft nichts weiter, und bei langer Pause können Produkte an andere Geräte gehen (siehe [B3](#b3-die-gemeinsame-produkt-datenbank-und-in-arbeit)).

Es kann je Chrome-Profil immer nur **ein** Lauf gleichzeitig laufen. Ist die Seite in einem zweiten Tab offen, zeigt dieser „Läuft in einem anderen Tab“ und sperrt Start, Abholen und Vergessen. Auf **verschiedenen Geräten** dürfen dagegen gleichzeitig Läufe laufen – jedes Gerät bekommt andere Produkte.

### B10. Was im Angebot steht (Aufbau der CSV-Datei)

Die Datei folgt eBays Upload-Vorlage für eBay.de (Semikolon als Trennzeichen, UTF-8, eine Info-Zeile, eine Kopfzeile, dann eine Zeile je Produkt). Die eingebaute **Muster-CSV** gibt die Spalten vor. In eBays Vorlage sind Pflichtspalten mit einem Stern markiert (z. B. *Category, *Title, *ConditionID, *Description, *Format, *Duration, *StartPrice, *Quantity, *Location).

Das schreibt der CSV-Lister in jede Zeile:

| Inhalt | Woher | Hinweise |
|---|---|---|
| **Aktion** | immer „Add“ (neues Angebot anlegen) | Der CSV-Lister ändert keine bestehenden Angebote. |
| **Custom Label** | eine eigene Kennung von Cash Lister (endet auf „==“) | genau wie beim Browser-Lister; so erkennt der Tracker die Angebote später wieder und der CSV-Lister kann eBays Ergebnis zuordnen |
| **Kategorie** | eBays Kategorievorschlag zum Titel (der erste Vorschlag) | Kein Vorschlag → Produkt übersprungen |
| **Titel** | KI-Titel (wie beim Browser-Lister), in der Sprache der eingestellten Domain (bei „DE“ deutsch) | Die Funde des Konkurrenz-Scanners bearbeitet nur der Browser-Lister, der CSV-Lister nimmt nur Produkte aus der Produkt-Datenbank. Seltene Ausnahme: Hat der Browser-Lister in diesem Chrome-Profil dasselbe Produkt vor Kurzem aus den Funden des Konkurrenz-Scanners entnommen, steht der dort gemerkte Titel des eBay-Verkäufers drin, ohne KI. Gesperrte Wörter werden entfernt (siehe unten), dann wortweise auf höchstens **80 Zeichen** gekürzt. Ist danach nichts übrig: übersprungen („Titel nach Wortfilter leer“). |
| **Zustand** | nach deinen Preis-Einstellungen | siehe „Zustand“ unten |
| **Zustandsbeschreibung** | Text aus „Zustandsbeschreibung“ | nur bei „Neu: Sonstige“ |
| **Bilder** | bis zu 12 Bilder von Amazon | siehe [B12](#b12-bilder) |
| **Beschreibung** | deine Vorlage oder schlichte Beschreibung | siehe „Beschreibung“ unten |
| **Format** | Festpreis | keine Auktionen |
| **Laufzeit** | „Gültig bis auf Widerruf“ | – |
| **Preis** | Verkaufspreis nach deinen Preis-Einstellungen | Kein Preis → übersprungen („kein Verkaufspreis aus der Preisstaffelung“) |
| **Menge** | siehe [B5](#b5-einstellungen-die-der-csv-lister-benutzt) | ohne gespeicherten Wert 1 |
| **Artikelstandort** | dein Feld „Artikelstandort (Ort oder PLZ)“ | – |
| **Rahmenbedingungen** | deine drei Namen | Versand, Rücknahme, Zahlung |
| **MwSt.** | „Mehrwertsteuersatz“ | nur wenn „Mehrwertsteuer im Angebot angeben“ an ist |
| **GPSR** | Hersteller und EU-verantwortliche Person von der Amazon-Seite | nur wenn „GPSR-Angaben übernehmen“ an ist; steht bei Amazon E-Mail und Webadresse in einem Feld, werden sie getrennt |
| **Artikelmerkmale** | KI, ergänzt nach festen Regeln | siehe „Merkmale“ unten; Merkmale, für die die Vorlage keine Spalte hat, bekommen automatisch eine eigene Spalte |
| **Marke** | siehe „Marke“ unten | – |
| **EAN** | echte EAN von Amazon oder „Nicht zutreffend“ | siehe „EAN“ unten |

**Werbung (Promoted Listings)** wird in der Datei **nicht** gesetzt.

#### Zustand

eBay-Zustände: **1000 = „Neu“**, **1500 = „Neu: Sonstige“** (neu, aber z. B. Verpackung geöffnet). Die Wahl:

Ob ein Produkt „Neu: Sonstige“ werden **soll**, entscheiden deine Preis-Einstellungen (Reiter „Preise & Listing“ → Karte „Preise“): Ist „Variable Preise (nach Preisspanne)“ an und fällt der Amazon-Preis in eine Regel, zählt der Haken „Neu: Sonstige“ **dieser Regel**. Passt keine Regel (oder sind variable Preise aus), zählt „Als „Neu: Sonstige“ listen (Standard)“.

1. Soll das Produkt „Neu: Sonstige“ werden und erlaubt die Kategorie 1500 → **Neu: Sonstige**.
2. Soll es „Neu: Sonstige“ werden, erlaubt die Kategorie 1500 aber nicht und ist „NUR „Neu: Sonstige“ listen“ an → **übersprungen**: „„Neu: Sonstige“ in dieser Kategorie nicht verfügbar (nur-Neu-Sonstige aktiv)“.
3. Sonst → **Neu** (1000), wenn erlaubt.
4. Sonst → der erste Zustand, den die Kategorie erlaubt.
5. Erlaubt die Kategorie gar keinen Zustand → übersprungen: „Kategorie bietet keinen zulässigen Zustand“.

#### Merkmale

- Die KI bekommt Titel, Stichpunkte, Beschreibung und Produktangaben von Amazon und füllt die Merkmale der Kategorie.
- Bei Merkmalen, bei denen eBay **nur Werte aus einer Liste** annimmt, werden Werte außerhalb der Liste verworfen.
- Höchstens 30 Werte je Mehrfach-Merkmal, höchstens 65 Zeichen je Wert (oder die Grenze, die eBay für das Merkmal meldet). Einzelwert-Merkmale bekommen nur einen Wert.
- **Nie gefüllt** werden Merkmale zu Personalisierung, Garantie/Gewährleistung und Kundenbewertung (das sind keine Produkteigenschaften).
- Kennungen wie EAN, UPC, GTIN oder ISBN fragt der CSV-Lister **nicht** bei der KI an – eine erfundene Nummer könnte das Angebot an ein fremdes Produkt hängen.
- Gesperrte Wörter werden auch aus den Merkmalswerten entfernt.
- **Leere Pflichtmerkmale** werden so aufgefüllt:
  - Kennungen (EAN, UPC …) → „Nicht zutreffend“
  - nur Listenwerte erlaubt → ein neutraler Listenwert, falls es einen gibt (z. B. „Nicht zutreffend“, „Keine Angabe“, „Sonstige“, „Universal“, „Markenlos“); gibt es keinen → **übersprungen**
  - Zahl oder Datum verlangt → **übersprungen**
  - freier Text → „Details In Description“

  Übersprungen wird dann mit: „Pflichtmerkmal ohne passenden Wert (nur Auswahl/Zahl): …“.

#### Marke

- **„Markenlos listen“ an (Standard):** Marke = „Markenlos“. Ausnahme: Nimmt eBay in dieser Kategorie für die Marke nur Werte aus einer festen Liste an, wird ein neutraler Wert aus dieser Liste genommen (z. B. „Markenlos“ oder „Nicht zutreffend“, falls vorhanden); gibt es dort keinen, wird die echte Marke eingetragen, damit eBay die Zeile nicht ablehnt.
- **Aus:** Marke von der KI; sonst die Marke von der Amazon-Seite; sonst „Markenlos“.
- Hat die Kategorie gar kein Merkmal „Marke“, wird keine Marke eingetragen.

#### EAN

- Die **EAN** (Europäische Artikelnummer, der Strichcode) übernimmt der CSV-Lister nur, wenn auf der Amazon-Seite **genau eine** gültige Nummer steht (bei Amazon heißt die Zeile „Global Trade Identification Number“). Bei Markenware ist das häufig der Fall, bei No-Name-Ware selten.
- Sonst steht „Nicht zutreffend“ (eBays Wert für „Artikel hat keine Kennung“ auf ebay.de).
- Die EAN steht sowohl im Merkmal „EAN“ als auch in eBays eigenem EAN-Feld.
- **Folge einer echten EAN:** Passt sie zu einem Produkt im eBay-Katalog, kann eBay die Kategorie auf die des Katalogprodukts umstellen und Merkmale (auch die Marke) durch die Katalogwerte ersetzen. Das Angebot ist trotzdem online; du siehst es als „mit eBay-Warnung“.

#### Beschreibung

- **Eigene Vorlage** (Reiter „Beschreibungsvorlage“ → „Beschreibungsvorlage (HTML)“): wird mit den Platzhaltern gefüllt, die über dem Feld stehen. Bilder in der Beschreibung (über die Bild-Platzhalter) zeigen auf die Bildadressen bei Amazon.
- **Keine eigene Vorlage (Feld leer):** schlichte Beschreibung ohne Design: Titel fett, darunter Stichpunkte, Produktbeschreibung, weitere Angaben und Tabelle – leere Teile fallen weg.
- **Spielzeug-Hinweis:** Die KI wird gefragt, ob das Produkt ein Spielzeug ist. Im Zweifel – und immer, wenn die KI nicht klar „nein“ sagt – werden drei Warnzeilen angehängt: „Achtung: Nicht für Kinder unter 36 Monaten geeignet“, „Achtung: Benutzung unter unmittelbarer Aufsicht von Erwachsenen“ und „Achtung: Enthält Spielzeug. Beaufsichtigung durch Erwachsene empfohlen“. Steht in deiner eigenen Vorlage der Platzhalter `_SPIELZEUG_WARNUNG_`, kommen sie dorthin, sonst ans Ende.
- Gesperrte Wörter werden auch aus der Beschreibung entfernt (nur aus dem sichtbaren Text).

#### Gesperrte Wörter (Wortfilter)

Eine fest eingebaute Liste mit Werbe- und Risikobegriffen wird aus Titel, Merkmalen und Beschreibung entfernt – z. B. „Original“, „Premium“, „Garantie“, „CE“. Das ist **nicht** deine Blacklist aus den Einstellungen: Deine Blacklist („Meine Liste“) sortiert ganze Produkte aus, dieser Wortfilter entfernt nur einzelne Wörter.

### B11. Gebührenprüfung bei „NUR Neu: Sonstige“

eBay gewährt für den Zustand „Neu: Sonstige“ nur in einem Teil der Kategorien eine ermäßigte Verkaufsprovision. Ist „NUR „Neu: Sonstige“ listen“ an, prüft der CSV-Lister zusätzlich die **Hauptkategorie** des eBay-Vorschlags:

- **Hauptkategorie ohne Ermäßigung** → übersprungen: „keine ermäßigte eBay-Gebühr für „Neu: Sonstige“ – …“
- **Hauptkategorie mit Ermäßigung** → weiter wie normal.
- **Hauptkategorie unbekannt** → **nicht** übersprungen, nur ein Hinweis am Produkt: „Gebühr unbekannt: Hauptkategorie „…“ steht in keiner der Gebührentabellen“.

Die Prüfung läuft **nur**, wenn „NUR „Neu: Sonstige“ listen“ an ist – dann aber für jedes Produkt.

**Eingebaute Liste (Stand: eBays Gebührenseite für gewerbliche Verkäufer, Anfang Oktober 2026):**

- **Mit Ermäßigung:** Computer, Tablets & Netzwerk · Foto & Camcorder · Handys & Kommunikation · Haushaltsgeräte · TV, Video & Audio · Business & Industrie · Büro & Schreibwaren · Garten & Terrasse · Heimwerker · Musikinstrumente · Sport · Reisen · Verschiedenes · Baby · Bastel- & Künstlerbedarf · Feinschmecker · Haustierbedarf · Möbel & Wohnen
- **Ohne Ermäßigung:** Auto & Motorrad (Teile, Fahrzeuge) · Kleidung & Accessoires · Uhren & Schmuck · Münzen · Filme & Serien / Filme & DVDs · Musik · Tickets & Erlebnisse / Tickets · PC- & Videospiele · Bücher & Zeitschriften / Bücher · Modellbau · Trading Cards / Sammelkartenspiele · Antiquitäten & Kunst · Beauty & Gesundheit · Briefmarken · Sammeln & Seltenes · Spielzeug
- **Ausnahmen:** Unter „PC- & Videospiele“ gelten die Zweige „Konsolen“, „Zubehör“, „Speicherkarten“ und „Ersatzteile & Werkzeuge“ als ermäßigt.

**Nicht sicher belegt:** die aktuellen Prozentsätze. eBay ändert seine Gebühren; die verbindlichen Sätze stehen auf eBays Gebührenseite. Die Liste in der Extension kann veralten.

### B12. Bilder

- Es werden **bis zu 12** Bilder von der Amazon-Seite genommen (in Galerie-Reihenfolge, wenn möglich in hoher Auflösung).
- Die Bilder werden geladen und kurzzeitig so bereitgestellt, dass eBay sie über eine sichere Adresse (HTTPS) abholen kann. eBay übernimmt sie kurz nach dem Listen auf seine eigenen Server.
- **Ein Bild lässt sich nicht laden** (Netzfehler, Seite nicht gefunden) → das ganze Produkt wird übersprungen: „Bild-Upload auf den Server scheitert: Bild nicht ladbar (…)“. Lieber kein Angebot als eins mit Lücken in der Galerie.
- **Ein Bild ist ungeeignet** – kein JPEG/PNG/WebP, leer oder größer als 12 MB – oder wird abgelehnt → nur dieses Bild wird **weggelassen**, das Produkt bleibt.
- **Kein Bild übrig** → übersprungen: „… kein verwendbares Bild (…)“ bzw. „kein Bild vom Server angenommen (…)“.
- **Bilder bei Amazon fehlen ganz** → übersprungen: „Amazon: keine Bilder“.
- **Bild-Upload zu langsam** → der Lauf hält an: „Bild-Server: Bild-Upload dauerte länger als … s (… MB) – Upload zu langsam oder Server hängt; bei „gleichzeitig“ eine kleinere Zahl wählen – Lauf angehalten.“
- **Bild-Server nicht erreichbar oder Anmeldung dort abgelehnt** → der Lauf hält an: „Bild-Server: … – Lauf angehalten.“

**Nach dem Listen:** Die CSV-Lister-Seite sieht bei gelisteten Angeboten auf der öffentlichen eBay-Seite nach, ob eBay die Bilder schon übernommen hat, und räumt die bereitgestellten Kopien erst danach weg. Das läuft jede Minute, solange die CSV-Lister-Seite offen ist, und sonst beim nächsten Öffnen oder Start. Du musst dafür nichts tun; die Seite nach dem Upload zu schließen schadet den Angeboten nicht – das Aufräumen passiert dann eben später.

### B13. Upload zu eBay und das Ergebnis

#### Ablauf

1. Nach dem letzten Produkt öffnet sich **im Vordergrund** ein Tab mit der Upload-Seite deines Seller Hub (bei Domain „DE“: www.ebay.de/sh/reports/uploads).
2. Die Extension klickt dort „Vorlage hochladen“, wählt die Datei aus und wartet, bis eBay sie verarbeitet hat. Den Fortschritt siehst du im Tab-Titel, z. B. „⏳ Hochladen startet“, „🔍 Suche Knopf „Vorlage hochladen““, „📂 Öffne Dialog…“, „🔍 Warte auf das Dateifeld“, „⚙️ Bereite CSV vor…“, „📤 Setze CSV ein…“, „📤 Lade Datei hoch…“, „🔍 Warte auf neue Zeile“, „🔄 Warte auf Ergebnisse“ und am Ende „✅ Hochladen fertig!“ bzw. „❌ Hochladen fehlgeschlagen“. Den Knopf „Vorlage hochladen“ sucht sie höchstens 15 Sekunden lang.
3. Die CSV-Lister-Seite zeigt währenddessen „Upload läuft: …“ und „Datei wird zu eBay hochgeladen …“. **Abbrechen ist jetzt nicht mehr möglich** – die Datei ist dann womöglich schon bei eBay.
4. Ist eBay fertig, holt die Extension die Ergebnisdatei, verbucht sie und schließt den Tab.
5. Insgesamt wartet sie bis zu 25 Minuten.

**Schließe den Seller-Hub-Tab während des Uploads nicht.**

#### Was eBays Ergebnis bedeutet

| eBay meldet | Bedeutung | Was mit dem Produkt passiert |
|---|---|---|
| Erfolg | Angebot ist online | „gelistet“ mit eBay-Artikelnummer; Vergabe wird **bestätigt**; Produkt verlässt die Produkt-Datenbank |
| Warnung | Angebot ist online, eBay hat aber etwas geändert (z. B. Kategorie umgestellt oder Merkmale aus dem eBay-Katalog übernommen) | wie Erfolg, zusätzlich „mit eBay-Warnung“ und der Text „eBay-Warnung: …“ – prüfe das Angebot bei eBay |
| Fehlschlag | eBay hat die Zeile abgelehnt | „abgelehnt“; Grund in „Titel / Grund“ als „eBay: … [Code]“; Vergabe wird **freigegeben**; Produkt verlässt die Produkt-Datenbank; **kein zweiter Versuch** |

Willst du ein abgelehntes Produkt doch noch listen, musst du es neu in die Produkt-Datenbank importieren (das geht nur, wenn es dann noch frei ist).

#### Mögliche Ausgänge des Uploads

- **Alles gut:** „csv-lister-….csv hochgeladen: … gelistet · … abgelehnt.“ Ggf. mit Zusätzen wie „· davon … aus früheren Läufen“, „· … Zeile(n) gehören zu keinem wartenden Produkt (ignoriert)“, „· … Vergabe(n) noch nicht bestätigt (wird nachgeholt)“.
- **Upload angenommen, Ergebnis nicht lesbar:**

  > Upload angenommen (Auftrag …), aber die Ergebnisdatei war nicht lesbar … – die Produkte warten auf „Ergebnisse bei eBay abholen".

  → später „Ergebnisse bei eBay abholen“ klicken.
- **Upload sicher nicht angekommen:**

  > Upload nicht gelungen: … – die Produkte gehen zurück in die Datenbank und kommen beim nächsten Lauf wieder dran.

  Die fertigen Zeilen werden verworfen („verworfen (Upload nicht gelungen)“). Die Produkte sind danach wieder frei – auch für deine anderen Geräte. Häufige Gründe:
  - „Nicht bei eBay angemeldet – bitte in diesem Chrome-Profil im Seller Hub anmelden und den Lauf neu starten“
  - „Seller Hub nicht erreichbar – die Uploads-Seite wurde umgeleitet nach …“
  - „Keine eBay-Domain eingestellt (Einstellungen → Preise & Listing → „Domain“).“
  - „Seller-Hub-Seite in 60 s nicht geladen“
  - „Upload-Skript nicht erreichbar … – bist du im Seller Hub angemeldet?“ (diese Meldung kann auch hinter „Upload-Ergebnis unklar: …“ stehen, siehe unten)
  - „Zeitüberschreitung beim Warten auf: Knopf „Vorlage hochladen““ (oder „… Knopf „Datei auswählen““) – der Knopf wurde nicht gefunden (Seller Hub in einer anderen Sprache? Seite anders aufgebaut?)
- **Unklar, ob angekommen:**

  > Upload-Ergebnis unklar: …. Die Datei wurde möglicherweise schon an eBay übergeben (Auftrag …) – die Produkte warten auf die Ergebnisdatei: über „Ergebnisse bei eBay abholen" oder automatisch beim Start des nächsten Laufs.

  Die Produkte bleiben „in Arbeit“, damit nichts doppelt gelistet wird.
- **„… gebaut, aber nicht hochgeladen.“** – die Datei entstand, wurde aber nicht hochgeladen. Das kommt nur in einem sehr seltenen Sonderfall vor: wenn „Abbrechen“ genau in dem kurzen Moment geklickt wird, nachdem die Datei gebaut ist und bevor der Upload beginnt. Die Produkte stehen dann „in Arbeit“ und warten auf ein Ergebnis, das nie kommt. Ausweg: erst „Ergebnisse bei eBay abholen“ (zur Sicherheit), danach „Wartende vergessen“ – siehe [B14](#b14-wartende-produkte-abholen-oder-vergessen).
- **„Keine Zeile entstanden – siehe Gründe in der Tabelle.“** – alle Produkte wurden übersprungen oder blieben offen; es gab nichts hochzuladen.

### B14. Wartende Produkte: abholen oder vergessen

**„In Arbeit“ mit fertiger Zeile** heißt: Für das Produkt ist eine Zeile hochgeladen (oder vielleicht hochgeladen), aber eBays Ergebnis ist noch nicht verbucht. Solche Produkte bleiben **bis zu 7 Tage** „in Arbeit“ – für alle deine Geräte und beide Lister. So wird nichts doppelt gelistet. Danach gelten sie wieder als normale, freie Produkte der Datenbank.

**Wichtig:** Die Liste der wartenden Produkte und das Abholen gehören zu dem **Chrome-Profil, in dem der Lauf lief**. „Ergebnisse bei eBay abholen“ und „Wartende vergessen“ wirken nur dort. Auf einem anderen Gerät siehst du diese Produkte in der Produkt-Datenbank nur als „in Arbeit“.

#### „Ergebnisse bei eBay abholen“

1. Klicke auf „Ergebnisse bei eBay abholen“.
2. Die Seite zeigt „Hole Ergebnisdateien aus dem Seller Hub …“ und öffnet die Upload-Seite des Seller Hub in einem Hintergrund-Tab.
3. Sie sucht dort die Ergebnisdateien der CSV-Lister-Dateien (Dateiname enthält „csv-lister“) und verbucht sie.
4. Ergebnis in der Hinweiszeile, z. B.:
   - „… Ergebnisdatei(en) abgeholt: … gelistet · … abgelehnt …“
   - „Keine neue Ergebnisdatei bei eBay gefunden“
   - „· … Upload(s) rechnet eBay noch“ – später erneut versuchen
   - „· … Datei(en) nicht lesbar“
   - „· … Produkt(e) warten weiter (CSV noch nicht hochgeladen oder Datei umbenannt?)“
   - „Kein Produkt wartet auf ein eBay-Ergebnis.“
   - „Nicht abgeholt: …“ (z. B. nicht bei eBay angemeldet)

Das Abholen passiert auch **automatisch vor jedem Lauf**. Den Knopf brauchst du vor allem, wenn kein Lauf startet (z. B. Tageskontingent erreicht) oder wenn ein Upload unklar war. Umbenannte Dateien findet das Abholen nicht.

#### „Wartende vergessen“

Nur für Fälle, in denen die Datei **sicher nicht** bei eBay angekommen ist (z. B. nach einem Absturz vor dem Upload). Rückfrage:

> … Produkt(e) warten auf ein eBay-Ergebnis.
>
> Nur vergessen, wenn ihre CSV NICHT bei eBay hochgeladen wurde. Wurde sie doch hochgeladen, wird das Ergebnis nicht mehr verbucht und die Produkte werden ein zweites Mal gelistet.
>
> Die Produkte gehen zurück in die Datenbank und werden wieder bearbeitet – auf diesem oder einem anderen Gerät. Fortfahren?

Danach: „… wartende(s) Produkt(e) vergessen – sie werden wieder normal gelistet.“ In der Tabelle steht bei diesen Produkten „vergessen“. Klappt es nicht: „Nicht vergessen: …“.

**Achtung:** „Wartende vergessen“ gilt für **alle** wartenden Produkte dieses Chrome-Profils, auch die aus anderen Läufen. Darum immer zuerst „Ergebnisse bei eBay abholen“ und nur vergessen, was danach noch wartet und sicher nicht hochgeladen wurde. Im Zweifel im Seller Hub auf der Upload-Seite nachsehen, ob dort eine Datei „csv-lister-…“ steht.

#### „… Vergabe(n) noch nicht bestätigt“

Nach erfolgreichem Listen wird die Produktvergabe bestätigt. Ist der Server in dem Moment kurz nicht erreichbar, merkt sich die Seite das und holt die Bestätigung beim nächsten Öffnen der Seite oder beim nächsten Start automatisch nach. Solange sie fehlt, ist dein Anspruch auf das Produkt nicht endgültig gesichert. Öffne die CSV-Lister-Seite also ab und zu, wenn diese Zeile erscheint. Am Produkt steht dann der Hinweis „Vergabe noch nicht bestätigt – wird automatisch nachgeholt“.

### B15. Was mit jedem Produkt passiert (Übersicht)

| Ergebnis | Bleibt in der Produkt-Datenbank? | Produktvergabe | Wann |
|---|---|---|---|
| **gelistet** (auch mit eBay-Warnung) | nein | bestätigt | eBay hat das Angebot angelegt |
| **abgelehnt** | nein | freigegeben | eBay hat die Zeile abgelehnt |
| **übersprungen** | **nein – wird gelöscht** | freigegeben (außer bei „bereits von einem anderen Nutzer vergeben“) | das Produkt passt nicht (siehe Liste unten) |
| **zurückgestellt** | ja – geht nach dem Lauf zurück, wieder frei für alle Geräte | bleibt | technisches Problem nur bei diesem Produkt |
| **offen** nach technischem Halt („Fehler“, „abgebrochen“ mit Grund „Lauf angehalten (Fehler in einem anderen Thread)“) | ja – zurück, wieder frei | bleibt | der Lauf wurde angehalten |
| **nicht bearbeitet** | ja – zurück, wieder frei | bleibt | der Lauf kam nicht mehr dazu |
| **verworfen (Abbruch)** / **abgebrochen** | ja – zurück, wieder frei | bleibt | du hast „Abbrechen“ geklickt |
| **verworfen (Upload nicht gelungen)** | ja – zurück, wieder frei | bleibt | Datei sicher nicht bei eBay |
| **Lauf unterbrochen (zurückgegeben)** | ja – zurück, wieder frei | bleibt | Seite/Browser war zu oder abgestürzt |
| **in Arbeit** (Zeile fertig) | ja, aber für alle Geräte gesperrt (bis zu 7 Tage) | bleibt | Datei hochgeladen, Ergebnis fehlt noch |
| **nicht mehr dran** / **verworfen (anderes Gerät)** | gehört jetzt einem anderen Gerät oder wurde gelöscht | – | siehe [B3](#b3-die-gemeinsame-produkt-datenbank-und-in-arbeit) |

**Wichtig:** Übersprungene Produkte werden **sofort aus der Produkt-Datenbank gelöscht** – es gibt keinen zweiten Versuch. Der Grund steht in der Tabelle „Produkte dieses Laufs“.

**Gründe fürs Überspringen** (Text in „Titel / Grund“):

- „bereits von einem anderen Nutzer vergeben“
- „Amazon: …“ mit dem Grund der Amazon-Prüfung, z. B.
  - „Amazon: Produkt ist nicht auf Lager“ (auch, wenn die Lieferzeit länger ist als „Max. verlängerte Lieferzeit“)
  - „Amazon: Nicht von Amazon versendet (Versand: …)“ (bei „Nur FBA“)
  - „Amazon: Kein chinesischer Verkäufer“ (bei „Nur chinesische Verkäufer“)
  - „Amazon: Keine GPSR-Angaben gefunden“ (bei „GPSR-Angaben übernehmen“)
  - „Amazon: Produkt enthält ein Wort aus der Blacklist: …“
  - „Amazon: Produkt ist gebraucht“
  - „Amazon: Produkt hat keinen kostenlosen Versand“
  - „Amazon: Produkt wird international versendet“
  - „Amazon: Produkt hat eine Mindestbestellmenge“
  - „Amazon: Amazon-Preis zu hoch (Filter „Preis bis“)“ / „Amazon: Amazon-Preis zu niedrig (Filter „Preis ab“)“
  - „Amazon: Produktseite existiert nicht“
  - „Amazon: ASIN und Adresse (URL) passen nicht zusammen“
  - „Amazon: Produkt ist schon gelistet (Duplikat)“ (du hast das Produkt in diesem Chrome-Profil schon einmal mit dem Browser-Lister erfolgreich gelistet)
- „Amazon: kein Angebot/Versender auf der Seite (ausverkauft?)“
- „Amazon: kein Titel“, „Amazon: keine Bilder“
- „kein Verkaufspreis aus der Preisstaffelung“
- „Titel nach Wortfilter leer“
- „kein Kategorievorschlag von eBay“
- „keine ermäßigte eBay-Gebühr für „Neu: Sonstige“ – …“
- „„Neu: Sonstige“ in dieser Kategorie nicht verfügbar (nur-Neu-Sonstige aktiv)“
- „Kategorie bietet keinen zulässigen Zustand“
- „KI-Schnittstelle antwortet nicht: …“ (die KI lieferte auch nach 5 Versuchen nichts Verwertbares)
- „Pflichtmerkmal ohne passenden Wert (nur Auswahl/Zahl): …“
- „Pflichtmerkmal ohne Spalte in der Muster-CSV: …“
- „Bild-Upload auf den Server scheitert: …“
- „eBay lehnt die Anfrage ab: … (auch schon in einem früheren Lauf)“ (siehe unten)

**Gründe fürs Zurückstellen** (Produkt geht nach dem Lauf zurück in die Datenbank, der Lauf geht weiter):

- „Amazon-Seite in 240 s nicht geladen“
- „Amazon-Skript hat in 300 s nicht geantwortet“
- „Amazon-Skript hängt seit … s im Schritt „…““
- „Amazon-Tab wurde geschlossen“ – schließe die Hintergrund-Tabs des Laufs nicht von Hand
- „Amazon-Skript ohne Ergebnis“, „Amazon-Skript ohne Produktdaten“
- „Amazon-Skript: …“ bei gescheitertem KI-Titel (z. B. „Amazon-Skript: KI-Titel ist leer“ oder „Amazon-Skript: Titel-Erstellung fehlgeschlagen“)
- „Chrome lässt gerade keinen Tab öffnen: …“
- erste eBay-Ablehnung eines Produkts (siehe unten)

#### Wenn eBay die Abfrage zu einem Produkt ablehnt

Manchmal lehnt eBay schon die Kategorie-/Merkmal-Abfrage zu einem Produkt ab („eBay lehnt die Anfrage ab: …“). Meist liegt das am Produkt, manchmal an einer Störung. Deshalb:

1. **Erste Ablehnung:** Das Produkt wird nur **zurückgestellt** und bleibt in der Datenbank. Text: „… – zurückgestellt; lehnt eBay es in einem späteren Lauf (frühestens 10 Minuten danach) wieder ab, wird es aussortiert“.
2. **Erneute Ablehnung in einem späteren Lauf, mindestens 10 Minuten nach der ersten:** endgültig **übersprungen** (aus der Datenbank gelöscht) mit „… (auch schon in einem früheren Lauf)“.
3. **Erneute Ablehnung weniger als 10 Minuten nach der ersten:** wieder nur zurückgestellt (Text: „… – zurückgestellt: erste Ablehnung vor weniger als 10 Minuten …“).
4. **Im selben Lauf** wird wegen einer Ablehnung nie gelöscht.
5. **5 erste Ablehnungen hintereinander** (ohne einen Erfolg dazwischen): Der Lauf hält an – dann ist vermutlich bei eBay oder beim Server etwas gestört. Meldung: „eBay hat die Abfragen zu 5 Produkten hintereinander abgelehnt (zuletzt: …) – vermutlich eine Störung bei eBay oder auf dem Server, Lauf angehalten. Erstmals abgelehnte Produkte bleiben in der Datenbank – bitte melden.“
6. Beantwortet eBay die Abfrage zu einem früher abgelehnten Produkt später doch, ist die frühere Ablehnung vergessen.
7. Eine gemerkte erste Ablehnung verfällt nach 7 Tagen.

Die gemerkten Ablehnungen gelten je Chrome-Profil.

### B16. Abbrechen, Anhalten, Seite geschlossen

#### Du klickst „Abbrechen“

1. Es steht „Abbruch angefordert – das laufende Produkt wird noch beendet.“
2. Laufende Wartezeiten werden sofort beendet; kein neues Produkt wird angefangen. Ein gerade bearbeitetes Produkt wird in der Regel an der nächsten Wartestelle unterbrochen und steht dann mit „abgebrochen“ und dem Grund „Lauf abgebrochen“ in der Tabelle.
3. **Alle fertigen Zeilen dieses Laufs werden verworfen – es wird nichts hochgeladen.** Die Produkte gehen zurück in die Datenbank (wieder frei, auch für deine anderen Geräte) und kommen beim nächsten Lauf wieder dran. Meldung: „Abgebrochen – … fertige Zeile(n) verworfen, die Produkte gehen zurück in die Datenbank.“
4. Bereits angefangene Produkte zählen für das Tageskontingent; der Rest wird zurückgebucht.
5. Während des Uploads ist „Abbrechen“ gesperrt.

#### Der Lauf hält von selbst an (technischer Fehler)

Bei Fehlern, die jedes weitere Produkt genauso treffen würden (z. B. Amazon-Captcha, Anmeldung weg, KI-Guthaben leer, Server nicht erreichbar), hält der Lauf an:

- Die rote Box zeigt den Grund.
- **Fertige Zeilen werden trotzdem hochgeladen.**
- Angefangene, nicht fertige und noch nicht angefangene Produkte gehen zurück in die Datenbank.
- Behebe die Ursache und starte neu.

#### Seite oder Browser während des Laufs geschlossen / abgestürzt

Beim nächsten Öffnen der CSV-Lister-Seite:

1. Es steht ggf. „Prüfe, ob der letzte Lauf noch in einem anderen Tab läuft … (bis 25 s)“. Die Seite wartet kurz, weil ein Lauf nach dem Ruhezustand oft noch lebt.
2. Ist der Lauf wirklich tot, räumt die Seite auf: offene Produkte gehen zurück in die Datenbank, verwaiste Amazon-Tabs werden geschlossen, nicht verbrauchtes Kontingent wird zurückgebucht.
3. In der roten Box steht z. B.:

   > Lauf wurde unterbrochen (Seite oder Browser geschlossen) – … offene(s) Produkt(e) an die Datenbank zurückgegeben – … fertige Zeile(n) gerettet, siehe „Letzte CSV herunterladen"

   **Achtung:** Einen Knopf „Letzte CSV herunterladen“ gibt es auf der Seite **nicht** – der Hinweis in der Meldung führt ins Leere. Die „geretteten“ Zeilen wurden **nicht** zu eBay hochgeladen; ihre Produkte stehen aber als „in Arbeit“ und würden bis zu 7 Tage für alle deine Geräte gesperrt bleiben. Was du tun kannst:
   1. Klicke „Ergebnisse bei eBay abholen“ (verbucht alles, was wirklich hochgeladen wurde).
   2. Warten danach noch Produkte und bist du sicher, dass seit dem Absturz keine Datei hochgeladen wurde: „Wartende vergessen“. Die Produkte gehen dann zurück in die Datenbank und kommen beim nächsten Lauf wieder dran.
4. Wurde **während des Uploads** unterbrochen, steht dort: „Lauf wurde während des Uploads unterbrochen – falls eBay die Datei angenommen hat, bitte die Ergebnisdatei einlesen.“ Ein Einlesen von Hand gibt es auf der Seite nicht; nutze „Ergebnisse bei eBay abholen“.

**Wenn du die Seite nach einem Absturz nicht wieder öffnest:** Die kurz gehaltenen Produkte werden nach etwa einer Stunde von selbst wieder frei. Produkte mit fertiger Zeile bleiben bis zu 7 Tage „in Arbeit“ – öffne die CSV-Lister-Seite auf **dem Gerät, auf dem der Lauf lief**, um aufzuräumen.

### B17. Meldungen an den Betreiber

Wenn du angemeldet bist, meldet der CSV-Lister **Probleme** zusätzlich an den Betreiber: übersprungene und zurückgestellte Produkte (mit Grund), eBay-Ablehnungen, eBay-Warnungen, Pausen der Seite, Upload-Fehler, unterbrochene Läufe und Läufe, die mit einem Fehler endeten. Erfolgreiche Listungen werden nicht gemeldet. Damit kann der Betreiber Fehler nachvollziehen. Klappt das Melden nicht, bremst das den Lauf nicht.

Für eine Frage an den Betreiber hilft es, wenn du ihm die ASIN, den genauen Text aus „Titel / Grund“ bzw. aus der roten Box und die Uhrzeit des Laufs schickst (am besten als Screenshot).

### B18. Schritt für Schritt: dein erster Lauf

1. **Version prüfen:** Unten in der Seitenleiste muss „Version 46.0“ (oder höher) stehen.
2. **Anmelden:** Im Dashboard mit deinem Zugang anmelden. Unten in der Seitenleiste sollte „Server verbunden“ stehen.
3. **Einstellungen öffnen** (Seitenleiste → „System“ → „Einstellungen“):
   1. Reiter „Preise & Listing“: Karte „Preise“ einstellen (Aufschläge, ggf. „Neu: Sonstige“); in der Karte „Listing“ bei „Domain“ „DE“ wählen.
   2. Reiter „eBay & Rahmenbedingungen“: in der Karte „Rahmenbedingungen“ die Namen deiner drei Rahmenbedingungen eintragen („Versand“, „Zahlung“, „Rücknahme“) – genau wie im Seller Hub – und den „Artikelstandort (Ort oder PLZ)“. Bei Bedarf „Mehrwertsteuer im Angebot angeben“ und die „Zustandsbeschreibung“ prüfen.
   3. Reiter „KI“: deinen „OpenAI-API-Schlüssel (für die Titel-Generierung)“ eintragen (falls noch nicht geschehen).
   4. Reiter „Produkt-Filter“: Filter, „Markenlos listen“, „Preis ab“/„Preis bis“ und deine Blacklist prüfen.
   5. Optional Reiter „Beschreibungsvorlage“: eigene Vorlage oder leer lassen.
4. **Bei eBay anmelden:** im selben Chrome-Profil den eBay Seller Hub öffnen und anmelden.
5. **Produkte importieren:** Produkte in die Produkt-Datenbank bringen (siehe produkte-finden-und-datenbank.md). Prüfe dort, dass Produkte frei sind (nicht alle „in Arbeit“).
6. **CSV-Lister öffnen:** Seitenleiste → „Arbeiten“ → „CSV-Lister“ (oder Dashboard → „Vorgänge“ → „CSV-Lister“).
7. **Status prüfen:** Oben muss grün „Bereit zum Listen“ stehen. Sonst „Details“ öffnen und die roten Punkte beheben.
8. **Erster Lauf mit 1 Produkt:** „Produkte“ auf 1 stellen (voreingestellt ist 5), „gleichzeitig“ auf 1. Grund: Stimmt ein Name der Rahmenbedingungen nicht genau, lehnt eBay die Zeilen ab, und abgelehnte Produkte sind danach aus der Produkt-Datenbank raus. Mit 1 Produkt verlierst du dabei höchstens eines.
9. **„Lauf starten“ klicken.** Die Seite offen lassen; Amazon-Tabs öffnen und schließen sich im Hintergrund.
10. **Upload:** Am Ende öffnet sich der Seller-Hub-Tab. Nicht schließen, warten.
11. **Ergebnis prüfen:** Kapseln „gelistet“/„abgelehnt“ ansehen, „Produkte dieses Laufs“ aufklappen, bei „abgelehnt“ den Grund lesen, bei „mit eBay-Warnung“ das Angebot bei eBay ansehen.
12. Ist das eine Produkt „gelistet“, kannst du die Zahl der Produkte und „gleichzeitig“ schrittweise erhöhen. Ist es „abgelehnt“, zuerst den Grund lesen und die Namen der Rahmenbedingungen mit dem Seller Hub vergleichen.

### B19. Häufige Fragen zum CSV-Lister

**Kann ich den CSV-Lister benutzen?**
Ja. Seit Version 46.0 steht er allen Kunden zur Verfügung (Seitenleiste → „Arbeiten“ → „CSV-Lister“). Einen Zugangscode brauchst du nicht mehr. Siehe [B2](#b2-wer-den-csv-lister-sieht-und-wie-du-ihn-öffnest), wenn er bei dir fehlt.

**Warum steht da noch „neu · im Test“?**
So ist die Seite beschriftet. Was das für dich bedeutet (z. B. ob sich Abläufe noch ändern), entscheidet der Betreiber – frag ihn im Zweifel.

**Muss ich selbst eine CSV-Datei erstellen?**
Nein. Der CSV-Lister baut die Datei aus deiner Produkt-Datenbank und lädt sie selbst hoch.

**Kann ich eine eigene CSV-Datei hochladen lassen?**
Nein. Die Seite hat dafür kein Feld; sie verarbeitet nur Produkte aus der Produkt-Datenbank.

**Kann ich die Datei vor dem Hochladen ansehen oder herunterladen?**
Auf der Seite gibt es dafür keinen Knopf. Den Inhalt jeder Zeile beschreibt [B10](#b10-was-im-angebot-steht-aufbau-der-csv-datei).

**Was ist der Unterschied zum Browser-Lister?**
Der Browser-Lister füllt für jedes Produkt das eBay-Formular aus; der CSV-Lister lädt alle Produkte eines Laufs als eine Datei hoch und wertet eBays Ergebnis je Produkt aus. Beide nutzen dieselbe Produkt-Datenbank und dieselben Amazon-Prüfungen.

**Kann ich Browser-Lister und CSV-Lister gleichzeitig laufen lassen?**
Ja. Seit Version 46.0 bekommt jeder Lister andere Produkte aus der Datenbank (Markierung „in Arbeit“). Der Prüfpunkt „Alter Browser-Lister“ zeigt dann „läuft gerade – geht gleichzeitig, jeder Lister bekommt andere Produkte“.

**Kann ich den CSV-Lister auf zwei Rechnern gleichzeitig laufen lassen?**
Ja, mit demselben Konto. Jedes Gerät bekommt andere Produkte. Das Tageskontingent gilt aber für dein Konto insgesamt. Auf **einem** Rechner (Chrome-Profil) läuft dagegen immer nur ein Lauf, und du solltest nur einen CSV-Lister-Tab offen haben.

**Was heißt „in Arbeit“ in der Produkt-Datenbank?**
Ein Lister (auf diesem oder einem anderen Gerät) hat das Produkt gerade genommen. Beim CSV-Lister steht dort z. B. „CSV-Lister (dieses Gerät) bis 14:32“. Siehe [B3](#b3-die-gemeinsame-produkt-datenbank-und-in-arbeit).

**Warum startet der CSV-Lister nicht, wenn der Server weg ist? Der Browser-Lister wartet doch.**
Der CSV-Lister nimmt alle Produkte eines Laufs beim Start vom Server. Ohne Server bekommt er keine – deshalb startet er gar nicht erst. Starte später neu.

**Was passiert mit meinen Produkten, wenn ich abbreche?**
Sie gehen zurück in die Datenbank und sind sofort wieder frei – für dieses und deine anderen Geräte. Die fertigen Zeilen dieses Laufs werden verworfen.

**Wie viele Produkte kann ich am Tag listen?**
So viele, wie dein Tageskontingent erlaubt – siehe Anzeige neben „Produkte“. Die Zahl legt der Betreiber fest.

**Zählen übersprungene Produkte zum Kontingent?**
Ja. Jedes Produkt, das der Lauf anfängt, zählt.

**Warum wurde mein Produkt gelöscht?**
Übersprungene und von eBay abgelehnte Produkte verlassen die Produkt-Datenbank sofort. Den Grund findest du in „Produkte dieses Laufs“ in der Spalte „Titel / Grund“.

**Kann ich ein gelöschtes Produkt zurückholen?**
Nur durch erneutes Importieren in die Produkt-Datenbank – sofern es dann noch frei ist.

**Was bedeutet „zurückgestellt“?**
Ein technisches Problem nur bei diesem Produkt. Es geht nach dem Lauf zurück in die Datenbank und kommt bei einem der nächsten Läufe (auf irgendeinem deiner Geräte) wieder dran.

**Was heißt „mit eBay-Warnung“?**
Das Angebot ist online, aber eBay hat etwas geändert – meist die Kategorie oder Merkmale aus dem eBay-Katalog (oft ausgelöst durch eine echte EAN). Sieh dir das Angebot bei eBay an.

**Warum steht als Marke „Markenlos“?**
Weil „Markenlos listen“ standardmäßig an ist. Du kannst es in den Einstellungen im Reiter „Produkt-Filter“ (Karte „Beim Listen“) ausschalten.

**Setzt der CSV-Lister Werbung (Promoted Listings)?**
Nein. Die „Anzeigengebühr (%)“ gilt nur für den Browser-Lister.

**Welche Menge bekommt jedes Angebot?**
Ohne früher gespeicherten Wert 1. Eine Einstellung dafür gibt es nicht.

**Kann ich Auktionen listen?**
Nein. Der CSV-Lister listet nur zum Festpreis mit Laufzeit „Gültig bis auf Widerruf“.

**Funktioniert der CSV-Lister für ebay.com, ebay.co.uk usw.?**
Er ist auf eBay.de ausgelegt (Datei für Deutschland/Euro, deutscher Kategoriebaum). Mit einer anderen „Domain“ würde der Upload an den Seller Hub dieser eBay-Seite gehen und der KI-Titel in deren Sprache entstehen – die Datei bliebe aber für Deutschland angelegt. **Nicht sicher belegt:** was eBay dann daraus macht – nicht ausprobieren, sondern den Betreiber fragen.

**Werden gelistete Produkte vom Tracker erkannt?**
Das Custom Label enthält dieselbe Kennung wie beim Browser-Lister (endet auf „==“); darüber findet der Tracker zum Angebot das Amazon-Produkt.

**Kann ich die Seite nach dem Upload schließen?**
Ja. Nach dem Upload ist der Lauf fertig. Das Wegräumen der Bilderkopien passiert, solange die Seite offen ist, sonst beim nächsten Öffnen.

**Was passiert, wenn ich den Rechner während des Laufs zuklappe?**
Solange die Seite angehalten ist, läuft nichts weiter. Danach läuft der Lauf meist einfach weiter. War die Pause lang, können einzelne Produkte inzwischen an ein anderes Gerät gegangen sein („nicht mehr dran“). Ist der Lauf beim Zurückkommen tot, räumt die Seite beim nächsten Öffnen auf (siehe [B16](#b16-abbrechen-anhalten-seite-geschlossen)).

**Wie viele Produkte gleichzeitig („gleichzeitig“) soll ich nehmen?**
Fang mit 1 an. Läuft alles, erhöhe schrittweise. Bei Meldungen über langsamen Bild-Upload oder vielen „zurückgestellt“ wieder verringern.

**Warum dauert der Amazon-Schritt so lange?**
Dort laufen Prüfungen, der KI-Titel und ggf. das Holen der GPSR-Angaben. In der Spalte „Schritt“ siehst du, woran gerade gearbeitet wird und seit wie vielen Sekunden.

**Gehen meine CSV-Lister-Einstellungen bei einem neuen Rechner verloren?**
Die Namen der Rahmenbedingungen, der Artikelstandort und die Zahl bei „gleichzeitig“ gehören zu den Einstellungen, die mit „Einstellungen exportieren“ und mit der Sicherung auf dem Server mitgehen (Reiter „Sicherung“). Dein **OpenAI-Schlüssel** geht nur mit der Export-Datei mit, **nicht** über die Sicherung auf dem Server – auf einem neuen Rechner musst du ihn also neu eintragen, wenn du nur „Einstellungen vom Server holen“ benutzt. Die **Produkt-Datenbank** liegt auf dem Server und ist auf jedem Gerät mit deiner Anmeldung dieselbe. Nicht mit umziehen: die Liste der wartenden Produkte, gemerkte eBay-Ablehnungen und der Stand des letzten Laufs – die gehören zum jeweiligen Chrome-Profil.

**Oben steht „Bereit zum Listen“, aber alle Produkte werden „zurückgestellt“ – warum?**
Die Statuszeile prüft nicht alles. Steht bei den Produkten „Amazon-Skript: KI-Titel ist leer“ oder „Amazon-Skript: Titel-Erstellung fehlgeschlagen“, konnte die KI keinen Titel erzeugen – meist fehlt der OpenAI-Schlüssel, er ist ungültig oder das OpenAI-Guthaben ist leer. Steht dort „Amazon-Seite in 240 s nicht geladen“ oder „Amazon-Skript hängt …“, liegt es eher an Internetverbindung oder zu vielen gleichzeitigen Produkten. Jedes zurückgestellte Produkt verbraucht trotzdem Tageskontingent – erst die Ursache beheben, dann neu starten.

**Mein Abo ist gesperrt – was ist mit dem CSV-Lister?**
Dann ist der Eintrag in der Seitenleiste ausgegraut, und ein laufender Lauf hält an (z. B. mit „Anmeldung weg (Sitzung abgelaufen oder Zugang abgeschaltet) – Lauf angehalten.“, „Dieser Zugang ist abgeschaltet.“ oder „Nicht angemeldet oder Sitzung abgelaufen – bitte im Dashboard neu anmelden.“). Unten in der Seitenleiste steht dann „Abo gesperrt“ – oder, falls der CSV-Lister die Sperre als Erster bemerkt hat, nur „Nicht angemeldet“. Meldest du dich im Dashboard neu an, zeigt die Anmeldung, ob das Abo gesperrt ist. Wie du das Abo wieder freibekommst, steht in konto-und-installation.md.

### B20. Probleme und Lösungen zum CSV-Lister

Die meisten Meldungen beim Start stehen in der Hinweiszeile mit „Nicht gestartet: “ davor.

#### Start klappt nicht

| Meldung | Lösung |
|---|---|
| „Rote Punkte oben zuerst beheben.“ / „Erst die offenen Punkte oben beheben.“ | „Details“ öffnen, rote Punkte beheben (Anmeldung, Rahmenbedingungen, Artikelstandort). |
| „Einstellungen fehlen: Versandbedingung, … (Einstellungen → eBay & Rahmenbedingungen)“ | Fehlende Felder in den Einstellungen im Reiter „eBay & Rahmenbedingungen“ → Karte „Rahmenbedingungen“ ausfüllen. |
| „Die Produkt-Datenbank ist leer.“ | Erst Produkte importieren. Direkt nach dem Update auf 46.0: im Dashboard nachsehen, ob noch „… werden noch auf den Server übertragen“ steht – dann etwas warten. |
| „Alle … Produkte der Datenbank sind gerade in Arbeit – auf diesem oder einem anderen Gerät, oder sie warten auf ein eBay-Ergebnis.“ | Kein freies Produkt da. In der Produkt-Datenbank in der Spalte „In Arbeit“ nachsehen, wer sie hat. Warten Produkte dieses Geräts auf eBay: „Ergebnisse bei eBay abholen“; wurden die Dateien sicher nie hochgeladen: „Wartende vergessen“. Sonst neue Produkte importieren oder warten, bis der andere Lauf fertig ist. |
| „Server nicht erreichbar – Lauf nicht gestartet. Die Produkt-Datenbank liegt auf dem Server, bitte später erneut starten.“ (ggf. mit „(HTTP …)“) | Internetverbindung prüfen, später erneut starten. Bleibt es, Betreiber benachrichtigen. |
| „Produkt-Datenbank: nicht angemeldet oder Sitzung abgelaufen – Lauf nicht gestartet (Dashboard → Anmelden).“ | Im Dashboard neu anmelden. |
| „Produkt-Datenbank: … Lauf nicht gestartet.“ | Der Server hat die Anfrage abgelehnt. Später erneut versuchen; bleibt es, den Betreiber mit dem genauen Text fragen. |
| Meldung beginnt mit „Claims-Server nicht erreichbar“ | Der Server des Betreibers ist gerade nicht erreichbar. Internetverbindung prüfen, später erneut versuchen; bleibt es, Betreiber benachrichtigen. |
| „Es läuft schon ein Lauf.“ | Warten, bis der Lauf fertig ist. |
| „In einem anderen Tab läuft gerade ein Lauf (Puls …).“ | Den anderen Tab benutzen oder dort abwarten. Immer nur einen CSV-Lister-Tab öffnen. |
| „Es werden gerade Ergebnisdateien abgeholt – bitte kurz warten.“ | Kurz warten, dann erneut starten. |
| „Tageskontingent erreicht – ab Mitternacht wieder frei.“ bzw. „Tageskontingent erreicht (… Produkte heute) – ab Mitternacht wieder frei.“ | Bis nach Mitternacht warten. Wartende Produkte kannst du trotzdem mit „Ergebnisse bei eBay abholen“ verbuchen. |
| „Tageskontingent erreicht – Rückgabe von … ausstehend – wird nachgeholt. Bitte in ein paar Minuten erneut starten.“ | Ein paar Minuten warten, dann erneut starten. Die Seite bucht nicht verbrauchtes Kontingent früherer Läufe von selbst zurück. |
| „Tageskontingent reicht nicht – heute noch … von … Produkten frei. Bitte erneut starten.“ | Einfach erneut starten. |
| „Tageskontingent nicht abrufbar: …“ / „Tageskontingent nicht buchbar: …“ | Im Dashboard neu anmelden; Internetverbindung prüfen; später erneut versuchen. Bleibt es, Betreiber fragen. |
| „Tageskontingent: die Buchung dieses Laufs wurde inzwischen von einer anderen Lister-Seite zurückgegeben (galt als unbeantwortet) – Lauf nicht gestartet, bitte erneut starten.“ | Die CSV-Lister-Seite ist in zwei Tabs offen. Einen Tab schließen, dann erneut starten. |
| Meldung beginnt mit „Der Claims-Server liefert Bildadressen ohne HTTPS …“ | Das liegt am Server des Betreibers, nicht an dir. Betreiber benachrichtigen. |
| Knopf „Lauf starten“ grau | Entweder läuft ein Lauf, ein Start ist noch in Arbeit, oder das Tageskontingent ist erreicht. |
| Eintrag „CSV-Lister“ in der Seitenleiste ausgegraut | Nicht angemeldet, Zugang abgeschaltet oder Abo gesperrt (siehe unten in der Seitenleiste). |

#### Lauf hält an (rote Box)

| Meldung | Bedeutung und Lösung |
|---|---|
| „Amazon zeigt Captcha oder Anmeldeseite – Lauf angehalten. Bitte im Browser lösen und neu starten.“ | Eine Amazon-Seite im selben Chrome-Profil öffnen, das Captcha lösen bzw. die Seite normal laden, dann neu starten. Die Produkte des Laufs gehen zurück in die Datenbank; fertige Zeilen werden trotzdem hochgeladen. |
| „Anmeldung weg (Sitzung abgelaufen oder Zugang abgeschaltet) – Lauf angehalten.“ | Im Dashboard neu anmelden. Steht unten in der Seitenleiste „Abo gesperrt“, siehe konto-und-installation.md. Klappt es nicht, Betreiber fragen. |
| „Amazon-Skript: nicht angemeldet – Lauf angehalten (Anmeldung/Mitgliedschaft prüfen).“ | Im Dashboard neu anmelden. |
| „Nicht angemeldet – bitte im Dashboard anmelden (die eBay-Abfragen laufen über den Server).“ / „Nicht angemeldet oder Sitzung abgelaufen – bitte im Dashboard neu anmelden.“ | Im Dashboard neu anmelden. |
| „Dieser Zugang ist abgeschaltet.“ | Dein Zugang ist gesperrt – oder dein Abo (der CSV-Lister zeigt bei beidem denselben Text). Unten in der Seitenleiste nachsehen; steht dort nur „Nicht angemeldet“, im Dashboard neu anmelden – die Anmeldung zeigt dann, ob das Abo gesperrt ist. Bei „Abo gesperrt“ siehe konto-und-installation.md, sonst an den Betreiber wenden. |
| „KI-Schnittstelle: Kein OpenAI API Key gesetzt (Options-Seite).“ | OpenAI-Schlüssel in den Einstellungen im Reiter „KI“ → „OpenAI-API-Schlüssel (für die Titel-Generierung)“ eintragen. (Ohne Schlüssel scheitert meist schon der KI-Titel – dann siehst du statt dieser Meldung viele „zurückgestellt“, siehe unten.) |
| „KI-Schnittstelle: OpenAI: API-Key ungültig oder abgelaufen – bitte prüfen (Einstellungen → KI → „OpenAI-API-Schlüssel“).“ | Schlüssel im Reiter „KI“ prüfen bzw. neu eintragen. |
| „KI-Schnittstelle: OpenAI-Guthaben leer: …“ | Guthaben bei OpenAI aufladen. |
| „KI-Schnittstelle vorübergehend nicht nutzbar: … – Lauf angehalten, später neu starten.“ | Die KI ist überlastet oder antwortet nicht; der Lauf hat schon Pausen gemacht. Später neu starten, ggf. mit weniger gleichzeitigen Produkten. |
| „Amazon: bei 15 Produkten hintereinander kein Versender erkennbar – Seitenaufbau vermutlich geändert, Lauf angehalten. Bitte melden.“ | Entweder viele ausverkaufte Produkte hintereinander oder Amazon hat seine Seite geändert. Dem Betreiber melden. |
| „Bild-Server: Bild-Upload dauerte länger als … s (… MB) – Upload zu langsam oder Server hängt; bei „gleichzeitig“ eine kleinere Zahl wählen – Lauf angehalten.“ | Bei „gleichzeitig“ eine kleinere Zahl wählen; Internetverbindung prüfen. |
| andere Meldungen, die mit „Bild-Server:“ beginnen und mit „– Lauf angehalten.“ enden | Der Bild-Dienst des Betreibers ist nicht erreichbar oder hat die Anmeldung abgelehnt. Im Dashboard neu anmelden, später erneut versuchen; bleibt es, Betreiber benachrichtigen. |
| „Server bremst die eBay-Abfragen auch nach 20 Wartezeiten – Lauf angehalten, bitte später neu starten.“ | Später erneut starten, ggf. mit weniger gleichzeitigen Produkten. |
| Meldung beginnt mit „eBay-Rate-Limit erreicht …“ | eBay bremst gerade. Später erneut starten. |
| Meldung beginnt mit „eBay-Zugang des Servers gestört …“ oder „Auf dem Server sind keine eBay-Schlüssel eingerichtet …“ | Problem auf dem Server des Betreibers. Die Produkte gehen zurück in die Datenbank. Betreiber benachrichtigen. |
| „Tageskontingent dieses Laufs aufgebraucht (… gebucht) – Lauf angehalten.“ / „Das Tageskontingent dieses Laufs wurde von einer anderen Lister-Seite zurückgegeben – Lauf angehalten, bitte erneut starten.“ | Kommt praktisch nur vor, wenn die CSV-Lister-Seite in zwei Tabs offen ist. Einen Tab schließen und neu starten. Fertige Zeilen wurden trotzdem hochgeladen. |
| „eBay hat die Abfragen zu 5 Produkten hintereinander abgelehnt …“ | Vermutlich eine Störung. Die Produkte bleiben in der Datenbank. Dem Betreiber melden; später erneut versuchen. |
| Meldung beginnt mit „Claims-Server nicht erreichbar“ | Der Server des Betreibers ist gerade nicht erreichbar. Internetverbindung prüfen, später erneut versuchen; bleibt es, Betreiber benachrichtigen. Die Rückgabe der Produkte holt die Seite von selbst nach. |
| „Lauf angehalten (Fehler in einem anderen Thread)“ (bei einzelnen Produkten) | Ein anderer Thread hatte einen technischen Fehler; der eigentliche Grund steht in der roten Box. |
| „Lauf wurde unterbrochen (Seite oder Browser geschlossen) – …“ | Siehe [B16](#b16-abbrechen-anhalten-seite-geschlossen). |

#### Einzelne Produkte

| Problem | Lösung |
|---|---|
| Viele „übersprungen“ mit „Amazon: Nicht von Amazon versendet …“ | Das ist der Filter „Nur FBA“. Wenn gewollt, alles richtig. |
| Viele „übersprungen“ mit „Amazon: Keine GPSR-Angaben gefunden“ oder „Amazon: Kein chinesischer Verkäufer“ | Die Filter „GPSR-Angaben übernehmen“ bzw. „Nur chinesische Verkäufer“ sind an (gelber Punkt in den Details). Im Reiter „Produkt-Filter“ ausschalten, wenn nicht gewollt – aber Achtung: übersprungene Produkte sind schon gelöscht. |
| Viele „übersprungen“ mit „Amazon: Amazon-Preis zu hoch (Filter „Preis bis“)“ | Im Reiter „Produkt-Filter“ → „Amazon-Filter“ „Preis bis“ prüfen. Oft steht dort noch eine 100 aus einer älteren Version; Zahl ändern oder den Schalter daneben ausschalten. |
| Viele „übersprungen“ mit „Amazon: Produkt ist nicht auf Lager“ | Entweder wirklich nicht lieferbar, oder die Lieferzeit ist länger als „Max. verlängerte Lieferzeit“ (Reiter „Produkt-Filter“ → „Amazon-Filter“). |
| Viele „keine ermäßigte eBay-Gebühr für „Neu: Sonstige“ …“ | „NUR „Neu: Sonstige“ listen“ ist an; Produkte in Kategorien ohne Ermäßigung werden aussortiert. Wenn nicht gewollt, den Schalter im Reiter „Preise & Listing“ ausschalten. |
| Viele „kein Kategorievorschlag von eBay“ | eBay findet zum Titel keine Kategorie. Mit „Kategorie und Merkmale zu einem Titel“ (unter „Technik“) kannst du Titel testen. |
| „Pflichtmerkmal ohne passenden Wert (nur Auswahl/Zahl): …“ | Die Kategorie verlangt ein Merkmal, für das weder die KI noch ein neutraler Wert passt. Das Produkt ist für diese Kategorie nicht automatisch listbar. |
| Viele oder alle Produkte „zurückgestellt“ mit „Amazon-Skript: KI-Titel ist leer“ (oder „… Titel-Erstellung fehlgeschlagen“) | Die KI konnte keinen Titel erzeugen. Häufigste Ursache: OpenAI-Schlüssel fehlt, ist ungültig oder das OpenAI-Guthaben ist leer. Schlüssel im Reiter „KI“ prüfen, Guthaben prüfen, dann neu starten. Die Produkte gehen zurück in die Datenbank, verbrauchen aber bei jedem Lauf Kontingent. |
| Viele „übersprungen“ mit „Amazon: Produkt ist schon gelistet (Duplikat)“ | Diese Produkte hast du in diesem Chrome-Profil schon mit dem Browser-Lister gelistet. Sie werden aus der Produkt-Datenbank gelöscht; so steht dasselbe Produkt nicht doppelt in deinem Shop. Gemerkt wird das nur in diesem Chrome-Profil – Produkte, die du anders oder an einem anderen Rechner gelistet hast, erkennt diese Prüfung nicht. |
| Dasselbe Produkt wird immer wieder „zurückgestellt“ | Es verbraucht bei jedem Lauf Kontingent. Prüfe den Grund. Bei „Amazon-Seite … nicht geladen“ oder „hängt“: Internetverbindung, weniger gleichzeitige Produkte. **Nicht sicher belegt:** alle Ursachen für „Amazon-Skript ohne Produktdaten“ – tritt es bei einem Produkt immer wieder auf, das Produkt in der Produkt-Datenbank löschen oder den Betreiber fragen. |
| Produkt steht als „nicht mehr dran“ oder „verworfen (anderes Gerät)“ | Die Seite war angehalten, inzwischen hat ein anderes Gerät das Produkt – oder es wurde in der Produkt-Datenbank gelöscht. Nichts zu tun; so wird es nicht doppelt gelistet. |
| „abgelehnt“ mit „eBay: …“ | eBays eigener Grund. Das Produkt ist schon aus der Datenbank. Bei häufig gleichem Grund (z. B. Rahmenbedingung, EAN, Merkmal) die Einstellungen prüfen und den Betreiber mit dem genauen Text informieren. |
| „mit eBay-Warnung“ | Angebot bei eBay öffnen und Kategorie/Merkmale prüfen; ggf. bei eBay von Hand korrigieren. |
| Ein Angebot hat bei eBay keine Bilder | **Nicht sicher belegt:** Ursache und Lösung. Dem Betreiber mit der eBay-Artikelnummer melden. |

#### Upload und Ergebnis

| Problem | Lösung |
|---|---|
| „Upload nicht gelungen: Nicht bei eBay angemeldet – …“ | Im selben Chrome-Profil im eBay Seller Hub anmelden, dann neu starten. Die Produkte sind zurück in der Datenbank. |
| „Upload nicht gelungen: Keine eBay-Domain eingestellt (Einstellungen → Preise & Listing → „Domain“).“ | In den Einstellungen im Reiter „Preise & Listing“ → Karte „Listing“ bei „Domain“ „DE“ wählen. |
| „Upload nicht gelungen: Zeitüberschreitung beim Warten auf: Knopf „Vorlage hochladen““ (o. Ä.) | Der Seller Hub sah anders aus als erwartet – z. B. andere Sprache als Deutsch/Englisch/Italienisch, ein Begrüßungsfenster oder eine Störung bei eBay. Seller Hub einmal von Hand öffnen, Sprache prüfen, dann neu starten. |
| „Upload-Ergebnis unklar: …“ | Nicht neu starten, um „nachzuhelfen“. Erst „Ergebnisse bei eBay abholen“. Meldet das „… Upload(s) rechnet eBay noch“: später nochmal. |
| „Upload angenommen …, aber die Ergebnisdatei war nicht lesbar …“ | „Ergebnisse bei eBay abholen“ klicken. |
| „… Produkt(e) warten weiter (CSV noch nicht hochgeladen oder Datei umbenannt?)“ | Prüfen, ob die Datei im Seller Hub hochgeladen ist. Wenn nicht und sicher nicht: „Wartende vergessen“. |
| „Nicht abgeholt: Seller Hub nicht erreichbar … – bist du bei eBay angemeldet?“ bzw. „Nicht abgeholt: Nicht bei eBay angemeldet – bitte in diesem Chrome-Profil im Seller Hub anmelden …“ | Im selben Chrome-Profil bei eBay anmelden, erneut abholen. |
| „Nicht abgeholt: Seller Hub hat in 120 s nicht geantwortet“ / „Nicht abgeholt: Seller-Hub-Seite in 60 s nicht geladen“ | eBay war gerade langsam. Später erneut auf „Ergebnisse bei eBay abholen“ klicken. |
| „Nicht abgeholt: Es läuft gerade ein Lauf oder ein Abholen.“ / „… In einem anderen Tab läuft gerade ein Lauf – bitte dort abwarten.“ | Warten. |
| „Lauf wurde unterbrochen … siehe „Letzte CSV herunterladen““ | Den Knopf gibt es nicht. Vorgehen siehe [B16](#b16-abbrechen-anhalten-seite-geschlossen). |
| Produkte bleiben auf einem anderen Gerät „in Arbeit“, weil dort ein Lauf abgestürzt ist | Die CSV-Lister-Seite auf **dem Gerät öffnen, auf dem der Lauf lief** – sie räumt dann auf. Kurz gehaltene Produkte werden ohnehin nach etwa einer Stunde wieder frei; Produkte mit fertiger Zeile erst nach „Ergebnisse bei eBay abholen“ / „Wartende vergessen“ auf jenem Gerät oder nach bis zu 7 Tagen. |

#### Sonstiges

| Problem | Lösung |
|---|---|
| Status „Muster-CSV“ rot | Installation beschädigt. Extension neu installieren oder Betreiber fragen. |
| „Server und eBay-Zugang prüfen“ zeigt „ACHTUNG“, „KEIN HTTPS“ oder rote Ausgabe | Das liegt nicht an dir. Text kopieren und dem Betreiber schicken; bis dahin keinen Lauf starten. |
| Seite zeigt „Läuft in einem anderen Tab“, obwohl kein anderer Tab offen ist | Ein bis zwei Minuten warten – dann erkennt die Seite den alten Lauf als beendet und räumt auf. Danach ggf. Seite neu laden. |
| Kontingent-Anzeige bleibt nach Mitternacht auf „erreicht“ | In den Tab klicken (die Seite prüft beim Zurückkehren neu) oder bis zu 10 Minuten warten. |
| Amazon-Tabs bleiben nach dem Lauf offen | Am Laufende schließt die Seite offene Amazon-Tabs des Laufs selbst. Bleiben trotzdem welche, kannst du sie von Hand schließen. |
| Der CSV-Lister fehlt in der Seitenleiste oder zeigt „Dieses Modul ist noch im Test“ | Alte Version geladen. Mit `update.bat` aktualisieren, Chrome komplett neu starten (bzw. unter `chrome://extensions` „Neu laden“). Bleibt es, Betreiber fragen. |
| Der Knopf „Einstellungen“ öffnet „Preise & Listing“, ich suche die Rahmenbedingungen | Oben auf der Einstellungsseite den Reiter „eBay & Rahmenbedingungen“ anklicken. |

---

## Neu in Version 46.0

Was Kunden, die bisher Version 45.5 hatten, jetzt anders finden:

**Allgemein**

- **Das kleine Fenster beim Klick auf das Symbol gibt es nicht mehr – es öffnet sich das Dashboard.** Den früheren Bereich „🧰 Werkzeuge“ mit den Knöpfen „Verkaufs-Übersicht“ und „CSV-Lister (neu)“ gibt es nicht mehr. Beide öffnest du über die Seitenleiste links (Verkaufs-Übersicht unter „Auswerten“, CSV-Lister unter „Arbeiten“), den CSV-Lister auch über die Dashboard-Karte unter „Vorgänge“.
- Neues Design und neuer Name „Cash Lister“ auf beiden Seiten; Anmeldung im Dashboard statt im kleinen Fenster.
- Jedes Modul öffnet in seinem eigenen Tab; ist es schon offen, springt der Klick dorthin.
- Was früher im kleinen Fenster eingestellt wurde (z. B. Preise, Domain), steht jetzt auf der Einstellungsseite im Reiter „Preise & Listing“.

**Verkaufs-Übersicht**

- Die Karte heißt jetzt „Berichte einlesen“ (früher „1 · Berichte einlesen“), die Schwelle „Vorschlag ab … Tagen ohne Verkauf“ (früher „Offline-Vorschlag ab …“).
- Die Felder heißen „Aktive Angebote“ und „Bestellbericht“ (mit „Active-Listings-CSV“ bzw. „Orders-CSV“ klein daneben).
- Fehlermeldungen zum Angebotsbericht beginnen jetzt mit „Angebotsbericht: …“ (früher „Active-Listings: …“).
- Der Durchschnitt bei der Anlaufzeit steht mit Komma („Ø 12,4 Tage“).
- Die Kennzahl „Aktive Angebote“ im Dashboard kann ihren Stand aus der Verkaufs-Übersicht nehmen („laut Verkaufs-Übersicht · Stand …“).
- Ablauf, Regeln, gespeicherte Daten, Schwelle und Haken bleiben beim Update unverändert.

**CSV-Lister**

1. **Für alle Kunden:** kein Zugangscode mehr; Eintrag in der Seitenleiste und Karte im Dashboard für alle.
2. **Gemeinsame Produkt-Datenbank:** Der CSV-Lister nimmt seine Produkte vom Server und markiert sie als „in Arbeit“. Mehrere Geräte und Browser-Lister und CSV-Lister gleichzeitig sind jetzt möglich; der gelbe Hinweis „Alter Bulk-Lister … besser nacheinander“ ist weg (jetzt „Alter Browser-Lister“, immer grün).
3. **Ohne Server startet kein Lauf** („Server nicht erreichbar – Lauf nicht gestartet. …“, meist schon vorher „Tageskontingent nicht abrufbar: …“).
4. **Nicht fertige Produkte gehen zurück in die Datenbank** (nach Abbruch, Halt, Absturz, misslungenem Upload) und sind sofort für alle Geräte wieder frei. Neue Texte: „… die Produkte gehen zurück in die Datenbank“, „Lauf unterbrochen (zurückgegeben)“, „… offene(s) Produkt(e) an die Datenbank zurückgegeben“.
5. Neue Meldung, wenn nichts frei ist: „Alle … Produkte der Datenbank sind gerade in Arbeit – auf diesem oder einem anderen Gerät, oder sie warten auf ein eBay-Ergebnis.“ (früher „… Ergebnisdatei einlesen oder 7 Tage warten.“).
6. Neue Schritte „nicht mehr dran“ und „verworfen (anderes Gerät)“.
7. **Einstellungen an neuer Stelle:** Rahmenbedingungen und Artikelstandort im Reiter „eBay & Rahmenbedingungen“ (Felder „Versand“, „Zahlung“, „Rücknahme“, „Artikelstandort (Ort oder PLZ)“); Domain und Preise im Reiter „Preise & Listing“; Filter und „Markenlos listen“ im Reiter „Produkt-Filter“. Die zweite Preistafel „Eigene Preise für „Neu: Sonstige““ gibt es nicht mehr – eine Preistafel für alle Zustände.
8. **Deutsche Meldungen** von der Amazon-Seite (z. B. „Amazon: Produkt ist nicht auf Lager“ statt „Item is not in stock“, „Amazon: Produkt ist schon gelistet (Duplikat)“ statt „Item is duplicate“, „KI-Titel ist leer“ statt „Title is undefined“) und deutsche Tab-Titel beim Upload (z. B. „📤 Lade Datei hoch…“).
9. Anmelde-Hinweise sagen jetzt „Dashboard → Anmelden“ (früher verwiesen sie auf das kleine Fenster beim Symbol).
10. Das Protokoll unter „Technik“ ist nicht mehr zu sehen.
11. Neuer Abschnitt im Dashboard: Karte „CSV-Lister“ unter „Vorgänge“, Hinweise in der Glocke, CSV-Lister-Zahlen bei „Heute gelistet“.

**Falls du von Version 45.4 oder älter kommst**, sind für Tester außerdem schon seit 45.5 neu: das Tageskontingent mit der Anzeige „Heute noch … von …“; erste eBay-Ablehnungen stellen ein Produkt nur zurück statt den Lauf anzuhalten; ungeeignete Bilder werden weggelassen statt das Produkt scheitern zu lassen; „Server bremst – warte … s“; ohne eigene Beschreibungsvorlage entsteht eine schlichte Beschreibung aus dem Produkttext.

---

## Was dieser Bereich nicht sicher weiß

Diese Punkte sind im Text mit **Nicht sicher belegt** markiert oder bewusst offen gelassen. Antworte hier nicht mit Vermutungen, sondern sag offen, dass es nicht sicher bekannt ist, und verweise auf den Betreiber:

- Die Menüpunkte und Beschriftungen im eBay Seller Hub, über die man zu den Berichten und zur Upload-Seite kommt, und auf welchem Weg genau der Bestellbericht erzeugt wird. (Belegt sind nur die Adressen www.ebay.de/sh/reports/downloads und www.ebay.de/sh/reports/uploads sowie der Knopf „Vorlage hochladen“.)
- Ob getrennte Chrome-Profile je Shop für die Verkaufs-Übersicht mit der Anmeldung vorgesehen sind.
- Weitere Ursachen für die Meldung „Datenbank: …“ in der Verkaufs-Übersicht, und ob deren Daten in jedem Einzelfall ein Update überstehen (z. B. bei Neuinstallation statt Aktualisierung).
- Wie hoch dein Tageskontingent ist und ob es erhöht werden kann (entscheidet der Betreiber; die Zahl steht neben „Produkte“).
- Ob der Server die Fristen für „in Arbeit“ (etwa eine Stunde für laufende Produkte, bis zu 7 Tage für Produkte mit fertiger Zeile) in jedem Fall genau so umsetzt – das sind die Werte, die die Extension verlangt.
- Was „neu · im Test“ für dich praktisch bedeutet (z. B. ob sich Abläufe noch ändern).
- Ob bei einem Kunden noch eine alte gespeicherte Menge je Angebot gilt (sonst 1).
- Was eBay genau tut, wenn der Name einer Rahmenbedingung nicht passt.
- Was beim CSV-Lister mit einer anderen Domain als „DE“ im Ergebnis passiert. (Belegt ist nur: Der Upload ginge dann an den Seller Hub dieser eBay-Seite, der KI-Titel käme in deren Sprache, die Datei selbst ist aber fest für Deutschland und Euro angelegt.)
- Die aktuellen Gebührensätze für „Neu: Sonstige“ (die eingebaute Liste kann veralten).
- Alle Ursachen für „Amazon-Skript ohne Produktdaten“.
- Ursache und Lösung, wenn ein gelistetes Angebot bei eBay keine Bilder hat.
- Zur Prüfung Auktion/Sofort-Kaufen gibt es hier keine Beschreibung – bei Fragen an den Betreiber wenden.
