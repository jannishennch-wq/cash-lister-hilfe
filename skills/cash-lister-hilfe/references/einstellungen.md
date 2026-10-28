# Einstellungen (Einstellungsseite der Extension)

Dieser Teil erklärt die Einstellungsseite von Cash Lister: jeden Reiter, jede Karte, jeden Schalter und jedes Feld. Dazu kommt, wie du deine Einstellungen sicherst, auf einen anderen Rechner mitnimmst und wiederherstellst.

> Hinweis für den Assistenten: Stellen, die mit **Nicht sicher belegt:** markiert sind, sind offen. Sag dem Kunden das ehrlich ("Das weiß ich nicht sicher") und verweise an den Betreiber, statt zu raten. Beschreibe nur, was hier steht.

## Inhalt

1. [Überblick: Was steht wo?](#1-überblick-was-steht-wo)
2. [So öffnest du die Einstellungsseite](#2-so-öffnest-du-die-einstellungsseite)
3. [Speichern: so funktioniert es wirklich](#3-speichern-so-funktioniert-es-wirklich)
4. [Aufbau der Seite: die sechs Reiter](#4-aufbau-der-seite-die-sechs-reiter)
5. [Reiter Preise und Listing: Karte Preise und die Preisrechnung](#5-reiter-preise-und-listing-karte-preise-und-die-preisrechnung)
6. [Reiter Preise und Listing: Karten Listing und Artikelmerkmale](#6-reiter-preise-und-listing-karten-listing-und-artikelmerkmale)
7. [Reiter Produkt-Filter: Karte Beim Listen](#7-reiter-produkt-filter-karte-beim-listen)
8. [Reiter Produkt-Filter: Karte Amazon-Filter](#8-reiter-produkt-filter-karte-amazon-filter)
9. [Reiter Produkt-Filter: Karte Blacklist und die eingebauten Wortfilter](#9-reiter-produkt-filter-karte-blacklist-und-die-eingebauten-wortfilter)
10. [Reiter eBay und Rahmenbedingungen: Karte Rahmenbedingungen](#10-reiter-ebay-und-rahmenbedingungen-karte-rahmenbedingungen)
11. [Reiter eBay und Rahmenbedingungen: Karten Beim Einstellen und Neu Sonstige](#11-reiter-ebay-und-rahmenbedingungen-karten-beim-einstellen-und-neu-sonstige)
12. [Reiter eBay und Rahmenbedingungen: Karte Server und Produkt-Vergabe](#12-reiter-ebay-und-rahmenbedingungen-karte-server-und-produkt-vergabe)
13. [Reiter eBay und Rahmenbedingungen: Karte Server-Modus](#13-reiter-ebay-und-rahmenbedingungen-karte-server-modus)
14. [Reiter Beschreibungsvorlage](#14-reiter-beschreibungsvorlage)
15. [Reiter KI: OpenAI-Schlüssel und Modell](#15-reiter-ki-openai-schlüssel-und-modell)
16. [Reiter Sicherung: Datei und Server](#16-reiter-sicherung-datei-und-server)
17. [Versand, Zahlung, Rücknahme, Artikelstandort](#17-versand-zahlung-rücknahme-artikelstandort)
18. [Mitgelieferte KI-Anweisungen und Wortlisten](#18-mitgelieferte-ki-anweisungen-und-wortlisten)
19. [Wechselwirkungen auf einen Blick](#19-wechselwirkungen-auf-einen-blick)
20. [Standardwerte auf einen Blick](#20-standardwerte-auf-einen-blick)
21. [Meldungen und was sie bedeuten](#21-meldungen-und-was-sie-bedeuten)
22. [Häufige Fragen (allgemein)](#22-häufige-fragen-allgemein)
23. [Probleme und Lösungen (allgemein)](#23-probleme-und-lösungen-allgemein)
24. [Kleines Wörterbuch](#24-kleines-wörterbuch)
25. [Was hier nicht sicher belegt ist](#25-was-hier-nicht-sicher-belegt-ist)
26. [Neu in Version 46.0](#26-neu-in-version-460)

---

## 1. Überblick: Was steht wo?

Seit Version 46.0 gibt es **kein kleines Fenster (Popup)** mehr. Ein Klick auf das Cash-Lister-Symbol oben rechts in Chrome öffnet das **Dashboard**. Alle Einstellungen, die früher im Popup standen, stehen jetzt auf der **Einstellungsseite**.

| Wo | Was du dort einstellst |
|---|---|
| **Einstellungsseite** (Tab-Titel "Cash Lister – Einstellungen", Überschrift "Einstellungen") | Preise und Aufschläge, Preisendung, "Neu: Sonstige", eBay-Land ("Domain"), automatisches Absenden, Anzeigengebühr, Artikelmerkmale per KI, Produkt-Filter (FBA, chinesische Verkäufer, GPSR, Bildabgleich), Amazon-Filter (Lieferzeit, Sterne, Bewertungen, Lagerbestand, Preisgrenzen), Blacklist, Rahmenbedingungen für den CSV-Lister, Angebotsgebühr, Bilder, Mehrwertsteuer, Zustandsbeschreibung, Produkt-Vergabe, Server-Modus, Beschreibungsvorlage, OpenAI-Schlüssel und Modell, Export/Import und Server-Sicherung |
| **Dashboard** (Klick auf das Cash-Lister-Symbol) | Anmeldung ("Benutzername", "Passwort", "Anmelden"), "Einrichtungsdatei einlesen", das aufklappbare Feld "Server-Adresse (nur auf Ansage ändern)", die Abo-Karte "Dein Abo". Das gehört nicht zur Einstellungsseite und steht in den Teilen über das Dashboard (`references/dashboard.md`) sowie über Konto und Installation (`references/konto-und-installation.md`). |
| **Browser-Lister** (früher "Bulk-Lister") | "Produkte aus", "Wie viele Angebote", "Gleichzeitig", "Fehler-Tabs schließen", "Zeitschaltung an" mit "danach … Stunden". Steht im Teil über das Listen. |
| **Tracker** (früher "CSV Tracker"), **Verkaufs-Übersicht**, **Konkurrenz-Scanner**, **CSV-Lister** | jeweils eigene Einstellungen auf ihrer Seite |
| **Amazon-Suchseite** | der Schalter "nur Verkauf durch Amazon" über dem Grabber-Knopf. Das ist **derselbe** Wert wie "Nur Verkauf durch Amazon" auf der Einstellungsseite (Abschnitt 8.7). |

Wichtig zu wissen:

- Alle Einstellungen gelten **pro Chrome-Profil**. Hast du zwei Chrome-Profile, hat jedes seine eigenen Einstellungen.
- Die Einstellungen liegen **in Chrome auf deinem Rechner**. Entfernst du die Extension aus Chrome, löscht Chrome sie mit. Darum gibt es die Export-Datei und – wenn du angemeldet bist – die automatische Sicherung auf dem Server (Abschnitt 16).
- Ein normales Update der Extension behält deine Einstellungen.
- Die **Produkt-Datenbank** gehört seit 46.0 nicht mehr zu den Einstellungen: Sie liegt für dein Konto auf dem Server. Mehrere Geräte mit demselben Konto sehen dieselbe Liste. Einzelheiten stehen im Teil über die Produkt-Datenbank.
- Die Einstellungsseite lässt sich auch **ohne Anmeldung** öffnen und ändern. Produkt-Vergabe und Server-Sicherung funktionieren aber nur mit Anmeldung (Anmeldung im Dashboard).

---

## 2. So öffnest du die Einstellungsseite

**Weg 1 – über das Dashboard (der normale Weg)**
1. Klicke oben rechts in Chrome auf das Cash-Lister-Symbol (eventuell erst über das Puzzle-Symbol anheften). Das Dashboard öffnet sich. Ist es schon offen, springt Chrome zu diesem Tab.
2. Links in der Seitenleiste, unter der Überschrift "System", auf "Einstellungen" klicken.

Ist die Einstellungsseite schon offen, springt der Klick in diesen Tab, statt einen zweiten zu öffnen.

**Weg 2 – von jeder anderen Seite der Extension**
Browser-Lister, Tracker, Produkt-Datenbank, Verkaufs-Übersicht, Konkurrenz-Scanner und CSV-Lister haben links dieselbe Seitenleiste. Dort unter "System" auf "Einstellungen" klicken.

**Weg 3 – Rechtsklick auf das Symbol**
1. Mit der **rechten** Maustaste auf das Cash-Lister-Symbol klicken.
2. "Optionen" wählen.

**Weg 4 – über die Chrome-Erweiterungsverwaltung**
1. `chrome://extensions` in die Adresszeile tippen und Enter drücken.
2. Bei "Cash Lister" auf "Details" klicken.
3. Nach unten scrollen und "Erweiterungsoptionen" anklicken.

**Weg 5 – aus dem Browser-Lister**
In der Karte "Tabs und Filter" steht bei "Produkt-Filter" der Knopf "Ändern". Er öffnet die Einstellungsseite.

**Weg 6 – aus dem CSV-Lister**
Oben in der Statuszeile auf "Einstellungen" klicken.

**Weg 7 – aus dem Dashboard-Hinweis**
Steht im Dashboard unter den Hinweisen (Glocken-Symbol "Hinweise") der Eintrag "Einstellungen: zwei Geräte", öffnet ein Klick darauf die Einstellungsseite. Danach selbst auf den Reiter "Sicherung" klicken (Abschnitt 16.5).

Die Seite öffnet sich immer mit dem ersten Reiter, "Preise & Listing". Welchen Reiter du zuletzt offen hattest, merkt sie sich nicht.

---

## 3. Speichern: so funktioniert es wirklich

Unter der Überschrift steht: "Preise, Listing, Filter, eBay-Angaben, Beschreibungsvorlage, Server und Sicherung · jede Änderung wird gespeichert, sobald du das Feld verlässt". Genauer:

- **Schalter** werden **sofort** gespeichert, wenn du sie umlegst.
- **Auswahllisten** ("Domain", "OpenAI-Modell") werden sofort gespeichert, wenn du einen Eintrag wählst.
- **Text- und Zahlenfelder** werden gespeichert, **sobald du das Feld verlässt** – also wenn du woanders hinklickst oder die Tab-Taste drückst.
- **Ausnahme Preise:** "% Aufschlag", "Fester Aufschlag (€)" und alle Felder der Preisregeln werden schon **beim Tippen** gespeichert.
- **Die Blacklist** wird knapp eine halbe Sekunde nach dem letzten Tastendruck gespeichert.
- **Der Knopf "Speichern"** (unten rechts, schwebt immer über der Seite) öffnet nur ein kleines Browser-Fenster mit "Einstellungen gespeichert", das du mit "OK" schließt. Er speichert selbst nichts zusätzlich. Weil du beim Klick aber das Feld verlässt, in dem du gerade getippt hast, wird dieses Feld dabei gespeichert. "Speichern" zu drücken schadet also nie. Im Reiter "Sicherung" wird der Knopf nicht angezeigt.

**Typischer Fehler:** Du tippst etwas in ein Textfeld und schließt sofort den Tab, ohne vorher woanders hinzuklicken. Dann kann die letzte Eingabe verloren sein.
**So vermeidest du das:** Nach dem Tippen einmal neben das Feld klicken oder "Speichern" drücken, dann den Tab schließen.

**Zurücksetzen:** Es gibt **keinen** Knopf "Zurücksetzen" oder "Standard wiederherstellen". Willst du zurück zu den Standardwerten, trag sie von Hand ein. Alle Standardwerte stehen in Abschnitt 20.

**Wann wirken Änderungen?**
- Der Produkt-Grabber auf Amazon-Seiten übernimmt geänderte Amazon-Filter sofort, auch wenn die Amazon-Seite schon offen ist.
- Beim Listen werden die Einstellungen bei jedem Produkt neu gelesen.
- Preise und Preisendung wirken sofort auch in einem **laufenden Tracker**.
- Die Einstellungsseite selbst liest die Werte nur beim Öffnen. Hast du woanders etwas geändert (zum Beispiel eine Datei eingespielt oder die Server-Sicherung geholt), lade die Einstellungsseite neu (F5).

---

## 4. Aufbau der Seite: die sechs Reiter

Links steht die Seitenleiste (Cash-Lister-Logo, die Module, unten der Verbindungsstand und die Versionsnummer). Rechts stehen oben die Überschrift "Einstellungen" und darunter sechs Reiter (Karteikarten-Knöpfe). Ein Klick auf einen Reiter zeigt seinen Inhalt.

| Reiter | Karten darin (von links oben nach rechts unten) | Abschnitt |
|---|---|---|
| "Preise & Listing" | "Preise"; rechts daneben "Listing" und "Artikelmerkmale (KI)" | 5, 6 |
| "Produkt-Filter" | "Beim Listen", "Amazon-Filter", darunter "Blacklist" | 7, 8, 9 |
| "eBay & Rahmenbedingungen" | oben "Rahmenbedingungen"; links "Beim Einstellen" und "Neu: Sonstige"; rechts "Server & Produkt-Vergabe" und "Server-Modus" | 10–13 |
| "Beschreibungsvorlage" | "Beschreibungsvorlage (HTML)" | 14 |
| "KI" | "KI (OpenAI)" | 15 |
| "Sicherung" | "Als Datei", "Auf dem Server" | 16 |

Dazu der Knopf "Speichern" unten rechts (Abschnitt 3).

Viele Zeilen haben unter dem Namen eine kleine graue Erklärung (zum Beispiel "Amazon muss der Versender sein"). Die Schalter stehen jeweils rechts in der Zeile.

---

## 5. Reiter Preise und Listing: Karte Preise und die Preisrechnung

Die Karte "Preise" trägt den Hinweis "gilt beim Listen und im Tracker". Hier legst du fest, zu welchem Preis deine Angebote bei eBay stehen. Gerechnet wird immer vom **Amazon-Preis** (deinem Einkaufspreis) aus.

### 5.1 "% Aufschlag"

**Was es macht:** Prozent-Aufschlag auf den Amazon-Preis.
**Standard bei einer neuen Installation:** 120 (wird bei der Installation eingetragen). Eine Einrichtungsdatei vom Betreiber oder die Server-Sicherung kann andere Werte mitbringen.
**Erlaubt:** ab 0, Cent-Schritte (zum Beispiel 35 oder 27,5). Ein leeres Feld zählt als 0, also kein Aufschlag.
**Beispiel:** Amazon-Preis 20 €, Aufschlag 30 → 20 + 6 = 26 € (vor Festbetrag und Preisendung).

**Wichtig nach einer Neuinstallation – sonst preist der Tracker zu billig nach:** Die Karte "Preise" speichert deine Preis-Einstellung erst vollständig, wenn du in "% Aufschlag" oder "Fester Aufschlag (€)" einmal etwas eintippst oder einen der Schalter für "Neu: Sonstige" bzw. "Variable Preise" umlegst (der Schalter der Preisendung zählt hier nicht). Bis dahin rechnet nur das **Listen** mit den 120 % (ohne festen Aufschlag). Der **Tracker** kennt dann noch keinen Aufschlag und preist zum **Amazon-Preis ohne Aufschlag** nach (nur mit Preisendung). So vermeidest du das:
1. Einstellungsseite öffnen, Reiter "Preise & Listing".
2. In "% Aufschlag" deinen Aufschlag eintippen – auch wenn dort schon der richtige Wert steht (zum Beispiel die letzte Ziffer löschen und neu tippen).
3. Fertig: Ab jetzt rechnen Listen und Tracker mit denselben Werten.

### 5.2 "Fester Aufschlag (€)"

**Was es macht:** Ein fester Betrag, der **nach** dem Prozent-Aufschlag dazukommt (zum Beispiel für Versand oder Gebühren).
**Standard:** 0.
**Beispiel:** 20 € Amazon-Preis, 30 % und fester Aufschlag 2 → 20 + 6 + 2 = 28 €.

### 5.3 "Preisendung" mit Schalter

Rechts neben dem Zahlenfeld steht ein Schalter ("Preisendung ein oder aus").

- **Schalter an (Standard):** Der Preis wird auf den nächsten vollen Euro **aufgerundet**, dann wird so viel abgezogen, dass die gewünschte Endung entsteht.
- **Schalter aus:** Es bleibt der Preis aus Aufschlag und Festbetrag, auf Cent genau. Das Zahlenfeld ist dann ausgegraut.

**Feld:** Werte von 0 bis 0,99. **Standard:** 0,99. Ist das Feld leer, trägt die Seite beim nächsten Öffnen wieder 0,99 ein.

**Typische Fehler:**
- *Feld geleert, um die Endung abzuschalten.* Dafür ist der Schalter da. Solange das Feld leer ist (und der Schalter an), kann die Extension keinen Verkaufspreis ausrechnen: Der CSV-Lister überspringt die Produkte mit "kein Verkaufspreis aus der Preisstaffelung", der Browser-Lister hat keinen Preis zum Eintragen, und auch der Tracker rechnet keinen gültigen Preis aus. Lösung: wieder eine Endung eintragen (zum Beispiel 0,99) oder den Schalter ausschalten. **Nicht sicher belegt:** welche Meldung der Browser-Lister in diesem Fall zeigt.
- *Zahl größer als 0,99 eingetippt* (zum Beispiel 5). Das wird nicht abgefangen und schiebt den Preis nach oben: Bei 5 wird aus 26,00 € ein Preis von 30,00 €. Nur Werte von 0 bis 0,99 eintragen.

### 5.4 So rechnet die Extension deinen eBay-Preis

1. Verkaufspreis = Amazon-Preis + (Amazon-Preis × "% Aufschlag" ÷ 100) + "Fester Aufschlag (€)"
2. Ist die Preisendung **an**: auf den nächsten vollen Euro aufrunden, dann auf die Endung bringen. Bei Endung 0 wird nur aufgerundet.
3. Ist die Preisendung **aus**: der Preis aus Schritt 1, auf Cent gerundet.

Sind "Variable Preise" an und passt eine Regel, nimmt Schritt 1 statt der beiden Felder oben die Werte dieser Regel (Abschnitt 5.5).

**Zahlenbeispiel:** Amazon-Preis 18,40 €, "% Aufschlag" 30, "Fester Aufschlag (€)" 2, Preisendung 0,99 (an):
- 18,40 + 5,52 + 2,00 = 25,92
- aufrunden → 26,00 → Endung 0,99 → **25,99 €**

Weitere Beispiele mit demselben Ausgangspreis:
- Preisendung 0,49 → 26,00 → **25,49 €** (also etwas *unter* den errechneten 25,92 €!)
- Preisendung 0 → nur aufrunden → **26,00 €**
- Preisendung aus → **25,92 €**

Achtung: Ergibt Schritt 1 genau einen vollen Betrag (zum Beispiel 28,00), wird daraus mit Endung 0,99 → 27,99 €.

**Wie weit der Endpreis abweichen kann:** Mit Endung 0,99 liegt er höchstens 1 Cent unter dem errechneten Preis und bis knapp 1 € darüber. Je kleiner die Endung, desto weiter kann er darunter liegen: bei 0,49 bis zu 0,51 € darunter, bei sehr kleinen Endungen wie 0,01 bis knapp 1 € darunter. Mit Endung 0 wird nur aufgerundet, der Preis liegt also nie darunter. Plane das bei einem knappen Aufschlag ein.

**Wo die Rechnung gilt:** beim Listen mit dem Browser-Lister und dem CSV-Lister und beim Nachpreisen im Tracker. Es gibt **eine** Preistafel für alle Zustände ("Neu" und "Neu: Sonstige").

### 5.5 "Variable Preise (nach Preisspanne)"

**Was es macht:** Unterschiedliche Aufschläge je nach Höhe des Amazon-Preises.
**Standard:** aus.

Schaltest du den Schalter an, erscheint darunter eine Liste mit Regeln und der Knopf "Regel" (mit Pluszeichen). Jeder Klick auf "Regel" fügt eine leere Regelzeile hinzu. Eine Regelzeile sieht so aus:

"ab €" [Feld] "bis €" [Feld] "→" [Feld] "% + €" [Feld] [Haken "Neu: Sonstige"] [Knopf mit ×, "Regel entfernen"]

- **"ab €" / "bis €":** Preisspanne des **Amazon-Preises**. Beide Grenzen zählen mit dazu ("ab 10 bis 20" gilt für 10,00 € und für 20,00 €).
- **Das Feld nach "→":** Prozent-Aufschlag für diese Spanne.
- **Das Feld nach "% + €":** fester Aufschlag für diese Spanne.
- **Haken "Neu: Sonstige":** Produkte dieser Spanne werden als "Neu: Sonstige" gelistet (Abschnitt 5.6).
- **×:** entfernt die Regel sofort.

**Regeln, die du kennen musst:**
- Es zählt die **erste** passende Regel in der Liste (von oben).
- Passt **keine** Regel, gelten "% Aufschlag" und "Fester Aufschlag (€)" oben sowie der Schalter "Als „Neu: Sonstige“ listen (Standard)".
- **Leere Felder zählen als 0.** Eine frisch angelegte, leere Regel passt deshalb nur auf einen Amazon-Preis von 0 € – praktisch nie. Fülle immer "ab" **und** "bis" aus.
- Ist der Schalter "Variable Preise" aus, werden die Regeln nicht benutzt, bleiben aber gespeichert.

**Beispiel:**

| ab € | bis € | % | + € | Neu: Sonstige |
|---|---|---|---|---|
| 0 | 19,99 | 50 | 1 | aus |
| 20 | 99,99 | 30 | 0 | an |

- Amazon-Preis 12 € → erste Regel: 12 + 6 + 1 = 19 → mit Endung 0,99 → **18,99 €**, Zustand "Neu".
- Amazon-Preis 25 € → zweite Regel: 25 + 7,50 = 32,50 → **32,99 €**, Zustand "Neu: Sonstige".
- Amazon-Preis 150 € → keine Regel passt → die Werte oben in der Karte.

**Typischer Fehler – Lücken:** "bis 19,99" und "ab 20" lässt eine Lücke für Preise wie 19,995 €. Amazon-Preise haben aber nur zwei Nachkommastellen, das ist also unkritisch. Eine Lücke wie "bis 19" und "ab 20" trifft dagegen echte Preise (zum Beispiel 19,50 €) – die fallen dann auf die Werte oben zurück.

### 5.6 "Als „Neu: Sonstige“ listen (Standard)" und "NUR „Neu: Sonstige“ listen"

"Neu: Sonstige" ist ein eBay-Zustand für neue Ware, deren Verpackung zum Beispiel geöffnet wurde.

**"Als „Neu: Sonstige“ listen (Standard)"** – Standard: aus.
- **An:** Produkte werden im Zustand "Neu: Sonstige" gelistet, wenn eBay ihn in der Kategorie anbietet.
- Bietet eBay den Zustand in der Kategorie nicht an, wird ersatzweise "Neu" genommen – außer "NUR „Neu: Sonstige“ listen" ist an.
- Sind "Variable Preise" an und passt eine Regel, entscheidet **der Haken "Neu: Sonstige" in dieser Regel** – in beide Richtungen. Der Schalter hier gilt dann nur für Produkte, auf die keine Regel passt.

**"NUR „Neu: Sonstige“ listen"** – Standard: aus.
- Wirkt nur bei Produkten, die als "Neu: Sonstige" gelistet werden sollen (siehe oben).
- **An:** Bietet eBay in der Kategorie "Neu: Sonstige" nicht an, wird das Produkt **übersprungen** statt als "Neu" gelistet. Meldung im Statusbericht: "„Neu: Sonstige" in dieser Kategorie nicht verfügbar (nur-Neu-Sonstige aktiv)".
- In Bekleidungs-Kategorien heißt der entsprechende eBay-Zustand oft "Neu ohne Etikett". Den erkennt die Extension **nicht** als "Neu: Sonstige" – mit diesem Haken wird so ein Produkt dann übersprungen.
- **Zusätzlich im CSV-Lister:** Ist der Haken an, überspringt der CSV-Lister auch Produkte, deren eBay-Kategorie für "Neu: Sonstige" keine ermäßigte eBay-Gebühr hat. Die Meldung beginnt mit "keine ermäßigte eBay-Gebühr für „Neu: Sonstige"".

**Wechselwirkung:** Wird als "Neu: Sonstige" gelistet, trägt die Extension den Text aus "Zustandsbeschreibung" (Abschnitt 11.5) ein.

#### Häufige Fragen
- **"Ich hatte im Popup eigene Preise für „Neu: Sonstige“ – wo sind die?"** – Diese zweite Preistafel gibt es seit 46.0 nicht mehr. Es gilt eine Tafel für alle Zustände. Was dort eingetragen war, wird nicht mehr benutzt. Willst du für "Neu: Sonstige" andere Aufschläge, lege dafür eigene Preisspannen mit dem Haken "Neu: Sonstige" an.
- **"Warum steht mein Preis unter dem errechneten?"** – Wegen der Preisendung (Abschnitt 5.4). Mit Endung 0,99 ist das höchstens 1 Cent.
- **"Gilt der Aufschlag auch für Angebote, die schon online sind?"** – Der Tracker preist mit denselben Werten nach. Was sofort passiert, steht im Teil über den Tracker.

#### Probleme und Lösungen
- *Eine Regel greift nicht* → "ab" und "bis" ausgefüllt? Liegt der Amazon-Preis wirklich in der Spanne? Steht weiter oben eine andere Regel, die schon passt?
- *Alles wird als "Neu" gelistet, obwohl der Schalter an ist* → Passt eine Preisregel, deren Haken "Neu: Sonstige" aus ist? Oder bietet eBay den Zustand in der Kategorie nicht an?
- *Viele Produkte übersprungen mit "… nicht verfügbar (nur-Neu-Sonstige aktiv)"* → "NUR „Neu: Sonstige“ listen" ausschalten, wenn ersatzweise "Neu" in Ordnung ist.

---

## 6. Reiter Preise und Listing: Karten Listing und Artikelmerkmale

### 6.1 Karte "Listing": "Domain"

Kleiner Text: "eBay-Seite, z. B. DE = ebay.de". Zur Wahl: "Keine", "USA", "CA", "UK", "AU", "DE", "FR", "IT", "ES", "NL".

**Standardwert:** normalerweise DE (wird bei der Installation gesetzt). Prüfe nach der Installation, ob DE ausgewählt ist.

**Was davon abhängt:**
- auf welcher eBay-Seite gelistet wird (zum Beispiel DE → ebay.de),
- die **Sprache des KI-Titels**: DE → Deutsch; USA, UK, AU, CA → Englisch; FR → Französisch; IT → Italienisch; ES → Spanisch; NL → Niederländisch,
- welche Produktkennung mit "Does not apply" gefüllt wird: bei UK, DE, FR, IT, ES, NL die EAN, sonst die UPC,
- auf welcher Amazon-Seite die Produkte aus deiner Produkt-Datenbank geöffnet werden: Die Datenbank merkt sich nur die ASIN, der Link entsteht aus dieser Auswahl (DE → amazon.de, USA → amazon.com, UK → amazon.co.uk usw.; bei "Keine" amazon.de). Das gilt für den Browser-Lister, den CSV-Lister und die Links in der Produkt-Datenbank,
- auf welcher Amazon-Seite die Prüfung "Nur chinesische Verkäufer" die Verkäuferseite öffnet (DE → amazon.de usw.),
- ob die KI einen Suchbegriff für die eBay-Kategoriesuche bestimmt (nur USA, CA, UK, AU).

**Beispiel:** Du sammelst Produkte auf amazon.de, hast aber "USA" gewählt. Dann öffnet der Browser-Lister die Produkte auf amazon.com, listet auf ebay.com und schreibt den Titel auf Englisch. Für ebay.de muss hier "DE" stehen.

**"Keine" nicht wählen:** Die Extension baut die eBay-Adresse aus dieser Auswahl.
- Der CSV-Lister und das Laden deiner Angebote im Tracker brechen dann ab mit: "Keine eBay-Domain eingestellt (Einstellungen → Preise & Listing → „Domain“)."
- Der Browser-Lister öffnet dann keine gültige eBay-Seite. **Nicht sicher belegt:** welche Meldung er dann zeigt.
- Steht "Keine" da, trägt die Extension beim nächsten Update von selbst wieder ein Land ein (normalerweise DE). Ein gewähltes Land bleibt bei Updates erhalten.

**Gut zu wissen:** "Preis ab"/"Preis bis" heißen "in €", vergleichen aber nur die Zahl mit dem Amazon-Preis – auf amazon.com also mit Dollar.

### 6.2 Karte "Listing": "Listing automatisch absenden"

**Was es macht:** Ist das eBay-Formular fertig ausgefüllt, klickt die Extension selbst auf eBays Knopf zum Einstellen.
- **An (Standard):** Das Angebot wird automatisch eingestellt.
- **Aus:** Das ausgefüllte Formular bleibt offen; du prüfst es und klickst selbst.

Gilt für den Browser-Lister. Der CSV-Lister liest diesen Schalter nicht (er stellt über eine Datei bei eBay ein).

**Wechselwirkung:** Zeigt eBay eine Angebotsgebühr über 0, wird nur abgesendet, wenn "Auch mit Angebotsgebühr einstellen" an ist (Abschnitt 11.1). Sonst wird das Produkt nicht eingestellt.

**Tipp:** Zum Testen einer neuen Beschreibungsvorlage oder neuer Preise kurz ausschalten, ein Produkt listen, das Formular prüfen.

### 6.3 Karte "Listing": "Anzeigengebühr (%)"

**Was es macht:** Bietet das eBay-Formular die Option für Anzeigen (beworbene Angebote, "Promoted Listings") an, schaltet die Extension sie ein und trägt diesen Prozentsatz ein.
**Standardwert:** 2,3. **Erlaubt laut Feld:** 2 bis 99, Schritte von 0,1.

**Wichtig:** Einen Aus-Schalter für die Anzeigen gibt es hier nicht. Was eBay dafür berechnet, legt eBay fest – schau in deinem eBay-Konto nach. **Nicht sicher belegt:** was passiert, wenn du das Feld leer lässt oder einen Wert unter 2 eintippst (die Seite hält das nicht auf).

Gilt für den Browser-Lister. Der CSV-Lister liest diesen Wert nicht.

### 6.4 Hinweis in der Karte "Listing"

Unten steht: "„Preis ab“ und „Preis bis“ stehen unter **Produkt-Filter → Amazon-Filter**." Die Preisgrenzen gibt es also nur einmal, im Reiter "Produkt-Filter" (Abschnitt 8.6).

### 6.5 Karte "Artikelmerkmale (KI)"

Artikelmerkmale sind die Angaben im eBay-Formular wie Marke, Farbe, Material.

**"Pflicht-Artikelmerkmale mit KI ausfüllen"** – Standard: an.
- **An:** Die KI füllt die Artikelmerkmale im eBay-Formular aus Angaben des Amazon-Produkttexts (Abschnitt 18). Danach bekommen Pflichtmerkmale, die noch leer sind: auf USA, CA, UK, AU den KI-Suchbegriff (Abschnitt 6.1), sonst "Details In Description".
- **Aus:** Keine KI für die Merkmale. Leere Pflichtmerkmale bekommen "Details In Description". Die Spielzeug-Frage für den Warnhinweis stellt die Extension dann einzeln (Abschnitt 14.5).
- Braucht den OpenAI-Schlüssel und nutzt das gewählte "OpenAI-Modell" (Abschnitt 15).

**"Optionale Artikelmerkmale mit KI ausfüllen"** – Standard: an.
- **An:** Zusätzlich werden leere freiwillige Merkmale (die ersten paar) mit dem KI-Suchbegriff gefüllt. Diesen Suchbegriff gibt es nur auf USA, CA, UK, AU.
- Auf deutschen, französischen, italienischen, spanischen und niederländischen eBay-Seiten gibt es keinen Suchbegriff; die Extension schickt für diese Felder dann einen leeren Wert. **Nicht sicher belegt:** wie eBay damit umgeht.

Beide Schalter gelten für den Browser-Lister. Der CSV-Lister liest sie nicht.

**Ausnahme Konkurrenz-Titel:** Hat ein Produkt einen gemerkten Titel aus dem Konkurrenz-Scanner, wird dieser Titel benutzt. Dann gibt es für dieses Produkt keinen KI-Titel, keine KI-Artikelmerkmale und keinen KI-Suchbegriff.

**Nie ausgefüllt** werden Merkmale mit "Personalisierung" (alle Formen) und "Durchschnittliche Kundenbewertung" im Namen.

#### Häufige Fragen
- **"Kann ich ohne KI listen?"** – Nein, seit 46.0 nicht mehr. Der Browser-Lister hat nur noch den Knopf "Starten", der Titel kommt immer von der KI. Den OpenAI-Schlüssel brauchst du also immer (Abschnitt 15).
- **"Spart es Geld, die Merkmale auszuschalten?"** – Dann entfällt die Merkmals-Anfrage an die KI; stattdessen wird eine kleinere Spielzeug-Anfrage gestellt. **Nicht sicher belegt:** wie groß der Unterschied bei deinen Kosten ist.

#### Probleme und Lösungen
- *Produkte scheitern beim Schritt "⏰ KI erstellt die Artikelmerkmale … bitte warten …"* → Guthaben, Schlüssel und "OpenAI-Modell" prüfen (Abschnitt 15). Liegt es am Modell, zuerst zurück auf "gpt-4o-mini — Standard, günstig" stellen. Zur Not "Pflicht-Artikelmerkmale mit KI ausfüllen" ausschalten – bei einem Modell-Problem steht dann aber der Spielzeug-Warnhinweis in jeder Beschreibung (Abschnitt 15.2).
- *Viele Merkmale stehen auf "Details In Description"* → Das kommt, wenn die KI ein Pflichtfeld nicht füllen konnte oder der Schalter aus ist.

---

## 7. Reiter Produkt-Filter: Karte Beim Listen

Hinweis an der Karte: "gilt im Browser-Lister und im CSV-Lister". Diese Filter werden geprüft, **wenn das Produkt gelistet wird** (auf der Amazon-Produktseite). Fällt ein Produkt durch, wird es nicht gelistet. Für den Produkt-Grabber gelten sie nicht.

Im Browser-Lister siehst du den Stand als Zeile, zum Beispiel "Aktuell: nur FBA an · nur chinesische Verkäufer aus · GPSR aus".

### 7.1 "Nur FBA"

Kleiner Text: "Amazon muss der Versender sein".

**Was es macht:** Prüft in der **Buybox** (dem Kaufkasten auf der Amazon-Produktseite), wer das Produkt versendet. Nur wenn **Amazon** versendet (FBA), wird gelistet.
- **An (Standard):** Versendet ein anderer Händler, wird nicht gelistet. Meldung: "Nicht von Amazon versendet (Versand: …)" mit dem Namen des Versenders. Kann die Extension den Versender nicht erkennen: "Versender auf der Produktseite nicht erkennbar".
- **Aus:** keine Versandprüfung.

**Wichtig:** Dieser Schalter gilt nur beim **Listen**. Der Tracker hat eine eigene Prüfung und wird davon nicht beeinflusst.

### 7.2 "Nur chinesische Verkäufer"

Kleiner Text: "sortiert alle anderen aus".

**Was es macht:** Öffnet für jedes Produkt im Hintergrund die Verkäuferseite des Buybox-Verkäufers auf Amazon und prüft, ob dort als Land "CN" (China) oder "HK" (Hongkong) steht. Nur dann wird gelistet.
- Die Verkäuferseite wird auf der Amazon-Seite des Landes geöffnet, das unter "Domain" gewählt ist.
- Ist **Amazon selbst** der Verkäufer, gilt das Produkt als **nicht** chinesisch.
- Lässt sich kein Verkäufer erkennen oder lädt die Verkäuferseite nicht rechtzeitig, gilt das Produkt ebenfalls als **nicht** chinesisch.
- **An:** Andere Produkte werden mit "Kein chinesischer Verkäufer" abgelehnt.
- **Aus (Standard):** keine Prüfung.

**Wechselwirkungen:**
- **Verträgt sich nicht mit "Nur Verkauf durch Amazon"** (Abschnitt 8.7): Der Grabber holt dann nur Produkte, die Amazon selbst verkauft – und genau die fallen beim Listen alle mit "Kein chinesischer Verkäufer" durch. Nie beide gleichzeitig einschalten.
- Mit "Nur FBA": Beide an = Produkte von Verkäufern aus China/Hongkong, die Amazon versendet.
- Das Listen dauert länger, weil pro Produkt eine zusätzliche Seite geöffnet wird.
- Der CSV-Lister **löscht** so aussortierte Produkte aus der Produkt-Datenbank.

**Nicht sicher belegt:** ob die Prüfung auf Amazon-Seiten außerhalb Europas genauso zuverlässig funktioniert.

### 7.3 "GPSR-Angaben übernehmen"

Kleiner Text: "Produkte ohne diese Angaben werden übersprungen".

**Was GPSR ist:** Die EU-Produktsicherheitsverordnung verlangt Angaben zum **Hersteller** und zur **verantwortlichen Person in der EU**.

**Was es macht (an):**
1. Die Extension liest auf der Amazon-Produktseite die Hersteller-Angaben aus. Der Amazon-Tab kann dabei kurz in den Vordergrund seines Fensters springen.
2. Fehlen die **Hersteller**-Angaben, wird das Produkt **nicht** gelistet. Meldung: "Keine GPSR-Angaben gefunden". Die Angabe zur verantwortlichen Person in der EU ist keine Bedingung.
3. Sind die Angaben da, trägt die Extension sie in eBays GPSR-Felder ein. Klappt das nicht, hängt sie einen Kasten "EU Compliance Information" mit "Manufacturer Info:" und "Responsible Person EU:" an die Beschreibung an (fehlt die verantwortliche Person, steht dort "N/A").
4. Zusätzlich lädt sie ein Bild mit den GPSR-Angaben als weiteres Angebotsbild hoch.

**Standardwert:** aus.

**Wechselwirkungen:** Das GPSR-Bild kommt auch bei "Nur ein Bild bei eBay einstellen" dazu (Abschnitt 11.2). Der CSV-Lister löscht Produkte ohne GPSR-Angaben aus der Produkt-Datenbank.

### 7.4 "Markenlos listen" (nur CSV-Lister)

**Was es macht:**
- **An (Standard):** Der CSV-Lister trägt als Marke "Markenlos" ein. Erlaubt eBay in einer Kategorie für die Marke nur Werte aus einer Liste, nimmt er daraus einen neutralen Wert (zum Beispiel "Markenlos", "Nicht zutreffend" oder "Unbranded"). Gibt es in der Liste keinen neutralen Wert, bleibt die echte Marke stehen, damit eBay die Zeile nicht ablehnt.
- **Aus:** Die echte Marke (aus den KI-Merkmalen, sonst von Amazon, sonst "Markenlos").

Gilt nur für den CSV-Lister, nicht für den Browser-Lister.

**EAN:** Mit diesem Schalter hat die EAN nichts zu tun. Der CSV-Lister trägt – egal ob der Schalter an oder aus ist – die echte EAN aus den Amazon-Angaben ein, wenn dort genau eine gültige Nummer steht, sonst "Nicht zutreffend". **Nicht sicher belegt:** in welchen Kategorien eBay eine echte EAN verlangt – im Zweifel an einem Testprodukt prüfen.

### 7.5 "Bildabgleich gegen fremde Angebote"

Kleiner Text: "überspringt Produkte, die auf eBay schon jemand anders anbietet".

**Was es macht (Browser-Lister):** Beim Listen kommt der Browser-Lister vor dem eigentlichen Angebotsformular über eine eBay-Zwischenseite, auf der eBay passende Produkte und oft vergleichbare Angebote anderer Verkäufer zeigt. Ist der Schalter an, vergleicht die Extension das **Amazon-Bild** deines Produkts mit den Bildern dieser Angebote (bis zu 8). Ist eines **bildgleich**, bietet das Produkt schon jemand anders an – dann wird es übersprungen. Meldung im Statusbericht:
"Übersprungen: dieses Amazon-Produkt wird auf eBay bereits von jemand anderem angeboten (Bildabgleich, Abstand N)"

- Der "Abstand" sagt, wie verschieden zwei Bilder sind: 0 = praktisch identisch. Die Grenze ist seit 46.0 **fest** eingestellt und lässt sich nicht mehr ändern (das frühere Feld "Erlaubter Bildabstand" ist weg).
- Zeigt eBay keine vergleichbaren Angebote, wird ganz normal gelistet.
- Lässt sich ein Bild nicht laden oder klappt der Vergleich nicht, wird gelistet (im Zweifel lieber listen).

**Standardwert:** aus. Gilt nur für den Browser-Lister.

#### Häufige Fragen
- **"Warum werden so viele Produkte mit 'Nicht von Amazon versendet' abgelehnt?"** – "Nur FBA" ist an (Standard), und die Buybox gehört gerade einem Händler, der selbst versendet. Das ändert sich bei Amazon oft.
- **"Gelten diese Filter auch für den Grabber?"** – Nein. Sie prüfen erst beim Listen. Die Grabber-Filter stehen in der Karte "Amazon-Filter".
- **"Ist der Bildabgleich dasselbe wie die Produkt-Vergabe?"** – Nein. Die Produkt-Vergabe verhindert Doppel-Listings **unter Cash-Lister-Kunden**. Der Bildabgleich schaut auf **alle** eBay-Verkäufer, die eBay auf dieser Seite zeigt.

#### Probleme und Lösungen
- *Fast alle Produkte "Kein chinesischer Verkäufer"* → Prüfe, ob "Nur Verkauf durch Amazon" an ist (siehe 7.2).
- *Viele "Keine GPSR-Angaben gefunden"* → Viele Amazon-Seiten haben keine Hersteller-Angaben. Entweder in Kauf nehmen oder "GPSR-Angaben übernehmen" ausschalten.
- *Häufig "Versender auf der Produktseite nicht erkennbar"* → Meist ist das Produkt gerade nicht lieferbar (keine Buybox). Passiert es bei sehr vielen Produkten hintereinander, kann Amazon seine Seite umgebaut haben – dann dem Betreiber melden.

---

## 8. Reiter Produkt-Filter: Karte Amazon-Filter

Hinweis an der Karte: "jeder Filter hat seinen eigenen Schalter".

### 8.1 So funktionieren die Schalter

Jeder Filter hat **ein Zahlenfeld** und rechts daneben **einen Schalter**:
- Schalter **an** → der Filter gilt mit der Zahl im Feld.
- Schalter **aus** → der Filter gilt nicht; das Zahlenfeld ist dann ausgegraut und lässt sich nicht ändern. Zum Ändern der Zahl den Schalter kurz einschalten.

Diese Filter wirken vor allem im **Produkt-Grabber** (dem Knopf "📦 … → Datenbank" auf Amazon-Suchseiten und in Verkäufer-Schaufenstern): Produkte, die durchfallen, kommen gar nicht erst in die Produkt-Datenbank. Der Knopf zeigt dann zum Beispiel "📦 40 Produkte · 12 vom Filter ausgeschlossen → Datenbank". Fährst du mit der Maus darüber, steht im Hinweis, welcher Filter wie viele ausgeschlossen hat, zum Beispiel "• 5 × Amazon-Preis außerhalb von … (Einstellungen → Produkt-Filter → „Preis ab“ / „Preis bis“)".

**Grundregel des Grabbers:** Lässt sich eine Angabe auf der Kachel nicht lesen (kein Preis, keine Sterne, kein Lagerhinweis), wird das Produkt **nicht** ausgeschlossen. Beim Listen wird ohnehin noch einmal geprüft.

Einige Werte wirken **zusätzlich beim Listen** und sogar **im Tracker** – das steht bei jedem Filter dabei.

### 8.2 "Max. verlängerte Lieferzeit"

Kleiner Text: "in Tagen". Platzhalter "z. B. 20".

**Was es macht:** Höchstzahl an Tagen bis zur Lieferung durch Amazon.
- **Im Grabber:** Kacheln, deren normale Lieferung länger dauert, werden übersprungen. Hinweis am Knopf: "× Lieferung dauert länger als N Tage (Einstellungen → Produkt-Filter → „Max. verlängerte Lieferzeit“)".
- **Beim Listen:** Dauert die Lieferung laut Amazon-Produktseite länger, gilt das Produkt als nicht lieferbar: "Produkt ist nicht auf Lager". Steht auf der Produktseite der englische Hinweis "Extended delivery time", gilt die Lieferung ebenfalls als zu lang – egal, welche Zahl eingestellt ist.
- **Im Tracker:** Ebenso – das Produkt gilt als nicht verfügbar und wird wie ein ausverkauftes behandelt. In der Tabelle steht dann praktisch immer "Error: Artikel bei Amazon nicht verfügbar" (die Meldung "Error: Lieferzeit bei Amazon verlängert" kommt praktisch nicht vor, siehe Teil über den Tracker).
- **Öffnest du selbst eine Amazon-Produktseite**, schreibt die Extension bei zu langer Lieferzeit "WARNUNG! LIEFERZEIT VERLÄNGERT - ZUM LISTEN BESTÄTIGEN -" vorn in den Tab-Titel.

**Standardwert:** 20 Tage, Schalter an – sobald die Einstellungsseite einmal geöffnet oder eine Amazon-Produktseite aufgerufen wurde. Vorher filtert der Grabber noch nicht nach Lieferzeit; beim Listen gelten von Anfang an 20 Tage.

**Grenze im Grabber:** Der Grabber liest das Lieferdatum aus dem Kacheltext und kennt nur **deutsche und englische** Monatsnamen sowie "heute", "morgen", "übermorgen" (bzw. englisch). Auf Amazon-Seiten in anderen Sprachen kann er das Datum meist nicht lesen – dann filtert er nicht.

**Sehr wichtig – der Schalter wirkt nur im Grabber:** Beim **Listen** und im **Tracker** wird die Zahl im Feld **immer** benutzt, auch wenn der Schalter aus ist. Steht dort nichts oder 0, gelten beim Listen 20 Tage, und die 20 wird ins Feld geschrieben.
- Stellst du die Zahl sehr niedrig ein (zum Beispiel 3), kann der Tracker viele deiner laufenden Angebote als "nicht verfügbar" behandeln.
- Die Zahl also nicht zum "Ausschalten" auf 0 oder sehr klein setzen.

### 8.3 "Mind. Sterne"

Kleiner Text: "0 bis 5". Platzhalter "z. B. 4.0".

**Was es macht (nur Grabber):** Produkte mit schlechterer Sternebewertung werden nicht übernommen. Hinweis am Knopf: "× weniger als … Sterne (Einstellungen → Produkt-Filter → „Mind. Sterne“)".
- Produkte **ohne** Bewertung werden **nicht** ausgeschlossen.
- Erlaubt: 0 bis 5, Schritte von 0,1. Höhere Eingaben werden auf 5 gesetzt.
- Erkannt werden nur deutsche oder englische Angaben ("… von 5" bzw. "… out of 5"). Auf Amazon-Seiten in anderen Sprachen filtert der Grabber dann meist nicht.

**Standardwert:** 0, Schalter aus.
**Beispiel:** 4.0 → 3,8 Sterne fällt raus, 4,2 bleibt, ohne Bewertung bleibt.

### 8.4 "Mind. Bewertungen"

Platzhalter "z. B. 20".

**Was es macht (nur Grabber):** Mindestzahl an Bewertungen (wie viele Leute bewertet haben – nicht wie gut). Hinweis: "× weniger als N Bewertungen (Einstellungen → Produkt-Filter → „Mind. Bewertungen“)".
- Hat eine Kachel gar keinen Bewertungsbereich, zählt das als 0 Bewertungen.

**Standardwert:** 0, Schalter aus.
**Beispiel:** 20 → ein Produkt mit 12 Bewertungen fällt raus.
**Tipp:** "Mind. Sterne" und "Mind. Bewertungen" zusammen nutzen – 4,5 Sterne bei nur 2 Bewertungen sagen wenig.

### 8.5 "Mind. Lagerbestand"

Kleiner Text: "höchstens 20". Platzhalter "z. B. 6".

**Was es macht (nur Grabber):** Amazon zeigt bei knappem Bestand "Nur noch 5 auf Lager". Steht dort weniger als deine Zahl, wird das Produkt übersprungen. Hinweis: "× weniger als N auf Lager (Einstellungen → Produkt-Filter → „Mind. Lagerbestand“)".
- **Kein** Lagerhinweis auf der Kachel = genug Bestand → nicht ausgeschlossen.
- Höchstens 20: Amazon zeigt den Hinweis nur bei knappem Bestand. Höhere Eingaben werden auf 20 gesetzt.
- Erkannt werden nur "Nur noch N auf Lager" und "Only N left in stock". Auf Amazon-Seiten in anderen Sprachen wirkt der Filter praktisch nicht.

**Standardwert:** 0, Schalter aus.
**Beispiel:** 6 → "Nur noch 5 auf Lager" fällt raus, "Nur noch 8 auf Lager" bleibt.

### 8.6 "Preis ab" und "Preis bis"

Kleiner Text jeweils: "in €". Platzhalter "z. B. 5" bzw. "z. B. 100".

**Was es macht:** Grenzen für den **Amazon-Preis** (deinen Einkaufspreis) – nicht für deinen eBay-Preis.
- **Im Grabber:** Kacheln außerhalb der Grenzen werden nicht übernommen (der durchgestrichene Streichpreis zählt nicht). Hinweis: "× Amazon-Preis außerhalb von … (Einstellungen → Produkt-Filter → „Preis ab“ / „Preis bis“)".
- **Beim Listen:** Liegt der Amazon-Preis außerhalb, wird nicht gelistet: "Amazon-Preis zu hoch (Filter „Preis bis“)" bzw. "Amazon-Preis zu niedrig (Filter „Preis ab“)". Im CSV-Lister steht davor "Amazon: ", und das Produkt wird aus der Produkt-Datenbank gelöscht.

**Erlaubt:** ab 0, Cent-Schritte. Ein leeres Feld oder 0 bedeutet: keine Grenze.

**Standardwert bei einer neuen Installation:** beide 0, Schalter aus – also keine Preisgrenze. (Bis Version 45.x trug das Popup als Höchstpreis von selbst 100 ein. Wer von dort kommt, hat oft noch "Preis bis" 100 mit Schalter an. Willst du teurere Produkte, erhöhe den Wert oder schalte den Schalter aus.)

**Beispiel:** "Preis ab" 5, "Preis bis" 60 → 4,50 € fällt raus ("zu niedrig"), 59,99 € bleibt, 79 € fällt raus ("zu hoch").

### 8.7 "Nur Verkauf durch Amazon"

Kleiner Text: "Produkt-Grabber: übernimmt nur Produkte, die Amazon selbst verkauft und versendet".

**Was es macht:** Gilt nur auf **normalen Amazon-Suchseiten**, nicht im Verkäufer-Schaufenster. Ist der Schalter an, prüft der Grabber für jedes Produkt in kurz geöffneten Hintergrund-Tabs, wer in der Buybox verkauft. Nur Produkte mit "Verkauf und Versand durch Amazon" werden übernommen.
- Die Pillen auf den Produktbildern zeigen dann zum Beispiel "Amazon ✓", "nicht Amazon" oder "kein Angebot".
- Wie viele Tabs gleichzeitig prüfen, richtet sich nach dem Feld "Gleichzeitig" im Tracker (höchstens 10; wurde dort nie etwas eingestellt, sind es 5).

**Gleicher Schalter wie auf Amazon:** Auf der Suchseite steht über dem Grabber-Knopf der Schalter "nur Verkauf durch Amazon". Das ist **derselbe** Wert.

**Standardwert:** aus.
**Wechselwirkung:** Verträgt sich **nicht** mit "Nur chinesische Verkäufer" (Abschnitt 7.2).

#### Häufige Fragen
- **"Ich sehe auf der Amazon-Seite 48 Produkte, der Knopf zählt aber nur 30."** – Die übrigen hat ein Filter ausgeschlossen. Maus über den Knopf halten: Der Hinweis sagt, welcher.
- **"Warum werden teure Produkte nicht übernommen?"** – Vermutlich ist "Preis bis" aktiv (oft noch 100 aus einer älteren Version). Siehe 8.6.
- **"Werden schon importierte Produkte nachträglich gefiltert, wenn ich einen Filter ändere?"** – Nein. Die Grabber-Filter wirken beim Übernehmen. Beim Listen greifen danach nur die Preisgrenzen, die Lieferzeit und die Filter aus Abschnitt 7.
- **"Warum ist nach einem Umzug auf einen neuen Rechner ein Filter wieder an?"** – Die Schalter werden nicht mitgesichert (Abschnitt 16.6).

#### Probleme und Lösungen
- *Der Tracker behandelt plötzlich viele Angebote als "nicht verfügbar"* → "Max. verlängerte Lieferzeit" prüfen. Ein zu kleiner Wert wirkt im Tracker – auch bei ausgeschaltetem Schalter.
- *Alles wird mit "Amazon-Preis zu hoch (Filter „Preis bis“)" abgelehnt* → "Preis bis" zu niedrig. Wert erhöhen oder Schalter aus.
- *Filter scheinen nicht zu greifen* → Schalter rechts neben dem Zahlenfeld prüfen. Nur mit Schalter an wirkt der Filter.
- *Ich kann die Zahl nicht ändern* → Das Feld ist ausgegraut, weil der Schalter aus ist. Schalter kurz einschalten.

---

## 9. Reiter Produkt-Filter: Karte Blacklist und die eingebauten Wortfilter

### 9.1 "Meine Liste" – deine eigene Sperrliste

Die Karte "Blacklist" hat den Hinweis "eigene Liste, ein Wort oder Begriff je Zeile". Darin steht das Feld "Meine Liste" (Platzhalter "Ein Wort oder Begriff je Zeile") und darunter die Anzahl, zum Beispiel "Wörter: 42".

**Was es macht:** Enthält ein Amazon-Produkt eines deiner Sperrwörter, wird es **nicht gelistet**.
- Meldung im Statusbericht: "Produkt enthält ein Wort aus der Blacklist: <dein Eintrag>".
- Öffnest du selbst eine Amazon-Produktseite mit einem Treffer, steht vorn im Tab-Titel "⚠️ BLACKLIST-WORT GEFUNDEN: <WORT>".

**Wo gesucht wird:** im Produkttitel, im Beschreibungstext, in den Stichpunkten und in den **Werten** der Produktangaben (bei "Marke: Lego" nur "Lego", nicht die Bezeichnung "Marke").

**Wie verglichen wird:**
- Ein Eintrag pro Zeile. Auch Wortgruppen sind erlaubt.
- Groß-/Kleinschreibung egal. Einträge werden beim Speichern klein geschrieben, doppelte und leere Zeilen entfernt. Im Feld siehst du das erst nach dem Neuladen der Seite.
- Nur **ganze Wörter** zählen: "öl" trifft "Öl", aber nicht "Heizöl".
- Satzzeichen zählen nicht: "e-bike" trifft "E-Bike" und "e bike"; "kinder spielzeug" trifft auch "Kinder-Spielzeug".

**Speichern:** automatisch, kurz nach dem letzten Tastendruck.

**Wann geprüft wird:** beim **Listen** (Browser-Lister und CSV-Lister; der CSV-Lister löscht so aussortierte Produkte aus der Produkt-Datenbank). **Nicht** beim Import über den Grabber und **nicht** im Tracker – schon gelistete Angebote werden nicht nachträglich geprüft.

**Standardwert:** leer.

**Schritt für Schritt: Marke sperren**
1. Einstellungsseite öffnen, Reiter "Produkt-Filter".
2. Nach unten zur Karte "Blacklist".
3. In "Meine Liste" eine neue Zeile mit dem Markennamen schreiben, zum Beispiel `nike`.
4. Kurz warten – "Wörter:" zählt hoch. Fertig.

### 9.2 VeRO

VeRO ist eBays Programm für Rechteinhaber: Markenfirmen können Angebote mit ihren Marken löschen lassen. **Eine automatische VeRO-Prüfung gibt es nicht.** Wenn du VeRO-Marken vermeiden willst, trag die Marken selbst in deine Blacklist ein.

### 9.3 Eingebauter Wortfilter (nicht einstellbar)

Unabhängig von deiner Blacklist entfernt die Extension beim Listen **automatisch** bestimmte Begriffe aus **Titel, Beschreibung und Artikelmerkmalen** – das Produkt wird trotzdem gelistet, nur ohne diese Wörter. Die Liste ist fest eingebaut und umfasst vor allem Werbeversprechen, Prüfzeichen, Garantie- und Herkunftsangaben (zum Beispiel "Original", "Premium", "Garantie", "CE").

**So wird verglichen:**
- Groß-/Kleinschreibung ist egal.
- Es zählen nur ganze Wörter bzw. Wortgruppen: "Leder" wird aus "Geldbörse aus Leder" entfernt, "Echtleder" bleibt stehen. "Test" wird entfernt, "Testgerät" bleibt.
- Zusätzliche Regel für **"CE", "IP" und "cert"**: Entfernt wird jedes Wort, das genau so lautet oder damit beginnt und direkt danach ein Zeichen oder eine Ziffer hat – zum Beispiel "IP67", "IP-Kamera", "CE-Kennzeichen", "cert." Auch das allein stehende französische Wort "ce" fällt darunter. Diese Regel wirkt auf den ganzen Text, auch auf den HTML-Code deiner Beschreibungsvorlage (Abschnitt 14.5).

**Merkmalsfelder:** Steht ein Begriff der Liste in der **Bezeichnung** eines Merkmals (zum Beispiel ein Feld "Herstellergarantie"), wird das ganze Merkmal weggelassen. In den **Werten** der Merkmale werden die Begriffe entfernt.

Der CSV-Lister benutzt dieselbe Liste und dieselben Regeln.

- Du kannst diese Liste weder ansehen noch ändern oder abschalten.
- Ein Produkt mit solchen Wörtern wird **nicht** abgelehnt – nur die Wörter fehlen danach. Ablehnen tut nur deine eigene Blacklist.

#### Häufige Fragen
- **"Ein Wort fehlt in meinem Titel, ich habe es aber nicht gesperrt."** – Wahrscheinlich der eingebaute Wortfilter (9.3).
- **"Werden Produkte mit Blacklist-Wort aus der Datenbank gelöscht?"** – Ja. Scheitert ein Produkt im Browser-Lister (zum Beispiel wegen eines Blacklist-Worts), verlässt es die Produkt-Datenbank und steht danach nur noch mit seiner Meldung im Statusbericht. Der CSV-Lister sortiert solche Produkte ebenfalls aus und löscht sie.
- **"Entfernt der eingebaute Wortfilter auch Produkte?"** – Nein, nur Wörter.
- **"Kann ich Teilwörter sperren, z. B. alles mit 'lego'?"** – Nein, nur ganze Wörter. "lego" trifft nicht "legosteine". Trag die Varianten einzeln ein.

#### Probleme und Lösungen
- *Sperrwort greift nicht* → Steht es nur als Teil eines längeren Wortes im Text? Dann trifft es nicht. Oder es steht nur in der Bezeichnung einer Produktangabe (dort wird nicht gesucht).
- *Zu viele Produkte gesperrt* → Allgemeine Wörter (zum Beispiel "set") treffen sehr oft. Liste ausmisten.

---

## 10. Reiter eBay und Rahmenbedingungen: Karte Rahmenbedingungen

Diese Karte steht oben im Reiter "eBay & Rahmenbedingungen" und trägt den Hinweis "CSV-Lister (neuer Lister, im Test)". Seit Version 46.0 sehen alle Kunden den CSV-Lister und damit auch diese Karte.

Der CSV-Lister braucht die **Namen** deiner eBay-Rahmenbedingungen (bei eBay gespeicherte Vorlagen für Versand, Zahlung und Rücknahme) und einen Artikelstandort:

| Feld | Was hinein muss | Platzhalter |
|---|---|---|
| "Versand" | Name deiner Versand-Rahmenbedingung | "genau wie in den Rahmenbedingungen" |
| "Zahlung" | Name deiner Zahlungs-Rahmenbedingung | "genau wie in den Rahmenbedingungen" |
| "Rücknahme" | Name deiner Rücknahme-Rahmenbedingung | "genau wie in den Rahmenbedingungen" |
| "Artikelstandort (Ort oder PLZ)" | Ort oder Postleitzahl, von dem aus du verschickst | "z. B. 78315" (nur ein Beispiel) |

Über den Feldern steht: "Die Namen müssen Buchstabe für Buchstabe so lauten wie im Seller Hub. Solange einer fehlt, startet der CSV-Lister keinen Lauf."

**Schritt für Schritt:**
1. Im eBay Seller Hub deine Rahmenbedingungen öffnen und die genauen Namen ansehen.
2. Jeden Namen **exakt** abschreiben (am sichersten kopieren und einfügen) – Groß-/Kleinschreibung, Leerzeichen, Sonderzeichen genau gleich.
3. Ort oder PLZ eintragen.
4. Neben das Feld klicken oder "Speichern" drücken.
5. Im CSV-Lister "Details" öffnen: Bei "Rahmenbedingungen (Versand, Zahlung, Rücknahme)" stehen jetzt deine drei Namen (mit " · " getrennt), beim Artikelstandort dein Ort bzw. deine PLZ.

**Fehlt etwas**, zeigt der CSV-Lister oben "Fehlt noch: Rahmenbedingungen" bzw. "Fehlt noch: Artikelstandort", und beim Start erscheint: "Einstellungen fehlen: Versandbedingung, … (Einstellungen → eBay & Rahmenbedingungen)".

**Standardwerte:** alle vier Felder leer. Für den Browser-Lister spielen diese Felder keine Rolle (Abschnitt 17).

**Wenn ein Name nicht genau stimmt:** Der CSV-Lister prüft nur, ob etwas eingetragen ist. Erst eBay lehnt die Zeilen ab (Angabe des Betreibers), und abgelehnte Produkte sind danach nicht mehr in der Produkt-Datenbank. Darum den ersten Lauf mit nur 1 Produkt machen (Bereich Produktübersicht und CSV-Lister, B18). **Nicht sicher belegt:** welche Meldung eBay dazu genau zeigt.

---

## 11. Reiter eBay und Rahmenbedingungen: Karten Beim Einstellen und Neu Sonstige

### 11.1 "Auch mit Angebotsgebühr einstellen"

Kleiner Text: "automatisch absenden, auch wenn eBay Angebotsgebühren über 0 anzeigt".

**Was es macht:** Bevor ein Angebot abgeschickt wird, schaut der Browser-Lister in die Zusammenfassung unten im eBay-Formular, ob eBay dort eine **Angebotsgebühr** (Einstellgebühr) über 0 anzeigt – also einen Betrag mit €, $ oder £, der größer als 0 ist.
- **Aus (Standard):** Zeigt eBay eine Gebühr über 0, wird das Angebot **nicht** abgeschickt. Meldung im Statusbericht: "Nicht eingestellt: eBay verlangt Angebotsgebühren (Einstellung „Auch mit Angebotsgebühr einstellen“ ist aus)". Das schützt dich vor ungewollten Gebühren.
- **An:** Die Extension macht trotz Gebühr weiter.

**Wechselwirkungen:**
- Selbst abgeschickt wird nur, wenn die Gebührenprüfung bestanden ist (keine Gebühr **oder** dieser Schalter an) **und** "Listing automatisch absenden" an ist (Abschnitt 6.2).
- Ob der eBay-Tab eines so abgebrochenen Produkts offen bleibt, entscheidet "Fehler-Tabs schließen" im Browser-Lister.

**Wann einschalten?** Nur wenn du bewusst bereit bist, Angebotsgebühren zu zahlen (zum Beispiel weil dein Gratis-Kontingent bei eBay aufgebraucht ist).

**Nicht sicher belegt:** ob die Prüfung jede Form der eBay-Gebührenanzeige erkennt (sie liest nur den Gebührenbereich der Zusammenfassung), und wie der CSV-Lister mit Angebotsgebühren umgeht (dieser Schalter gilt für den Browser-Lister).

### 11.2 "Nur ein Bild bei eBay einstellen"

**Was es macht (Browser-Lister):** Normalerweise werden das Titelbild **und** die weiteren Amazon-Bilder zu eBay hochgeladen; bei Produkten mit mindestens vier Bildern kommt ein Sammelbild dazu.
- **An:** Es wird nur **ein** Bild hochgeladen – das Titelbild. Kein Sammelbild, keine weiteren Bilder.
- **Aus (Standard):** Titelbild plus weitere Bilder (und gegebenenfalls Sammelbild).

**Wechselwirkungen:**
- Ist "GPSR-Angaben übernehmen" an (Abschnitt 7.3), kommt **zusätzlich** das GPSR-Bild dazu. Dann hast du also zwei Bilder.
- Die Bilderliste in deiner Beschreibungsvorlage zeigt die zu eBay hochgeladenen Bilder – mit diesem Schalter also nur das eine (Abschnitt 14.4).

Gilt nur für den Browser-Lister, nicht für den CSV-Lister.

### 11.3 "Mehrwertsteuer im Angebot angeben"

**Was es macht:** Trägt beim Listen den Satz aus "Mehrwertsteuersatz" in das MwSt-Feld im Preisbereich des eBay-Formulars ein.
- Gibt es das Feld im eBay-Formular nicht, passiert nichts.
- **Aus (Standard):** Das Feld wird nicht angefasst.

Gilt auch für den CSV-Lister.
**Nicht sicher belegt:** bei welchen eBay-Konten das MwSt-Feld angezeigt wird (das entscheidet eBay, meist bei gewerblichen Konten).

### 11.4 "Mehrwertsteuersatz"

Feld mit "%" dahinter, Platzhalter "z. B. 19".
- **Standardwert:** 19
- Nur die Zahl eintragen, ohne Prozentzeichen (zum Beispiel 19 oder 7).
- Wirkt **nur**, wenn "Mehrwertsteuer im Angebot angeben" an ist.

### 11.5 Karte "Neu: Sonstige": Feld "Zustandsbeschreibung"

**Was es macht:** Wird ein Produkt im Zustand **"Neu: Sonstige"** eingestellt, zeigt eBay ein zusätzliches Feld für die Zustandsbeschreibung. Die Extension schreibt diesen Text hinein.

**Standardtext:**
"Neuware. Die Originalverpackung wurde ggf. zur Prüfung geöffnet. Der Artikel ist unbenutzt, vollständig und voll funktionsfähig, ohne Gebrauchsspuren."

**Regeln:**
- Höchstens **1000 Zeichen** werden übernommen; der Rest wird abgeschnitten.
- Leerzeichen am Anfang und Ende werden entfernt.
- Ist das Feld leer, trägt die Extension nichts ein.
- Bei Angeboten im Zustand "Neu" wird der Text **nicht** benutzt, weil eBay das Feld dann nicht anbietet.

**Wechselwirkung:** Ob ein Produkt als "Neu: Sonstige" gelistet wird, entscheiden die Schalter in der Karte "Preise" (Abschnitt 5.6). Gilt für den Browser-Lister und den CSV-Lister.

#### Häufige Fragen
- **"Mein Text erscheint nicht im Angebot."** – Das Angebot war wahrscheinlich im Zustand "Neu". Prüfe die "Neu: Sonstige"-Schalter und die Preisregeln (Abschnitt 5.6).
- **"Kann ich HTML benutzen?"** – Das Feld ist ein einfaches Textfeld von eBay. **Nicht sicher belegt:** wie eBay HTML dort behandelt. Schreib reinen Text.
- **"Warum werden plötzlich alle Produkte wegen Angebotsgebühren nicht eingestellt?"** – eBay zeigt bei deinen Angeboten eine Gebühr an, meist weil dein monatliches Gratis-Kontingent aufgebraucht ist. Entweder warten, Kontingent bei eBay prüfen, oder "Auch mit Angebotsgebühr einstellen" einschalten, wenn du die Gebühren zahlen willst.

---

## 12. Reiter eBay und Rahmenbedingungen: Karte Server und Produkt-Vergabe

Die Karte heißt "Server & Produkt-Vergabe" und trägt den Hinweis "verhindert doppeltes Listen".

### 12.1 Was die Produkt-Vergabe macht

Mehrere Kunden von Cash Lister sollen nicht dasselbe Amazon-Produkt auf eBay anbieten. Darum reserviert die Extension ein Produkt für dich – schon beim **Import in die Produkt-Datenbank** und noch einmal direkt **vor dem Listen**.

Was du davon siehst:
- Ein Produkt, das schon ein anderer Kunde hat, kommt **gar nicht erst** in deine Produkt-Datenbank.
- Wird es trotzdem beim Listen erkannt, steht im Statusbericht: "Produkt bereits von einem anderen Nutzer vergeben".
- Schlägt dein Listen fehl, wird die Reservierung wieder freigegeben. Klappt es, wird sie bestätigt.

Die Produkt-Vergabe läuft **nur, wenn du angemeldet bist** (Anmeldung im Dashboard). In der Karte steht dazu: "Achtung: Ohne Anmeldung ist die Produkt-Vergabe komplett aus." und "Es kommt keine Fehlermeldung – es wird dann einfach nichts mehr reserviert."

### 12.2 "Server-Adresse"

**Normalerweise ist das Feld leer** (im leeren Feld steht nur ein grauer Beispieltext). Leer heißt: Die Extension nimmt von selbst die richtige, eingebaute Adresse. Hast du eine Einrichtungsdatei vom Betreiber eingespielt, kann hier schon eine Adresse stehen – die lässt du so.

**Trag hier nur etwas ein, wenn der Betreiber dich ausdrücklich darum bittet.** Mit einer falschen Adresse funktionieren Anmeldung, Produkt-Datenbank, Produkt-Vergabe und Server-Sicherung nicht mehr. Hast du aus Versehen etwas eingetragen: Feld komplett leeren, daneben klicken.

Dasselbe Feld gibt es im Dashboard in der Anmelde-Karte unter "Server-Adresse (nur auf Ansage ändern)" (grauer Text "wird automatisch gesetzt"). Auch dort gilt: nur auf Ansage des Betreibers ändern.

### 12.3 Die Statuszeile

Neben dem Knopf "Verbindung prüfen" steht farbig, wie es gerade aussieht:
- grün: "● Produkt-Vergabe: AN (über deine Anmeldung)" – alles gut.
- rot: "● Produkt-Vergabe: AUS – keine Server-Adresse hinterlegt." – **Achtung, der Text führt in die Irre:** Diese Zeile erscheint, wenn du **nicht angemeldet** bist. Es fehlt also nicht die Adresse, sondern die Anmeldung. Lösung: im Dashboard anmelden, dann die Einstellungsseite neu laden (F5).
- rot: "● Produkt-Vergabe: AUS – nicht angemeldet. Es wird NICHTS reserviert!" – diese Zeile gibt es auch, sie kommt im aktuellen Stand aber praktisch nicht vor (statt ihrer erscheint die Zeile darüber).

### 12.4 Knopf "Verbindung prüfen"

Klick darauf testet, ob die Produkt-Vergabe wirklich funktioniert. Erst steht "prüfe …", dann eine dieser Antworten:

| Antwort | Bedeutung | Was tun |
|---|---|---|
| "OK – angemeldet als „Name“, N Produkte reserviert." | Alles in Ordnung; N ist die Zahl deiner reservierten Produkte | nichts |
| "Keine Server-Adresse hinterlegt." | Bedeutet fast immer: **du bist nicht angemeldet** (der Text ist irreführend, siehe 12.3) | Im Dashboard anmelden, Seite neu laden, erneut prüfen. Bleibt es trotz Anmeldung, an den Betreiber wenden |
| "Nicht angemeldet – bitte im Dashboard anmelden." | Keine Anmeldung (kommt praktisch nicht vor) | Im Dashboard anmelden |
| "Anmeldung abgelehnt (401) – bitte im Dashboard neu anmelden." | Deine Anmeldung gilt nicht mehr | Im Dashboard ab- und wieder anmelden. Zeigt die Anmeldung dann einen Hinweis zum Abo, liegt es am Abo (siehe Teil über Konto und Installation) |
| "Zugang ist abgeschaltet (403)." | Dein Zugang ist gesperrt | Im Dashboard nachsehen, ob dort ein Hinweis zum Abo steht; sonst an den Betreiber wenden |
| beginnt mit "Server erreichbar, kennt aber" | Problem auf der Server-Seite – du kannst nichts dagegen tun | An den Betreiber wenden |
| "Server antwortet mit HTTP …" (mit einer Zahl) | Unerwarteter Fehler des Servers | Später erneut, sonst Betreiber |
| beginnt mit "Keine Antwort:" | Server nicht erreichbar oder Internet weg (nach 15 Sekunden ohne Antwort wird abgebrochen) | Internet prüfen; die Adresse **nicht** selbst ändern, auch wenn die Meldung das nahelegt; Betreiber fragen |

Bist du angemeldet, steht nach jeder Prüfung eine zweite Zeile, die mit "Server:" beginnt. Die musst du nicht verstehen; sie hilft dem Betreiber, wenn du ihm die Meldung schickst.

### 12.5 "Beenden-CSV für Duplikate erstellen"

Kleiner Text: "wenn ein anderer Nutzer das Produkt zuerst hatte".

**Was es macht:** Gilt im **Tracker**. Sobald dort deine Angebotsliste geladen ist (über "Angebote von eBay laden" oder eine hochgeladene Datei), gleicht der Tracker deine Angebote mit der Produkt-Vergabe ab. Meldet der Server dabei, dass du ein Produkt anbietest, das ein anderer Kunde **vor dir** reserviert hatte (du warst also "der Spätere"), dann:
- **An:** Die Extension lädt eine fertige **Beenden-Datei** (CSV) herunter, mit der du diese Angebote bei eBay beenden kannst. Dazu kommt die Meldung "⚠️ N Produkt(e) bereits von einem anderen Nutzer belegt. Beenden-Datei mit M Angebot(en) heruntergeladen – bei eBay hochladen." Findet sie keine eBay-Artikelnummer dazu: "⚠️ N doppelte Produkt(e) gefunden, aber keine ItemID dazu gefunden."
- **Aus (Standard):** keine Datei und **auch keine Meldung**.

**Warum Standard aus:** Der Server meldet die Dopplungen bei **jedem** Abgleich erneut – mit Schalter an landet bei jedem Abgleich wieder dieselbe Datei in deinem Download-Ordner, bis du die Angebote beendet hast.

**Schritt für Schritt (Duplikate beenden):**
1. Schalter "Beenden-CSV für Duplikate erstellen" einschalten.
2. Tracker öffnen und "Angebote von eBay laden" klicken (oder deine Angebotsdatei wählen).
3. Erscheint die Meldung mit der Beenden-Datei: die Datei im eBay Seller Hub hochladen (Berichte → Uploads).
4. Danach den Schalter wieder ausschalten.

#### Häufige Fragen
- **"Sehe ich, welche Produkte andere Kunden haben?"** – Nein. Du merkst nur, dass ein Produkt nicht in deine Datenbank kommt oder beim Listen als "vergeben" abgelehnt wird.
- **"Wie lange bleibt ein Produkt für mich reserviert?"** – Das weiß ich nicht sicher; frag bei Bedarf den Betreiber. Gelistete Angebote werden beim Listen bestätigt, und der Abgleich im Tracker hält deine Vergaben aktuell.
- **"Muss ich die SKU meiner Angebote so lassen?"** – Ja. Die Extension erkennt deine Angebote an der SKU (Custom Label). Angebote ohne lesbare ASIN in der SKU sind beim Abgleich nicht dabei; der Tracker meldet dann: "Hinweis zur Produkt-Vergabe: … Angeboten haben keine lesbare ASIN in der SKU und waren im Abgleich NICHT dabei. Deren Reservierungen bleiben unbestätigt und laufen ab."

#### Probleme und Lösungen
- *Status rot "AUS – keine Server-Adresse hinterlegt."* → Du bist sehr wahrscheinlich nicht angemeldet. Im Dashboard anmelden, dann die Einstellungsseite neu laden (F5).
- *Status bleibt rot, obwohl ich angemeldet bin* → Einstellungsseite neu laden. Bleibt es rot: im Dashboard ab- und neu anmelden. Steht im Feld "Server-Adresse" etwas, das dir der Betreiber nicht gegeben hat: Feld leeren, daneben klicken, Seite neu laden.
- *Viele Produkte kommen nicht in die Datenbank* → Sie sind vermutlich schon an andere Kunden vergeben. Das ist gewollt.

---

## 13. Reiter eBay und Rahmenbedingungen: Karte Server-Modus

Die Karte heißt "Server-Modus" mit dem Hinweis "z. B. ein gemieteter Server". Sie ist neu in 46.0.

**Wofür:** Manche Kunden lassen Tracker und Browser-Lister auf einem eigenen Gerät laufen, zum Beispiel einem gemieteten Windows-Server mit Chrome. Mit dem Server-Modus siehst du im Dashboard deiner **anderen** Geräte (gleiches Konto), was auf diesem Gerät läuft.

### 13.1 "Dieses Gerät ist ein Server"

Kleiner Text: "meldet etwa jede Minute seinen Stand · nur mit Anmeldung".
- **An:** Dieses Gerät meldet regelmäßig seinen Stand. Das Dashboard auf deinen anderen Geräten zeigt dann, was hier läuft (Tracker, Browser-Lister, heute gelistet).
- **Aus (Standard):** keine Meldung.
- Funktioniert nur, wenn du auf diesem Gerät angemeldet bist.

### 13.2 "Gerätename"

Platzhalter "z. B. Server-1". Unter diesem Namen erscheint das Gerät im Dashboard der anderen Geräte.
- **Standard:** "Server". Lässt du das Feld leer, wird "Server" gespeichert und angezeigt.
- Höchstens 40 Zeichen; mehrfache Leerzeichen werden zu einem.
- Ausschalten lässt den Namen stehen.

Unter den Feldern steht: "Das Dashboard auf deinen anderen Geräten zeigt dann, was hier läuft (Tracker, Browser-Lister, heute gelistet). Gilt nur für dieses Gerät."

**Wichtig:** Schalter und Gerätename gelten **nur für dieses Gerät**. Sie stehen weder in der Export-Datei noch in der Server-Sicherung. So wird ein zweites Gerät nicht versehentlich selbst zum "Server", wenn du dort Einstellungen einspielst.

**Schritt für Schritt:**
1. Auf dem Server-Gerät: Chrome öffnen, im Dashboard anmelden.
2. Einstellungen → Reiter "eBay & Rahmenbedingungen" → Karte "Server-Modus".
3. "Dieses Gerät ist ein Server" einschalten.
4. Bei "Gerätename" einen erkennbaren Namen eintragen (zum Beispiel "Server-1") und daneben klicken.
5. Auf deinem normalen Rechner das Dashboard öffnen: Nach kurzer Zeit erscheint dort der Stand des Server-Geräts.

**Nicht sicher belegt:** wie lange das Dashboard ein Gerät noch anzeigt, das sich nicht mehr meldet – bei Fragen den Betreiber fragen.

---

## 14. Reiter Beschreibungsvorlage

Die Karte heißt "Beschreibungsvorlage (HTML)" mit dem Hinweis "leer lassen = schlichte Beschreibung aus dem Produkttext". Hier legst du fest, wie die **Artikelbeschreibung** deiner eBay-Angebote aussieht. Die Beschreibung entsteht **ohne KI**: aus deiner Vorlage und den Daten der Amazon-Produktseite.

### 14.1 Leer lassen oder eigene Vorlage?

- **Feld leer (Standard bei neuer Installation):** Die Extension baut eine **schlichte Beschreibung**: der Titel fett, darunter die Stichpunkte als Liste, darunter der Beschreibungstext von Amazon. Ohne Farben, ohne Kästen, ohne Bilder, ohne Überschriften – dadurch passt sie in jedem eBay-Land.
- **Eigene Vorlage eingetragen:** Die Extension nimmt deine Vorlage und ersetzt die Platzhalter durch die Produktdaten.

Ein Feld, das nur Leerzeichen enthält, zählt als leer.

### 14.2 Die Platzhalter

Die Erklärzeile über dem Feld nennt sie: "Platzhalter: _TITLE_, _ORIGINAL_TITLE_, _MAIN_IMAGE_, _FEATURES_CONTENT_, _DESCRIPTION_CONTENT_, _SECTIONS_CONTENT_ / Bilderliste: _BEGIN_IMAGE_LIST_ / _BEGIN_IMAGE_ITEM_ / _IMAGE_URL_ / _END_IMAGE_ITEM_ / _END_IMAGE_LIST_ / Bereiche: _BEGIN_x_SECTION_ … _END_x_SECTION_"

| Platzhalter | Wo er funktioniert |
|---|---|
| `_TITLE_`, `_ORIGINAL_TITLE_`, `_MAIN_IMAGE_` | überall in der Vorlage |
| `_FEATURES_CONTENT_` | **nur** innerhalb von `_BEGIN_FEATURES_SECTION_ … _END_FEATURES_SECTION_` |
| `_DESCRIPTION_CONTENT_` | **nur** innerhalb von `_BEGIN_DESCRIPTION_SECTION_ … _END_DESCRIPTION_SECTION_` |
| `_IMAGE_URL_` | **nur** innerhalb von `_BEGIN_IMAGE_LIST_ … _END_IMAGE_LIST_` (siehe 14.4) |
| `_SPIELZEUG_WARNUNG_` | überall in der Vorlage |

**Wichtig:** Schreibst du `_FEATURES_CONTENT_` oder `_DESCRIPTION_CONTENT_` **ohne** den passenden Bereich drumherum, wird der Platzhalter **nicht** ersetzt und steht wörtlich im Angebot.

| Platzhalter | Wird ersetzt durch |
|---|---|
| `_TITLE_` | den Titel deines eBay-Angebots (KI-Titel oder Konkurrenz-Titel) |
| `_ORIGINAL_TITLE_` | den ursprünglichen Titel von der Amazon-Seite |
| `_MAIN_IMAGE_` | die Adresse des ersten Bildes, das für das Angebot zu eBay hochgeladen wurde |
| `_FEATURES_CONTENT_` | die Stichpunkte ("Über diesen Artikel") von Amazon als Aufzählungsliste |
| `_DESCRIPTION_CONTENT_` | den Beschreibungstext von der Amazon-Seite |
| `_SECTIONS_CONTENT_` | nichts – siehe Hinweis unten |
| `_SPIELZEUG_WARNUNG_` | (steht nicht in der Erklärzeile, funktioniert aber) die Stelle für den Spielzeug-Warnhinweis – siehe 14.5 |

**Hinweis zu _SECTIONS_CONTENT_:** Dieser Platzhalter steht in der Erklärzeile, bekommt aber **nie** einen Inhalt. Ein Bereich `_BEGIN_SECTIONS_SECTION_ … _END_SECTIONS_SECTION_` fällt deshalb immer komplett weg. Dasselbe gilt für `_TABLE_CONTENT_` (Bereich `_BEGIN_TABLE_SECTION_ … _END_TABLE_SECTION_`). Wenn du dir die Produktangaben-Tabelle von Amazon in der Beschreibung wünschst, ist das ein Wunsch an den Betreiber.

### 14.3 Bereiche, die verschwinden, wenn nichts da ist

Ein "Bereich" ist ein Stück Vorlage zwischen `_BEGIN_x_SECTION_` und `_END_x_SECTION_`. Für `x` gibt es: `FEATURES`, `DESCRIPTION`, `SECTIONS`, `TABLE`.
- Hat das Produkt Inhalt für diesen Teil, bleibt der Bereich stehen und der Platzhalter wird ersetzt.
- Hat es keinen Inhalt, **verschwindet der ganze Bereich** – samt deiner Überschrift darin.

**Beispiel:**
```html
<h2>_TITLE_</h2>
_BEGIN_FEATURES_SECTION_
<h3>Highlights</h3>
_FEATURES_CONTENT_
_END_FEATURES_SECTION_
_BEGIN_DESCRIPTION_SECTION_
<h3>Beschreibung</h3>
<div>_DESCRIPTION_CONTENT_</div>
_END_DESCRIPTION_SECTION_
_SPIELZEUG_WARNUNG_
```
Hat ein Produkt keine Stichpunkte, fehlt im fertigen Angebot der ganze Block "Highlights".

### 14.4 Die Bilderliste

Mit diesem Aufbau wiederholst du ein Stück HTML für **jedes** Bild, das zu eBay hochgeladen wurde:
```html
_BEGIN_IMAGE_LIST_
<div class="galerie">
  _BEGIN_IMAGE_ITEM_<img src="_IMAGE_URL_" style="max-width:100%">_END_IMAGE_ITEM_
</div>
_END_IMAGE_LIST_
```
- Alles zwischen `_BEGIN_IMAGE_ITEM_` und `_END_IMAGE_ITEM_` wird pro Bild einmal eingesetzt, `_IMAGE_URL_` jeweils durch die Bildadresse ersetzt.
- Gibt es keine Bilder, verschwindet die ganze Liste.
- Beim Browser-Lister sind die Bildadressen die Bilder auf eBay (nicht die Amazon-Bilder).
- `_IMAGE_URL_` außerhalb dieser Liste wird nicht ersetzt.
- Mit "Nur ein Bild bei eBay einstellen" ist das nur ein Bild (Abschnitt 11.2).

### 14.5 Was immer automatisch dazukommt

1. **Spielzeug-Warnhinweis.** Vorgeschrieben bei Spielzeug. Die Extension fragt dazu die KI, ob das Produkt ein Spielzeug ist (meist zusammen mit den Artikelmerkmalen, sonst einzeln). Der Hinweis besteht aus drei fett gedruckten Zeilen, die mit "Achtung: Nicht für Kinder unter 36 Monaten geeignet" beginnen.
   - Steht `_SPIELZEUG_WARNUNG_` in deiner Vorlage, kommt der Hinweis genau dorthin (bei Nicht-Spielzeug verschwindet der Platzhalter spurlos).
   - Steht er nicht drin, wird der Hinweis **unten angehängt**.
   - **Im Zweifel wird gewarnt.** Nur wenn die KI ausdrücklich "kein Spielzeug" antwortet, entfällt der Hinweis. Antwortet die KI nicht oder fehlt ein gültiger Schlüssel, steht der Hinweis in der Beschreibung.
   - Ausschalten lässt sich der Hinweis nicht.
2. **GPSR-Angaben** (nur mit "GPSR-Angaben übernehmen", Browser-Lister): Kann die Extension die Hersteller-Angaben nicht in eBays eigene Felder eintragen, hängt sie den Kasten "EU Compliance Information" an. Lange Ziffernfolgen und E-Mail-Adressen werden daraus entfernt.
3. **Eingebauter Wortfilter:** Bestimmte Werbe- und Prüfzeichen-Begriffe werden aus dem Text entfernt (Abschnitt 9.3). **Achtung:** Die Regel für Wörter, die mit "CE", "IP" oder "cert" beginnen, wirkt auf den **ganzen** Text samt HTML-Code. Benutze in deiner Vorlage deshalb keine Klassennamen, Bildadressen oder sonstigen Code-Teile, die mit "ce", "ip" oder "cert" beginnen und direkt danach ein Zeichen wie "-", "_" oder eine Ziffer haben (zum Beispiel `class="ce-box"`) – solche Teile können herausgeschnitten werden.

### 14.6 Wenn am Ende nichts übrig bleibt

Ist die fertige Beschreibung leer (zum Beispiel weil die Vorlage nur aus Bereichen besteht, die alle leer waren), bricht der Browser-Lister dieses Produkt ab, damit kein Angebot ohne Beschreibung online geht. Im Statusbericht steht dann:
"Beschreibung konnte nicht in den eBay-Editor geschrieben werden: Beschreibungs-Vorlage ist leer (nach Wortfilter nichts uebrig). - Listing abgebrochen, damit es nicht leer online geht."

### 14.7 Schritt für Schritt: eigene Vorlage einrichten

1. Einstellungsseite öffnen, Reiter "Beschreibungsvorlage".
2. Deinen HTML-Code in das große Feld einfügen (Platzhaltertext: "HTML-Code der Beschreibungsvorlage hier einfügen").
3. Platzhalter an die gewünschten Stellen setzen (Tabelle 14.2).
4. Neben das Feld klicken oder "Speichern" drücken.
5. Im Reiter "Preise & Listing" kurz "Listing automatisch absenden" ausschalten, ein Testprodukt listen und die Beschreibung im eBay-Formular prüfen. Danach wieder einschalten.

**Zurück zur schlichten Beschreibung:** Feld komplett leeren, daneben klicken. Fertig.

### 14.8 Größe der Vorlage

Die Einstellungen werden auf dem Server gesichert (Abschnitt 16). Wird alles zusammen zu groß, zeigt der Reiter "Sicherung": "Aktueller Stand zu groß für die Sicherung (… KB, erlaubt 512 KB) – Vorlagen oder Bild-Templates kürzen." Das Dashboard meldet dann "Einstellungen zu groß für die Sicherung". Sehr lange Vorlagen (zum Beispiel mit eingebetteten Bildern als Text) sind der häufigste Grund. Verlinke Bilder lieber, statt sie einzubetten.

#### Häufige Fragen
- **"Wird die Beschreibung von der KI geschrieben?"** – Nein. Sie entsteht aus deiner Vorlage (oder der schlichten Beschreibung) und den Amazon-Daten. Die KI wird nur für die Spielzeug-Frage benutzt.
- **"Gilt die Vorlage auch für den CSV-Lister?"** – Ja, nach denselben Regeln.
- **"Kann ich eine fertige Vorlage vom Betreiber bekommen?"** – Eine mitgelieferte Standardvorlage gibt es nicht. Frag den Betreiber, ob er eine anbietet.
- **"Warum fehlen Wörter wie 'Original' oder 'Premium' in meiner Beschreibung?"** – Der eingebaute Wortfilter entfernt sie (Abschnitt 9.3).
- **"In meinem Feld steht eine Standardvorlage, die ich nie eingetragen habe."** – Die hat eine ältere Version (45.4) automatisch eingetragen. Sie bleibt und wird benutzt. Willst du die schlichte Beschreibung, leere das Feld.

#### Probleme und Lösungen
- *Platzhalter steht wörtlich im Angebot (z. B. "_TITEL_")* → Tippfehler. Die Platzhalter müssen genau so geschrieben sein wie in der Tabelle, mit Unterstrichen und Großbuchstaben (`_TITLE_`, nicht `_TITEL_`).
- *"_FEATURES_CONTENT_" oder "_DESCRIPTION_CONTENT_" steht wörtlich im Angebot* → Der Platzhalter steht nicht innerhalb seines Bereichs (siehe 14.2 und 14.3).
- *Ein Teil deines HTML-Codes fehlt oder die Gestaltung ist kaputt* → Prüfe, ob in der Vorlage etwas mit "ce", "ip" oder "cert" beginnt und direkt ein Zeichen oder eine Ziffer folgt (14.5 Punkt 3). Umbenennen.
- *Überschrift fehlt bei manchen Produkten* → Sie steht in einem Bereich, und das Produkt hatte dafür keinen Inhalt. Das ist gewollt.
- *Spielzeug-Hinweis bei einer Bohrmaschine* → Wenn die KI nicht antwortet oder der Schlüssel ungültig ist, wird immer gewarnt. Schlüssel und Guthaben prüfen (Abschnitt 15).
- *Bilder in der Beschreibung fehlen* → Nur zu eBay hochgeladene Bilder erscheinen. Prüfe "Nur ein Bild bei eBay einstellen".

---

## 15. Reiter KI: OpenAI-Schlüssel und Modell

Die Karte heißt "KI (OpenAI)". Cash Lister nutzt die KI von OpenAI – mit **deinem eigenen** OpenAI-Schlüssel. Die Kosten rechnet OpenAI direkt mit dir ab.

### 15.1 "OpenAI-API-Schlüssel (für die Titel-Generierung)"

**Was es ist:** Dein persönlicher Zugangsschlüssel zu OpenAI. Er beginnt meist mit `sk-` (so steht es auch als Platzhalter im Feld). Das Feld zeigt nur Punkte, damit niemand mitlesen kann.

**Seit 46.0 brauchst du ihn für jedes Listing**, denn der Titel kommt immer von der KI (es gibt kein "Ohne KI starten" mehr).

| Funktion | Braucht den Schlüssel? | Was passiert ohne gültigen Schlüssel? |
|---|---|---|
| KI-Titel (Browser-Lister und CSV-Lister, bei jedem Produkt) | ja | Nach mehreren Versuchen (rund eine Minute je Produkt) scheitert das Produkt mit "KI-Titel ist leer". Im Browser-Lister verlässt ein gescheitertes Produkt die Produkt-Datenbank; der CSV-Lister stellt es zurück. |
| Artikelmerkmale per KI ("Pflicht-Artikelmerkmale mit KI ausfüllen") | ja | Ohne Schlüssel kommt das Listen gar nicht bis hierher (scheitert am Titel). Scheitert die KI genau bei diesem Schritt (zum Beispiel Guthaben gerade aufgebraucht, zu viele Anfragen, oder OpenAI lehnt das gewählte Modell ab), wird das Produkt **nicht** eingestellt. Die Meldung beginnt mit "Nicht eingestellt: Fehler beim Ausfüllen des eBay-Formulars" und nennt den Schritt "⏰ KI erstellt die Artikelmerkmale … bitte warten …". |
| Spielzeug-Frage für den Warnhinweis | ja, bei jedem Listen | Der Warnhinweis steht in der Beschreibung (Abschnitt 14.5). |
| Suchbegriff für die eBay-Kategoriesuche (nur USA, CA, UK, AU) | ja | Ohne Schlüssel kommt das Listen nicht bis hierher. **Nicht sicher belegt:** welche Meldung im Statusbericht steht, wenn die KI genau bei diesem Schritt scheitert. |
| CSV-Lister: Artikelmerkmale und Spielzeug-Frage | ja | Meldungen, die mit "KI-Schnittstelle" beginnen; je nach Fehler wird das Produkt zurückgestellt oder der Lauf angehalten. |

**Ausnahme Konkurrenz-Titel:** Ist für ein Produkt aus dem Konkurrenz-Scanner der Titel des eBay-Verkäufers gemerkt, nimmt der Browser-Lister diesen Titel. Dann gibt es keinen KI-Titel, keine KI-Artikelmerkmale und keine KI-Kategoriesuche für dieses Produkt. Die Spielzeug-Frage läuft trotzdem.

**Woher bekomme ich einen Schlüssel?** Bei OpenAI unter platform.openai.com (dort auch Guthaben aufladen unter "Billing"). Das Konto bei OpenAI brauchst du selbst.

**Schritt für Schritt eintragen:**
1. Einstellungsseite öffnen, Reiter "KI".
2. In "OpenAI-API-Schlüssel (für die Titel-Generierung)" den Schlüssel einfügen (Strg+V).
3. Neben das Feld klicken oder "Speichern" drücken.
4. Ein Testprodukt listen (am besten mit "Listing automatisch absenden" aus) und prüfen, ob ein KI-Titel entsteht.

**Sicherheit:**
- Der Schlüssel bleibt in Chrome auf deinem Rechner, wird nur für die Anfragen an OpenAI benutzt und **nie** auf den Cash-Lister-Server gesichert.
- Er steht aber in der **Export-Datei** (Abschnitt 16.1). Gib diese Datei deshalb niemandem weiter.
- Nach einer Neuinstallation oder auf einem neuen Rechner musst du den Schlüssel neu eintragen – außer du spielst deine eigene Export-Datei ein.

### 15.2 "OpenAI-Modell (für KI-Beschreibung & Generierung)"

Auswahlliste:
- "gpt-4o-mini — Standard, günstig" (**Standard**)
- "gpt-4.1-mini"
- "gpt-4.1-nano — sehr günstig"
- "gpt-4o — stärker"
- "gpt-4.1 — stärker"

**Wofür die Auswahl wirklich gilt:** für die Artikelmerkmale per KI, die Spielzeug-Frage, den Suchbegriff für die Kategoriesuche und die KI-Schritte des CSV-Listers.
**Wofür sie nicht gilt:** Der **KI-Titel** wird immer mit gpt-4o-mini erzeugt, egal was hier steht. Und die **Beschreibung** entsteht gar nicht per KI (Abschnitt 14) – die Beschriftung "für KI-Beschreibung" ist älter als der heutige Stand.

**Wichtige Wechselwirkung:** Weil der KI-Titel immer gpt-4o-mini nimmt, die übrigen KI-Schritte aber das hier gewählte Modell, kann Folgendes passieren: Du wählst ein Modell, das OpenAI für dein Konto ablehnt. Dann klappt der KI-Titel weiter, aber mit "Pflicht-Artikelmerkmale mit KI ausfüllen" scheitert jedes Produkt beim Schritt "⏰ KI erstellt die Artikelmerkmale … bitte warten …" und wird nicht eingestellt. Auf USA, CA, UK und AU kann es schon vorher beim Suchbegriff für die Kategoriesuche hängen bleiben (**Nicht sicher belegt:** mit welcher Meldung). Schaltest du die Pflicht-Artikelmerkmale aus, scheitert die Spielzeug-Frage ebenso – dann steht der Spielzeug-Warnhinweis in jeder Beschreibung. Lösung in jedem Fall: zurück auf "gpt-4o-mini — Standard, günstig".

**Empfehlung:** Beim Standard bleiben. Laut Beschriftung sind die "stärker"-Modelle teurer und "gpt-4.1-nano" sehr günstig. **Nicht sicher belegt:** wie groß der Unterschied in Qualität und Kosten bei dir ausfällt – das hängt von OpenAIs aktuellen Preisen ab.

### 15.3 Fehlermeldungen der KI

Diese Meldungen können im Statusbericht des Browser-Listers (Spalte "Meldung") oder im CSV-Lister stehen:

| Meldung | Bedeutung | Was tun |
|---|---|---|
| "OpenAI: API-Key ungültig oder abgelaufen – bitte prüfen (Einstellungen → KI → „OpenAI-API-Schlüssel“)." | Schlüssel falsch, gelöscht oder abgelaufen | Schlüssel bei OpenAI prüfen, neu einfügen |
| "OpenAI-Guthaben leer: kein Guthaben mehr auf dem OpenAI-Konto. Bitte unter platform.openai.com unter Billing Guthaben aufladen." | Kein Guthaben | Bei OpenAI Guthaben aufladen |
| "OpenAI: Rate-Limit (zu viele Anfragen) – kurz warten und erneut versuchen." | Zu viele Anfragen auf einmal | Kurz warten; weniger gleichzeitig listen |
| "OpenAI hat innerhalb von 90 Sekunden nicht geantwortet." | OpenAI überlastet | Später erneut |
| "OpenAI nicht erreichbar: …" | Internet- oder OpenAI-Problem | Internet prüfen, später erneut |
| "Kein OpenAI API Key gesetzt (Options-Seite)." | Feld ist leer | Schlüssel im Reiter "KI" eintragen |
| beginnt mit "OpenAI" und einer dreistelligen Zahl, danach englischer Text von OpenAI | sonstiger Fehler von OpenAI (zum Beispiel ein Modell, das dein Konto nicht nutzen darf) | Modell auf "gpt-4o-mini — Standard, günstig" stellen; bleibt es, den Text an den Betreiber schicken |
| "OpenAI: keine verwertbare Antwort (kein Function-Call) – evtl. Content-Filter beim Produkttext." | OpenAI hat zu diesem Produkt keine brauchbare Antwort gegeben, oft wegen des Produkttexts | betrifft meist nur einzelne Produkte |
| "KI-Titel ist leer" | Es kam kein KI-Titel zustande – sehr oft fehlender/ungültiger Schlüssel oder kein Guthaben | Schlüssel und Guthaben prüfen |
| "Titel-Erstellung fehlgeschlagen" | Im Titel kam die Buchstabenfolge "error" vor (Groß-/Kleinschreibung egal) – zum Beispiel, weil eine Fehlermeldung statt eines Titels zurückkam. Auch ein Titel, in dem "Error" wirklich vorkommt, löst das aus | Schlüssel und Guthaben prüfen, später erneut |
| beginnt mit "Nicht eingestellt: Fehler beim Ausfüllen des eBay-Formulars (Schritt „⏰ KI erstellt die Artikelmerkmale … bitte warten …")" | Die KI-Artikelmerkmale sind gescheitert | Guthaben, Schlüssel und Modellwahl prüfen; zur Not "Pflicht-Artikelmerkmale mit KI ausfüllen" ausschalten |
| "Listen fehlgeschlagen – keine verwertbare Antwort der Amazon-Seite" | Allgemeiner Fehlschlag; stand kurz vorher ein KI-Fehler fest, wird stattdessen dieser angezeigt | Siehe Zeilen oben |

#### Häufige Fragen
- **"Brauche ich unbedingt einen OpenAI-Schlüssel?"** – Ja. Seit 46.0 kommt jeder Titel von der KI.
- **"Zahlt der Betreiber die KI?"** – Nein, die Anfragen laufen über deinen eigenen Schlüssel.
- **"Kann ich den Titel-Text (Prompt) selbst bestimmen?"** – Nein. Ein Feld dafür gibt es nicht.

#### Probleme und Lösungen
- *Alle Produkte scheitern mit "KI-Titel ist leer"* → Schlüssel fehlt, ist ungültig, oder kein Guthaben. Vor dem nächsten Start prüfen – sonst verlassen weitere Produkte die Produkt-Datenbank.
- *Zwei Rechner, ein Schlüssel, viele "Rate-Limit"-Meldungen* → Beide teilen sich die Grenze bei OpenAI. Weniger gleichzeitig listen oder nacheinander arbeiten.

---

## 16. Reiter Sicherung: Datei und Server

Es gibt zwei Arten der Sicherung: die **Export-Datei** (machst du selbst, Karte "Als Datei") und die **Server-Sicherung** (läuft automatisch, wenn du angemeldet bist, Karte "Auf dem Server").

### 16.1 Karte "Als Datei": "Einstellungen exportieren"

Hinweis an der Karte: "z. B. für einen Rechnerwechsel". Darunter eine Warnung: "Enthält API-Schlüssel und Lizenz – nicht weitergeben." Dieselbe Warnung erscheint beim Drüberfahren über den Knopf.

**Was passiert:** Chrome lädt eine Datei herunter, die "einstellungen-privat-<Datum>.json" heißt (zum Beispiel einstellungen-privat-2026-10-26.json).

**Was drin ist:**
- die Einstellungen von dieser Seite und aus Browser-Lister, Tracker (auch die Adressen deiner Google-Tabellen, falls eingerichtet), Verkaufs-Übersicht, Konkurrenz-Scanner und CSV-Lister, die Blacklist, die Beschreibungsvorlage,
- dein **Anmeldename** (nicht das Passwort),
- deine **Schlüssel** (zum Beispiel den OpenAI-Schlüssel),
- die gemerkten Konkurrenten.

**Was nicht drin ist:**
- dein Passwort und deine Anmeldung selbst (nach dem Einspielen musst du dich neu anmelden),
- die **Produkt-Datenbank** – sie liegt seit 46.0 für dein Konto auf dem Server. (Der Hinweistext in der Karte, "Der Export enthält alle Einstellungen, die Schlüssel und die Produkt-Datenbank", ist in diesem Punkt älter als der heutige Stand.)
- "Mind. Sterne", "Mind. Bewertungen", "Mind. Lagerbestand" und alle Schalter der Amazon-Filter (siehe 16.6),
- der Server-Modus (Abschnitt 13),
- Statusbericht, Zähler, laufende Vorgänge.

**Gib die Datei niemandem weiter** – sie enthält deinen OpenAI-Schlüssel und, falls eingerichtet, die Adressen deiner Google-Tabellen.

### 16.2 Karte "Als Datei": "Einstellungen importieren"

1. "Einstellungen importieren" klicken.
2. Die .json-Datei auswählen.
3. Meldung: "Einstellungen importiert (N Einträge). Lade offene Seiten von Cash Lister (z. B. den Tracker) bitte neu."
4. Offene Seiten von Cash Lister neu laden, auch die Einstellungsseite selbst (F5).

Fehlermeldungen: "Ungültige Einstellungsdatei." und "Die Datei ist kein gültiges JSON." (falsche Datei gewählt), "Import fehlgeschlagen: …".

**Beim Import werden alle Werte aus der Datei übernommen; Einstellungen, die nicht in der Datei stehen, bleiben, wie sie sind.**

**Ältere Export-Dateien** (vor 46.0) enthalten noch deine Produkt-Datenbank. Spielst du so eine Datei ein, lädt die Extension diese Produkte in deine Produkt-Datenbank auf dem Server – sofern du angemeldet bist, beim nächsten Anlass (zum Beispiel nach der Anmeldung, beim Öffnen der Produkt-Datenbank oder beim nächsten Chrome-Start). Schon gelistete Produkte werden dabei aussortiert, doppelte kommen nicht zweimal hinein.

### 16.3 Datei vor der Anmeldung einspielen (im Dashboard)

Bist du noch nicht angemeldet (zum Beispiel auf einem neuen Rechner), gibt es im Dashboard in der Anmelde-Karte rechts den Bereich "Einrichtungsdatei" mit dem Knopf "Einrichtungsdatei einlesen".
- Ist es eine **Einrichtungsdatei vom Betreiber**, meldet sich die Extension damit gleich an: "N Einstellungen übernommen – melde an …". Behandle so eine Datei wie dein Passwort und gib sie niemandem weiter.
- Ist es deine **eigene Export-Datei**, steht: "N Einstellungen übernommen. Die Datei enthielt keine Zugangsdaten – bitte von Hand anmelden." Dann normal mit "Benutzername" und "Passwort" anmelden.

Fehlermeldungen dort: "Die Datei ist kein gültiges JSON.", "Das ist keine Einstellungsdatei.", "Import fehlgeschlagen: …".

### 16.4 Karte "Auf dem Server": automatische Sicherung

Hinweis an der Karte: "für dein Konto · nur mit Anmeldung". Darunter: "Mit Anmeldung werden deine Einstellungen von selbst auf dem Server gesichert – ohne Schlüssel und Produkt-Datenbank."

**So läuft es:** Wenn du angemeldet bist, sichert die Extension deine Einstellungen etwa eine halbe Minute nach deiner letzten Änderung. Ist der Server gerade nicht erreichbar, versucht sie es später noch einmal und bei jedem Chrome-Start.

**Auf dem Server liegen NICHT:** deine Schlüssel (OpenAI usw.), die Werte aus 16.6, der Server-Modus und die gemerkten Konkurrenten (die stehen nur in der Export-Datei). Die Produkt-Datenbank liegt zwar auch auf dem Server, gehört aber nicht zur Einstellungs-Sicherung.

**Kein laufender Abgleich zwischen Geräten:** Die Sicherung ist eine Kopie für den Notfall, kein Abgleich. Ändert sich etwas auf Gerät A, landet das in der Sicherung – auf Gerät B kommt es aber **nicht** von selbst an. Von selbst geholt wird die Sicherung nur nach einer Neuinstallation (oder wenn auf dem Gerät noch fast nichts eingestellt ist), und zwar beim Anmelden. Sonst holst du sie mit "Einstellungen vom Server holen" (16.5).

**Statuszeile unten in der Karte:**
- "Auf dem Server gesichert: <Datum Uhrzeit>"
- "Noch nicht auf dem Server gesichert."
- "… · Vom Server übernommen: <Datum Uhrzeit>" (einmal nach einer Wiederherstellung)
- "… · Aktueller Stand zu groß für die Sicherung (… KB, erlaubt 512 KB) – Vorlagen oder Bild-Templates kürzen." → Deine Einstellungen (meist die Beschreibungsvorlage) sind zu groß; kürzen (Abschnitt 14.8).
- leer → du bist nicht angemeldet.

Auch das **Dashboard** zeigt den Stand: In der Liste für heute steht der Punkt "Einstellungen gesichert" (zum Beispiel "Zuletzt … auf dem Server", "Noch nicht gesichert", "Server nicht erreicht – wird wiederholt" oder "Erst nach der Anmeldung").

**Nach einer Neuinstallation** (Extension entfernt und neu geladen, neuer Rechner, neues Chrome-Profil) holt die Extension die Sicherung nach dem Anmelden **automatisch** zurück.

### 16.5 "Einstellungen vom Server holen" und "Dieses Gerät auf den Server sichern"

Unter den Knöpfen steht: "„Einstellungen vom Server holen“ ersetzt die Einstellungen auf diesem Gerät; Schlüssel und Produkt-Datenbank bleiben."

**"Einstellungen vom Server holen":**
1. Klicken. Es erscheint "Frage den Server …".
2. Eine Rückfrage zeigt den Stand auf dem Server und auf diesem Gerät: "Einstellungen vom Server übernehmen? … Die Einstellungen auf diesem Gerät werden ersetzt. Schlüssel (OpenAI usw.) und die Produkt-Datenbank bleiben."
3. "OK" → "Übernommen (N Einstellungen). Lade offene Seiten von Cash Lister bitte neu."
4. Offene Seiten von Cash Lister neu laden, auch die Einstellungsseite (F5).

**Gut zu wissen:** "Ersetzt" ist wörtlich gemeint. Einstellungen, die gesichert werden können, aber in der Server-Sicherung fehlen, werden auf diesem Gerät gelöscht und stehen danach wieder auf dem Standard. Was gar nicht gesichert wird (Schlüssel, Werte aus 16.6, Server-Modus), bleibt unverändert.

Mögliche Antworten: "Auf dem Server liegt noch keine Sicherung für dieses Konto.", "Nicht möglich: …", "Übernehmen fehlgeschlagen."

**Konflikt mit zwei Geräten:** Typischer Fall: Du meldest dich auf einem zweiten Rechner an, auf dem schon eigene Einstellungen stehen, und liegt auf dem Server bereits die Sicherung eines anderen Geräts, sichert die Extension nichts, sondern meldet in der Statuszeile:
"Achtung: Auf dem Server liegt eine Sicherung vom <Datum> mit N Einstellungen von einem anderen Gerät. Dieses Gerät hat M Einstellungen und wurde noch nicht gesichert. Bitte entscheiden: "Einstellungen vom Server holen" oder "Dieses Gerät auf den Server sichern"."
Das Dashboard meldet dann "Einstellungen: zwei Geräte". Zusätzlich erscheint der Knopf **"Dieses Gerät auf den Server sichern"**.
- Willst du die Einstellungen vom anderen Gerät hier haben → "Einstellungen vom Server holen".
- Sollen die Einstellungen **dieses** Geräts gelten → "Dieses Gerät auf den Server sichern" → Rückfrage ("Die Sicherung auf dem Server (…) wird durch die … Einstellungen dieses Geräts ersetzt. Fortfahren?") bestätigen. Es erscheint "Sichere …", danach der neue Stand. Meldet es "Sichern fehlgeschlagen: …", später erneut versuchen.

Außerhalb eines solchen Konflikts gilt: Was zuletzt gesichert wurde, gilt.

### 16.6 Was beim Umzug oder nach dem Zurückholen fehlt

Nach dem Einspielen der Export-Datei oder nach dem Zurückholen vom Server auf einem **neuen Rechner bzw. nach einer Neuinstallation** prüfe:
1. **OpenAI-Schlüssel** – kommt nur über die Export-Datei mit, nicht über den Server.
2. **"Mind. Sterne", "Mind. Bewertungen", "Mind. Lagerbestand"** – werden weder exportiert noch gesichert. Neu eintragen.
3. **Die Schalter der Amazon-Filter** – werden nicht mitgesichert. Die Extension leitet sie beim ersten Öffnen der Einstellungsseite aus den Zahlen ab: Steht eine Zahl über 0 im Feld, gilt der Filter als **an**. Beispiel: Hattest du "Preis bis" 100 mit Schalter **aus**, ist der Filter danach **an**. Ebenso "Max. verlängerte Lieferzeit" mit 20.
4. **Server-Modus** – gilt nur für das jeweilige Gerät, auf dem neuen Rechner bei Bedarf neu einschalten.
5. **Produkt-Datenbank** – nichts zu tun: Nach der Anmeldung siehst du dieselbe Liste wie vorher, weil sie auf dem Server liegt.
6. **Gemerkte Konkurrenten** (Konkurrenz-Scanner) – kommen nur über die Export-Datei mit, nicht über den Server.

Holst du die Sicherung dagegen auf **demselben** Rechner zurück (ohne Neuinstallation), bleiben die Punkte 1 bis 4 und 6 so, wie sie auf diesem Rechner eingestellt waren.

### 16.7 Schritt für Schritt: Umzug auf einen neuen Rechner

1. Alter Rechner: Einstellungen → Reiter "Sicherung" → "Einstellungen exportieren". Datei sicher aufbewahren (nicht per öffentlichem Link teilen).
2. Neuer Rechner: Extension installieren (wie vom Betreiber beschrieben), auf das Cash-Lister-Symbol klicken – das Dashboard öffnet sich.
3. Im Dashboard in der Anmelde-Karte "Einrichtungsdatei einlesen" → deine Datei wählen.
4. Mit "Benutzername" und "Passwort" anmelden.
5. Einstellungsseite öffnen und die Punkte aus 16.6 prüfen (Amazon-Filter, Schalter, Schlüssel).
6. Im Reiter "eBay & Rahmenbedingungen" bei "Server & Produkt-Vergabe" auf "Verbindung prüfen" klicken – es sollte "OK – angemeldet als …" kommen.

**Ohne Export-Datei:** Einfach anmelden – die Server-Sicherung wird automatisch zurückgeholt. Danach den OpenAI-Schlüssel neu eintragen und die Punkte aus 16.6 prüfen. Deine Produkt-Datenbank ist trotzdem da (sie liegt auf dem Server).

#### Häufige Fragen
- **"Die Extension war plötzlich weg, alle Einstellungen auch – was tun?"** – Extension neu installieren, im Dashboard anmelden. Die Server-Sicherung kommt automatisch zurück, die Produkt-Datenbank ist auf dem Server. Den OpenAI-Schlüssel neu eintragen (oder deine Export-Datei einspielen).
- **"Wie oft soll ich exportieren?"** – Nach größeren Änderungen. Wichtig ist die Datei vor allem für deinen OpenAI-Schlüssel und die Werte aus 16.6, die der Server nicht sichert.
- **"Kann ich meine Einstellungen einem Freund geben?"** – Nicht die Export-Datei: Sie enthält deinen Schlüssel und deinen Anmeldenamen.

---

## 17. Versand, Zahlung, Rücknahme, Artikelstandort

- **Browser-Lister:** Auf der Einstellungsseite gibt es für den Browser-Lister **keine** Felder für Versand-, Zahlungs- oder Rücknahmebedingungen und keinen Artikelstandort. Der Browser-Lister wählt keine dieser Bedingungen selbst aus; es gilt, was eBay im Angebotsformular vorbelegt. Einzige Ausnahme im Versandbereich: Bietet eBay (auf englischsprachigen eBay-Seiten) den Knopf "Switch to advanced options" an, klickt der Browser-Lister ihn an. **Nicht sicher belegt:** nach welcher Regel eBay die Vorbelegung wählt – prüfe sie in deinem eBay-Konto bei den Rahmenbedingungen und an einem Testangebot mit "Listing automatisch absenden" aus.
- **Frühere Felder:** Ältere Fassungen hatten Felder für einen fest vorgegebenen Artikelstandort und eine feste Rücknahme-Richtlinie. Diese Felder sind ausgeblendet. Was dort früher einmal eingetragen wurde, wirkt weiter. Ändern kannst du es auf der Seite nicht – bei Bedarf an den Betreiber wenden.
- **CSV-Lister:** hat eigene Felder für die Namen der Rahmenbedingungen und den Standort (Abschnitt 10).

---

## 18. Mitgelieferte KI-Anweisungen und Wortlisten

Die Anweisungen an die KI und die Wortlisten kommen fest mit der Extension. Du kannst sie nicht ändern (sie werden bei Updates ersetzt). Gut zu wissen:

- **Artikelmerkmale per KI** (mit "Pflicht-Artikelmerkmale mit KI ausfüllen"): Die KI soll Merkmale **nur** aus Angaben füllen, die im Amazon-Produkttext stehen – nicht raten, nichts ableiten. Gibt es eine Liste erlaubter Werte, soll sie nur daraus wählen; passt keiner, soll sie das Feld frei lassen (leere Pflichtmerkmale füllt die Extension danach, siehe unten). Einige Merkmalsfelder gibt die Extension der KI gar nicht erst (zum Beispiel auf englischsprachigen eBay-Seiten "Brand" und "MPN"). Mit derselben Anfrage wird auch die Spielzeug-Frage beantwortet (Abschnitt 14.5).
- **Produktkennungen:** Am Ende setzt der Browser-Lister die Produktkennung auf "Does not apply" (bei UK, DE, FR, IT, ES, NL die EAN, sonst die UPC). **Nicht sicher belegt:** ob damit in jeder Kategorie ein von der KI eingetragener Kennungswert sicher überschrieben wird.
- **Anweisung für den Kategorie-Suchbegriff:** Auf englischsprachigen eBay-Seiten (USA, CA, UK, AU) bestimmt die KI aus dem Titel einen allgemeinen Suchbegriff, mit dem eBay die passende Kategorie findet. Ist "Pflicht-Artikelmerkmale mit KI ausfüllen" an und gibt es einen solchen Suchbegriff, kommt er außerdem in Pflichtmerkmale, die danach noch leer sind. In allen anderen Fällen (auch immer auf deutschen eBay-Seiten) bekommen leere Pflichtmerkmale "Details In Description".
- **Wortliste für den eingebauten Wortfilter:** siehe Abschnitt 9.3.

---

## 19. Wechselwirkungen auf einen Blick

| Einstellung A | Einstellung B | Was passiert |
|---|---|---|
| "% Aufschlag" / "Fester Aufschlag (€)" | "Variable Preise (nach Preisspanne)" | Passt eine Regel, gelten deren Werte statt der beiden Felder. |
| Karte "Preise" noch nie bearbeitet (neue Installation) | Tracker | Listen rechnet mit 120 %, der Tracker preist ohne Aufschlag nach. Einmal den Aufschlag eintippen (Abschnitt 5.1). |
| "Preisendung" (Feld leer, Schalter an) | Listen und Tracker | Kein gültiger Verkaufspreis (Abschnitt 5.3). |
| Haken "Neu: Sonstige" in einer Preisregel | "Als „Neu: Sonstige“ listen (Standard)" | Die passende Regel entscheidet, in beide Richtungen. |
| "NUR „Neu: Sonstige“ listen" | Kategorie ohne "Neu: Sonstige" | Produkt wird übersprungen statt als "Neu" gelistet. Im CSV-Lister zusätzlich: Kategorien ohne ermäßigte Gebühr werden übersprungen. |
| "Preisendung" | errechneter Preis | Aufrunden und Endung können den Preis leicht unter den errechneten drücken (Abschnitt 5.4). |
| Schalter "Max. verlängerte Lieferzeit" | Listen und Tracker | Schalter wirkt nur im Grabber. Listen und Tracker nutzen die Zahl immer. |
| "Nur Verkauf durch Amazon" | "Nur chinesische Verkäufer" | Schließen sich aus: Beim Listen fällt dann alles mit "Kein chinesischer Verkäufer" durch. |
| "Nur Verkauf durch Amazon" (Einstellungen) | Schalter "nur Verkauf durch Amazon" (Amazon-Suchseite) | Derselbe Wert. |
| "Auch mit Angebotsgebühr einstellen" | "Listing automatisch absenden" | Selbst abgeschickt wird nur, wenn die Gebührenprüfung bestanden ist **und** automatisches Absenden an ist. |
| "Nur ein Bild bei eBay einstellen" | "GPSR-Angaben übernehmen" | Mit GPSR kommt trotzdem ein zweites Bild (GPSR-Bild) dazu. |
| "Nur ein Bild bei eBay einstellen" | Bilderliste in der Beschreibungsvorlage | Nur die hochgeladenen Bilder erscheinen. |
| Kein/ungültiger OpenAI-Schlüssel | Listen | Jedes Produkt scheitert mit "KI-Titel ist leer" (außer mit Konkurrenz-Titel). |
| "OpenAI-Modell" | KI-Titel | Der KI-Titel nutzt immer gpt-4o-mini, egal welche Auswahl. |
| "OpenAI-Modell" | KI-Artikelmerkmale | Lehnt OpenAI das gewählte Modell ab, scheitern die Produkte beim Merkmals-Schritt, obwohl der Titel klappt. |
| Eingebauter Wortfilter ("CE", "IP", "cert") | HTML-Code der Beschreibungsvorlage | Code-Teile, die so beginnen und direkt ein Zeichen oder eine Ziffer haben, können herausgeschnitten werden. |
| "Mehrwertsteuer im Angebot angeben" | "Mehrwertsteuersatz" | Der Satz wird nur eingetragen, wenn der Schalter an ist. |
| "Zustandsbeschreibung" | "Neu: Sonstige"-Schalter und Preisregeln | Text erscheint nur bei Angeboten im Zustand "Neu: Sonstige". |
| Anmeldung (Dashboard) | Produkt-Vergabe, Server-Sicherung, Server-Modus | Alle drei laufen nur mit Anmeldung. Ohne Anmeldung zeigt die Statuszeile (irreführend) "AUS – keine Server-Adresse hinterlegt." |
| Export/Server-Sicherung | Amazon-Filter | Sterne, Bewertungen, Lagerbestand und die Schalter fehlen in der Sicherung. |
| "Domain" | KI-Titel, eBay-Seite, Amazon-Seite, EAN/UPC, Kategorie-Suchbegriff | Bestimmt Sprache, eBay-Land, auf welcher Amazon-Seite die Produkte aus der Datenbank geöffnet werden, Kennungsfeld und ob es einen KI-Suchbegriff gibt. |
| "Pflicht-Artikelmerkmale mit KI ausfüllen" | Spielzeug-Frage | An: Frage läuft mit den Merkmalen. Aus: Frage läuft einzeln. |

---

## 20. Standardwerte auf einen Blick

| Einstellung (Reiter → Karte) | Standard |
|---|---|
| "% Aufschlag" (Preise & Listing → Preise) | 120 (bei der Installation eingetragen; einmal eintippen, damit auch der Tracker ihn kennt – Abschnitt 5.1) |
| "Fester Aufschlag (€)" | 0 |
| "Als „Neu: Sonstige“ listen (Standard)" | aus |
| "NUR „Neu: Sonstige“ listen" | aus |
| "Variable Preise (nach Preisspanne)" | aus, keine Regeln |
| "Preisendung" | 0,99, Schalter an |
| "Domain" (Preise & Listing → Listing) | DE (normalerweise; nach der Installation prüfen) |
| "Listing automatisch absenden" | an |
| "Anzeigengebühr (%)" | 2,3 |
| "Pflicht-Artikelmerkmale mit KI ausfüllen" | an |
| "Optionale Artikelmerkmale mit KI ausfüllen" | an |
| "Nur FBA" (Produkt-Filter → Beim Listen) | an |
| "Nur chinesische Verkäufer" | aus |
| "GPSR-Angaben übernehmen" | aus |
| "Markenlos listen" (CSV-Lister) | an |
| "Bildabgleich gegen fremde Angebote" | aus (Grenze fest) |
| "Max. verlängerte Lieferzeit" (Produkt-Filter → Amazon-Filter) | 20, Schalter an (sobald die Einstellungsseite einmal geöffnet wurde) |
| "Mind. Sterne" | 0, aus |
| "Mind. Bewertungen" | 0, aus |
| "Mind. Lagerbestand" | 0, aus |
| "Preis ab" | 0, aus |
| "Preis bis" | 0, aus (keine Grenze) bei neuer Installation |
| "Nur Verkauf durch Amazon" | aus |
| "Meine Liste" (Blacklist) | leer |
| "Versand", "Zahlung", "Rücknahme", "Artikelstandort (Ort oder PLZ)" (eBay & Rahmenbedingungen → Rahmenbedingungen) | leer |
| "Auch mit Angebotsgebühr einstellen" (→ Beim Einstellen) | aus |
| "Nur ein Bild bei eBay einstellen" | aus |
| "Mehrwertsteuer im Angebot angeben" | aus |
| "Mehrwertsteuersatz" | 19 |
| "Zustandsbeschreibung" (→ Neu: Sonstige) | "Neuware. Die Originalverpackung wurde ggf. zur Prüfung geöffnet. Der Artikel ist unbenutzt, vollständig und voll funktionsfähig, ohne Gebrauchsspuren." |
| "Server-Adresse" (→ Server & Produkt-Vergabe) | leer (leer = eingebaute Adresse, richtig so) |
| "Beenden-CSV für Duplikate erstellen" | aus |
| "Dieses Gerät ist ein Server" (→ Server-Modus) | aus |
| "Gerätename" | "Server" |
| "Beschreibungsvorlage (HTML)" | leer (= schlichte Beschreibung) |
| "OpenAI-API-Schlüssel (für die Titel-Generierung)" (KI) | leer |
| "OpenAI-Modell (für KI-Beschreibung & Generierung)" | gpt-4o-mini |

---

## 21. Meldungen und was sie bedeuten

Meldungen, die mit Einstellungen von dieser Seite zu tun haben. Die meisten erscheinen im Statusbericht des Browser-Listers (Browser-Lister → "Statusbericht", Spalte "Meldung").

| Meldung | Ursache (Einstellung) | Abschnitt |
|---|---|---|
| "Nicht eingestellt: eBay verlangt Angebotsgebühren (Einstellung „Auch mit Angebotsgebühr einstellen“ ist aus)" | eBay zeigt eine Angebotsgebühr, Schalter aus | 11.1 |
| "Produkt enthält ein Wort aus der Blacklist: …" | Treffer in deiner Blacklist | 9.1 |
| "Nicht von Amazon versendet (Versand: …)" | "Nur FBA" an, anderer Versender | 7.1 |
| "Versender auf der Produktseite nicht erkennbar" | "Nur FBA" an, Versender nicht lesbar (oft nicht lieferbar) | 7.1 |
| "Kein chinesischer Verkäufer" | "Nur chinesische Verkäufer" an | 7.2 |
| "Keine GPSR-Angaben gefunden" | "GPSR-Angaben übernehmen" an, keine Herstellerangaben | 7.3 |
| "Amazon-Preis zu hoch (Filter „Preis bis“)" / "Amazon-Preis zu niedrig (Filter „Preis ab“)" | Amazon-Preis außerhalb der Preisgrenzen | 8.6 |
| "Produkt ist nicht auf Lager" | u. a. Lieferzeit länger als "Max. verlängerte Lieferzeit" | 8.2 |
| "Error: Artikel bei Amazon nicht verfügbar" (Tracker; die eigene Meldung "Error: Lieferzeit bei Amazon verlängert" kommt praktisch nicht vor) | u. a. Lieferzeit länger als "Max. verlängerte Lieferzeit" | 8.2 |
| "„Neu: Sonstige" in dieser Kategorie nicht verfügbar (nur-Neu-Sonstige aktiv)" | "NUR „Neu: Sonstige“ listen" an | 5.6 |
| beginnt mit "keine ermäßigte eBay-Gebühr für „Neu: Sonstige"" (CSV-Lister) | "NUR „Neu: Sonstige“ listen" an | 5.6 |
| "Übersprungen: dieses Amazon-Produkt wird auf eBay bereits von jemand anderem angeboten (Bildabgleich, Abstand N)" | Bildabgleich an, bildgleiches Fremdangebot | 7.5 |
| "Produkt bereits von einem anderen Nutzer vergeben" | Produkt-Vergabe: ein anderer Kunde hat es | 12 |
| "KI-Titel ist leer" | kein funktionierender OpenAI-Zugang | 15 |
| beginnt mit "Nicht eingestellt: Fehler beim Ausfüllen des eBay-Formulars (Schritt „⏰ KI erstellt die Artikelmerkmale … bitte warten …")" | KI-Artikelmerkmale gescheitert (Guthaben, Rate-Limit, Modellwahl) | 15.1, 15.2 |
| "OpenAI: API-Key ungültig oder abgelaufen – …" | Schlüssel falsch | 15.3 |
| "OpenAI-Guthaben leer: …" | kein Guthaben bei OpenAI | 15.3 |
| "Beschreibung konnte nicht in den eBay-Editor geschrieben werden: Beschreibungs-Vorlage ist leer (nach Wortfilter nichts uebrig). - Listing abgebrochen, damit es nicht leer online geht." | Vorlage ergibt leere Beschreibung | 14.6 |
| "Einstellungen fehlen: … (Einstellungen → eBay & Rahmenbedingungen)" | CSV-Lister-Felder leer | 10 |
| "Einstellungen gespeichert" | Klick auf "Speichern" | 3 |
| Statuszeile "● Produkt-Vergabe: AUS – keine Server-Adresse hinterlegt." | fast immer: nicht angemeldet | 12.3 |
| "Aktueller Stand zu groß für die Sicherung (… KB, erlaubt 512 KB) – …" | Einstellungen zu groß, meist die Beschreibungsvorlage | 14.8, 16.4 |
| "Achtung: Auf dem Server liegt eine Sicherung vom … von einem anderen Gerät …" | zwei Geräte mit verschiedenen Einstellungen | 16.5 |
| Tab-Titel beginnt mit "WARNUNG! LIEFERZEIT VERLÄNGERT - ZUM LISTEN BESTÄTIGEN -" | Lieferzeit auf der Amazon-Seite länger als erlaubt | 8.2 |
| Tab-Titel beginnt mit "⚠️ BLACKLIST-WORT GEFUNDEN:" | Blacklist-Treffer auf einer selbst geöffneten Amazon-Seite | 9.1 |

---

## 22. Häufige Fragen (allgemein)

**Wo ist das kleine Fenster, das beim Klick auf das Symbol aufging?**
Das gibt es seit 46.0 nicht mehr. Der Klick öffnet das Dashboard. Die Einstellungen aus dem kleinen Fenster stehen jetzt auf der Einstellungsseite in den Reitern "Preise & Listing" und "Sicherung".

**Muss ich nach jeder Änderung "Speichern" drücken?**
Nein, gespeichert wird automatisch (Schalter sofort, Felder beim Verlassen, Preise beim Tippen). "Speichern" ist ein sicherer Abschluss.

**Gibt es "Auf Standard zurücksetzen"?**
Nein. Die Standardwerte stehen in Abschnitt 20; trag sie bei Bedarf von Hand ein.

**Gelten die Einstellungen für alle meine Chrome-Profile?**
Nein, jedes Chrome-Profil hat eigene Einstellungen.

**Werden meine Einstellungen gespeichert, wenn Chrome abstürzt?**
Ja, sie liegen in Chrome und überstehen einen Absturz. Weg sind sie nur, wenn die Extension entfernt wird – dann helfen Server-Sicherung und Export-Datei.

**Ich habe zwei Rechner. Muss ich alles doppelt einstellen?**
Nicht beim Einrichten: Ist Cash Lister auf dem zweiten Rechner frisch installiert, holt er beim ersten Anmelden mit demselben Konto die Server-Sicherung (ohne OpenAI-Schlüssel und ohne die Werte aus 16.6). Danach gleichen sich die Rechner aber **nicht** von selbst ab: Änderst du später etwas auf Rechner A, holst du es auf Rechner B mit "Einstellungen vom Server holen" im Reiter "Sicherung" (16.5) – oder stellst es dort von Hand ein. Die Produkt-Datenbank ist dagegen immer für beide dieselbe. Bei einem Konflikt entscheidest du im Reiter "Sicherung" (16.5).

**Wo ändere ich das eBay-Land?**
Reiter "Preise & Listing", Karte "Listing", "Domain" (Abschnitt 6.1).

**Wo stelle ich die Preise ein?**
Reiter "Preise & Listing", Karte "Preise" (Abschnitt 5).

**Wo stelle ich ein, dass nur Produkte unter 50 € gelistet werden?**
Reiter "Produkt-Filter", Karte "Amazon-Filter", "Preis bis" 50 und Schalter an (Abschnitt 8.6).

**Kann ich ohne KI listen?**
Nein, seit 46.0 nicht mehr (Abschnitt 15.1).

**Wo sehe ich mein Abo?**
Nicht auf der Einstellungsseite, sondern im Dashboard in der Karte "Dein Abo". Einzelheiten stehen im Teil über das Dashboard (`references/dashboard.md`, Abschnitt 14) und im Teil über Konto und Installation (Abschnitt 7).

**Kann ich die Einstellungen öffnen, wenn ich nicht angemeldet bin?**
Ja. Ändern geht auch. Produkt-Vergabe, Server-Sicherung und Server-Modus brauchen aber die Anmeldung.

**Warum finde ich das Feld "Erlaubter Bildabstand" / "Title Prompt" / die zweite Preistafel für „Neu: Sonstige“ nicht mehr?**
Diese Dinge sind entfallen (Abschnitt 26).

---

## 23. Probleme und Lösungen (allgemein)

**Einstellung "springt zurück"**
- Hast du das Feld verlassen, bevor du den Tab geschlossen hast? Wenn nicht, war die Eingabe nicht gespeichert (Abschnitt 3).
- Wurde auf diesem Gerät "Einstellungen vom Server holen" geklickt? Dann gilt der Stand vom Server – möglicherweise der eines anderen Geräts mit demselben Konto (16.5).
- "Max. verlängerte Lieferzeit" steht wieder auf 20? Ein leeres Feld oder 0 ersetzt die Extension beim Listen durch 20 (8.2).

**Einstellungsseite zeigt alte Werte**
- Seite neu laden (F5). Die Seite liest die Werte nur beim Öffnen.

**Ein Bereich fehlt, den ich von früher kenne**
- Viele Bereiche heißen jetzt anders und stehen in Reitern (Abschnitt 4 und 26). Erst alle sechs Reiter durchklicken.

**Nach einem Update ist alles anders**
- Ein Update behält deine Einstellungen; neu sind Aussehen, Namen und Reiter (Abschnitt 26). Nach einem Update Chrome einmal komplett schließen und neu starten (oder unter `chrome://extensions` bei Cash Lister "Neu laden" klicken), damit überall der neue Stand läuft.
- Wenn wirklich alles weg ist, wurde die Extension entfernt und neu installiert → im Dashboard anmelden, die Server-Sicherung kommt zurück, ggf. Export-Datei einspielen.

**Viele Produkte scheitern beim Listen**
- Im Statusbericht in die Spalte "Meldung" schauen und die Meldung in Abschnitt 21 suchen.

**Ich weiß nicht, ob die Produkt-Vergabe läuft**
- Reiter "eBay & Rahmenbedingungen" → Karte "Server & Produkt-Vergabe" → "Verbindung prüfen" (Abschnitt 12.4).

**Produkt-Vergabe zeigt "AUS – keine Server-Adresse hinterlegt."**
- Fast immer heißt das: nicht angemeldet. Im Dashboard anmelden, Einstellungsseite neu laden (12.3).

**Titel klappt, aber jedes Produkt scheitert bei den Artikelmerkmalen**
- Modellwahl prüfen (15.2), Guthaben bei OpenAI prüfen. Zur Not "Pflicht-Artikelmerkmale mit KI ausfüllen" ausschalten.

**Wörter fehlen in Titel oder Beschreibung**
- Eingebauter Wortfilter (9.3). Abschalten lässt er sich nicht.

**Preise stimmen nicht**
- Preisrechnung in Abschnitt 5.4 nachrechnen. Sind "Variable Preise" an und passt eine Regel? Ist die Preisendung an?
- Steht im Feld "Preisendung" eine Zahl über 0,99 oder gar nichts? Siehe 5.3.

**Der Tracker preist meine Angebote zum Amazon-Preis (ohne Aufschlag) nach**
- Die Karte "Preise" wurde nach der Installation nie bearbeitet. Einmal den Aufschlag in "% Aufschlag" eintippen (Abschnitt 5.1), dann rechnet auch der Tracker mit deinen Werten.

---

## 24. Kleines Wörterbuch

- **Dashboard** – die Startseite von Cash Lister. Öffnet sich beim Klick auf das Cash-Lister-Symbol. Hier meldest du dich an.
- **Seitenleiste** – die Leiste links auf Dashboard und allen Modulseiten mit den Modulen; unter "System" steht "Einstellungen".
- **Reiter** – die Karteikarten-Knöpfe oben auf der Einstellungsseite.
- **ASIN** – Amazons eigene Artikelnummer, 10 Zeichen (zum Beispiel B0ABC12345).
- **Buybox** – der Kaufkasten rechts auf der Amazon-Produktseite mit Preis und "In den Einkaufswagen". Dort steht auch, wer verkauft und wer versendet.
- **FBA** – "Fulfillment by Amazon": Amazon lagert und versendet die Ware, auch wenn ein anderer Händler sie verkauft.
- **GPSR** – EU-Produktsicherheitsverordnung; verlangt Angaben zu Hersteller und verantwortlicher Person in der EU.
- **VeRO** – eBays Programm für Rechteinhaber; Markenfirmen können Angebote mit ihren Marken entfernen lassen. Keine automatische Prüfung in der Extension – nutze die Blacklist.
- **SKU / Custom Label** – eigene Artikelnummer in deinem eBay-Angebot. Die Extension trägt dort beim Listen eine eigene Kennung ein (endet auf „==“). Daran erkennen Tracker und Produkt-Vergabe deine Angebote – nicht ändern.
- **EAN / UPC** – Strichcode-Nummern für Produkte (EAN in Europa, UPC in Nordamerika). "Does not apply" heißt: keine Angabe.
- **Angebotsgebühr / Einstellgebühr** – Gebühr, die eBay fürs Einstellen eines Angebots verlangen kann.
- **Anzeigengebühr** – Prozentsatz für beworbene Angebote ("Promoted Listings") bei eBay.
- **Preisendung** – die Cent-Endung deines eBay-Preises, zum Beispiel ,99.
- **Rahmenbedingungen** – bei eBay gespeicherte Vorlagen für Versand, Zahlung und Rücknahme (eBay-Geschäftsrichtlinien).
- **"Neu: Sonstige"** – eBay-Zustand für neue Ware, deren Verpackung zum Beispiel geöffnet wurde.
- **Artikelmerkmale** – die Angaben im eBay-Formular wie Marke, Farbe, Material.
- **Produkt-Grabber** – der Knopf auf Amazon-Suchseiten, der Produkte in deine Produkt-Datenbank übernimmt.
- **Produkt-Datenbank** – deine Liste von Produkten, die gelistet werden sollen; liegt für dein Konto auf dem Server.
- **Statusbericht** – die Liste im Browser-Lister mit Ergebnis und Meldung je Produkt.

---

## 25. Was hier nicht sicher belegt ist

Diese Punkte konnte ich nicht sicher klären. Sag dem Kunden ehrlich, dass du es nicht weißt, und verweise an den Betreiber:

- **Nicht sicher belegt:** welche Versand-/Zahlungsbedingungen eBay beim Browser-Lister vorbelegt (Abschnitt 17).
- **Nicht sicher belegt:** wie zuverlässig "Nur chinesische Verkäufer" auf Amazon-Seiten außerhalb Europas arbeitet (7.2).
- **Nicht sicher belegt:** wie eBay den leeren Wert behandelt, den "Optionale Artikelmerkmale mit KI ausfüllen" auf DE/FR/IT/ES/NL-eBay-Seiten schickt (6.5).
- **Nicht sicher belegt:** was bei leerer "Anzeigengebühr (%)" oder einem Wert unter 2 passiert (6.3).
- **Nicht sicher belegt:** welche Meldung der Browser-Lister bei "Domain" = "Keine" zeigt (6.1). (CSV-Lister und Tracker melden "Keine eBay-Domain eingestellt …".)
- **Nicht sicher belegt:** welche Meldung der Browser-Lister zeigt, wenn das Feld "Preisendung" leer ist (5.3).
- **Nicht sicher belegt:** bei welchen eBay-Konten das MwSt-Feld erscheint (11.3).
- **Nicht sicher belegt:** ob die Gebührenprüfung jede Form der eBay-Gebührenanzeige erkennt, und wie der CSV-Lister mit Angebotsgebühren umgeht (11.1).
- **Nicht sicher belegt:** wie eBay HTML im Feld "Zustandsbeschreibung" behandelt (11.5).
- **Nicht sicher belegt:** wie sich die Modellwahl auf Qualität und Kosten auswirkt (15.2), und wie viel das Ausschalten der KI-Merkmale spart (6.5).
- **Nicht sicher belegt:** welche Meldung im Statusbericht steht, wenn die KI genau beim Kategorie-Suchbegriff scheitert (15.1, 15.2).
- **Nicht sicher belegt:** ob ein von der KI eingetragener Kennungswert (EAN usw.) in jeder Kategorie sicher durch "Does not apply" ersetzt wird (18).
- **Nicht sicher belegt:** welche Meldung eBay zeigt, wenn im CSV-Lister ein Rahmenbedingungs-Name nicht exakt stimmt (10).
- **Nicht sicher belegt:** in welchen Kategorien eBay eine echte EAN verlangt (7.4).
- **Nicht sicher belegt:** wie lange das Dashboard ein Server-Gerät noch anzeigt, das sich nicht mehr meldet (13).
- Wie lange eine Reservierung der Produkt-Vergabe gilt, beantwortet dieser Teil bewusst nicht – bei Bedarf den Betreiber fragen.

---

## 26. Neu in Version 46.0

Was Kunden mit einer älteren Version (45.x) jetzt anders finden:

1. **Kein kleines Fenster mehr beim Klick aufs Symbol.** Es öffnet sich das Dashboard. Angemeldet wird im Dashboard. Die Einstellungen erreichst du über die Seitenleiste links ("System" → "Einstellungen").
2. **Neues Aussehen mit sechs Reitern:** "Preise & Listing", "Produkt-Filter", "eBay & Rahmenbedingungen", "Beschreibungsvorlage", "KI", "Sicherung". Alle Beschriftungen sind deutsch. Der Knopf heißt "Speichern" (früher "Save"), die Meldung "Einstellungen gespeichert" (früher "Settings saved").
3. **Die Einstellungen aus dem kleinen Fenster** stehen jetzt im Reiter "Preise & Listing": "% Aufschlag", "Fester Aufschlag (€)", "Als „Neu: Sonstige“ listen (Standard)", "NUR „Neu: Sonstige“ listen", "Variable Preise (nach Preisspanne)" (früher "nach Preis-Range"), "Preisendung" mit Schalter (früher "End Price" mit Knopf "An"/"Aus"), "Domain" ("None" heißt jetzt "Keine"), "Listing automatisch absenden" (früher "Auto Submit Listing"), "Anzeigengebühr (%)" (früher "Promoted Listing Ad Rate"), "Pflicht-/Optionale Artikelmerkmale mit KI ausfüllen" (früher "Fill Required/Optional Item Specifics with AI"). Export, Import und Server-Sicherung stehen im Reiter "Sicherung". "Min Price (AutoList):"/"Max Price (AutoList):" gibt es nur noch als "Preis ab"/"Preis bis" im Reiter "Produkt-Filter".
4. **Umbenannte Felder der Einstellungsseite:**
   - "Allow automatic listing when eBay shows insertion fees above 0" → "Auch mit Angebotsgebühr einstellen"
   - "Only List One Picture on Ebay" → "Nur ein Bild bei eBay einstellen"
   - "Use VAT On Listing" → "Mehrwertsteuer im Angebot angeben"; "Custom VAT Percentage" → "Mehrwertsteuersatz"
   - "Text:" (Zustandsbeschreibung) → Karte "Neu: Sonstige", Feld "Zustandsbeschreibung"
   - "Nur FBA (Amazon versendet)" → "Nur FBA"; "Nur chinesische Verkäufer (nur EU)" → "Nur chinesische Verkäufer"; "GPSR-Angaben holen" → "GPSR-Angaben übernehmen"
   - "Max Extended Delivery Days" → "Max. verlängerte Lieferzeit"; "Minimum Stars (0–5)" → "Mind. Sterne"; "Minimum Reviews" → "Mind. Bewertungen"; "Minimum Stock (max. 20)" → "Mind. Lagerbestand"; "Minimum Price (€)"/"Maximum Price (€)" → "Preis ab"/"Preis bis"
   - "Produkt-Grabber: nur Produkte übernehmen, die Amazon selbst verkauft und versendet" → "Nur Verkauf durch Amazon"
   - "Produkte überspringen, die auf eBay schon jemand anders anbietet" → "Bildabgleich gegen fremde Angebote"
   - "My list (one per line)" → "Meine Liste" in der Karte "Blacklist"
   - "Produkt-Vergabe (verhindert doppeltes Listen)" → Karte "Server & Produkt-Vergabe"
   - "OpenAI API Key (für Titel-Generierung)" → "OpenAI-API-Schlüssel (für die Titel-Generierung)"
   - Die CSV-Lister-Felder heißen jetzt "Versand", "Zahlung", "Rücknahme", "Artikelstandort (Ort oder PLZ)".
5. **Entfallen:**
   - der Knopf "Standard-List (0.2)" im Browser-Lister (Listen ohne KI-Titel). Es gibt nur noch "Starten" (früher "Opti-List"), der Titel kommt **immer** von der KI. Ohne gültigen OpenAI-Schlüssel wird nichts mehr gelistet.
   - die zweite Preistafel "Eigene Preise für „Neu: Sonstige“". Es gilt eine Tafel für alle Zustände; was dort stand, wird nicht mehr benutzt (Abschnitt 5.6).
   - das Feld "Erlaubter Bildabstand". Der Bildabgleich arbeitet mit einer festen Grenze.
   - die Auswahl einer geplanten Startzeit bei eBay ("Schedule Listing Time" im kleinen Fenster).
   - die langen Erklärungstexte auf der Einstellungsseite (es gibt nur noch kurze graue Hinweise).
6. **Neu:** die Karte "Server-Modus" (Abschnitt 13).
7. **CSV-Lister für alle:** Die Karte "Rahmenbedingungen" und "Markenlos listen" sehen jetzt alle Kunden (früher nur freigeschaltete Tester).
8. **Produkt-Datenbank auf dem Server:** Sie gehört nicht mehr zu den Einstellungen und steht nicht mehr in der Export-Datei. Mehrere Geräte mit demselben Konto sehen dieselbe Liste.
9. **Keine automatische Preisgrenze 100 € mehr:** Bei neuen Installationen ist "Preis bis" aus. Wer von einer älteren Version kommt, hat oft noch 100 mit Schalter an (Abschnitt 8.6).
10. **Meldungen auf Deutsch**, zum Beispiel: "insertion fees" → "Nicht eingestellt: eBay verlangt Angebotsgebühren (…)", "Price is too high" → "Amazon-Preis zu hoch (Filter „Preis bis“)", "Item contains blacklisted word" → "Produkt enthält ein Wort aus der Blacklist: …", "Not a Chinese seller" → "Kein chinesischer Verkäufer", "not gpsr item" → "Keine GPSR-Angaben gefunden", "Item is not in stock" → "Produkt ist nicht auf Lager", "Title is undefined" → "KI-Titel ist leer", "Auto listing failed" → "Listen fehlgeschlagen – keine verwertbare Antwort der Amazon-Seite".
11. **Einrichtungsdatei** wird jetzt im Dashboard mit "Einrichtungsdatei einlesen" eingespielt (früher "Einstellungen importieren" im Anmeldefenster des kleinen Fensters).
12. **Nach dem Update** Chrome einmal komplett neu starten (oder unter `chrome://extensions` bei Cash Lister "Neu laden"). Deine Einstellungen bleiben erhalten.

Wer noch von Version 45.4 kommt, findet außerdem diese älteren Änderungen: Der frühere Haken, ob du bei eBay ein Abo hast, ist weg (er hatte keinen Einfluss auf deine Preise). Der frühere eigene Titel-Generator mit eigenem Titel-Prompt ist weg – es gilt immer der normale KI-Titel; dein OpenAI-Schlüssel blieb erhalten. Das automatische Lösen von Sicherheitsabfragen gibt es nicht mehr; Sicherheitsabfragen löst du selbst. Die frühere VeRO-Prüfung gibt es nicht mehr – nutze die Blacklist (9.2). Die Export-Datei heißt "einstellungen-privat-<Datum>.json".
