# Produkte finden und verwalten

Dieser Bereich erklärt, wie Produkte von Amazon (oder aus dem Angebot eines eBay-Konkurrenten) in Cash Lister kommen, wo sie bis zum Listen warten und welche Helfer Cash Lister dafür auf Amazon- und eBay-Seiten einblendet. Seit Version 46.0 liegt die **Produkt-Datenbank je Konto auf dem Server**: Alle deine Geräte sehen dieselbe Liste. Wie der Browser-Lister die Produkte beim Listen benutzt, steht ausführlich im Bereich Browser-Lister (`references/listen-auf-ebay.md`, Abschnitt 6).

## Inhalt

1. [Überblick: Wie kommen Produkte in Cash Lister?](#1-überblick-wie-kommen-produkte-in-cash-lister)
2. [Begriffe kurz erklärt](#2-begriffe-kurz-erklärt)
3. [Amazon-Suchseiten: der Knopf zur Datenbank (Produkt-Grabber)](#3-amazon-suchseiten-der-knopf-zur-datenbank-produkt-grabber)
4. [Schalter nur Verkauf durch Amazon](#4-schalter-nur-verkauf-durch-amazon)
5. [Verkäufer-Schaufenster und Ganzer Shop](#5-verkäufer-schaufenster-und-ganzer-shop)
6. [Die Amazon-Filter in den Einstellungen](#6-die-amazon-filter-in-den-einstellungen)
7. [Die Einstellung Domain und das Amazon-Land deiner Produkte](#7-die-einstellung-domain-und-das-amazon-land-deiner-produkte)
8. [Amazon-Produktseiten (Adresse mit /dp/)](#8-amazon-produktseiten-adresse-mit-dp)
9. [Amazon-Verkäuferseiten (Adresse mit /sp)](#9-amazon-verkäuferseiten-adresse-mit-sp)
10. [Die Produkt-Datenbank](#10-die-produkt-datenbank)
    - [10.1 Eine Liste für alle Geräte deines Kontos](#101-eine-liste-für-alle-geräte-deines-kontos)
    - [10.2 So öffnest du die Produkt-Datenbank](#102-so-öffnest-du-die-produkt-datenbank)
    - [10.3 Aufbau der Seite](#103-aufbau-der-seite)
    - [10.4 Die Zahlen oben und der Hinweis zur Übertragung](#104-die-zahlen-oben-und-der-hinweis-zur-übertragung)
    - [10.5 Roter Kasten: Server nicht erreichbar oder nicht angemeldet](#105-roter-kasten-server-nicht-erreichbar-oder-nicht-angemeldet)
    - [10.6 Erster Start nach dem Update: deine alte Liste wandert auf den Server](#106-erster-start-nach-dem-update-deine-alte-liste-wandert-auf-den-server)
    - [10.7 Links hinzufügen (von Hand)](#107-links-hinzufügen-von-hand)
    - [10.8 Die Tabelle Bestand](#108-die-tabelle-bestand)
    - [10.9 Die Spalte In Arbeit](#109-die-spalte-in-arbeit)
    - [10.10 Einzelne Produkte löschen](#1010-einzelne-produkte-löschen)
    - [10.11 Alle löschen](#1011-alle-löschen)
    - [10.12 Die Sortierung](#1012-die-sortierung)
    - [10.13 Als TXT exportieren](#1013-als-txt-exportieren)
    - [10.14 Verbindung zum Browser-Lister](#1014-verbindung-zum-browser-lister)
    - [10.15 Häufige Fragen (Produkt-Datenbank)](#1015-häufige-fragen-produkt-datenbank)
    - [10.16 Probleme und Lösungen (Produkt-Datenbank)](#1016-probleme-und-lösungen-produkt-datenbank)
11. [Sheet-Abgleich: Schutz vor doppelten eigenen Angeboten](#11-sheet-abgleich-schutz-vor-doppelten-eigenen-angeboten)
12. [Der Konkurrenz-Scanner](#12-der-konkurrenz-scanner)
13. [Produktvergabe: damit nicht zwei Kunden dasselbe Produkt listen](#13-produktvergabe-damit-nicht-zwei-kunden-dasselbe-produkt-listen)
14. [eBay-Artikelseiten: die violette Lupe](#14-ebay-artikelseiten-die-violette-lupe)
15. [Was dieser Bereich nicht kann](#15-was-dieser-bereich-nicht-kann)
16. [Neu in Version 46.0](#16-neu-in-version-460)

---

## 1. Überblick: Wie kommen Produkte in Cash Lister?

Es gibt zwei „Vorräte“, aus denen der Browser-Lister später Angebote baut (die Produkt-Datenbank benutzt außerdem der CSV-Lister, siehe `references/produktuebersicht-und-csv-lister.md`):

| Vorrat | Wie kommen Produkte hinein? | Wo liegt er? | Wo verwaltest du ihn? |
|---|---|---|---|
| **Produkt-Datenbank** | (a) auf Amazon-Suchseiten mit dem blauen Knopf unten rechts, (b) im Verkäufer-Schaufenster auf Amazon (auch alle Seiten auf einmal), (c) von Hand: Links oder ASINs einfügen | **auf dem Server, je Konto** – gemeinsam für alle deine Geräte | Seitenleiste → „Produkt-Datenbank“ |
| **Funde des Konkurrenz-Scanners** | Der Scanner sucht zu den Produkten eines eBay-Verkäufers die passende Amazon-Quelle; außerdem Import einer CSV-Datei | **nur in diesem Chrome-Profil** | Seitenleiste → „Konkurrenz-Scanner“ |

Wichtig zum Verständnis:

- **Ohne Anmeldung oder ohne erreichbaren Server kommt nichts in die Produkt-Datenbank.** Der Knopf auf Amazon und „Zur Datenbank hinzufügen“ melden dann, dass nichts importiert wurde (Abschnitte 3.5 und 10.7).
- Im Browser-Lister wählst du bei „Produkte aus“, aus welchem Vorrat ein Lauf seine Produkte nimmt: „Produkt-Datenbank“ oder „Konkurrenz-Scanner“. Ein Lauf nimmt immer nur aus **einem** Vorrat.
- Jedes Produkt in deiner Produkt-Datenbank ist für dein Konto reserviert (Produktvergabe, Abschnitt 13). Produkte, die schon ein anderer Kunde hat, kommen gar nicht erst hinein („belegt“).
- Produkte, die du laut deinen Google Sheets schon gelistet hast, kommen ebenfalls nicht in die Produkt-Datenbank (Sheet-Abgleich, Abschnitt 11). Dasselbe gilt für Produkte, die du mit deinem Konto schon erfolgreich gelistet hast (Abschnitt 3.4, „bereits gelistet“).
- Beide Werkzeuge öffnest du über die **Seitenleiste** links auf jeder Seite von Cash Lister: „Produkt-Datenbank“ steht in der Gruppe „Arbeiten“, „Konkurrenz-Scanner“ in der Gruppe „Auswerten“ (die Gruppennamen werden in Großbuchstaben angezeigt). Ohne Anmeldung sind diese Einträge ausgegraut. Das Dashboard öffnest du mit einem Klick auf das Cash-Lister-Symbol in der Chrome-Leiste.

---

## 2. Begriffe kurz erklärt

- **ASIN**: Amazons Artikelnummer, 10 Zeichen lang, z. B. `B0ABCDEFGH`. Du findest sie in der Adresse einer Amazon-Produktseite hinter `/dp/`. Cash Lister erkennt jedes Produkt an seiner ASIN – doppelte ASINs werden zusammengefasst.
- **Kachel**: ein einzelnes Produkt in der Trefferliste einer Amazon-Suche (Bild, Titel, Preis, Sterne).
- **Buybox**: der Kaufkasten rechts auf einer Amazon-Produktseite mit „In den Einkaufswagen“. Der Händler, dessen Angebot dort steht, ist der „Buybox-Verkäufer“.
- **FBA** („Fulfillment by Amazon“, Versand durch Amazon): Die Ware liegt in einem Amazon-Lager und Amazon verschickt sie – auch wenn ein anderer Händler sie verkauft.
- **„Verkauf und Versand durch Amazon“**: Amazon selbst ist der Verkäufer. Das ist strenger als FBA.
- **Verkäufer-Schaufenster**: die Amazon-Suchseite mit allen Produkten eines bestimmten Händlers (in der Adresse steht `me=`).
- **Produkt-Datenbank (je Konto)**: deine Warteliste mit Amazon-Produkten, die noch gelistet werden sollen. Sie liegt auf dem Server und ist auf allen Geräten, auf denen du mit demselben Konto angemeldet bist, dieselbe.
- **Gerät**: ein Chrome-Profil mit Cash Lister. Zwei Chrome-Profile auf demselben Rechner zählen als zwei Geräte.
- **„In Arbeit“**: Ein Produkt der Produkt-Datenbank, das gerade ein Gerät (oder der CSV-Lister) zum Listen genommen hat. Andere Geräte bekommen es so lange nicht.
- **„frei“**: ein Produkt der Produkt-Datenbank, das gerade niemand in Arbeit hat. Nur freie Produkte kann ein Lauf nehmen.
- **„belegt“**: Ein anderer Kunde hat dieses Produkt schon. Es kommt nicht in deine Produkt-Datenbank.
- **SKU / Custom Label / Bestandseinheit**: deine eigene Artikelnummer bei eBay. eBay.de nennt das Feld „Bestandseinheit“, die englische eBay-Seite „Custom label (SKU)“. Cash Lister trägt dort beim Listen eine eigene Kennung ein (endet auf „==“).
- **GPSR**: EU-Produktsicherheitsverordnung. Gemeint sind die Angaben zum Hersteller und zur verantwortlichen Person in der EU, die eBay bei vielen Angeboten verlangt.
- **Produktvergabe / Reservierung**: Cash Lister meldet dem Server, welche Produkte du bearbeitest. So listen nicht zwei Kunden dasselbe Amazon-Produkt (Abschnitt 13).
- **Sheet-Abgleich**: Cash Lister liest deine hinterlegten Google Sheets und überspringt Produkte, die dort schon als gelistet stehen (Abschnitt 11).

---

## 3. Amazon-Suchseiten: der Knopf zur Datenbank (Produkt-Grabber)

### 3.1 Wo und wann erscheint der Knopf?

Der Knopf erscheint **unten rechts** auf Amazon-Seiten, deren Adresse mit `www.amazon.<Land>/s` beginnt, und zwar nur in zwei Fällen:

1. **Normale Suche** (du hast oben bei Amazon einen Suchbegriff eingegeben; in der Adresse steht `k=`).
2. **Verkäufer-Schaufenster** (alle Produkte eines Händlers; in der Adresse steht `me=`).

Auf Kategorie-Seiten ohne Suchbegriff, auf Marken-Shops und auf anderen Amazon-Seiten ist der Knopf ausgeblendet – dort gibt es auch keine Häkchen auf den Kacheln.

Unterstützte Amazon-Länder: amazon.de, .com, .co.uk, .fr, .it, .es, .nl, .ca, .com.au, .co.jp, .in, .com.br, .com.mx (jeweils mit `www.` davor).

**Vorher anmelden:** Melde dich vor dem Einsammeln im Dashboard an. Ohne Anmeldung zeigt der Knopf zwar alles an, aber beim Klick kommt „❌ Bitte zuerst in Cash Lister anmelden – nichts importiert.“

**Welches Amazon-Land gespeichert wird:** Gespeichert wird nur die **ASIN**. Mit welchem Amazon-Land das Produkt später geöffnet und gelistet wird, bestimmt deine Einstellung „Domain“ – nicht die Amazon-Seite, auf der du eingesammelt hast (Abschnitt 7).

### 3.2 Was du auf der Seite siehst

**a) Der Hauptknopf (dunkelblau, rund, unten rechts)**

Er zeigt, wie viele Produkte er importieren würde, zum Beispiel:

- „📦 48 Produkte → Datenbank“ – alle 48 übernehmbaren Kacheln sind angehakt.
- „📦 45 von 48 Produkten → Datenbank“ – du hast 3 Häkchen entfernt.
- „📦 40 Produkte · 8 vom Filter ausgeschlossen → Datenbank“ – 8 Kacheln fallen durch deine Amazon-Filter (Abschnitt 6).

Wenn du mit der Maus über den Knopf fährst, zeigt ein Hinweisfenster, **welcher Filter wie viele Produkte ausgeschlossen hat** (nur wenn überhaupt ein Filter etwas ausschließt). Die erste Zeile lautet z. B. „8 Produkt(e) vom Filter ausgeschlossen:“, darunter je Filter eine Zeile:

- „• 5 × Lieferung dauert länger als 20 Tage (Einstellungen → Produkt-Filter → „Max. verlängerte Lieferzeit“)“
- „• 2 × Amazon-Preis außerhalb von höchstens 100 € (Einstellungen → Produkt-Filter → „Preis ab“ / „Preis bis“)“ (je nach Einstellung auch „mindestens 5 €“ oder „5–100 €“)
- „• 1 × weniger als 4,5 Sterne (Einstellungen → Produkt-Filter → „Mind. Sterne“)“ (eine ganze Zahl steht ohne Komma da, z. B. „weniger als 4 Sterne“)
- „• … × weniger als 6 auf Lager (Einstellungen → Produkt-Filter → „Mind. Lagerbestand“)“
- „• … × weniger als 20 Bewertungen (Einstellungen → Produkt-Filter → „Mind. Bewertungen“)“

Ein Produkt kann an mehreren Filtern scheitern; die Gesamtzahl im Knopf zählt es trotzdem nur einmal.

**b) Die Häkchen-Pillen auf den Produktbildern**

Jede übernehmbare Kachel bekommt **oben rechts im Produktbild** eine farbige Pille mit Häkchen:

| Pille | Farbe | Bedeutung |
|---|---|---|
| „importieren“ | blau | angehakt, wird übernommen |
| „übersprungen“ | grau | du hast das Häkchen entfernt, wird nicht übernommen |
| „Amazon ✓“ | blau | nur mit „nur Verkauf durch Amazon“: Amazon verkauft selbst, wird übernommen |
| „nicht Amazon“ | grau | nur mit „nur Verkauf durch Amazon“: ein anderer Händler verkauft, wird nicht übernommen |
| „kein Angebot“ | grau | nur mit „nur Verkauf durch Amazon“: kein Angebot in der Buybox (nicht lieferbar), wird nicht übernommen |

- Alle Häkchen sind **von Anfang an gesetzt**. Nimm das Häkchen weg, um ein Produkt auszulassen.
- Ein Klick auf die Pille öffnet **nicht** das Produkt – er schaltet nur das Häkchen um.
- Hinweis beim Darüberfahren: „Häkchen weg = nicht übernehmen“, bei geprüften Produkten „Verkäufer: <Name> – wird nicht übernommen“ bzw. „Kein Angebot in der Buybox (nicht lieferbar) – wird nicht übernommen“.
- Kacheln **ohne** Pille werden nicht übernommen: das sind gesponserte Anzeigen, Produkte, die an einem Filter scheitern, und Kacheln außerhalb der eigentlichen Trefferliste (z. B. Karussells mit „ähnlichen Produkten“).
- Deine Abwahl bleibt erhalten, solange die Seite offen ist, auch wenn Amazon Teile der Seite nachlädt.

**c) Der zweite Knopf darüber**

- Auf einer **normalen Suche**: der Schalter „nur Verkauf durch Amazon“ (Abschnitt 4).
- Im **Verkäufer-Schaufenster**: der Knopf „📚 Ganzer Shop → Datenbank“ (Abschnitt 5).

**d) Das Meldungsfeld**

Über den Knöpfen erscheint ein weißes Feld mit Meldungen (z. B. das Ergebnis eines Imports). Ergebnis- und Hinweismeldungen verschwinden nach etwa 8 Sekunden. Stehen bleiben (bis zur nächsten Meldung): „Importiere … Produkte …“, die Meldungen zur laufenden Verkäufer-Prüfung, die Meldungen, auf die du reagieren musst (z. B. Captcha oder „Prüfung abgebrochen …“), und die Fehlermeldungen „❌ Nichts importiert …“, „❌ Bitte zuerst in Cash Lister anmelden …“ und „⚠️ Nur teilweise importiert …“.

Während ein Import läuft, lässt sich der blaue Knopf nicht anklicken; er wird wieder klickbar, sobald die Antwort da ist.

### 3.3 Welche Kacheln überhaupt übernommen werden

Gezählt wird **eine ASIN pro Kachel** – Farb- oder Größenvarianten innerhalb einer Kachel werden nicht einzeln übernommen. Ausgelassen werden:

1. **Gesponserte Kacheln** (Anzeigen).
2. Kacheln aus Karussells außerhalb der eigentlichen Trefferliste (z. B. „ähnliche Produkte“).
3. Kacheln, die an einem deiner **Amazon-Filter** scheitern (Lieferzeit, Preis, Sterne, Lagerbestand, Anzahl Bewertungen – Abschnitt 6).
4. Kacheln, deren Häkchen du entfernt hast.

### 3.4 Schritt für Schritt: Suchergebnisse in die Datenbank holen

1. Melde dich im Dashboard an (falls noch nicht geschehen).
2. Öffne Amazon (z. B. amazon.de) und suche oben nach einem Begriff oder einer Marke.
3. Warte, bis die Trefferliste geladen ist. Unten rechts erscheint der blaue Knopf „📦 … → Datenbank“.
4. Schau dir die Kacheln an und nimm bei unpassenden Produkten das Häkchen in der Pille weg.
5. Optional: Fahre mit der Maus über den Knopf, um zu sehen, was deine Filter ausschließen.
6. Klicke auf den blauen Knopf. Es erscheint „Importiere … Produkte …“ (bei mehr als 200 Produkten zusätzlich „Bei so vielen dauert das etwas.“).
7. Nach dem Import steht im Meldungsfeld z. B.:
   „✅ 40 neu in der Datenbank · 3 schon in DB · 2 bereits gelistet · 1 von anderen Kunden belegt · Bestand: 312 (3 abgewählt)“
8. Blättere auf die nächste Ergebnisseite und wiederhole die Schritte 4 bis 7. Doppelte Produkte werden automatisch übersprungen.

Bedeutung der Zahlen in der Erfolgsmeldung:

| Teil der Meldung | Bedeutung |
|---|---|
| „neu in der Datenbank“ | wirklich neu aufgenommen (und damit für dich reserviert) |
| „schon in DB“ | diese ASIN lag schon in der Produkt-Datenbank deines Kontos (egal, von welchem Gerät sie kam) |
| „bereits gelistet“ | steht in einem deiner Google Sheets als schon gelistet (Abschnitt 11) **oder** wurde mit deinem Konto schon erfolgreich gelistet (laut Produktvergabe) |
| „von anderen Kunden belegt“ | ein anderer Kunde hat das Produkt schon; es kommt nicht in deine Datenbank (Abschnitt 13) |
| „Bestand: …“ | so viele Produkte liegen jetzt insgesamt in der Produkt-Datenbank deines Kontos (alle Geräte, auch die „In Arbeit“) |
| „(… abgewählt)“ | so viele Häkchen hattest du entfernt |

**Nicht sicher belegt:** wie lange der Server sich merkt, dass du ein Produkt schon gelistet hast (und es deshalb als „bereits gelistet“ meldet). Wenn das für dich wichtig ist, frag den Betreiber.

### 3.5 Alle Meldungen des Knopfs auf Suchseiten

| Meldung | Bedeutung / was tun |
|---|---|
| „Importiere … Produkte …“ | Der Import läuft. Warten. |
| „✅ … neu in der Datenbank · …“ | Fertig (siehe Tabelle oben). |
| „Alle … Produkte sind abgewählt – nichts zu importieren.“ | Du hast alle Häkchen entfernt. |
| „Keine Produktkacheln auf dieser Seite gefunden.“ | Es gibt keine übernehmbaren Kacheln. Das erscheint **auch**, wenn alle Kacheln von deinen Filtern ausgeschlossen werden – schau in den Knopftext („… vom Filter ausgeschlossen“). |
| „❌ Bitte zuerst in Cash Lister anmelden – nichts importiert.“ | Du bist nicht (mehr) angemeldet – oder deine Anmeldung ist abgelaufen. Dieselbe Meldung kommt auch, wenn dein Zugang abgeschaltet oder dein Abo gesperrt ist. Es wurde nichts gespeichert. Im Dashboard anmelden, dann auf der Amazon-Seite einfach noch einmal klicken (neu laden ist nicht nötig – deine Häkchen und eine schon gelaufene Verkäufer-Prüfung bleiben so erhalten). Steht unten in der Seitenleiste von Cash Lister „Abo gesperrt“ oder „Zugang abgeschaltet“, liegt es daran – siehe `references/konto-und-installation.md`. |
| „❌ Nichts importiert – Server nicht erreichbar. Bitte später erneut versuchen.“ | Der Server hat nicht geantwortet. Es wurde **nichts** gespeichert. Später erneut klicken. Hält das an, an den Betreiber wenden. |
| „⚠️ Nur teilweise importiert – … Von … Produkten wurden die ersten … verarbeitet (… neu), der Rest nicht – einfach noch einmal importieren, Doppelte werden erkannt.“ | Nur bei großen Mengen (mehr als 200 Produkte auf einmal, meist bei „Ganzer Shop“): Mitten im Import brach die Verbindung ab. Am Anfang der Meldung steht der Grund, z. B. dass der Server nicht erreichbar war, „Sitzung abgelaufen – bitte im Dashboard neu anmelden.“, „Abo gesperrt – bitte im Dashboard nachsehen.“ oder „Zugang abgeschaltet – bitte beim Betreiber melden.“. Ein Teil ist gespeichert. Grund beheben (z. B. neu anmelden) und einfach noch einmal klicken; was schon drin ist, wird als „schon in DB“ übersprungen. |
| „❌ Nichts importiert: … lehnt die Anfrage ab (HTTP …) – bitte die Extension aktualisieren oder beim Betreiber melden. …“ | Der Server nimmt die Anfrage nicht an. Extension aktualisieren (update.bat, danach Chrome komplett neu starten). Hilft das nicht, an den Betreiber wenden. |
| „❌ Nichts importiert: …“ mit einem anderen Text | Ein unerwarteter Fehler; es wurde nichts gespeichert. Amazon-Seite neu laden und noch einmal klicken. Bleibt es, den Text dem Betreiber schicken. |
| „… Hintergrunddienst antwortet nicht, neuer Versuch (1/2) …“ | Die Extension war kurz „eingeschlafen“; sie versucht es automatisch noch zweimal. Doppelte Produkte entstehen dabei nicht. |
| „❌ Fehler: keine Antwort vom Hintergrunddienst … – Extension in diesem Browser aktualisieren/neu laden?“ | Die Extension antwortet nicht. Amazon-Seite neu laden (F5). Hilft das nicht: unter `chrome://extensions` bei Cash Lister auf „Neu laden“ klicken bzw. Chrome komplett neu starten und es erneut versuchen. |

### 3.6 Häufige Fragen (Suchseiten)

**Warum zählt der Knopf weniger Produkte, als ich auf der Seite sehe?**
Gesponserte Kacheln und Kacheln, die an einem Filter scheitern, werden nicht mitgezählt. Fahre mit der Maus über den Knopf – dort steht, welcher Filter wie viele ausschließt.

**Werden alle Ergebnisseiten auf einmal übernommen?**
Bei einer normalen Suche nein – nur die Seite, die du gerade siehst. Blättere weiter und klicke erneut. Nur im Verkäufer-Schaufenster gibt es „📚 Ganzer Shop → Datenbank“ (Abschnitt 5).

**Werden Varianten (Farben, Größen) alle übernommen?**
Nein. Pro Kachel wird genau eine ASIN übernommen – die, die Amazon in der Kachel zeigt.

**Prüft der Knopf, ob das Produkt per FBA versendet wird?**
Nein. Ohne den Schalter „nur Verkauf durch Amazon“ wird beim Einsammeln nicht geprüft, wer verkauft oder versendet. Ob Amazon versendet, prüft der Browser-Lister beim Listen (Einstellungen → Reiter „Produkt-Filter“ → Karte „Beim Listen“ → „Nur FBA“). Wenn du nur Produkte willst, die Amazon selbst verkauft, nutze den Schalter aus Abschnitt 4.

**Muss ich die Produkt-Datenbank offen haben?**
Nein. Der Knopf legt die Produkte direkt in die Datenbank. Eine offene Datenbank-Seite holt den neuen Stand, sobald du wieder in ihren Tab wechselst; sonst einmal neu laden (F5).

**Ich habe auf amazon.com eingesammelt – werden die Produkte jetzt von amazon.com gelistet?**
Nicht automatisch. Gespeichert wird nur die ASIN; geöffnet wird das Amazon-Land deiner Einstellung „Domain“ (Abschnitt 7).

**Werden Produkte, die ich schon gelistet habe, nochmal importiert?**
Nicht, wenn sie in deinen hinterlegten Google Sheets stehen (Abschnitt 11) oder mit deinem Konto schon erfolgreich gelistet wurden (dann „bereits gelistet“). Außerdem prüft der Browser-Lister beim Listen, ob die ASIN in **diesem Chrome-Profil** schon einmal erfolgreich mit Cash Lister gelistet wurde („Produkt ist schon gelistet (Duplikat)“).

### 3.7 Probleme und Lösungen (Suchseiten)

| Problem | Lösung |
|---|---|
| Der blaue Knopf erscheint nicht. | Prüfe, ob du wirklich auf einer Suchergebnisseite (Suchbegriff eingegeben) oder im Verkäufer-Schaufenster bist. Auf Kategorie-Seiten ohne Suchbegriff und in Marken-Shops gibt es den Knopf nicht. Seite neu laden. Prüfe unter `chrome://extensions`, ob „Cash Lister“ eingeschaltet ist. |
| Der Knopf zeigt „0 Produkte“. | Meist schließen deine Filter alles aus (Hinweis beim Darüberfahren). Prüfe in den Einstellungen (Reiter „Produkt-Filter“, Karte „Amazon-Filter“) vor allem „Preis bis“ und „Max. verlängerte Lieferzeit“. |
| Nach dem Import steht „0 neu in der Datenbank“. | Die Meldung sagt, warum: schon in der Datenbank, schon gelistet oder von anderen Kunden belegt. |
| Viele Produkte „von anderen Kunden belegt“. | Diese Produkte bearbeitet bereits ein anderer Kunde. Das ist gewollt (Abschnitt 13). Such dir andere Produkte. |
| „❌ Bitte zuerst in Cash Lister anmelden – nichts importiert.“, obwohl ich angemeldet bin. | Die Anmeldung kann abgelaufen sein. Dashboard öffnen (Klick auf das Cash-Lister-Symbol) und schauen, ob du dort angemeldet bist; ggf. neu anmelden. Unten in der Seitenleiste steht, ob die Verbindung steht („Server verbunden“) oder ob z. B. „Abo gesperrt“ oder „Zugang abgeschaltet“ da steht. |
| „❌ Nichts importiert – Server nicht erreichbar …“ | Später noch einmal klicken. Die Seitenleiste zeigt unten „Server nicht erreicht“, solange der Ausfall dauert. Dauert er lange, an den Betreiber wenden. |
| Nach einem Update der Extension meldet der Knopf „❌ Fehler: keine Antwort vom Hintergrunddienst …“ oder reagiert nicht mehr richtig. | Die Amazon-Seite neu laden (F5). Seiten, die vor einem Update geöffnet wurden, können nicht mehr mit der Extension sprechen. Nach jedem Update Chrome komplett neu starten oder unter `chrome://extensions` bei Cash Lister „Neu laden“ klicken. |

---

## 4. Schalter nur Verkauf durch Amazon

### 4.1 Was macht der Schalter?

Mit dem Schalter „nur Verkauf durch Amazon“ übernimmt der Knopf auf Suchseiten **nur Produkte, die Amazon selbst verkauft** („Verkauf und Versand durch Amazon“). Wer verkauft, steht nicht auf der Suchseite, sondern nur in der Buybox der Produktseite. Deshalb öffnet Cash Lister jede angehakte Produktseite kurz in einem eigenen Tab, liest den Buybox-Verkäufer und schließt den Tab wieder.

- Produkte, bei denen ein **anderer Händler** in der Buybox steht, werden aussortiert – **auch wenn Amazon für ihn versendet (FBA)**.
- Gebrauchtware von „Amazon Retourenkauf“ zählt **nicht** als Amazon.
- Produkte **ohne Angebot in der Buybox** (nicht lieferbar) werden aussortiert („kein Angebot“). Dasselbe gilt, wenn Amazon für das Produkt „Seite nicht gefunden“ meldet.

### 4.2 Wo ist der Schalter?

Es gibt ihn an zwei Stellen – beide sind **dieselbe Einstellung**:

1. Auf Amazon-**Suchseiten** direkt über dem blauen Knopf: Kästchen „nur Verkauf durch Amazon“.
2. In den Einstellungen, Reiter „Produkt-Filter“, Karte „Amazon-Filter“, ganz unten: Schalter „Nur Verkauf durch Amazon“ (darunter klein: „Produkt-Grabber: übernimmt nur Produkte, die Amazon selbst verkauft und versendet“).

Standard: **aus**. Der Schalter gilt nur auf **normalen Suchseiten**, nicht im Verkäufer-Schaufenster (dort ist der Verkäufer ja gerade der Händler) und nicht bei „📚 Ganzer Shop → Datenbank“. Während eine Prüfung läuft, ist der Schalter gesperrt.

### 4.3 Wie viele Tabs gleichzeitig?

So viele, wie im **Tracker** im Feld „Gleichzeitig“ steht (erlaubt 1 bis 10, Standard 5). Den Tracker öffnest du über die Seitenleiste → „Tracker“. Mehr Tabs = schneller, aber Amazon zeigt dann eher ein Captcha.

Die Prüf-Tabs öffnen sich **im Hintergrund direkt neben der Suchseite** und schließen sich von selbst. Sie laden nur den Text der Seite ohne Bilder (deshalb sehen sie leer bzw. kaputt aus – das ist normal).

### 4.4 Schritt für Schritt

1. Im Dashboard angemeldet sein (sonst wird nach der Prüfung nichts importiert).
2. Amazon-Suche öffnen (z. B. nach einer Marke).
3. Über dem blauen Knopf das Kästchen „nur Verkauf durch Amazon“ anhaken.
4. Der Knopf zeigt jetzt z. B. „📦 48 Produkte · nur Verkauf durch Amazon (wird geprüft) → Datenbank“. Sind schon einige Produkte geprüft (z. B. nach einem Abbruch), steht dort stattdessen der Zwischenstand, z. B. „📦 48 Produkte · 7× Amazon, 5× andere, 36 noch offen → Datenbank“.
5. Unpassende Produkte abwählen (abgewählte werden gar nicht erst geprüft).
6. Auf den Knopf klicken. Es erscheint z. B.: „Prüfe den Verkäufer von 48 Produkten in 5 Tabs gleichzeitig (ca. 35 s). Nochmal klicken = abbrechen.“
7. Während der Prüfung zeigt der Knopf den Fortschritt, z. B. „⏳ Verkäufer 12/48 · 7× Amazon · 5 Tabs – Klick = abbrechen“. Die Pillen auf den Kacheln wechseln auf „Amazon ✓“, „nicht Amazon“ oder „kein Angebot“.
8. Ist alles geprüft, werden **nur die „Amazon ✓“-Produkte** importiert. Die Meldung nennt zusätzlich die aussortierten Händler, z. B. „… · 5 andere Verkäufer aussortiert (Philips Home Appliances ×3, ohne Angebot ×2)“.

Gut zu wissen:

- **Abbrechen:** Während der Prüfung nochmal auf den Knopf klicken. Es erscheint „Prüfung abgebrochen. … von … sind geprüft und bleiben gemerkt; ein weiterer Klick prüft nur den Rest. Importiert wurde noch nichts.“
- **Ergebnisse bleiben gemerkt**, solange die Amazon-Seite offen ist – auch beim Weiterblättern. Ein neuer Klick prüft nur, was noch fehlt. Lädst du die Seite neu, ist das Gemerkte weg.
- Was du **während** der Prüfung abwählst, wird nicht importiert, auch wenn es „Amazon ✓“ bekommen hat.
- Ein Doppelklick zählt als ein Klick (damit du nicht aus Versehen gleich wieder abbrichst).
- Schließt du die Amazon-Suchseite, werden ihre offenen Prüf-Tabs ebenfalls geschlossen.
- Die Prüfung dauert grob gut 3 Sekunden pro Produkt und Tab; Cash Lister schätzt die Dauer vorher selbst und zeigt sie an.
- Der Import danach läuft genauso wie ohne Schalter – mit denselben Meldungen (Abschnitt 3.5), auch bei fehlender Anmeldung oder Server-Ausfall.

### 4.5 Meldungen der Prüfung

| Meldung | Bedeutung / was tun |
|---|---|
| „Für amazon.xx ist die Händler-ID von Amazon nicht hinterlegt – „nur Verkauf durch Amazon“ geht hier nicht. Den Schalter ausschalten.“ | Die Prüfung gibt es nur für amazon.de, .com, .co.uk, .fr, .it, .es, .nl, .ca, .co.jp und .com.au. Auf amazon.in, .com.br und .com.mx den Schalter ausschalten. |
| „⛔ Amazon zeigt ein Captcha – Prüfung angehalten. Der Tab mit dem Captcha ist vorne: dort lösen, dann hier nochmal klicken.“ | Amazon will prüfen, ob ein Mensch surft. Im nach vorne geholten Tab das Captcha lösen, zurück zur Suchseite, nochmal klicken. Bereits Geprüftes bleibt gemerkt. |
| „⛔ Amazon zeigt ein Captcha bzw. eine Sperrseite – Prüfung angehalten. Eine Amazon-Produktseite öffnen, das Captcha lösen und nochmal klicken.“ | Wie oben, aber es blieb kein Captcha-Tab offen. Selbst irgendeine Amazon-Produktseite öffnen, Captcha lösen, dann nochmal klicken. Eventuell im Tracker bei „Gleichzeitig“ eine kleinere Zahl einstellen. |
| „⛔ Mehrere Produktseiten nicht abrufbar (<Grund>) – Prüfung angehalten.“ | Dreimal hintereinander ging eine Produktseite nicht. Mögliche Gründe in Klammern: „Preis nicht verfügbar – Amazon bremst vermutlich“, „keine Produktseite erhalten“, „Produktseite in 45 s nicht geladen“, „Produktseite laedt nicht (Chrome-Fehlerseite)“, „Pruef-Tab wurde geschlossen“, „keine Antwort in 60 s“, „Hintergrunddienst antwortet nicht“, „Tab liess sich nicht oeffnen (…)“, „Produktseite liess sich nicht aufrufen (…)“, „HTTP …“. Kurz warten, Internetverbindung prüfen, im Tracker eine kleinere Zahl bei „Gleichzeitig“ einstellen, Prüf-Tabs nicht von Hand schließen, dann nochmal klicken. |
| „… Extension wurde neu geladen – Amazon-Seite neu laden“ (als Grund) | Die Extension wurde aktualisiert oder neu geladen, während die Seite offen war. Amazon-Seite neu laden (F5). |
| „Alle Produkte wurden während der Prüfung abgewählt – nichts importiert.“ | Du hast während der Prüfung alles abgewählt. |
| „Keins der … Produkte wird von Amazon verkauft (…) – nichts importiert.“ / „Das Produkt wird nicht von Amazon verkauft …“ | Kein einziger Treffer. In Klammern stehen die häufigsten anderen Verkäufer. |
| Zusatz „· … nicht prüfbar“ | So viele Produkte konnten nicht geprüft werden; sie werden nicht importiert. |

### 4.6 Häufige Fragen (nur Verkauf durch Amazon)

**Was ist der Unterschied zu „Nur FBA“ in den Einstellungen?**
„nur Verkauf durch Amazon“ wirkt **beim Einsammeln** auf Suchseiten und verlangt, dass **Amazon selbst** der Verkäufer ist. „Nur FBA“ (Reiter „Produkt-Filter“, Karte „Beim Listen“, Standard an) wirkt **beim Listen** im Browser-Lister und verlangt nur, dass **Amazon versendet** – der Verkäufer darf ein anderer Händler sein.

**Warum öffnen sich plötzlich viele Tabs?**
Das ist die Prüfung. Die Tabs schließen sich von selbst. Bitte nicht von Hand schließen.

**Warum sehen die Prüf-Tabs leer oder kaputt aus?**
Sie laden absichtlich nur den Seitentext ohne Bilder und Gestaltung. Das ist schneller und reicht für die Prüfung.

**Kann ich die Anzahl der Tabs ändern?**
Ja, im Tracker im Feld „Gleichzeitig“ (1 bis 10). Die Änderung wirkt sofort, auch auf schon offenen Amazon-Seiten.

### 4.7 Probleme und Lösungen (nur Verkauf durch Amazon)

| Problem | Lösung |
|---|---|
| Ständig Captchas. | Im Tracker bei „Gleichzeitig“ eine kleinere Zahl einstellen (z. B. 2 oder 3), Captcha lösen, erneut klicken. |
| Das Kästchen lässt sich nicht anklicken. | Während einer laufenden Prüfung ist es gesperrt. Prüfung abwarten oder mit Klick auf den Knopf abbrechen. |
| Das Kästchen ist gar nicht da. | Es erscheint nur auf normalen Suchseiten (mit Suchbegriff), nicht im Verkäufer-Schaufenster. |
| Ein Produkt, das laut Amazon „Versand durch Amazon“ hat, wurde als „nicht Amazon“ aussortiert. | Richtig so: Der Schalter verlangt, dass Amazon **verkauft**. FBA eines anderen Händlers reicht nicht. Willst du auch FBA-Produkte anderer Händler, Schalter ausschalten und beim Listen „Nur FBA“ nutzen. |
| Nach langer Prüfung kam „❌ Bitte zuerst in Cash Lister anmelden – nichts importiert.“ | Die Prüfung lief, aber importieren ging ohne Anmeldung nicht. Im Dashboard anmelden und nochmal klicken – die Prüfergebnisse sind gemerkt, solange die Seite offen ist, es wird also nicht alles neu geprüft. |

---

## 5. Verkäufer-Schaufenster und Ganzer Shop

### 5.1 Was ist das Verkäufer-Schaufenster?

Das ist die Amazon-Suchseite mit **allen Produkten eines bestimmten Händlers**. Du erkennst sie daran, dass in der Adresse `me=` steht. Auf dieser Seite gibt es über dem blauen Knopf den weißen Knopf „📚 Ganzer Shop → Datenbank“.

**Nicht sicher belegt:** wie der Link zu dieser Seite auf Amazons Händlerprofil genau beschriftet ist (Amazon ändert das gelegentlich). Typischerweise gelangst du über das Händlerprofil (Klick auf den Verkäufernamen in der Buybox) zu einer Liste seiner Produkte.

### 5.2 Normaler Knopf und Ganzer Shop im Vergleich

- Der **blaue Knopf** übernimmt nur die gerade sichtbare Seite (wie bei der Suche, mit Häkchen und Filtern).
- **„📚 Ganzer Shop → Datenbank“** holt zusätzlich alle weiteren Seiten des Schaufensters im Hintergrund nach (ohne neue Tabs) und wendet **dieselben Filter** an. Häkchen, die du auf der sichtbaren Seite entfernt hast, werden berücksichtigt. Auf den nachgeladenen Seiten kannst du nichts abwählen.
- Höchstens **30 Seiten** pro Klick; zwischen den Seiten wartet Cash Lister kurz, um Amazon nicht zu überlasten. Er hört früher auf, wenn alle Treffer des Shops gesehen sind oder es keine weitere Seite gibt.
- **Wichtig – auf Seite 1 starten:** Der Knopf nimmt die Seite, die du gerade siehst, und lädt dann die Seiten 2 bis 30 nach. Bist du gerade auf einer späteren Seite (z. B. Seite 3), fehlt Seite 1 im Ergebnis. Bist du auf der letzten Seite, wird nur diese eine übernommen.
- Der Schalter „nur Verkauf durch Amazon“ gilt hier **nicht**.
- Auch hier gilt: vorher im Dashboard anmelden, sonst wird am Ende nichts importiert.

### 5.3 Schritt für Schritt: einen ganzen Amazon-Shop übernehmen

1. Im Dashboard angemeldet sein.
2. Öffne das Schaufenster des Händlers (Adresse enthält `me=`) und bleib auf der **ersten** Ergebnisseite.
3. Prüfe die erste Seite und entferne bei Bedarf Häkchen.
4. Klicke auf „📚 Ganzer Shop → Datenbank“.
5. Der Knopf zeigt den Fortschritt, z. B. „⏳ Seite 3 … (41 Produkte)“, danach „⏳ Importiere 95 …“. Bei mehr als 200 Produkten steht im Meldungsfeld zusätzlich „Importiere … Produkte – bei so vielen dauert das etwas …“.
6. Ergebnis, z. B.: „✅ Ganzer Shop: 6 Seite(n), 96 Kacheln geprüft von 96 · 80 neu in der Datenbank · 10 schon drin · 3 bereits gelistet · 2 von anderen Kunden belegt.“

Die Zahlen bedeuten dasselbe wie in Abschnitt 3.4 („schon drin“ = „schon in DB“).

### 5.4 Meldungen von Ganzer Shop

| Meldung | Bedeutung / was tun |
|---|---|
| „Seite … : HTTP … – Abbruch, bisher Gefundenes wird übernommen.“ | Amazon hat eine Seite nicht geliefert (oft wegen zu vieler Anfragen). Alles bis dahin Gefundene wird trotzdem importiert. Später erneut versuchen – doppelte Produkte werden übersprungen. |
| „Abbruch beim Blättern: …“ | Unerwarteter Fehler beim Nachladen. Seite neu laden, erneut versuchen. |
| „Nichts gefunden – alle Kacheln von den Filtern ausgeschlossen?“ | Kein einziges Produkt hat die Filter bestanden. Filter in den Einstellungen prüfen (Abschnitt 6). |
| „❌ Bitte zuerst in Cash Lister anmelden – nichts importiert.“ / „❌ Nichts importiert – Server nicht erreichbar …“ / „⚠️ Nur teilweise importiert – …“ / „❌ Nichts importiert: …“ | Wie in Abschnitt 3.5. Bei „Nur teilweise importiert“ einfach noch einmal auf „📚 Ganzer Shop → Datenbank“ klicken – schon Gespeichertes wird als „schon drin“ übersprungen. |
| „❌ Fehler: …“ | Die Extension hat nicht richtig geantwortet. Amazon-Seite neu laden und erneut versuchen (siehe Abschnitt 3.5). |

### 5.5 Häufige Fragen (Schaufenster)

**Warum gibt es Ganzer Shop nicht bei der normalen Suche?**
Nur im Schaufenster ist die Gesamtmenge bekannt und begrenzt. Bei einer normalen Suche blätterst du selbst und klickst pro Seite.

**Hat der Shop mehr als 30 Seiten – was dann?**
Nach 30 Seiten hört der Knopf auf. Einen Weg, mit „Ganzer Shop“ ab Seite 31 weiterzumachen, gibt es nicht: Auch wenn du auf Seite 31 klickst, lädt der Knopf danach wieder die Seiten 2 bis 30. Für die Seiten ab 31 blätterst du auf Amazon selbst weiter und benutzt auf jeder Seite den blauen Knopf (er nimmt nur die sichtbare Seite). Schon vorhandene Produkte werden dabei automatisch übersprungen.

**Ich war beim Klick nicht auf Seite 1 – was nun?**
Geh im Schaufenster auf Seite 1 und klick dort den blauen Knopf. Doppelte Produkte werden übersprungen, es entsteht also nichts doppelt.

---

## 6. Die Amazon-Filter in den Einstellungen

Die Filter stehen in den **Einstellungen** (Seitenleiste → „Einstellungen“, oder Rechtsklick auf das Cash-Lister-Symbol → „Optionen“), Reiter **„Produkt-Filter“**, Karte **„Amazon-Filter“** (Hinweis daneben: „jeder Filter hat seinen eigenen Schalter“). Jeder Filter hat einen **eigenen Schalter** rechts neben dem Zahlenfeld: Nur wenn der Schalter an ist, wirkt die Zahl. Ist er aus, ist das Zahlenfeld ausgegraut. Ein Schalter wird beim Anklicken gespeichert, eine Zahl, sobald du das Feld verlässt. Der Knopf „Speichern“ ganz unten speichert nichts zusätzlich, er zeigt nur „Einstellungen gespeichert“ an. Offene Amazon-Suchseiten übernehmen Änderungen sofort.

| Einstellung | Was sie beim Einsammeln auf Suchseiten macht | Wirkt außerdem … | Hinweise |
|---|---|---|---|
| „Max. verlängerte Lieferzeit“ (in Tagen) | Überspringt Kacheln, deren **normale** (kostenlose) Lieferung länger dauert als so viele Tage. Bei einem Zeitraum zählt das spätere Datum. Die „schnellste Lieferung“ (meist gegen Aufpreis) wird ignoriert. | auf Produktseiten (Warnung im Tab-Titel) und beim Listen | Vorgabe 20; der Schalter ist dann in der Regel an. **Achtung:** Der Schalter wirkt nur auf das Einsammeln auf Suchseiten. Die Warnung auf der Produktseite und die Prüfung beim Listen richten sich immer nach der eingetragenen Zahl – auch wenn der Schalter aus ist. |
| „Mind. Sterne“ (0 bis 5) | Überspringt Kacheln mit weniger Sternen. | nur beim Einsammeln auf Suchseiten | Produkte **ohne** Bewertung werden nicht ausgeschlossen. |
| „Mind. Bewertungen“ | Überspringt Kacheln mit weniger Bewertungen (Anzahl). | nur beim Einsammeln auf Suchseiten | Produkte ganz **ohne** Bewertungen zählen als 0 und fallen deshalb heraus. |
| „Mind. Lagerbestand“ (höchstens 20) | Überspringt Kacheln mit „Nur noch N auf Lager“, wenn N kleiner ist. | nur beim Einsammeln auf Suchseiten | Amazon zeigt den Hinweis nur bei knappem Bestand; ohne Hinweis gilt das Produkt als ausreichend vorrätig. Höher als 20 geht nicht – eine größere Zahl wird auf 20 zurückgesetzt. |
| „Preis ab“ (in €) | Überspringt Kacheln mit niedrigerem Amazon-Preis. | beim Listen („Amazon-Preis zu niedrig (Filter „Preis ab“)“) | Durchgestrichene Preise werden ignoriert. Ohne lesbaren Preis wird nicht gefiltert. |
| „Preis bis“ (in €) | Überspringt Kacheln mit höherem Amazon-Preis. | beim Listen („Amazon-Preis zu hoch (Filter „Preis bis“)“) | Siehe Hinweis unten. |
| „Nur Verkauf durch Amazon“ | Siehe Abschnitt 4. | – | Standard aus. |

Wichtige Zusammenhänge:

- **Sterne, Bewertungen und Lagerbestand werden nur auf Amazon-Suchseiten geprüft.** Produkte, die du von Hand in die Produkt-Datenbank einfügst, und Funde des Konkurrenz-Scanners werden danach **nicht** gefiltert.
- **Lieferzeit und Preis werden beim Einsammeln nur geprüft, wenn sie auf der Kachel lesbar sind.** Steht dort kein Datum oder Preis, wird das Produkt nicht ausgeschlossen. Beim Listen wird ohnehin noch einmal geprüft.
- **„Preis ab“ und „Preis bis“ gibt es nur noch hier.** Im Reiter „Preise & Listing“ steht dazu nur der Hinweis „„Preis ab“ und „Preis bis“ stehen unter Produkt-Filter → Amazon-Filter.“ Ob sie wirken, entscheidet der Schalter.
- **Schalter noch nie angefasst:** Steht eine Zahl größer als 0 im Feld und wurde der Schalter noch **nie** gesetzt (z. B. weil du die Einstellungsseite seit dem Update noch nie geöffnet hast), behandelt Cash Lister den Filter als **eingeschaltet**. Beim ersten Öffnen der Einstellungsseite wird der Schalter dann passend dazu gesetzt. Wer mit einer älteren Version gearbeitet hat (das frühere kleine Fenster am Cash-Lister-Symbol trug dort beim ersten Öffnen 100 ein), hat deshalb oft noch eine aktive Obergrenze „Preis bis“ = 100. Fehlen dir teure Produkte, ist das meist der Grund.
  **Nicht sicher belegt:** was bei dir genau eingestellt ist – das hängt auch von einer eventuell vom Betreiber geschickten Einstellungsdatei oder einer zurückgeholten Sicherung ab. Schau in den Einstellungen bei „Preis bis“ nach.
- Die Preisgrenze ist eine reine Zahl in der Währung der jeweiligen Amazon-Seite (auf amazon.com also Dollar), auch wenn „€“ dabeisteht.
- **Sicherung und Rechnerwechsel:** Die Schalter der Filter sowie die Werte für „Mind. Sterne“, „Mind. Bewertungen“ und „Mind. Lagerbestand“ werden beim „Einstellungen exportieren“ und bei der Sicherung auf dem Server **nicht** mitgenommen. Mitgenommen werden die Zahlen für „Max. verlängerte Lieferzeit“, „Preis ab“ und „Preis bis“ sowie der Schalter „Nur Verkauf durch Amazon“. Auf einem neu eingerichteten Rechner fehlen dann die Schalter, und es gilt die Regel von oben: Steht eine Zahl drin, ist der Filter eingeschaltet – auch wenn du ihn auf dem alten Rechner ausgeschaltet hattest. Sterne, Bewertungen und Lagerbestand musst du dort neu eintragen. Nach einem Umzug auf einen anderen Rechner deshalb einmal die Karte „Amazon-Filter“ kontrollieren und die Schalter richtig setzen.

---

## 7. Die Einstellung Domain und das Amazon-Land deiner Produkte

Die Einstellung steht in den Einstellungen, Reiter **„Preise & Listing“**, Karte **„Listing“**, Feld **„Domain“** (darunter klein: „eBay-Seite, z. B. DE = ebay.de“). Auswahl: „Keine“, „USA“, „CA“, „UK“, „AU“, „DE“, „FR“, „IT“, „ES“, „NL“.

Sie legt nicht nur die eBay-Seite fest, sondern in diesem Bereich auch das **Amazon-Land**:

| Wo | Was „Domain“ dort bestimmt | Bei „Keine“ |
|---|---|---|
| Produkt-Datenbank (Tabelle, „Als TXT exportieren“) und das Listen aus der Produkt-Datenbank | Jedes Produkt wird als `https://www.amazon.<Domain>/dp/<ASIN>` angezeigt, exportiert und vom Browser-Lister geöffnet. Bei „DE“ also amazon.de. | amazon.de |
| eBay-Suchknopf am Titel einer Amazon-Produktseite (Abschnitt 8.1) | Auf welcher eBay-Seite gesucht wird (ebay.de, ebay.com …). | Die Suche funktioniert nicht (kaputte Adresse). |
| Violette Lupe auf eBay-Artikelseiten (Abschnitt 14) | Welches Amazon-Land geöffnet wird. | amazon.de |
| Prüfung „Nur chinesische Verkäufer“ beim Listen (Abschnitt 9) | Auf welchem Amazon-Land das Händlerprofil geöffnet wird. | Die Adresse des Händlerprofils ist dann ungültig, die Prüfung bekommt keine Antwort. Nach etwa 30 Sekunden Warten wird das Produkt deshalb als „Kein chinesischer Verkäufer“ übersprungen – auch wenn der Händler aus China kommt. Also ein Land wählen. |

Wichtig:

- **Die Produkt-Datenbank merkt sich kein Amazon-Land pro Produkt.** Gespeichert wird nur die ASIN. Ein Link von amazon.co.uk, den du einfügst, wird bei „Domain“ = „DE“ als amazon.de-Produkt angezeigt und gelistet. Gibt es die ASIN auf diesem Amazon-Land nicht, scheitert das Listen später mit „Produktseite existiert nicht“.
- Änderst du „Domain“, ändern sich auf **diesem Gerät sofort alle** Links in der Produkt-Datenbank (du musst nichts neu einfügen). Deine anderen Geräte benutzen weiter ihre eigene „Domain“-Einstellung. Stell „Domain“ deshalb auf allen deinen Geräten gleich ein.
- **„Keine“ nicht wählen.** Nach einer Neuinstallation, nach einem Update der Extension (auch nach „Neu laden“ unter `chrome://extensions`) und nach einem Update von Chrome trägt Cash Lister von selbst wieder ein Land ein, normalerweise „DE“, wenn bei „Domain“ nichts bzw. „Keine“ steht. Kontrolliere „Domain“ deshalb nach einer Neuinstallation (und schadet nicht: nach einem Update). Steht dort z. B. „USA“, obwohl du auf amazon.de/ebay.de arbeitest, öffnet der Browser-Lister amazon.com.

---

## 8. Amazon-Produktseiten (Adresse mit /dp/)

Auf Amazon-Produktseiten blendet Cash Lister **keinen eigenen Bereich und keine Listen-Knöpfe** ein. Du siehst nur zwei Dinge (Abschnitte 8.1 und 8.2).

Außerdem entfernt Cash Lister beim Öffnen einer Produktseite einen Teil der erweiterten Herstellerbeschreibung: Von den bebilderten Blöcken weiter unten auf der Seite (bei Amazon „A+-Inhalte“, z. B. „Aus der Herstellerbeschreibung“) bleibt nur der erste stehen. Wenn dir auf einer Produktseite solche Blöcke fehlen, liegt das an Cash Lister, nicht an Amazon. **Nicht sicher belegt:** ob Amazon diese Blöcke derzeit überall so aufbaut, dass das bei jedem Produkt greift.

### 8.1 Der eBay-Suchknopf am Produkttitel

Direkt **hinter dem Produkttitel** steht ein kleines Symbol: eine **hellviolette Einkaufstasche mit Lupe**. Beim Darüberfahren steht dort „Diesen Artikel bei eBay suchen“.

Ein Klick öffnet in einem neuen Tab (im Vordergrund) eine **eBay-Suche nach dem Produkttitel** (auf höchstens 80 Zeichen gekürzt, an einer Wortgrenze), gefiltert auf neue Artikel mit kostenlosem Versand. So siehst du schnell, ob und zu welchem Preis das Produkt schon auf eBay angeboten wird.

Welche eBay-Seite (ebay.de, ebay.com …) benutzt wird, richtet sich nach der Einstellung „Domain“ (Abschnitt 7). Steht dort „Keine“, funktioniert die Suche nicht – stelle dein Land ein (z. B. „DE“).

### 8.2 Warnungen im Tab-Titel

Beim Öffnen einer Produktseite prüft Cash Lister einige Punkte und schreibt Warnungen **vorne in den Titel des Browser-Tabs**. Bei den meisten wechselt außerdem das kleine Tab-Symbol auf ein **gelbes Warndreieck mit Ausrufezeichen**, bei Blacklist-Treffern auf einen **Totenkopf**. Mehrere Warnungen können hintereinander stehen.

Diese Warnungen sind **nur Hinweise**. Beim bloßen Ansehen passiert nichts – auf der Produktseite gibt es auch keinen Knopf, mit dem man etwas bestätigen müsste. Der Zusatz „ZUM LISTEN BESTÄTIGEN“ ist dabei nur Teil des Textes.

| Text im Tab-Titel | Tab-Symbol | Bedeutung |
|---|---|---|
| „WARNUNG! NICHT AUF LAGER - ZUM LISTEN BESTÄTIGEN -“ | Warndreieck | Die Verfügbarkeitsangabe passt nicht zu den bekannten „auf Lager“-Texten – oder die Lieferzeit ist zu lang (zu lange Lieferzeit zählt für Cash Lister wie „nicht auf Lager“). |
| „WARNUNG! LIEFERZEIT VERLÄNGERT - ZUM LISTEN BESTÄTIGEN -“ | Warndreieck | Auf der Seite steht „Extended delivery time“ oder das Lieferdatum liegt weiter entfernt als die Zahl bei „Max. verlängerte Lieferzeit“ (Vorgabe 20 Tage). |
| „WARNUNG! KEIN KOSTENLOSER VERSAND - ZUM LISTEN BESTÄTIGEN -“ | Warndreieck | Im Kaufkasten wurde kein Hinweis auf kostenlose Lieferung gefunden (z. B. „GRATIS Lieferung“, „free delivery“). Als in Ordnung gilt auch, wenn dort „für 3,99“ steht. |
| „WARNUNG! GEBRAUCHT - ZUM LISTEN BESTÄTIGEN -“ | Warndreieck | Amazon zeigt als Hauptangebot ein Gebraucht-Angebot. |
| „WARNUNG! MINDESTBESTELLMENGE <Zahl> - ZUM LISTEN BESTÄTIGEN -“ | Warndreieck | Amazon verlangt eine Mindestbestellmenge größer als 1. Erkannt wird nur der englische Hinweis „Minimum order quantity“. **Nicht sicher belegt:** ob amazon.de diesen Hinweis auf Deutsch zeigt – dann erkennt Cash Lister ihn nicht. |
| „WARNUNG! ASIN PASST NICHT ZUR ADRESSE - ZUM LISTEN BESTÄTIGEN -“ | Warndreieck | Die ASIN der angezeigten Seite steht nicht in der Adresse (z. B. weil Amazon auf eine andere Variante umgeleitet hat). |
| „WARNUNG! KEIN PRIME - ZUM LISTEN BESTÄTIGEN -“ | unverändert | Grober Hinweis, dass kein Amazon-Versand erkannt wurde. Verlass dich nicht darauf – verbindlich ist die Versand-Prüfung beim Listen („Nur FBA“). |
| „WARNUNG! INTERNATIONALER VERSAND - ZUM LISTEN BESTÄTIGEN -“ | unverändert | Amazon zeigt bei der Lieferung „free international delivery“ (kommt praktisch nur auf englischsprachigen Amazon-Seiten vor). |
| „⚠️ BLACKLIST-WORT GEFUNDEN: <WORT> - <wort>“ | Totenkopf | Ein Eintrag aus deiner Blacklist steht im Titel, in der Beschreibung, in den Stichpunkten oder in den Werten der Produktmerkmale. Der ursprüngliche Seitentitel wird dabei durch das gefundene Wort ersetzt; Warnungen, die schon vorher im Tab-Titel standen, können dabei verschwinden. |

Zur Blacklist: Du pflegst sie in den Einstellungen, Reiter „Produkt-Filter“, Karte „Blacklist“, Feld „Meine Liste“ – ein Wort oder eine Wortgruppe pro Zeile (Platzhaltertext: „Ein Wort oder Begriff je Zeile“); darunter steht „Wörter: <Anzahl>“. Die Liste speichert sich beim Tippen von selbst (doppelte Einträge werden zusammengefasst, alles wird kleingeschrieben gespeichert). Verglichen werden ganze Wörter, Groß- und Kleinschreibung egal. Bei Merkmalen werden nur die Werte geprüft, nicht die Bezeichnungen.

### 8.3 Während eines Browser-Lister-Laufs

Wenn der Browser-Lister läuft, öffnet er Amazon-Produktseiten selbst. In diesen Tabs siehst du Fortschrittstexte im Tab-Titel, z. B. „Auto-Listing - <ASIN>“, „Hole GPSR-Angaben...“, „GPSR-Angaben erhalten!“, „Prüfe chinesischen Verkäufer...“, „Auto-Listing - KI-Titel wird erstellt...- <ASIN>  KI-Titel wird erstellt...“, „Auto-Listing - <ASIN>  Erstelle Bild...“ und am Ende „Wird bei eBay gelistet: <Titel> - <ASIN>  ...“. Das Tab-Symbol ist dabei animiert. Während die GPSR-Angaben geholt werden, können kurz Zwischentexte im Tab-Titel stehen (z. B. „GPSR 2: Sicherheitskontakte geöffnet, warte auf die Herstellerangaben“, „GPSR: Versuch 6, die Sicherheitskontakte zu öffnen“, „GPSR: Hersteller und EU-Verantwortlicher gelesen“) – das ist normal.

Erscheint in so einem Tab eine Warnung, wird das Produkt in diesem Lauf **übersprungen** und als fehlgeschlagen gezählt. Den Grund findest du im „Statusbericht“ des Browser-Listers (Spalte „Meldung“):

| Tab-Titel im Lauf | Meldung im Statusbericht |
|---|---|
| „WARNUNG! SEITE EXISTIERT NICHT“ | „Produktseite existiert nicht“ |
| „WARNUNG! SCHON GELISTET (DUPLIKAT) - ZUM LISTEN BESTÄTIGEN -“ | „Produkt ist schon gelistet (Duplikat)“ (diese ASIN wurde in diesem Chrome-Profil schon einmal erfolgreich mit Cash Lister gelistet) |
| „⚠️ WARNUNG! PRODUKT ENTHÄLT BLACKLIST-WÖRTER (<wort>) - ZUM LISTEN BESTÄTIGEN -“ | „Produkt enthält ein Wort aus der Blacklist: <wort>“ |
| „WARNUNG! ASIN PASST NICHT ZUR ADRESSE - ZUM LISTEN BESTÄTIGEN -“ | „ASIN und Adresse (URL) passen nicht zusammen“ |
| „ÜBERSPRUNGEN! Mindestbestellmenge“ | „Produkt hat eine Mindestbestellmenge“ |
| „WARNUNG! NICHT AUF LAGER - ZUM LISTEN BESTÄTIGEN -“ | „Produkt ist nicht auf Lager“ (auch bei zu langer Lieferzeit) |
| „WARNUNG! INTERNATIONALER VERSAND - ZUM LISTEN BESTÄTIGEN -“ | „Produkt wird international versendet“ |
| „WARNUNG! NICHT FBA - ZUM LISTEN BESTÄTIGEN -“ | „Nicht von Amazon versendet (Versand: …)“ oder „Versender auf der Produktseite nicht erkennbar“ (nur mit „Nur FBA“, das von Haus aus eingeschaltet ist) |
| „WARNUNG! KEIN KOSTENLOSER VERSAND - ZUM LISTEN BESTÄTIGEN -“ | „Produkt hat keinen kostenlosen Versand“ |
| „WARNUNG! GEBRAUCHT - ZUM LISTEN BESTÄTIGEN -“ | „Produkt ist gebraucht“ |
| „WARNUNG! PREIS ZU HOCH - ZUM LISTEN BESTÄTIGEN -“ / „WARNUNG! PREIS ZU NIEDRIG - ZUM LISTEN BESTÄTIGEN -“ | „Amazon-Preis zu hoch (Filter „Preis bis“)“ / „Amazon-Preis zu niedrig (Filter „Preis ab“)“ |
| „WARNUNG! KEIN CHINESISCHER VERKÄUFER - ZUM LISTEN BESTÄTIGEN -“ | „Kein chinesischer Verkäufer“ (nur mit „Nur chinesische Verkäufer“) |
| „ÜBERSPRUNGEN! keine GPSR-Angaben“ | „Keine GPSR-Angaben gefunden“ (nur mit „GPSR-Angaben übernehmen“) |
| „Auto-Listing - <ASIN>  FEHLER! Nicht angemeldet!“ | „nicht angemeldet“ – du bist in Cash Lister nicht (mehr) angemeldet. Dazu erscheint das Fenster „Nicht angemeldet - bitte im Dashboard anmelden.“ |
| „Auto-Listing - <ASIN>  FEHLER! Titel ist leer!“ / „Auto-Listing - <ASIN>  FEHLER! Titel-Erstellung fehlgeschlagen!“ | „KI-Titel ist leer“ / „Titel-Erstellung fehlgeschlagen“ – der KI-Titel konnte nicht erzeugt werden. |

Was danach mit dem Produkt in der Produkt-Datenbank passiert, steht in Abschnitt 10.14. Mehr zum Lauf selbst steht im Bereich Browser-Lister (`references/listen-auf-ebay.md`), alle Meldungen auch in `references/meldungen-und-fehler.md`.

### 8.4 Häufige Fragen (Produktseite)

**Kann ich direkt von der Amazon-Produktseite aus listen?**
Nein. Produkte kommen über die Produkt-Datenbank (oder den Konkurrenz-Scanner) in den Browser-Lister. Willst du ein einzelnes Produkt listen: Link kopieren, in der Produkt-Datenbank bei „Links hinzufügen“ einfügen, dann im Browser-Lister listen.

**Gibt es auf der Produktseite einen Knopf „zur Datenbank hinzufügen“?**
Nein. Kopiere die Adresse oder die ASIN und füge sie in der Produkt-Datenbank ein (Abschnitt 10.7).

**Der Tab-Titel ist voller „WARNUNG!“ – muss ich etwas tun?**
Nein. Beim Ansehen sind das reine Hinweise. Relevant werden sie erst, wenn der Browser-Lister das Produkt listen soll – dann wird es aus diesen Gründen übersprungen.

**Warum steht „NICHT AUF LAGER“, obwohl Amazon „Auf Lager“ zeigt?**
Mögliche Gründe: Die Lieferzeit ist länger als bei „Max. verlängerte Lieferzeit“ eingestellt (dann steht meist zusätzlich „LIEFERZEIT VERLÄNGERT“), auf der Seite steht „Extended delivery time“, oder Amazon verwendet einen Verfügbarkeitstext, den Cash Lister nicht kennt. Cash Lister kennt „auf Lager“-Texte auf Deutsch, Englisch, Italienisch, Spanisch und Niederländisch. **Nicht sicher belegt:** welche Amazon-Texte im Einzelnen fehlen (besonders auf Amazon-Seiten in anderen Sprachen) – melde solche Fälle mit Link dem Betreiber.

### 8.5 Probleme und Lösungen (Produktseite)

| Problem | Lösung |
|---|---|
| Das Taschen-Symbol am Titel fehlt. | Seite neu laden. Das Symbol erscheint nur auf Seiten, deren Adresse `/dp/` enthält. Prüfe, ob die Extension eingeschaltet ist. |
| Klick auf das Taschen-Symbol öffnet eine kaputte Adresse. | Bei „Domain“ ist vermutlich „Keine“ gewählt. Dein Land einstellen (Abschnitt 7). |
| Klick auf das Taschen-Symbol sucht auf der falschen eBay-Seite. | „Domain“ richtig einstellen (Abschnitt 7). |
| „LIEFERZEIT VERLÄNGERT“ erscheint, obwohl ich den Schalter bei „Max. verlängerte Lieferzeit“ ausgeschaltet habe. | Auf der Produktseite und beim Listen zählt immer die eingetragene Zahl, der Schalter wirkt nur beim Einsammeln auf Suchseiten. Trage eine größere Zahl ein, wenn dir längere Lieferzeiten recht sind. |
| Totenkopf im Tab, aber ich sehe das Wort nicht. | Das Wort kann auch in der Beschreibung, in den Stichpunkten oder in einem Merkmal-Wert stehen. Der Tab-Titel nennt das gefundene Wort. Passt der Treffer nicht, den Eintrag in der Blacklist anpassen. |

---

## 9. Amazon-Verkäuferseiten (Adresse mit /sp)

Auf Händlerprofilen bei Amazon zeigt Cash Lister **nichts** an.

Gebraucht wird diese Seite nur für die Prüfung „Nur chinesische Verkäufer“ (Einstellungen, Reiter „Produkt-Filter“, Karte „Beim Listen“; darunter klein: „sortiert alle anderen aus“). Ist sie eingeschaltet, öffnet der Browser-Lister beim Prüfen eines Produkts das Händlerprofil kurz in einem Hintergrund-Tab neben dem Amazon-Tab, liest den Firmensitz und schließt den Tab wieder. Öffnest du ein Händlerprofil selbst, passiert für dich sichtbar nichts. Als „chinesischer Verkäufer“ zählt ein Händler, in dessen Geschäftsadresse im Profil eine Zeile nur aus dem Länderkürzel „CN“ (China) oder „HK“ (Hongkong) besteht. Verkauft Amazon selbst, gilt das Produkt als „kein chinesischer Verkäufer“. Die Händlerseite wird auf dem Amazon-Land geöffnet, das bei „Domain“ eingestellt ist (Abschnitt 7).

---

## 10. Die Produkt-Datenbank

Die Produkt-Datenbank ist die Warteliste deiner Amazon-Produkte, die noch gelistet werden sollen.

### 10.1 Eine Liste für alle Geräte deines Kontos

- Seit Version 46.0 liegt die Produkt-Datenbank **auf dem Server, je Konto**. Alle Geräte, auf denen du mit demselben Konto angemeldet bist, sehen und benutzen **dieselbe** Liste. Oben auf der Seite steht dazu: „Die Produkt-Datenbank gilt für alle Geräte deines Kontos. Ein Lauf nimmt freie Produkte von oben.“
- Was du auf einem Gerät einsammelst, siehst du auf dem anderen Gerät, sobald du dort die Seite neu lädst oder in ihren Tab zurückwechselst.
- Was du auf einem Gerät löschst, ist auf allen Geräten weg.
- Ein Produkt, das gerade ein Gerät listet, ist **„In Arbeit“** und wird von keinem anderen Gerät genommen (Abschnitt 10.9).
- **Ohne Server gibt es keine Produkt-Datenbank:** Ohne Anmeldung oder bei einem Server-Ausfall zeigt die Seite keine Liste, sondern einen roten Kasten (Abschnitt 10.5). Importieren geht dann nicht, und der Browser-Lister nimmt keine Produkte daraus (er pausiert und macht von selbst weiter, sobald der Server wieder antwortet – siehe `references/listen-auf-ebay.md`, Abschnitt 6.5).
- Die Liste gilt für das **Konto**, nicht für einen eBay-Shop. **Nicht sicher belegt:** ob du für einen zweiten Shop ein eigenes Konto (und damit eine eigene Liste) bekommen kannst – das klärt der Betreiber.

### 10.2 So öffnest du die Produkt-Datenbank

- Seitenleiste (links auf jeder Seite von Cash Lister) → Gruppe „Arbeiten“ → „Produkt-Datenbank“, oder
- im Dashboard bei „Vorgänge“ auf die Karte „Produkte sammeln“ klicken, oder
- im Browser-Lister bei „Produkte aus“ „Produkt-Datenbank“ wählen und auf „Verwalten“ klicken.

Die Seite öffnet sich in einem eigenen Tab (Tab-Titel „Cash Lister – Produkt-Datenbank“). Ist sie schon offen, springt der Klick in diesen Tab, statt einen zweiten zu öffnen. Ohne Anmeldung (und ebenso bei abgeschaltetem Zugang oder gesperrtem Abo) sind der Eintrag in der Seitenleiste und die Karte im Dashboard ausgegraut.

**Aktualisieren:** Die Seite holt den aktuellen Stand vom Server, wenn du sie öffnest, wenn du wieder in ihren Tab wechselst und nach jeder Aktion auf der Seite. Läuft nebenbei ein Lister oder sammelst du auf Amazon ein, während der Tab im Vordergrund bleibt, siehst du Änderungen erst nach F5 oder nach einem Tab-Wechsel.

### 10.3 Aufbau der Seite

**Kopf**

- Überschrift „Produkt-Datenbank“.
- Darunter die Zahlen, z. B. „1.234 Produkte · 1.220 frei · 14 in Arbeit“ (Abschnitt 10.4).
- Darunter: „Die Produkt-Datenbank gilt für alle Geräte deines Kontos. Ein Lauf nimmt freie Produkte von oben.“
- Nur während einer Übertragung: ein orangefarbener Hinweis wie „120 Produkte werden noch auf den Server übertragen …“ (Abschnitt 10.6).

**Roter Kasten** (nur bei einem Problem, Abschnitt 10.5) mit den Knöpfen „Erneut versuchen“ und – wenn du nicht angemeldet bist – „Zum Dashboard (Anmelden)“.

**Karte „Links hinzufügen“** (links; bei schmalem Fenster oben)

- Feld „Amazon-Links oder ASINs, eine pro Zeile“ (Beispiel im Feld: `https://www.amazon.de/dp/B0ABCDEFGH` und `B0XYZ12345`).
- Knopf „Zur Datenbank hinzufügen“ und darunter die Ergebnis-Meldung.

**Karte „Bestand“** (rechts; bei schmalem Fenster darunter)

- Neben der Überschrift bei mehr als 200 Produkten der angezeigte Bereich, z. B. „(1–200 von 523)“.
- Rechts oben die Auswahl „Sortierung“ mit „Älteste zuerst“ und „Neuste zuerst“ (Abschnitt 10.12).
- Die Tabelle mit den Spalten „ASIN“, „Link“, „Hinzugefügt“, „Quelle“, „In Arbeit“ und einem roten „✕“ pro Zeile (die Spaltenköpfe werden in Großbuchstaben angezeigt).
- Unten die Knöpfe „Sheet-Abgleich prüfen“, „Als TXT exportieren“, „Alle löschen“ (rot), daneben eine kurze Meldungszeile, ganz rechts „◂ Zurück“ und „Weiter ▸“.
- Nach „Sheet-Abgleich prüfen“ erscheint ganz unten in der Karte, unter den Knöpfen, das Ergebnis (Abschnitt 11.3).

### 10.4 Die Zahlen oben und der Hinweis zur Übertragung

| Anzeige | Bedeutung |
|---|---|
| „…“ | Die Seite lädt noch. |
| „1.234 Produkte · 1.220 frei · 14 in Arbeit“ | 1.234 Produkte liegen insgesamt in der Produkt-Datenbank deines Kontos. 1.220 davon sind frei (ein Lauf kann sie nehmen), 14 hat gerade ein Gerät oder der CSV-Lister in Arbeit. |
| „1.234 Produkte“ (ohne „frei“/„in Arbeit“) | Die Liste kam an, die genaueren Zahlen nicht. Seite neu laden. |
| „Bestand gerade nicht abrufbar“ | Server nicht erreichbar oder du bist nicht angemeldet – siehe roter Kasten (Abschnitt 10.5). |
| „1 Produkt wird noch auf den Server übertragen …“ / „… Produkte werden noch auf den Server übertragen …“ (orange) | Deine alte Liste aus diesem Chrome-Profil wird gerade hochgeladen (Abschnitt 10.6). Die Seite holt sich dann etwa alle 10 Sekunden selbst den neuen Stand, bis alles übertragen ist. |
| „1 Produkt dieses Geräts wartet darauf, nach der Anmeldung auf den Server übertragen zu werden.“ / „… Produkte dieses Geräts warten darauf, nach der Anmeldung …“ | Es liegt noch eine alte Liste in diesem Chrome-Profil, aber du bist nicht angemeldet. Nach der Anmeldung wird sie hochgeladen. |
| „… Produkte dieses Geräts warten darauf, sobald der Server erreichbar ist, auf den Server übertragen zu werden.“ | Wie oben, aber der Server ist gerade nicht erreichbar. Es geht von selbst weiter. |

Dieselben Zahlen siehst du im Dashboard in der Karte „Produkte in der Datenbank“ (siehe `references/dashboard.md`).

### 10.5 Roter Kasten: Server nicht erreichbar oder nicht angemeldet

Kann die Seite die Liste nicht vom Server holen, steht oben ein roter Kasten. Die Tabelle ist dann leer, „◂ Zurück“ und „Weiter ▸“ sind gesperrt, oben steht „Bestand gerade nicht abrufbar“. **Deine Produkte sind deshalb nicht weg** – sie liegen auf dem Server und erscheinen wieder, sobald die Verbindung steht.

| Text im roten Kasten | Bedeutung / was tun |
|---|---|
| „Server nicht erreichbar – die Produkt-Datenbank liegt jetzt auf dem Server. Bitte später erneut versuchen.“ | Der Server hat nicht geantwortet. Später auf „Erneut versuchen“ klicken. Die Seitenleiste zeigt unten „Server nicht erreicht“. Hält das lange an, an den Betreiber wenden. |
| „Bitte zuerst anmelden – das geht im Dashboard.“ (mit Knopf „Zum Dashboard (Anmelden)“) | Du bist nicht angemeldet oder deine Anmeldung ist abgelaufen. Auf „Zum Dashboard (Anmelden)“ klicken, dort anmelden, dann hier „Erneut versuchen“. Dieser Text erscheint auch, wenn dein **Zugang abgeschaltet** oder dein **Abo gesperrt** ist – schau dann unten in die Seitenleiste: Steht dort „Abo gesperrt“ oder „Zugang abgeschaltet“, liegt es daran (siehe `references/konto-und-installation.md`). |
| „Fehler: … lehnt die Anfrage ab (HTTP …) – bitte die Extension aktualisieren oder beim Betreiber melden.“ | Der Server nimmt die Anfrage nicht an. Extension aktualisieren (update.bat, danach Chrome komplett neu starten). Hilft das nicht, an den Betreiber wenden. |
| „Fehler: …“ mit anderem Text | Ein unerwarteter Fehler. „Erneut versuchen“; hilft das nicht, Seite neu laden bzw. Chrome neu starten. Bleibt es, den Text dem Betreiber schicken. |

Der rote Kasten erscheint auch, wenn ein Löschen, „Alle löschen“ oder „Als TXT exportieren“ am Server scheitert; die Tabelle bleibt dann stehen.

### 10.6 Erster Start nach dem Update: deine alte Liste wandert auf den Server

Bis Version 45.x lag die Produkt-Datenbank nur in deinem Chrome-Profil. Nach dem Update auf 46.0 lädt Cash Lister diese alte Liste **von selbst** auf den Server hoch. Du musst nichts tun.

1. Das passiert, sobald du angemeldet bist – beim Start von Chrome, nach der Anmeldung oder wenn du eine Seite öffnest, die die Produkt-Datenbank braucht (z. B. die Seite „Produkt-Datenbank“).
2. Bei einer großen Liste dauert das etwas. Oben auf der Seite steht dann z. B. „350 Produkte werden noch auf den Server übertragen …“, im Dashboard „… werden noch auf den Server übertragen“ bzw. „Die bisherige Datenbank dieses PCs wird auf den Server übertragen“.
3. **Was mitgenommen wird:** ASIN, Datum der Aufnahme (die Reihenfolge bleibt also erhalten) und die Quelle.
4. **Was nicht in die neue Liste kommt:** Produkte, die in deinen Google Sheets als gelistet stehen (Abschnitt 11), Produkte, die mit deinem Konto schon gelistet sind, Produkte, die schon ein anderer Kunde hat („belegt“), und Einträge ohne gültige ASIN. Sie verschwinden einfach aus der alten Liste.
5. Ist der Server während der Übertragung weg oder bist du abgemeldet, bleibt der Rest in diesem Chrome-Profil liegen und wird beim nächsten Anlass weiter hochgeladen.
6. Haben **mehrere Geräte** eine alte Liste, lädt jedes seine hoch. Doppelte ASINs landen nur einmal in der gemeinsamen Liste.

### 10.7 Links hinzufügen (von Hand)

Schritt für Schritt:

1. Im Dashboard angemeldet sein.
2. Amazon-Links oder ASINs sammeln (z. B. aus einer Tabelle kopieren).
3. Ins Feld unter „Links hinzufügen“ einfügen – **ein Produkt pro Zeile**.
4. „Zur Datenbank hinzufügen“ klicken. Es erscheint „Füge … Links hinzu …“ (bei mehr als 200 Zeilen zusätzlich „Bei vielen Links dauert das etwas.“). Der Knopf ist so lange gesperrt.
5. Danach steht dort z. B.: „✅ 25 hinzugefügt, 3 schon drin, 2 schon gelistet, 1 belegt (hat schon ein anderer Kunde), 1 ohne erkennbare ASIN ignoriert.“ Teile, die 0 wären, fehlen in der Meldung (im einfachsten Fall steht nur „✅ 25 hinzugefügt.“).
6. Bei Erfolg wird das Feld geleert und die Tabelle springt auf Seite 1. **Bei einem Fehler bleiben deine Links im Feld stehen**, damit du sie später einfach noch einmal abschicken kannst.

Was erkannt wird (pro Zeile):

- Amazon-Links in vielen Formen: mit `/dp/`, `/gp/product/`, `/gp/aw/d/` (Handy-Links), `/product/`, `/exec/obidos/asin/` oder `asin=` in der Adresse – auch gesponserte Links, Links mit Zusätzen hinten dran und Links aus einer kopierten Tabellenzeile (z. B. „Link“ + Tabulator + „Preis“).
- Eine **reine ASIN am Zeilenanfang** (in Großbuchstaben), danach darf ein Leerzeichen, Tabulator, Komma oder Semikolon folgen.
- Notfalls irgendwo in der Zeile eine ASIN der Form `B0` + 8 Zeichen.
- Leere Zeilen werden ignoriert.

Was mit erkannten Produkten passiert:

- Gespeichert wird **nur die ASIN** (mit Datum und Quelle „Links“). Das Amazon-Land aus deinem Link wird **nicht** gespeichert – angezeigt und gelistet wird immer mit dem Land deiner Einstellung „Domain“ (Abschnitt 7).
- Dieselbe ASIN zweimal in deiner Eingabe zählt einmal als „schon drin“.
- ASINs, die schon in der Produkt-Datenbank deines Kontos liegen, zählen als „schon drin“.
- Produkte, die laut deinen Google Sheets schon gelistet sind (Abschnitt 11) oder mit deinem Konto schon gelistet wurden, zählen als „schon gelistet“ und kommen nicht hinein.
- Produkte, die schon ein anderer Kunde hat, zählen als „belegt (hat schon ein anderer Kunde)“ und kommen nicht hinein (Abschnitt 13).
- Jedes neu aufgenommene Produkt ist damit für dein Konto reserviert.
- Wo das neue Produkt in der Liste steht, hängt von der „Sortierung“ ab (Abschnitt 10.12).

Meldungen beim Hinzufügen:

| Meldung | Bedeutung / was tun |
|---|---|
| „Füge … Links hinzu …“ | Läuft. Bei langen Listen kann das dauern. |
| „✅ … hinzugefügt …“ | Fertig, siehe Teile oben. |
| „… schon drin“ | schon in der Produkt-Datenbank deines Kontos (oder doppelt in deiner Eingabe) |
| „… schon gelistet“ | steht in deinen Google Sheets oder wurde mit deinem Konto schon gelistet |
| „… belegt (hat schon ein anderer Kunde)“ | ein anderer Kunde hat das Produkt; nicht aufgenommen |
| „… ohne erkennbare ASIN ignoriert“ | in der Zeile wurde keine ASIN gefunden; Zeile prüfen |
| „Nichts importiert – Server nicht erreichbar. Bitte später erneut versuchen.“ (rot) | Der Server hat nicht geantwortet. Es wurde **nichts** gespeichert; die Links bleiben im Feld. Später noch einmal klicken. |
| „Nichts importiert – bitte zuerst im Dashboard anmelden.“ (rot) | Du bist nicht angemeldet (oder die Anmeldung ist abgelaufen, oder Zugang/Abo ist gesperrt – siehe Seitenleiste unten). Im Dashboard anmelden, dann noch einmal klicken. |
| „Nur teilweise importiert – … Von … Produkten wurden die ersten … verarbeitet (… neu), der Rest nicht – einfach noch einmal importieren, Doppelte werden erkannt.“ (rot) | Nur bei großen Mengen (mehr als 200 Produkte, die nach dem Aussortieren von Doppelten und schon Gelisteten übrig bleiben): Mitten im Import brach die Verbindung ab. Der Anfang der Meldung nennt den Grund, z. B. Server nicht erreichbar, „Sitzung abgelaufen – bitte im Dashboard neu anmelden.“, „Abo gesperrt – bitte im Dashboard nachsehen.“ oder „Zugang abgeschaltet – bitte beim Betreiber melden.“. Ein Teil ist gespeichert. Die Links stehen noch im Feld – einfach noch einmal auf „Zur Datenbank hinzufügen“ klicken; was schon drin ist, zählt dann als „schon drin“. |
| „Nichts importiert – Fehler: …“ (rot) | Ein anderer Fehler, z. B. „… lehnt die Anfrage ab (HTTP …) – bitte die Extension aktualisieren oder beim Betreiber melden.“ oder „keine Antwort“ bzw. ein englischer Text von Chrome wie „The message port closed before a response was received.“ (die Extension hat nicht geantwortet). Seite neu laden und erneut versuchen; bei „lehnt die Anfrage ab“ die Extension aktualisieren bzw. an den Betreiber wenden. Doppelte Produkte entstehen beim erneuten Versuch nicht. |

Wenn das Feld leer ist, passiert beim Klick nichts. Eine feste Obergrenze für die Anzahl der Zeilen gibt es in der Extension nicht; große Mengen werden in Teilen zum Server geschickt. **Nicht sicher belegt:** ob der Server selbst eine Höchstzahl an Produkten je Konto hat – frag bei Bedarf den Betreiber.

### 10.8 Die Tabelle Bestand

| Spalte | Inhalt |
|---|---|
| „ASIN“ | die Amazon-Artikelnummer |
| „Link“ | der Amazon-Link in Kurzform, z. B. „amazon.de/dp/B0ABCDEFGH“ – gebildet aus der ASIN und deiner Einstellung „Domain“; Klick öffnet die Produktseite in einem neuen Tab |
| „Hinzugefügt“ | Datum und Uhrzeit der Aufnahme, z. B. „26.10.2026 14:32“ |
| „Quelle“ | woher das Produkt kam: „Links“ (von Hand eingefügt), „Amazon-Suche“ (Knopf auf einer Amazon-Suchseite), „Schaufenster“ (Verkäufer-Schaufenster, auch „Ganzer Shop“) |
| „In Arbeit“ | leer, wenn das Produkt frei ist; sonst wer es gerade bearbeitet und bis wann (Abschnitt 10.9) |
| „✕“ | löscht dieses eine Produkt (Abschnitt 10.10) |

- Eine Seite zeigt **200 Produkte**. „◂ Zurück“ und „Weiter ▸“ sind immer da, aber nur klickbar, wenn es eine vorherige bzw. weitere Seite gibt.
- Bei mehr als 200 Produkten steht neben der Überschrift „Bestand“ der angezeigte Bereich, z. B. „(1–200 von 523)“.
- Hat ein anderes Gerät inzwischen so viel gelistet oder gelöscht, dass deine Seite nicht mehr existiert, springt die Tabelle von selbst auf die letzte vorhandene Seite.
- Es gibt **keine** Suche, **keinen** Filter und **keine** Sortierung per Klick auf die Spaltenköpfe. Alles in der Tabelle wartet noch auf das Listen – sobald ein Produkt gelistet wurde (oder beim Listen gescheitert ist), ist es nicht mehr in der Datenbank.

### 10.9 Die Spalte In Arbeit

In der Spalte „In Arbeit“ steht bei einem Produkt, das gerade ein Lister genommen hat, eine farbige Marke mit **Gerät und Uhrzeit**, z. B.:

- „Gerät a1b2c3 bis 14:32“ – ein Gerät ohne eingetragenen Namen (die Zeichen sind eine Kennung des Geräts).
- „Server-1 bis 26.10. 14:32“ – ein Gerät mit eigenem Namen; bei einem anderen Tag steht das Datum dabei.
- „… (dieses Gerät)“ – das Gerät, an dem du gerade sitzt.
- „CSV-Lister“ bzw. „<Name> · CSV-Lister“ – der CSV-Lister hat das Produkt (seit Version 46.0 steht er allen Kunden zur Verfügung, siehe `references/produktuebersicht-und-csv-lister.md`). Läuft er auf dem Gerät, an dem du sitzt, steht auch hier „(dieses Gerät)“ dahinter.
- „anderes Gerät“ – selten: Der Server hat zu dem Vermerk weder einen Namen noch eine Kennung mitgeschickt.

Was du darüber wissen musst:

- Ein Produkt „In Arbeit“ nimmt **kein anderes Gerät**. So listen zwei deiner Geräte nie dasselbe Produkt gleichzeitig.
- Die Uhrzeit hinter „bis“ sagt, wie lange der Vermerk gerade gilt. Solange das Gerät am Produkt arbeitet, verlängert es den Vermerk von selbst. Ist die Zeit abgelaufen, gilt das Produkt wieder als frei, und die Zelle bleibt leer (die Seite lässt dabei etwa eine Minute Spielraum, falls die Uhr deines Rechners etwas anders geht als die des Servers).
- So weit in die Zukunft reicht die Zeit hinter „bis“ (Werte, die Cash Lister selbst beim Server anfragt):
  - **Browser-Lister:** etwa 30 Minuten; solange er das Produkt hat, verlängert er etwa alle 5 Minuten.
  - **CSV-Lister:** etwa 1 Stunde; solange seine Seite läuft, verlängert er etwa alle 10 Minuten. Steht ein Produkt schon in einer CSV-Datei, die zu eBay hochgeladen wird bzw. auf das Ergebnis von eBay wartet, verlängert der CSV-Lister auf bis zu **7 Tage**. Ein „bis“ mehrere Tage in der Zukunft beim CSV-Lister ist also normal.
- **Namen für deine Geräte:** Trägst du in den Einstellungen (Reiter „eBay & Rahmenbedingungen“, Karte „Server-Modus“) bei „Gerätename“ einen Namen ein, steht dieser Name in der Spalte statt „Gerät …“. Ist bei „Dieses Gerät ist ein Server“ der Schalter an, steht dort mindestens „Server“. Mehr zum Server-Modus in `references/einstellungen.md`.
- Fährst du mit der Maus über die Marke, siehst du die vollständige Kennung des Geräts.
- Stürzt ein Gerät ab (oder wird Chrome mitten im Lauf beendet), während es ein Produkt in Arbeit hat, bleibt der Vermerk stehen, bis die Uhrzeit hinter „bis“ erreicht ist, und das Produkt wird dann von selbst wieder frei. Beim Browser-Lister ist das also spätestens nach etwa einer halben Stunde der Fall, beim CSV-Lister nach etwa einer Stunde bzw. – bei Produkten, die schon in einer CSV-Datei standen – erst nach bis zu 7 Tagen. Willst du nicht warten, kannst du das Produkt mit „✕“ löschen (mit Rückfrage, Abschnitt 10.10).

### 10.10 Einzelne Produkte löschen

Mit dem roten „✕“ am Ende der Zeile löschst du ein einzelnes Produkt. Es verschwindet aus der Produkt-Datenbank **aller** deiner Geräte, und seine Reservierung wird freigegeben – andere Kunden können es danach bekommen.

- **Produkt ist frei** (Spalte „In Arbeit“ leer): Es wird **sofort, ohne Rückfrage** gelöscht. Hinweis beim Darüberfahren: „Eintrag löschen“.
- **Produkt ist „In Arbeit“**: Hinweis beim Darüberfahren „In Arbeit: <wer> bis <Uhrzeit> – Löschen nur nach Rückfrage“. Beim Klick fragt Cash Lister:
  „<ASIN> ist gerade in Arbeit (<wer> bis <Uhrzeit>). Trotzdem löschen? Wird es dort gerade gelistet, ist die Reservierung danach weg – ein anderer Kunde könnte dasselbe Produkt listen. Nur löschen, wenn das Gerät nicht mehr daran arbeitet (z. B. abgestürzt).“
  - „Abbrechen“: nichts passiert.
  - „OK“: Das Produkt wird trotzdem gelöscht. Was dann mit dem Gerät passiert, das es hatte:
    - Hat **dieses** Gerät (Browser-Lister) es nur bereitgelegt und noch nicht mit dem Listen angefangen, listet es das Produkt nicht mehr.
    - Hat ein **anderes** Gerät es nur bereitgelegt, merkt es spätestens bei seiner nächsten Verlängerung (Browser-Lister etwa alle 5 Minuten, CSV-Lister etwa alle 10 Minuten) oder – beim Browser-Lister – bei einer Nachfrage kurz vor dem Listen, dass das Produkt weg ist, und lässt es los. Hat ein Browser-Lister das Produkt erst vor Kurzem (etwa innerhalb der letzten Minute) genommen, fragt er vor dem Listen nicht nach und kann trotzdem mit dem Listen beginnen.
    - Ist ein Gerät **schon mitten im Listen** (Amazon-/eBay-Tab läuft), listet es das Produkt trotzdem zu Ende.
    - Wird das Produkt so trotzdem gelistet, ist die Reservierung durch das Löschen weg – ein anderer Kunde könnte dasselbe Produkt listen. **Nicht sicher belegt:** ob die Reservierung nach einem solchen Zu-Ende-Listen wieder für dich gilt – das entscheidet der Server, frag bei Bedarf den Betreiber.
    - Deshalb nur löschen, wenn das Gerät wirklich nicht mehr daran arbeitet (z. B. abgestürzt).
- Während des Löschens ist das „✕“ ausgegraut.

Mögliche Meldungen unten in der Karte (neben „Alle löschen“):

| Meldung | Bedeutung |
|---|---|
| „<ASIN> ist gerade in Arbeit gekommen und bleibt stehen – nach dem Neuladen mit Rückfrage löschbar.“ | Zwischen dem Anzeigen und deinem Klick hat ein Gerät das Produkt genommen. Es wurde nicht gelöscht. Seite neu laden, dann erscheint die Rückfrage. |
| „<ASIN> war schon nicht mehr in der Datenbank.“ | Ein anderes Gerät hat es inzwischen gelistet oder gelöscht. Nichts zu tun. |

Scheitert das Löschen am Server, erscheint der rote Kasten (Abschnitt 10.5), und das Produkt bleibt stehen.

### 10.11 Alle löschen

1. Unten in der Karte „Bestand“ auf „Alle löschen“ (rot) klicken.
2. Cash Lister fragt: „Wirklich ALLE Produkte aus der Datenbank löschen? Das gilt für alle Geräte deines Kontos – die Liste ist danach überall leer.“
3. Bei „OK“ werden alle **freien** Produkte gelöscht und ihre Reservierungen freigegeben – andere Kunden können diese Produkte danach greifen.
4. **Produkte „In Arbeit“ bleiben stehen** – egal, ob dieses oder ein anderes Gerät sie gerade bearbeitet. Die Meldung lautet dann z. B. „3 Produkte sind gerade in Arbeit und bleiben stehen (einzeln mit ✕ löschbar).“ bzw. „1 Produkt ist gerade in Arbeit und bleibt stehen (einzeln mit ✕ löschbar).“ Ohne solche Produkte: „Datenbank geleert.“
5. Liegt in diesem Chrome-Profil noch eine alte, nicht übertragene Liste (Abschnitt 10.6), wird sie vor dem Löschen erst hochgeladen und dann mitgelöscht. Klappt das Hochladen nicht (Server weg, nicht angemeldet), wird **nichts** gelöscht und der rote Kasten erscheint.

Das lässt sich nicht rückgängig machen. Wenn du die Produkte behalten willst, vorher „Als TXT exportieren“.

### 10.12 Die Sortierung

Ein Lauf nimmt **immer die obersten freien Produkte** zuerst. Mit „Sortierung“ (rechts oben in der Karte „Bestand“) legst du fest, was als Nächstes gelistet wird:

- „Älteste zuerst“ (Standard): Neue Produkte landen unten, der älteste Bestand wird zuerst abgearbeitet.
- „Neuste zuerst“: Neue Produkte landen oben und werden als Nächstes gelistet.

Wichtig:

- Die Sortierung gilt **nur für dieses Gerät** (Hinweis beim Darüberfahren: „Gilt nur für dieses Gerät: Anzeige und welche freien Produkte es als Nächstes nimmt“). Sie bestimmt die Anzeige auf diesem Gerät und welche Produkte der Browser-Lister dieses Geräts als Nächstes nimmt. Deine anderen Geräte können anders sortiert sein; doppelt nehmen kann trotzdem keines, weil jedes Produkt immer nur bei einem Gerät „In Arbeit“ ist.
- Die Liste selbst wird dabei nicht verändert, nur anders angezeigt und anders abgearbeitet.
- Beim Umstellen springt die Tabelle auf Seite 1. Die Einstellung bleibt gespeichert.
- Klappt das Umstellen nicht, erscheint ein Fenster „Sortieren fehlgeschlagen: …“ – dann die Seite neu laden und noch einmal versuchen.
- **Nicht sicher belegt:** in welcher Reihenfolge Produkte stehen, die mit demselben Klick (z. B. einer Amazon-Seite) aufgenommen wurden.

### 10.13 Als TXT exportieren

1. Unten in der Karte „Bestand“ auf „Als TXT exportieren“ klicken. Es erscheint „Exportiere …“.
2. Cash Lister lädt eine Textdatei herunter: `produkt-datenbank_<Datum>.txt` (Datum als Jahr-Monat-Tag, z. B. `produkt-datenbank_2026-10-26.txt`; das Datum richtet sich nach der Weltzeit – kurz nach Mitternacht kann deshalb noch das Datum des Vortags im Namen stehen). Sie enthält **alle** Produkte der Produkt-Datenbank deines Kontos (auch die „In Arbeit“), einen Amazon-Link pro Zeile. Die Links werden mit deiner Einstellung „Domain“ gebildet.
3. Danach steht dort z. B. „1.234 Links exportiert.“ Ist die Datenbank leer: „Die Datenbank ist leer – nichts zu exportieren.“

Die Produkte **bleiben** dabei in der Datenbank, und ihre Reservierung bleibt bestehen. (Anders beim Konkurrenz-Scanner: dort entfernt der Export die Funde.)

Die Datei kannst du z. B. als Sicherung aufheben. Da die Produkt-Datenbank ohnehin auf allen deinen Geräten gleich ist, brauchst du sie zum Umziehen auf einen anderen Rechner nicht mehr.

### 10.14 Verbindung zum Browser-Lister

Im Browser-Lister steht oben:

- „Produkte aus“ – Auswahl „Produkt-Datenbank“ oder „Konkurrenz-Scanner“, daneben der Bestand (bei der Produkt-Datenbank z. B. „1.220 verfügbar · 14 in Arbeit“) und der Knopf „Verwalten“ (öffnet die gewählte Seite oder springt in ihren Tab).
- „Wie viele Angebote“ – so viele **erfolgreiche** Angebote soll der Lauf erzeugen (Standard 100).

So hängen Produkt-Datenbank und Lauf zusammen (ausführlich in `references/listen-auf-ebay.md`, Abschnitt 6):

1. Der Lauf nimmt **ein freies Produkt nach dem anderen von oben** (nach der Sortierung dieses Geräts) – genau so viele, wie er für die Zielzahl braucht.
2. Ein genommenes Produkt bleibt in der Liste stehen, ist aber **„In Arbeit“** für dieses Gerät.
3. **Erfolgreich gelistet:** Das Produkt verlässt die Produkt-Datenbank, die Reservierung bleibt für dich bestätigt.
4. **Fehlgeschlagen** (z. B. „Produkt ist nicht auf Lager“): Das Produkt verlässt ebenfalls die Produkt-Datenbank, die Reservierung wird freigegeben, und es erscheint im „Statusbericht“. Es kommt **nicht automatisch** zurück. Willst du es später erneut versuchen, füge den Link wieder hinzu.
5. **Genommen, aber noch nicht bearbeitet** (z. B. bei „Stoppen & zurücksetzen“ oder wenn die Zielzahl erreicht ist): Das Produkt geht zurück und ist sofort wieder frei.
6. Ist kein freies Produkt mehr da, bevor die Zielzahl erreicht ist, meldet der Browser-Lister „Quelle aufgebraucht - … von … gelistet. Erst neue Produkte einsammeln, dann noch einmal starten.“
7. Startest du mit leerer Datenbank, kommt „Die Produkt-Datenbank ist leer - erst Produkte einsammeln.“ Sind zwar Produkte da, aber alle „In Arbeit“: „Alle … Produkte der Datenbank sind gerade in Arbeit - auf einem anderen Gerät oder im CSV-Lister. Später erneut starten.“
8. Ist der Server beim Start nicht erreichbar: „Server nicht erreichbar - die Produkt-Datenbank liegt auf dem Server. Bitte später erneut starten.“ Bist du nicht angemeldet: „Nicht angemeldet oder Sitzung abgelaufen - bitte im Dashboard anmelden, dann starten.“
9. Fällt der Server während eines Laufs aus, pausiert der Browser-Lister und macht von selbst weiter.
10. Während eines Laufs sind die Auswahl „Produkte aus“ und das Feld „Wie viele Angebote“ gesperrt.
11. Ist „Konkurrenz-Scanner“ gewählt und die Fundliste leer, kommt beim Start „Der Konkurrenz-Scanner hat noch keine Funde.“

### 10.15 Häufige Fragen (Produkt-Datenbank)

**Ist meine Produkt-Datenbank auf allen meinen Rechnern gleich?**
Ja – auf allen Geräten, auf denen du mit **demselben Konto** angemeldet bist. Du musst nichts übertragen. Je Gerät gelten nur die „Sortierung“, die Einstellung „Domain“ und die im Tracker eingetragenen Google Sheets (für den Sheet-Abgleich beim Einsammeln, Abschnitt 11).

**Ich sehe auf meinem zweiten Rechner eine leere Liste.**
Prüfe, ob du dort mit demselben Konto angemeldet bist (Dashboard bzw. unten in der Seitenleiste „angemeldet als …“). Lade die Seite neu. Steht oben „… Produkte dieses Geräts warten darauf …“, wird gerade noch eine alte Liste dieses Geräts hochgeladen.

**Ist die Produkt-Datenbank in „Einstellungen exportieren“ enthalten?**
Nein. Sie liegt auf dem Server und kommt nicht mehr in diese Datei – auch wenn der Hinweistext im Reiter „Sicherung“ noch sagt, der Export enthalte die Produkt-Datenbank. Brauchst du eine Kopie, nimm „Als TXT exportieren“. „Einstellungen vom Server holen“ ändert an der Produkt-Datenbank nichts (Hinweis am Knopf: „… Schlüssel und Produkt-Datenbank bleiben.“).

**Was passiert, wenn ich eine alte Einstellungsdatei importiere, in der noch eine Produkt-Datenbank steckt?**
Die Produkte aus der Datei werden zu deiner Produkt-Datenbank auf dem Server **hinzugefügt** (nicht ersetzt) – auf dem gleichen Weg wie beim ersten Start nach dem Update (Abschnitt 10.6). Doppelte, schon gelistete und von anderen belegte Produkte fallen dabei heraus.

**Wie viele Produkte passen in die Datenbank?**
In der Extension gibt es keine feste Obergrenze; die Tabelle zeigt sie in Seiten zu je 200. **Nicht sicher belegt:** ob der Server eine Grenze hat – frag den Betreiber.

**Warum ist ein Produkt, das ich gerade importiert habe, nicht in der Liste?**
Entweder lag es schon drin („schon drin“), es steht in deinen Sheets oder wurde schon gelistet („schon gelistet“), ein anderer Kunde hat es („belegt“), oder die Seite ist noch nicht neu geladen. Lies die Meldung nach dem Import.

**Warum wird die Datenbank kleiner, obwohl ich nichts lösche?**
Der Browser-Lister (auch auf deinen anderen Geräten) nimmt während eines Laufs Produkte – auch die, die beim Listen scheitern, verlassen danach die Liste.

**Warum steht bei einem Produkt „In Arbeit“, obwohl gerade kein Lister läuft?**
Entweder läuft auf einem anderen Gerät (oder im CSV-Lister) etwas, oder ein Gerät wurde mitten im Lauf beendet bzw. ist abgestürzt. Der Vermerk läuft dann von selbst ab (Abschnitt 10.9). Eilig? Mit „✕“ und Rückfrage löschen.

**Kann ich Produkte in der Datenbank bearbeiten (z. B. Titel oder Preis vorgeben)?**
Nein. Die Datenbank speichert nur ASIN, Datum und Quelle. Titel und Preis entstehen beim Listen. (Eigene Titel gehen nur über die Funde des Konkurrenz-Scanners, Abschnitt 12.)

**Kann ich einzelne Produkte nach oben schieben?**
Nein. Es gibt nur die beiden Sortierungen „Älteste zuerst“ / „Neuste zuerst“.

**Kann ich auf einem Gerät amazon.de und auf einem anderen amazon.com benutzen?**
Die Liste ist dieselbe, aber jedes Gerät bildet die Links mit seiner eigenen „Domain“. Ein Gerät mit „USA“ würde dieselben ASINs auf amazon.com listen. Stell „Domain“ deshalb auf allen Geräten gleich ein (Abschnitt 7).

### 10.16 Probleme und Lösungen (Produkt-Datenbank)

| Problem | Lösung |
|---|---|
| Roter Kasten „Server nicht erreichbar …“. | Später „Erneut versuchen“. Deine Produkte sind nicht weg. Hält es lange an, an den Betreiber wenden. |
| Roter Kasten „Bitte zuerst anmelden – das geht im Dashboard.“ | „Zum Dashboard (Anmelden)“, dort anmelden, zurück, „Erneut versuchen“. Steht unten in der Seitenleiste „Abo gesperrt“ oder „Zugang abgeschaltet“, liegt es daran – siehe `references/konto-und-installation.md`. |
| Die Seite zeigt „Bestand gerade nicht abrufbar“ und eine leere Tabelle. | Das ist der Fehlerzustand – siehe roter Kasten oben auf der Seite (Abschnitt 10.5). |
| „Nichts importiert – …“ beim Hinzufügen. | Die Links stehen noch im Feld. Grund in der Meldung beheben (anmelden bzw. warten, bis der Server wieder da ist), dann noch einmal klicken. |
| „Nur teilweise importiert – …“. | Einfach noch einmal auf „Zur Datenbank hinzufügen“ klicken – schon gespeicherte Produkte zählen dann als „schon drin“. |
| „Nichts importiert – Fehler: keine Antwort“ (oder dahinter ein englischer Text von Chrome, z. B. „The message port closed before a response was received.“). | Seite neu laden und noch einmal versuchen. Hilft das nicht, Chrome komplett neu starten (oder unter `chrome://extensions` bei Cash Lister „Neu laden“). Bei sehr langen Listen in kleineren Teilen einfügen. |
| Viele Zeilen „ohne erkennbare ASIN ignoriert“. | Prüfe die Zeilen: Ist es wirklich ein Amazon-Produktlink? Steht eine reine ASIN in Großbuchstaben am Zeilenanfang? Kurzlinks wie „amzn.to/…“ enthalten keine ASIN – öffne sie im Browser und kopiere die lange Adresse. |
| Die Links in der Tabelle zeigen auf amazon.com statt amazon.de (oder umgekehrt). | Einstellung „Domain“ prüfen (Einstellungen → „Preise & Listing“ → „Listing“). Die Links passen sich sofort an; du musst nichts neu einfügen. |
| Ein Produkt steht ewig „In Arbeit“. | Läuft wirklich kein Lister (auch nicht auf einem anderen Gerät oder im CSV-Lister)? Dann abwarten, bis der Vermerk abläuft, oder mit „✕“ und Rückfrage löschen. |
| „Alle löschen“ hat nicht alles gelöscht. | Richtig: Produkte „In Arbeit“ bleiben stehen. Einzeln mit „✕“ löschen (mit Rückfrage) oder warten, bis sie fertig gelistet bzw. wieder frei sind. |
| Oben steht seit Langem „… Produkte werden noch auf den Server übertragen …“. | Die Übertragung läuft in Teilen und wartet, wenn der Server nicht antwortet. Angemeldet bleiben und warten. Bewegt sich die Zahl gar nicht, Chrome neu starten; bleibt es, an den Betreiber wenden. |
| Ein Produkt soll erneut gelistet werden, nachdem es fehlgeschlagen ist. | Den Link aus dem „Statusbericht“ kopieren und bei „Links hinzufügen“ wieder einfügen. |
| Der Eintrag „Produkt-Datenbank“ in der Seitenleiste ist ausgegraut. | Du bist nicht angemeldet (oder Zugang/Abo ist gesperrt). Im Dashboard anmelden. |

---

## 11. Sheet-Abgleich: Schutz vor doppelten eigenen Angeboten

### 11.1 Was macht der Sheet-Abgleich?

Wenn du Produkte in die Produkt-Datenbank holst (Knopf auf Amazon, „Ganzer Shop“ oder von Hand) und wenn die alte Liste nach dem Update hochgeladen wird, liest Cash Lister deine hinterlegten **Google Sheets** und überspringt jede ASIN, die dort schon steht. So landen Produkte, die du (oder ein anderer deiner Shops) schon gelistet hast, gar nicht erst wieder in der Datenbank. In den Meldungen zählen sie zu „bereits gelistet“ bzw. „schon gelistet“.

- Erkannt werden ASINs aus Amazon-Links mit `/dp/`, `/gp/product/` oder `/product/` (oder `asin=`) und reine ASINs der Form `B0…` irgendwo im Sheet. ASINs, die nicht mit „B0“ beginnen, werden nur in Link-Form erkannt. Handy-Links (`/gp/aw/d/`) werden im Sheet **nicht** erkannt (anders als beim Einfügen in die Produkt-Datenbank).
- Von einem Google Sheet wird nur **ein Tabellenblatt** gelesen: das, dessen Kennung im Link steht (`gid=…`, das ist das Blatt, das beim Kopieren des Links offen war). Fehlt die Kennung, wird das Blatt mit der Kennung 0 gelesen – meist das zuerst angelegte Blatt. Stehen deine gelisteten Produkte auf einem anderen Blatt, kopiere den Link, während genau dieses Blatt geöffnet ist.
- Ist ein Sheet nicht lesbar oder antwortet es nicht innerhalb von etwa 12 Sekunden, wird es **übergangen** – der Import läuft trotzdem weiter, dann aber ohne den Abgleich mit diesem Sheet.
- Die Sheets werden beim Einsammeln höchstens etwa einmal pro Minute neu gelesen.
- Der Sheet-Abgleich läuft auf dem Gerät, auf dem du einsammelst – mit den Sheets, die **dort** eingetragen sind.
- Für die Funde des **Konkurrenz-Scanners** gibt es keinen Sheet-Abgleich.

### 11.2 Wo trägst du die Sheets ein?

Im **Tracker** (Seitenleiste → „Tracker“), Karte „Google Sheets“ (darunter: „Duplikat-Abgleich mit deinen Shop-Sheets“):

- „Haupt-Sheet dieses Shops – Web-App-URL“
- „Haupt-Sheet – Lese-Link“ (wird bevorzugt, wenn vorhanden – dann wird die Web-App-URL für den Abgleich gar nicht gelesen)
- „Weitere Shop-Sheets (eine pro Zeile)“

Freigabe der Sheets: „Jeder mit dem Link – Betrachter“ (steht auch als Hinweis unter den Feldern).

### 11.3 Knopf Sheet-Abgleich prüfen (in der Produkt-Datenbank)

Unten in der Karte „Bestand“. Prüft jedes hinterlegte Sheet (währenddessen steht dort „Prüfe Sheets …“) und zeigt ganz unten in der Karte, unter den Knöpfen, pro Sheet eine Zeile:

| Anzeige | Bedeutung |
|---|---|
| „✅ <Name>: <Zahl> ASINs gelesen“ | Sheet lesbar, ASINs gefunden. |
| „⚠️ <Name>: 0 ASINs – Sheet leer oder Format nicht erkannt“ | Sheet lesbar, aber keine ASIN gefunden. Stehen dort wirklich Amazon-Links oder B0-ASINs? |
| „❌ <Name>: nicht lesbar (Freigabe „Jeder mit dem Link – Betrachter"? Makro ohne doGet?)“ | Sheet konnte nicht gelesen werden. Freigabe prüfen; bei der Web-App-Adresse lieber zusätzlich den „Lese-Link“ eintragen. |
| „Keine Sheets hinterlegt. Trage im Tracker das Haupt-Sheet und/oder weitere Shop-Sheets ein.“ | Es ist kein Sheet eingetragen – dann findet kein Abgleich statt. |
| „Insgesamt <Zahl> bereits gelistete ASINs für den Abgleich.“ | Summe über alle lesbaren Sheets. |
| „Fehler: …“ (rot) | Die Extension hat nicht geantwortet. Seite neu laden und erneut prüfen. |

Als Namen erscheinen „Haupt-Sheet (Lese-Link)“, „Haupt-Sheet (Web-App /exec)“ oder „Shop-Sheet 1“, „Shop-Sheet 2“ … Unter jedem Namen steht die eingetragene Adresse.

Nach dieser Prüfung liest der nächste Import die Sheets garantiert frisch ein.

### 11.4 Häufige Fragen und Probleme (Sheet-Abgleich)

**Ein Produkt wurde importiert, obwohl es in meinem Sheet steht.**
Mit „Sheet-Abgleich prüfen“ nachsehen, ob das Sheet lesbar ist und ASINs findet. Ist es „nicht lesbar“, wird es beim Import übergangen. Steht die ASIN im Sheet nur als reine Nummer, die nicht mit „B0“ beginnt, wird sie nicht erkannt – dann als Amazon-Link eintragen. Steht sie auf einem anderen Tabellenblatt als dem im Link, wird sie ebenfalls nicht gefunden (siehe 11.1). Hast du das Sheet gerade erst ergänzt: Cash Lister liest die Sheets höchstens etwa einmal pro Minute neu – kurz warten oder vorher „Sheet-Abgleich prüfen“ klicken. Hast du auf einem anderen Gerät eingesammelt: Sind die Sheets dort im Tracker eingetragen?

**Ich habe kein Google Sheet – geht es trotzdem?**
Ja. Dann entfällt nur dieser Abgleich. Was du mit deinem Konto über Cash Lister gelistet hast, erkennt der Server zusätzlich als „bereits gelistet“ (Abschnitt 3.4). Und der Browser-Lister fängt beim Listen doppelte ASINs ab („Produkt ist schon gelistet (Duplikat)“) – aber nur, wenn das Produkt in **diesem Chrome-Profil** schon einmal erfolgreich mit Cash Lister gelistet wurde. Was du von Hand oder mit einem anderen Programm gelistet hast, erkennt nur der Sheet-Abgleich.

---

## 12. Der Konkurrenz-Scanner

### 12.1 Was macht er?

Der Scanner nimmt die Produkte eines **eBay-Verkäufers** und sucht zu jedem Produkt die **passende Amazon-Quelle**:

1. Er öffnet die Verkäufer-Seite auf eBay und liest die Produkte (Titel, Bild, Preis, ggf. Verkaufszahl).
2. Für jedes Produkt sucht er auf **amazon.de** nach dem eBay-Titel.
3. Er vergleicht das eBay-Bild mit allen Bildern der Amazon-Treffer. Ist ein Bild nahezu gleich, gilt dieses Amazon-Produkt als Quelle.
4. Gibt es mehrere fast gleiche Bilder (dasselbe Produkt von mehreren Anbietern), nimmt er das **günstigste**.
5. Optional prüft er, ob du den Verkäufer mit deinen Preis-Einstellungen sicher unterbieten kannst.
6. Treffer werden **sofort für dich reserviert** und in der Liste „Gefundene Produkte“ gespeichert.

Der Browser-Lister kann diese Funde später listen (Quelle „Konkurrenz-Scanner“). Dabei wird als eBay-Titel **der Titel des Konkurrenten** benutzt (höchstens 80 Zeichen) statt eines KI-Titels.

Der Scanner ist auf **eBay.de und amazon.de** ausgelegt: Er sucht immer auf amazon.de, öffnet Artikelseiten auf ebay.de und liest Preise nur in „EUR“ und Verkaufszahlen nur mit dem Wort „verkauft“. Auf einer eBay-Seite ohne EUR-Preise fehlt deshalb der eBay-Preis – mit eingeschalteter Preisprüfung wird dann jeder Treffer als „Preis unbekannt“ übersprungen. Die Funde werden immer als amazon.de-Produkte gespeichert und gelistet (unabhängig von „Domain“). **Nicht sicher belegt:** ob er auf anderen eBay-Ländern überhaupt brauchbare Ergebnisse liefert – davon ist eher nicht auszugehen.

Er arbeitet nur mit dem, was du auch im Browser siehst: Er öffnet echte Tabs und liest die angezeigten Seiten.

**Wichtig:** Die Funde des Scanners liegen – anders als die Produkt-Datenbank – **nur in diesem Chrome-Profil**, nicht auf dem Server. Deine anderen Geräte sehen sie nicht. Zum Umziehen gibt es „Exportieren (CSV)“ und „Importieren (CSV)“ (Abschnitt 12.6).

### 12.2 So öffnest du ihn

- Seitenleiste → Gruppe „Auswerten“ → „Konkurrenz-Scanner“, oder
- im Browser-Lister bei „Produkte aus“ „Konkurrenz-Scanner“ wählen und „Verwalten“ klicken.

Die Seite heißt „Konkurrenz-Scanner“ (darunter: „Verkäufer scannen und Amazon-Quellen per Bild finden“; Tab-Titel „Cash Lister – Konkurrenz-Scanner“) und hat zwei Karten: „Verkäufer scannen“ und „Gefundene Produkte“. Ohne Anmeldung ist der Eintrag in der Seitenleiste ausgegraut.

### 12.3 Karte Verkäufer scannen

| Feld | Standard | Was es macht | Tipps |
|---|---|---|---|
| „Link zur Verkäufer-Produktseite“ | leer (Beispiel: `https://www.ebay.de/str/verkaeufername`) | Die eBay-Seite, auf der die Produkte des Verkäufers zu sehen sind. Fehlt „https://“, wird es ergänzt. | Füge genau die Seite ein, die die Artikel zeigt (z. B. den eBay-Shop oder die Liste „alle Artikel“ des Verkäufers). Der Scanner baut keine Adresse aus einem Namen. Er blättert mit eBays „Weiter“-Knopf; die Anzahl Artikel pro Seite, die du auf eBay eingestellt hast, bleibt erhalten. |
| „Mind. Verkäufe“ | 0 | 0 = kein Filter. Sonst werden Produkte übersprungen, die weniger oft verkauft wurden. Steht die Zahl nicht auf der Verkäufer-Seite, öffnet der Scanner die Artikelseite und liest sie dort; findet er dort keine Zahl, wird das Produkt übersprungen. | Ein Wert über 0 macht den Scan langsamer, weil zusätzliche Artikelseiten geöffnet werden. |
| „Pause (Sek.)“ | 4 | Wartezeit vor jedem weiteren Produkt einer Seite (vor dem ersten Produkt einer Seite wird nicht gewartet). Vor jedem Seitenwechsel wird doppelt so lange gewartet. 0 = keine Pause. Die Pfeile am Feld gehen in halben Sekunden. | Zu kurze Pausen erhöhen das Risiko, dass Amazon oder eBay Captchas zeigen. |
| „Max. Seiten“ | 3 | Wie viele Seiten des Verkäufers höchstens abgearbeitet werden (das Feld ist für 1 bis 50 gedacht; leer oder 0 wirkt wie 1). | Große Verkäufer haben tausende Artikel – mit wenigen Seiten anfangen. |
| „Nur zeigen, wenn ich den Verkäufer sicher unterbiete“ | an | Übernimmt nur Treffer, bei denen dein späterer Verkaufspreis deutlich unter dem Preis des Konkurrenten liegt. | Siehe Preisprüfung unten. |
| „mindestens … %“ | 10 | Um so viel Prozent musst du günstiger sein … | |
| „und mindestens … €“ | 2.00 | … **und** um so viele Euro. Beide Bedingungen müssen erfüllt sein. | Prozent hilft bei teuren, Euro bei billigen Artikeln. |

**Der Bildabstand ist fest eingestellt.** Wie ähnlich das eBay- und das Amazon-Bild sein müssen, kannst du nicht mehr einstellen (das frühere Feld „Bildabstand max.“ gibt es nicht mehr). Als Treffer zählt ein Bildabstand bis 15 (0 = identisch). In der Liste „Gefundene Produkte“ siehst du bei jedem Fund den gemessenen Abstand.

**Die Preisprüfung:** Dein Preis wird aus dem Amazon-Preis mit deinen Preis-Einstellungen berechnet (Einstellungen → Reiter „Preise & Listing“ → Karte „Preise“: „% Aufschlag“, „Fester Aufschlag (€)“ und – wenn eingeschaltet – „Variable Preise (nach Preisspanne)“) – genauso wie beim Listen, nur **ohne** die „Preisendung“. Der Treffer bleibt nur, wenn dein Preis höchstens „Preis des Konkurrenten minus Prozent“ **und** höchstens „Preis des Konkurrenten minus Euro“ ist. Fehlt der eBay- oder Amazon-Preis, wird der Treffer übersprungen. Gibt es gar keine Aufschlag-Einstellung, wird die Preisprüfung übersprungen und der Treffer trotzdem übernommen (das kommt praktisch nur vor, wenn überhaupt keine Preis-Einstellung gespeichert ist). Ist der Haken „Nur zeigen, wenn ich den Verkäufer sicher unterbiete“ aus, wird gar nicht nach Preisen geprüft.

Alle Felder werden **automatisch gespeichert**, beim nächsten Öffnen wieder eingetragen und mit deinen Einstellungen gesichert (Export-Datei und Sicherung auf dem Server).

**Knöpfe und Anzeigen:**

- „Scan starten“ startet den Scan. Während eines Scans ist er ausgegraut.
- „Stoppen“ (rot, nur während eines Scans klickbar; Hinweis: „Scan stoppen – die Funde bis dahin bleiben in der Liste“) hält den Scan an. Der laufende Schritt wird noch beendet; daneben steht „stoppe …“, im Protokoll „Stopp angefordert – der laufende Schritt wird noch beendet.“ Was bis dahin gefunden wurde, bleibt in der Liste.
- Links daneben ein Fortschrittsbalken, darunter „Produkt 5 von 60: <Titel>“ und rechts eine Statuszeile, z. B. „lese Seite 2 …“, „suche auf Amazon …“, „lese Verkaufszahl (Artikelseite) …“, „blättere auf Seite 3 …“. Am Ende steht dort „Fertig.“ bzw. „Gestoppt.“ und die Bilanz.
- Darunter ein **Protokoll** mit Uhrzeit, das Schritt für Schritt zeigt, was der Scanner tut.
- Rote Fehlermeldungen erscheinen unter dem Protokoll.

### 12.4 Schritt für Schritt: einen Konkurrenten scannen

1. Prüfe in den Einstellungen (Reiter „Preise & Listing“, Karte „Preise“) deine Aufschläge – sonst rechnet die Preisprüfung falsch.
2. Öffne den Konkurrenz-Scanner.
3. Kopiere auf eBay.de die Adresse der Seite, die die Artikel des Verkäufers zeigt, und füge sie bei „Link zur Verkäufer-Produktseite“ ein.
4. Stelle „Mind. Verkäufe“, „Pause (Sek.)“, „Max. Seiten“ und die Preisprüfung ein.
5. Klicke „Scan starten“. Es öffnen sich **zwei Tabs im Vordergrund**: sofort die Verkäufer-Seite und, sobald das erste Produkt nachgeschlagen wird, ein zweiter Tab für Artikelseiten und Amazon-Suchen. So kannst du zusehen.
6. Lass die beiden Tabs in Ruhe, bis der Scan fertig ist. (Navigierst du im Verkäufer-Tab weg, springt der Scanner zurück: „Verkäufer-Tab war verstellt – zurück auf Seite …“.)
7. Am Ende schließen sich beide Tabs. Im Protokoll steht z. B. „Fertig – 12 neue Treffer bei 180 Produkten.“ Zeigten mehrere Angebote auf ein schon gefundenes Produkt, steht dahinter z. B. „(4 Angebote zeigten auf ein bereits gefundenes Produkt)“. Hast du gestoppt: „Gestoppt. 12 neue Treffer bei 180 Produkten.“
8. Prüfe die Treffer in der Karte „Gefundene Produkte“ und entferne falsche mit „Verwerfen“.
9. Im Browser-Lister „Produkte aus“ auf „Konkurrenz-Scanner“ stellen und listen.

Der Scanner fängt **jedes Mal wieder bei der eingefügten Seite** an, er merkt sich keine Stelle (eBay mischt die Reihenfolge, eine gemerkte Stelle wäre unzuverlässig). Schon gefundene Produkte werden dabei erkannt und nicht doppelt gespeichert.

### 12.5 Wichtige Protokollzeilen

| Protokollzeile | Bedeutung |
|---|---|
| „Scan gestartet.“ / „Öffne Verkäufer-Seite: …“ | Start |
| „Seite 1: 60 Produkte gefunden.“ | So viele Produkte stehen auf der Seite. |
| „[5/60] <Titel>“ | Dieses Produkt wird gerade bearbeitet. |
| „── Seite 2 ──“ | Der Scanner hat auf die nächste Verkäufer-Seite geblättert. |
| „Verkäufer-Tab war verstellt – zurück auf Seite ….“ | Der Verkäufer-Tab stand nicht mehr auf der richtigen Seite (z. B. weil du darin geklickt hast); der Scanner hat ihn zurückgestellt. |
| „Noch keine Artikel sichtbar – warte und lese erneut …“ | eBay lädt langsam; der Scanner versucht es nochmal. |
| „Filter „≥ … Verkäufe": … mit sichtbar zu kleiner Zahl aussortiert, … verbleiben.“ | Wirkung von „Mind. Verkäufe“. |
| „Verkaufszahl nicht im Shop → Artikelseite öffnen …“ / „… verkauft.“ / „keine Zahl gefunden → übersprungen (unter …).“ | Verkaufszahl wird auf der Artikelseite nachgelesen. |
| „… Pause 4–6 s …“ | die eingestellte Pause (leicht gestreut) |
| „Amazon-Suche nach dem Titel …“ / „… Amazon-Trefferbilder – vergleiche …“ | Suche und Bildvergleich |
| „… gleiche Bilder – günstigstes genommen: … statt ….“ | Mehrere Anbieter, der günstigste wurde gewählt. |
| „[Daten] best=… zweit=…“ | Bester und zweitbester Bildabstand (zur Einschätzung, wie eindeutig der Treffer ist). |
| „✓ Treffer: <ASIN> (<Preis>) – Bildabstand ….“ (grün) | Treffer gespeichert. |
| „kein identisches Bild (bester Abstand …, nächster: <ASIN>).“ + Zeile „Diagnose Abstand … – eBay-Bild gegen Amazon-Bild (<ASIN>)“ | Kein Treffer. Über die beiden Links kannst du die verglichenen Bilder selbst ansehen. |
| „eBay-Bild nicht ladbar → übersprungen.“ | Bild nicht erreichbar. |
| „Preis unbekannt (eBay oder Amazon) → übersprungen.“ | Für die Preisprüfung fehlt ein Preis. |
| „Keine Aufschlag-Einstellung gefunden – Preisfilter übersprungen.“ | Keine Preis-Einstellungen gespeichert. |
| „Unterbietung zu knapp: mein Preis … € vs. seine … € → übersprungen.“ | Preisprüfung nicht bestanden. |
| „<ASIN> ist schon in der Fundliste (anderes Angebot, gleiches Produkt).“ | Doppelter Treffer. |
| „Schon in der Fundliste – nicht doppelt gespeichert.“ | Das Produkt lag schon in der Liste; es wurde nicht ein zweites Mal gespeichert. |
| „Produkt bereits an einen anderen Nutzer vergeben → übersprungen.“ | Ein anderer Kunde hat das Produkt (Abschnitt 13). |
| „⚠ ohne Reservierung übernommen – die Produkt-Vergabe hat nicht bestätigt.“ (gelb) | Gespeichert, aber nicht für dich reserviert (Abschnitt 13). |
| „Produkt-Vergabe antwortet nicht – Treffer wird trotzdem übernommen.“ | Der Server hat nicht rechtzeitig geantwortet; der Treffer ist gespeichert, aber nicht für dich reserviert (Abschnitt 13). |
| „NICHT gespeichert: …“ (rot) | Speichern fehlgeschlagen. |
| „Seitengrenze erreicht (…).“ | „Max. Seiten“ erreicht. |
| „Kein Weiterblättern: Weiter-Knopf ausgegraut (letzte Seite).“ / „Kein Weiterblättern: kein Weiter-Knopf auf der Seite.“ | Letzte Seite erreicht bzw. eBay-Knopf nicht gefunden. |
| „Stopp angefordert – der laufende Schritt wird noch beendet.“ | Du hast „Stoppen“ geklickt. |
| „Fertig – … neue Treffer bei … Produkten.“ / „Gestoppt. … neue Treffer bei … Produkten.“ | Ende. |
| „FEHLER: …“ (rot) | Der Scan ist abgebrochen; Grund folgt. |

Fehlermeldungen unter dem Protokoll:

| Meldung | Was tun |
|---|---|
| „Bitte den Link zur Verkäufer-Produktseite einfügen.“ | Feld ist leer. |
| „Bitte einen eBay-Link einfügen – die Seite, die die Produkte des Verkäufers zeigt.“ | Die Adresse ist keine eBay-Adresse. |
| „Fehler: Keine Produkte gefunden. Zeigt die eingefügte Seite wirklich die Artikel des Verkäufers?“ | Auf der ersten Seite blieben keine Artikel übrig. Meist wurden keine Artikel erkannt: Seite im Browser öffnen und prüfen; ggf. eine andere Ansicht (alle Artikel des Verkäufers) verwenden. Die Meldung kommt aber **auch**, wenn „Mind. Verkäufe“ auf Seite 1 alle Artikel aussortiert hat (im Protokoll steht dann davor „Filter „≥ … Verkäufe": … aussortiert, 0 verbleiben.“) – dann „Mind. Verkäufe“ senken. |
| „Fehler: …“ mit anderem Text | Oft wurde ein Arbeits-Tab geschlossen. Scan neu starten und die Tabs offen lassen. |

### 12.6 Karte Gefundene Produkte

Oben in der Karte:

- „<Zahl> Produkte warten auf das Listen“
- rechts die Knöpfe „Exportieren (CSV)“, „Importieren (CSV)“ und „Alle verwerfen“ (rot)
- unten der Hinweis: „Der Export nimmt die Produkte aus der Liste und gibt die Vergabe frei – keine Sicherungskopie.“

**Exportieren (CSV)** – zum Weitergeben an einen anderen Rechner:

1. Klick fragt: „<Zahl> Produkte exportieren? Sie werden dabei aus dieser Liste entfernt und die Produkt-Vergabe wird freigegeben – die CSV-Datei ist danach die einzige Kopie. Importiere sie auf dem anderen Rechner, damit die Produkte dort wieder für dich reserviert werden.“
2. Bei „OK“ wird `konkurrenz-funde-<Datum>.csv` heruntergeladen (Spalten „ASIN“, „Titel“, „eBay-Preis“, „Amazon-Preis“, „eBay-ID“, „URL“, getrennt mit Semikolon; öffnet sich direkt in Excel).
3. Danach ist die Liste leer: „<Zahl> Produkte exportiert, aus der Liste entfernt und die Vergabe freigegeben.“
4. Auf dem anderen Rechner sofort importieren, damit die Produkte wieder für dich reserviert werden – in der Zwischenzeit könnte sie ein anderer Kunde greifen.

Bei leerer Liste: „Nichts zu exportieren.“

**Importieren (CSV):**

1. Klick öffnet die Dateiauswahl (.csv oder .txt).
2. Die Datei braucht Semikolon als Trenner. Hat sie eine Kopfzeile mit „ASIN“, werden die Spalten über die Kopfzeile gefunden („ASIN“, „Titel“, „eBay-Preis“, „Amazon-Preis“, „eBay-ID“, „URL“). Ohne Kopfzeile gilt genau diese Reihenfolge.
3. Erst steht dort kurz „lese Datei …“, dann prüft Cash Lister die Vergabe in Blöcken: „prüfe Vergabe … 20 von 85“.
4. Ergebnis z. B.: „80 von 85 übernommen, 3 schon an andere vergeben, 2 waren schon in der Liste.“ Wurden Produkte nicht bestätigt reserviert, steht davor in Orange: „⚠️ … Produkte wurden OHNE Reservierung übernommen – die Produkt-Vergabe hat nicht bestätigt. Sie sind für andere Nutzer weiter frei.“
5. Meldungen bei Problemen: „Datei ist leer.“, „Keine gültigen ASINs in der Datei gefunden.“, „Fehler: …“.

Tipp: Die Spalte „Titel“ wird beim Listen als eBay-Titel benutzt (längere Titel werden auf 80 Zeichen gekürzt). Ist sie leer, erzeugt der Browser-Lister den Titel wie üblich. Fehlt die Spalte „URL“, wird der Link `https://www.amazon.de/dp/<ASIN>` angelegt. Importierte Funde haben keine Bilder und keinen Bildabstand – in der Tabelle bleiben diese Felder leer bzw. zeigen „–“.

**Alle verwerfen:** fragt „Alle gesammelten Funde verwerfen? Die Produkt-Vergabe wird dabei wieder freigegeben.“ und meldet danach „verworfen, Vergabe freigegeben.“ Nicht rückgängig zu machen.

**Die Tabelle** zeigt alle gespeicherten Funde, **die neuesten oben** – auch nach dem Neuladen der Seite und über mehrere Scans hinweg. Sie erscheint, sobald es Funde gibt oder ein Scan gestartet wurde. Während eines Scans steht darüber z. B. „12 neue Treffer in diesem Lauf · 3 schon in der Liste · 40 ohne identisches Bild · 5 unter Mindestverkäufen“.

Spalten (die Überschriften werden in Großbuchstaben angezeigt):

| Spalte | Inhalt |
|---|---|
| (Bild) | Bild des eBay-Angebots |
| „eBay-Produkt“ | Titel des Konkurrenten (Klick öffnet das eBay-Angebot), darunter ggf. „<Zahl> verkauft“ |
| „Verkäufer-Preis“ | Preis des Konkurrenten |
| (Bild) | Bild des Amazon-Treffers |
| „Amazon-Quelle“ | ASIN (Klick öffnet Amazon), darunter der Anfang des Amazon-Titels |
| „Amazon-Preis“ | Amazon-Preis, dahinter grün „+X,XX €“ = Verkäufer-Preis minus Amazon-Preis. Das ist der **Preisabstand beim Konkurrenten**, nicht dein Gewinn (Gebühren, Steuern und deine Aufschläge sind nicht berücksichtigt). Ist Amazon teurer als der Konkurrent (kommt praktisch nur ohne Preisprüfung vor), steht dort ein Minusbetrag in der Form „+-1,50 €“. Fehlt einer der beiden Preise, steht kein grüner Betrag da. |
| „Bildabstand“ | „identisch“ bei 0, sonst die Zahl; „–“ bei Funden aus einer CSV-Datei |
| (Knopf) „Verwerfen“ | entfernt diesen Fund sofort (ohne Rückfrage) und gibt seine Reservierung frei |

Ist die Fundliste nicht lesbar, steht „Fundliste nicht lesbar: …“ und als Anzahl „?“ – Seite neu laden.

### 12.7 Häufige Fragen (Konkurrenz-Scanner)

**Funktioniert der Scanner mit eBay.com oder amazon.co.uk?**
Er ist auf eBay.de und amazon.de ausgelegt (Amazon-Suche immer auf amazon.de, Preise in EUR). Für andere Länder ist er nicht gedacht.

**Kann ich einstellen, wie ähnlich die Bilder sein müssen?**
Nein, nicht mehr. Der Bildabstand ist fest eingestellt (Treffer bis 15). Falsche Treffer entfernst du mit „Verwerfen“.

**Werden die Funde nach meinen Amazon-Filtern (Sterne, Lieferzeit, Lager …) gefiltert?**
Nein, nicht beim Scannen. Preisgrenzen, Lieferzeit, Versand usw. prüft erst der Browser-Lister beim Listen.

**Gibt es beim Scanner einen Sheet-Abgleich?**
Nein. Der Browser-Lister erkennt aber beim Listen, wenn du eine ASIN in diesem Chrome-Profil schon gelistet hast („Produkt ist schon gelistet (Duplikat)“).

**Wird beim Listen der Titel des Konkurrenten benutzt?**
Ja, wenn der Lauf seine Produkte aus „Konkurrenz-Scanner“ nimmt. Achte selbst darauf, dass der Titel keine geschützten Markennamen oder unpassenden Angaben enthält.

**Kann ich den Scanner nebenbei laufen lassen?**
Ja, aber die beiden Arbeits-Tabs öffnen sich im Vordergrund und müssen offen bleiben. Ein Scan über mehrere Seiten kann lange dauern.

**Bleiben die Funde erhalten, wenn ich die Seite schließe?**
Ja. Sie werden gespeichert und erscheinen beim nächsten Öffnen wieder. Sie sind aber nur in diesem Chrome-Profil gespeichert – nicht auf dem Server, nicht auf deinen anderen Geräten und nicht in „Einstellungen exportieren“. Zum Umziehen „Exportieren (CSV)“ benutzen.

**Landen die Funde in der Produkt-Datenbank?**
Nein. Funde und Produkt-Datenbank sind zwei getrennte Vorräte. Im Browser-Lister wählst du, aus welchem ein Lauf nimmt.

**Was ist der Unterschied zwischen „Verwerfen“ und dem Listen?**
„Verwerfen“ entfernt den Fund und gibt die Reservierung frei. Beim Listen nimmt der Browser-Lister den Fund aus der Liste; klappt das Listing, bleibt die Reservierung bestehen und wird bestätigt. Scheitert es, ist der Fund trotzdem aus der Liste weg, und die Reservierung wird freigegeben.

### 12.8 Probleme und Lösungen (Konkurrenz-Scanner)

| Problem | Lösung |
|---|---|
| Nach der ersten Seite hört der Scan auf. | „Max. Seiten“ prüfen. Steht im Protokoll „Kein Weiterblättern: …“, hat eBay keine weitere Seite oder der Weiter-Knopf wurde nicht gefunden. |
| Fast nur „kein identisches Bild“. | eBay-Verkäufer nutzen oft eigene Fotos – dann gibt es kein passendes Amazon-Bild. Der Bildabstand ist fest; über die „Diagnose“-Links im Protokoll kannst du die Bilder vergleichen. Probier einen anderen Verkäufer. |
| Falsche Treffer (anderes Produkt). | Falsche Funde mit „Verwerfen“ entfernen. Ein Blick auf die Spalte „Bildabstand“ hilft: Je kleiner die Zahl, desto sicherer der Treffer. |
| Fast alles „Unterbietung zu knapp“. | „mindestens … %“ / „und mindestens … €“ senken, die Preisprüfung ausschalten oder deine Aufschläge in den Einstellungen (Reiter „Preise & Listing“) prüfen. |
| „Mind. Verkäufe“ scheint nicht zu wirken. | Der Wert muss größer als 0 sein. Produkte ohne sichtbare Zahl werden auf der Artikelseite nachgelesen; ohne Zahl werden sie übersprungen. |
| Im Protokoll steht immer wieder „0 Amazon-Trefferbilder – vergleiche …“. | Der Scanner erkennt Captchas nicht von selbst: Zeigt Amazon im zweiten Arbeits-Tab ein Captcha, findet er einfach keine Treffer und macht weiter. Schau in den Arbeits-Tab, löse das Captcha dort; die folgenden Produkte laufen dann wieder normal. Die betroffenen Produkte zählen als „ohne identisches Bild“ – starte den Scan später erneut, schon Gefundenes wird nicht doppelt gespeichert. „Pause (Sek.)“ erhöhen, damit es seltener passiert. |
| Captcha auf der eBay-Verkäuferseite. | Dann findet der Scanner auf Seite 1 keine Artikel („Keine Produkte gefunden …“). Seite im Browser öffnen, Captcha lösen, Scan neu starten. |
| „Stoppen“ reagiert nicht sofort. | Der laufende Schritt wird noch beendet; das kann einen Moment dauern. |
| Viele „ohne Reservierung übernommen“. | Siehe Abschnitt 13 (Anmeldung und Verbindung prüfen). Danach die betroffenen Funde verwerfen und den Scan wiederholen. |
| Meine Funde sind auf dem anderen Rechner nicht da. | Richtig – die Funde liegen nur in diesem Chrome-Profil. Mit „Exportieren (CSV)“ und „Importieren (CSV)“ umziehen. |

---

## 13. Produktvergabe: damit nicht zwei Kunden dasselbe Produkt listen

### 13.1 Was ist das?

Alle Kunden von Cash Lister melden dem Server, welche Amazon-Produkte sie bearbeiten. Ist ein Produkt vergeben, bekommen weitere Kunden es nicht mehr. So entstehen keine doppelten Angebote desselben Produkts von mehreren Kunden.

Für dein **eigenes** Konto ist ein Produkt, das du schon reserviert hast, nie „belegt“ – auch nicht auf einem anderen Gerät mit demselben Konto.

Die Produktvergabe läuft **über deine Anmeldung**.

- **Produkt-Datenbank:** Sie baut direkt auf der Produktvergabe auf. Jedes Produkt in deiner Produkt-Datenbank ist für dein Konto reserviert. Ohne Anmeldung oder ohne Server kommt **nichts** hinein – es gibt dort also keine Produkte „ohne Reservierung“ mehr.
- **Konkurrenz-Scanner:** Er reserviert jeden Fund einzeln. Antwortet der Server nicht (oder bist du nicht angemeldet), übernimmt er den Fund trotzdem – dann aber **ohne** Reservierung, mit einer Warnung im Protokoll bzw. beim CSV-Import. In den Einstellungen steht dazu: „Achtung: Ohne Anmeldung ist die Produkt-Vergabe komplett aus.“ und „Es kommt keine Fehlermeldung – es wird dann einfach nichts mehr reserviert.“

### 13.2 Wann wird reserviert, wann freigegeben?

| Ereignis | Was mit der Reservierung passiert |
|---|---|
| Produkt kommt in die Produkt-Datenbank (Amazon-Knopf, „Ganzer Shop“, von Hand, Übertragung der alten Liste) | wird für dich reserviert (ohne Server: Produkt kommt gar nicht hinein) |
| Konkurrenz-Scanner findet ein Produkt / Import einer Scanner-CSV | wird für dich reserviert (ohne Server: Fund ohne Reservierung, mit Warnung) |
| Browser-Lister listet das Produkt erfolgreich | Reservierung wird bestätigt (dein Angebot ist online) |
| Browser-Lister scheitert beim Listen | wird freigegeben |
| „✕“ in der Produkt-Datenbank / „Alle löschen“ (nur freie Produkte) | wird freigegeben |
| „Verwerfen“ / „Alle verwerfen“ / „Exportieren (CSV)“ im Scanner | wird freigegeben |
| „Als TXT exportieren“ in der Produkt-Datenbank | bleibt bestehen |

Beim Listen von **Scanner-Funden** prüft der Browser-Lister die Vergabe noch einmal. Hat inzwischen ein anderer Kunde das Produkt, wird es übersprungen: „Produkt bereits von einem anderen Nutzer vergeben“ im Statusbericht. War der Fund noch nicht für dich reserviert und ist das Produkt noch frei, wird es bei dieser Prüfung für dich reserviert. Produkte aus der **Produkt-Datenbank** sind seit dem Import reserviert; dort entfällt diese zweite Prüfung.

**Nicht sicher belegt:** wie lange eine Reservierung hält, wenn du ein Produkt lange liegen lässt und nie listest, und wann der Server Reservierungen von Konten freigibt, die nicht mehr arbeiten. Das legt der Betreiber fest – frag ihn bei Bedarf.

### 13.3 Was du davon siehst

| Wo | Was du siehst, wenn ein anderer Kunde das Produkt hat | Wenn nicht reserviert werden konnte |
|---|---|---|
| Amazon-Suchseite (blauer Knopf) | „… von anderen Kunden belegt“ in der Meldung | „❌ Bitte zuerst in Cash Lister anmelden – nichts importiert.“ bzw. „❌ Nichts importiert – Server nicht erreichbar …“ – es wird nichts gespeichert |
| „Ganzer Shop“ | „… von anderen Kunden belegt.“ | wie oben |
| Produkt-Datenbank, „Links hinzufügen“ | „…, … belegt (hat schon ein anderer Kunde)“ | „Nichts importiert – …“ – es wird nichts gespeichert |
| Konkurrenz-Scanner (Scan) | Protokoll: „Produkt bereits an einen anderen Nutzer vergeben → übersprungen.“ | Protokoll: „⚠ ohne Reservierung übernommen …“ bzw. „Produkt-Vergabe antwortet nicht – Treffer wird trotzdem übernommen.“ |
| Konkurrenz-Scanner (CSV-Import) | „…, … schon an andere vergeben“ | orange „⚠️ … OHNE Reservierung übernommen …“ |
| Browser-Lister (nur Scanner-Funde) | Statusbericht: „Produkt bereits von einem anderen Nutzer vergeben“ | – |

Produkte, die ein anderer Kunde hat, landen gar nicht erst in deinen Vorräten. Du siehst auch nicht, **welcher** Kunde sie hat.

### 13.4 So prüfst du, ob die Produktvergabe bei dir aktiv ist

**Schnell:** Unten in der Seitenleiste (auf jeder Seite von Cash Lister) steht der Stand:

| Anzeige unten in der Seitenleiste | Bedeutung |
|---|---|
| „Server verbunden“ / „angemeldet als …“ / „Produkt-Vergabe aktiv“ | alles gut |
| „Nicht angemeldet“ / „Produkt-Vergabe aus“ | im Dashboard anmelden |
| „Server nicht erreicht“ / „Lister nehmen keine Produkte“ | Server antwortet gerade nicht; Import in die Produkt-Datenbank geht nicht, der Browser-Lister wartet |
| „Zugang abgeschaltet“ / „Produkt-Vergabe aus“ | an den Betreiber wenden |
| „Abo gesperrt“ / „Details im Dashboard“ / „Produkt-Vergabe aus“ | siehe Karte „Dein Abo“ im Dashboard und `references/konto-und-installation.md` |

**Genauer:**

1. Einstellungen öffnen (Seitenleiste → „Einstellungen“).
2. Reiter „eBay & Rahmenbedingungen“ wählen, Karte „Server & Produkt-Vergabe“ (Hinweis daneben: „verhindert doppeltes Listen“).
3. Die Statuszeile lesen:
   - „● Produkt-Vergabe: AN (über deine Anmeldung)“ – alles gut.
   - „● Produkt-Vergabe: AUS – nicht angemeldet. Es wird NICHTS reserviert!“ – im Dashboard anmelden.
   - „● Produkt-Vergabe: AUS – keine Server-Adresse hinterlegt.“ – **trotz des Wortlauts heißt das in der Praxis meist: du bist nicht angemeldet.** Im Dashboard anmelden, dann die Einstellungsseite neu laden (F5). Steht der Text trotz Anmeldung noch da, an den Betreiber wenden. Selbst keine Adresse eintragen.
4. Auf „Verbindung prüfen“ klicken. Während der Prüfung steht dort „prüfe …“, danach eins davon:
   - „OK – angemeldet als „<Name>“, <Zahl> Produkte reserviert.“ – alles gut; die Zahl zeigt, wie viele Produkte für dich reserviert sind.
   - „Nicht angemeldet – bitte im Dashboard anmelden.“ – im Dashboard anmelden.
   - „Keine Server-Adresse hinterlegt.“ – heißt in der Praxis ebenfalls meist: nicht angemeldet. Im Dashboard anmelden, Seite neu laden, erneut prüfen. Bleibt es trotz Anmeldung, an den Betreiber wenden.
   - „Anmeldung abgelehnt (401) – bitte im Dashboard neu anmelden.“ – im Dashboard abmelden und neu anmelden.
   - „Zugang ist abgeschaltet (403).“ – an den Betreiber wenden (bei gesperrtem Abo siehe Dashboard).
   - „Keine Antwort: …“ oder „Server antwortet mit HTTP …“ – Internetverbindung prüfen; bleibt es so, an den Betreiber wenden.
   - eine andere, hier nicht genannte Meldung – an den Betreiber wenden.

   Eine zweite Zeile mit technischen Angaben brauchst du nicht zu beachten; nenne sie dem Betreiber, wenn er danach fragt.

Das Feld „Server-Adresse“ (in dieser Karte und im Dashboard unter „Server-Adresse (nur auf Ansage ändern)“) bitte **nicht ändern** – nur, wenn der Betreiber es dir ausdrücklich sagt.

### 13.5 Häufige Fragen (Produktvergabe)

**Warum sind so viele Produkte „belegt“?**
Andere Kunden haben sie vor dir eingesammelt. Das ist der Zweck der Vergabe: Es soll nicht mehrere Kunden mit demselben Produkt geben.

**Kann ich ein belegtes Produkt trotzdem bekommen?**
Nein, nicht über Cash Lister. Erst wenn der andere Kunde es freigibt (z. B. weil er es löscht oder das Listen scheitert), ist es wieder frei.

**Ich lösche Produkte aus der Datenbank – sind die dann für andere frei?**
Ja. Löschen („✕“, „Alle löschen“) gibt die Reservierung frei.

**Kann ich ohne Anmeldung einsammeln und später reservieren?**
Nein, nicht in der Produkt-Datenbank: Ohne Anmeldung wird dort gar nichts gespeichert. Erst anmelden, dann einsammeln.

**Gilt meine Reservierung auch auf meinem zweiten Rechner?**
Ja. Die Reservierung hängt an deinem Konto, nicht am Rechner – und die Produkt-Datenbank ist auf beiden Rechnern dieselbe.

### 13.6 Probleme und Lösungen (Produktvergabe)

| Problem | Lösung |
|---|---|
| Plötzlich ist **jedes** Produkt „belegt“. | Das ist ungewöhnlich. Stand in den Einstellungen prüfen und „Verbindung prüfen“ klicken; Ergebnis dem Betreiber mitteilen. |
| Konkurrenz-Scanner: viele „ohne Reservierung übernommen“. | Anmeldung prüfen (13.4). Bei „OK – angemeldet …“ und trotzdem Warnung: an den Betreiber wenden. Betroffene Funde verwerfen und neu scannen. |
| Import in die Produkt-Datenbank klappt gar nicht („Nichts importiert …“). | Anmeldung und Verbindung prüfen (13.4). Läuft der Server wieder, noch einmal importieren. |

---

## 14. eBay-Artikelseiten: die violette Lupe

### 14.1 Was ist das?

Auf eBay-Angebotsseiten (Adresse mit `/itm/`) erscheint **vor dem Titel eine kleine violette Lupe**, wenn das Angebot **mit Cash Lister gelistet** wurde. Beim Darüberfahren steht dort „Amazon-Produkt öffnen“. Ein Klick öffnet das zugehörige Amazon-Produkt in einem neuen Tab.

So findest du von deinem eBay-Angebot schnell zurück zur Amazon-Quelle – z. B. um Preis oder Lieferbarkeit zu prüfen.

### 14.2 Wann erscheint die Lupe?

- Nur bei Angeboten, deren „Bestandseinheit“ / „Custom label (SKU)“ die von Cash Lister eingetragene Kennung enthält (endet auf „==“).
- eBay zeigt diese Angabe normalerweise **nur dir als Verkäufer**, wenn du bei eBay angemeldet bist – z. B. in den Artikelmerkmalen oder im Verkäufer-Kasten „Angebotsinformationen“. Bei fremden Angeboten erscheint deshalb keine Lupe.
- Die Lupe wird eingefügt, sobald eBay die Seite fertig nachgeladen hat (Cash Lister wartet bis zu 10 Sekunden).

Welches Amazon-Land geöffnet wird, richtet sich nach der Einstellung „Domain“ (Abschnitt 7; bei „Keine“ oder ungültigem Wert: amazon.de). Änderst du die Domain, passt sich eine schon angezeigte Lupe sofort an.

### 14.3 Häufige Fragen und Probleme (Lupe)

| Frage / Problem | Antwort / Lösung |
|---|---|
| Die Lupe fehlt bei meinem Angebot. | Bist du bei eBay als Verkäufer dieses Angebots angemeldet? Wurde das Angebot mit Cash Lister gelistet (Bestandseinheit endet auf „==“)? Seite neu laden. **Nicht sicher belegt:** ob eBay die Bestandseinheit auf jeder Seitenvariante anzeigt – fehlt sie auf der Seite, kann Cash Lister keine Lupe zeigen. |
| Die Lupe öffnet das falsche Amazon-Land. | „Domain“ richtig einstellen (Abschnitt 7). |
| Bei Angeboten anderer Verkäufer gibt es keine Lupe. | Richtig – die Lupe gibt es nur für deine eigenen, mit Cash Lister gelisteten Angebote. |

---

## 15. Was dieser Bereich nicht kann

Damit du keine falschen Erwartungen hast – folgende Dinge gibt es **nicht**:

- Kein Listen direkt von der Amazon-Produktseite und kein „zur Datenbank“-Knopf auf der Produktseite.
- Keine Suche, kein Filter und keine Sortierung per Spaltenkopf in der Produkt-Datenbank; keine Möglichkeit, Titel oder Preise dort vorzugeben; kein Nach-oben-Schieben einzelner Produkte.
- Kein Amazon-Land pro Produkt in der Produkt-Datenbank – das Land kommt immer aus „Domain“.
- Keine getrennten Listen je Gerät oder je Shop: eine Produkt-Datenbank je Konto.
- Kein Import in die Produkt-Datenbank ohne Anmeldung oder ohne erreichbaren Server.
- Kein automatischer Abgleich der **Scanner-Funde** zwischen mehreren Rechnern (die liegen nur im Chrome-Profil).
- Keine Anzeige, welcher andere Kunde ein Produkt reserviert hat.
- „nur Verkauf durch Amazon“ nicht im Verkäufer-Schaufenster und nicht bei „Ganzer Shop“.
- Sterne-, Bewertungs- und Lagerfilter nur beim Einsammeln auf Amazon-Suchseiten.
- Konkurrenz-Scanner nur für eBay.de/amazon.de; kein einstellbarer Bildabstand.
- Kein „Ganzer Shop“ bei der normalen Amazon-Suche und höchstens 30 Seiten pro Klick im Schaufenster.
- Keine Helfer auf anderen Shop-Seiten: Cash Lister blendet nur auf Amazon (Suchseiten, Produktseiten) und auf eBay-Artikelseiten etwas ein.
- Keine VeRO-Prüfung. Willst du bestimmte Marken meiden, trag sie in die Blacklist ein (Einstellungen → „Produkt-Filter“ → „Meine Liste“) – dann warnt die Produktseite und der Browser-Lister überspringt solche Produkte.

Wenn ein Kunde nach einer Funktion fragt, die hier nicht beschrieben ist: offen sagen, dass sie in diesem Bereich nicht dokumentiert ist, und an den Betreiber verweisen.

---

## 16. Neu in Version 46.0

Das findet ein Kunde der Vorversion in diesem Bereich jetzt anders:

**Öffnen und Bedienen**

- Das kleine Fenster beim Klick auf das Cash-Lister-Symbol gibt es nicht mehr – es öffnet sich das Dashboard. „Produkt-Datenbank“ und „Konkurrenz-Scanner“ öffnest du über die **Seitenleiste** (oder im Dashboard über „Produkte sammeln“ bzw. im Browser-Lister über „Verwalten“). Jede Seite öffnet sich im eigenen Tab; ist sie schon offen, springt der Klick dorthin.
- Der „Bulk-Lister“ heißt jetzt **Browser-Lister**, der „CSV Tracker“ heißt **Tracker**. Das Feld „Threads:“ im Tracker heißt jetzt „Gleichzeitig“ (es bestimmt weiterhin die Tabs für „nur Verkauf durch Amazon“).
- Den **CSV-Lister** sehen jetzt alle Kunden (Seitenleiste → „Arbeiten“). Er nimmt seine Produkte ebenfalls aus der Produkt-Datenbank; die Produkte, die er gerade hat, stehen dort in der Spalte „In Arbeit“ mit „CSV-Lister“.

**Produkt-Datenbank**

- Sie liegt jetzt **auf dem Server, je Konto** – alle deine Geräte sehen dieselbe Liste. Beim ersten Start wird deine alte Liste automatisch hochgeladen.
- Neue Spalte **„In Arbeit“**, oben die Zahlen „… Produkte · … frei · … in Arbeit“.
- Ohne Anmeldung oder Server: roter Kasten statt Liste; Importieren scheitert mit Meldung (die Links bleiben im Feld). Die orange Warnung „OHNE Reservierung aufgenommen“ gibt es hier nicht mehr.
- Ergebnis-Meldung beim Hinzufügen neu formuliert: „schon drin“, „schon gelistet“, „belegt (hat schon ein anderer Kunde)“. „Schon gelistet“ erkennt jetzt auch, was du mit deinem Konto schon gelistet hast.
- „✕“ fragt nach, wenn das Produkt „In Arbeit“ ist; „Alle löschen“ lässt Produkte „In Arbeit“ stehen und gilt für alle Geräte.
- Spalte „Quelle“ zeigt jetzt „Links“, „Amazon-Suche“, „Schaufenster“.
- Das Amazon-Land kommt bei **allen** Produkten aus der Einstellung „Domain“ (nicht mehr aus dem eingefügten Link).
- „Sortierung“ gilt nur noch für das jeweilige Gerät.
- „Einstellungen exportieren“ nimmt die Produkt-Datenbank nicht mehr mit; eine alte Datei mit Produkt-Datenbank **ergänzt** beim Import die Liste auf dem Server, statt sie zu ersetzen.

**Amazon-Seiten**

- Der Knopf auf Suchseiten meldet „… von anderen Kunden belegt“ und „bereits gelistet“ (ohne „(Sheets)“) und neue Fehlermeldungen, wenn du nicht angemeldet bist oder der Server fehlt. Der Hinweis beim Darüberfahren verweist auf die neuen Namen der Filter.
- Die Amazon-Filter stehen jetzt in den Einstellungen im Reiter **„Produkt-Filter“**, Karte „Amazon-Filter“, mit deutschen Namen („Max. verlängerte Lieferzeit“, „Mind. Sterne“, „Mind. Bewertungen“, „Mind. Lagerbestand“, „Preis ab“, „Preis bis“, „Nur Verkauf durch Amazon“). Die Felder „Min Price (AutoList):“/„Max Price (AutoList):“ im alten Fenster gibt es nicht mehr.
- „Domain“ steht jetzt in den Einstellungen, Reiter „Preise & Listing“, Karte „Listing“ („Keine“ statt „None“).
- Die Warnungen im Tab-Titel sind jetzt **deutsch** (z. B. „WARNUNG! NICHT AUF LAGER - ZUM LISTEN BESTÄTIGEN -“ statt „WARNING! NOT IN STOCK - CONFIRM TO LIST-“), ebenso die Gründe im Statusbericht.
- Der eBay-Suchknopf am Produkttitel heißt beim Darüberfahren „Diesen Artikel bei eBay suchen“.
- Die Blacklist heißt in den Einstellungen „Meine Liste“ (Reiter „Produkt-Filter“, Karte „Blacklist“).

**Konkurrenz-Scanner**

- Das Feld „Bildabstand max.“ ist weg – der Bildabstand ist fest eingestellt.
- Die Knöpfe heißen „Scan starten“ und „Stoppen“; die Karten heißen „Verkäufer scannen“ und „Gefundene Produkte“; die Spalte „eBay-Preis“ heißt „Verkäufer-Preis“, der Knopf je Zeile „Verwerfen“. Am Ende eines gestoppten Scans steht „Gestoppt.“ statt „Abgebrochen.“
