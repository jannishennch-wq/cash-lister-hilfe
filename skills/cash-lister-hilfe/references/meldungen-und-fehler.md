# Meldungen und Fehler – das Nachschlagewerk

Hier stehen alle Meldungen, die du in Cash Lister sehen kannst: Fenster mit „OK“, Hinweiszeilen, kleine Einblendungen unten rechts, Einträge im Statusbericht, Texte im Dashboard und in der Seitenleiste, Tab-Titel und die Meldungen des Update-Programms. Zu jeder Meldung steht der genaue Wortlaut, wann sie kommt, was sie bedeutet und was du tun kannst.

> **Hinweis für die Hilfe:** Alle Meldungen hier sind am Stand von Version 46.3 geprüft. Teile in spitzen Klammern wie `<Zahl>` oder `<Grund>` sind Platzhalter, dort steht im Programm ein wechselnder Text. Teile in eckigen Klammern `[…]` erscheinen nur manchmal. Seit 46.0 sind fast alle Meldungen deutsch. Englisch geblieben sind nur wenige Kennwörter im Tracker („Success“, „Skipped“, „ERROR_503“, „Tab failed to load“, das vorangestellte „Error: “ und „Unknown error“), das Wort „Ultimate“ in einer Tracker-Meldung, technische Texte von Chrome und die Texte, die eBay selbst anzeigt. Gib Meldungen so weiter, wie sie dastehen. Stellen mit **Nicht sicher belegt:** sind offen: Sag dort ehrlich, dass du es nicht sicher weißt, und verweise an den Betreiber. Findest du eine Meldung hier nicht, sag das offen. Rate die Bedeutung nicht, sondern bitte um einen Screenshot und verweise an den Betreiber.

## Inhaltsverzeichnis

1. [So findest du eine Meldung schnell](#1-so-findest-du-eine-meldung-schnell)
2. [Stichwortliste A–Z](#2-stichwortliste-az)
3. [Die häufigsten Ursachen zuerst prüfen](#3-die-häufigsten-ursachen-zuerst-prüfen)
4. [Anmeldung und Zugang (Dashboard)](#4-anmeldung-und-zugang-dashboard)
5. [Seitenleiste: der Verbindungskasten](#5-seitenleiste-der-verbindungskasten)
6. [Dashboard: Glocke, Kennzahlen, Vorgänge, Checkliste](#6-dashboard-glocke-kennzahlen-vorgänge-checkliste)
7. [Abo: Warnleiste, Karte „Dein Abo“, Abo-Sperre](#7-abo-warnleiste-karte-dein-abo-abo-sperre)
8. [Einstellungen](#8-einstellungen)
9. [Browser-Lister](#9-browser-lister)
10. [Statusbericht – Meldungen je Produkt](#10-statusbericht--meldungen-je-produkt)
11. [Tab-Titel (beim Listen und auf Amazon-Produktseiten)](#11-tab-titel-beim-listen-und-auf-amazon-produktseiten)
12. [Amazon-Suchseiten: Knopf „→ Datenbank“ (Grabber)](#12-amazon-suchseiten-knopf--datenbank-grabber)
13. [Produkt-Datenbank](#13-produkt-datenbank)
14. [Konkurrenz-Scanner](#14-konkurrenz-scanner)
15. [Tracker](#15-tracker)
16. [Verkaufs-Übersicht](#16-verkaufs-übersicht)
17. [CSV-Lister](#17-csv-lister)
18. [OpenAI-Meldungen (Sammelstelle)](#18-openai-meldungen-sammelstelle)
19. [Update-Programm](#19-update-programm)
20. [Häufige Fragen](#20-häufige-fragen)
21. [Probleme und Lösungen (bereichsübergreifend)](#21-probleme-und-lösungen-bereichsübergreifend)
22. [Was diese Datei nicht sicher weiß](#22-was-diese-datei-nicht-sicher-weiß)
23. [Neu in Version 46.0](#23-neu-in-version-460)

---

## 1. So findest du eine Meldung schnell

1. Lass dir den **genauen Wortlaut** geben, am besten als Screenshot (ohne Passwörter oder Schlüssel im Bild).
2. Frag, **wo** die Meldung stand: im Dashboard, in der Seitenleiste links, in den Einstellungen, im Browser-Lister, im Statusbericht, im Tracker, als Tab-Titel, auf einer Amazon-Seite, im Fenster von `update.bat` …
3. Such in der Stichwortliste (Abschnitt 2) nach einem auffälligen Wort aus der Meldung. Viele Meldungen beginnen gleich (z. B. „Produkt-Vergabe: …“, „Sheet …“, „OpenAI …“, „WARNUNG! …“, „Nicht eingestellt: …“, „Error: …“).
4. Steht die Meldung in mehreren Bereichen (z. B. „Server nicht erreichbar“), nimm den Abschnitt des Bereichs, in dem der Kunde sie gesehen hat.
5. Findest du sie nicht: offen sagen und an den Betreiber verweisen (siehe Abschnitt 22).

**Wichtig:** Manche Meldungen klingen dramatisch oder führen auf eine falsche Spur, meinen aber nur: **nicht angemeldet**. Beispiele: „Für den Tracker brauchst du die Ultimate-Mitgliedschaft.“, „● Produkt-Vergabe: AUS – keine Server-Adresse hinterlegt.“, „Produkt-Vergabe: API-Key ungültig.“. Das steht jeweils dabei.

---

## 2. Stichwortliste A–Z

| Stichwort / Anfang der Meldung | Abschnitt |
|---|---|
| „Abbruch beim Blättern: …“ (Ganzer Shop) | 12.2 |
| „Abgebrochen – … fertige Zeile(n) verworfen …“ (CSV-Lister) | 17.3 |
| „Abgebrochen: …“ (Statusbericht) | 10.1 |
| „Abgebrochen: Fehler beim Ausfuellen“ (Tab-Titel) | 11.1 |
| „Abo beendet“ / „Abo gesperrt“ | 7 |
| „Abo gesperrt – bitte im Dashboard nachsehen.“ | 7.4, 9.2, 10.1 |
| „Abo verwalten“ (Hinweise darunter) | 7.3 |
| „Achtung: Auf dem Server liegt eine Sicherung …“ | 8.4 |
| „Achtung: Keine Bestellung aus …“ | 16 |
| „Aktuell: nur FBA …“ | 9.2 |
| „Alle … Produkte der Datenbank sind gerade in Arbeit …“ | 9.1, 17.3 |
| „Alle … Produkte sind abgewählt …“ | 12.2 |
| „Alle gesammelten Funde verwerfen?“ | 14.3 |
| „Amazon zeigt Captcha oder Anmeldeseite …“ (CSV-Lister) | 17.5 |
| „Amazon zeigt ein Captcha …“ (⛔, Grabber) | 12.2 |
| „Amazon hat deine IP … vorübergehend gesperrt.“ | 15.4 |
| „Amazon-Preis zu hoch / zu niedrig …“ | 10.2 |
| „Amazon: kein Angebot/Versender …“ | 17.4 |
| „Angebot eingestellt!“ (Tab-Titel) | 11.1 |
| „Anmeldung abgelehnt (401) …“ | 8.2 |
| „Anmeldung abgelehnt: Abo gesperrt.“ | 4.2, 7.4 |
| „Anmeldung fehlgeschlagen (HTTP …)“ | 4.2, 19 |
| „Anmeldung weg (Sitzung abgelaufen oder Zugang abgeschaltet) …“ | 17.5 |
| „Artikel bei Amazon nicht verfügbar“ / „… nicht Prime-fähig“ / „… ohne kostenlosen Versand“ | 15.3 |
| „ASIN passt nicht: erwartet …“ | 15.3 |
| „ASIN und Adresse (URL) passen nicht zusammen“ | 10.2 |
| „Auf dem Server gesichert: …“ / „Auf dem Server liegt noch keine Sicherung …“ | 8.4 |
| „Beenden-Datei mit … heruntergeladen …“ | 15.9, 16 |
| „Bericht wird erstellt…“ / „Bericht fertig“ (Tab-Titel) | 15.2 |
| „Bericht wird eingelesen …“ | 15.1 |
| „Beschreibung konnte nicht in den eBay-Editor geschrieben werden …“ | 10.4 |
| „Bitte den Link zur Verkäufer-Produktseite einfügen.“ / „Bitte einen eBay-Link einfügen …“ | 14.1 |
| „Bitte nur einen Angebotsbericht auf einmal …“ | 16 |
| „Bitte <Zahl> Sekunden warten.“ (unter „Abo verwalten“) | 7.3 |
| „Bitte oben eintragen, wie viele Angebote entstehen sollen.“ | 9.1 |
| „Bitte zuerst anmelden – das geht im Dashboard.“ | 13.1 |
| „Bitte zuerst in Cash Lister anmelden – nichts importiert.“ (❌) | 12.2 |
| „Browser-Lister beendet: …“ | 9.2, 10.1 |
| Captcha / Sicherheitsabfrage | 12.2, 15.4, 17.5, 21 |
| „Claims-Server nicht erreichbar …“ / „Der Claims-Server lehnt die Anfrage ab …“ | 13.1, 13.2, 12.2 |
| „Das ist keine Einstellungsdatei.“ | 4.3 |
| „Datei ist leer.“ | 14.3 |
| „Dauerbetrieb …“ | 15.7 |
| „Datenbank geleert.“ | 13.3 |
| „Deine Version der Extension ist veraltet …“ | 4.2 |
| „Der Hintergrund hat geantwortet, aber ohne Ergebnis …“ | 15.2 |
| „Der Konkurrenz-Scanner hat noch keine Funde.“ | 9.1 |
| „Die Datei ist kein gültiges JSON.“ | 4.3, 8.3 |
| „Die eBay-Berichtsseite meldet sich nicht …“ | 15.2 |
| „Die Produkt-Datenbank ist leer …“ | 9.1, 17.3 |
| „Dieser Zugang ist abgeschaltet.“ | 4.2, 17.5 |
| „Dieses Modul ist noch im Test“ | 23 |
| „Du hast bereits die neueste Version.“ / „Du hast bereits die aktuelle Fassung …“ (Update-Programm) | 19 |
| „eBay hat auf eine andere Seite umgeleitet …“ | 15.2 |
| „eBay lieferte eine HTML-Seite statt des Berichts …“ | 15.2 |
| „eBay-Fehlerseite - Angebot nicht eingestellt“ | 10.4 |
| „eBay-Serverfehler (upstream connect error) …“ | 10.4 |
| „Einstellen fehlgeschlagen!“ (Tab-Titel) | 11.1 |
| „Einstellen fehlgeschlagen, eBay nennt keinen Grund: …“ | 10.4 |
| „Einstellungen gespeichert“ | 8.1 |
| „Einstellungen importiert (…)“ | 8.3 |
| „Einstellungen vom Server übernehmen?“ | 8.4 |
| „Erfolgreich gelistet!“ | 10.1 |
| „Error: …“ (Spalte „Status“ im Tracker) | 15.3 |
| „ERROR_503 …“ | 15.3 |
| „Erst die offenen Punkte oben beheben.“ | 17.1 |
| „Es wird gerade noch eingelesen …“ | 16 |
| „FEHLER: …“ (Update-Programm) | 19 |
| „Fehler beim CSV-Download: …“ | 15.2 |
| „Fehlt noch: …“ (CSV-Lister) | 17.1 |
| „Format geprüft …“ / „Format-Prüfung …“ / „Nicht eingestellt: kein Sofort-Kaufen“ | 10.5 |
| „Fertig - die eingestellte Zahl an Angeboten ist erreicht.“ / „Fertig: … von … gelistet.“ | 9.1, 9.2 |
| „Fertig – … neue Treffer bei … Produkten …“ (Konkurrenz-Scanner) | 14.1 |
| „Frage den Server …“ | 8.4 |
| „Für den Tracker brauchst du die Ultimate-Mitgliedschaft.“ | 15.1 |
| „Gestoppt.“ (Konkurrenz-Scanner) | 14.1 |
| „Heute noch … von …“ / „Tageskontingent …“ | 17.2 |
| „Hinweis“ (Spalte „Status“ im Statusbericht) | 10.1 |
| „Hinweis zur Produkt-Vergabe: …“ | 15.9 |
| „Importiere … Produkte …“ | 12.2 |
| „In Arbeit“ (Spalte, Zahl) | 13 |
| „Keine Antwort vom Hintergrunddienst …“ | 4.2, 6.2, 21 |
| „Keine eBay-Domain eingestellt …“ | 15.2, 17.3 |
| „Keine Hinweise – alles in Ordnung.“ | 6.1 |
| „Keine Preis-/Bestandsänderungen – Upload übersprungen.“ | 15.6 |
| „Keine Produktkacheln auf dieser Seite gefunden.“ | 12.2 |
| „Keine Produkte gefunden. Zeigt die eingefügte Seite …“ | 14.1 |
| „Keine Server-Adresse hinterlegt …“ | 4.2, 8.2 |
| „Keine Sheets hinterlegt.“ | 13.4 |
| „Keine Zeilen zum Verarbeiten – lade zuerst einen Angebotsbericht.“ | 15.1 |
| „Keins der … Produkte wird von Amazon verkauft …“ | 12.2 |
| „Kein chinesischer Verkäufer“ | 10.2 |
| „Keine GPSR-Angaben gefunden“ | 10.2 |
| „KI-Schnittstelle …“ | 17.5, 18 |
| „KI-Titel ist leer“ | 10.3 |
| „Kundenportal …“ | 7.3 |
| „Kurz warten!“ (⏳) | 15.4 |
| „Lauf des Trackers unterbrochen“ | 6.1 |
| „Lieferzeit bei Amazon verlängert“ | 15.3 |
| „Listen fehlgeschlagen – keine verwertbare Antwort der Amazon-Seite“ | 10.3 |
| „Mehrere Produktseiten nicht abrufbar …“ (⛔) | 12.2 |
| „Melde an …“ | 4.2 |
| „Melde dich mit deinem Zugang an …“ | 4.1 |
| „meldet sich nicht“ (Server-Gerät) | 6.1, 6.2 |
| „Nachgelagerter Fehler: …“ | 10.1 |
| „Name oder Passwort falsch.“ | 4.2 |
| „Name und Passwort noetig“ | 4.2 |
| „„Neu: Sonstige" in dieser Kategorie nicht verfügbar …“ | 10.4 |
| „Netzwerkfehler beim Abruf der Amazon-Daten“ | 15.3 |
| „Nicht angemeldet“ (Seitenleiste, Dashboard) | 4.1, 5 |
| „Nicht angemeldet - bitte im Dashboard anmelden.“ (Fenster auf Amazon) | 10.2 |
| „Nicht angemeldet oder Sitzung abgelaufen …“ | 9.1, 17.5 |
| „Nicht angemeldet oder Zugang deaktiviert - bitte im Dashboard anmelden.“ | 9.1 |
| „Nicht angemeldet – bitte im Dashboard anmelden.“ (Einstellungen) | 8.2 |
| „Nicht eingestellt: eBay verlangt Angebotsgebühren …“ | 10.4 |
| „Nicht eingestellt: Fehler beim Ausfüllen des eBay-Formulars …“ | 10.4 |
| „Nicht gestartet: …“ (CSV-Lister) | 17.3 |
| „Nicht möglich: …“ | 8.4 |
| „Nicht von Amazon versendet (Versand: …)“ | 10.2 |
| „Nichts gefunden – alle Kacheln von den Filtern ausgeschlossen?“ | 12.2 |
| „Nichts importiert – …“ | 13.2, 12.2 |
| „Nichts markiert.“ | 16 |
| „Noch kein Abo eingerichtet …“ | 7 |
| Notbremse („⛔ Notbremse: …“) | 15.5 |
| „Nur teilweise importiert – …“ | 13.2, 12.2 |
| „OK – angemeldet als …“ | 8.2 |
| „OpenAI …“ | 18 |
| „Preisregeln …“ / „Bitte füge die Preisregeln als JSON ein.“ | 15.10 |
| „Produkt bereits von einem anderen Nutzer vergeben“ | 10.1 |
| „Produkt enthält ein Wort aus der Blacklist: …“ | 10.2 |
| „Produkt hat eine Mindestbestellmenge“ | 10.2 |
| „Produkt hat keinen kostenlosen Versand“ / „Produkt ist gebraucht“ | 10.2 |
| „Produkt ist nicht auf Lager“ / „Produkt wird international versendet“ | 10.2 |
| „Produkt ist schon gelistet (Duplikat)“ | 10.2 |
| „Produkt-Datenbank auf dem Server noch nicht bereit …“ / „(Produkt-Datenbank noch nicht bereit)“ | 13.2, 9.2, 10.1 |
| „Produkt-Datenbank nicht abrufbar: …“ | 9.1 |
| „Produkt-Datenbank: …“ (CSV-Lister) | 17.3 |
| „Produkt-Vergabe: …“ (Tracker) | 15.9 |
| „● Produkt-Vergabe: AN/AUS …“ (Einstellungen) | 8.2 |
| „Produktseite existiert nicht“ | 10.2 |
| „Prüfung abgebrochen.“ | 12.2 |
| „Quelle aufgebraucht - …“ | 9.2 |
| „Server nicht erreicht“ (Dashboard, Seitenleiste) | 5, 6.1 |
| „Server bremst die eBay-Abfragen …“ (CSV-Lister) | 17.5 |
| „Server nicht erreichbar …“ | 4.2, 8.4, 9, 12.2, 13, 15.9, 19, 21 |
| „Server wieder erreichbar – Lister läuft weiter …“ | 10.1 |
| „Server-Fehler: …“ | 4.2 |
| „Sheet …“ / „Sheet-Sync …“ / „Sheet-Update …“ | 15.8 |
| „Sichern fehlgeschlagen: …“ | 8.4 |
| „Sitzung abgelaufen – bitte im Dashboard neu anmelden.“ | 6.2, 9.2, 10.1 |
| „Skipped“ | 15.3 |
| „Sortieren fehlgeschlagen: …“ | 13.3 |
| „Success“ | 15.3 |
| „Tab failed to load …“ | 15.3 |
| „Titel-Erstellung fehlgeschlagen“ | 10.3 |
| „Übernommen (… Einstellungen) …“ | 8.4 |
| „Übernehmen fehlgeschlagen.“ | 8.4 |
| „Übersprungen: dieses Amazon-Produkt wird auf eBay bereits …“ | 10.4 |
| „ÜBERSPRUNGEN! …“ (Tab-Titel) | 11.1 |
| „Ungültige Einstellungsdatei.“ | 8.3 |
| „Unknown error“ (Tracker) | 15.3 |
| „Upload zu eBay fehlgeschlagen: …“ | 15.6 |
| „Upload nicht gelungen: …“ / „Upload-Ergebnis unklar: …“ (CSV-Lister) | 17.3 |
| „verfügbar“ (Browser-Lister) | 9.2 |
| „Verlauf gelöscht.“ | 16 |
| „Verbindung wird geprüft …“ (Seitenleiste) | 5 |
| „Versender auf der Produktseite nicht erkennbar“ | 10.2 |
| „WARNUNG! …“ (Tab-Titel) | 11.1, 11.2 |
| „Willkommen bei Cash Lister“ (Dashboard) | 4.1 |
| „Wirklich ALLE Produkte aus der Datenbank löschen?“ | 13.3 |
| „Wörter: …“ | 8.1 |
| „Zahlung offen“ / „Zahlung überfällig“ / „Erste Zahlung fehlgeschlagen“ | 7.1 |
| „Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“ | 10.4 |
| „Zeitüberschreitung (timeout): …“ | 15.3 |
| „Zeitüberschreitung beim Warten auf: …“ | 15.2, 15.6 |
| „Zu viele Fehlversuche …“ | 4.2 |
| „Zu viele Versuche …“ (Update-Programm) | 19 |
| „Zugang abgeschaltet“ / „Zugang abgeschaltet – bitte beim Betreiber melden. …“ | 4.1, 5, 9.2 |
| „Zugang ist abgeschaltet (403).“ | 8.2 |
| „Zustand nicht wählbar: Kachel „Neu mit Etikett“ nicht gefunden“ | 10.4 |
| „✅ … neu in der Datenbank …“ | 12.2 |
| „✅ … hinzugefügt …“ | 13.2 |
| „✅ Produkt-Vergabe abgeglichen: …“ | 15.9 |
| „✅ Sperrbegriffe aus den Artikelmerkmalen entfernt“ (Tab-Titel) | 11.1 |
| „⚠ Server nicht erreichbar – Lister pausiert …“ | 9.2 |
| „⚠️ … Produkte wurden OHNE Reservierung übernommen …“ | 14.3 |
| „⚠️ BLACKLIST-WORT GEFUNDEN: …“ (Tab-Titel) | 11.2 |
| „😴 Schläft – Kontingent erreicht …“ / „⏱ Zeitschaltung: …“ | 9.2 |
| „⛔ Tracker angehalten – … % ohne Ergebnis“ (Tab-Titel) | 15.5 |

---

## 3. Die häufigsten Ursachen zuerst prüfen

Viele verschiedene Meldungen haben dieselben wenigen Ursachen. Bevor du tief einsteigst, prüf mit dem Kunden diese sechs Punkte:

1. **Angemeldet?** Links unten in der Seitenleiste steht der Verbindungskasten. Dort muss „Server verbunden“ stehen und darunter „angemeldet als <Name>“. Steht dort „Nicht angemeldet“, zuerst im Dashboard anmelden (Klick auf das Cash-Lister-Symbol oben rechts in Chrome öffnet das Dashboard). Ohne Anmeldung sind Browser-Lister, Tracker, CSV-Lister, Produkt-Datenbank, Verkaufs-Übersicht und Konkurrenz-Scanner in der Seitenleiste ausgegraut, und die **Produktvergabe** (Schutz davor, dass zwei Kunden dasselbe Produkt listen) ist aus.
2. **Abo gesperrt oder Zugang abgeschaltet?** Steht in der Seitenleiste „Abo gesperrt“ oder „Zugang abgeschaltet“, sperren sich die Module. Was zu tun ist: Abschnitt 7.4 bzw. 4.1.
3. **Server erreichbar?** Seit 46.0 liegt die Produkt-Datenbank je Konto auf dem Server. Steht in der Seitenleiste „Server nicht erreicht“, nehmen die Lister keine neuen Produkte. Der Browser-Lister wartet und macht von selbst weiter, sobald der Server wieder antwortet (Abschnitt 9.2, 21).
4. **Hintergrunddienst nach einem Update neu geladen?** Der **Hintergrunddienst** ist der unsichtbare Teil der Extension, der im Hintergrund arbeitet. Nach einem Update läuft dort manchmal noch die alte Version. Typische Zeichen: „Keine Antwort vom Hintergrunddienst“, „keine Antwort vom Hintergrund“, „? verfügbar“, Knöpfe ohne Wirkung, die Meldung „veraltet“ trotz neuer Versionsnummer. Lösung: Chrome komplett schließen und neu starten, notfalls in `chrome://extensions` bei Cash Lister auf „Neu laden“ klicken (Schritte in `konto-und-installation.md`, Abschnitt zum Hintergrunddienst).
5. **Bei eBay und Amazon im selben Chrome-Profil angemeldet?** Viele Fehler beim Listen, beim Laden des eBay-Angebotsberichts und beim Hochladen kommen daher, dass die eBay-Anmeldung abgelaufen ist.
6. **„Domain“ gesetzt, OpenAI-Schlüssel mit Guthaben?** Die Auswahl „Domain“ (Einstellungen → Reiter „Preise & Listing“ → Karte „Listing“) legt fest, auf welchem eBay-Marktplatz gearbeitet wird. Steht sie auf „Keine“, kommt z. B. „Keine eBay-Domain eingestellt …“. Titel schreibt seit 46.0 immer die KI; dafür braucht es einen eigenen OpenAI-Schlüssel mit Guthaben (Einstellungen → Reiter „KI“).

---

## 4. Anmeldung und Zugang (Dashboard)

Wo: im **Dashboard**. Ein Klick auf das Cash-Lister-Symbol oben rechts in Chrome öffnet es (ein kleines Fenster gibt es seit 46.0 nicht mehr). Ist niemand angemeldet, steht oben auf der Seite die **Anmeldekarte** mit den Feldern „Benutzername“ und „Passwort“, dem Knopf „Anmelden“ und rechts daneben dem Bereich „Einrichtungsdatei“. Meldungen zum Anmelden stehen in einer Zeile direkt unter dem Knopf „Anmelden“ (rot bei Fehlern).

### 4.1 Wo der Anmeldestand steht

| Stelle | Text | Bedeutung | Was tun |
|---|---|---|---|
| Überschrift oben im Dashboard | „Guten Morgen, <Name>“ / „Guten Tag, <Name>“ / „Guten Abend, <Name>“ | Angemeldet | nichts |
| Überschrift oben im Dashboard | „Willkommen bei Cash Lister“ | Nicht angemeldet, gesperrt oder abgeschaltet | Zeile darunter und Anmeldekarte lesen |
| Zeile unter der Überschrift | „<Wochentag, Datum> · Server verbunden“ | Alles in Ordnung | nichts |
| Zeile unter der Überschrift | „… · Server nicht erreicht“ | Der Server hat länger nicht geantwortet, oder die Produkt-Datenbank meldet einen Ausfall | Abschnitt 6.1 und 21 |
| Zeile unter der Überschrift | „… · nicht angemeldet“ / „… · Zugang abgeschaltet“ / „… · Abo gesperrt“ | wie es dasteht | siehe unten |
| Kontofeld oben rechts | Name und klein „angemeldet“ | Angemeldet | nichts |
| Kontofeld oben rechts | „Nicht angemeldet“ | Nicht angemeldet. Ein Klick setzt den Cursor ins Feld „Benutzername“ | anmelden |
| Kontofeld oben rechts | klein „Zugang abgeschaltet“ bzw. „Abo gesperrt“ | wie es dasteht | siehe unten |
| Anmeldekarte, Titel „Nicht angemeldet“ | „Melde dich mit deinem Zugang an. Danach füllt sich diese Seite von selbst.“ | Abgemeldet oder Sitzung abgelaufen | mit Benutzername und Passwort anmelden |
| Anmeldekarte, Titel „Zugang abgeschaltet“ | „Zugang abgeschaltet – bitte beim Betreiber melden. Mit einem anderen Zugang kannst du dich hier neu anmelden.“ | Der Betreiber hat deinen Zugang abgeschaltet. Die Module sind gesperrt | Beim Betreiber melden. Die Hilfe kann nichts freischalten |
| Anmeldekarte, Titel „Abo gesperrt“ | Text vom Server, siehe Abschnitt 7.4 | Dein Abo ist wegen einer offenen Zahlung gesperrt | Abschnitt 7.4 |

**Gut zu wissen:**
- Ist die Sitzung abgelaufen oder wurde das Passwort geändert, steht irgendwann wieder „Nicht angemeldet“. Eine eigene Meldung dafür gibt es nicht. Einfach neu anmelden.
- Dasselbe passiert, wenn deine Version der Extension zu alt ist: Du wirst ohne eigene Meldung abgemeldet. Erst beim nächsten Anmelden erscheint der Hinweis „Deine Version der Extension ist veraltet …“ (4.2).
- Ohne Anmeldung sind die Modulkarten im Dashboard und die Module in der Seitenleiste ausgegraut. Nur „Dashboard“ und „Einstellungen“ bleiben anklickbar.

### 4.2 Meldungen beim Anmelden

Diese Texte stehen unter dem Knopf „Anmelden“.

| Meldung | Wann / Bedeutung | Was tun |
|---|---|---|
| „Melde an …“ (grau) | Die Anmeldung läuft | kurz warten |
| „Name oder Passwort falsch.“ | Benutzername oder Passwort stimmen nicht. Absichtlich wird nicht verraten, welches von beiden falsch ist | Groß-/Kleinschreibung und Leerzeichen prüfen. Am sichersten mit der Einrichtungsdatei anmelden (4.3). Klappt es nicht: Betreiber fragen |
| „Name und Passwort noetig“ | Eines der beiden Felder war leer | Beide Felder ausfüllen |
| „Zu viele Fehlversuche. Bitte <Zahl> Sekunden warten.“ | Mehrmals hintereinander falsch angemeldet; die Anmeldung ist kurz gesperrt (Schutz gegen Durchprobieren) | Die genannte Zeit abwarten, dann sorgfältig neu eingeben |
| „Zu viele Fehlversuche. Bitte kurz warten.“ | Dasselbe, wenn keine Sekundenzahl mitkam | Ein paar Minuten warten |
| „Dieser Zugang ist abgeschaltet.“ | Name und Passwort stimmen, aber der Zugang ist abgeschaltet | Beim Betreiber melden |
| „Anmeldung abgelehnt: Abo gesperrt.“ | Name und Passwort stimmen, aber dein Abo ist gesperrt. Darüber zeigt die Karte den Titel „Abo gesperrt“ und den Text vom Server | Abschnitt 7.4 |
| „Deine Version der Extension ist veraltet und wird nicht mehr unterstuetzt. Bitte melde dich beim Betreiber - du bekommst dann die neue Version.“ | Die laufende Extension ist älter als die Mindestversion und wird nicht mehr angemeldet | Update machen (`konto-und-installation.md`, Updates und Mindestversion), danach Chrome komplett neu starten. Kommt die Meldung, obwohl links unten in der Seitenleiste schon die neue Versionsnummer steht, läuft im Hintergrund noch die alte Version: Hintergrunddienst neu laden (Abschnitt 3, Punkt 4) |
| „Server nicht erreichbar (<Adresse>). Adresse prüfen oder später erneut versuchen.“ | Der Server hat innerhalb von etwa 20 Sekunden nicht geantwortet, oder die Verbindung kam nicht zustande | Internetverbindung prüfen. Das Feld „Server-Adresse (nur auf Ansage ändern)“ in der Anmeldekarte **nicht** selbst ändern, außer der Betreiber sagt es. Später erneut versuchen. Bleibt es dabei: Betreiber fragen |
| „Server-Fehler: <Text>“ | Auf dem Server ist ein Fehler aufgetreten | Später erneut versuchen; bleibt es: Betreiber mit Screenshot informieren |
| „Anmeldung fehlgeschlagen (HTTP <Zahl>).“ | Unerwartete Antwort des Servers | Später erneut versuchen; bleibt es: Betreiber mit Screenshot informieren |
| „Keine Antwort vom Hintergrunddienst – bitte noch einmal versuchen.“ | Nach etwa 30 Sekunden kam vom Hintergrunddienst kein Ergebnis | Noch einmal auf „Anmelden“ klicken. Hilft das nicht: Hintergrunddienst neu laden (Abschnitt 3, Punkt 4) |
| „Keine Server-Adresse hinterlegt. Bitte eintragen (Einstellungen → eBay → „Server & Produkt-Vergabe“).“ | Es ist keine Serveradresse bekannt. Kommt normalerweise nicht vor, weil die Extension eine Voreinstellung hat | Nicht selbst etwas eintragen. Screenshot an den Betreiber |

Nach dem heutigen Stand sind das alle Texte, die beim Anmelden erscheinen können. **Nicht sicher belegt:** ob künftig weitere dazukommen. Die Extension zeigt Texte des Servers wörtlich an. Steht ein Text hier nicht: Screenshot an den Betreiber.

### 4.3 Knopf „Einrichtungsdatei einlesen“

Wo: in der Anmeldekarte rechts, Bereich „Einrichtungsdatei“ (nur sichtbar, solange du nicht angemeldet bist). Die Meldung erscheint direkt unter dem Knopf.

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Die Datei ist kein gültiges JSON.“ | Die gewählte Datei ist keine Einstellungsdatei (falsche Datei, beschädigt, umbenannte andere Datei) | Die Originaldatei vom Betreiber nehmen (`zugang.json` oder `leck-atakan-einrichtung-<Name>.json`); nicht in Word o. Ä. öffnen und speichern |
| „Das ist keine Einstellungsdatei.“ | Die Datei ist lesbar, hat aber nicht den richtigen Aufbau | Richtige Datei wählen; sonst Betreiber um eine neue Datei bitten |
| „Import fehlgeschlagen: <Grund>“ | Chrome konnte die Einstellungen nicht speichern | Chrome neu starten und noch einmal versuchen; bleibt es: Betreiber mit Screenshot |
| „<Zahl> Einstellungen übernommen – melde an …“ (grün) | Datei gelesen; die Extension meldet dich jetzt mit den Zugangsdaten aus der Datei an | Kurz warten. Danach verschwindet die Anmeldekarte, oder unter dem Knopf „Anmelden“ steht eine Meldung aus 4.2 |
| „<Zahl> Einstellungen übernommen. Die Datei enthielt keine Zugangsdaten – bitte von Hand anmelden.“ | Die Datei enthielt nur Einstellungen, keinen Namen und kein Passwort (z. B. eine selbst exportierte Datei) | Links Benutzername und Passwort eintippen |

Die Einrichtungsdatei vom Betreiber gehört nur dir – nicht weitergeben.

### 4.4 Abmelden

Wo: Dashboard → Kontofeld oben rechts anklicken → Eintrag „Abmelden“ („Danach sperren sich die Module bis zur nächsten Anmeldung.“).

| Text | Bedeutung | Was tun |
|---|---|---|
| Im aufgeklappten Kontofeld: „Angemeldet · Server verbunden“ / „Angemeldet · Server nicht erreicht“ | Zustand der Anmeldung | nichts |
| Fenster „Gerade läuft auf diesem PC: <Module>. Nach dem Abmelden sperren sich die Module. Trotzdem abmelden?“ | Sicherheitsfrage, wenn Tracker, Browser-Lister oder CSV-Lister gerade laufen | „OK“ meldet ab, „Abbrechen“ lässt alles laufen |
| „wird abgemeldet …“ / „Wird abgemeldet …“ | Die Abmeldung läuft (höchstens etwa 30 Sekunden) | warten |

---

## 5. Seitenleiste: der Verbindungskasten

Wo: links unten in der Seitenleiste, auf jeder Seite von Cash Lister. Darunter steht die Versionsnummer („Version <Zahl>“). Der Kasten frischt sich etwa alle 15 Sekunden auf.

| Erste Zeile (mit Punkt) | Zeilen darunter | Bedeutung | Was tun |
|---|---|---|---|
| „Verbindung wird geprüft …“ | – | Die Seite ist gerade erst geladen | kurz warten |
| „Server verbunden“ (grüner Punkt) | „angemeldet als <Name>“, „Produkt-Vergabe aktiv“ | Alles in Ordnung | nichts |
| „Server nicht erreicht“ (oranger Punkt) | „antwortet nicht seit <Zeit>“ oder „zuletzt erreicht <Zeit>“, dazu „Lister nehmen keine Produkte“ | Der Server antwortet nicht, oder die letzte erfolgreiche Prüfung ist länger als etwa eine Stunde her. Ohne Server nehmen die Lister keine Produkte aus der Produkt-Datenbank | Internet prüfen, etwas warten. Der Browser-Lister macht von selbst weiter, sobald der Server wieder antwortet. Bleibt es lange so: Betreiber informieren |
| „Nicht angemeldet“ | „Produkt-Vergabe aus“ | Nicht angemeldet | Im Dashboard anmelden |
| „Zugang abgeschaltet“ (roter Punkt) | „angemeldet als <Name>“, „Produkt-Vergabe aus“ | Der Betreiber hat den Zugang abgeschaltet | Beim Betreiber melden |
| „Abo gesperrt“ (roter Punkt) | „Details im Dashboard“, „Produkt-Vergabe aus“ | Dein Abo ist gesperrt | Dashboard öffnen, Abschnitt 7.4 |

**Gut zu wissen:** Nach einer längeren Pause (Chrome war zu, PC im Ruhezustand) kann kurz „Server nicht erreicht“ mit „zuletzt erreicht <Zeit>“ stehen, bis die Extension die Anmeldung beim Server neu geprüft hat. Diese Prüfung läuft beim Start von Chrome, beim Öffnen des Dashboards und sonst regelmäßig im Hintergrund. Antwortet der Server dabei, steht wieder „Server verbunden“. Das Dashboard zu öffnen löst es also meist schnell. **Nicht sicher belegt:** wie lange es im Einzelfall dauert, bis die Seitenleiste umspringt.

---

## 6. Dashboard: Glocke, Kennzahlen, Vorgänge, Checkliste

Ausführlich zum Dashboard: `dashboard.md`. Hier nur die Texte, die auf ein Problem hinweisen.

### 6.1 Die Glocke (Hinweise)

Wo: Glocke oben rechts im Dashboard. Ein Punkt an der Glocke heißt: Es gibt Hinweise (rot, wenn einer davon ernst ist). Ein Klick klappt die Liste auf. Hinweise mit Modulbezug öffnen beim Anklicken das passende Modul. Ohne Anmeldung zeigt die Glocke nichts.

| Titel | Text | Bedeutung | Was tun |
|---|---|---|---|
| – | „Keine Hinweise – alles in Ordnung.“ | nichts offen | nichts |
| „Zahlung offen“ / „Zahlung überfällig“ / „Erste Zahlung fehlgeschlagen“ / „Abo gesperrt“ / „Abo beendet“ / „Noch kein Abo eingerichtet“ | siehe Abschnitt 7.1 | Abo-Hinweis. Ein Klick öffnet deine Zahlungsseite, falls bekannt | Abschnitt 7 |
| „Server nicht erreicht“ | „Antwortet nicht seit <Zeit>.“ bzw. „Zuletzt erreicht <Zeit>.“, dazu „Ohne Server nehmen die Lister keine Produkte aus der Datenbank – der Browser-Lister wartet und macht danach von selbst weiter.“ | Der Server antwortet nicht | Internet prüfen, warten; bleibt es lange: Betreiber |
| „<Gerätename> meldet sich seit <Dauer> nicht“ | „Letzte Meldung <Zeit>. Läuft dort Chrome mit Cash Lister und Internet?“ | Ein anderes Gerät deines Kontos mit eingeschaltetem Schalter „Dieses Gerät ist ein Server“ (Einstellungen → Reiter „eBay & Rahmenbedingungen“ → Karte „Server-Modus“) hat sich seit mehr als 5 Minuten nicht gemeldet | Auf dem Gerät nachsehen: Läuft Chrome, ist Cash Lister angemeldet, gibt es Internet? |
| „Tracker angehalten“ | „Zu viele Artikel ohne Ergebnis – im Tracker nachsehen.“ | Die Notbremse des Trackers hat ausgelöst | Abschnitt 15.5 |
| „Lauf des Trackers unterbrochen“ | „Bei <Zahl> von <Zahl> – im Tracker fortsetzen.“ | Der Tracker-Tab wurde während eines Laufs geschlossen | Tracker öffnen und „Lauf starten“ klicken |
| „Tracker wartet“ | „Amazon hat kurz gesperrt, der Tracker macht danach von selbst weiter.“ | Automatische Pause wegen Amazon-Sperre | warten (Abschnitt 15.4) |
| „Browser-Lister-Tab geschlossen“ | „Der Lauf endet nach dem aktuellen Produkt.“ bzw. „Der Lauf endet nach der Pause.“ | Der Tab, aus dem der Lauf gestartet wurde, ist zu | Browser-Lister wieder öffnen und neu starten, wenn weitergelistet werden soll |
| „CSV-Lister-Lauf unterbrochen“ | „Der Tab wurde geschlossen. Beim nächsten Öffnen räumt der CSV-Lister auf.“ | CSV-Lister-Tab während eines Laufs geschlossen | CSV-Lister öffnen |
| „CSV-Lister: Hochladen fehlgeschlagen“ | Grund aus dem CSV-Lister | Upload gescheitert | Abschnitt 17.3 |
| „CSV-Lister angehalten“ | Grund aus dem CSV-Lister | Lauf technisch angehalten | Abschnitt 17.5 |
| „<Zahl> Produkte warten auf das eBay-Ergebnis“ | „Im CSV-Lister „Ergebnisse bei eBay abholen“.“ | Hochgeladene Produkte warten auf eBays Ergebnisdatei | Im CSV-Lister „Ergebnisse bei eBay abholen“ |
| „Einstellungen: zwei Geräte“ | „Ein anderes Gerät hat anders gesichert. Unter Einstellungen → Sicherung entscheiden, welcher Stand gilt.“ | Konflikt bei der Einstellungs-Sicherung | Abschnitt 8.4 |
| „Einstellungen zu groß für die Sicherung“ | „<Zahl> KB – sie werden nicht auf dem Server gesichert.“ | Einstellungen zu groß | Lange Beschreibungsvorlagen kürzen (8.4) |

### 6.2 Kennzahlen und Vorgänge

| Wo | Text | Bedeutung | Was tun |
|---|---|---|---|
| Kennzahl „Produkte in der Datenbank“ | „…“ und „wird geladen“ | Die Zahl wird gerade beim Server abgefragt | warten |
| Kennzahl „Produkte in der Datenbank“ | „–“ und „Server nicht erreichbar“ | Der Server antwortet nicht. Die Zahl ist unbekannt, die Datenbank ist **nicht** leer | Abschnitt 21 |
| Kennzahl „Produkte in der Datenbank“ | „–“ und „nach der Anmeldung sichtbar“ | Nicht angemeldet | anmelden |
| Kennzahl „Produkte in der Datenbank“ | „–“ und z. B. „Sitzung abgelaufen – bitte im Dashboard neu anmelden.“ | Der Server lehnt deine Sitzung ab. Die Anmeldekarte erscheint kurz danach | neu anmelden |
| Kennzahl „Produkte in der Datenbank“ | „<Zahl> werden noch auf den Server übertragen“ / Zusatz „· <Zahl> noch zu übertragen“ | Beim ersten Start von 46.0 wird die bisherige Liste dieses PCs auf den Server übertragen | warten, das läuft von selbst |
| Kennzahl „Produkte in der Datenbank“ | „leer – Produkte sammeln“ | Die Datenbank ist leer | Produkte sammeln (`produkte-finden-und-datenbank.md`) |
| Karte „Produkte sammeln“ | Marker „nicht erreichbar“, „alle in Arbeit“, „wird übertragen“, „leer“ | wie die Kennzahl; „alle in Arbeit“ = alle Produkte sind gerade von einem Lister entnommen | bei „alle in Arbeit“: warten oder Produkte nachsammeln |
| Karte „Browser-Lister“ | „Keine Antwort vom Hintergrunddienst“ | Der Hintergrunddienst hat nicht geantwortet | Seite neu laden; ggf. Hintergrunddienst neu laden |
| Karte „Browser-Lister“ | Marker „wartet auf den Server“, Text „Server nicht erreichbar seit <Zeit> – macht von selbst weiter · <Zahl> gelistet“ | Der Lauf pausiert, weil der Server nicht antwortet | warten |
| Karte „Browser-Lister“ | Marker „Tab geschlossen“, Text „Tab geschlossen – der Lauf endet nach dem aktuellen Produkt“ | Lister-Tab zu | Browser-Lister wieder öffnen und neu starten |
| Karte „Browser-Lister“ | Marker „Pause bis <Uhrzeit> – Tab zu“, Text „Tab geschlossen – der Lauf endet nach der Pause“ | Zeitschaltung macht Pause, aber der Tab ist zu | wie oben |
| Karte „Browser-Lister“ / „Tracker“ | Marker „meldet sich nicht“ | Der Stand kommt von einem Server-Gerät, das sich seit mehr als 5 Minuten nicht gemeldet hat | auf dem Gerät nachsehen |
| Karte „Tracker“ | Marker „wartet (Amazon-Sperre)“ | automatische Pause (15.4) | warten |
| Karte „Tracker“ | Marker „angehalten“ | Notbremse (15.5) | Abschnitt 15.5 |
| Karte „Tracker“ | Marker „unterbrochen“, Text „Unterbrochen bei <Zahl> von <Zahl> – im Tracker fortsetzen“ | Tracker-Tab während des Laufs geschlossen | Tracker öffnen, „Lauf starten“ |
| Karte „CSV-Lister“ | Marker „unterbrochen“, Text „Lauf von <Zeit> unterbrochen – der Tab wurde geschlossen“ | CSV-Lister-Tab zu | CSV-Lister öffnen |

### 6.3 Checkliste „Heute“

| Punkt | Text mit Warnzeichen | Was tun |
|---|---|---|
| „Genug Produkte in der Datenbank“ | „Produkt-Datenbank: Server nicht erreichbar“ | Abschnitt 21 |
| „Genug Produkte in der Datenbank“ | „Alle <Zahl> Produkte sind gerade in Arbeit – Produkte sammeln“ / „Die Datenbank ist leer – Produkte sammeln“ | Produkte sammeln |
| „Preise & Bestand abgeglichen“ | „Angehalten bei …“, „Unterbrochen bei …“, „Pausiert bei …“, „Keine Meldung bei …“ | Tracker öffnen (Abschnitt 15) |
| „Einstellungen gesichert“ | „Ein anderes Gerät hat anders gesichert – unter Einstellungen → Sicherung entscheiden“ | Abschnitt 8.4 |
| „Einstellungen gesichert“ | „Zu groß für die Sicherung (<Zahl> KB)“ | Vorlagen kürzen |
| „Einstellungen gesichert“ | „Server nicht erreicht – wird wiederholt“ | warten; die Extension versucht es von selbst wieder |
| „Einstellungen gesichert“ | „Erst nach der Anmeldung“ / „Stand nicht verfügbar“ / „Noch nicht gesichert“ | anmelden bzw. kurz warten |

---

## 7. Abo: Warnleiste, Karte „Dein Abo“, Abo-Sperre

Cash Lister läuft als Monatsabo. Alles rund um Preise, Zahlung und Kündigen steht in `konto-und-installation.md` (Abschnitt „Abo und Zahlung“). Hier nur die Meldungen. Warnleiste und Karte erscheinen nur, wenn du angemeldet bist und für dein Konto ein Abo abgerechnet wird.

### 7.1 Warnleiste oben im Dashboard (und in der Glocke)

Die Leiste steht oben im Dashboard, orange oder rot. Rechts hat sie einen Knopf zur Zahlungsseite: „Jetzt bezahlen“ bzw. „Abo einrichten“.

| Titel | Text | Bedeutung | Was tun |
|---|---|---|---|
| „Zahlung offen“ | „Ohne Zahlung wird dein Zugang nach dem <Datum> gesperrt.“ bzw. „Die Sperre ist fällig – bitte jetzt bezahlen.“ | Eine Zahlung ist noch nicht eingegangen | Auf „Jetzt bezahlen“ klicken und bezahlen |
| „Zahlung überfällig“ | „Die Abbuchung hat nicht geklappt. …“ und der Satz zur Sperre wie oben | Die Abbuchung ist gescheitert | Zahlungsart prüfen und bezahlen („Jetzt bezahlen“ oder „Abo verwalten“) |
| „Erste Zahlung fehlgeschlagen“ | „Die erste Abbuchung hat nicht geklappt. …“ und der Satz zur Sperre | Die erste Abbuchung ist gescheitert | wie oben |
| „Abo gesperrt“ | „Ein Shop deines Abos ist wegen einer offenen Zahlung gesperrt.“ | Ein anderer Shop deines Abos ist gesperrt | Bezahlen; bei Fragen Betreiber |
| „Noch kein Abo eingerichtet“ | „Dein Zugang läuft bis <Datum>. Richte das Abo auf der Zahlungsseite ein, damit es weitergeht.“ bzw. „Dein Zugang ist abgelaufen. …“ | Erscheint in den letzten 7 Tagen vor dem Ende des Zugangs | Auf „Abo einrichten“ klicken |
| „Abo beendet“ | wie bei „Noch kein Abo eingerichtet“ | Das Abo ist beendet | Abo neu einrichten oder beim Betreiber melden |

Fehlt der Knopf zur Zahlungsseite, ist für dein Konto kein Zahlungslink bekannt. Dann den Betreiber nach deinem persönlichen Zahlungslink fragen.

### 7.2 Karte „Dein Abo“

Wo: unten im Dashboard. Sie zeigt einen Marker, einen Statustext, „Shops“, „Monatlich“ (netto, mit „zzgl. 19 % USt“) und je nach Stand „Erste Abbuchung“, „Gekündigt zum“ oder „Zugang bis“.

| Marker | Bedeutung |
|---|---|
| „aktiv“ | Abo läuft, bezahlt |
| „eingerichtet“ | Abo eingerichtet, erste Abbuchung kommt noch |
| „Zahlung unterwegs“ | Eine Lastschrift ist unterwegs |
| „gekündigt“ | Gekündigt; der Zugang läuft bis zum genannten Tag |
| „Zahlung offen“ / „überfällig“ / „Zahlung fehlgeschlagen“ | Zahlung fehlt; siehe 7.1 |
| „kein Abo“ / „beendet“ | Kein laufendes Abo |
| „gesperrt“ | Gesperrt wegen offener Zahlung |

Der **Statustext** neben dem Marker kommt vom Server. Beispiele aus dem aktuellen Stand: „Aktiv bis <Datum> – nächste Abbuchung <Datum>“, „Eingerichtet – erste Abbuchung am <Datum>“, „Lastschrift unterwegs – Sperre spätestens <Datum>“, „Gekündigt zum <Datum> – Zugang bis <Datum>“, „Aktiv, Zahlung offen – Sperre ab <Datum>“, „Überfällig seit <Datum> – Sperre ab <Datum>“, „Erste Zahlung fehlgeschlagen – Sperre ab <Datum>“, „Kein Abo – Zugang bis <Datum>“, „Abo beendet – Zugang bis <Datum>“, „Gesperrt seit <Datum>“. Ist eine Sperre schon fällig, steht statt „Sperre ab …“ der Zusatz „überfällig – Sperre fällig seit <Datum>“. **Nicht sicher belegt:** ob der Server diese Texte künftig anders formuliert – gib weiter, was beim Kunden dasteht.

Laut AGB (https://cash-lister.de) kann der Zugang gesperrt werden, wenn das Entgelt drei Tage nach Fälligkeit nicht bezahlt ist. Den genauen Tag zeigt die Karte bzw. die Warnleiste.

### 7.3 Knopf „Abo verwalten“

Wo: Karte „Dein Abo“. Er öffnet das **Kundenportal** im neuen Tab (dort: Rechnungen, Zahlungsart ändern, Kündigen zum Ende der Abrechnungsperiode). Die Meldungen stehen in der Zeile unter dem Knopf; nach etwa 10 Sekunden kehrt dort der Erklärtext „Kündigen, Zahlungsart ändern, Rechnungen: alles im Kundenportal unter „Abo verwalten“.“ zurück.

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Kundenportal wird geöffnet …“ | läuft | warten |
| „Kundenportal im neuen Tab geöffnet.“ | geklappt | im neuen Tab weiter |
| „Noch kein Abo eingerichtet – das geht über die Zahlungsseite.“ | Es gibt noch kein Abo; daneben erscheint der Link „Zahlungsseite“ | Über „Zahlungsseite“ das Abo einrichten |
| „Noch kein Abo eingerichtet – bitte beim Betreiber melden.“ | Kein Abo und kein Zahlungslink bekannt | Betreiber nach dem Zahlungslink fragen |
| „Bitte <Zahl> Sekunden warten.“ | Zu schnell hintereinander geklickt | kurz warten, dann erneut |
| „Server nicht erreichbar – bitte später erneut versuchen.“ | Keine Verbindung zum Server | Internet prüfen, später erneut |
| „Kundenportal gerade nicht erreichbar – bitte später erneut versuchen.“ | Das Kundenportal ließ sich gerade nicht öffnen | später erneut; bleibt es: Betreiber |
| „Nicht angemeldet.“ | Nicht angemeldet | anmelden |
| „Zugang gesperrt.“ oder ein Sperrtext vom Server | Zugang abgeschaltet oder Abo gesperrt | Abschnitt 7.4 bzw. Betreiber |

Kommst du aus dem Kundenportal oder von der Zahlungsseite zurück ins Dashboard, holt es den Abo-Stand neu.

### 7.4 Abo gesperrt

**Woran du es erkennst:** Die Anmeldekarte im Dashboard zeigt den Titel „Abo gesperrt“ und einen Text vom Server, z. B. „Abo abgelaufen – bitte die Zahlung erneuern oder beim Betreiber melden.“ (fehlt der Text: „Bitte die Zahlung erneuern oder beim Betreiber melden.“). In der Seitenleiste steht „Abo gesperrt“ mit „Details im Dashboard“. Die Module sind gesperrt. Ein laufender Browser-Lister endet mit „Browser-Lister beendet: Abo gesperrt – bitte im Dashboard nachsehen. Danach neu starten.“

**Was tun:**
1. In der Anmeldekarte auf „Zur Zahlungsseite“ klicken (der Knopf erscheint, wenn dein Zahlungslink bekannt ist) und die offene Zahlung erledigen.
2. Danach im Dashboard wieder anmelden („Nach der Zahlung hier wieder anmelden.“). Laut AGB hebt der Betreiber die Sperre nach Eingang der Zahlung in der Regel automatisch auf.
3. Kommt beim Anmelden weiter „Anmeldung abgelehnt: Abo gesperrt.“, ist die Zahlung noch nicht verbucht. Etwas warten und erneut versuchen. Bleibt es dabei oder fehlt der Knopf „Zur Zahlungsseite“: beim Betreiber melden.

Die Hilfe kann keine Sperre aufheben und keinen Zahlungsstand prüfen.

---

## 8. Einstellungen

Wo: Seitenleiste → „Einstellungen“ (oder Rechtsklick auf das Cash-Lister-Symbol → „Optionen“). Die Seite heißt „Einstellungen“ und hat sechs Reiter: „Preise & Listing“, „Produkt-Filter“, „eBay & Rahmenbedingungen“, „Beschreibungsvorlage“, „KI“, „Sicherung“. Ausführlich: `einstellungen.md`.

### 8.1 Knopf „Speichern“ und Blacklist

| Meldung | Bedeutung |
|---|---|
| Fenster „Einstellungen gespeichert“ | Nur eine Bestätigung. Jede Änderung wird schon beim Verlassen des Feldes bzw. beim Umlegen eines Schalters gespeichert |
| „Wörter: <Zahl>“ (Reiter „Produkt-Filter“, Karte „Blacklist“) | Anzahl der Einträge in „Meine Liste“. Doppelte und leere Zeilen zählen nicht mit |

### 8.2 Karte „Server & Produkt-Vergabe“ (Reiter „eBay & Rahmenbedingungen“)

**Die Produktvergabe** sorgt dafür, dass nicht zwei Kunden dasselbe Amazon-Produkt auf eBay listen. Wer ein Produkt zuerst übernimmt, bekommt es. Für die anderen gilt es als vergeben.

Statuszeile neben dem Knopf „Verbindung prüfen“ (wird beim Öffnen der Seite gesetzt; nach dem Anmelden die Seite neu laden):

| Text | Bedeutung | Was tun |
|---|---|---|
| „● Produkt-Vergabe: AN (über deine Anmeldung)“ (grün) | Du bist angemeldet | nichts |
| „● Produkt-Vergabe: AUS – keine Server-Adresse hinterlegt.“ (rot) | **Trotz des Wortlauts heißt das fast immer: Du bist nicht angemeldet.** | Im Dashboard anmelden, dann diese Seite neu laden (F5). Nicht selbst eine Adresse eintragen. Steht der Text trotz Anmeldung noch da: Betreiber fragen |
| „● Produkt-Vergabe: AUS – nicht angemeldet. Es wird NICHTS reserviert!“ (rot) | Nicht angemeldet. Kommt auf der Einstellungsseite praktisch nicht vor: Ohne Anmeldung steht dort der Text darüber („… keine Server-Adresse hinterlegt.“) | im Dashboard anmelden |

Dazu der feste Hinweis auf der Seite: „Achtung: Ohne Anmeldung ist die Produkt-Vergabe komplett aus. Es kommt keine Fehlermeldung – es wird dann einfach nichts mehr reserviert.“

**Gut zu wissen:** Diese Statuszeile prüft nur, ob eine Anmeldung gespeichert ist. Ist dein Zugang abgeschaltet oder das Abo gesperrt, kann hier trotzdem „AN“ stehen. Maßgeblich ist der Verbindungskasten in der Seitenleiste (Abschnitt 5).

**Knopf „Verbindung prüfen“** (Ergebnis darunter):

| Text | Bedeutung | Was tun |
|---|---|---|
| „prüfe …“ | läuft | warten |
| „OK – angemeldet als „<Name>“, <Zahl> Produkte reserviert.“ (grün) | Verbindung und Anmeldung in Ordnung; die Zahl sind die Produkte, die gerade für dich reserviert sind | nichts |
| „Keine Server-Adresse hinterlegt.“ | Wie bei der Statuszeile: heißt fast immer **nicht angemeldet** | Im Dashboard anmelden, Seite neu laden, erneut prüfen |
| „Nicht angemeldet – bitte im Dashboard anmelden.“ | Nicht angemeldet | anmelden |
| „Anmeldung abgelehnt (401) – bitte im Dashboard neu anmelden.“ | Die Sitzung ist abgelaufen | Im Dashboard abmelden (Kontofeld → „Abmelden“) und neu anmelden |
| „Zugang ist abgeschaltet (403).“ | Zugang abgeschaltet oder Abo gesperrt | Dashboard ansehen; Abschnitt 4.1 bzw. 7.4 |
| Text, der mit „Server erreichbar, kennt aber …“ beginnt | Der Server antwortet, kann diese Prüfung aber nicht | An den Betreiber weitergeben, nicht selbst lösbar |
| „Server antwortet mit HTTP <Zahl>.“ | Unerwartete Antwort | später erneut; bleibt es: Betreiber |
| „Keine Antwort: <technischer Grund> …“ | Keine Verbindung zum Server | Internet prüfen, später erneut; das Feld „Server-Adresse“ nur auf Ansage des Betreibers ändern |

Nach einer Prüfung steht unter dem Ergebnis eine Zeile „Server: <Adresse>“. Sie zeigt nur, welche Adresse benutzt wurde. Die Hilfe nennt keine Serveradressen.

### 8.3 Reiter „Sicherung“, Karte „Als Datei“

| Meldung | Bedeutung | Was tun |
|---|---|---|
| Fenster „Ungültige Einstellungsdatei.“ | Die Datei ist lesbar, aber keine Einstellungsdatei | Die richtige Datei wählen (z. B. `einstellungen-privat-<Datum>.json` aus „Einstellungen exportieren“) |
| Fenster „Die Datei ist kein gültiges JSON.“ | Die Datei ist keine Einstellungsdatei oder beschädigt | Richtige Datei wählen |
| Fenster „Import fehlgeschlagen: <Grund>“ | Chrome konnte nicht speichern | Chrome neu starten, erneut versuchen |
| Fenster „Einstellungen importiert (<Zahl> Einträge). Lade offene Seiten von Cash Lister (z. B. den Tracker) bitte neu.“ | Import hat geklappt | Offene Tabs von Cash Lister neu laden (F5) |

Beim Exportieren selbst gibt es keine Meldung: Die Datei landet im Download-Ordner. Die Karte warnt: „Enthält API-Schlüssel und Lizenz – nicht weitergeben.“

### 8.4 Reiter „Sicherung“, Karte „Auf dem Server“

Die Standzeile steht unter den Knöpfen. Ohne Anmeldung bleibt sie leer. Ausführlich zur Sicherung: `einstellungen.md` und `konto-und-installation.md`.

**Standanzeige (ohne Klick):**

| Text | Bedeutung | Was tun |
|---|---|---|
| „Auf dem Server gesichert: <Datum, Uhrzeit>“ | Deine Einstellungen sind gesichert | nichts |
| „Noch nicht auf dem Server gesichert.“ | Es gibt noch keine Sicherung von diesem Gerät | Kurz nach dem ersten Anmelden normal. Die Extension sichert von selbst, etwa 30 Sekunden nach einer Änderung. Steht es dauerhaft da: Betreiber fragen |
| „… · Aktueller Stand zu groß für die Sicherung (<Zahl> KB, erlaubt 512 KB) – Vorlagen oder Bild-Templates kürzen.“ | Deine Einstellungen sind zu groß; der aktuelle Stand wird nicht gesichert | Lange Beschreibungsvorlagen kürzen (große eingebettete Bilder sind die häufigste Ursache) |
| „… · Vom Server übernommen: <Datum, Uhrzeit>“ | Die Extension hat deine gesicherten Einstellungen auf dieses Gerät geholt (z. B. nach einer Neuinstallation). Erscheint einmal | nichts |
| „Achtung: Auf dem Server liegt eine Sicherung vom <Datum> mit <Zahl> Einstellungen[ von einem anderen Gerät]. Dieses Gerät hat <Zahl> Einstellungen und wurde noch nicht gesichert. Bitte entscheiden: "Einstellungen vom Server holen" oder "Dieses Gerät auf den Server sichern".“ | **Konflikt:** Auf dem Server liegt schon eine Sicherung (oft von einem anderen PC oder Chrome-Profil), und dieses Gerät hat eigene Einstellungen. Es wird nichts überschrieben, bis du entscheidest. Dazu erscheint der Knopf „Dieses Gerät auf den Server sichern“ | Sollen die Einstellungen von dort gelten: „Einstellungen vom Server holen“. Sollen die dieses Geräts gelten: „Dieses Gerät auf den Server sichern“ |

**Nach Klick auf „Einstellungen vom Server holen“:**

| Text | Bedeutung | Was tun |
|---|---|---|
| „Frage den Server …“ | läuft | kurz warten |
| „Nicht möglich: nicht angemeldet“ | Nicht angemeldet | anmelden |
| „Nicht möglich: Server nicht erreichbar“ | Keine Verbindung zum Server | Internet prüfen, später erneut |
| „Nicht möglich: HTTP <Zahl>“ | Unerwartete Antwort | später erneut; bleibt es: Betreiber |
| „Nicht möglich: keine Antwort“ (oder ein technischer Text von Chrome) | Der Hintergrunddienst hat nicht geantwortet | Hintergrunddienst neu laden (Abschnitt 3) |
| „Auf dem Server liegt noch keine Sicherung für dieses Konto.“ | Für deinen Zugang ist nichts gesichert | nichts zu holen |
| Fenster „Einstellungen vom Server übernehmen? Server: <Datum> (<Zahl> Einstellungen) Dieses Gerät: <Zahl> Einstellungen. Die Einstellungen auf diesem Gerät werden ersetzt. Schlüssel (OpenAI usw.) und die Produkt-Datenbank bleiben.“ | Sicherheitsfrage | „OK“ = übernehmen, „Abbrechen“ = nichts ändern |
| „Übernommen (<Zahl> Einstellungen). Lade offene Seiten von Cash Lister bitte neu.“ | Fertig | Offene Tabs von Cash Lister neu laden |
| „Übernehmen fehlgeschlagen.“ | Konnte nicht übernommen werden | Erneut versuchen; Hintergrunddienst neu laden; bleibt es: Betreiber |

**Nach Klick auf „Dieses Gerät auf den Server sichern“** (nur bei Konflikt sichtbar):

| Text | Bedeutung | Was tun |
|---|---|---|
| Fenster „Die Sicherung auf dem Server (<Zahl> Einstellungen vom <Datum>) wird durch die <Zahl> Einstellungen dieses Geräts ersetzt. Fortfahren?“ | Sicherheitsfrage | „OK“ = ersetzen |
| „Sichere …“ | läuft | warten |
| „Sichern fehlgeschlagen: <Grund>“ | Grund z. B. „nicht angemeldet“, „Server nicht erreichbar“, „zu gross“, „nichts zu sichern“, „HTTP <Zahl>“ oder „keine Antwort“ | je nach Grund: anmelden / später erneut / Vorlagen kürzen / Hintergrunddienst neu laden; bleibt es: Betreiber |

---

## 9. Browser-Lister

Wo: Seitenleiste → „Browser-Lister“ (früher „Bulk-Lister“). Ausführlich: `listen-auf-ebay.md`.

### 9.1 Fenster beim Klick auf „Starten“

| Meldung | Wann / Bedeutung | Was tun |
|---|---|---|
| „Nicht angemeldet oder Zugang deaktiviert - bitte im Dashboard anmelden.“ | Du bist nicht angemeldet, dein Zugang ist abgeschaltet oder dein Abo gesperrt | Dashboard öffnen, Anmeldestand prüfen (Abschnitt 4.1 / 7.4) |
| „Bitte oben eintragen, wie viele Angebote entstehen sollen.“ | Im Feld „Wie viele Angebote“ steht 0 oder nichts | Eine Zahl größer als 0 eintragen |
| „Nicht angemeldet oder Sitzung abgelaufen - bitte im Dashboard anmelden, dann starten.“ | Bei „Produkte aus“ = „Produkt-Datenbank“: der Server lehnt die Sitzung ab | Im Dashboard neu anmelden |
| „Server nicht erreichbar - die Produkt-Datenbank liegt auf dem Server. Bitte später erneut starten.“ | Die Produkt-Datenbank ist gerade nicht erreichbar | Internet prüfen, später erneut |
| „Produkt-Datenbank nicht abrufbar: <Grund>“ | Anderer Fehler beim Abfragen der Datenbank | Grund lesen; bleibt es: Betreiber |
| „Die Produkt-Datenbank ist leer - erst Produkte einsammeln.“ | Die Datenbank ist leer | Erst Produkte sammeln (`produkte-finden-und-datenbank.md`) |
| „Alle <Zahl> Produkte der Datenbank sind gerade in Arbeit - auf einem anderen Gerät oder im CSV-Lister. Später erneut starten.“ | Es gibt Produkte, aber gerade ist keines frei. **„In Arbeit“** heißt: ein Lister (auf irgendeinem Gerät deines Kontos) hat das Produkt gerade entnommen | Später erneut starten oder neue Produkte sammeln |
| „Der Konkurrenz-Scanner hat noch keine Funde.“ | Bei „Produkte aus“ = „Konkurrenz-Scanner“, aber die Fundliste ist leer | Erst mit dem Konkurrenz-Scanner suchen oder auf „Produkt-Datenbank“ umstellen |

### 9.2 Während und nach dem Lauf

| Meldung | Wo / Bedeutung | Was tun |
|---|---|---|
| „<Zahl> verfügbar“ bzw. „<Zahl> verfügbar · <Zahl> in Arbeit“ | Neben „Produkte aus“: so viele **freie** Produkte hat die Quelle noch | nichts |
| „? verfügbar“ | Keine Antwort vom Hintergrunddienst | Seite neu laden, ggf. Hintergrunddienst neu laden |
| „nicht angemeldet – bitte im Dashboard anmelden“ | Neben „Produkte aus“ | anmelden |
| „Server nicht erreichbar – Bestand gerade nicht abrufbar“ | Neben „Produkte aus“ | Internet prüfen, warten |
| „⚠ Server nicht erreichbar – Lister pausiert, macht von selbst weiter.“ (auch mit „(Produkt-Datenbank noch nicht bereit).“ oder „(HTTP <Zahl>).“ am Ende) | Neben „Produkte aus“: Der laufende Lauf wartet auf den Server. Kein Produkt wird ohne Server gelistet. Etwa alle 30 Sekunden versucht er es erneut | Warten. Mit „Stoppen & zurücksetzen“ kannst du den Lauf beenden |
| Fenster „Fertig - die eingestellte Zahl an Angeboten ist erreicht.“ | Die Zahl bei „Wie viele Angebote“ ist erreicht (nur ohne Zeitschaltung) | nichts |
| „Fertig: <Zahl> von <Zahl> gelistet.“ | Abschlusszeile unter dem Fortschrittsbalken | nichts |
| „Quelle aufgebraucht - <Zahl> von <Zahl> gelistet. Erst neue Produkte einsammeln, dann noch einmal starten.“ (orange) | Die Quelle ist leer, bevor die Zielzahl erreicht war | Neue Produkte sammeln, dann neu starten |
| „<Zahl> von <Zahl> gelistet. Browser-Lister beendet: <Grund> Danach neu starten.“ (orange) | Der Lauf endete vorzeitig, weil die Anmeldung weg ist oder der Server die Anfrage grundsätzlich ablehnt. Grund z. B. „Sitzung abgelaufen – bitte im Dashboard neu anmelden.“, „Nicht angemeldet – bitte im Dashboard anmelden.“, „Zugang abgeschaltet – bitte beim Betreiber melden.“, „Abo gesperrt – bitte im Dashboard nachsehen.“ oder ein Text, der mit „Der Claims-Server lehnt die Anfrage ab (HTTP <Zahl> …“ beginnt und mit „– bitte die Extension aktualisieren oder beim Betreiber melden.“ endet. Was schon in Arbeit war, wird noch fertig | Wie im Grund beschrieben handeln, dann neu starten. Beim Text „… lehnt die Anfrage ab …“: prüfen, ob die neueste Version läuft (Versionsnummer links unten in der Seitenleiste), sonst Screenshot an den Betreiber |
| „⏱ Zeitschaltung: <Zahl> von <Zahl> dieser Runde gelistet. Danach <Dauer> Pause.“ | Nur bei eingeschalteter „Zeitschaltung“: Stand der aktuellen Runde | nichts |
| „😴 Schläft – Kontingent erreicht (<Zahl> von <Zahl>). Weiter in <Zeit>.“ | Zeitschaltung: Die Runde ist voll, der Lauf macht Pause und geht danach von selbst weiter | Warten, oder mit „Stoppen & zurücksetzen“ beenden |
| „Aktuell: nur FBA an · nur chinesische Verkäufer aus · GPSR aus“ (die Werte wechseln) | Karte „Tabs und Filter“: welche Produkt-Filter aus den Einstellungen gerade gelten | Ändern über „Ändern“ daneben |
| „<Zahl> erfolgreich gelistet“, „<Zahl> fehlgeschlagen“ | Zähler | Gründe für Fehlschläge im Statusbericht (Abschnitt 10) |

**FBA** heißt „Fulfillment by Amazon“: Amazon lagert und verschickt die Ware selbst. **GPSR** sind die EU-Pflichtangaben zu Hersteller und verantwortlicher Person.

---

## 10. Statusbericht – Meldungen je Produkt

Wo: Browser-Lister → Knopf „Statusbericht“ oben rechts. Spalten: „#“, „Amazon-Link“, „Status“, „Meldung“, „eBay-Link“. In „Status“ steht „gelistet“ (grün), „fehlgeschlagen“ (rot) oder „Hinweis“ (eine Zeile zum Lauf, kein Produkt). Die Liste aktualisiert sich nicht von selbst: für neue Einträge die Seite neu laden (F5). Der Knopf „Leeren“ leert sie sofort, ohne Rückfrage. Bei jedem Start und bei „Stoppen & zurücksetzen“ beginnt sie ebenfalls leer. Ausführlich mit Tipps: `listen-auf-ebay.md` (Abschnitt „Der Statusbericht und alle Meldungen“).

Viele Meldungen beginnen mit einem Leerzeichen. Das hat keine Bedeutung.

### 10.1 Erfolg, Produktvergabe und Hinweiszeilen

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Erfolgreich gelistet!“ | Das Angebot ist auf eBay eingestellt | nichts |
| „Produkt bereits von einem anderen Nutzer vergeben“ | Nur bei Produkten aus dem Konkurrenz-Scanner: Ein anderer Kunde hat dieses Produkt schon. Es wird nicht gelistet | nichts; das Produkt ist nicht für dich |
| „Abgebrochen: <Grund>“ | Beim Öffnen der Tabs oder im Ablauf ist ein unerwarteter Fehler passiert. Das Produkt wurde wieder freigegeben | Erneut versuchen; kommt es oft: Screenshot an den Betreiber |
| „Nachgelagerter Fehler: <Grund>“ | Das Ergebnis stand schon fest und ist verbucht; danach ist noch ein Fehler passiert | Im eBay-Verkäuferbereich nachsehen, ob das Angebot da ist. Kommt es oft: Betreiber |
| Status „Hinweis“: „Server nicht erreichbar – Lister pausiert, macht von selbst weiter.“ (auch mit „(Produkt-Datenbank noch nicht bereit).“ oder „(HTTP <Zahl>).“) | Der Lauf wartet auf den Server | warten |
| Status „Hinweis“: „Server wieder erreichbar – Lister läuft weiter (Pause etwa <Zahl> Min.).“ | Die Pause ist vorbei | nichts |
| Status „Hinweis“: „Browser-Lister beendet: <Grund> Danach neu starten.“ | Der Lauf endete, weil die Anmeldung weg ist oder der Server die Anfrage ablehnt (siehe 9.2) | wie dort |

### 10.2 Prüfungen auf der Amazon-Seite (vor dem Listen)

Bei diesen Meldungen wird das Produkt **nicht** gelistet. Im Amazon-Tab steht dazu ein Warn-Titel (Abschnitt 11).

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Produktseite existiert nicht“ | Die Seite ist keine richtige Produktseite (Produkt gelöscht, Fehlerseite, nicht geladen) | Link selbst öffnen und ansehen |
| „Produkt ist schon gelistet (Duplikat)“ | Du hast dieses Produkt aus diesem Chrome-Profil schon einmal erfolgreich gelistet | nichts; Schutz vor Doppel-Angeboten |
| „Produkt enthält ein Wort aus der Blacklist: <Wort>“ | Ein Eintrag aus deiner Blacklist (Einstellungen → Reiter „Produkt-Filter“ → Karte „Blacklist“, Feld „Meine Liste“) steht als ganzes Wort im Amazon-Titel, in der Beschreibung, in den Stichpunkten oder in den Werten der Produktmerkmale. Teile eines längeren Wortes zählen nicht | Wenn das Wort nicht gemeint war: Liste anpassen |
| „ASIN und Adresse (URL) passen nicht zusammen“ | Amazon hat auf ein anderes Produkt oder eine andere Variante umgeleitet. Die **ASIN** ist die 10-stellige Amazon-Produktnummer | Link prüfen, ggf. die richtige Variante neu importieren |
| „Produkt hat eine Mindestbestellmenge“ | Das Produkt hat eine Mindestbestellmenge über 1 | nichts |
| „Produkt ist nicht auf Lager“ | Laut Amazon nicht auf Lager, **oder** die Lieferzeit ist länger als „Max. verlängerte Lieferzeit“ (Einstellungen → „Produkt-Filter“ → „Amazon-Filter“, Vorgabe 20 Tage) | Später erneut; Wert prüfen (Hinweis unten) |
| „Produkt wird international versendet“ | Amazon liefert das Produkt nur international | nichts |
| „Nicht von Amazon versendet (Versand: <Versender>)“ | Der Schalter „Nur FBA“ (Einstellungen → „Produkt-Filter“ → „Beim Listen“) ist an, und in der **Buybox** (dem Kaufkasten rechts auf der Amazon-Seite) verschickt jemand anderes | nichts, oder den Schalter ausschalten |
| „Versender auf der Produktseite nicht erkennbar“ | „Nur FBA“ ist an, aber in der Buybox steht keine Versandangabe (oft: derzeit nicht lieferbar) | Seite selbst ansehen. Passiert es bei sehr vielen Produkten: Betreiber informieren (vielleicht hat Amazon die Seite umgebaut) |
| „Produkt hat keinen kostenlosen Versand“ | Kein kostenloser Versand in der Buybox | nichts |
| „Produkt ist gebraucht“ | Das Angebot in der Buybox ist gebraucht | nichts |
| „Amazon-Preis zu hoch (Filter „Preis bis“)“ | Amazon-Preis liegt über „Preis bis“ (Einstellungen → „Produkt-Filter“ → „Amazon-Filter“) | Grenze und Schalter daneben prüfen |
| „Amazon-Preis zu niedrig (Filter „Preis ab“)“ | Amazon-Preis liegt unter „Preis ab“ | Grenze und Schalter prüfen |
| „Kein chinesischer Verkäufer“ | „Nur chinesische Verkäufer“ ist an, und der Verkäufer gilt nicht als chinesisch | nichts, oder Schalter ausschalten |
| „Keine GPSR-Angaben gefunden“ | „GPSR-Angaben übernehmen“ ist an, aber Amazon zeigt keine Herstellerangaben | nichts, oder Schalter ausschalten |
| „nicht angemeldet“, dazu auf der Amazon-Seite das Fenster „Nicht angemeldet - bitte im Dashboard anmelden.“ | Deine Anmeldung ist während des Laufs weggefallen (auch bei abgeschaltetem Zugang oder Abo-Sperre) | Im Dashboard Anmeldestand prüfen, dann neu starten |

**Hinweis zu „Max. verlängerte Lieferzeit“:** Beim Listen (und im Tracker) zählt immer der eingetragene Wert, auch wenn der Schalter daneben aus ist. Ist kein Wert eingetragen, gelten 20 Tage. Steht auf der Amazon-Seite der englische Hinweis „Extended delivery time“, gilt das Produkt ebenfalls als nicht lieferbar. Nur beim Knopf „→ Datenbank“ auf Amazon-Suchseiten wirkt der Schalter. Wer längere Lieferzeiten zulassen will, muss also die Zahl erhöhen; den Schalter auszuschalten reicht beim Listen nicht. **Nicht sicher belegt:** ob dieses Verhalten so bleiben soll. Bei Fragen dazu an den Betreiber verweisen.

### 10.3 Titel und KI

Seit 46.0 schreibt immer die KI den Titel. Ausnahme: Produkte aus dem Konkurrenz-Scanner bekommen den Titel des eBay-Verkäufers.

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „KI-Titel ist leer“ | Die KI hat auch nach mehreren Versuchen keinen Titel geliefert. Häufigste Gründe: kein OpenAI-Schlüssel, Schlüssel ungültig, kein Guthaben bei OpenAI | Schlüssel und Guthaben prüfen (Abschnitt 18) |
| „Titel-Erstellung fehlgeschlagen“ | Der Titel, mit dem gelistet werden sollte, enthält die Buchstabenfolge „error“ – auch als Teil eines Wortes (z. B. „Terror“). Das gilt für KI-Titel und für übernommene Titel aus dem Konkurrenz-Scanner. Das Produkt wird übersprungen | Bei KI-Titeln kann ein neuer Versuch helfen, weil die KI einen anderen Titel schreibt. Bei Produkten aus dem Konkurrenz-Scanner kommt immer derselbe Titel: Produkt überspringen |
| „Listen fehlgeschlagen – keine verwertbare Antwort der Amazon-Seite“ | Der Amazon-Tab hat nach dem Laden innerhalb von etwa 4 Minuten kein Ergebnis geliefert (Seite lädt nicht, bleibt hängen oder das Skript ist abgestürzt) | Link selbst öffnen; erneut versuchen |
| Eine OpenAI-Meldung (z. B. „OpenAI-Guthaben leer: …“) | Steht **statt** „Listen fehlgeschlagen – …“, wenn kurz vorher (innerhalb von 90 Sekunden) ein KI-Fehler auftrat | Abschnitt 18 |

### 10.4 Auf der eBay-Seite

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Übersprungen: dieses Amazon-Produkt wird auf eBay bereits von jemand anderem angeboten (Bildabgleich, Abstand <Zahl>)“ | Der Schalter „Bildabgleich gegen fremde Angebote“ (Einstellungen → „Produkt-Filter“ → „Beim Listen“) ist an, und eBay zeigt ein fremdes Angebot mit gleichem Bild | nichts; oder den Schalter ausschalten |
| „„Neu: Sonstige" in dieser Kategorie nicht verfügbar (nur-Neu-Sonstige aktiv)“ | „NUR „Neu: Sonstige“ listen“ (Einstellungen → „Preise & Listing“ → „Preise“) ist an, aber die eBay-Kategorie bietet diesen Zustand nicht an | nichts, oder den Schalter ausschalten |
| „Zustand nicht wählbar: Kachel „Neu mit Etikett“ nicht gefunden“ | Bei der Zustandsauswahl per Kacheln fand die Extension „Neu mit Etikett“ nicht | nichts; das Produkt passt nicht |
| „Nicht eingestellt: Fehler beim Ausfüllen des eBay-Formulars (Schritt „<Schritt>"): <Grund>“ | Beim Ausfüllen ist etwas schiefgegangen; der Schritt steht dabei | Erneut versuchen. Passiert es oft beim selben Schritt: Screenshot an den Betreiber |
| „Beschreibung konnte nicht in den eBay-Editor geschrieben werden: <Grund> - Listing abgebrochen, damit es nicht leer online geht.“ | Die Beschreibung kam nicht im eBay-Editor an | Beschreibungsvorlage prüfen (`einstellungen.md`, Reiter „Beschreibungsvorlage“), erneut versuchen |
| „Nicht eingestellt: eBay verlangt Angebotsgebühren (Einstellung „Auch mit Angebotsgebühr einstellen“ ist aus)“ | eBay würde eine Angebotsgebühr über 0 verlangen, und automatisches Einstellen bei Gebühren ist aus | Gebühren bei eBay prüfen. Wer trotzdem einstellen will: Schalter „Auch mit Angebotsgebühr einstellen“ (Einstellungen → „eBay & Rahmenbedingungen“ → „Beim Einstellen“) |
| „Einstellen fehlgeschlagen, eBay nennt keinen Grund: <Adresse>“ | Nach dem Absenden kam keine Erfolgsseite, und es war kein Fehlertext lesbar | Im eBay-Verkäuferbereich nachsehen, ob das Angebot doch online oder als Entwurf da ist; erneut versuchen |
| eBays eigener Fehlertext | eBay hat das Einstellen abgelehnt (z. B. Pflichtangabe fehlt, Verkaufslimit erreicht) | Text lesen. Zum Ansehen im eBay-Tab den Schalter „Fehler-Tabs schließen“ im Browser-Lister ausschalten. Verkaufslimit: `listen-auf-ebay.md` |
| „eBay-Fehlerseite - Angebot nicht eingestellt“ | eBay hat eine Fehlerseite des Angebotsformulars gezeigt | erneut versuchen |
| „eBay-Serverfehler (upstream connect error) - Angebot nicht eingestellt“ | eBay-Seite mit Verbindungsfehler (Störung bei eBay) | später erneut versuchen |
| „Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“ | Der eBay-Teil hat 15 Minuten lang kein Ergebnis gemeldet. Häufig: eBay-Anmeldung abgelaufen, Sicherheitsabfrage offen, „Listing automatisch absenden“ (Einstellungen → „Preise & Listing“ → „Listing“) aus – dann wartet das Formular auf deinen Klick | eBay-Anmeldung und den Schalter prüfen; siehe `listen-auf-ebay.md` |

### 10.5 Zusätze „Format geprüft …“ und Meldungen zum Angebotsformat

An manche Meldungen hängt ein Zusatz wie „ · Format geprüft: …“ oder „ · Format-Prüfung: keine Rückmeldung“. Außerdem gibt es Meldungen, die mit „Nicht eingestellt:“ beginnen und das Angebotsformat, „Auktion“ oder „Sofort-Kaufen“ nennen (Tab-Titel dazu: „Nicht eingestellt: kein Sofort-Kaufen“).

**Zu dieser Prüfung gibt es keine Beschreibung - bei Fragen an den Betreiber wenden.**

---

## 11. Tab-Titel (beim Listen und auf Amazon-Produktseiten)

### 11.1 Arbeits-Tabs des Browser-Listers

Während des Listens zeigen die Arbeits-Tabs im Titel, was gerade passiert. Die vollständige Liste steht in `listen-auf-ebay.md` (Abschnitt „Tab-Titel und Tab-Symbole während des Listens“). Wichtig für die Fehlersuche:

**Amazon-Tab – Warn-Titel (das Produkt wird übersprungen):**
- „WARNUNG! SEITE EXISTIERT NICHT“, „WARNUNG! SCHON GELISTET (DUPLIKAT) - ZUM LISTEN BESTÄTIGEN - …“, „⚠️ WARNUNG! PRODUKT ENTHÄLT BLACKLIST-WÖRTER (<Wort>) - ZUM LISTEN BESTÄTIGEN - …“, „WARNUNG! ASIN PASST NICHT ZUR ADRESSE - ZUM LISTEN BESTÄTIGEN - …“, „ÜBERSPRUNGEN! Mindestbestellmenge“, „WARNUNG! NICHT AUF LAGER - ZUM LISTEN BESTÄTIGEN - …“, „WARNUNG! INTERNATIONALER VERSAND - ZUM LISTEN BESTÄTIGEN - …“, „WARNUNG! NICHT FBA - ZUM LISTEN BESTÄTIGEN - …“, „WARNUNG! KEIN KOSTENLOSER VERSAND - ZUM LISTEN BESTÄTIGEN - …“, „WARNUNG! GEBRAUCHT - ZUM LISTEN BESTÄTIGEN - …“, „WARNUNG! PREIS ZU HOCH - ZUM LISTEN BESTÄTIGEN - …“, „WARNUNG! PREIS ZU NIEDRIG - ZUM LISTEN BESTÄTIGEN - …“, „WARNUNG! KEIN CHINESISCHER VERKÄUFER - ZUM LISTEN BESTÄTIGEN - …“, „ÜBERSPRUNGEN! keine GPSR-Angaben“, „Auto-Listing - <ASIN>  FEHLER! Nicht angemeldet!“, „Auto-Listing - <ASIN>  FEHLER! Titel ist leer!“, „Auto-Listing - <ASIN>  FEHLER! Titel-Erstellung fehlgeschlagen!“
- Die Bedeutung entspricht den Meldungen in 10.2 und 10.3.
- Der Zusatz „ZUM LISTEN BESTÄTIGEN“ ist nur ein alter Wortlaut. Es gibt keinen Knopf, mit dem man das Produkt trotzdem listen könnte.
- Bei einem Blacklist-Treffer steht am Ende des Titels statt des Produktnamens das gefundene Wort.
- Titel mit „GPSR …“ (z. B. „GPSR 1: Knopf „Sicherheitskontakte“ nicht gefunden“, „GPSR 3: Herstellerangaben nicht gefunden“) zeigen nur den Zwischenstand beim Lesen der Herstellerangaben. Am Ende zählt, ob „GPSR-Angaben erhalten!“ oder „ÜBERSPRUNGEN! keine GPSR-Angaben“ kommt.

**Amazon-Tab – normaler Ablauf:** „Auto-Listing - <ASIN>“, „Prüfe chinesischen Verkäufer...“, „Hole GPSR-Angaben...“, „Auto-Listing - KI-Titel wird erstellt...- <ASIN>  KI-Titel wird erstellt...“, „Auto-Listing - <ASIN>  Erstelle Bild...“, „Wird bei eBay gelistet: <Titel> - <ASIN>  ...“.

**eBay-Tab – Ende:**
- „Angebot eingestellt!“ (grünes Symbol) = eingestellt.
- „Einstellen fehlgeschlagen!“ (rotes Symbol) = nicht eingestellt (auch auf eBays Fehlerseite).
- „Beschreibung fehlgeschlagen“, „Abgebrochen: Fehler beim Ausfuellen“ = abgebrochen.
- „Nicht eingestellt: kein Sofort-Kaufen“ = siehe 10.5.
- „✅ Sperrbegriffe aus den Artikelmerkmalen entfernt“ = die Extension hat die Artikelmerkmale auf Sperrwörter geprüft und betroffene Merkmale geleert. Der Titel erscheint nach jeder Prüfung, auch wenn nichts geleert werden musste. Kein Fehler.
- Titel, die mit „eBay-Produktsuche“ beginnen, gehören zum Anfang des Ablaufs (eBay sucht die passende Produktseite). Kein Fehler.

### 11.2 Amazon-Produktseiten, die du selbst öffnest

Auch wenn du eine Amazon-Produktseite von Hand öffnest, prüft die Extension die Seite beim Laden und schreibt Warnungen vor den Tab-Titel. Das ist **keine Fehlermeldung** und hat keine Folgen: Es wird nichts gelistet und nichts gespeichert. Es ist nur ein Hinweis, wie der Browser-Lister das Produkt einschätzen würde. Mehrere Warnungen können hintereinander stehen.

| Tab-Titel beginnt mit | Bedeutung |
|---|---|
| „WARNUNG! NICHT AUF LAGER - ZUM LISTEN BESTÄTIGEN -“ | Laut Amazon nicht auf Lager oder Lieferzeit zu lang (wie „Produkt ist nicht auf Lager“ in 10.2) |
| „WARNUNG! LIEFERZEIT VERLÄNGERT - ZUM LISTEN BESTÄTIGEN -“ | Lieferzeit länger als „Max. verlängerte Lieferzeit“ (Hinweis in 10.2) |
| „WARNUNG! KEIN KOSTENLOSER VERSAND - ZUM LISTEN BESTÄTIGEN -“ | Kein kostenloser Versand in der Buybox |
| „WARNUNG! GEBRAUCHT - ZUM LISTEN BESTÄTIGEN -“ | Das Angebot in der Buybox ist gebraucht |
| „WARNUNG! MINDESTBESTELLMENGE <Zahl> - ZUM LISTEN BESTÄTIGEN -“ | Mindestbestellmenge über 1 |
| „WARNUNG! KEIN PRIME - ZUM LISTEN BESTÄTIGEN -“ | Die Extension erkennt das Angebot nicht als Prime/von Amazon versendet |
| „WARNUNG! INTERNATIONALER VERSAND - ZUM LISTEN BESTÄTIGEN -“ | Nur internationaler Versand |
| „WARNUNG! ASIN PASST NICHT ZUR ADRESSE - ZUM LISTEN BESTÄTIGEN -“ | Amazon zeigt ein anderes Produkt bzw. eine andere Variante als im Link |
| „⚠️ BLACKLIST-WORT GEFUNDEN: <WORT> -“ | Ein Eintrag aus deiner Blacklist kommt auf der Seite vor (Regeln wie in 10.2) |

Bei einem Blacklist-Treffer ersetzt die Extension den eigentlichen Seitentitel durch das gefundene Wort. Der Tab heißt dann z. B. „⚠️ BLACKLIST-WORT GEFUNDEN: WORT - wort“. Bei den meisten Warnungen wechselt außerdem das Tab-Symbol.

**Gut zu wissen:** „KEIN PRIME“ auf einer von Hand geöffneten Seite ist eine andere Prüfung als die Versand-Prüfung beim Listen. Beim Listen prüft die Extension den Versender in der Buybox (siehe „Nicht von Amazon versendet“ in 10.2). Die beiden Ergebnisse können deshalb voneinander abweichen. Maßgeblich für das Listen ist die Prüfung beim Listen.

---

## 12. Amazon-Suchseiten: Knopf „→ Datenbank“ (Grabber)

Wo: auf Amazon-Suchseiten und Verkäufer-Schaufenstern unten rechts. Der runde Knopf zeigt z. B. „📦 <Zahl> Produkte → Datenbank“. Die Meldungen erscheinen in einem weißen Kasten darüber. Abschließende Meldungen verschwinden nach etwa 8 Sekunden von selbst; Fortschrittsmeldungen („Importiere …“, „Prüfe den Verkäufer …“, die „⛔“-Meldungen, Server-Fehler) bleiben stehen, bis die nächste Meldung kommt. Ausführlich: `produkte-finden-und-datenbank.md`.

Gut zu wissen:
- Der Schalter „nur Verkauf durch Amazon“ auf der Suchseite ist dieselbe Einstellung wie „Nur Verkauf durch Amazon“ in Einstellungen → „Produkt-Filter“ → „Amazon-Filter“.
- Wie viele Prüf-Tabs gleichzeitig aufgehen, richtet sich nach dem Feld „Gleichzeitig“ im Tracker.
- Seit 46.0 liegt die Produkt-Datenbank auf dem Server. Ohne Anmeldung oder ohne Server wird **nichts** importiert, und der Kasten sagt das.

### 12.1 Beschriftung des Knopfs und der Häkchen

| Text | Bedeutung |
|---|---|
| „📦 <Zahl> Produkte → Datenbank“ / „📦 <Zahl> von <Zahl> Produkten → Datenbank“ | So viele Produkte würden importiert (bei abgewählten: „von“) |
| „… · <Zahl> vom Filter ausgeschlossen …“ | So viele Kacheln fallen durch die Filter aus den Einstellungen. Beim Darüberfahren mit der Maus steht, welcher Filter: z. B. „• <Zahl> × Lieferung dauert länger als <Zahl> Tage (Einstellungen → Produkt-Filter → „Max. verlängerte Lieferzeit“)“, „• <Zahl> × Amazon-Preis außerhalb von … (Einstellungen → Produkt-Filter → „Preis ab“ / „Preis bis“)“, „• <Zahl> × weniger als <Zahl> Sterne (Einstellungen → Produkt-Filter → „Mind. Sterne“)“, „• <Zahl> × weniger als <Zahl> auf Lager (Einstellungen → Produkt-Filter → „Mind. Lagerbestand“)“, „• <Zahl> × weniger als <Zahl> Bewertungen (Einstellungen → Produkt-Filter → „Mind. Bewertungen“)“ |
| „… · nur Verkauf durch Amazon (wird geprüft)“ / „… · <Zahl>× Amazon, <Zahl>× andere, <Zahl> noch offen“ | Schalter „nur Verkauf durch Amazon“ ist an; Stand der Verkäuferprüfung |
| „⏳ Verkäufer <Zahl>/<Zahl> · <Zahl>× Amazon · <Zahl> Tabs – Klick = abbrechen“ | Die Verkäuferprüfung läuft. Ein Klick bricht ab |
| Häkchen-Pille im Produktbild: „importieren“, „übersprungen“, „Amazon ✓“, „nicht Amazon“, „kein Angebot“ | Zustand je Produkt. Beim Darüberfahren: „Häkchen weg = nicht übernehmen“, „Verkäufer: <Name> – wird nicht übernommen“ oder „Kein Angebot in der Buybox (nicht lieferbar) – wird nicht übernommen“ |
| „📚 Ganzer Shop → Datenbank“ / „⏳ Seite <Zahl> … (<Zahl> Produkte)“ / „⏳ Importiere <Zahl> …“ | Zweiter Knopf im Verkäufer-Schaufenster und sein Fortschritt |

### 12.2 Meldungen im Kasten

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Importiere <Zahl> Produkte …[ Bei so vielen dauert das etwas.]“ | Läuft | warten |
| „✅ <Zahl> neu in der Datenbank · <Zahl> schon in DB · <Zahl> bereits gelistet · <Zahl> von anderen Kunden belegt · Bestand: <Zahl>“ | Ergebnis. „schon in DB“ = lag schon in deiner Produkt-Datenbank. „bereits gelistet“ = steht in deinen eingetragenen Google-Sheets oder ist für dich schon als gelistet bestätigt. „von anderen Kunden belegt“ = ein anderer Kunde hat es. „Bestand“ = Produkte jetzt in der Datenbank. Am Ende ggf. „(<Zahl> abgewählt)“ oder Angaben zu aussortierten Verkäufern | nichts |
| „✅ Ganzer Shop: <Zahl> Seite(n), <Zahl> Kacheln geprüft[ von <Zahl>] · <Zahl> neu in der Datenbank · <Zahl> schon drin · <Zahl> bereits gelistet · <Zahl> von anderen Kunden belegt.“ | Ergebnis von „📚 Ganzer Shop → Datenbank“ | nichts |
| „❌ Nichts importiert – Server nicht erreichbar. Bitte später erneut versuchen.“ | Der Server antwortet nicht; es wurde nichts gespeichert | Später erneut klicken |
| „❌ Bitte zuerst in Cash Lister anmelden – nichts importiert.“ | Nicht angemeldet (auch bei abgeschaltetem Zugang oder Abo-Sperre) | Im Dashboard anmelden, dann erneut klicken |
| „⚠️ Nur teilweise importiert – <Meldung>“ | Bei sehr vielen Produkten brach der Server mittendrin weg. Die Meldung sagt, wie viele schon drin sind | Einfach noch einmal importieren; Doppelte werden erkannt |
| „❌ Nichts importiert: <Grund>“ | Anderer Fehler; nichts gespeichert | Grund lesen; bleibt es: Betreiber |
| „❌ Fehler: <Grund> – Extension in diesem Browser aktualisieren/neu laden?“ | Der Import kam nicht an. Häufig: „keine Antwort vom Hintergrunddienst“ | Amazon-Seite neu laden; Hintergrunddienst neu laden (Abschnitt 3); erneut klicken. Doppelte Produkte entstehen dabei nicht |
| „❌ Fehler: <Grund>“ | Dasselbe beim „Ganzer Shop“-Import | wie oben |
| „… Hintergrunddienst antwortet nicht, neuer Versuch (<Zahl>/2) …“ | Die Extension versucht es von selbst noch einmal | warten |
| „Alle <Zahl> Produkte sind abgewählt – nichts zu importieren.“ | Alle Häkchen sind weg | Häkchen wieder setzen |
| „Keine Produktkacheln auf dieser Seite gefunden.“ | Auf der Seite sind keine passenden Produkte, oder alle sind durch Filter ausgeschlossen | Filter prüfen; andere Seite |
| „Nichts gefunden – alle Kacheln von den Filtern ausgeschlossen?“ | „Ganzer Shop“ fand nichts Passendes | Filter in den Einstellungen prüfen |
| „Seite <Zahl>: HTTP <Zahl> – Abbruch, bisher Gefundenes wird übernommen.“ | Beim Blättern lieferte Amazon eine Seite nicht | Das Gefundene wird trotzdem importiert. Später für den Rest erneut |
| „Abbruch beim Blättern: <Grund>“ | Unerwarteter Fehler beim Blättern | Seite neu laden, erneut |
| „Prüfe den Verkäufer von <Zahl> Produkten in <Zahl> Tabs gleichzeitig (ca. <Zeit>). Nochmal klicken = abbrechen.“ | Mit „nur Verkauf durch Amazon“: Die Extension öffnet kurz jede Produktseite in einem eigenen Tab | warten |
| „⛔ Amazon zeigt ein Captcha – Prüfung angehalten. Der Tab mit dem Captcha ist vorne: dort lösen, dann hier nochmal klicken. <Zahl> von <Zahl> sind geprüft und bleiben gemerkt; ein weiterer Klick prüft nur den Rest. Importiert wurde noch nichts.“ | Amazon zeigt eine Sicherheitsabfrage | Im vorderen Tab die Abfrage selbst lösen, dann erneut klicken |
| „⛔ Amazon zeigt ein Captcha bzw. eine Sperrseite – Prüfung angehalten. Eine Amazon-Produktseite öffnen, das Captcha lösen und nochmal klicken. …“ | Amazon bremst oder zeigt eine Sperrseite | Eine Amazon-Produktseite öffnen, Abfrage lösen, etwas warten, erneut klicken |
| „⛔ Mehrere Produktseiten nicht abrufbar (<Grund>) – Prüfung angehalten. …“ | Mehrere Produktseiten hintereinander ließen sich nicht prüfen. Gründe z. B. „Preis nicht verfügbar – Amazon bremst vermutlich“, „keine Produktseite erhalten“, „Produktseite in 45 s nicht geladen“, „Produktseite laedt nicht (Chrome-Fehlerseite)“, „Tab liess sich nicht oeffnen (…)“, „Pruef-Tab wurde geschlossen“, „keine Antwort in <Zahl> s“, „Hintergrunddienst antwortet nicht“, „HTTP <Zahl>“ | Etwas warten, Internet prüfen, keine Prüf-Tabs von Hand schließen, erneut klicken. Bei „Hintergrunddienst antwortet nicht“: Hintergrunddienst neu laden |
| „Extension wurde neu geladen – Amazon-Seite neu laden“ (als Grund) | Die Extension wurde neu geladen, während die Seite offen war | Amazon-Seite neu laden (F5) |
| „Prüfung abgebrochen. …“ | Du hast abgebrochen | nichts; ein weiterer Klick prüft den Rest |
| „Alle Produkte wurden während der Prüfung abgewählt – nichts importiert.“ | Während der Prüfung alle Häkchen entfernt | nichts |
| „Das Produkt wird nicht von Amazon verkauft …“ / „Keins der <Zahl> Produkte wird von Amazon verkauft (…) – nichts importiert.“ | Mit „nur Verkauf durch Amazon“: Keines der Produkte wird von Amazon selbst verkauft. In Klammern die häufigsten Händler | nichts, oder Schalter ausschalten |
| „Für <Marktplatz> ist die Händler-ID von Amazon nicht hinterlegt – „nur Verkauf durch Amazon“ geht hier nicht. Den Schalter ausschalten.“ | Auf diesem Amazon-Marktplatz kann die Extension Amazon als Verkäufer nicht erkennen | Schalter „nur Verkauf durch Amazon“ ausschalten |

---

## 13. Produkt-Datenbank

Wo: Seitenleiste → „Produkt-Datenbank“. Seit 46.0 liegt die Liste **je Konto auf dem Server**: Alle Geräte deines Kontos sehen dieselbe Liste. Ausführlich: `produkte-finden-und-datenbank.md`.

### 13.1 Kopfzeile und roter Fehlerkasten

| Text | Bedeutung | Was tun |
|---|---|---|
| „<Zahl> Produkte · <Zahl> frei · <Zahl> in Arbeit“ | Stand. **„In Arbeit“** = gerade von einem Lister entnommen (Browser-Lister oder CSV-Lister, auf irgendeinem Gerät deines Kontos) | nichts |
| „Bestand gerade nicht abrufbar“ | Die Liste kam nicht vom Server; darüber steht der rote Fehlerkasten | siehe unten |
| Fehlerkasten „Bitte zuerst anmelden – das geht im Dashboard.“ mit Knöpfen „Erneut versuchen“ und „Zum Dashboard (Anmelden)“ | Nicht angemeldet, Sitzung abgelaufen, Zugang abgeschaltet oder Abo gesperrt | „Zum Dashboard (Anmelden)“ klicken, dort Anmeldestand prüfen |
| Fehlerkasten „Server nicht erreichbar – die Produkt-Datenbank liegt jetzt auf dem Server. Bitte später erneut versuchen.“ | Keine Verbindung zum Server | Internet prüfen; später „Erneut versuchen“ |
| Fehlerkasten „Fehler: <Meldung>“ | Anderer Fehler, z. B. ein Text, der mit „Der Claims-Server lehnt die Anfrage ab …“ beginnt und mit „… bitte die Extension aktualisieren oder beim Betreiber melden.“ endet, oder „Fehler: keine Antwort“ | Seite neu laden. Beim Text „… lehnt die Anfrage ab …“: prüfen, ob die neueste Version läuft (Versionsnummer links unten), sonst Betreiber. Bei „keine Antwort“: Hintergrunddienst neu laden (Abschnitt 3) |
| „<Zahl> Produkte werden noch auf den Server übertragen …“ | Beim ersten Start von 46.0 wird die bisherige Liste dieses PCs automatisch auf den Server übertragen | warten; die Seite aktualisiert sich von selbst |
| „<Zahl> Produkte dieses Geräts warten darauf, nach der Anmeldung auf den Server übertragen zu werden.“ bzw. „… darauf, sobald der Server erreichbar ist, auf den Server übertragen zu werden.“ | Die alte Liste dieses PCs ist noch nicht übertragen | anmelden bzw. warten. Die Übertragung läuft dann von selbst |

### 13.2 Karte „Links hinzufügen“

| Meldung | Wann / Bedeutung | Was tun |
|---|---|---|
| „Füge <Zahl> Links hinzu …[ Bei vielen Links dauert das etwas.]“ | Nach Klick auf „Zur Datenbank hinzufügen“ | warten |
| „✅ <Zahl> hinzugefügt[, <Zahl> schon drin][, <Zahl> schon gelistet][, <Zahl> belegt (hat schon ein anderer Kunde)][, <Zahl> ohne erkennbare ASIN ignoriert].“ | Ergebnis. „schon drin“ = lag schon in der Datenbank. „schon gelistet“ = steht in deinen Google-Sheets oder ist für dich schon als gelistet bestätigt. „belegt“ = ein anderer Kunde hat es; es kommt nicht in deine Datenbank. „ohne erkennbare ASIN“ = Zeile war kein Amazon-Link und keine ASIN | nichts; ggf. falsche Zeilen korrigieren |
| „Nichts importiert – Server nicht erreichbar. Bitte später erneut versuchen.“ | Server weg; **nichts** gespeichert. Die Links bleiben im Feld stehen | später einfach erneut auf „Zur Datenbank hinzufügen“ |
| „Nichts importiert – bitte zuerst im Dashboard anmelden.“ | Nicht angemeldet (oder Zugang/Abo gesperrt) | anmelden, dann erneut |
| „Nur teilweise importiert – <Meldung>“ | Bei vielen Links (mehr als 200) brach der Server mittendrin weg. Die Meldung beginnt mit dem Grund, z. B. „Claims-Server nicht erreichbar … – bitte später erneut versuchen.“ oder „Produkt-Datenbank auf dem Server noch nicht bereit (HTTP 503) – bitte später erneut versuchen.“, und endet mit „Von <Zahl> Produkten wurden die ersten <Zahl> verarbeitet (<Zahl> neu), der Rest nicht – einfach noch einmal importieren, Doppelte werden erkannt.“ | Später noch einmal importieren |
| „Nichts importiert – Fehler: <Meldung>“ | Anderer Fehler | Meldung lesen (siehe 13.1); bleibt es: Betreiber |

### 13.3 Karte „Bestand“: Löschen, Export, Sortierung

| Meldung | Bedeutung | Was tun |
|---|---|---|
| Spalte „In Arbeit“: „<Gerätename> bis <Uhrzeit>“ (ggf. „(dieses Gerät)“) | Das Produkt ist bis zu dieser Zeit von einem Lister entnommen. Danach ist es wieder frei | nichts |
| Fenster „<ASIN> ist gerade in Arbeit (…). Trotzdem löschen? …“ | Nach Klick auf „✕“ bei einem Produkt in Arbeit. Löschst du es, während es gelistet wird, ist die Reservierung weg | Nur „OK“, wenn das Gerät nicht mehr daran arbeitet (z. B. abgestürzt) |
| „<ASIN> ist gerade in Arbeit gekommen und bleibt stehen – nach dem Neuladen mit Rückfrage löschbar.“ | Zwischen Anzeige und Klick hat ein Lister das Produkt genommen | Seite neu laden, ggf. erneut |
| „<ASIN> war schon nicht mehr in der Datenbank.“ | Ein anderes Gerät hat es inzwischen gelistet oder gelöscht | nichts |
| Fenster „Wirklich ALLE Produkte aus der Datenbank löschen? Das gilt für alle Geräte deines Kontos – die Liste ist danach überall leer.“ | Nach Klick auf „Alle löschen“ | „OK“ löscht alles, was nicht gerade in Arbeit ist |
| „Datenbank geleert.“ | Alles gelöscht | nichts |
| „1 Produkt ist gerade in Arbeit und bleibt stehen (einzeln mit ✕ löschbar).“ / „<Zahl> Produkte sind gerade in Arbeit und bleiben stehen (einzeln mit ✕ löschbar).“ | „Alle löschen“ lässt Produkte in Arbeit stehen | Bei Bedarf einzeln mit „✕“ löschen (mit Rückfrage) |
| „Exportiere …“ / „<Zahl> Links exportiert.“ / „Die Datenbank ist leer – nichts zu exportieren.“ | Rund um „Als TXT exportieren“ | nichts |
| Fenster „Sortieren fehlgeschlagen: <Grund>“ | Die neue Sortierung wurde nicht gespeichert | Seite neu laden, erneut |

### 13.4 Knopf „Sheet-Abgleich prüfen“

| Meldung | Wann / Bedeutung | Was tun |
|---|---|---|
| „Prüfe Sheets …“ | läuft | warten |
| „Keine Sheets hinterlegt. Trage im Tracker das Haupt-Sheet und/oder weitere Shop-Sheets ein.“ | Im Tracker sind keine Google-Sheets eingetragen | Im Tracker, Karte „Google Sheets“, die Links eintragen |
| „✅ <Name>: <Zahl> ASINs gelesen“ | Sheet gelesen | nichts |
| „⚠️ <Name>: 0 ASINs – Sheet leer oder Format nicht erkannt“ | Sheet erreichbar, aber keine ASINs gefunden. Erkannt werden Amazon-Links (z. B. mit „/dp/“) und ASINs, die mit „B0“ beginnen | Inhalt des Sheets prüfen |
| „❌ <Name>: nicht lesbar (Freigabe „Jeder mit dem Link – Betrachter"? Makro ohne doGet?)“ | Sheet nicht lesbar. <Name> ist z. B. „Haupt-Sheet (Lese-Link)“, „Haupt-Sheet (Web-App /exec)“ oder „Shop-Sheet 1“ | Am sichersten den normalen Google-Sheets-Link eintragen (beginnt mit „https://docs.google.com/spreadsheets/d/“) und das Sheet in Google auf „Jeder mit dem Link – Betrachter“ freigeben. Steht beim Namen „Haupt-Sheet (Web-App /exec)“, ist im Tracker das Feld „Haupt-Sheet – Lese-Link“ leer; dann den normalen Sheet-Link dort eintragen. Der Teil „Makro ohne doGet?“ betrifft nur eingetragene Web-App-Adressen (enden auf „/exec“). **Nicht sicher belegt:** wie so ein Script genau aussehen muss; dazu an den Betreiber verweisen |
| „Insgesamt <Zahl> bereits gelistete ASINs für den Abgleich.“ | Summe | nichts |
| „Fehler: <Grund>“ | Prüfung gescheitert | Seite neu laden, erneut |

Wichtig: Ein Sheet, das nicht lesbar ist, wird beim Import einfach übergangen. Es blockiert dann kein Produkt, schützt aber auch nicht vor Doppel-Angeboten.

---

## 14. Konkurrenz-Scanner

Wo: Seitenleiste → „Konkurrenz-Scanner“. Ausführlich: `produkte-finden-und-datenbank.md`. Rot unter dem Startbereich stehen Fehler, darüber ein Protokoll und eine Statuszeile.

### 14.1 Start und Abschluss

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Bitte den Link zur Verkäufer-Produktseite einfügen.“ | Feld „Link zur Verkäufer-Produktseite“ leer | Link der eBay-Seite einfügen, die die Artikel des Verkäufers zeigt |
| „Bitte einen eBay-Link einfügen – die Seite, die die Produkte des Verkäufers zeigt.“ | Der Link ist kein eBay-Link | Richtigen eBay-Link einfügen |
| „Fehler: Keine Produkte gefunden. Zeigt die eingefügte Seite wirklich die Artikel des Verkäufers?“ | Auf der ersten Seite wurden keine Artikel erkannt | Link im Browser öffnen und prüfen |
| „Fehler: <Grund>“ (dazu im Protokoll „FEHLER: <Grund>“) | Anderer Fehler | Erneut versuchen; bleibt es: Screenshot an den Betreiber |
| „Fertig – <Zahl> neue Treffer bei <Zahl> Produkten[ (<Zahl> Angebote zeigten auf ein bereits gefundenes Produkt)].“ | Lauf beendet | Funde in der Tabelle „Gefundene Produkte“ |
| „Gestoppt. …“ | Du hast „Stoppen“ geklickt. Die Funde bis dahin bleiben | nichts |
| „stoppe …“ / „Stopp angefordert – der laufende Schritt wird noch beendet.“ | Nach „Stoppen“ | kurz warten |
| Kopfzeile „<Zahl> neue Treffer in diesem Lauf · <Zahl> schon in der Liste · <Zahl> ohne identisches Bild · <Zahl> unter Mindestverkäufen“ | Zwischenstand | nichts |

### 14.2 Protokollzeilen (Auswahl, die wichtigen)

| Zeile | Bedeutung |
|---|---|
| „Noch keine Artikel sichtbar – warte und lese erneut …“ | eBay hat die Seite noch nicht fertig angezeigt |
| „Verkäufer-Tab war verstellt – zurück auf Seite <Zahl>.“ | Der Verkäufer-Tab war auf einer anderen Seite; die Extension korrigiert das. Den Tab beim Scannen nicht anfassen |
| „… → übersprungen (unter <Zahl>).“ | Zu wenige Verkäufe laut „Mind. Verkäufe“ |
| „eBay-Bild nicht ladbar → übersprungen.“ | Das Bild des eBay-Angebots ließ sich nicht laden |
| „Preis unbekannt (eBay oder Amazon) → übersprungen.“ | Mit Preisfilter: ein Preis fehlt |
| „Keine Aufschlag-Einstellung gefunden – Preisfilter übersprungen.“ | Es ist kein Preisaufschlag eingerichtet (Einstellungen → „Preise & Listing“ → „Preise“); der Preisfilter greift nicht |
| „Unterbietung zu knapp: mein Preis <Betrag> € vs. seine <Betrag> € → übersprungen.“ | Dein Verkaufspreis läge nicht genug unter seinem Preis (Felder „mindestens … %“ und „und mindestens … €“) |
| „<ASIN> ist schon in der Fundliste (anderes Angebot, gleiches Produkt).“ | Doppelt, wird nicht noch einmal gezählt |
| „Produkt bereits an einen anderen Nutzer vergeben → übersprungen.“ | Ein anderer Kunde hat das Produkt |
| „Produkt-Vergabe antwortet nicht – Treffer wird trotzdem übernommen.“ | Keine Antwort zur Reservierung innerhalb von 25 Sekunden |
| „⚠ ohne Reservierung übernommen – die Produkt-Vergabe hat nicht bestätigt.“ | Der Fund ist in deiner Liste, aber nicht für dich reserviert (meist: nicht angemeldet oder Server nicht erreichbar) |
| „✓ Treffer: <ASIN> (<Preis>) – Bildabstand <Zahl>.“ | Gefunden |
| „kein identisches Bild (bester Abstand <Zahl>, nächster: <ASIN>).“ | Kein Amazon-Produkt mit gleichem Bild gefunden |
| „NICHT gespeichert: <Grund>“ | Fund konnte nicht gespeichert werden |
| „Seitengrenze erreicht (<Zahl>).“ | Feld „Max. Seiten“ erreicht |
| „Kein Weiterblättern: kein Weiter-Knopf auf der Seite.“ / „… Weiter-Knopf ausgegraut (letzte Seite).“ / „… Seite nicht lesbar.“ | Ende der Verkäuferseiten oder Seite nicht lesbar |

### 14.3 Bereich „Gefundene Produkte“

| Meldung | Bedeutung | Was tun |
|---|---|---|
| Fenster „Alle gesammelten Funde verwerfen? Die Produkt-Vergabe wird dabei wieder freigegeben.“ | Nach „Alle verwerfen“ | „OK“ löscht die Liste und gibt die Reservierungen frei |
| „verwerfe …“ / „verworfen, Vergabe freigegeben.“ | Fortschritt/Ergebnis | nichts |
| „Nichts zu exportieren.“ | Fundliste leer | nichts |
| Fenster „<Zahl> Produkte exportieren? Sie werden dabei aus dieser Liste entfernt und die Produkt-Vergabe wird freigegeben – die CSV-Datei ist danach die einzige Kopie. Importiere sie auf dem anderen Rechner, damit die Produkte dort wieder für dich reserviert werden.“ | Nach „Exportieren (CSV)“ | Nur „OK“, wenn du die Funde wirklich auf einen anderen Rechner bringen willst. Danach die Datei gut aufheben |
| „<Zahl> Produkte exportiert, aus der Liste entfernt und die Vergabe freigegeben.“ | Export fertig | Datei auf dem anderen Rechner mit „Importieren (CSV)“ einlesen |
| „lese Datei …“ / „prüfe Vergabe … <Zahl> von <Zahl>“ | Import läuft | warten |
| „Datei ist leer.“ | Leere Datei gewählt | richtige Datei |
| „Keine gültigen ASINs in der Datei gefunden.“ | Keine Zeile mit gültiger ASIN | Datei aus „Exportieren (CSV)“ verwenden |
| „<Zahl> von <Zahl> übernommen[, <Zahl> schon an andere vergeben][, <Zahl> waren schon in der Liste].“ | Ergebnis des Imports | nichts |
| „⚠️ <Zahl> Produkte wurden OHNE Reservierung übernommen – die Produkt-Vergabe hat nicht bestätigt. Sie sind für andere Nutzer weiter frei.“ (orange) | Nicht reserviert | Anmeldung prüfen; in den Einstellungen „Verbindung prüfen“ (8.2) |
| „Fundliste nicht lesbar: <Grund>“ / „Fehler: <Grund>“ | Unerwarteter Fehler | Seite neu laden; bleibt es: Betreiber |

---

## 15. Tracker

Wo: Seitenleiste → „Tracker“ (früher „CSV Tracker“). Der Tracker gleicht Preise und Bestand deiner eBay-Angebote mit Amazon ab und lädt die Änderungen zu eBay hoch. Ausführlich: `tracker.md`.

Viele Meldungen kommen als kleine farbige Einblendungen unten rechts, jeweils mit der Uhrzeit davor. Rote Einblendungen (Problem) bleiben etwa 30 Sekunden stehen, blaue (Information) etwa 12 Sekunden. Es sind höchstens 6 gleichzeitig zu sehen; bei mehr verschwinden die ältesten zuerst. Wer eine Meldung verpasst hat: Sie steht auch in der Konsole der Seite (F12), das ist aber nur für die Fehlersuche mit dem Betreiber nötig.

### 15.1 Beim Öffnen und beim Start

| Meldung | Bedeutung | Was tun |
|---|---|---|
| Fenster „Für den Tracker brauchst du die Ultimate-Mitgliedschaft.“, danach ist die Seite leer | Trotz des Wortlauts: **Du bist nicht angemeldet, dein Zugang ist abgeschaltet oder dein Abo gesperrt.** Es gibt keine Stufen zum „Upgraden“ in der Extension | Im Dashboard Anmeldestand prüfen und anmelden, dann den Tracker-Tab neu laden |
| „Bericht wird eingelesen … (<Zahl>)“ | Der Angebotsbericht wird eingelesen; die Zahl zählt die gelesenen Zeilen | warten |
| „Bericht: <Zahl> Zeilen geladen“ / „Bericht: keine geladen“ | Stand oben in der Laufkarte | Bei „keine geladen“: erst „Angebote von eBay laden“ |
| „Keine Zeilen zum Verarbeiten – lade zuerst einen Angebotsbericht.“ | „Lauf starten“ geklickt, aber es ist kein Angebotsbericht geladen | Erst „Angebote von eBay laden“ klicken oder eine CSV-Datei wählen |
| Tab-Titel „⛔ Tracker angehalten – <Zahl> % ohne Ergebnis“ oder „⛔ Tracker angehalten – 200 Artikel in Folge nicht kaufbar“ | Die Notbremse hat ausgelöst | siehe 15.5 |

### 15.2 „Angebote von eBay laden“ (Angebotsbericht holen)

Die Extension öffnet dabei die eBay-Berichtsseite im Seller Hub (auf www.ebay.de: „www.ebay.de/sh/reports/downloads“) in einem Tab im Hintergrund (er kommt nicht nach vorne) und schließt ihn danach wieder. Sein Tab-Titel zeigt „Bericht wird erstellt…“ und am Ende „Bericht fertig“. Das kann einige Minuten dauern; die Extension wartet bis etwa 10 Minuten auf den Bericht. Welcher eBay-Marktplatz benutzt wird, bestimmt die Auswahl „Domain“ in den Einstellungen (Reiter „Preise & Listing“), nicht das Feld „eBay-Seite“ im Tracker.

| Meldung (Einblendung) | Bedeutung | Was tun |
|---|---|---|
| „Fehler beim CSV-Download: Keine eBay-Domain eingestellt (Einstellungen → Preise & Listing → „Domain“).“ | „Domain“ steht auf „Keine“ | In den Einstellungen deinen Marktplatz wählen |
| „Fehler beim CSV-Download: eBay hat auf eine andere Seite umgeleitet (<Adresse>) - vermutlich bist du dort nicht angemeldet.“ | eBay-Anmeldung fehlt oder ist abgelaufen | Im selben Chrome-Profil bei eBay anmelden, erneut klicken |
| „Fehler beim CSV-Download: eBay lieferte eine HTML-Seite statt des Berichts (Anmeldung abgelaufen?)“ | Dasselbe | bei eBay neu anmelden |
| „Fehler beim CSV-Download: Der Bericht von eBay kam leer zurueck“ / „… Der Bericht kam ohne Inhalt zurueck (kein CSV in der Antwort der eBay-Seite).“ | eBay hat einen leeren Bericht geliefert | Später erneut; prüfen, ob du aktive Angebote hast |
| „Fehler beim CSV-Download: Abruf des Berichts fehlgeschlagen, Status <Zahl>“ | eBay hat den fertigen Bericht nicht herausgegeben | Später erneut; eBay-Anmeldung prüfen |
| „Fehler beim CSV-Download: Die eBay-Berichtsseite meldet sich nicht (<Grund>).“ | Die Berichtsseite hat nicht geantwortet | eBay-Anmeldung prüfen, später erneut |
| „Fehler beim CSV-Download: Zeitüberschreitung beim Warten auf: <Schritt>“ | Auf der eBay-Berichtsseite fand die Extension einen Knopf oder ein Feld nicht rechtzeitig. <Schritt> ist z. B. „Knopf „Herunterladen“ im Banner“, „Auswahl „Quelle““, „Option „Alle Angebote““, „Knopf „Bericht erstellen““ oder „neue Berichtszeile“ | Später erneut. Passiert es immer: Betreiber informieren (eBay hat die Seite vielleicht umgebaut) |
| „Fehler beim CSV-Download: Keine Antwort von der eBay-Seite innerhalb von <Zahl> s“ / „… Die eBay-Seite hat leer geantwortet“ | Die eBay-Seite hat nicht oder falsch geantwortet | Später erneut; eBay-Anmeldung prüfen |
| „Fehler beim CSV-Download: <Grund> (keine Antwort vom Hintergrund)“ / „… Der Hintergrund hat geantwortet, aber ohne Ergebnis: …“ | Der Hintergrunddienst hat zwischendurch neu gestartet | Erneut klicken; ggf. Hintergrunddienst neu laden |

Nach erfolgreichem Laden folgen automatisch der Sheet-Abgleich (15.8) und der Produktvergabe-Abgleich (15.9). Deren Einblendungen kommen deshalb direkt danach. Dasselbe passiert, wenn du die Angebotsdatei von Hand auswählst (Feld neben „oder“).

### 15.3 Spalte „Status“ in „Verarbeitete Artikel“

**Wichtig zum Lesen:** Außer „Success“ und „Skipped“ beginnen die Statustexte meist mit „Error: “, zum Beispiel „Error: Artikel bei Amazon nicht verfügbar“ oder „Error: ERROR_503: IP bei Amazon gesperrt“. Das „Error: “ allein sagt noch nicht, wie schlimm es ist. Entscheidend ist der Text danach.

| Status (Text nach „Error: “) | Bedeutung | Was beim Hochladen passiert |
|---|---|---|
| „Success“ | Preis und Verfügbarkeit von Amazon gelesen | Preis/Menge werden nach deinen Einstellungen aktualisiert |
| „Skipped“ | Das Angebot gehört nicht zum gewählten Lieferanten. Meist: die **SKU** (das „Custom label“, deine eigene Artikelnummer bei eBay) wurde nicht von dieser Extension vergeben, z. B. bei von Hand eingestellten Angeboten. Steht bei „Lieferant“ „Keiner“, wird **jede** Zeile „Skipped“ | Nichts, das Angebot bleibt unverändert |
| „ERROR_503: IP bei Amazon gesperrt“ | Amazon bremst, zeigt eine Sicherheitsabfrage oder eine Fehlerseite | **Vorübergehend:** nichts wird geändert, der nächste Lauf prüft neu. Zählt für die automatische Pause (15.4) |
| „ERROR_503: Zeitüberschreitung beim Abruf der Produktdaten (Lieferant amazon, ASIN <ASIN>)“ | Die Produktseite hat nicht rechtzeitig geantwortet | Vorübergehend, nichts wird geändert. Zählt für die automatische Pause |
| „ERROR_503: Tab failed to load: <Grund>“ (z. B. „net::ERR_…“) | Netzwerkfehler beim Laden der Seite | Vorübergehend, nichts wird geändert. Zählt für die automatische Pause |
| „Zeitüberschreitung (timeout): keine Antwort von der Seite im Tab.“ / „Zeitüberschreitung (timeout): Seite im Tab nicht fertig geladen“ / „Zeitüberschreitung (timeout): Seite wurde nicht stabil“ | Der Prüf-Tab hat nicht rechtzeitig Daten geliefert (Seite zu langsam oder hängt) | Vorübergehend, nichts wird geändert. Zählt **nicht** für die automatische Pause |
| „Netzwerkfehler beim Abruf der Amazon-Daten“ | Netzwerkfehler | Vorübergehend, nichts wird geändert |
| „Unknown error“ oder Texte wie „Could not establish connection …“, „… message port closed …“ | Verbindung zum Hintergrunddienst abgerissen | Vorübergehend, nichts wird geändert |
| „Artikel bei Amazon nicht verfügbar“ | Laut Amazon-Seite nicht verfügbar. Auch eine zu lange Lieferzeit (über „Max. verlängerte Lieferzeit“, siehe Hinweis in 10.2) landet meist hier | **Endgültig:** je nach Einstellung „Ausverkaufte / fehlgeschlagene Artikel“ wird die Menge auf 0 gesetzt („Menge auf 0 setzen“) oder das Angebot beendet („Angebot beenden“) |
| „Lieferzeit bei Amazon verlängert“ | Lieferzeit länger als „Max. verlängerte Lieferzeit“. Selten, weil die Lieferzeit meist schon bei „nicht verfügbar“ erkannt wird | Endgültig, wie oben |
| „Artikel bei Amazon nicht Prime-fähig“ | Die Extension erkennt das Angebot nicht als Prime-berechtigt | Endgültig, wie oben |
| „Artikel bei Amazon ohne kostenlosen Versand“ | Kein kostenloser Versand | Endgültig, wie oben |
| „ASIN passt nicht: erwartet <ASIN>, erhalten <ASIN>“ | Amazon hat auf ein anderes Produkt oder eine andere Variante umgeleitet | Endgültig, wie oben. Bei vielen solchen Zeilen das Produkt selbst ansehen |

**Gut zu wissen:**
- Im Fenster „Upload-Einstellungen“ zählt „Fehlgeschlagen / ausverkauft insgesamt: <Zahl>“ alle Zeilen mit „Error“ im Status (vorübergehende und endgültige) sowie Zeilen mit Menge 0. Die Zahl sagt also nicht, wie viele Angebote beendet werden.
- Der Tracker prüft auf dem Amazon-Marktplatz, der bei „eBay-Seite“ gewählt ist. Steht dort „Keine“, prüft er amazon.com (und lädt auch zu ebay.com hoch). Passt der Marktplatz nicht zu deinen Produkten, kommen massenhaft falsche Ergebnisse.
- Setzt du einen Lauf fort (nach „Pausieren“ oder nach der Sperr-Pause) oder ist der Bericht schon ganz durchgeprüft, prüft „Lauf starten“ die Zeilen mit „ERROR_503“ zuerst noch einmal. Ein ganz neuer Lauf prüft ohnehin alle Zeilen neu.
- Welche Fälle als vorübergehend gelten, erkennt das Programm an Wörtern im Statustext. **Nicht sicher belegt:** ob jede denkbare Fehlermeldung richtig eingeordnet wird. Bei ungewöhnlichen Statustexten vor dem nächsten Hochladen im Fenster „Upload-Einstellungen“ in die „Vorschau (erste 3 Artikel)“ schauen oder den Betreiber fragen.

### 15.4 „⏳ Kurz warten!“ – automatische Pause bei Amazon-Sperre

Fenster: „⏳ Kurz warten!“ – „Amazon hat deine IP wegen zu vieler Anfragen vorübergehend gesperrt.“ – „Der Tracker wartet kurz und versucht es dann von selbst weiter.“ – „noch <Zahl> Sekunden …“

- **Wann:** Mehr als 10 Produkte **hintereinander** kamen mit einem „ERROR_503 …“-Status zurück.
- **Bedeutung:** Amazon bremst. Der Tracker pausiert 120 Sekunden (Countdown im Fenster) und macht danach von selbst weiter.
- **Was tun:** Warten. Mit dem „×“ oben rechts schließt du das Fenster. Der Lauf bleibt dann pausiert und geht erst mit „Lauf starten“ weiter. Passiert es oft: Zahl bei „Gleichzeitig“ verkleinern.

### 15.5 „⛔ Notbremse“

Einblendung: „⛔ Notbremse: <Zahl> von <Zahl> Artikeln ohne verwertbares Ergebnis (<Zahl> %). Lauf angehalten, nichts hochgeladen.“ oder „⛔ Notbremse: 200 Artikel hintereinander als nicht kaufbar gewertet. Lauf angehalten, nichts hochgeladen.“ Dazu der Tab-Titel „⛔ Tracker angehalten – <Zahl> % ohne Ergebnis“ bzw. „⛔ Tracker angehalten – 200 Artikel in Folge nicht kaufbar“.

- **Wann:** Entweder galten 200 Artikel hintereinander als nicht kaufbar (ein „Success“ setzt die Zählung zurück; „Skipped“ und vorübergehende Fehler wie „ERROR_503“ zählen nicht mit), oder ab 200 geprüften Artikeln hatten mehr als 70 % kein „Success“ („Skipped“ zählt nicht mit).
- **Bedeutung:** Schutz deines Shops. Liefert Amazon keine Seiten mehr (leise Sperre, umgebaute Seiten, Netzproblem), sähe das aus wie „nicht verfügbar“, und der Tracker würde massenhaft Angebote auf 0 setzen oder beenden. Darum hält er an und lädt **nichts** hoch. „Dauerhaft wiederholen“ plant keinen neuen Lauf.
- **Was tun:**
  1. Ein paar Amazon-Produktseiten selbst öffnen: Kommt eine Sicherheitsabfrage oder Sperrseite? Dann lösen und eine Weile warten.
  2. Internetverbindung prüfen.
  3. In der Tabelle nachsehen, welche Statustexte gehäuft vorkommen.
  4. Erst dann wieder „Lauf starten“ klicken.
  5. Sieht alles normal aus und die Bremse löst trotzdem aus: Betreiber informieren.
- Wer weniger als 200 geprüfte Angebote hat („Skipped“ zählt nicht mit), bei dem greift die Notbremse nie.
- Der Tab-Titel „⛔ Tracker angehalten …“ bleibt stehen, bis du die Seite neu lädst.

### 15.6 Hochladen zu eBay

Seit 46.0 lädt der Tracker nach **jedem** fertigen Lauf automatisch hoch (einen Schalter dafür gibt es nicht mehr). Er öffnet dafür selbst die eBay-Upload-Seite im Seller Hub (auf www.ebay.de: „www.ebay.de/sh/reports/uploads“, bei anderen Marktplätzen entsprechend) in einem eigenen Tab, der nach vorne kommt, und lädt die Datei dort hoch. Welcher eBay-Marktplatz benutzt wird, bestimmt hier das Feld „eBay-Seite“ im Tracker. Hat es geklappt, schließt sich der Tab wieder. Bei einem echten Fehler bleibt er offen, damit du eBays Meldung lesen kannst.

Tab-Titel dieses Upload-Tabs: zuerst Zwischenstände wie „⏳ Hochladen startet“, „🔍 Suche Knopf „Vorlage hochladen““, „📂 Öffne Dialog…“, „📤 Lade Datei hoch…“, „🔍 Warte auf neue Zeile“, „🔄 Warte auf Ergebnisse“, am Ende „✅ Hochladen fertig!“ oder „❌ Hochladen fehlgeschlagen“.

| Meldung (Einblendung) | Bedeutung | Was tun |
|---|---|---|
| „Keine Preis-/Bestandsänderungen – Upload übersprungen.“ | Seit der letzten Übertragung (bzw. seit dem Laden des Angebotsberichts) hat sich nichts geändert | nichts |
| „✅ <Zahl> geänderte Zeilen zu eBay hochgeladen.“ | Hochgeladen | Ergebnis ggf. bei eBay auf der Upload-Seite ansehen |
| „Upload zu eBay fehlgeschlagen: <Grund>“ | Hochladen hat nicht geklappt. Gründe z. B. eBay-Anmeldung abgelaufen oder ein Knopf auf der Upload-Seite nicht gefunden („Zeitüberschreitung beim Warten auf: …“) | Den offenen eBay-Tab ansehen, bei eBay anmelden, erneut versuchen |
| „Upload zu eBay fehlgeschlagen: unbekannt“ | Die Extension hat keine Bestätigung bekommen. Meist läuft der Upload in diesem Fall trotzdem durch | Auf der eBay-Upload-Seite nachsehen, ob die Datei angekommen ist, bevor du erneut hochlädst. **Nicht sicher belegt:** wie die Menüpunkte bei eBay genau heißen, über die man zu dieser Seite kommt; die Adresse oben führt direkt hin |

### 15.7 Dauerbetrieb („Dauerhaft wiederholen“)

| Einblendung | Bedeutung |
|---|---|
| „Dauerbetrieb aktiv – nächster Lauf um <Uhrzeit> Uhr.“ | Nach einem Lauf: wann der nächste startet (Abstand: Feld „Pause … Minuten“) |
| „Dauerbetrieb: hole aktuellen Angebotsbericht …“ | Vor jedem Lauf holt der Tracker den Bericht neu |
| „Dauerbetrieb: neuer Lauf startet (<Zahl> Zeilen).“ | Lauf beginnt |
| „Dauerbetrieb: Bericht nicht abrufbar – Lauf mit dem letzten Stand.“ (rot) | Der neue Bericht kam nicht; der Tracker arbeitet mit dem letzten geladenen Stand. Meist eBay-Anmeldung abgelaufen. Prüfen, sonst fehlen neue Verkäufe in der Rechnung |

### 15.8 Google Sheets

Diese Einblendungen kommen jedes Mal, wenn ein Angebotsbericht geladen wurde (über „Angebote von eBay laden“, von Hand oder im Dauerbetrieb). Sie hängen davon ab, was in der Karte „Google Sheets“ eingetragen ist. Die Extension schickt dabei für jedes Angebot mit lesbarer SKU die eBay-Artikelnummer und den Amazon-Link an das Haupt-Sheet.

| Einblendung | Bedeutung | Was tun |
|---|---|---|
| „Sheet-Sync übersprungen: kein Haupt-Sheet (Web-App-URL) hinterlegt.“ | Feld „Haupt-Sheet dieses Shops – Web-App-URL“ leer | Wenn du kein Sheet nutzt: ignorieren. Sonst eintragen |
| „Sheet-Sync: die Haupt-Sheet-URL sieht ungültig aus (muss mit http/https beginnen).“ | Eintrag ist keine Adresse | Vollständige Adresse eintragen |
| „Sheet-Sync: 0 gültige Zeilen aus <Zahl> Listings (<Zahl> mit nicht-dekodierbarer SKU). Nichts gesendet, damit das Sheet nicht geleert wird.“ | Keines deiner Angebote hatte eine von der Extension vergebene SKU | Absichtlicher Schutz. Bei Zweifeln: Betreiber |
| „✅ Sheet aktualisiert: <Zahl> Zeilen gesendet. Script meldet: <Text>“ | Erfolg | nichts |
| „Sheet NICHT aktualisiert: Google verlangt eine Anmeldung bzw. Autorisierung. Die Web-App ist nicht für alle freigegeben – in Apps Script unter „Bereitstellen → Bereitstellungen verwalten" das Stiftsymbol anklicken und BEIDES setzen: „Ausführen als: Ich" und „Zugriff: Jeder" (nicht „Jeder mit Google-Konto"). Danach speichern; die /exec-URL bleibt dabei gleich.“ | Die Google-Web-App ist nicht freigegeben | Genau wie in der Meldung beschrieben in Google Apps Script einstellen |
| „Sheet NICHT aktualisiert: Google hat eine Webseite zurückgegeben statt einer Script-Antwort. …“ | Die Bereitstellung ist veraltet oder nicht freigegeben | Wie in der Meldung: in Apps Script neu bereitstellen und die neue Adresse eintragen |
| „Sheet-Update abgeschickt: das Script lief, antwortet aber mit einer HTML-Seite …“ / „Sheet-Update abgeschickt, aber das Script hat nichts zurückgemeldet …“ | Ob die Daten angekommen sind, lässt sich nicht sagen | Im Sheet nachsehen |
| „Sheet NICHT aktualisiert: HTTP <Zahl>. Antwort: …“ / „Sheet NICHT aktualisiert – das Script meldet: …“ / „… meldet einen Fehler: …“ / „Sheet-Update fehlgeschlagen: …“ | Fehler beim Senden oder im Script | Text lesen; Script-Einrichtung prüfen. **Nicht sicher belegt:** wie das Google-Script aufgebaut sein muss; dazu an den Betreiber verweisen |

### 15.9 Produktvergabe-Abgleich (nach dem Laden des Angebotsberichts)

Beim Abgleich meldet die Extension, welche Produkte du auf eBay hast. So werden deine Reservierungen bestätigt und beendete Angebote freigegeben. Er läuft jedes Mal, wenn ein Angebotsbericht geladen wurde. Bist du nicht angemeldet, findet er ohne Meldung nicht statt.

| Einblendung | Bedeutung | Was tun |
|---|---|---|
| „✅ Produkt-Vergabe abgeglichen: <Zahl> Artikel · <Zahl> bestätigt · <Zahl> neu · <Zahl> freigegeben“ | Erfolg | nichts |
| „… (Sicherung aktiv – nichts freigegeben)“ als Zusatz | Zur Sicherheit wurde nichts freigegeben, weil deutlich weniger Angebote gemeldet wurden als vorher bestätigt waren. Das schützt davor, dass ein unvollständiger Bericht deine Produkte freigibt | Prüfen, ob der richtige und vollständige Angebotsbericht geladen war |
| „Hinweis zur Produkt-Vergabe: <Zahl> von <Zahl> Angeboten haben keine lesbare ASIN in der SKU und waren im Abgleich NICHT dabei. Deren Reservierungen bleiben unbestätigt und laufen ab.“ | Einige Angebote haben eine SKU, die nicht von dieser Extension stammt | Normal bei von Hand eingestellten Angeboten. Sonst: Betreiber |
| „Produkt-Vergabe: KEIN Abgleich – <Zahl> Angebote geladen, 0 mit gültiger ASIN … Es wurde nichts bestätigt!“ | Kein einziges Angebot hatte eine lesbare SKU | Prüfen, ob der richtige Shop/Bericht geladen ist; sonst Betreiber |
| „⚠️ <Zahl> Produkt(e) bereits von einem anderen Nutzer belegt. Beenden-Datei mit <Zahl> Angebot(en) heruntergeladen – bei eBay hochladen.“ | Nur wenn „Beenden-CSV für Duplikate erstellen“ (Einstellungen → „eBay & Rahmenbedingungen“ → „Server & Produkt-Vergabe“) an ist: Ein anderer Kunde hatte diese Produkte zuerst. Die Datei zum Beenden liegt im Download-Ordner | Die Datei bei eBay hochladen. Erst dann werden die Angebote beendet. Die Extension lädt sie **nicht** selbst hoch |
| „⚠️ <Zahl> doppelte Produkt(e) gefunden, aber keine ItemID dazu gefunden.“ | Doppelte Produkte, aber die eBay-Artikelnummer war nicht zuzuordnen | Betreiber informieren |
| „Produkt-Vergabe: API-Key ungültig.“ | Trotz des Wortlauts: deine **Anmeldung** ist ungültig oder abgelaufen | Im Dashboard abmelden und neu anmelden |
| „Produkt-Vergabe: Abgleich fehlgeschlagen (HTTP <Zahl>).“ | Unerwartete Antwort. Bei „HTTP 403“ ist meist der Zugang abgeschaltet oder das Abo gesperrt | Dashboard ansehen; sonst später erneut; bleibt es: Betreiber |
| „Produkt-Vergabe: Server nicht erreichbar.“ | Keine Verbindung | Internet prüfen, später erneut |

### 15.10 Fenster „Upload-Einstellungen“

Wo: Knopf „Upload-Einstellungen“ oben rechts im Tracker. Unten: „Einstellungen speichern“.

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Noch keine verarbeiteten Artikel.“ (in der Vorschau) | Die Tabelle „Verarbeitete Artikel“ ist leer | Erst einen Lauf machen |
| „Bitte füge die Preisregeln als JSON ein.“ / „Ungültiges JSON. Erwartet wird eine Liste von Regeln.“ / „Preisregeln übernommen.“ | Gehören zu einem Preisbereich in diesem Fenster, der **ausgeblendet** ist. Diese Meldungen solltest du nicht sehen. Die Preise im Tracker kommen aus den Einstellungen (Reiter „Preise & Listing“) | Preise in den Einstellungen setzen. Taucht eine dieser Meldungen doch auf: Screenshot an den Betreiber |

---

## 16. Verkaufs-Übersicht

Wo: Seitenleiste → „Verkaufs-Übersicht“. Fehler stehen rot oben, der Einlese-Stand darunter. Ausführlich: `produktuebersicht-und-csv-lister.md`.

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Wird eingelesen …“ / „Gespeicherter Stand wird geladen …“ | Läuft | warten |
| „Angebote: <Zahl> aktiv[ · <Zahl> Bestellungen zu nicht aktiven Angeboten aussortiert]“ | Angebotsbericht eingelesen | nichts |
| „Bestellungen: <Zahl> gelesen, davon <Zahl> zu aktiven Angeboten · neueste vom <Datum>“ | Bestellbericht eingelesen | nichts |
| „Nichts eingelesen.“ | Es wurde nichts gespeichert (Fehler oder abgebrochen) | Meldung darüber lesen |
| „Fehler: <Datei>: weder Angebots- noch Bestellbericht erkannt.“ | Die Datei ist keiner der beiden eBay-Berichte | Richtige Berichte bei eBay herunterladen (aktive Angebote bzw. Bestellungen) |
| „Fehler: <Datei>: Angebotsbericht: Kopfzeile nicht gefunden (erwarte 'Item number', 'Custom label', 'Available quantity', 'Sold quantity', 'Start date').“ | Im Angebotsbericht fehlen erwartete Spalten | Den Bericht unverändert lassen (nicht in Excel speichern); ggf. neu herunterladen |
| „Fehler: <Datei>: Angebotsbericht: keine Datenzeilen gefunden.“ | Bericht ohne Angebote | anderen Bericht nehmen |
| „Fehler: <Datei>: Bestellbericht: Kopfzeile nicht gefunden (erwarte 'Artikelnummer', 'Bestandseinheit', 'Verkauft am').“ | Im Bestellbericht fehlen erwartete Spalten | Bericht unverändert neu herunterladen |
| „Fehler: <Datei>: Bestellbericht: keine Bestellzeilen gefunden.“ | Bericht ohne Bestellungen | anderen Zeitraum wählen |
| „Fehler: Bitte nur einen Angebotsbericht auf einmal – sonst ist unklar, welcher der aktuelle ist.“ | Zwei Angebotsberichte gleichzeitig gewählt | Nur den neuesten wählen |
| Fenster „Keines der <Zahl> gespeicherten Angebote steht in diesem Angebotsbericht – das ist ein anderer Shop. Die Übersicht speichert immer nur einen Shop. Beim Einlesen fällt der gespeicherte Verkaufsverlauf des bisherigen Shops weg. Trotzdem einlesen?“ | Der neue Bericht passt zu keinem gespeicherten Angebot | „Abbrechen“, wenn es ein Versehen war. „OK“ ersetzt den alten Shop |
| „Achtung: Keine Bestellung aus <Datei> gehört zu den gespeicherten Angeboten. Ist der Bestellbericht von einem anderen Shop? Dann den passenden Angebotsbericht dazu einlesen.“ | Bestellbericht passt nicht zu den Angeboten | passenden Bericht einlesen |
| „Es wird gerade noch eingelesen – bitte <Datei> danach noch einmal wählen.“ | Während des Einlesens eine weitere Datei gewählt | Abwarten, dann erneut wählen |
| „Die Verkaufsdaten reichen nur bis <Datum>, der Angebotsbericht ist vom <Datum>. Verkäufe dazwischen fehlen – bitte den aktuellen Bestellbericht einlesen. Bis dahin wird nichts zum Beenden vorgeschlagen.“ | Der Bestellbericht ist deutlich älter als der Angebotsbericht | Aktuellen Bestellbericht einlesen |
| „<Zahl> von <Zahl> Angeboten ab <Zahl> Tagen ohne Verkauf (gezählt bis <Datum>, Stand der Verkaufsdaten)“ | Zählzeile über der Tabelle | nichts |
| „Noch keine verlässliche Anlaufzeit.“ | Reiter „Wann zum ersten Mal verkauft“: noch zu wenige sichere Daten | nichts |
| Fenster „Nichts markiert.“ | „Beenden-CSV für markierte erstellen“ ohne markierte Angebote | Erst Angebote anhaken |
| „Beenden-Datei mit <Zahl> Angebot(en) heruntergeladen – bei eBay hochladen, erst dann werden sie beendet.“ | Datei liegt im Download-Ordner | Bei eBay hochladen |
| „Es wird gerade eingelesen – bitte danach löschen.“ | „Gespeicherten Verlauf löschen“ während des Einlesens | abwarten |
| Fenster „Den kompletten gespeicherten Verlauf löschen? Angebote und Bestellungen werden entfernt.“ | Sicherheitsfrage | „OK“ löscht alles |
| „Verlauf gelöscht.“ | Fertig | nichts |
| „Datenbank: <Grund>“ | Der gespeicherte Verlauf in diesem Browser ließ sich nicht lesen | Seite neu laden; bleibt es: Betreiber |

---

## 17. CSV-Lister

Seit 46.0 sehen alle Kunden den CSV-Lister (Seitenleiste → „CSV-Lister“, im Titel „neu · im Test“). Ausführlich: `produktuebersicht-und-csv-lister.md`.

**Nicht sicher belegt:** Der CSV-Lister hat sehr viele Meldungen. Hier stehen die wichtigsten. Bei allem, was hier fehlt: an den Betreiber verweisen.

### 17.1 Statuszeile und Prüfpunkte

Oben steht eine Statuszeile mit Punkt; „Details“ klappt die Prüfpunkte auf.

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Bereit zum Listen“ | Alle Voraussetzungen erfüllt | starten |
| „Fehlt noch: Anmeldung, Rahmenbedingungen, Artikelstandort“ (je nach Fall) | Voraussetzungen fehlen; die Prüfpunkte klappen dann von selbst auf | Fehlende Punkte erledigen |
| „Erst die offenen Punkte oben beheben.“ / „Rote Punkte oben zuerst beheben.“ | Start nicht möglich | Rote Punkte beheben |
| Prüfpunkt „eBay-Abfragen (laufen über den Server)“: „nicht angemeldet – ohne Anmeldung keine eBay-Abfragen (Dashboard → Anmelden)“ | Nicht angemeldet | anmelden |
| Prüfpunkt „Anmeldung (Produkt-Vergabe, Server)“: „nicht angemeldet – Produkt-Vergabe und Lister-Log sind aus“ | Nicht angemeldet | anmelden |
| Prüfpunkt „Rahmenbedingungen …“: „fehlt: Versand, Zahlung, Rücknahme – ohne die drei Namen startet kein Lauf“ | In den Einstellungen (Reiter „eBay & Rahmenbedingungen“, Karte „Rahmenbedingungen“) fehlen die Namen deiner eBay-Rahmenbedingungen | eintragen, Buchstabe für Buchstabe wie im Seller Hub |
| Prüfpunkt „Artikelstandort“: „fehlt – Ort oder Postleitzahl für die Spalte *Location“ | Artikelstandort fehlt | in derselben Karte eintragen |
| Prüfpunkt „Muster-CSV“ rot mit „… nicht lesbar: <Grund>“ | Die mitgelieferte Musterdatei ist nicht lesbar | Extension neu laden; bleibt es: Betreiber |
| Prüfpunkt „Produkt-Filter (Einstellungen)“: „… – Produkte ohne passenden Verkäufer bzw. ohne GPSR-Angaben werden aussortiert und gelöscht (ändern: Einstellungen)“ | „Nur chinesische Verkäufer“ oder „GPSR-Angaben übernehmen“ ist an | Bewusst entscheiden; aussortierte Produkte verlassen die Datenbank |
| Prüfpunkt „Alter Browser-Lister“: „läuft gerade – geht gleichzeitig, jeder Lister bekommt andere Produkte“ | Browser-Lister läuft gleichzeitig. Seit 46.0 geht das | nichts |

### 17.2 Tageskontingent

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Heute noch <Zahl> von <Zahl>“ | So viele Produkte darfst du heute noch über den CSV-Lister listen | nichts |
| „Tageskontingent erreicht – ab Mitternacht wieder frei“ / „Nicht gestartet: Tageskontingent erreicht – ab Mitternacht wieder frei.“ | Kontingent für heute aufgebraucht | Morgen weiter |
| „Heute noch 0 von <Zahl> – der Rest ist für den laufenden Lauf gebucht“ | Ein laufender Lauf hat den Rest belegt | Lauf abwarten |
| „Rückgabe von <Zahl> Produkten ausstehend – wird nachgeholt“ / „Nicht gestartet: Tageskontingent erreicht – Rückgabe von … ausstehend – wird nachgeholt. Bitte in ein paar Minuten erneut starten.“ | Nicht verbrauchte Plätze werden gerade zurückgebucht | Ein paar Minuten warten |
| „Prüfe das Tageskontingent …“ | Läuft | warten |
| „Nicht gestartet: Nicht angemeldet – das Tageskontingent kommt vom Server (Dashboard → Anmelden).“ | Nicht angemeldet | anmelden |
| „Nicht gestartet: Tageskontingent nicht abrufbar: <Grund>“ | Der Server hat das Kontingent nicht geliefert | später erneut; bleibt es: Betreiber |
| „Tageskontingent dieses Laufs aufgebraucht (<Zahl> gebucht) – Lauf angehalten.“ / „Das Tageskontingent dieses Laufs wurde von einer anderen Lister-Seite zurückgegeben – Lauf angehalten, bitte erneut starten.“ | Lauf angehalten | erneut starten |

Die Höhe des Kontingents legt der Betreiber fest. Die Hilfe kennt die Zahl nicht. Sie steht in der Meldung.

### 17.3 Start, Lauf und Ergebnis

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Nicht gestartet: <Grund>“ | Start abgelehnt; der Grund steht dahinter | je nach Grund |
| „Nicht gestartet: Die Produkt-Datenbank ist leer.“ | keine Produkte | Produkte sammeln |
| „Nicht gestartet: Alle <Zahl> Produkte der Datenbank sind gerade in Arbeit – auf diesem oder einem anderen Gerät, oder sie warten auf ein eBay-Ergebnis.“ | Kein Produkt ist frei | Später erneut; ggf. „Ergebnisse bei eBay abholen“ |
| „Nicht gestartet: Produkt-Datenbank: nicht angemeldet oder Sitzung abgelaufen – Lauf nicht gestartet (Dashboard → Anmelden).“ | Nicht angemeldet | anmelden |
| „Nicht gestartet: Server nicht erreichbar – Lauf nicht gestartet. Die Produkt-Datenbank liegt auf dem Server, bitte später erneut starten.[ (HTTP <Zahl>)]“ | Server weg | später erneut |
| „Upload nicht gelungen: Keine eBay-Domain eingestellt (Einstellungen → Preise & Listing → „Domain“). – …“ bzw. „Nicht abgeholt: Keine eBay-Domain eingestellt …“ | „Domain“ fehlt; die Datei konnte nicht zu eBay | In den Einstellungen „Domain“ setzen, dann neu starten bzw. erneut abholen |
| „Nicht gestartet: Einstellungen fehlen: <Liste> (Einstellungen → eBay & Rahmenbedingungen)“ | Rahmenbedingungen oder Standort fehlen | eintragen |
| „In einem anderen Tab läuft gerade ein Lauf – bitte dort abwarten.“ / „Es läuft gerade ein Lauf oder ein Abholen.“ / „Es läuft schon ein Lauf.“ / „Es werden gerade Ergebnisdateien abgeholt – bitte kurz warten.“ | Es läuft schon etwas | abwarten; nur einen CSV-Lister-Tab benutzen |
| „Prüfe, ob der letzte Lauf noch in einem anderen Tab läuft … (bis 25 s)“ | Beim Öffnen der Seite | warten |
| „Läuft in einem anderen Tab“ | Fortschrittsanzeige zeigt einen Lauf aus einem anderen Tab | dort weiterarbeiten |
| „Abbruch angefordert – das laufende Produkt wird noch beendet.“ / „Wird abgebrochen – das laufende Produkt wird noch fertig“ | nach „Abbrechen“ | warten |
| „Abgebrochen – <Zahl> fertige Zeile(n) verworfen, die Produkte gehen zurück in die Datenbank.“ | Abbruch ohne Upload | nichts |
| „Keine Zeile entstanden – siehe Gründe in der Tabelle.“ | Alle Produkte wurden übersprungen oder zurückgestellt | Gründe unter „Produkte dieses Laufs“ lesen |
| „<Datei> hochgeladen: <Zahl> gelistet · <Zahl> abgelehnt …“ | Upload fertig und Ergebnis gelesen | nichts |
| „Upload nicht gelungen: <Grund> – die Produkte gehen zurück in die Datenbank und kommen beim nächsten Lauf wieder dran.“ | Upload gescheitert | eBay-Anmeldung prüfen, erneut |
| „Upload-Ergebnis unklar: <Grund>. Die Datei wurde [möglicherweise ]schon an eBay übergeben … – die Produkte warten auf die Ergebnisdatei: über „Ergebnisse bei eBay abholen" oder automatisch beim Start des nächsten Laufs.“ | Ob eBay die Datei hat, ist offen | „Ergebnisse bei eBay abholen“ |
| „Hole Ergebnisdateien aus dem Seller Hub …“ / „<Zahl> Ergebnisdatei(en) abgeholt: …“ / „Keine neue Ergebnisdatei bei eBay gefunden …“ / „Kein Produkt wartet auf ein eBay-Ergebnis.“ / „Nicht abgeholt: <Grund>“ | Rund um „Ergebnisse bei eBay abholen“ | Bei „Nicht abgeholt“: bei eBay anmelden (Grund z. B. „Seller Hub nicht erreichbar … – bist du bei eBay angemeldet?“), erneut |
| Fenster „<Zahl> Produkt(e) warten auf ein eBay-Ergebnis. Nur vergessen, wenn ihre CSV NICHT bei eBay hochgeladen wurde. …“ | Nach „Wartende vergessen“ | Nur „OK“, wenn die Datei sicher nicht bei eBay ist, sonst wird doppelt gelistet |
| „<Zahl> wartende(s) Produkt(e) vergessen – sie werden wieder normal gelistet.“ | Erledigt | nichts |

### 17.4 Gründe je Produkt (Tabelle „Produkte dieses Laufs“, Auswahl)

- „bereits von einem anderen Nutzer vergeben“: ein anderer Kunde hat das Produkt.
- „Amazon: kein Angebot/Versender auf der Seite (ausverkauft?)“: kein Angebot, das Produkt wird aussortiert.
- „Amazon: <Grund>“ (z. B. „Amazon: Produkt ist nicht auf Lager“): eine Prüfung aus Abschnitt 10.2 hat angeschlagen; das Produkt wird aussortiert.
- „Amazon: kein Titel“, „Amazon: keine Bilder“, „kein Verkaufspreis aus der Preisstaffelung“, „Titel nach Wortfilter leer“, „kein Kategorievorschlag von eBay“: das Produkt wird übersprungen.
- „Pflichtmerkmal ohne Spalte in der Muster-CSV: …“, „Pflichtmerkmal ohne passenden Wert (nur Auswahl/Zahl): …“: eBay verlangt eine Angabe, die nicht gefüllt werden kann.
- „keine ermäßigte eBay-Gebühr für „Neu: Sonstige" – …“: übersprungen wegen Gebühr.
- „Bild-Upload auf den Server scheitert: …“: Bilder ließen sich nicht hochladen.
- „… – zurückgestellt; lehnt eBay es in einem späteren Lauf … wieder ab, wird es aussortiert“: eBay hat das Produkt einmal abgelehnt; es bleibt in der Datenbank.
- „nicht mehr dran – die Seite war angehalten, inzwischen hat ein anderes Gerät das Produkt (oder es wurde gelöscht)“: der Tab war eingeschlafen; das Produkt ist nicht mehr bei diesem Lauf.

**Wichtig:** Ein übersprungenes (aussortiertes) Produkt verlässt beim CSV-Lister die Produkt-Datenbank. Ausnahme: Steht beim Grund „zurückgestellt“, bleibt das Produkt in der Datenbank.

### 17.5 Lauf angehalten (technische Gründe)

| Meldung | Was tun |
|---|---|
| „Anmeldung weg (Sitzung abgelaufen oder Zugang abgeschaltet) – Lauf angehalten.“ | Kommt auch bei einer Abo-Sperre. Im Dashboard Anmeldestand prüfen (Abschnitt 4.1 bzw. 7.4), neu anmelden |
| „Nicht angemeldet oder Sitzung abgelaufen – bitte im Dashboard neu anmelden.“ / „Dieser Zugang ist abgeschaltet.“ | „Dieser Zugang ist abgeschaltet.“ steht im CSV-Lister auch bei einer Abo-Sperre. Im Dashboard nachsehen: steht dort „Abo gesperrt“, Abschnitt 7.4; sonst anmelden bzw. beim Betreiber melden |
| „Amazon zeigt Captcha oder Anmeldeseite – Lauf angehalten. Bitte im Browser lösen und neu starten.“ | Auf Amazon die Abfrage selbst lösen, neu starten |
| „Amazon: bei <Zahl> Produkten hintereinander kein Versender erkennbar – Seitenaufbau vermutlich geändert, Lauf angehalten. Bitte melden.“ | Betreiber informieren |
| „Amazon-Skript: <Grund> – Lauf angehalten (Anmeldung/Mitgliedschaft prüfen).“ | Anmeldestand im Dashboard prüfen |
| „KI-Schnittstelle: <Grund>“ (z. B. mit „OpenAI-Guthaben leer …“ oder „OpenAI: API-Key ungültig …“) | OpenAI-Schlüssel und Guthaben prüfen (Abschnitt 18), neu starten |
| „KI-Schnittstelle vorübergehend nicht nutzbar: <Grund> – Lauf angehalten, später neu starten.“ / „KI-Schnittstelle antwortet nicht: <Grund>“ | später neu starten |
| „Bild-Server: … – Lauf angehalten.“ | später erneut; bleibt es: Betreiber |
| „Chrome lässt gerade keinen Tab öffnen: …“ | Keine Tabs ziehen oder verschieben, während der Lauf läuft; erneut starten |
| „Server bremst die eBay-Abfragen (zu viele je Minute) – neuer Versuch in <Zahl> s.“ | warten, die Extension versucht es selbst erneut |
| „Server bremst die eBay-Abfragen auch nach <Zahl> Wartezeiten – Lauf angehalten, bitte später neu starten.“ | Die Wartezeiten haben nicht gereicht. Später neu starten; kommt es oft: Betreiber |
| „eBay lehnt die Anfrage ab: …“ / „eBay-Rate-Limit erreicht – …“ / „eBay hat die Abfragen zu <Zahl> Produkten hintereinander abgelehnt …“ | später erneut; bleibt es: Betreiber |
| Meldungen, die die Einrichtung des Servers betreffen (z. B. beginnend mit „Server hat keinen eBay-Zugang“, „eBay-Zugang des Servers gestört …“, „Auf dem Server sind keine eBay-Schlüssel eingerichtet …“ oder Hinweise zu Bildadressen ohne HTTPS) | Das kann nur der Betreiber beheben. Screenshot an den Betreiber. Nichts selbst ändern |

### 17.6 Bereich „Technik“

Unten auf der Seite steht der aufklappbare Bereich „Technik“ („für die Fehlersuche: eBay-Zugang, Kategorie-Abfrage“). Die Knöpfe „Server und eBay-Zugang prüfen“ und „Abfragen“ zeigen dort technische Ergebnisse. Für Kunden heißt nur: Steht dort etwas Rotes oder ein Text mit „ACHTUNG“, einen Screenshot an den Betreiber schicken. **Nicht sicher belegt:** eine Erklärung der einzelnen Technik-Ausgaben; dafür ist der Betreiber zuständig.

---

## 18. OpenAI-Meldungen (Sammelstelle)

Die KI-Funktionen laufen über deinen **eigenen OpenAI-Schlüssel** (Einstellungen → Reiter „KI“ → Feld „OpenAI-API-Schlüssel (für die Titel-Generierung)“). Diese Meldungen stehen im Statusbericht (statt „Listen fehlgeschlagen – …“), im CSV-Lister („KI-Schnittstelle: …“) oder in anderen KI-Fehlern. Im Browser-Lister zeigt sich ein KI-Problem meist als „KI-Titel ist leer“ (10.3).

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Kein OpenAI API Key gesetzt (Options-Seite).“ | Kein Schlüssel eingetragen | Schlüssel in den Einstellungen, Reiter „KI“, eintragen |
| „OpenAI: API-Key ungültig oder abgelaufen – bitte prüfen (Einstellungen → KI → „OpenAI-API-Schlüssel“).“ | Schlüssel falsch, gelöscht oder abgelaufen | Bei OpenAI einen gültigen Schlüssel erzeugen und neu eintragen |
| „OpenAI-Guthaben leer: kein Guthaben mehr auf dem OpenAI-Konto. Bitte unter platform.openai.com unter Billing Guthaben aufladen.“ | Kein Guthaben bei OpenAI | Bei OpenAI Guthaben aufladen. Das Guthaben gehört zu deinem eigenen OpenAI-Konto, nicht zu Cash Lister |
| „OpenAI: Rate-Limit (zu viele Anfragen) – kurz warten und erneut versuchen.“ | Zu viele Anfragen in kurzer Zeit (z. B. viele gleichzeitige Tabs, mehrere PCs mit demselben Schlüssel) | Weniger gleichzeitig, später erneut |
| „OpenAI hat innerhalb von 90 Sekunden nicht geantwortet.“ | OpenAI war zu langsam | später erneut |
| „OpenAI nicht erreichbar: <Grund>“ | Keine Verbindung zu OpenAI | Internet prüfen, später erneut |
| „OpenAI <Zahl>: <Text>“ | Anderer Fehler von OpenAI | Text lesen; später erneut; bleibt es: Betreiber |
| „OpenAI: keine verwertbare Antwort (kein Function-Call) – evtl. Content-Filter beim Produkttext.“ | Die KI hat keine brauchbare Antwort geliefert, eventuell wegen des Produkttexts | Produkt überspringen oder später erneut |

---

## 19. Update-Programm

Die Meldungen von `update.bat` (Windows) und `update.command` (Mac) stehen ausführlich in `konto-und-installation.md` (Abschnitte zu Updates). Die häufigsten:

| Meldung | Was tun |
|---|---|
| „FEHLER: Die Einrichtungsdatei fehlt. …“ (`update.bat`) bzw. „FEHLER: Keine Zugangsdatei gefunden. Lege die Datei vom Betreiber (zugang.json oder leck-atakan-einrichtung-*.json) neben diese update.bat.“ | Einrichtungsdatei neben `update.bat` legen |
| „FEHLER: Im Ordner "extension" liegt keine Extension.“ | `update.bat` liegt am falschen Ort; sie muss neben dem Ordner `extension` liegen |
| „Chrome laeuft noch. Bitte Chrome KOMPLETT schliessen (auch im Infobereich unten rechts).“ | Chrome komplett schließen (auch unten rechts im Infobereich), dann eine Taste drücken |
| „FEHLER: Name oder Passwort stimmen nicht. Bitte beim Betreiber melden.“ | Neue Einrichtungsdatei beim Betreiber anfordern |
| „FEHLER: Dein Zugang ist abgeschaltet. Bitte beim Betreiber melden.“ | Betreiber |
| „FEHLER: Zu viele Versuche. Bitte ein paar Minuten warten.“ | warten |
| „FEHLER: Server nicht erreichbar (<Adresse>). Internetverbindung pruefen.“ | Internet prüfen, später erneut. Geht das Internet und steht im Dashboard „Abo gesperrt“: erst die Zahlung erledigen (Abschnitt 7.4) – auch dann kommt unter Windows diese Meldung |
| „FEHLER: Anmeldung fehlgeschlagen (HTTP <Zahl>).“ (Mac) | später erneut; bleibt es: Betreiber. Bei „HTTP 402“: Abo gesperrt (Abschnitt 7.4) |
| „FEHLER: Der Ordner 'extension' laesst sich nicht umbenennen. Laeuft Chrome doch noch? (…)“ | Chrome komplett schließen, erneut starten |
| „Du hast bereits die neueste Version.“ (Windows) bzw. „Du hast bereits die aktuelle Fassung. Nichts zu tun.“ (Mac) | nichts zu tun |
| „Aktualisiert auf Version <Zahl>.“ und „Fertig. Chrome jetzt wieder starten.“ (Windows) bzw. „Chrome kann jetzt wieder gestartet werden.“ (Mac) | Chrome starten. Die Versionsnummer steht links unten in der Seitenleiste. Danach sicherheitshalber den Hintergrunddienst aktualisieren (Abschnitt 3, Punkt 4) |
| „Update fehlgeschlagen - Meldungen oben.“ und „Deine alte Fassung ist unveraendert.“ (Windows) | Die Zeile mit „FEHLER:“ darüber lesen |

---

## 20. Häufige Fragen

**Was bedeutet „Nicht angemeldet oder Zugang deaktiviert - bitte im Dashboard anmelden.“?**
Du bist nicht angemeldet, dein Zugang ist abgeschaltet oder dein Abo gesperrt. Klick auf das Cash-Lister-Symbol oben rechts in Chrome, dann siehst du im Dashboard, was los ist.

**Der Tracker zeigt „Für den Tracker brauchst du die Ultimate-Mitgliedschaft.“ und dann eine leere Seite. Muss ich etwas kaufen?**
Nein. Die Meldung heißt nur, dass du nicht angemeldet bist (oder dein Zugang abgeschaltet bzw. dein Abo gesperrt ist). Im Dashboard anmelden und den Tracker-Tab neu laden.

**„Produkt-Vergabe: API-Key ungültig.“ – welchen Schlüssel soll ich eintragen?**
Keinen. Gemeint ist deine Anmeldung. Im Dashboard abmelden (Kontofeld oben rechts → „Abmelden“) und neu anmelden.

**In den Einstellungen steht „● Produkt-Vergabe: AUS – keine Server-Adresse hinterlegt.“ Muss ich eine Adresse eintragen?**
Nein. Dieser Text erscheint, wenn du nicht angemeldet bist. Im Dashboard anmelden und die Einstellungsseite neu laden (F5). Danach sollte „● Produkt-Vergabe: AN (über deine Anmeldung)“ stehen. Steht der Text trotz Anmeldung weiter da: Betreiber fragen.

**In der Seitenleiste steht „Server nicht erreicht“. Was passiert jetzt mit meinem Lauf?**
Ohne Server nehmen die Lister keine neuen Produkte aus der Produkt-Datenbank. Der Browser-Lister wartet und macht von selbst weiter, sobald der Server wieder antwortet; im Statusbericht steht dann eine „Hinweis“-Zeile. Es wird nichts ohne Reservierung gelistet.

**Im Tracker steht bei fast allen Zeilen „Error: …“. Ist alles kaputt?**
Nicht unbedingt. Außer „Success“ und „Skipped“ beginnt fast jeder Status mit „Error: “. Wichtig ist der Text danach: Abrufprobleme (z. B. „ERROR_503 …“, „Zeitüberschreitung (timeout) …“) ändern nichts an deinen Angeboten, „Artikel bei Amazon nicht verfügbar“ und ähnliche Fälle dagegen schon (Abschnitt 15.3).

**Ich sehe „Produkt bereits von einem anderen Nutzer vergeben“. Kann ich das Produkt trotzdem listen?**
Die Extension listet es nicht, weil ein anderer Kunde es zuerst übernommen hat. So macht ihr euch keine Konkurrenz. Such dir ein anderes Produkt. Ausnahmen kann nur der Betreiber beantworten.

**Warum steht im Amazon-Tab „… - ZUM LISTEN BESTÄTIGEN“, aber ich finde keinen Knopf zum Bestätigen?**
Das ist ein alter Wortlaut. Einen Bestätigen-Knopf gibt es nicht. Beim Listen wird das Produkt übersprungen; den Grund siehst du im Statusbericht. Auf Amazon-Seiten, die du selbst öffnest, ist es nur ein Hinweis ohne Folgen (Abschnitt 11.2).

**Im Statusbericht steht „KI-Titel ist leer“. Was ist los?**
Die KI hat keinen Titel geliefert. Fast immer fehlt der OpenAI-Schlüssel, er ist ungültig, oder das OpenAI-Guthaben ist leer (Abschnitt 18). Seit 46.0 gibt es keinen Start mehr ohne KI.

**Ich bekomme „Upload zu eBay fehlgeschlagen: unbekannt“. Ist wirklich nichts hochgeladen?**
Nicht unbedingt. Die Extension hat dann nur keine Bestätigung bekommen, und meist läuft der Upload trotzdem durch. Sieh bei eBay auf der Upload-Seite im Seller Hub nach (Adresse siehe Abschnitt 15.6), bevor du noch einmal hochlädst.

**Was ist der Unterschied zwischen „vorübergehend“ und „endgültig“ beim Tracker?**
Vorübergehend (z. B. „ERROR_503 …“, Netzwerkfehler, Zeitüberschreitung) heißt: Der Tracker weiß nicht, wie es um das Produkt steht, und ändert nichts. Endgültig (z. B. „Artikel bei Amazon nicht verfügbar“) heißt: Das Produkt gilt als nicht kaufbar, und beim Hochladen wird je nach Einstellung die Menge auf 0 gesetzt oder das Angebot beendet.

**Die Notbremse hat ausgelöst. Ist etwas kaputt?**
Nein, das ist ein Schutz. Entweder lieferten mehr als 70 % der Artikel kein brauchbares Ergebnis, oder 200 Artikel hintereinander galten als nicht kaufbar. Deshalb wurde nichts hochgeladen. Meist bremst Amazon gerade. Ablauf in Abschnitt 15.5.

**Im Dashboard steht „Zahlung offen“. Was muss ich tun?**
Auf „Jetzt bezahlen“ in der Warnleiste klicken und die Zahlung erledigen. Bis zum genannten Datum läuft alles weiter. Fragen zu Rechnungen und Beträgen beantwortet der Betreiber (Abschnitt 7).

**Ich sehe „Format geprüft …“ in meinen Meldungen. Was heißt das?**
Zu dieser Prüfung gibt es keine Beschreibung - bei Fragen an den Betreiber wenden.

**Warum sind ein paar Meldungen noch englisch?**
Seit 46.0 ist fast alles deutsch. Englisch geblieben sind einige Kennwörter im Tracker („Success“, „Skipped“, „ERROR_503“, „Tab failed to load“, das vorangestellte „Error: “ und „Unknown error“), technische Texte von Chrome und die Texte, die eBay oder Amazon selbst anzeigen.

---

## 21. Probleme und Lösungen (bereichsübergreifend)

### „Keine Antwort vom Hintergrunddienst“ / „keine Antwort vom Hintergrund“ / „? verfügbar“
**Ursache:** Der Hintergrunddienst schläft, hat neu gestartet oder läuft nach einem Update noch in der alten Version.
**Lösung:**
1. Seite neu laden (F5) und erneut versuchen.
2. Hilft das nicht: Chrome komplett schließen (auch unten rechts im Infobereich) und neu starten.
3. Hilft das nicht: `chrome://extensions` öffnen, bei Cash Lister auf „Neu laden“ klicken, danach offene Amazon-Seiten und Cash-Lister-Tabs neu laden.

### Überall „Nicht angemeldet“, obwohl ich mich angemeldet hatte
**Ursache:** Die Sitzung ist abgelaufen, das Passwort wurde geändert, oder deine Version ist unter die Mindestversion gefallen. Eine eigene Meldung dafür gibt es nicht.
**Lösung:** Im Dashboard neu anmelden. Kommt dabei „Deine Version der Extension ist veraltet …“: Update machen. Kommt „Name oder Passwort falsch.“: Einrichtungsdatei verwenden oder den Betreiber fragen.

### Module in der Seitenleiste sind ausgegraut
**Ursache:** Nicht angemeldet, Zugang abgeschaltet oder Abo gesperrt.
**Lösung:** Verbindungskasten links unten lesen (Abschnitt 5) und entsprechend handeln.

### Einstellungen zeigen „● Produkt-Vergabe: AUS – keine Server-Adresse hinterlegt.“
**Ursache:** Du bist nicht angemeldet (der Text ist irreführend, siehe 8.2).
**Lösung:** Im Dashboard anmelden, Einstellungsseite neu laden (F5). Nichts in das Feld „Server-Adresse“ eintragen.

### „Server nicht erreichbar“ / „Server nicht erreicht“ an mehreren Stellen
**Ursache:** Internet weg, Firewall/Virenschutz blockiert, oder der Server ist gerade nicht erreichbar.
**Folgen seit 46.0:** Die Produkt-Datenbank ist nicht abrufbar, Importe scheitern mit einer Meldung (es wird nichts halb gespeichert), der Browser-Lister pausiert und macht von selbst weiter, der CSV-Lister startet nicht.
**Lösung:**
1. Internetverbindung prüfen (eine beliebige Webseite öffnen).
2. Etwas warten und erneut versuchen.
3. Das Feld „Server-Adresse“ nicht selbst ändern.
4. Bleibt es über längere Zeit: Betreiber informieren.

### Dashboard zeigt „Abo gesperrt“
**Lösung:** Abschnitt 7.4.

### Meldungen zu eBay-Seiten (Bericht, Upload, Listen) schlagen alle fehl
**Ursache:** eBay-Anmeldung im Chrome-Profil abgelaufen, oder eBay zeigt eine Sicherheitsabfrage.
**Lösung:** eBay im selben Chrome-Profil öffnen, anmelden, eine eventuelle Abfrage selbst lösen, dann erneut versuchen.

### Viele Amazon-Fehler (Captcha, Sperrseite, „ERROR_503“, Notbremse)
**Ursache:** Amazon bremst wegen zu vieler Seitenaufrufe.
**Lösung:**
1. Eine Amazon-Seite selbst öffnen und eine Sicherheitsabfrage lösen.
2. Eine Weile (z. B. 15–30 Minuten) warten.
3. Weniger gleichzeitige Tabs: im Tracker „Gleichzeitig“, im Browser-Lister „Gleichzeitig“ verkleinern. „Gleichzeitig“ im Tracker bestimmt auch, wie viele Prüf-Tabs der Knopf „→ Datenbank“ mit „nur Verkauf durch Amazon“ gleichzeitig öffnet.

**Nicht sicher belegt:** Wie lange Amazon-Sperren typischerweise dauern. Das hängt von Amazon ab.

### Im Tracker steht bei (fast) allen Zeilen „Skipped“
**Ursache:** Bei „Lieferant“ steht „Keiner“, oder die Angebote haben keine SKU, die diese Extension vergeben hat (z. B. von Hand eingestellt oder mit einem anderen Programm).
**Lösung:** „Lieferant“ auf „Amazon“ stellen. Angebote mit fremder SKU kann der Tracker nicht prüfen; sie bleiben unverändert.

### Im Tracker viele „Artikel bei Amazon nicht verfügbar“, obwohl die Produkte lieferbar sind
**Mögliche Ursachen:**
1. „eBay-Seite“ passt nicht zum Amazon-Marktplatz der Produkte (bei „Keine“ prüft der Tracker amazon.com).
2. Die Lieferzeit ist länger als „Max. verlängerte Lieferzeit“ in den Einstellungen (Vorgabe 20 Tage). Das zählt auch bei ausgeschaltetem Schalter (Hinweis in 10.2).

**Lösung:** Beide Punkte prüfen, ein Produkt aus der Tabelle selbst öffnen und vergleichen. Den Tracker vorher pausieren, denn nach jedem fertigen Lauf wird automatisch hochgeladen. Passt beides und das Problem bleibt: Screenshot an den Betreiber. Andere Ursachen kennt die Hilfe nicht sicher.

### Browser-Lister startet nicht: „Alle … Produkte der Datenbank sind gerade in Arbeit“
**Ursache:** Ein anderer Lister (anderes Gerät deines Kontos oder der CSV-Lister) hat gerade alle freien Produkte entnommen.
**Lösung:** In der Produkt-Datenbank in die Spalte „In Arbeit“ schauen. Läuft dort wirklich etwas, später erneut starten oder neue Produkte sammeln. Ist ein Gerät abgestürzt, werden die Produkte nach Ablauf der angezeigten Zeit („bis <Uhrzeit>“) von selbst wieder frei.

### Eine Meldung ist hier nicht aufgeführt
**Lösung:** Ehrlich sagen, dass die Hilfe diese Meldung nicht kennt. Den Kunden bitten, einen Screenshot, die Version (links unten in der Seitenleiste), den Bereich und die letzten Schritte an den Betreiber zu schicken (siehe SKILL.md, „Weitergeben an den Betreiber“).

---

## 22. Was diese Datei nicht sicher weiß

- **Nicht sicher belegt:** Ob der Server über die hier genannten Texte hinaus weitere Meldungen schickt, die die Extension wörtlich anzeigt (vor allem in Klammern hinter „HTTP <Zahl>“ und bei „eBay lehnt die Anfrage ab: …“ im CSV-Lister). Für das Anmelden im Dashboard sind die Texte in Abschnitt 4.2 nach dem heutigen Stand vollständig.
- **Nicht sicher belegt:** Wie lange es nach einer längeren Pause dauert, bis in Seitenleiste und Dashboard statt „Server nicht erreicht“ wieder „Server verbunden“ steht (Abschnitt 5).
- **Nicht sicher belegt:** Die genauen Statustexte der Karte „Dein Abo“ und der Sperrtext bei „Abo gesperrt“ kommen vom Server und können sich ändern. Die Beispiele in Abschnitt 7 entsprechen dem Stand bei Erscheinen von 46.0.
- **Nicht sicher belegt:** Ob dieses Verhalten so bleiben soll: Beim Listen und im Tracker gilt der Wert „Max. verlängerte Lieferzeit“ auch bei ausgeschaltetem Schalter.
- **Nicht sicher belegt:** Wie ein Google-Apps-Script für den Sheet-Abgleich aufgebaut sein muss (Schreiben ins Haupt-Sheet und Lesen über eine Web-App-Adresse).
- **Nicht sicher belegt:** Wie die Menüpunkte bei eBay genau heißen, über die man zur Upload- bzw. Berichtsseite im Seller Hub kommt (die Adressen stehen in 15.2 und 15.6).
- **Nicht sicher belegt:** Die vollständige Liste der CSV-Lister-Meldungen (Abschnitt 17 ist eine Auswahl) und eine Erklärung der Ausgaben im Bereich „Technik“.
- **Nicht sicher belegt:** Wie lange Amazon- oder eBay-Sperren dauern.
- **Nicht sicher belegt:** Wie lange nach einer Zahlung die Abo-Sperre im Einzelfall aufgehoben ist (laut AGB „in der Regel automatisch“).
- Die Prüfung des Angebotsformats („Format geprüft …“, „Nicht eingestellt: … Sofort-Kaufen …“): Zu dieser Prüfung gibt es keine Beschreibung - bei Fragen an den Betreiber wenden.

---

## 23. Neu in Version 46.0

Hier steht nur, was sich bei den **Meldungen** geändert hat. Änderungen an Knöpfen und Seiten stehen in den jeweiligen Bereichsdateien.

- **Kein Popup mehr:** Das kleine Fenster beim Klick auf das Symbol gibt es nicht mehr – es öffnet sich das Dashboard. Damit sind alle Meldungen des Popups weg (z. B. „Not logged in“, „Angemeldet als …“ oben im Fenster, „End Price: An/Aus“). Anmeldung und ihre Meldungen stehen jetzt in der Anmeldekarte des Dashboards (Abschnitt 4), Export/Import und Server-Sicherung in Einstellungen → Reiter „Sicherung“ (Abschnitt 8.3/8.4). Hinweise wie „… bitte im Popup anmelden“ heißen jetzt „… bitte im Dashboard anmelden“.
- **Neue Anzeigen:** Verbindungskasten in der Seitenleiste (Abschnitt 5), Glocke, Kennzahlen und Checkliste im Dashboard (Abschnitt 6).
- **Abo:** Warnleiste, Karte „Dein Abo“, „Abo verwalten“ und die Abo-Sperre sind neu (Abschnitt 7).
- **Irreführende englische Texte ersetzt:** Die frühere englische Meldung beim Start des Bulk-Listers ohne Anmeldung heißt jetzt „Nicht angemeldet oder Zugang deaktiviert - bitte im Dashboard anmelden.“; die frühere englische Tracker-Meldung zur Mitgliedschaft heißt jetzt „Für den Tracker brauchst du die Ultimate-Mitgliedschaft.“ (Bedeutung beide Male unverändert: nicht angemeldet).
- **Statusbericht deutsch:** z. B. „Item Listed Successfully!“ → „Erfolgreich gelistet!“, „Item is duplicate“ → „Produkt ist schon gelistet (Duplikat)“, „Item is not in stock“ → „Produkt ist nicht auf Lager“, „Price is too high“ → „Amazon-Preis zu hoch (Filter „Preis bis“)“, „Title is undefined“ → „KI-Titel ist leer“, „Title generation error“ → „Titel-Erstellung fehlgeschlagen“, „Auto listing failed“ → „Listen fehlgeschlagen – keine verwertbare Antwort der Amazon-Seite“, „insertion fees“ → „Nicht eingestellt: eBay verlangt Angebotsgebühren …“, „Item Failed to List! …“ → „Einstellen fehlgeschlagen, eBay nennt keinen Grund: …“, „Ebay Error Page“ → „eBay-Fehlerseite - Angebot nicht eingestellt“, „timeout: no response after 15 minutes“ → „Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“, „Condition Grading Error, not supported“ → „Zustand nicht wählbar: Kachel „Neu mit Etikett“ nicht gefunden“. Neu ist die Statusart „Hinweis“ für Server-Pausen.
- **Tab-Titel deutsch:** „WARNING! … - CONFIRM TO LIST“ → „WARNUNG! … - ZUM LISTEN BESTÄTIGEN“, „SKIPPED! …“ → „ÜBERSPRUNGEN! …“, „Submitted the Listing!“ → „Angebot eingestellt!“, „Failed to Submit the Listing!“ → „Einstellen fehlgeschlagen!“, „✅ Removed restricted words from item specifics“ → „✅ Sperrbegriffe aus den Artikelmerkmalen entfernt“.
- **Titel immer per KI:** Den Start ohne KI („Standard-List (0.2)“) gibt es nicht mehr, damit auch keine Meldungen dazu.
- **Produkt-Datenbank auf dem Server:** Neue Meldungen bei fehlender Anmeldung oder fehlendem Server (Abschnitt 13), Hinweise zur ersten Übertragung, die Spalte „In Arbeit“ und „Alle … Produkte der Datenbank sind gerade in Arbeit …“. Die Warnung „… OHNE Reservierung aufgenommen …“ beim Import in die Produkt-Datenbank gibt es nicht mehr – ohne Server wird nichts importiert. Beim Grabber heißt es jetzt „… von anderen Kunden belegt“ statt „an anderen Nutzer vergeben“.
- **Tracker deutsch:** Statustexte (z. B. „Item is not available on Amazon“ → „Artikel bei Amazon nicht verfügbar“, „ERROR_503: IP is blocked on Amazon“ → „ERROR_503: IP bei Amazon gesperrt“, „SKU mismatch: …“ → „ASIN passt nicht: …“, „Timeout occurred while waiting for the message.“ → „Zeitüberschreitung (timeout): keine Antwort von der Seite im Tab.“), „⏳ Hold Tight!“ → „⏳ Kurz warten!“, „Continuous Tracking …“ → „Dauerbetrieb …“, Upload-Tab-Titel („✅ Hochladen fertig!“ statt „✅ Upload complete!“). Englisch geblieben sind nur „Success“, „Skipped“, „ERROR_503“, „Tab failed to load“, das vorangestellte „Error: “ und „Unknown error“. Nach jedem fertigen Lauf wird immer hochgeladen.
- **Einstellungen:** „Settings saved“ → „Einstellungen gespeichert“, „Words:“ → „Wörter:“. Das Feld „Erlaubter Bildabstand“ beim Bildabgleich gibt es nicht mehr.
- **Konkurrenz-Scanner:** „Abgebrochen.“ heißt jetzt „Gestoppt.“ (Knopf „Stoppen“), die Funde bis dahin bleiben.
- **CSV-Lister für alle:** Er braucht keinen Zugangscode mehr. Der Hinweis „Dieses Modul ist noch im Test“ mit Codefeld erscheint nicht mehr. Läuft der Browser-Lister gleichzeitig, ist das kein Problem mehr.
- **Mindestversion:** Unverändert gilt: Versionen unter der Mindestversion können sich nicht anmelden („Deine Version der Extension ist veraltet …“). Nach jedem Update Chrome komplett neu starten bzw. den Hintergrunddienst aktualisieren.
