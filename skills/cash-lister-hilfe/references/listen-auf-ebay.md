# Listen auf eBay – der Browser-Lister

Dieser Bereich erklärt, wie du mit dem **Browser-Lister** Produkte aus deiner Produkt-Datenbank oder aus dem Konkurrenz-Scanner automatisch als Angebote auf eBay einstellst. Bis Version 45.5 hieß er „Bulk-Lister“. Beschrieben sind jede Einstellung, jeder Knopf und jeder Schritt auf Amazon und eBay. Dazu kommt, wie der Browser-Lister mit der gemeinsamen Produkt-Datenbank deines Kontos arbeitet („In Arbeit“, mehrere Geräte, Server-Ausfall), und jede Meldung, die du dabei sehen kannst.

Stand: Version 46.3.

> Hinweis für die Antwort: Wo in diesem Text **Nicht sicher belegt:** steht, ist die Sache nicht sicher geklärt. Sag das dem Kunden offen und verweise bei Bedarf an den Betreiber. Nichts dazuerfinden.

## Inhaltsverzeichnis

1. [Wichtige Begriffe kurz erklärt](#1-wichtige-begriffe-kurz-erklärt)
2. [Was der Browser-Lister macht – in einem Absatz](#2-was-der-browser-lister-macht--in-einem-absatz)
3. [Bevor du startest: Checkliste](#3-bevor-du-startest-checkliste)
4. [Browser-Lister öffnen und Aufbau der Seite](#4-browser-lister-öffnen-und-aufbau-der-seite)
5. [Alle Bedienelemente im Einzelnen](#5-alle-bedienelemente-im-einzelnen)
6. [Die Produkt-Datenbank beim Listen: Entnahme, „In Arbeit“, Server-Ausfall](#6-die-produkt-datenbank-beim-listen-entnahme-in-arbeit-server-ausfall)
7. [Schritt-für-Schritt-Anleitungen](#7-schritt-für-schritt-anleitungen)
8. [Was während eines Laufs passiert](#8-was-während-eines-laufs-passiert)
9. [Prüfungen auf der Amazon-Seite vor dem Listen (Buybox/FBA und mehr)](#9-prüfungen-auf-der-amazon-seite-vor-dem-listen-buyboxfba-und-mehr)
10. [Titel](#10-titel)
11. [Beschreibung](#11-beschreibung)
12. [Artikelmerkmale](#12-artikelmerkmale)
13. [Custom Label / SKU](#13-custom-label--sku)
14. [Bilder](#14-bilder)
15. [Preis beim Listen](#15-preis-beim-listen)
16. [Zustand: „Neu“ oder „Neu: Sonstige“](#16-zustand-neu-oder-neu-sonstige)
17. [Weitere Dinge, die im eBay-Formular passieren](#17-weitere-dinge-die-im-ebay-formular-passieren)
18. [Absenden, Angebotsgebühren und Erfolg](#18-absenden-angebotsgebühren-und-erfolg)
19. [Produktvergabe beim Listen](#19-produktvergabe-beim-listen)
20. [Doppelte Angebote vermeiden](#20-doppelte-angebote-vermeiden)
21. [eBay-Verkaufslimit](#21-ebay-verkaufslimit)
22. [Sicherheitsabfragen (Captcha) bei Amazon und eBay](#22-sicherheitsabfragen-captcha-bei-amazon-und-ebay)
23. [Der Statusbericht und alle Meldungen](#23-der-statusbericht-und-alle-meldungen)
24. [Tab-Titel und Tab-Symbole während des Listens](#24-tab-titel-und-tab-symbole-während-des-listens)
25. [Häufige Fragen](#25-häufige-fragen)
26. [Probleme und Lösungen](#26-probleme-und-lösungen)
27. [Neu in Version 46.0](#27-neu-in-version-460)
28. [Was dieser Bereich nicht sicher beantworten kann](#28-was-dieser-bereich-nicht-sicher-beantworten-kann)

---

## 1. Wichtige Begriffe kurz erklärt

- **ASIN**: Die zehnstellige Produktnummer von Amazon (z. B. `B09HGQQ5B6`). Jedes Amazon-Produkt hat eine. Sie steht im Amazon-Link hinter `/dp/`.
- **Buybox**: Der Kaufkasten rechts auf der Amazon-Produktseite (mit „In den Einkaufswagen“). Dort steht, wer verkauft und wer versendet.
- **FBA** („Fulfillment by Amazon“, Versand durch Amazon): Ein Händler verkauft auf Amazon, aber Amazon lagert und verschickt die Ware. Für den Browser-Lister zählt auch „Amazon verkauft und verschickt selbst“ als Versand durch Amazon.
- **SKU / Custom Label**: Eine eigene Kennung, die jedes eBay-Angebot haben kann. Auf eBay heißt das Feld „Custom label (SKU)“, auf eBay.de „Bestandseinheit“. Der Browser-Lister trägt dort eine eigene Kennung ein, sie endet auf „==“ (siehe [Abschnitt 13](#13-custom-label--sku)).
- **VeRO**: eBays Programm, mit dem Markeninhaber Angebote mit ihren Marken entfernen lassen können. Eine eigene VeRO-Prüfung hat die Extension nicht (mehr).
- **GPSR**: EU-Produktsicherheitsverordnung. Sie verlangt Angaben zum Hersteller und zur verantwortlichen Person in der EU.
- **„Gleichzeitig“** (früher „Thread Count“): Wie viele Produkte der Browser-Lister zur selben Zeit bearbeitet. Jeder dieser parallelen Durchgänge listet ein Produkt nach dem anderen.
- **Artikelmerkmale** (auf eBay „Item Specifics“): Die Felder im eBay-Formular wie Marke, Farbe, Material usw.
- **Promoted Listing / Anzeigengebühr**: Bezahlte Anzeigenplatzierung bei eBay. eBay nimmt bei einem Verkauf über die Anzeige einen Prozentsatz.
- **Neu: Sonstige**: eBay-Artikelzustand „Neu: Sonstige (siehe Artikelbeschreibung)“.
- **Produkt-Datenbank**: Deine Liste gesammelter Produkte, die noch gelistet werden sollen. Sie liegt seit Version 46.0 **je Konto auf dem Server**. Alle Geräte, auf denen du mit demselben Konto angemeldet bist, sehen dieselbe Liste.
- **„In Arbeit“**: Ein Produkt der Produkt-Datenbank, das gerade ein Gerät (oder der CSV-Lister) zum Listen genommen hat. Andere Geräte bekommen es so lange nicht.
- **Dashboard**: Die Startseite von Cash Lister. Sie öffnet sich, wenn du auf das Cash-Lister-Symbol in Chrome klickst. Dort meldest du dich an.
- **Seitenleiste**: Die Leiste links auf jeder Cash-Lister-Seite mit den Modulen (z. B. „Browser-Lister“, „Produkt-Datenbank“, „Einstellungen“), unten mit dem Serverstatus und der Versionsnummer.
- **Statusbericht** (früher „Status Report“): Die Liste mit dem Ergebnis jedes Produkts des aktuellen bzw. letzten Laufs.
- **Lauf**: Ein Durchgang des Browser-Listers vom Klick auf „Starten“ bis zum Ende.

## 2. Was der Browser-Lister macht – in einem Absatz

Du sagst dem Browser-Lister, **woher** er die Produkte nehmen soll (Produkt-Datenbank oder Konkurrenz-Scanner) und **wie viele Angebote** am Ende entstehen sollen. Dann klickst du auf „Starten“. Der Browser-Lister nimmt sich Produkt für Produkt aus der gewählten Quelle. Bei der Produkt-Datenbank ist das Produkt dann „In Arbeit“, kein anderes Gerät bekommt es. Für jedes Produkt öffnet er im Hintergrund einen Amazon-Tab (Prüfungen, Daten, Bilder, Preis, KI-Titel) und danach einen eBay-Tab. Dort füllt er das Formular aus und stellt das Angebot ein. Fehlgeschlagene Produkte zählen nicht mit: Der Lauf holt so lange neue Produkte nach, bis die gewünschte Zahl erreicht oder die Quelle leer ist. Das Ergebnis jedes Produkts steht im „Statusbericht“. Ist der Server nicht erreichbar, wartet der Browser-Lister und macht von selbst weiter, sobald der Server wieder antwortet.

## 3. Bevor du startest: Checkliste

1. **Im Dashboard angemeldet?** Klick auf das Cash-Lister-Symbol in Chrome. Es öffnet sich das Dashboard. Steht dort „Nicht angemeldet“ und das Anmeldeformular, melde dich mit „Benutzername“ und „Passwort“ über „Anmelden“ an. Angemeldet zeigt die Seitenleiste unten „Server verbunden“ und „angemeldet als …“. Ohne Anmeldung sind die Module in der Seitenleiste grau, und „Starten“ meldet „Nicht angemeldet oder Zugang deaktiviert - bitte im Dashboard anmelden.“ Mehr zur Anmeldung: `references/konto-und-installation.md`.
2. **Abo in Ordnung?** Cash Lister läuft als Monatsabo. Ist dein Abo gesperrt, steht in der Seitenleiste „Abo gesperrt“, und „Starten“ startet keinen Lauf. Den Stand siehst du im Dashboard in der Karte „Dein Abo“. Alles zum Abo: `references/konto-und-installation.md`.
3. **Domain gewählt?** In den Einstellungen, Reiter „Preise & Listing“, Karte „Listing“, Feld „Domain“ (darunter klein: „eBay-Seite, z. B. DE = ebay.de“). Hier wählst du den eBay-Marktplatz: „USA“, „CA“, „UK“, „AU“, „DE“, „FR“, „IT“, „ES“ oder „NL“. **Wichtig:** Bei Produkten aus der Produkt-Datenbank bestimmt dieselbe Einstellung auch, welche Amazon-Seite geöffnet wird (z. B. „DE“ → amazon.de, „USA“ → amazon.com). „Keine“ nicht stehen lassen.
4. **Bei eBay angemeldet?** Du musst im selben Chrome-Profil bei eBay (auf dem gewählten Marktplatz) eingeloggt sein. Die Extension meldet sich nicht selbst bei eBay an, und eine eigene Meldung „nicht bei eBay angemeldet“ gibt es nicht. Die Produkte laufen dann in der Regel erst nach 15 Minuten mit „Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“ aus. Eine Anmeldung bei Amazon braucht die Extension nicht. **Nicht sicher belegt:** ob Amazon je nach Anmeldung oder Lieferadresse andere Liefer- und Versandangaben zeigt (das kann die Prüfungen in [Abschnitt 9](#9-prüfungen-auf-der-amazon-seite-vor-dem-listen-buyboxfba-und-mehr) beeinflussen).
5. **Produkte vorhanden?** Auf der Browser-Lister-Seite steht rechts neben „Produkte aus“, wie viele Produkte verfügbar sind (z. B. „2.340 verfügbar · 12 in Arbeit“).
6. **Preise eingestellt?** Einstellungen, Reiter „Preise & Listing“, Karte „Preise“ (siehe [Abschnitt 15](#15-preis-beim-listen)).
7. **OpenAI-Schlüssel eingetragen?** Einstellungen, Reiter „KI“, Karte „KI (OpenAI)“, Feld „OpenAI-API-Schlüssel (für die Titel-Generierung)“. Ohne gültigen Schlüssel scheitert jedes Produkt aus der Produkt-Datenbank, denn der Titel kommt immer von der KI (siehe [Abschnitt 10](#10-titel)). Die KI-Kosten laufen über dein eigenes OpenAI-Konto. Der Schlüssel wird nicht auf dem Server gesichert. Auf einem neuen Rechner musst du ihn neu eintragen (oder per Einstellungsdatei mitnehmen).
8. **„Listing automatisch absenden“ an?** Einstellungen, Reiter „Preise & Listing“, Karte „Listing“. Nur wenn der Schalter an ist, klickt die Extension selbst auf eBays Knopf zum Einstellen. Standard: an.
9. **Filter geprüft?** Einstellungen, Reiter „Produkt-Filter“ (Karten „Beim Listen“ und „Amazon-Filter“). Auf der Browser-Lister-Seite steht der Stand der drei Listen-Filter in der Zeile „Aktuell: …“. Prüfe besonders „Preis bis“ (siehe [9.4](#94-preis-ab-und-preis-bis)).
10. **Versand, Zahlung, Rücknahme bei eBay eingerichtet?** Der Browser-Lister trägt diese Angaben nicht selbst ein; es gilt, was eBay im Formular vorbelegt. **Nicht sicher belegt:** was eBay bei dir vorbelegt – prüfe ein fertiges Angebot.

## 4. Browser-Lister öffnen und Aufbau der Seite

**So öffnest du ihn** (zwei Wege):

- Im **Dashboard** im Bereich „Vorgänge“ auf die Karte „Browser-Lister“ klicken (Text darunter: „Listet im Browser über Amazon- und eBay-Tabs, auf Wunsch mit Zeitschaltung.“).
- In der **Seitenleiste** links in der Gruppe „Arbeiten“ auf „Browser-Lister“ klicken.

Der Browser-Lister öffnet sich in einem eigenen Tab. **Ist er schon offen, springt der Klick zu diesem Tab**, es entsteht kein zweiter. Ohne Anmeldung sind die Karte und der Eintrag in der Seitenleiste grau.

Der Tab heißt „Cash Lister – Browser-Lister“. Oben steht die Überschrift „Browser-Lister“, darunter „Listet Produkte über Amazon- und eBay-Tabs, bis die gewünschte Zahl an Angeboten steht.“ Rechts oben ist der Knopf „Statusbericht“.

**Aufbau von oben nach unten:**

1. **Kopf:** Überschrift und rechts der Knopf „Statusbericht“.
2. **Große Karte für den Lauf:**
   - Erste Zeile: „Produkte aus“ (Auswahl), daneben die Bestandsanzeige (z. B. „1.204 verfügbar · 3 in Arbeit“) und der Knopf „Verwalten“; rechts „Wie viele Angebote“ (Zahlenfeld) und „Gleichzeitig“ (Auswahl 1 bis 10).
   - Zweite Zeile: links „Pausieren“ und „Fortsetzen“, rechts „Stoppen & zurücksetzen“ und der Hauptknopf „Starten“.
   - Darunter der Fortschrittsbalken und die Zeile „Fortschritt … %“ mit „… erfolgreich gelistet“ und „… fehlgeschlagen“.
   - Nach einem Lauf erscheint darunter eine Abschlusszeile.
3. **Karte „Tabs und Filter“:** der Schalter „Fehler-Tabs schließen“ und die Zeile „Produkt-Filter“ mit dem aktuellen Stand und dem Knopf „Ändern“.
4. **Karte „Zeitschaltung“:** der Haken „Zeitschaltung an“, das Feld „danach … Stunden Pause, dann weiter“, ein kurzer Hilfetext und (wenn die Zeitschaltung an ist) die Statuszeile.

**Wichtig:** Lass den Browser-Lister-Tab während des Laufs offen. Vor jedem neuen Produkt prüft der Lauf, ob dieser Tab noch da ist. Ist er geschlossen, holt der Lauf keine neuen Produkte mehr und endet, sobald die gerade laufenden Produkte fertig sind. In einer Pause der Zeitschaltung endet er erst nach der Pause (jeder parallele Durchgang listet dann noch ein Produkt). Das Dashboard warnt dann mit „Browser-Lister-Tab geschlossen“.

## 5. Alle Bedienelemente im Einzelnen

### 5.1 „Produkte aus“

- **Wo:** Erste Zeile der großen Karte, ganz links.
- **Was es macht:** Legt fest, aus welcher Quelle der Lauf seine Produkte nimmt. Pro Lauf gibt es genau eine Quelle, es wird nicht gemischt.
  - „Produkt-Datenbank“: deine gesammelten bzw. importierten Produkte. Die Liste gehört zu deinem Konto und liegt auf dem Server (siehe [Abschnitt 6](#6-die-produkt-datenbank-beim-listen-entnahme-in-arbeit-server-ausfall)).
  - „Konkurrenz-Scanner“: Funde aus dem Konkurrenz-Scanner. Sie bringen den eBay-Titel des Konkurrenten mit; der wird als Titel benutzt, die KI schreibt dann keinen Titel (siehe [Abschnitt 10](#10-titel)). Diese Funde liegen nur in diesem Chrome-Profil, nicht auf dem Server.
- **Standard:** „Produkt-Datenbank“.
- **Reihenfolge:** Der Lauf nimmt die Produkte **von oben**. Bei der Produkt-Datenbank bestimmt das die „Sortierung“ auf der Seite „Produkt-Datenbank“ („Älteste zuerst“ oder „Neuste zuerst“). Diese Sortierung gilt nur für das Gerät, auf dem du sie einstellst.
- **Während eines Laufs** ist die Auswahl gesperrt (grau), damit nicht mitten im Lauf die Quelle wechselt. Nach „Pausieren“ ist sie wieder bedienbar. Ein Wechsel wirkt dann ab dem nächsten entnommenen Produkt.
- Was mit einem entnommenen Produkt danach passiert (Erfolg, Fehlschlag, Abbruch): [6.3](#63-was-nach-dem-listen-mit-dem-produkt-passiert).

### 5.2 Die Bestandsanzeige neben „Produkte aus“

Rechts neben der Auswahl steht, wie viel die gewählte Quelle noch hergibt. Die Anzeige wird beim Öffnen der Seite, beim Wechsel der Quelle und während des Laufs nach jedem Produkt neu geholt.

| Anzeige | Bedeutung |
|---|---|
| „…“ | wird gerade geladen |
| „1.204 verfügbar“ | so viele Produkte sind frei und können gelistet werden |
| „1.204 verfügbar · 12 in Arbeit“ | dazu sind 12 Produkte gerade „In Arbeit“ – bei einem anderen Gerät, im CSV-Lister oder in diesem Lauf. Sie zählen nicht als verfügbar. |
| „⚠ Server nicht erreichbar – Lister pausiert, macht von selbst weiter.“ | Ein laufender Lauf wartet auf den Server (siehe [6.5](#65-wenn-der-server-nicht-erreichbar-ist-pause)). Statt des Punkts am Ende kann auch „(Produkt-Datenbank noch nicht bereit).“ oder „(HTTP …).“ stehen. |
| „nicht angemeldet – bitte im Dashboard anmelden“ | Du bist nicht (mehr) angemeldet. |
| „Server nicht erreichbar – Bestand gerade nicht abrufbar“ | Kein Lauf wartet, aber die Produkt-Datenbank ist gerade nicht abrufbar. |
| „? verfügbar“ | Die Extension hat keine Antwort bekommen. Seite neu laden (F5). |

Beim Konkurrenz-Scanner steht nur „… verfügbar“ (bzw. „? verfügbar“), ohne „In Arbeit“.

### 5.3 „Verwalten“

- **Wo:** Neben der Bestandsanzeige.
- **Was es macht:** Öffnet die Seite der gewählten Quelle: „Produkt-Datenbank“ oder „Konkurrenz-Scanner“. Ist diese Seite schon in einem Tab offen, springt der Klick dorthin.

### 5.4 „Wie viele Angebote“

- **Wo:** Erste Zeile der großen Karte, rechts.
- **Was es macht:** Die Zahl der **erfolgreich eingestellten** Angebote, nach der der Lauf aufhört. Fehlgeschlagene Produkte zählen nicht mit; der Lauf holt dafür Ersatz aus der Quelle.
- **Standard:** 100. Kleinster Wert 1.
- **Beispiel:** Du trägst 50 ein, 10 Produkte schlagen fehl → der Lauf entnimmt 60 Produkte und endet mit 50 Angeboten (sofern die Quelle genug hergibt).
- **Mit mehreren parallelen Durchgängen („Gleichzeitig“):** Der Lauf zählt Produkte, die gerade in Arbeit sind, schon mit. Dadurch entstehen nicht mehr Angebote als eingestellt.
- **Mit Zeitschaltung:** Die Zahl ist dann nicht das Ende des Laufs, sondern die Menge **pro Runde** (siehe [5.13](#513-karte-zeitschaltung)).
- **Gesperrt während eines Laufs.** Nach „Pausieren“ ist das Feld wieder bedienbar; eine geänderte Zahl gilt nach „Fortsetzen“ sofort (der Lauf prüft sie vor jedem neuen Produkt).
- **Typische Fehler:** Feld leer oder 0 → Meldung „Bitte oben eintragen, wie viele Angebote entstehen sollen.“ und der Lauf startet nicht. Quelle kleiner als die Zahl → der Lauf endet früher mit „Quelle aufgebraucht - …“.

### 5.5 „Gleichzeitig“

- **Wo:** Erste Zeile der großen Karte, ganz rechts. Bis Version 45.5 hieß das Feld „Thread Count“.
- **Was es macht:** Wie viele Produkte gleichzeitig bearbeitet werden.
- **Werte:** 1 bis 10. **Standard:** 1.
- **Wirkung:** Jeder parallele Durchgang öffnet für sein Produkt einen Amazon-Tab und danach einen eBay-Tab, beide rechts neben dem Browser-Lister-Tab im selben Fenster. Bei 5 gleichzeitig können also bis zu 10 Arbeits-Tabs offen sein (bei „Nur chinesische Verkäufer“ kurz zusätzlich je ein Tab für die Verkäuferseite). Bei der Produkt-Datenbank sind entsprechend viele Produkte gleichzeitig „In Arbeit“.
- **Mehr gleichzeitig** = schneller, aber mehr Last für deinen Rechner und mehr gleichzeitige Zugriffe auf Amazon, eBay und dein OpenAI-Konto.
- **Wann wirkt eine Änderung?** Die Zahl wird beim Start eines Laufs gelesen. Eine Änderung während des Laufs gilt erst beim nächsten Start.
- **Nicht sicher belegt:** Eine empfohlene Zahl gibt es nicht. Wenn Bilder beim Hochladen auf eBay häufig fehlschlagen oder Sicherheitsabfragen auftauchen, ist eine kleinere Zahl der erste Versuch.

### 5.6 „Starten“

- **Wo:** Zweite Zeile der großen Karte, ganz rechts (der hervorgehobene Knopf). Bis Version 45.5 hieß er „Opti-List“.
- **Hinweis beim Darüberfahren:** „Titel und Artikelmerkmale schreibt die KI (Merkmale je nach Einstellungen → Preise & Listing → „Artikelmerkmale (KI)“), ab vier Fotos dazu ein Sammelbild“.
- **Was es macht:** Startet einen Lauf. Es gibt nur noch diesen einen Start-Knopf. **Der Titel kommt bei Produkten aus der Produkt-Datenbank immer von der KI.** Einen Start ohne KI („Standard-List“, „Ohne KI starten“) gibt es nicht mehr. Ausnahme: Produkte aus dem Konkurrenz-Scanner nehmen den eBay-Titel des Konkurrenten.

**Was beim Klick geprüft wird (Startprüfung, in dieser Reihenfolge):**

1. **Angemeldet und freigeschaltet?** Sonst: „Nicht angemeldet oder Zugang deaktiviert - bitte im Dashboard anmelden.“ Das kommt auch, wenn dein Zugang abgeschaltet oder dein Abo gesperrt ist.
2. **Steht bei „Wie viele Angebote“ eine Zahl über 0?** Sonst: „Bitte oben eintragen, wie viele Angebote entstehen sollen.“
3. **Nur bei Quelle „Produkt-Datenbank“: Ist die Produkt-Datenbank erreichbar?**
   - „Nicht angemeldet oder Sitzung abgelaufen - bitte im Dashboard anmelden, dann starten.“ – deine Anmeldung gilt nicht mehr. Im Dashboard neu anmelden.
   - „Server nicht erreichbar - die Produkt-Datenbank liegt auf dem Server. Bitte später erneut starten.“ – der Server antwortet gerade nicht.
   - „Produkt-Datenbank nicht abrufbar: …“ – ein anderer Fehler; der Grund steht hinter dem Doppelpunkt.
4. **Gibt die Quelle etwas her?** Gezählt werden nur **freie** Produkte, nicht die „In Arbeit“.
   - „Der Konkurrenz-Scanner hat noch keine Funde.“
   - „Alle … Produkte der Datenbank sind gerade in Arbeit - auf einem anderen Gerät oder im CSV-Lister. Später erneut starten.“ – es gibt Produkte, aber alle sind gerade bei einem anderen Gerät oder im CSV-Lister „In Arbeit“. (Den CSV-Lister sehen seit Version 46.0 alle Kunden in der Seitenleiste, siehe `references/produktuebersicht-und-csv-lister.md`.)
   - „Die Produkt-Datenbank ist leer - erst Produkte einsammeln.“

In allen diesen Fällen startet der Lauf nicht.

**Beim Start werden zurückgesetzt:** „erfolgreich gelistet“, „fehlgeschlagen“, der Fortschritt und der Statusbericht (er wird geleert). Die Runde der Zeitschaltung wird beim normalen Start **nicht** zurückgesetzt.

**Voraussetzung:** ein gültiger OpenAI-Schlüssel (siehe [Checkliste](#3-bevor-du-startest-checkliste), Punkt 7). Ohne ihn scheitert jedes Produkt aus der Produkt-Datenbank mit „KI-Titel ist leer“. Produkte aus dem Konkurrenz-Scanner brauchen keinen KI-Titel; ohne Schlüssel bekommen sie aber immer den Spielzeug-Warnhinweis (siehe [11.3](#113-spielzeug-warnhinweis)).

### 5.7 „Pausieren“ und „Fortsetzen“

- **„Pausieren“:** Hält den Lauf an. Produkte, die gerade bearbeitet werden, laufen zu Ende. Danach wartet jeder parallele Durchgang, bevor er das nächste Produkt bearbeitet. Jeder Durchgang hat das nächste Produkt meist schon aus der Quelle genommen und hält es bereit; es wird nach „Fortsetzen“ gelistet.
  - Bei der Produkt-Datenbank bleibt so ein bereitgehaltenes Produkt während der Pause „In Arbeit“ für dieses Gerät. Andere Geräte bekommen es nicht.
  - Ist seit der Entnahme mehr als etwa eine Minute vergangen (z. B. nach einer Pause), fragt die Extension vor dem Listen beim Server nach, ob das Produkt noch diesem Gerät gehört. Gehört es nicht mehr dazu, wird es **nicht** gelistet und bleibt in der Produkt-Datenbank. Lässt sich das gerade nicht prüfen (Server weg), wird es ebenfalls nicht gelistet, sofern das Gerät nicht mehr sicher ist, dass es ihm noch gehört. Im Statusbericht steht für so ein Produkt keine Zeile.
- **„Fortsetzen“:** Setzt einen pausierten Lauf fort.
- **Zustände:** Ohne laufenden Lauf ist „Pausieren“ grau. Während des Laufs ist „Fortsetzen“ grau. Nach „Pausieren“ ist „Pausieren“ grau und „Fortsetzen“ aktiv; „Produkte aus“ und „Wie viele Angebote“ sind dann wieder bedienbar.
- **Typischer Fehler:** „Fortsetzen“ klicken, obwohl gar kein Lauf läuft. Dann merkt sich die Seite „läuft“, und nach dem nächsten Neuladen ist „Starten“ grau. Abhilfe: „Stoppen & zurücksetzen“.
- Eine Pause der Zeitschaltung wird durch „Pausieren“/„Fortsetzen“ nicht verkürzt.
- Den Stand „pausiert“ zeigt auch das Dashboard auf der Karte „Browser-Lister“.

### 5.8 „Stoppen & zurücksetzen“

- **Wo:** Zweite Zeile der großen Karte, links neben „Starten“. Bis Version 45.5 hieß er „Reset & Terminate“.
- **Hinweis beim Darüberfahren:** „Lauf stoppen, Zähler, Statusbericht und Runde der Zeitschaltung zurücksetzen, Seite neu öffnen. Gelistete Angebote bleiben bei eBay.“
- **Was er macht:**
  - Der Lauf holt keine neuen Produkte mehr.
  - Produkte der Produkt-Datenbank, die schon entnommen, aber noch nicht in Bearbeitung sind (auch die während einer Pause bereitgehaltenen), gehen **sofort in die Produkt-Datenbank zurück** und sind wieder frei – auch für deine anderen Geräte.
  - „erfolgreich gelistet“ und „fehlgeschlagen“ auf 0, Fortschritt auf 0 %.
  - Der Statusbericht wird geleert.
  - Die Runde der Zeitschaltung wird zurückgesetzt (eine laufende Pause der Zeitschaltung endet).
  - Wartet der Lauf gerade auf den Server, endet auch diese Wartezeit sofort.
  - Der Browser-Lister-Tab wird geschlossen und an derselben Stelle neu geöffnet (das sieht aus wie ein Neuladen).
- **Was er NICHT macht:** Er schließt keine Amazon- oder eBay-Tabs, die gerade bearbeitet werden. Produkte, die schon in Bearbeitung sind, laufen zu Ende und können noch eingestellt werden. Ihre Ergebnisse zählen dann nicht mehr in den (frisch genullten) Zählern mit. Im Dashboard unter „Heute gelistet“ zählen sie trotzdem.
- **Danach neu starten:** Warte, bis sich alle Arbeits-Tabs des abgebrochenen Laufs geschlossen haben (bzw. bei Fehlern stehen bleiben), bevor du einen neuen Lauf startest. Sonst können Durchgänge, die beim Abbrechen noch ein Produkt in Arbeit hatten, im neuen Lauf weiterarbeiten – dann laufen mehr Durchgänge als eingestellt, und die Zielzahl kann überschritten werden.
- **Wann benutzen:** Wenn du einen Lauf abbrechen willst, oder wenn „Starten“ grau ist, obwohl kein Lauf läuft (siehe [Probleme und Lösungen](#26-probleme-und-lösungen)).
- **Achtung bei Pause:** Siehe [7.4](#74-lauf-abbrechen).

### 5.9 „Statusbericht“

- Rechts oben auf der Seite. Öffnet die Seite „Statusbericht“ mit dem Ergebnis jedes Produkts. Ist der Statusbericht schon offen, springt der Klick zu diesem Tab – **dann F5 drücken**, denn die Seite aktualisiert sich nicht von selbst. Alles dazu in [Abschnitt 23](#23-der-statusbericht-und-alle-meldungen).

### 5.10 Fortschritt, Zähler und Abschlusszeile

- **Balken und „Fortschritt … %“:** Erfolgreiche Angebote geteilt durch „Wie viele Angebote“ (mit Zeitschaltung: durch die Menge pro Runde). Die Prozentzahl ist ganzzahlig und abgerundet (99,6 % zeigt also noch „99 %“).
- **„… erfolgreich gelistet“:** erfolgreich eingestellte Angebote in diesem Lauf.
- **„… fehlgeschlagen“:** fehlgeschlagene Produkte in diesem Lauf (jeder Grund, auch „schon vergeben“ oder ein Filter).
- **Abschlusszeile** (unter dem Fortschritt, nach dem Ende eines Laufs):
  - „Fertig: X von Y gelistet.“
  - „Quelle aufgebraucht - X von Y gelistet. Erst neue Produkte einsammeln, dann noch einmal starten.“ (orange). Das kommt auch, wenn in der Produkt-Datenbank zwar noch Produkte stehen, aber keines mehr frei ist (alle „In Arbeit“).
  - „X von Y gelistet. Browser-Lister beendet: … Danach neu starten.“ (orange) – der Lauf wurde vorzeitig beendet, z. B. weil die Anmeldung abgelaufen ist (siehe [6.6](#66-abgemeldet-zugang-abgeschaltet-oder-abo-gesperrt-während-des-laufs)).
- **Meldungsfenster** „Fertig - die eingestellte Zahl an Angeboten ist erreicht.“ – erscheint, wenn die Zielzahl erreicht ist (nicht bei eingeschalteter Zeitschaltung).
- Die Abschlusszeile verschwindet, sobald du „Produkte aus“ oder „Wie viele Angebote“ änderst oder einen neuen Lauf startest.

### 5.11 Karte „Tabs und Filter“: „Fehler-Tabs schließen“

- **Wo:** Karte „Tabs und Filter“, Schalter rechts. Darunter klein: „Amazon- und eBay-Tab eines fehlgeschlagenen Angebots zumachen“. Bis Version 45.5 hieß er „Close Errored Listings“.
- **Was er macht:** Schlägt ein Produkt fehl, nachdem schon ein eBay-Tab geöffnet war, schließt die Extension den Amazon- und den eBay-Tab dieses Produkts.
- **Standard:** an.
- **Aus:** Fehlgeschlagene Tabs bleiben offen, damit du dir ansehen kannst, wo es gehakt hat. Bei vielen Fehlern sammeln sich dann viele Tabs.
- Erfolgreiche Produkte: Beide Tabs werden immer geschlossen.
- Scheitert ein Produkt schon auf der Amazon-Seite (bevor ein eBay-Tab offen war), wird der Amazon-Tab immer geschlossen – unabhängig von diesem Schalter.

### 5.12 Karte „Tabs und Filter“: „Produkt-Filter“ und „Ändern“

- Text: „Produkt-Filter“, darunter klein: „nur FBA, nur chinesische Verkäufer, GPSR – stehen in den Einstellungen und gelten auch für den CSV-Lister“.
- Darunter der aktuelle Stand, z. B. „Aktuell: nur FBA an · nur chinesische Verkäufer aus · GPSR aus“. Die Zeile aktualisiert sich von selbst, wenn du in den Einstellungen etwas umstellst.
- **Knopf „Ändern“:** Öffnet die Einstellungen. Die Einstellungsseite öffnet mit dem ersten Reiter „Preise & Listing“ – klick dort auf den Reiter „Produkt-Filter“. Die drei Schalter stehen in der Karte „Beim Listen“. Ist die Einstellungsseite schon in einem Tab offen, holt Chrome diesen Tab nach vorne; dann ist der Reiter offen, den du dort zuletzt gewählt hattest.
- Was die Filter bewirken: [Abschnitt 9](#9-prüfungen-auf-der-amazon-seite-vor-dem-listen-buyboxfba-und-mehr).

### 5.13 Karte „Zeitschaltung“

- **Wo:** Karte „Zeitschaltung“: Haken „Zeitschaltung an“, Zahlenfeld zwischen „danach“ und „Stunden Pause, dann weiter“. Bis Version 45.5 hieß das „Listing-Timer“.
- **Hilfetext auf der Seite:** „Eine Runde ist die Zahl bei „Wie viele Angebote“. Ist sie erreicht, ruht der Lauf und macht danach mit der nächsten Runde weiter.“
- **Was sie macht:** Verteilt das Listen auf Runden. Die Zahl bei „Wie viele Angebote“ wird zur Menge **pro Runde**. Ist diese Menge in einer Runde erfolgreich eingestellt, ruht der Lauf für die eingestellten Stunden und macht dann mit der nächsten Runde weiter – so lange, bis die Quelle leer ist oder du „Stoppen & zurücksetzen“ drückst.
- **Beispiel:** „Wie viele Angebote“ 100, Zeitschaltung an, 24 Stunden → nach dem 100. erfolgreichen Angebot 24 Stunden Pause, dann die nächsten 100 usw.
- **Standard:** Haken aus. Stunden: 24. Das Feld ist auf Schritte von 0,25 Stunden (15 Minuten) ausgelegt; mit den Pfeilen kommst du nicht unter 0,25.
- **Stunden leer oder 0:** Dann gilt die Zeitschaltung als aus, auch wenn der Haken gesetzt ist – die Statuszeile erscheint nicht, und der Lauf endet bei der Zahl unter „Wie viele Angebote“ wie ohne Zeitschaltung. Trag eine Zahl über 0 ein.
- **Das Stundenfeld** ist ausgegraut, solange der Haken aus ist.
- **Wann beginnt die Pause?** Erst wenn die Menge der Runde erreicht ist – nicht schon während gelistet wird. Gezählt werden nur **erfolgreiche** Angebote.
- **Mehrere gleichzeitig:** Mit Zeitschaltung zählt der Lauf Produkte, die gerade in Arbeit sind, nicht vorab mit. Produkte, die beim Erreichen der Rundenmenge schon in Arbeit sind, laufen noch zu Ende. In einer Runde können deshalb ein paar Angebote mehr entstehen als eingestellt (höchstens etwa so viele, wie bei „Gleichzeitig“ eingestellt sind).
- **Statuszeile** (erscheint unter dem Hilfetext, wenn die Zeitschaltung an ist):
  - „⏱ Zeitschaltung: X von Y dieser Runde gelistet. Danach Z Pause.“ – die Runde läuft (oder es läuft gerade gar kein Lauf; die Zeile ist absichtlich neutral). Z ist die eingestellte Pausenlänge.
  - „😴 Schläft – Kontingent erreicht (X von Y). Weiter in ….“ – die Pause läuft, mit Restzeit (z. B. „3 Std 12 Min“, „4 Min 30 Sek“ oder „25 Sek“).
- **Fortschrittsbalken:** Bei eingeschalteter Zeitschaltung zeigt der Balken den Fortschritt der **aktuellen Runde**, nicht des ganzen Laufs.
- **Rundenzähler:**
  - Wird beim **Einschalten** des Hakens auf 0 gesetzt.
  - Wird bei „Stoppen & zurücksetzen“ auf 0 gesetzt.
  - Wird bei einem normalen Start **nicht** zurückgesetzt. Wer einen Lauf mit Zeitschaltung beendet und später neu startet, macht in derselben Runde weiter. War die Runde voll, wartet ein neuer Lauf erst die Restpause ab.
  - Zählt nur, solange die Zeitschaltung an ist.
- **Am Ende der Zielzahl** kommt bei eingeschalteter Zeitschaltung **keine** Meldung „Fertig - die eingestellte Zahl an Angeboten ist erreicht.“, weil der Lauf ja weitergeht.
- **Chrome und der Browser-Lister-Tab müssen während der Pause offen bleiben.** Ein geschlossener Browser setzt den Lauf nicht von selbst fort.
- Das Dashboard zeigt eine laufende Pause auf der Karte „Browser-Lister“ als „Pause bis HH:MM“.
- **Nicht verwechseln:** Die Zeitschaltung verteilt deine Läufe. Eine Uhrzeit, zu der eBay ein Angebot online stellt („Schedule Listing Time“), gibt es seit Version 46.0 nicht mehr.

### 5.14 Welche Knöpfe wann bedienbar sind

| Zustand | „Starten“ | „Pausieren“ | „Fortsetzen“ | „Produkte aus“ / „Wie viele Angebote“ |
|---|---|---|---|---|
| Seite frisch geöffnet, kein Lauf | aktiv | grau | aktiv | bedienbar |
| Lauf läuft | grau | aktiv | grau | gesperrt |
| Nach „Pausieren“ | grau | grau | aktiv | bedienbar |
| Nach „Pausieren“ und Neuladen der Seite (F5) | aktiv | grau | aktiv | bedienbar |
| Lauf zu Ende (Seite nicht neu geladen) | bleibt grau | bleibt aktiv | grau | gesperrt |
| Nach „Stoppen & zurücksetzen“ (Seite öffnet neu) | aktiv | grau | aktiv | bedienbar |

Ist ein Lauf von selbst zu Ende gegangen, aktualisiert die Seite die Knöpfe nicht von selbst: Lade die Seite neu (F5), dann ist „Starten“ wieder aktiv.

**Achtung nach „Pausieren“ und Neuladen:** „Starten“ ist dann wieder aktiv, obwohl der pausierte Lauf noch besteht. Zum Weitermachen „Fortsetzen“ nehmen, nicht „Starten“. Ein Klick auf „Starten“ beginnt einen neuen Lauf (Zähler und Statusbericht werden geleert), und die Durchgänge des pausierten Laufs laufen dabei zusätzlich wieder an – wie in [7.4](#74-lauf-abbrechen), Punkt 6, beschrieben. **Nicht sicher belegt:** wie sich das im Einzelfall auswirkt.

## 6. Die Produkt-Datenbank beim Listen: Entnahme, „In Arbeit“, Server-Ausfall

Seit Version 46.0 liegt die Produkt-Datenbank **je Konto auf dem Server**. Wie du Produkte sammelst, importierst und löschst, steht in `references/produkte-finden-und-datenbank.md`. Hier geht es darum, was beim Listen mit ihr passiert.

### 6.1 Eine Liste für alle deine Geräte

- Alle Geräte, auf denen du mit demselben Konto angemeldet bist, sehen und benutzen **dieselbe** Produkt-Datenbank.
- „Gerät“ heißt hier: ein Chrome-Profil mit Cash Lister. Zwei Chrome-Profile auf demselben Rechner zählen als zwei Geräte.
- Ohne Server gibt es keine Produkt-Datenbank: Ohne Anmeldung oder bei einem Server-Ausfall nimmt der Browser-Lister keine Produkte daraus.

### 6.2 Entnahme Stück für Stück und „In Arbeit“

- Der Browser-Lister nimmt **ein Produkt nach dem anderen**, immer nur so viele, wie er für die Zielzahl braucht. Er nimmt die Produkte von oben, in der „Sortierung“ dieses Geräts.
- Ab der Entnahme ist das Produkt **„In Arbeit“** für dieses Gerät. Auf der Seite „Produkt-Datenbank“ steht es dann in der Spalte „In Arbeit“; die Bestandsanzeige im Browser-Lister zählt es unter „in Arbeit“.
- Andere Geräte (und der CSV-Lister) bekommen ein Produkt, das „In Arbeit“ ist, nicht. So listen zwei deiner Geräte nie dasselbe Produkt gleichzeitig.
- Solange das Gerät das Produkt hält (auch während „Pausieren“), meldet es sich regelmäßig beim Server, damit das Produkt „In Arbeit“ bleibt.

### 6.3 Was nach dem Listen mit dem Produkt passiert

| Ergebnis | Was mit dem Produkt passiert |
|---|---|
| Erfolgreich gelistet | Es verlässt die Produkt-Datenbank. Die Produktvergabe bleibt für dich bestätigt (siehe [Abschnitt 19](#19-produktvergabe-beim-listen)). |
| Fehlgeschlagen (jeder Grund, auch ein Filter wie „Nur FBA“) | Es verlässt ebenfalls die Produkt-Datenbank, und die Vergabe wird freigegeben – das Produkt ist dann auch für andere Kunden wieder frei. Den Amazon-Link findest du im Statusbericht (siehe [7.5](#75-fehlgeschlagene-produkte-noch-einmal-versuchen)). |
| Entnommen, aber noch nicht in Bearbeitung („Stoppen & zurücksetzen“, Browser-Lister-Tab geschlossen, Zielzahl erreicht, Lauf zu Ende) | Es geht **zurück in die Produkt-Datenbank** und ist sofort wieder frei. |
| Chrome abgestürzt oder geschlossen, während das Produkt „In Arbeit“ war | Es bleibt bis zur Uhrzeit hinter „bis“ in der Spalte „In Arbeit“ der Produkt-Datenbank „In Arbeit“ für dieses Gerät und wird danach von selbst wieder frei – beim Browser-Lister nach etwa einer halben Stunde (`references/produkte-finden-und-datenbank.md`, Abschnitt 10.9). **Nicht sicher belegt:** ob der Server diese Zeit in jedem Fall genau so übernimmt. |
| Erfolg oder Fehlschlag, aber der Server war in diesem Moment nicht erreichbar | Die Extension merkt sich die Meldung und holt sie nach (auch nach einem Chrome-Neustart, wenn du wieder mit demselben Konto angemeldet bist). Bis dahin bleibt das Produkt „In Arbeit“. |

### 6.4 Auf mehreren Geräten gleichzeitig listen

- Du kannst auf mehreren Geräten gleichzeitig einen Browser-Lister laufen lassen, alle aus derselben Produkt-Datenbank. Durch „In Arbeit“ bekommt jedes Gerät andere Produkte.
- Jedes Gerät hat seinen eigenen Lauf, seine eigenen Zähler und seinen eigenen Statusbericht.
- Ist die Datenbank fast leer, kann ein Gerät beim Start „Alle … Produkte der Datenbank sind gerade in Arbeit - …“ melden, obwohl die Liste nicht leer ist: Die anderen Geräte haben gerade alle übrigen Produkte.
- Das Dashboard zählt unter „Heute gelistet“ die Angebote dieses Geräts und aller Geräte, auf denen in den Einstellungen (Reiter „eBay & Rahmenbedingungen“, Karte „Server-Modus“) „Dieses Gerät ist ein Server“ eingeschaltet ist (z. B. „davon 36 auf Server-1“). Von diesen Geräten zeigt dein Dashboard auch, was dort gerade läuft. Geräte ohne diesen Schalter tauchen im Dashboard der anderen Geräte nicht auf. Mehr dazu in `references/einstellungen.md`.

### 6.5 Wenn der Server nicht erreichbar ist (Pause)

- Antwortet der Server während eines Laufs nicht, **pausiert der Browser-Lister** und macht **von selbst weiter**, sobald der Server wieder antwortet. Du musst nichts tun.
- Jeder parallele Durchgang versucht es etwa alle 30 Sekunden erneut. Produkte, die schon in Bearbeitung sind, laufen zu Ende.
- **Woran du es siehst:**
  - Bestandsanzeige: „⚠ Server nicht erreichbar – Lister pausiert, macht von selbst weiter.“ (ggf. mit „(Produkt-Datenbank noch nicht bereit).“ oder „(HTTP …).“ am Ende).
  - Statusbericht: eine Zeile mit Status „Hinweis“ und derselben Meldung; geht es weiter, eine zweite Zeile „Server wieder erreichbar – Lister läuft weiter (Pause etwa N Min.).“
  - Dashboard: Karte „Browser-Lister“ mit „wartet auf den Server“ und „Server nicht erreichbar seit … – macht von selbst weiter · … gelistet“; in den Hinweisen (Glocke) „Server nicht erreicht“.
  - Seitenleiste unten: „Server nicht erreicht“ und „Lister nehmen keine Produkte“.
- **„Stoppen & zurücksetzen“** beendet die Wartezeit sofort.
- **Ohne Server listet der Browser-Lister keine Produkte aus der Produkt-Datenbank** – auch nicht ohne Reservierung.
- Dauert der Ausfall lange, wende dich an den Betreiber.

### 6.6 Abgemeldet, Zugang abgeschaltet oder Abo gesperrt während des Laufs

Stellt der Server beim Nehmen eines Produkts fest, dass du nicht mehr angemeldet bist, **endet der Lauf** (Warten würde hier nichts bringen). Produkte, die gerade in Bearbeitung sind, laufen zu Ende. Im Statusbericht steht eine „Hinweis“-Zeile, und die Abschlusszeile zeigt den Grund:

| Meldung | Was tun |
|---|---|
| „Browser-Lister beendet: Nicht angemeldet – bitte im Dashboard anmelden. Danach neu starten.“ | Im Dashboard anmelden, dann neu starten. |
| „Browser-Lister beendet: Sitzung abgelaufen – bitte im Dashboard neu anmelden. Danach neu starten.“ | Im Dashboard neu anmelden, dann neu starten. |
| „Browser-Lister beendet: Zugang abgeschaltet – bitte beim Betreiber melden. Danach neu starten.“ | An den Betreiber wenden. |
| „Browser-Lister beendet: Abo gesperrt – bitte im Dashboard nachsehen. Danach neu starten.“ | Im Dashboard in der Karte „Dein Abo“ bzw. im Anmeldebereich nachsehen und die offene Zahlung erledigen (siehe `references/konto-und-installation.md`). |
| „Browser-Lister beendet: … lehnt die Anfrage ab (HTTP …) – bitte die Extension aktualisieren oder beim Betreiber melden. Danach neu starten.“ | Extension aktualisieren (update.bat, danach Chrome komplett neu starten); hilft das nicht, an den Betreiber wenden. |

### 6.7 Erster Start nach dem Update: deine alte Liste wird hochgeladen

- Bis Version 45.5 lag die Produkt-Datenbank nur in deinem Chrome-Profil. Nach dem Update lädt die Extension diese alte Liste **von selbst** auf den Server hoch, sobald du angemeldet bist. Du musst nichts tun.
- Produkte, die schon in deinen Google-Sheets als gelistet stehen, werden dabei nicht hochgeladen. Produkte, die einem anderen Kunden gehören, kommen ebenfalls nicht in deine Liste.
- Bei einer großen alten Liste dauert das etwas. Das Dashboard zeigt dann z. B. „… Produkte werden noch auf den Server übertragen“.
- Mehr dazu: `references/produkte-finden-und-datenbank.md`.

### 6.8 Was du sonst wissen musst

- **Importieren ohne Server geht nicht:** Ist der Server nicht erreichbar, scheitert „Zur Datenbank hinzufügen“ mit einer Meldung. Details: `references/produkte-finden-und-datenbank.md`.
- **„Alle löschen“** auf der Seite „Produkt-Datenbank“ lässt Produkte stehen, die gerade „In Arbeit“ sind – also auch die, die dein laufender Browser-Lister gerade bearbeitet.

### 6.9 Der Konkurrenz-Scanner als Quelle

- Die Funde des Konkurrenz-Scanners liegen **nur in diesem Chrome-Profil**, nicht auf dem Server. Es gibt dort kein „In Arbeit“.
- Der Lauf nimmt die Funde von oben aus der Liste und entfernt sie dabei – auch wenn das Listen danach fehlschlägt. Zurückgelegt wird ein Fund nur, wenn du genau zwischen Entnahme und Bearbeitung abbrichst.
- Vor jedem Fund prüft der Browser-Lister die Produktvergabe (siehe [Abschnitt 19](#19-produktvergabe-beim-listen)).

### 6.10 Produkt-Datenbank und Konkurrenz-Scanner im Vergleich

| | „Produkt-Datenbank“ | „Konkurrenz-Scanner“ |
|---|---|---|
| Wo die Produkte liegen | auf dem Server, gemeinsam für alle Geräte deines Kontos | nur in diesem Chrome-Profil |
| „In Arbeit“ | ja | nein |
| Server nicht erreichbar | Lauf pausiert, macht von selbst weiter | nur mit „Server verbunden“ listen (siehe [Abschnitt 19](#19-produktvergabe-beim-listen)) |
| Titel | KI-Titel ohne Marken- und Firmennamen, höchstens 80 Zeichen | eBay-Titel des Konkurrenten (keine KI), höchstens 80 Zeichen |
| Suchbegriff auf eBays Einstiegsseite zum Einstellen | USA/CA/UK/AU: ein KI-Suchbegriff (aus dem Amazon-Titel); andere Domains: der Amazon-Titel | der Amazon-Titel |
| KI füllt Artikelmerkmale | ja, wenn „Pflicht-Artikelmerkmale mit KI ausfüllen“ an ist | nein |
| Leere optionale Merkmale | werden mit dem KI-Suchbegriff gefüllt, wenn „Optionale Artikelmerkmale mit KI ausfüllen“ an ist und es einen Suchbegriff gibt | nein |
| Sammelbild | wird versucht (siehe [Abschnitt 14](#14-bilder)) | nein |
| Spielzeug-Prüfung per KI | ja | ja |
| Braucht OpenAI-Schlüssel | ja | nur für die Spielzeug-Prüfung (ohne Schlüssel kommt der Warnhinweis immer) |

## 7. Schritt-für-Schritt-Anleitungen

### 7.1 Dein erster Lauf

1. Prüfe die [Checkliste](#3-bevor-du-startest-checkliste).
2. Öffne den Browser-Lister: im Dashboard die Karte „Browser-Lister“ oder in der Seitenleiste „Browser-Lister“.
3. Wähle bei „Produkte aus“ die Quelle und prüfe, dass die Bestandsanzeige mehr als 0 „verfügbar“ zeigt.
4. Trag bei „Wie viele Angebote“ eine kleine Zahl ein, z. B. 3, um es zu testen.
5. Lass „Gleichzeitig“ für den Anfang auf 1.
6. Lass „Zeitschaltung an“ aus.
7. Schalte „Fehler-Tabs schließen“ für den Test **aus**. Dann bleiben die Tabs fehlgeschlagener Produkte offen und du siehst, was passiert ist.
8. Klick auf „Starten“.
9. Rechts neben dem Browser-Lister-Tab öffnen sich die Arbeits-Tabs. Der Tab-Titel zeigt jeweils den aktuellen Schritt (siehe [Abschnitt 24](#24-tab-titel-und-tab-symbole-während-des-listens)).
10. Öffne nach dem Ende den „Statusbericht“ (rechts oben) und schau dir die neuen Angebote über die Spalte „eBay-Link“ bzw. in deinem eBay-Verkäuferbereich an.
11. Prüfe ein fertiges Angebot: Titel, Preis, Bilder, Beschreibung, Zustand, Versand. Passt alles, kannst du größere Läufe starten und „Fehler-Tabs schließen“ wieder einschalten.

### 7.2 Lauf mit Zeitschaltung (z. B. 100 Angebote pro Tag)

1. Browser-Lister öffnen.
2. „Wie viele Angebote“ auf die Menge pro Runde setzen, z. B. 100.
3. In der Karte „Zeitschaltung“ den Haken „Zeitschaltung an“ setzen (dabei wird der Rundenzähler auf 0 gesetzt).
4. Bei „danach … Stunden Pause, dann weiter“ die Stunden eintragen, z. B. 24.
5. Auf „Starten“ klicken.
6. Die Statuszeile zeigt „⏱ Zeitschaltung: … von 100 dieser Runde gelistet. …“. Nach dem 100. Erfolg wechselt sie zu „😴 Schläft – …“ mit der Restzeit.
7. Rechner, Chrome und den Browser-Lister-Tab offen lassen.
8. Der Lauf endet erst, wenn die Quelle leer ist oder du „Stoppen & zurücksetzen“ drückst. Neue Produkte, die du währenddessen in die Quelle legst (auch von einem anderen Gerät aus), werden in späteren Runden mitgenommen.

### 7.3 Lauf anhalten und fortsetzen

1. Auf „Pausieren“ klicken.
2. Warten, bis die gerade laufenden Produkte fertig sind (die Arbeits-Tabs schließen sich bzw. bleiben bei Fehlern stehen).
3. Zum Fortsetzen auf „Fortsetzen“ klicken.

### 7.4 Lauf abbrechen

1. Auf „Stoppen & zurücksetzen“ klicken.
2. Der Browser-Lister-Tab öffnet neu, Zähler und Statusbericht sind leer.
3. Produkte der Produkt-Datenbank, die noch nicht in Bearbeitung waren, sind sofort wieder frei in der Produkt-Datenbank.
4. Offene Arbeits-Tabs laufen noch zu Ende. Willst du nicht, dass ein Produkt noch eingestellt wird, schließ dessen eBay-Tab selbst. Der zugehörige Durchgang wartet danach trotzdem noch bis zu 15 Minuten auf eine Rückmeldung, bevor er das Produkt als fehlgeschlagen abschließt und endet.
5. Einen neuen Lauf erst starten, wenn alle Arbeits-Tabs des alten Laufs zu sind (siehe [5.8](#58-stoppen--zurücksetzen)). Hast du einen eBay-Tab selbst geschlossen, warte dafür die 15 Minuten ab – oder schließ Chrome komplett und öffne es neu; das beendet alle alten Durchgänge sicher.
6. **Achtung, wenn du vorher „Pausieren“ gedrückt hattest:** Jeder parallele Durchgang hält dann schon das nächste Produkt bereit.
   - Quelle „Produkt-Datenbank“: Diese Produkte gehen beim Stoppen in die Produkt-Datenbank zurück und sind wieder frei. Es geht nichts verloren.
   - Quelle „Konkurrenz-Scanner“: Diese Funde (höchstens einer je Durchgang) stehen nach dem Abbrechen nicht mehr in der Liste des Konkurrenz-Scanners. Besser: Erst „Fortsetzen“ drücken, warten, bis die Arbeits-Tabs für diese Produkte aufgehen, und dann „Stoppen & zurücksetzen“.
   - Ein Lauf, der pausiert war und nur mit „Stoppen & zurücksetzen“ beendet wurde, kann beim nächsten Start zusätzlich zu den neuen Durchgängen kurz wieder anlaufen. **Nicht sicher belegt:** wie sich das im Einzelfall genau auswirkt. Sicher beendet ein komplettes Schließen von Chrome alle alten Durchgänge; danach im Browser-Lister einmal „Stoppen & zurücksetzen“ drücken und neu starten.

### 7.5 Fehlgeschlagene Produkte noch einmal versuchen

Eine Knopf-Funktion „Wiederholen“ gibt es nicht. Fehlgeschlagene Produkte werden auch nicht von selbst in die Quelle zurückgelegt.

1. „Statusbericht“ öffnen (bzw. den offenen Statusbericht mit F5 neu laden).
2. In den Zeilen mit Status „fehlgeschlagen“ die Spalte „Meldung“ lesen und die Ursache beheben (siehe [Abschnitt 23](#23-der-statusbericht-und-alle-meldungen)).
3. Den Amazon-Link aus der Spalte „Amazon-Link“ kopieren.
4. Im Browser-Lister bei „Produkte aus“ „Produkt-Datenbank“ wählen und „Verwalten“ klicken (oder in der Seitenleiste „Produkt-Datenbank“).
5. Dort in der Karte „Links hinzufügen“ den Link einfügen und „Zur Datenbank hinzufügen“ klicken. Das geht nur, wenn der Server erreichbar ist.
6. Einen neuen Lauf starten.

Bei Produkten mit „Produkt bereits von einem anderen Nutzer vergeben“ lohnt sich das nicht – sie gehören einem anderen Kunden.

### 7.6 Testlauf, bei dem du selbst auf eBays Knopf zum Einstellen klickst

1. In den Einstellungen, Reiter „Preise & Listing“, Karte „Listing“, „Listing automatisch absenden“ ausschalten.
2. Im Browser-Lister „Wie viele Angebote“ auf 1 und „Gleichzeitig“ auf 1.
3. Auf „Starten“ klicken.
4. Warten, bis der Titel des eBay-Tabs „Bereit zum Einstellen!“ zeigt.
5. In den eBay-Tab wechseln, alles prüfen und selbst auf eBays Knopf zum Einstellen klicken. Die Extension erkennt den Klick und meldet Erfolg oder Fehler an den Browser-Lister.
6. Wenn du nicht innerhalb von 15 Minuten klickst, gilt das Produkt als fehlgeschlagen („Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“).
7. Danach „Listing automatisch absenden“ wieder einschalten.

Hinweis: Zeigt eBay eine Angebotsgebühr über 0 und ist „Auch mit Angebotsgebühr einstellen“ aus, wird das Produkt sofort als fehlgeschlagen gemeldet („Nicht eingestellt: eBay verlangt Angebotsgebühren …“) – auch in diesem Testlauf. Klickst du danach trotzdem selbst, erfährt der Browser-Lister davon nichts.

### 7.7 Auf zwei Geräten gleichzeitig listen

1. Auf beiden Geräten (bzw. Chrome-Profilen) mit **demselben** Cash-Lister-Konto im Dashboard anmelden.
2. Auf beiden in den Einstellungen die „Domain“ prüfen und auf beiden bei eBay angemeldet sein – in dem eBay-Konto, in dem die Angebote entstehen sollen.
3. Auf beiden den Browser-Lister öffnen, „Produkte aus“ auf „Produkt-Datenbank“, Zielzahl eintragen, „Starten“.
4. Jedes Gerät nimmt sich andere Produkte; die gerade bearbeiteten stehen auf der Seite „Produkt-Datenbank“ als „In Arbeit“ mit dem Gerät.
5. Jedes Gerät hat seinen eigenen Statusbericht. Willst du im Dashboard des einen Geräts auch sehen, was das andere listet, schalte auf dem anderen Gerät in den Einstellungen (Reiter „eBay & Rahmenbedingungen“, Karte „Server-Modus“) „Dieses Gerät ist ein Server“ ein; dann zählt es auch unter „Heute gelistet“ mit.

**Nicht sicher belegt:** ob eBay mehrere gleichzeitige Läufe auf einem eBay-Konto anders behandelt (z. B. mit mehr Sicherheitsabfragen).

## 8. Was während eines Laufs passiert

### 8.1 Reihenfolge für jedes einzelne Produkt

1. **Entnahme:** Ein paralleler Durchgang nimmt das oberste freie Produkt aus der Quelle. Bei der Produkt-Datenbank ist es ab jetzt „In Arbeit“.
2. **Produktvergabe (nur Konkurrenz-Scanner):** Die Extension prüft, ob das Produkt für dich reserviert werden kann (siehe [Abschnitt 19](#19-produktvergabe-beim-listen)). Ist es schon an einen anderen Kunden vergeben, endet das Produkt hier. Produkte aus der Produkt-Datenbank sind schon seit dem Import für dich reserviert.
3. **Amazon-Tab:** Die Amazon-Produktseite öffnet sich im Hintergrund. Dort laufen die Prüfungen aus [Abschnitt 9](#9-prüfungen-auf-der-amazon-seite-vor-dem-listen-buyboxfba-und-mehr). Danach berechnet die Extension den Preis, holt ggf. GPSR-Angaben, lässt den Titel erstellen und lädt das Titelbild.
4. **eBay-Tab, Einstiegsseite zum Einstellen (Suchfeld für das Produkt):** Die Extension trägt einen Suchbegriff ein und klickt auf Weiter.
5. **eBay-Seite „Passendes Produkt finden“:** Ggf. Bildabgleich (Dubletten), dann Zustand wählen, eBays Kategorie-Vorschlag übernehmen, Weiter.
6. **eBay-Angebotsformular:** Bilder, Titel, Artikelmerkmale, Preis, Custom Label, Marke, Beschreibung, Anzeigen-Option usw. (Abschnitte 10–17).
7. **Absenden:** Gebührenprüfung, dann Klick auf eBays Knopf zum Einstellen (wenn „Listing automatisch absenden“ an ist).
8. **Ergebnis:** Erfolg oder Fehler landet im Statusbericht, die Zähler laufen weiter, Tabs werden geschlossen (Erfolg immer, Fehler je nach „Fehler-Tabs schließen“). Bei der Produkt-Datenbank verlässt das Produkt die Liste (siehe [6.3](#63-was-nach-dem-listen-mit-dem-produkt-passiert)).

### 8.2 Zeitgrenzen

- **Amazon-Teil:** Die Amazon-Seite darf bis zu etwa 4 Minuten zum Laden brauchen. Danach wartet die Extension noch einmal bis zu etwa 4 Minuten auf das Ergebnis der Prüfungen, des Titels und des Titelbilds. Kommt bis dahin nichts, gilt das Produkt als fehlgeschlagen („Listen fehlgeschlagen – keine verwertbare Antwort der Amazon-Seite“ oder ein konkreter KI-Fehler, siehe [Abschnitt 23](#23-der-statusbericht-und-alle-meldungen)).
- **eBay-Teil:** Meldet der eBay-Tab innerhalb von 15 Minuten weder Erfolg noch Fehler, gilt das Produkt als fehlgeschlagen („Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“).

### 8.3 Wo die Tabs aufgehen

Alle Arbeits-Tabs öffnen sich im Hintergrund rechts neben dem Browser-Lister-Tab, im selben Fenster. Du kannst sie anklicken und zusehen. Schließ sie nicht von Hand, solange sie arbeiten – sonst schlägt das Produkt fehl. Bei „GPSR-Angaben übernehmen“ holt die Extension den Amazon-Tab kurz nach vorne, um die Herstellerangaben zu öffnen.

### 8.4 Der Browser-Lister im Dashboard

Das Dashboard zeigt im Bereich „Vorgänge“ auf der Karte „Browser-Lister“ den Stand. Ein Klick auf die Karte öffnet den Browser-Lister (oder springt zu seinem Tab). Alles Weitere zum Dashboard selbst steht in `references/dashboard.md`.

| Markierung oben rechts auf der Karte | Bedeutung |
|---|---|
| „bereit“ | kein Lauf; darunter z. B. „Heute 37 gelistet, 4 fehlgeschlagen“ und ggf. „· Zeitschaltung: je 100, dann 24 Std. Pause“ |
| „läuft · X von Y“ | Lauf aktiv; darunter „Läuft seit … · X gelistet, Z fehlgeschlagen“ |
| „pausiert“ | nach „Pausieren“ |
| „wartet auf den Server“ | Server-Pause (siehe [6.5](#65-wenn-der-server-nicht-erreichbar-ist-pause)) |
| „Pause bis HH:MM“ | Pause der Zeitschaltung |
| „Pause bis HH:MM – Tab zu“ | Pause der Zeitschaltung, aber der Browser-Lister-Tab ist geschlossen; der Lauf endet nach der Pause |
| „Tab geschlossen“ | Der Browser-Lister-Tab ist zu; darunter „Tab geschlossen – der Lauf endet nach dem aktuellen Produkt“ |
| „wird beendet“ | nach „Stoppen & zurücksetzen“, die letzten Produkte laufen noch zu Ende |
| „meldet sich nicht“ | nur bei einem anderen Gerät im Server-Modus, das sich länger nicht gemeldet hat |

Außerdem im Dashboard:
- Kennzahl „Heute gelistet“ mit Verlauf der letzten 14 Tage (dieses Gerät plus Geräte im Server-Modus, siehe [6.4](#64-auf-mehreren-geräten-gleichzeitig-listen)).
- Im Kasten „Heute“ die Punkte „Genug Produkte in der Datenbank“ (z. B. „… bereit · ein Lauf des Browser-Listers zielt auf 100“) und „Produkte gelistet“.
- In den Hinweisen (Glocke) z. B. „Browser-Lister-Tab geschlossen“ mit „Der Lauf endet nach dem aktuellen Produkt.“ bzw. „Der Lauf endet nach der Pause.“
- Meldest du dich im Dashboard ab, während der Browser-Lister läuft, fragt das Dashboard vorher nach („Gerade läuft auf diesem PC: Browser-Lister. … Trotzdem abmelden?“).

## 9. Prüfungen auf der Amazon-Seite vor dem Listen (Buybox/FBA und mehr)

Auf der Amazon-Seite prüft die Extension jedes Produkt der Reihe nach. **Die erste Prüfung, die nicht besteht, beendet das Produkt** – es wird übersprungen (zählt bei „fehlgeschlagen“) und die Meldung landet im Statusbericht. Der Zusatz „ZUM LISTEN BESTÄTIGEN“ in manchen Tab-Titeln hat im Browser-Lister keine Bedeutung: Das Produkt wird einfach übersprungen, du musst nichts bestätigen.

| Reihenfolge | Prüfung | Abschaltbar? | Meldung im Statusbericht |
|---|---|---|---|
| 1 | Amazon zeigt eine Sicherheitsabfrage | – | (keine eigene; siehe [Abschnitt 22](#22-sicherheitsabfragen-captcha-bei-amazon-und-ebay)) |
| 2 | Seite ist eine richtige Produktseite (mit Bildbereich) | nein | „Produktseite existiert nicht“ |
| 3 | Produkt wurde aus diesem Chrome-Profil schon einmal erfolgreich gelistet | nein | „Produkt ist schon gelistet (Duplikat)“ |
| 4 | Wort aus deiner Blacklist in Titel, Beschreibung, Stichpunkten oder Werten der Produktinformationen | über die Liste (leer = keine Prüfung) | „Produkt enthält ein Wort aus der Blacklist: …“ |
| 5 | ASIN der Seite passt zum Link (Amazon hat nicht auf ein anderes Produkt umgeleitet) | nein | „ASIN und Adresse (URL) passen nicht zusammen“ |
| 6 | Mindestbestellmenge größer als 1 | nein | „Produkt hat eine Mindestbestellmenge“ |
| 7 | Auf Lager (und Lieferzeit nicht zu lang) | nein | „Produkt ist nicht auf Lager“ |
| 8 | Kein Artikel mit „free international delivery“ | nein | „Produkt wird international versendet“ |
| 9 | Versand durch Amazon (Buybox) | ja: „Nur FBA“ | „Nicht von Amazon versendet (Versand: …)“ oder „Versender auf der Produktseite nicht erkennbar“ |
| 10 | Kostenloser Versand in der Buybox | nein | „Produkt hat keinen kostenlosen Versand“ |
| 11 | Kein Gebraucht-Angebot | nein | „Produkt ist gebraucht“ |
| 12 | Amazon-Preis nicht über „Preis bis“ | ja: Schalter bei „Preis bis“ | „Amazon-Preis zu hoch (Filter „Preis bis“)“ |
| 13 | Amazon-Preis nicht unter „Preis ab“ | ja: Schalter bei „Preis ab“ | „Amazon-Preis zu niedrig (Filter „Preis ab“)“ |
| 14 | Verkäufer sitzt in China/Hongkong | ja: „Nur chinesische Verkäufer“ (Standard aus) | „Kein chinesischer Verkäufer“ |
| 15 | GPSR-Herstellerangaben vorhanden | ja: „GPSR-Angaben übernehmen“ (Standard aus) | „Keine GPSR-Angaben gefunden“ |

Danach folgen Titel und Bild – Fehler dort siehe [Abschnitt 10](#10-titel) und [23](#23-der-statusbericht-und-alle-meldungen).

Wo die Schalter stehen: Einstellungen, Reiter „Produkt-Filter“. Karte „Beim Listen“ (neben der Überschrift klein: „gilt im Browser-Lister und im CSV-Lister“) mit „Nur FBA“, „Nur chinesische Verkäufer“, „GPSR-Angaben übernehmen“, „Markenlos listen“ und „Bildabgleich gegen fremde Angebote“. „Markenlos listen“ wirkt nur im CSV-Lister; der Browser-Lister trägt als Marke immer „Unbranded“ ein, egal wie dieser Schalter steht (siehe [Abschnitt 12](#12-artikelmerkmale)). Karte „Amazon-Filter“ (klein: „jeder Filter hat seinen eigenen Schalter“) mit „Max. verlängerte Lieferzeit“, „Mind. Sterne“, „Mind. Bewertungen“, „Mind. Lagerbestand“, „Preis ab“, „Preis bis“ und „Nur Verkauf durch Amazon“. Karte „Blacklist“.

### 9.1 „Nur FBA“ – die Buybox-Prüfung

- **Wo:** Einstellungen → Reiter „Produkt-Filter“ → Karte „Beim Listen“ → „Nur FBA“ (darunter klein: „Amazon muss der Versender sein“).
- **Standard:** an.
- **Was geprüft wird:** Wer laut Buybox **versendet**:
  - „Versand: Amazon“ (ein Händler verkauft, Amazon verschickt) → besteht.
  - „Versender / Verkäufer: Amazon“ (Amazon verkauft und verschickt) → besteht.
  - „Versender / Verkäufer: <Händler>“ (Händler verschickt selbst) → besteht nicht: „Nicht von Amazon versendet (Versand: <Händler>)“.
- Findet die Extension auf der Seite keine Angabe zum Versender, meldet sie „Versender auf der Produktseite nicht erkennbar“ und überspringt das Produkt.
- **Aus:** Keine Versand-Prüfung, Produkte werden unabhängig vom Versender gelistet.
- Es geht um den Versand durch Amazon, **nicht** um Prime.

### 9.2 „Nur chinesische Verkäufer“

- **Wo:** Einstellungen → Reiter „Produkt-Filter“ → Karte „Beim Listen“ (darunter klein: „sortiert alle anderen aus“).
- **Standard:** aus.
- **Was passiert:** Die Extension öffnet die Amazon-Verkäuferseite des Buybox-Verkäufers kurz in einem eigenen Tab und liest das Land der Geschäftsadresse. Nur „CN“ oder „HK“ besteht.
- Verkauft Amazon selbst, gilt das als **nicht** chinesisch → „Kein chinesischer Verkäufer“.
- Zusammen mit „Nur FBA“ müssen beide Bedingungen erfüllt sein.
- Kann die Verkäuferseite nicht gelesen werden, gilt der Verkäufer als nicht chinesisch.

### 9.3 „GPSR-Angaben übernehmen“

- **Wo:** Einstellungen → Reiter „Produkt-Filter“ → Karte „Beim Listen“ (darunter klein: „Produkte ohne diese Angaben werden übersprungen“).
- **Standard:** aus.
- **Was passiert auf Amazon:** Die Extension holt den Amazon-Tab kurz nach vorne, öffnet auf der Produktseite den Bereich mit den Sicherheitskontakten und liest Hersteller und verantwortliche Person in der EU aus. Gibt es dort keine Herstellerangaben, wird das Produkt übersprungen („Keine GPSR-Angaben gefunden“).
- **Was passiert auf eBay:** siehe [Abschnitt 17](#17-weitere-dinge-die-im-ebay-formular-passieren) (Herstellerangaben, ggf. Text in der Beschreibung und ein zusätzliches Bild „GPSR“).
- Tab-Titel dabei: „Hole GPSR-Angaben...“, „GPSR-Angaben erhalten!“ oder „ÜBERSPRUNGEN! keine GPSR-Angaben“. Dazwischen können kurz Zwischenstände stehen (z. B. „GPSR 1: Knopf „Sicherheitskontakte“ nicht gefunden“, wenn Amazon keinen solchen Bereich zeigt).

### 9.4 „Preis ab“ und „Preis bis“

- **Wo:** Einstellungen → Reiter „Produkt-Filter“ → Karte „Amazon-Filter“ → „Preis ab“ und „Preis bis“ (jeweils „in €“), jeder mit eigenem Ein/Aus-Schalter rechts. Ist der Schalter aus, ist das Zahlenfeld ausgegraut. Im Reiter „Preise & Listing“ steht dazu nur der Hinweis „„Preis ab“ und „Preis bis“ stehen unter **Produkt-Filter → Amazon-Filter**.“
- **Geprüft wird der Amazon-Preis** (Einkaufspreis), nicht dein späterer eBay-Preis.
- Die beiden Grenzen gelten auch beim Einsammeln mit dem Produkt-Grabber.
- **Ob die Grenze gilt, entscheidet der Schalter.** Ein Wert von 0 oder ein leeres Feld bedeutet: keine Grenze.
- **Achtung, wenn du von einer älteren Version kommst:** Das frühere Popup hat beim Öffnen 100 als Höchstpreis eingetragen, wenn dort nichts stand. Diese 100 steht oft noch in „Preis bis“. Solange der Schalter noch nie gesetzt wurde (Einstellungsseite seit dem Update nie geöffnet), gilt dieser Wert als Grenze – Produkte über 100 werden dann mit „Amazon-Preis zu hoch (Filter „Preis bis“)“ übersprungen. Öffnest du die Einstellungen zum ersten Mal, wird der Schalter bei „Preis bis“ automatisch eingeschaltet, wenn dort schon ein Wert über 0 steht – du siehst die Grenze von 100 dann also eingeschaltet. Abhilfe: Einstellungen öffnen, Reiter „Produkt-Filter“, und den Schalter bei „Preis bis“ bewusst ein- oder ausschalten bzw. den Wert anpassen.
- **Nach einer Wiederherstellung von Einstellungen** (Datei-Import oder „Einstellungen vom Server holen“, z. B. auf einem neuen Rechner): Die Ein/Aus-Schalter der Amazon-Filter werden nicht mit übertragen, nur die Zahlen. Bis du die Einstellungsseite öffnest, gilt dann jeder übertragene Preis über 0 als Grenze. Öffne danach einmal die Einstellungen und prüfe die Schalter.

### 9.5 Lagerbestand und Lieferzeit („Produkt ist nicht auf Lager“)

- Die Extension vergleicht den Verfügbarkeits-Text der Seite mit einer Liste bekannter „Auf Lager“-Texte (Englisch, Deutsch, Italienisch, Spanisch, Niederländisch).
- Auch eine **zu lange Lieferzeit** führt zu „Produkt ist nicht auf Lager“: Liegt das angezeigte Lieferdatum weiter in der Zukunft als die Zahl bei „Max. verlängerte Lieferzeit“ (Einstellungen → Reiter „Produkt-Filter“ → Karte „Amazon-Filter“, „in Tagen“, Standard 20), oder steht „Extended delivery time“ auf der Seite.
- Nach aktuellem Stand benutzt die Listen-Prüfung die Zahl bei „Max. verlängerte Lieferzeit“ auch dann, wenn der Schalter daneben aus ist (steht dort nichts, gelten 20 Tage). Der Schalter wirkt sicher auf den Produkt-Grabber. Willst du beim Listen längere Lieferzeiten zulassen, erhöhe die Zahl – den Schalter auszuschalten reicht nicht. **Nicht sicher belegt:** ob das so beabsichtigt ist – bei Fragen an den Betreiber wenden.

### 9.6 Was beim Listen NICHT geprüft wird

Diese Einstellungen im Reiter „Produkt-Filter“, Karte „Amazon-Filter“, gelten nur beim Einsammeln mit dem Produkt-Grabber, **nicht** beim Listen im Browser-Lister:
- „Mind. Sterne“
- „Mind. Bewertungen“
- „Mind. Lagerbestand“
- „Nur Verkauf durch Amazon“ (darunter klein: „Produkt-Grabber: übernimmt nur Produkte, die Amazon selbst verkauft und versendet“)

Beim Listen zählen aus dieser Karte nur „Preis ab“, „Preis bis“ und die Zahl bei „Max. verlängerte Lieferzeit“. Der Versand durch Amazon wird beim Listen über „Nur FBA“ geprüft (siehe [9.1](#91-nur-fba--die-buybox-prüfung)).

### 9.7 Kostenloser Versand, international, gebraucht, Mindestmenge

Diese Prüfungen sind immer aktiv und haben keinen Schalter:
- „Produkt hat keinen kostenlosen Versand“: In der Buybox wurde kein Hinweis auf kostenlose Lieferung gefunden (z. B. „GRATIS Lieferung“, „free delivery“).
- „Produkt wird international versendet“: Die Lieferung ist als „free international delivery“ gekennzeichnet.
- „Produkt ist gebraucht“: Die Buybox ist ein Gebraucht-Angebot.
- „Produkt hat eine Mindestbestellmenge“: Amazon verlangt eine Mindestbestellmenge über 1.

### 9.8 Deine Blacklist

- **Wo:** Einstellungen → Reiter „Produkt-Filter“ → Karte „Blacklist“ (klein: „eigene Liste, ein Wort oder Begriff je Zeile“) → Feld „Meine Liste“. Ein Wort oder eine Wortgruppe pro Zeile. Darunter „Wörter: …“ mit der Anzahl. Wird beim Tippen automatisch gespeichert.
- **Was geprüft wird:** Titel, Beschreibung, Stichpunkte und die **Werte** der Produktinformationen (nicht deren Bezeichnungen) der Amazon-Seite.
- **Wie:** Nur ganze Wörter, Groß-/Kleinschreibung egal, auch mit Umlauten und ß. Ein Eintrag „öl“ trifft also „Öl“, aber nicht „Heizöl“.
- **Folge:** Das Produkt wird übersprungen („Produkt enthält ein Wort aus der Blacklist: <Eintrag>“).
- Nicht zu verwechseln mit dem eingebauten Wortfilter, der Wörter nur **entfernt** (siehe [10.4](#104-eingebauter-wortfilter)).

## 10. Titel

### 10.1 Woher der Titel kommt

- **Produkte aus der Produkt-Datenbank:** **Immer die KI.** Sie schreibt den Titel in der Sprache deiner eBay-Domain (DE → Deutsch, USA/UK/CA/AU → Englisch, FR → Französisch, IT → Italienisch, ES → Spanisch, NL → Niederländisch), ohne Marken- und Firmennamen, mit höchstens 80 Zeichen.
  - Klappt die KI nicht, versucht die Extension es mehrmals. Klappt es dann immer noch nicht: „KI-Titel ist leer“.
  - Für Titel nutzt die Extension immer das Modell gpt-4o-mini, egal was bei „OpenAI-Modell (für KI-Beschreibung & Generierung)“ eingestellt ist.
  - Einen Weg, ohne KI mit dem Amazon-Titel zu listen, gibt es seit Version 46.0 nicht mehr.
- **Produkte aus dem Konkurrenz-Scanner:** Der eBay-Titel des Konkurrenten, gekürzt auf 80 Zeichen. Keine KI.

### 10.2 Länge

eBay erlaubt 80 Zeichen. Ist ein Titel länger, kürzt die Extension ihn auf 77 Zeichen und hängt „...“ an.

### 10.3 Titel enthält das Wort „error“

Enthält der fertige Titel das Wort „error“ (auch als Teil eines Wortes), bricht die Extension ab: „Titel-Erstellung fehlgeschlagen“.

### 10.4 Eingebauter Wortfilter

Die Extension hat eine eingebaute Liste mit Wörtern und Wendungen, die auf eBay Probleme machen können (z. B. „Garantie“, „CE“, „Original“, „Premium“). Diese werden aus **Titel, Beschreibung und Artikelmerkmalen** entfernt (nur ganze Wörter, Groß-/Kleinschreibung egal) – das Produkt wird trotzdem gelistet. Außerdem entfernt die Extension „IP“, „CE“ und „cert“ (Groß-/Kleinschreibung egal), wenn danach kein Buchstabe folgt – also das Wort allein und Angaben wie „IP67“ oder „CE-geprüft“. Diese Liste kannst du nicht selbst bearbeiten.

### 10.5 Titel nachträglich ändern

Der Browser-Lister ändert keine bestehenden Angebote. Titel änderst du direkt bei eBay.

## 11. Beschreibung

### 11.1 Eigene Vorlage oder schlichte Beschreibung

- **Wo:** Einstellungen → Reiter „Beschreibungsvorlage“ → Karte „Beschreibungsvorlage (HTML)“ (klein: „leer lassen = schlichte Beschreibung aus dem Produkttext“). Ein großes Textfeld für HTML-Code. Alles zur Vorlage auch in `references/einstellungen.md`.
- **Leeres Feld:** Die Extension baut eine schlichte Beschreibung ohne Design: Titel fett, die Stichpunkte als Liste, die Produktbeschreibung von Amazon.
- **Mit eigener Vorlage:** Deine Vorlage wird benutzt und die Platzhalter werden ersetzt.
- Eine KI-Beschreibung gibt es im Browser-Lister nicht; die Beschreibung entsteht immer aus Vorlage und Amazon-Daten. (Der Tab-Titel „Trage KI-Beschreibung ein“ heißt nur so.)

### 11.2 Platzhalter

| Platzhalter | wird ersetzt durch |
|---|---|
| `_TITLE_` | den eBay-Titel |
| `_ORIGINAL_TITLE_` | den ursprünglichen Amazon-Titel |
| `_MAIN_IMAGE_` | den Link zum ersten Bild, das schon bei eBay hochgeladen wurde |
| `_FEATURES_CONTENT_` | die Stichpunkte von Amazon als Liste |
| `_DESCRIPTION_CONTENT_` | die Produktbeschreibung von Amazon |
| `_SECTIONS_CONTENT_` | weitere Produktinfos – im Browser-Lister bleibt dieser Platzhalter nach aktuellem Stand leer |
| `_BEGIN_IMAGE_LIST_` … `_END_IMAGE_LIST_` | eine Bilderliste; der Teil zwischen `_BEGIN_IMAGE_ITEM_` und `_END_IMAGE_ITEM_` wird für jedes hochgeladene Bild wiederholt, `_IMAGE_URL_` ist darin der Bild-Link |
| `_BEGIN_x_SECTION_` … `_END_x_SECTION_` | ein Bereich, der ganz wegfällt, wenn sein Inhalt leer ist (für x: `FEATURES`, `DESCRIPTION`, `SECTIONS`, außerdem `TABLE`) |
| `_TABLE_CONTENT_` | steht nicht in der Feldbeschriftung; gedacht für die Tabelle der Produktinformationen – bleibt im Browser-Lister nach aktuellem Stand aber ebenfalls leer (ein Bereich `_BEGIN_TABLE_SECTION_` … `_END_TABLE_SECTION_` fällt also weg) |
| `_SPIELZEUG_WARNUNG_` | die Stelle, an der der Spielzeug-Warnhinweis erscheinen soll (steht nicht in der Feldbeschriftung, funktioniert aber) |

Beispiel: `_BEGIN_FEATURES_SECTION_<h3>Eigenschaften</h3>_FEATURES_CONTENT__END_FEATURES_SECTION_` – hat das Produkt keine Stichpunkte, verschwindet auch die Überschrift.

Die Bilder in der Beschreibung sind die Bilder, die bei eBay bereits hochgeladen wurden (eBay-Bildlinks), nicht die Amazon-Bilder.

### 11.3 Spielzeug-Warnhinweis

- Für jedes Produkt fragt die Extension die KI, ob es ein Spielzeug ist (bei beiden Quellen).
- Ist es ein Spielzeug, ist die KI unsicher, ist kein OpenAI-Schlüssel eingetragen oder kommt keine Antwort, wird der Warnhinweis eingefügt. Nur ein klares „kein Spielzeug“ verhindert ihn.
- Der Hinweis lautet (fett, auf Deutsch – auch auf anderen eBay-Domains):
  - „Achtung: Nicht für Kinder unter 36 Monaten geeignet“
  - „Achtung: Benutzung unter unmittelbarer Aufsicht von Erwachsenen“
  - „Achtung: Enthält Spielzeug. Beaufsichtigung durch Erwachsene empfohlen“
- Steht `_SPIELZEUG_WARNUNG_` in deiner Vorlage, erscheint der Hinweis dort (bei Nicht-Spielzeug wird der Platzhalter einfach entfernt). Sonst hängt er unten an.
- Ausschalten kannst du den Hinweis nicht.

### 11.4 Weitere Regeln

- Der eingebaute Wortfilter ([10.4](#104-eingebauter-wortfilter)) läuft auch über die Beschreibung.
- Bei „GPSR-Angaben übernehmen“ kann ein Text mit den Herstellerangaben unten angehängt werden (siehe [Abschnitt 17](#17-weitere-dinge-die-im-ebay-formular-passieren)).
- Ist die Beschreibung nach dem Filtern leer, oder lässt sie sich nicht in eBays Editor schreiben, bricht die Extension das Produkt ab, damit kein Angebot ohne Beschreibung online geht: „Beschreibung konnte nicht in den eBay-Editor geschrieben werden: … - Listing abgebrochen, damit es nicht leer online geht.“

## 12. Artikelmerkmale

Die Extension füllt die Merkmale in dieser Reihenfolge:

0. **Vorbelegte Merkmale aufräumen:** Hat eBay schon Merkmale vorbelegt, die ein Wort aus dem eingebauten Wortfilter enthalten ([10.4](#104-eingebauter-wortfilter)), leert die Extension diese Felder zuerst. Tab-Titel dabei: „⏳ Leere Merkmal: …“, danach „✅ Sperrbegriffe aus den Artikelmerkmalen entfernt“.
1. **eBays eigene Vorschläge übernehmen:** Zeigt eBay im Formular Merkmale an, die es selbst aus dem Titel erkannt hat, übernimmt die Extension alle davon.
2. **KI-Merkmale** (nur Produkte aus der Produkt-Datenbank, nur wenn „Pflicht-Artikelmerkmale mit KI ausfüllen“ an ist): Die KI füllt passende Merkmalfelder des Formulars (Pflichtfelder und weitere Felder; einige Felder schließt die Extension von vornherein aus) anhand der Produktdaten. Sie muss kein Feld füllen, zu dem im Produkttext nichts steht. Nummern wie EAN, UPC, GTIN, ISBN, MPN oder Herstellernummer erfindet die KI nicht. Tab-Titel: „⏰ KI erstellt die Artikelmerkmale … bitte warten …“.
3. **Leere Pflichtfelder:** Bleiben Pflichtfelder leer, trägt die Extension „Details In Description“ ein (in einem Feld mit der Bezeichnung „MPN“ mit Unterstrichen: „Details_In_Description“). Ausnahme: Ist „Pflicht-Artikelmerkmale mit KI ausfüllen“ an und gibt es einen KI-Suchbegriff (nur auf den Domains USA/CA/UK/AU), wird stattdessen dieser Suchbegriff eingetragen (auf höchstens 65 Zeichen gekürzt).
4. **Leere optionale Felder** (nur Produkte aus der Produkt-Datenbank, nur wenn „Optionale Artikelmerkmale mit KI ausfüllen“ an ist): Die Extension sieht sich etwa die ersten fünf optionalen Felder an (Felder für Länge, UPC/EAN/GTIN/ISBN/Barcode und „Device Charging Range“ lässt sie aus) und füllt die leeren davon mit dem KI-Suchbegriff. Einen solchen Suchbegriff gibt es nur auf USA/CA/UK/AU. Auf DE, FR, IT, ES und NL hat die Extension also keinen Wert, den sie dort eintragen könnte – sie schickt dann einen leeren Wert. **Nicht sicher belegt:** ob der Schalter auf diesen Domains bei eBay überhaupt etwas Sichtbares bewirkt.
5. **Merkmale von der Amazon-Seite:** Die Produktinformationen von Amazon werden eingetragen, bis zusammen etwa 43 Merkmale belegt sind. Wörter aus dem eingebauten Wortfilter werden entfernt; Merkmale mit problematischen Bezeichnungen fallen weg.
6. **Marke:** Die Extension trägt als Marke immer „Unbranded“ ein.
7. **EAN/UPC:** Auf UK, DE, FR, IT, ES, NL wird als EAN „Does not apply“ gesetzt, auf den anderen Domains als UPC „Does Not Apply“.

Felder zu Personalisierung und Kundenbewertung füllt die Extension nicht selbst aus.

**Die beiden Schalter** stehen in den Einstellungen, Reiter „Preise & Listing“, Karte „Artikelmerkmale (KI)“:
- „Pflicht-Artikelmerkmale mit KI ausfüllen“ – Standard: an. Schaltet das Ausfüllen durch die KI (Schritt 2) und den KI-Suchbegriff für leere Pflichtfelder (Schritt 3) ein.
- „Optionale Artikelmerkmale mit KI ausfüllen“ – Standard: an. Schaltet nur Schritt 4 ein.

Bei Produkten aus dem Konkurrenz-Scanner wirken beide Schalter nicht; leere Pflichtfelder bekommen dort immer „Details In Description“.

**Welches KI-Modell:** Für die Artikelmerkmale, den Suchbegriff und die Spielzeug-Prüfung nimmt die Extension das Modell aus den Einstellungen (Reiter „KI“, „OpenAI-Modell (für KI-Beschreibung & Generierung)“, Standard „gpt-4o-mini — Standard, günstig“). Nur der Titel läuft immer über gpt-4o-mini.

## 13. Custom Label / SKU

- **Was eingetragen wird:** In das eBay-Feld „Custom label (SKU)“ (eBay.de: „Bestandseinheit“) trägt die Extension eine **eigene Kennung** ein. Sie endet immer auf „==“.
- **Warum so:** Daran erkennt die Extension später, welches Amazon-Produkt zu deinem eBay-Angebot gehört – zum Beispiel der Tracker beim Abgleich von Preis und Bestand.
- **Ändere das Custom Label deiner Angebote nicht**, sonst kann die Extension das Angebot keinem Amazon-Produkt mehr zuordnen.
- **Feld ausgeblendet?** Ist das SKU-Feld in deinem eBay-Formular ausgeblendet, schaltet die Extension es selbst ein (Tab-Titel „Schalte SKU-Feld ein“). Klappt das nicht, geht das Angebot ohne Custom Label online – ohne Meldung. Ein solches Angebot kann die Extension später keinem Amazon-Produkt zuordnen.
- **Lupe auf der eBay-Artikelseite:** Öffnest du eines deiner eigenen Angebote auf eBay, steht vor dem Titel eine kleine violette Lupe („Amazon-Produkt öffnen“). Ein Klick öffnet das zugehörige Amazon-Produkt. Die Lupe erscheint nur, wenn eBay dir das Custom Label auf der Seite zeigt (eBay zeigt es nur dem Verkäufer). Der Amazon-Link richtet sich nach der Einstellung „Domain“.

## 14. Bilder

- **Titelbild (Bild 1):** Das erste Hauptbild der Amazon-Seite, das sich laden lässt (große Version bevorzugt). Lässt sich gar kein Bild laden, kommt der Amazon-Teil zu keinem Ergebnis und das Produkt schlägt nach Ablauf der Wartezeit ([8.2](#82-zeitgrenzen)) mit „Listen fehlgeschlagen – keine verwertbare Antwort der Amazon-Seite“ fehl.
- **Weitere Bilder:** Die übrigen Hauptbilder der Amazon-Seite (große Versionen; nur wenn es weniger als zwei große, aber mehr als zwei kleine gibt, die kleinen). Das Titelbild wird nicht doppelt hochgeladen. Bilder, die sich nicht laden lassen, werden übersprungen. Zu kleine Bilder werden auf mindestens 500 × 500 Pixel gebracht. Eine feste Höchstzahl legt die Extension nicht fest; bei sehr vielen Amazon-Bildern lässt sie am Ende ein bis zwei weg. **Nicht sicher belegt:** wie viele Bilder eBay im Einzelfall annimmt.
- **„Nur ein Bild bei eBay einstellen“** (Einstellungen → Reiter „eBay & Rahmenbedingungen“ → Karte „Beim Einstellen“, Standard aus): Nur das Titelbild wird hochgeladen (plus ggf. das GPSR-Bild).
- **Sammelbild (Collage):** Der Hinweis am Knopf „Starten“ sagt „ab vier Fotos dazu ein Sammelbild“. Bei Produkten aus der Produkt-Datenbank mit mindestens vier Bildern versucht die Extension, ein Sammelbild aus vier Produktbildern als Bild 2 zu erstellen. Dafür braucht sie ein Wasserzeichen-Bild, für das es in der Oberfläche kein Feld gibt. Ohne Wasserzeichen entfällt das Sammelbild ohne Fehlermeldung. Ein Wasserzeichen kann bei dir höchstens noch aus einer früheren Version, einer älteren Einstellungsdatei oder einer Sicherung stammen. **Nicht sicher belegt:** ob bei deiner Installation eins hinterlegt ist – frag im Zweifel den Betreiber.
- **GPSR-Bild:** Bei „GPSR-Angaben übernehmen“ lädt die Extension zusätzlich ein Bild hoch, das die Hersteller- und EU-Verantwortlichen-Angaben zeigt („GPSR“).
- **Fehlgeschlagene Uploads:** Zeigt eBay bei einem Bild „Fehler beim Hochladen“, entfernt die Extension die fehlerhaften Bilder über eBays Knopf „Fotos mit Fehlern entfernen“ und schickt sie erneut – bis zu zwei Durchgänge. Bleiben danach Bilder fehlerhaft, geht das Angebot trotzdem mit den übrigen Bildern online.

## 15. Preis beim Listen

### 15.1 Die Rechnung

Der Verkaufspreis entsteht aus dem **Amazon-Preis** der Produktseite:

1. **Aufschlag:** Verkaufspreis = Amazon-Preis + Amazon-Preis × (% Aufschlag ÷ 100) + fester Aufschlag.
2. **Preisendung:** Ist der Schalter bei „Preisendung“ an, wird auf den nächsten vollen Betrag **aufgerundet** und dann (1 − Endung) abgezogen.
3. Bei den Domains DE, FR, IT, ES, NL trägt die Extension den Preis mit Komma ein.

**Wo du das einstellst:** Einstellungen → Reiter „Preise & Listing“ → Karte „Preise“ (klein: „gilt beim Listen und im Tracker“):
- „% Aufschlag“ und „Fester Aufschlag (€)“.
- „Variable Preise (nach Preisspanne)“ – Schalter einschalten, dann legst du mit dem Knopf „Regel“ Regeln an. Jede Regel hat die Form „ab € … bis € … → … % + € …“ und einen Haken „Neu: Sonstige“; mit dem Knopf „Regel entfernen“ (×) am Ende löschst du sie. Die Regeln gelten nur, solange der Schalter „Variable Preise (nach Preisspanne)“ an ist. Gilt eine Regel für den Amazon-Preis (von–bis, jeweils einschließlich), ersetzt sie % und festen Aufschlag. Passt keine Regel, gelten die allgemeinen Werte.
- „Als „Neu: Sonstige“ listen (Standard)“ und „NUR „Neu: Sonstige“ listen“ – siehe [Abschnitt 16](#16-zustand-neu-oder-neu-sonstige).
- „Preisendung“ mit Zahlenfeld (Standard 0.99, erlaubt 0 bis 0.99) und Schalter daneben (Standard an). Ist der Schalter aus, ist das Zahlenfeld ausgegraut.

Jede Änderung wird sofort gespeichert und wirkt auch in einem laufenden Tracker. Eine zweite Preistafel nur für „Neu: Sonstige“ gibt es seit Version 46.0 nicht mehr: Eine Tafel gilt für alle Zustände.

Bei einer frischen Installation steht bei „% Aufschlag“ zunächst 120.

**Keine Währungsumrechnung:** Die Extension nimmt den Amazon-Preis als Zahl und rechnet nur deine Aufschläge dazu. Das „€“ in den Beschriftungen ist nur Beschriftung – listest du auf einer Domain mit anderer Währung, gelten die Zahlen in der Währung der Amazon-Seite.

### 15.2 Beispiele

- Amazon 10,00 €, 50 % Aufschlag, 2 € fest → 10 + 5 + 2 = 17,00 → Preisendung 0.99: aufrunden auf 17, minus 0,01 → **16,99 €**.
- Amazon 10,00 €, 50 %, 0 € fest → 15,00 → Preisendung 0.99 → **14,99 €**.
- Amazon 12,40 €, 0 % → 12,40 → Preisendung 0.49: aufrunden auf 13, minus 0,51 → **12,49 €**.
- Amazon 12,60 €, 0 % → 12,60 → Preisendung 0.49: aufrunden auf 13, minus 0,51 → **12,49 €** – also **unter** dem Aufschlagspreis. Bei einer Endung unter 0.99 kann der Preis durch die Rundung leicht sinken.
- Preisendung 0 → es wird nur auf volle Euro aufgerundet (12,60 → 13,00).
- Schalter bei „Preisendung“ aus → der Aufschlagspreis wird mit zwei Nachkommastellen genommen (12,60 → 12,60).

### 15.3 Mehrwertsteuer

- **Wo:** Einstellungen → Reiter „eBay & Rahmenbedingungen“ → Karte „Beim Einstellen“ → „Mehrwertsteuer im Angebot angeben“ (Standard aus) und darunter „Mehrwertsteuersatz … %“ (Standard 19).
- Ist der Schalter an und zeigt dein eBay-Formular ein Mehrwertsteuer-Feld, trägt die Extension den Prozentsatz dort ein. Fehlt das Feld in deinem Formular, passiert nichts. **Nicht sicher belegt:** bei welchen eBay-Konten eBay dieses Feld zeigt.

### 15.4 Was nicht verändert wird

Der Browser-Lister rechnet keine eBay-Gebühren in den Preis ein – es zählen nur deine Aufschläge. Er trägt keine Stückzahl ein (es gilt eBays Vorbelegung). **Nicht sicher belegt:** welche Stückzahl eBay bei dir vorbelegt.

**Wenn Amazon keinen Preis zeigt** (z. B. wenn die Buybox statt eines Preises nur auf andere Kaufoptionen verweist): Dann kann die Extension keinen Verkaufspreis berechnen, und das Preisfeld im eBay-Formular bleibt leer. Ist „Preis ab“ eingeschaltet, wird so ein Produkt schon auf der Amazon-Seite mit „Amazon-Preis zu niedrig (Filter „Preis ab“)“ übersprungen. **Nicht sicher belegt:** welche Meldung eBay zeigt, wenn das Formular ohne Preis abgeschickt wird.

### 15.5 Promoted Listing (Anzeigen)

- Bietet dein eBay-Formular die Option für Promoted Listings an, **schaltet die Extension sie immer ein** und setzt die Anzeigenrate.
- **Rate:** Einstellungen → Reiter „Preise & Listing“ → Karte „Listing“ → „Anzeigengebühr (%)“ (Standard 2.3, Feld von 2 bis 99).
- Einen Schalter, um das Bewerben in der Extension ganz abzuschalten, gibt es nicht.

## 16. Zustand: „Neu“ oder „Neu: Sonstige“

### 16.1 Wie entschieden wird

Auf eBays Seite „Passendes Produkt finden“ wählt die Extension den Zustand:

- **Standard:** „Neu“.
- **„Neu: Sonstige“**, wenn „Als „Neu: Sonstige“ listen (Standard)“ an ist (Einstellungen → Reiter „Preise & Listing“ → Karte „Preise“), oder – bei eingeschalteten variablen Preisen – wenn die passende Preisregel den Haken „Neu: Sonstige“ hat. Eine passende Regel hat Vorrang vor dem allgemeinen Schalter.
- Bietet die eBay-Kategorie „Neu: Sonstige“ nicht an, nimmt die Extension ersatzweise „Neu“.
- In manchen Kategorien (z. B. Kleidung) steht an der Stelle von „Neu: Sonstige“ der Zustand „Neu ohne Etikett“. Den wählt die Extension **nicht** als Ersatz – es gilt dann dasselbe wie „„Neu: Sonstige“ nicht vorhanden“.
- **Kachel-Auswahl** (z. B. Mode-Kategorien mit Zustandskacheln statt einer Liste): Die Extension wählt die Kachel „Neu mit Etikett“ und klickt auf Weiter. Findet sie die Kachel nach mehreren Versuchen nicht: „Zustand nicht wählbar: Kachel „Neu mit Etikett“ nicht gefunden“. Gesucht wird dabei nach der deutschen Beschriftung („Neu mit Etikett“ bzw. „Sonstige“); auf eBay-Seiten in anderen Sprachen findet sie die Kachel deshalb nicht.

### 16.2 „NUR „Neu: Sonstige“ listen“

- Schalter in den Einstellungen → Reiter „Preise & Listing“ → Karte „Preise“.
- Soll ein Produkt „Neu: Sonstige“ werden und die Kategorie bietet das nicht an, wird das Produkt **übersprungen** statt als „Neu“ gelistet: „„Neu: Sonstige" in dieser Kategorie nicht verfügbar (nur-Neu-Sonstige aktiv)“.
- Bei Kachel-Auswahl sucht die Extension dann eine Kachel mit „Sonstige“.

### 16.3 Zustandsbeschreibung

- **Wo:** Einstellungen → Reiter „eBay & Rahmenbedingungen“ → Karte „Neu: Sonstige“ → Feld „Zustandsbeschreibung“.
- **Vorgabe:** „Neuware. Die Originalverpackung wurde ggf. zur Prüfung geöffnet. Der Artikel ist unbenutzt, vollständig und voll funktionsfähig, ohne Gebrauchsspuren.“
- Wird eingetragen, wenn das eBay-Formular das Feld für die Zustandsbeschreibung zeigt (das ist bei „Neu: Sonstige“ der Fall). Höchstens 1000 Zeichen. Leeres Feld = keine Zustandsbeschreibung.

### 16.4 Kategorie

Die Kategorie suchst du nicht selbst aus: Die Extension übernimmt den ersten Kategorie-Vorschlag, den eBay anbietet. **Nicht sicher belegt:** welche Kategorie eBay im Einzelfall vorschlägt und ob eBay das Angebot einem Katalogprodukt zuordnet.

## 17. Weitere Dinge, die im eBay-Formular passieren

- **GPSR (Herstellerangaben):** Bei „GPSR-Angaben übernehmen“ versucht die Extension, Hersteller und verantwortliche Person in der EU in eBays Felder zu setzen. Gelingt das nicht direkt, hängt sie die Angaben als Text an die Beschreibung an und versucht es zusätzlich über eBays Formular für die Herstellerangaben. Dazu kommt das GPSR-Bild ([Abschnitt 14](#14-bilder)).
- **Erweiterte Versandoptionen:** Zeigt eBay den englischen Knopf „Switch to advanced options“, klickt die Extension ihn an.
- **Versand-, Zahlungs- und Rücknahmeangaben:** setzt der Browser-Lister nicht selbst; es gilt eBays Vorbelegung. Frühere Versionen hatten Einstellungen für Artikelstandort und Rücknahme-Richtlinie; diese sind nicht mehr sichtbar, wirken aber weiter, falls dort früher etwas eingetragen wurde (Tab-Titel dann „Setze Artikelstandort“ bzw. „Setze Rücknahmebedingungen“). **Nicht sicher belegt:** ob das bei dir der Fall ist – bei Fragen an den Betreiber wenden.
- **Keine geplante Einstellzeit mehr:** Die frühere Auswahl „Schedule Listing Time“ (Angebot erst zu einer bestimmten Uhrzeit online stellen) gibt es seit Version 46.0 nicht mehr. Angebote gehen sofort online, wenn sie abgeschickt werden.
- **Prüfung des Angebotsformats (Auktion/Sofort-Kaufen):** Zu dieser Prüfung gibt es keine Beschreibung – bei Fragen an den Betreiber wenden.

## 18. Absenden, Angebotsgebühren und Erfolg

### 18.1 Angebotsgebühren

- **Wo:** Einstellungen → Reiter „eBay & Rahmenbedingungen“ → Karte „Beim Einstellen“ → „Auch mit Angebotsgebühr einstellen“ (darunter klein: „automatisch absenden, auch wenn eBay Angebotsgebühren über 0 anzeigt“). **Standard:** aus.
- Zeigt eBay in der Zusammenfassung des Formulars eine Gebühr über 0 (in €, $ oder £), wird das Angebot **nicht** eingestellt, solange der Schalter aus ist. Meldung: „Nicht eingestellt: eBay verlangt Angebotsgebühren (Einstellung „Auch mit Angebotsgebühr einstellen“ ist aus)“. Das gilt auch, wenn „Listing automatisch absenden“ aus ist.
- Schalter an: Die Extension stellt auch bei angezeigter Gebühr ein – die Gebühren zahlst du an eBay.

### 18.2 „Listing automatisch absenden“

- **Wo:** Einstellungen → Reiter „Preise & Listing“ → Karte „Listing“. **Standard:** an.
- **An:** Die Extension klickt selbst auf eBays Knopf zum Einstellen.
- **Aus:** Das Formular wird fertig ausgefüllt (Tab-Titel „Bereit zum Einstellen!“) und wartet auf deinen Klick. Die Extension erkennt deinen Klick und meldet das Ergebnis. Ohne Klick innerhalb von 15 Minuten: „Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“. Für normale Läufe deshalb an lassen.

### 18.3 Wie Erfolg erkannt wird

- Nach dem Klick wartet die Extension bis zu etwa 20 Sekunden darauf, dass eBay im Formular-Tab die Erfolgsmeldung zeigt. Zusätzlich meldet eBays eigene Erfolgsseite den Erfolg an die Extension. Es zählt die Meldung, die zuerst ankommt.
- **Erfolg:** Status „gelistet“, Meldung „Erfolgreich gelistet!“, Tab-Titel „Angebot eingestellt!“, grünes Tab-Symbol. Erkennt die Extension den Erfolg im Formular-Tab, liest sie den Link zum neuen Angebot und schreibt ihn in die Spalte „eBay-Link“. Kommt die Meldung zuerst von eBays Erfolgsseite, enthält sie keinen Link – die Spalte „eBay-Link“ bleibt dann leer. Ein leeres Feld ist also kein Fehler; das Angebot findest du in deinem eBay-Verkäuferbereich. **Nicht sicher belegt:** wie oft welcher der beiden Wege zuerst ankommt.
- **Kein Erfolg:** Die Extension liest eBays sichtbare Fehlermeldungen von der Seite und schreibt sie zusammen mit der Seitenadresse in den Statusbericht. Findet sie keine, steht dort „Einstellen fehlgeschlagen, eBay nennt keinen Grund: <Adresse>“. Tab-Titel „Einstellen fehlgeschlagen!“, rotes Tab-Symbol.

## 19. Produktvergabe beim Listen

**Wozu:** Die Produktvergabe verhindert, dass mehrere Kunden dasselbe Amazon-Produkt auf eBay listen und sich gegenseitig Konkurrenz machen. Ist ein Produkt schon an einen anderen Kunden vergeben, kannst du es nicht listen. (Davon zu unterscheiden ist „In Arbeit“: Das verhindert, dass zwei **deiner eigenen** Geräte dasselbe Produkt gleichzeitig listen, siehe [Abschnitt 6](#6-die-produkt-datenbank-beim-listen-entnahme-in-arbeit-server-ausfall).)

**Produkte aus der Produkt-Datenbank:**
1. Schon beim Import in die Produkt-Datenbank werden sie für dich reserviert. Produkte, die schon einem anderen Kunden gehören, kommen gar nicht erst in deine Liste.
2. Beim Listen prüft der Browser-Lister nicht noch einmal einzeln – das Produkt ist ja schon reserviert und „In Arbeit“.
3. Wird das Angebot erfolgreich eingestellt, wird die Zuordnung für dich bestätigt.
4. Schlägt das Listen fehl, wird die Reservierung freigegeben – das Produkt ist dann auch für andere wieder frei.

**Produkte aus dem Konkurrenz-Scanner:**
1. Schon wenn der Konkurrenz-Scanner etwas findet, werden die Funde für dich reserviert.
2. Beim Listen prüft der Browser-Lister vor jedem Fund noch einmal. Ist er inzwischen einem anderen Kunden zugeordnet, öffnet der Browser-Lister gar keine Tabs. Im Statusbericht steht dann „fehlgeschlagen“ mit „Produkt bereits von einem anderen Nutzer vergeben“. Er zählt bei „fehlgeschlagen“ und ist aus der Liste entfernt.
3. Erfolg bestätigt, Fehlschlag gibt frei – wie oben.
4. Liste Scanner-Funde nur, wenn unten in der Seitenleiste „Server verbunden“ steht. Ohne Verbindung kann die Produktvergabe nicht prüfen, ob ein anderer Kunde das Produkt schon hat.

**Wo du den Zustand siehst:**
- **Seitenleiste unten:** „Produkt-Vergabe aktiv“ (alles in Ordnung) bzw. „Produkt-Vergabe aus“ (nicht angemeldet, Zugang abgeschaltet oder Abo gesperrt).
- **Einstellungen → Reiter „eBay & Rahmenbedingungen“ → Karte „Server & Produkt-Vergabe“** (klein: „verhindert doppeltes Listen“): eine Statuszeile, z. B. „● Produkt-Vergabe: AN (über deine Anmeldung)“ (alles in Ordnung) oder „● Produkt-Vergabe: AUS – keine Server-Adresse hinterlegt.“ – **trotz des Wortlauts heißt das in der Praxis: du bist nicht angemeldet.** Dann im Dashboard anmelden und die Einstellungsseite neu laden; selbst keine Adresse eintragen. (Den Text „● Produkt-Vergabe: AUS – nicht angemeldet. Es wird NICHTS reserviert!“ gibt es auch, er erscheint im aktuellen Stand aber praktisch nie.) Mit dem Knopf „Verbindung prüfen“ testest du die Verbindung; bei Erfolg steht dort „OK – angemeldet als „…“, … Produkte reserviert.“. Darunter der Hinweis „Achtung: Ohne Anmeldung ist die Produkt-Vergabe komplett aus.“ – melde dich deshalb immer an, bevor du importierst oder listest. Das Feld „Server-Adresse“ änderst du nur, wenn der Betreiber es dir sagt.

**Wenn du unsicher bist, ob die Produktvergabe läuft:** Prüfe es mit „Verbindung prüfen“. Meldet die Prüfung eine Störung, wende dich an den Betreiber.

## 20. Doppelte Angebote vermeiden

Es gibt vier voneinander unabhängige Schutzmechanismen:

1. **Eigene Doppelt-Liste („Produkt ist schon gelistet (Duplikat)“):** Die Extension merkt sich in deinem Chrome-Profil die Produkte, die sie erfolgreich eingestellt hat. Kommt dasselbe Produkt noch einmal, wird es übersprungen. Diese Liste gilt nur für dieses Chrome-Profil, du kannst sie in der Oberfläche nicht einsehen oder leeren, und sie wird weder beim Exportieren der Einstellungen noch bei der Sicherung mitgenommen. Eingetragen wird ein Produkt nur, wenn die Extension den Erfolg selbst im eBay-Formular-Tab erkennt (siehe [18.3](#183-wie-erfolg-erkannt-wird)). **Nicht sicher belegt:** ob deshalb einzelne erfolgreiche Angebote in dieser Liste fehlen.
2. **Produktvergabe** gegen Doppel-Listings zwischen verschiedenen Kunden ([Abschnitt 19](#19-produktvergabe-beim-listen)).
3. **„In Arbeit“** gegen gleichzeitiges Listen desselben Produkts auf zwei deiner Geräte ([Abschnitt 6](#6-die-produkt-datenbank-beim-listen-entnahme-in-arbeit-server-ausfall)).
4. **Bildabgleich (optional):** Einstellungen → Reiter „Produkt-Filter“ → Karte „Beim Listen“ → „Bildabgleich gegen fremde Angebote“ (darunter klein: „überspringt Produkte, die auf eBay schon jemand anders anbietet“). **Standard:** aus.
   - **Wie es funktioniert:** Auf eBays Seite „Passendes Produkt finden“ zeigt eBay vergleichbare Angebote anderer Verkäufer. Die Extension vergleicht das Amazon-Hauptbild mit bis zu 8 dieser Bilder. Ist eines (fast) gleich, wird das Produkt übersprungen: „Übersprungen: dieses Amazon-Produkt wird auf eBay bereits von jemand anderem angeboten (Bildabgleich, Abstand N)“.
   - **Wie streng:** Der erlaubte Bildabstand ist seit Version 46.0 fest eingestellt (15; je kleiner, desto ähnlicher müssen die Bilder sein). Ein Feld dafür gibt es nicht mehr.
   - Zeigt eBay keine Vergleichsangebote oder klappt der Vergleich nicht, wird gelistet.

Zusätzlich prüft die Produkt-Datenbank beim Import gegen deine hinterlegten Google-Sheets (siehe `references/produkte-finden-und-datenbank.md`).

## 21. eBay-Verkaufslimit

- Eine Anzeige deines eBay-Verkaufslimits (wie viele Angebote oder welcher Wert schon verbraucht ist und wie viel erlaubt ist) gibt es im Browser-Lister **nicht**.
- Lehnt eBay das Einstellen ab, übernimmt die Extension eBays sichtbaren Fehlertext in die Spalte „Meldung“. **Nicht sicher belegt:** mit welchem genauen Text eBay ein erreichtes Verkaufslimit meldet.
- Die Zeitschaltung ([5.13](#513-karte-zeitschaltung)) hilft, das Listen über den Tag bzw. mehrere Tage zu verteilen. Sie zählt nur erfolgreiche Angebote.
- Fragen zu eBays Limits selbst beantwortet eBay; das ist allgemeines eBay-Wissen, nicht Teil von Cash Lister.

## 22. Sicherheitsabfragen (Captcha) bei Amazon und eBay

- **Amazon:** Zeigt Amazon eine Sicherheitsabfrage, kann die Extension sie **nicht** für dich lösen. Löse sie im Amazon-Tab selbst: Die Extension schickt ihren Schritt erneut, sobald die Seite danach fertig geladen ist, und macht dann weiter. Das muss innerhalb der Wartezeit des Amazon-Teils passieren ([8.2](#82-zeitgrenzen)); sonst gilt das Produkt als fehlgeschlagen („Listen fehlgeschlagen – keine verwertbare Antwort der Amazon-Seite“). Bei mehreren gleichzeitigen Durchgängen und vielen Abfragen ist das kaum zu schaffen – dann besser eine kleinere Zahl bei „Gleichzeitig“. **Nicht sicher belegt:** ob es nach dem Lösen in jedem Fall weitergeht.
- **eBay:** Zeigt eBay eine Sicherheitsseite, löse sie im eBay-Tab selbst. Die Extension schickt ihren Schritt nach dem Neuladen der Seite erneut. **Nicht sicher belegt:** ob es danach in jedem Fall weitergeht; spätestens nach 15 Minuten gilt das Produkt als fehlgeschlagen.
- Häufen sich Sicherheitsabfragen: eine kleinere Zahl bei „Gleichzeitig“ verwenden.

## 23. Der Statusbericht und alle Meldungen

### 23.1 Die Seite

- **Öffnen:** Im Browser-Lister rechts oben auf „Statusbericht“. Der Tab heißt „Cash Lister – Browser-Lister-Statusbericht“, oben steht „Statusbericht“ und darunter „Browser-Lister · jedes Produkt des aktuellen bzw. letzten Laufs mit Ergebnis“. Ist der Statusbericht schon offen, springt der Klick dorthin.
- **Die Liste aktualisiert sich nicht von selbst.** Für neue Einträge die Seite neu laden (F5) – auch nach einem Sprung in den schon offenen Tab.
- **Leer:** Steht noch nichts drin, zeigt die Seite „Noch keine Einträge – sie entstehen, sobald ein Lauf Produkte abarbeitet.“
- **Knopf „Leeren“** (unten): Leert die Liste sofort (ohne Rückfrage) und lädt die Seite neu.
- **Geleert wird sie außerdem** bei jedem Start eines Laufs und bei „Stoppen & zurücksetzen“. Sie bleibt auch nach einem Browser-Neustart erhalten, bis eines davon passiert.
- Der Statusbericht gilt nur für dieses Gerät. Läufe auf anderen Geräten stehen dort nicht.

### 23.2 Die Spalten

| Spalte | Inhalt |
|---|---|
| „#“ | laufende Nummer |
| „Amazon-Link“ | der Amazon-Link des Produkts (anklickbar; lange Links enden mit „…“, der Klick öffnet trotzdem den ganzen Link) |
| „Status“ | „gelistet“ (grün) = eingestellt; „fehlgeschlagen“ (rot) = nicht eingestellt; „Hinweis“ = keine Produktzeile, sondern ein Hinweis zum Lauf (z. B. Server-Pause) |
| „Meldung“ | die Meldung bzw. der Grund |
| „eBay-Link“ | der Link zum neuen eBay-Angebot, wenn er gelesen werden konnte |

Bei manchen Zeilen hängt an der Meldung ein Zusatz mit „· Format geprüft: …“ oder „· Format-Prüfung: keine Rückmeldung“. Zu dieser Prüfung gibt es keine Beschreibung – bei Fragen an den Betreiber wenden.

### 23.3 Alle Meldungen: Bedeutung und was du tun kannst

**Erfolg**

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Erfolgreich gelistet!“ | Angebot ist eingestellt | nichts |

**Hinweise zum Lauf** (Status „Hinweis“, ohne Amazon-Link)

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Server nicht erreichbar – Lister pausiert, macht von selbst weiter.“ (ggf. mit „(Produkt-Datenbank noch nicht bereit).“ oder „(HTTP …).“) | Der Lauf wartet auf den Server | nichts; dauert es lange, an den Betreiber wenden ([6.5](#65-wenn-der-server-nicht-erreichbar-ist-pause)) |
| „Server wieder erreichbar – Lister läuft weiter (Pause etwa N Min.).“ | Die Pause ist vorbei | nichts |
| „Browser-Lister beendet: … Danach neu starten.“ | Lauf vorzeitig beendet (abgemeldet, Sitzung abgelaufen, Zugang abgeschaltet, Abo gesperrt, Anfrage abgelehnt) | siehe Tabelle in [6.6](#66-abgemeldet-zugang-abgeschaltet-oder-abo-gesperrt-während-des-laufs) |

**Vor dem Öffnen der Tabs**

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Produkt bereits von einem anderen Nutzer vergeben“ | Ein anderer Kunde hat dieses Produkt (nur bei Konkurrenz-Scanner-Funden) | nichts; das Produkt ist nicht für dich |
| „Abgebrochen: …“ | Ein unerwarteter Fehler beim Öffnen der Tabs oder im Ablauf; die Reservierung wurde freigegeben | Produkt neu importieren und erneut versuchen; tritt es oft auf, an den Betreiber wenden |

**Auf der Amazon-Seite** (siehe auch [Abschnitt 9](#9-prüfungen-auf-der-amazon-seite-vor-dem-listen-buyboxfba-und-mehr))

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Produktseite existiert nicht“ | Keine richtige Produktseite (Produkt weg, Seite nicht geladen, Fehlerseite) | Link im Browser öffnen und prüfen |
| „Produkt ist schon gelistet (Duplikat)“ | Schon einmal aus diesem Chrome-Profil erfolgreich gelistet | nichts; Absicht |
| „Produkt enthält ein Wort aus der Blacklist: …“ | Wort aus deiner Blacklist gefunden | Liste in den Einstellungen prüfen, falls das Wort nicht gemeint war |
| „ASIN und Adresse (URL) passen nicht zusammen“ | Amazon hat auf ein anderes Produkt/eine andere Variante umgeleitet | Link prüfen, ggf. die richtige Variante neu importieren |
| „Produkt hat eine Mindestbestellmenge“ | Mindestbestellmenge über 1 | nichts |
| „Produkt ist nicht auf Lager“ | Nicht auf Lager oder Lieferzeit länger als „Max. verlängerte Lieferzeit“ | ggf. später erneut versuchen; Grenze in den Einstellungen prüfen |
| „Produkt wird international versendet“ | Internationale Lieferung | nichts |
| „Nicht von Amazon versendet (Versand: …)“ | Händler verschickt selbst, „Nur FBA“ ist an | nichts, oder „Nur FBA“ ausschalten |
| „Versender auf der Produktseite nicht erkennbar“ | Die Extension findet in der Buybox keine Versandangabe | Seite selbst ansehen; tritt es bei vielen Produkten auf, an den Betreiber wenden |
| „Produkt hat keinen kostenlosen Versand“ | Kein kostenloser Versand in der Buybox | nichts |
| „Produkt ist gebraucht“ | Buybox ist ein Gebraucht-Angebot | nichts |
| „Amazon-Preis zu hoch (Filter „Preis bis“)“ | Amazon-Preis über „Preis bis“ | Schalter/Wert „Preis bis“ prüfen ([9.4](#94-preis-ab-und-preis-bis)) |
| „Amazon-Preis zu niedrig (Filter „Preis ab“)“ | Amazon-Preis unter „Preis ab“ (oder Amazon zeigt keinen Preis) | Schalter/Wert „Preis ab“ prüfen |
| „Kein chinesischer Verkäufer“ | „Nur chinesische Verkäufer“ ist an, Verkäufer ist nicht aus CN/HK | nichts, oder Filter ausschalten |
| „Keine GPSR-Angaben gefunden“ | „GPSR-Angaben übernehmen“ ist an, Amazon zeigt keine Herstellerangaben | nichts, oder Filter ausschalten |
| „nicht angemeldet“ (dazu im Amazon-Tab das Fenster „Nicht angemeldet - bitte im Dashboard anmelden.“) | Deine Anmeldung ist während des Laufs weggefallen (auch: Zugang abgeschaltet, Abo gesperrt) | im Dashboard neu anmelden, Lauf neu starten |
| „KI-Titel ist leer“ | Die KI hat auch nach mehreren Versuchen keinen Titel geliefert | OpenAI-Schlüssel, OpenAI-Guthaben und -Konto prüfen ([26](#26-probleme-und-lösungen)) |
| „Titel-Erstellung fehlgeschlagen“ | Der Titel enthielt das Wort „error“ | erneut versuchen |
| „Listen fehlgeschlagen – keine verwertbare Antwort der Amazon-Seite“ | Der Amazon-Tab hat innerhalb der Wartezeit ([8.2](#82-zeitgrenzen)) kein Ergebnis geliefert (Seite lädt nicht, kein Bild ladbar, Sicherheitsabfrage nicht gelöst, KI zu langsam, unerwarteter Fehler) | Link selbst öffnen und prüfen; erneut versuchen |
| „OpenAI-Guthaben leer: kein Guthaben mehr auf dem OpenAI-Konto. Bitte unter platform.openai.com unter Billing Guthaben aufladen.“ | steht statt der Meldung darüber, wenn kurz vorher dieser KI-Fehler auftrat | Guthaben bei OpenAI aufladen |
| „OpenAI: API-Key ungültig oder abgelaufen – bitte prüfen (Einstellungen → KI → „OpenAI-API-Schlüssel“).“ | dito, Schlüssel falsch | Schlüssel in den Einstellungen neu eintragen |
| „OpenAI: Rate-Limit (zu viele Anfragen) – kurz warten und erneut versuchen.“ | dito, zu viele Anfragen | kleinere Zahl bei „Gleichzeitig“, später erneut |
| „OpenAI hat innerhalb von 90 Sekunden nicht geantwortet.“ | dito, keine Antwort | später erneut |
| „OpenAI nicht erreichbar: …“ / „OpenAI <Zahl>: …“ | dito, sonstiger KI-Fehler | Internet prüfen, später erneut |

**Auf eBay**

| Meldung | Bedeutung | Was tun |
|---|---|---|
| „Übersprungen: dieses Amazon-Produkt wird auf eBay bereits von jemand anderem angeboten (Bildabgleich, Abstand N)“ | Bildabgleich hat ein gleiches Angebot gefunden | nichts; oder „Bildabgleich gegen fremde Angebote“ ausschalten |
| „„Neu: Sonstige" in dieser Kategorie nicht verfügbar (nur-Neu-Sonstige aktiv)“ | „NUR „Neu: Sonstige“ listen“ an, Kategorie hat kein „Neu: Sonstige“ | nichts, oder den Schalter ausschalten |
| „Zustand nicht wählbar: Kachel „Neu mit Etikett“ nicht gefunden“ | Bei der Zustands-Kachelauswahl wurde „Neu mit Etikett“ nicht gefunden | nichts; Produkt passt nicht ([16.1](#161-wie-entschieden-wird)) |
| „Nicht eingestellt: Fehler beim Ausfüllen des eBay-Formulars (Schritt „…"): …“ | Beim Ausfüllen ist etwas schiefgegangen; der Schritt steht in der Meldung | erneut versuchen; tritt es oft beim selben Schritt auf, die Meldung an den Betreiber schicken |
| „Beschreibung konnte nicht in den eBay-Editor geschrieben werden: … - Listing abgebrochen, damit es nicht leer online geht.“ | Beschreibung leer oder nicht übernommen | Vorlage prüfen (leer nach Wortfilter?); erneut versuchen |
| „Nicht eingestellt: eBay verlangt Angebotsgebühren (Einstellung „Auch mit Angebotsgebühr einstellen“ ist aus)“ | eBay zeigt eine Angebotsgebühr über 0 | Gebühr bei eBay prüfen; ggf. Schalter in den Einstellungen setzen ([18.1](#181-angebotsgebühren)) |
| Andere Meldungen, die mit „Nicht eingestellt:“ beginnen und das Angebotsformat, „Auktion“ oder „Sofort-Kaufen“ nennen | Zu dieser Prüfung gibt es keine Beschreibung – bei Fragen an den Betreiber wenden. | an den Betreiber wenden |
| eBays eigener Fehlertext + Seitenadresse | eBay hat das Einstellen abgelehnt | Text lesen; im eBay-Tab nachsehen (dafür „Fehler-Tabs schließen“ ausschalten) |
| „Einstellen fehlgeschlagen, eBay nennt keinen Grund: <Adresse>“ | Nach dem Klick keine Erfolgsseite, kein lesbarer Fehlertext | Angebot in deinem eBay-Verkäuferbereich suchen (evtl. doch eingestellt oder als Entwurf); erneut versuchen |
| „eBay-Fehlerseite - Angebot nicht eingestellt“ | eBay hat eine Fehlerseite des Angebotsformulars gezeigt | erneut versuchen |
| „eBay-Serverfehler (upstream connect error) - Angebot nicht eingestellt“ | eBay-Seite mit Verbindungsfehler | später erneut versuchen |
| „Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“ | Der eBay-Teil hat 15 Minuten lang kein Ergebnis gemeldet | siehe [Probleme und Lösungen](#26-probleme-und-lösungen): eBay-Anmeldung, Sicherheitsabfrage, „Listing automatisch absenden“ |

### 23.4 Alte Meldungen (bis Version 45.5) und ihre neuen Namen

Seit Version 46.0 sind alle Meldungen deutsch. Schickt dir jemand einen Screenshot aus einer älteren Version, hilft diese Tabelle:

| Bis 45.5 | Seit 46.0 |
|---|---|
| „itemListed“ / „itemFailed“ (Spalte Status) | „gelistet“ / „fehlgeschlagen“ |
| „Item Listed Successfully!“ | „Erfolgreich gelistet!“ |
| „Page doesnt exist“ | „Produktseite existiert nicht“ |
| „Item is duplicate“ | „Produkt ist schon gelistet (Duplikat)“ |
| „Item contains blacklisted word: …“ | „Produkt enthält ein Wort aus der Blacklist: …“ |
| „ASIN and URL are not the same“ | „ASIN und Adresse (URL) passen nicht zusammen“ |
| „min order qty item“ | „Produkt hat eine Mindestbestellmenge“ |
| „Item is not in stock“ | „Produkt ist nicht auf Lager“ |
| „Item is international“ | „Produkt wird international versendet“ |
| „Item doesnt have free shipping“ | „Produkt hat keinen kostenlosen Versand“ |
| „Item is used“ | „Produkt ist gebraucht“ |
| „Price is too high“ / „Price is too low“ | „Amazon-Preis zu hoch (Filter „Preis bis“)“ / „Amazon-Preis zu niedrig (Filter „Preis ab“)“ |
| „Not a Chinese seller“ | „Kein chinesischer Verkäufer“ |
| „not gpsr item“ | „Keine GPSR-Angaben gefunden“ |
| „Title is undefined“ | „KI-Titel ist leer“ |
| „Title generation error“ | „Titel-Erstellung fehlgeschlagen“ |
| „Auto listing failed“ | „Listen fehlgeschlagen – keine verwertbare Antwort der Amazon-Seite“ |
| „Condition Grading Error, not supported“ | „Zustand nicht wählbar: Kachel „Neu mit Etikett“ nicht gefunden“ |
| „insertion fees“ | „Nicht eingestellt: eBay verlangt Angebotsgebühren (Einstellung „Auch mit Angebotsgebühr einstellen“ ist aus)“ |
| „Item Failed to List! <Adresse>“ | „Einstellen fehlgeschlagen, eBay nennt keinen Grund: <Adresse>“ |
| „Ebay Error Page“ | „eBay-Fehlerseite - Angebot nicht eingestellt“ |
| „upstream connect error or disconnect/reset before headers. …“ | „eBay-Serverfehler (upstream connect error) - Angebot nicht eingestellt“ |
| „timeout: no response after 15 minutes“ | „Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“ |

## 24. Tab-Titel und Tab-Symbole während des Listens

Der Titel der Arbeits-Tabs zeigt, wo die Extension gerade ist. Das hilft, einen hängenden Schritt zu finden.

**Amazon-Tab – Warnungen schon beim Laden der Seite:**
Sobald eine Amazon-Produktseite lädt (auch wenn du selbst surfst), schreibt die Extension Hinweise vor den Tab-Titel, z. B. „WARNUNG! KEIN PRIME - ZUM LISTEN BESTÄTIGEN -“, „WARNUNG! NICHT AUF LAGER - ZUM LISTEN BESTÄTIGEN -“, „WARNUNG! LIEFERZEIT VERLÄNGERT - ZUM LISTEN BESTÄTIGEN -“, „WARNUNG! KEIN KOSTENLOSER VERSAND - ZUM LISTEN BESTÄTIGEN -“, „WARNUNG! GEBRAUCHT - ZUM LISTEN BESTÄTIGEN -“, „WARNUNG! INTERNATIONALER VERSAND - ZUM LISTEN BESTÄTIGEN -“, „WARNUNG! MINDESTBESTELLMENGE … - ZUM LISTEN BESTÄTIGEN -“, „WARNUNG! ASIN PASST NICHT ZUR ADRESSE - ZUM LISTEN BESTÄTIGEN -“ oder „⚠️ BLACKLIST-WORT GEFUNDEN: …“. Kurz kann auch nur das gefundene Blacklist-Wort im Tab-Titel stehen. Diese Hinweise allein bedeuten noch nicht, dass das Produkt übersprungen wird – „KEIN PRIME“ zum Beispiel ist beim Listen gar keine Prüfung mehr. Maßgeblich ist, was im Statusbericht steht.

**Amazon-Tab – während der Prüfungen und danach:**
- „Prüfe chinesischen Verkäufer...“ – Verkäuferprüfung.
- „Auto-Listing - <ASIN>“ – die Prüfungen bis zur Verkäuferprüfung sind bestanden.
- „Hole GPSR-Angaben...“ / „GPSR-Angaben erhalten!“ – GPSR-Angaben. Dazwischen können kurz Zwischenstände stehen (z. B. „GPSR 1: Knopf „Sicherheitskontakte“ nicht gefunden“, „GPSR 2: Sicherheitskontakte geöffnet, warte auf die Herstellerangaben“).
- „Auto-Listing - KI-Titel wird erstellt...- <ASIN>  KI-Titel wird erstellt...“ – Titel wird erstellt.
- „Auto-Listing - <ASIN>  Erstelle Bild...“ – Titelbild wird geladen.
- „Wird bei eBay gelistet: <Titel> - <ASIN>  ...“ – Amazon-Teil fertig, eBay-Teil beginnt (Tab-Symbol: Pfeil).

**Amazon-Tab – Titel, bei denen das Produkt übersprungen wird** (jeweils mit Warn-Symbol, bei der Blacklist mit Totenkopf; „ZUM LISTEN BESTÄTIGEN“ heißt hier nichts, du musst nichts bestätigen):

| Tab-Titel beginnt mit | Meldung im Statusbericht |
|---|---|
| „WARNUNG! SEITE EXISTIERT NICHT“ | „Produktseite existiert nicht“ |
| „WARNUNG! SCHON GELISTET (DUPLIKAT) - ZUM LISTEN BESTÄTIGEN -“ | „Produkt ist schon gelistet (Duplikat)“ |
| „⚠️ WARNUNG! PRODUKT ENTHÄLT BLACKLIST-WÖRTER (…) - ZUM LISTEN BESTÄTIGEN -“ | „Produkt enthält ein Wort aus der Blacklist: …“ |
| „WARNUNG! ASIN PASST NICHT ZUR ADRESSE - ZUM LISTEN BESTÄTIGEN -“ | „ASIN und Adresse (URL) passen nicht zusammen“ |
| „ÜBERSPRUNGEN! Mindestbestellmenge“ | „Produkt hat eine Mindestbestellmenge“ |
| „WARNUNG! NICHT AUF LAGER - ZUM LISTEN BESTÄTIGEN -“ | „Produkt ist nicht auf Lager“ |
| „WARNUNG! INTERNATIONALER VERSAND - ZUM LISTEN BESTÄTIGEN -“ | „Produkt wird international versendet“ |
| „WARNUNG! NICHT FBA - ZUM LISTEN BESTÄTIGEN -“ | „Nicht von Amazon versendet (Versand: …)“ bzw. „Versender auf der Produktseite nicht erkennbar“ |
| „WARNUNG! KEIN KOSTENLOSER VERSAND - ZUM LISTEN BESTÄTIGEN -“ | „Produkt hat keinen kostenlosen Versand“ |
| „WARNUNG! GEBRAUCHT - ZUM LISTEN BESTÄTIGEN -“ | „Produkt ist gebraucht“ |
| „WARNUNG! PREIS ZU HOCH - ZUM LISTEN BESTÄTIGEN -“ | „Amazon-Preis zu hoch (Filter „Preis bis“)“ |
| „WARNUNG! PREIS ZU NIEDRIG - ZUM LISTEN BESTÄTIGEN -“ | „Amazon-Preis zu niedrig (Filter „Preis ab“)“ |
| „WARNUNG! KEIN CHINESISCHER VERKÄUFER - ZUM LISTEN BESTÄTIGEN -“ | „Kein chinesischer Verkäufer“ |
| „ÜBERSPRUNGEN! keine GPSR-Angaben“ | „Keine GPSR-Angaben gefunden“ |
| „Auto-Listing - <ASIN>  FEHLER! Titel ist leer!“ | „KI-Titel ist leer“ |
| „Auto-Listing - <ASIN>  FEHLER! Titel-Erstellung fehlgeschlagen!“ | „Titel-Erstellung fehlgeschlagen“ |
| „Auto-Listing - <ASIN>  FEHLER! Nicht angemeldet!“ | „nicht angemeldet“ |

**eBay-Tab:**
- „eBay-Produktsuche“, „eBay-Produktsuche - Start“, „eBay-Produktsuche - Start - Suchbegriff wird ermittelt“, „eBay-Produktsuche - Suchbegriff eingetragen“, „eBay-Produktsuche - fertig“ – Einstiegsseite, der Suchbegriff wird eingetragen. „eBay-Produktsuche - Titel fehlt im Suchfeld, neuer Versuch“ – der erste Versuch hat nicht gegriffen, die Extension trägt den Titel erneut ein.
- „eBay: Produkt zuordnen“ – Seite „Passendes Produkt finden“ (Bildabgleich, Zustand, Kategorie).
- „Skript eingefügt“ – das Ausfüllen des Formulars beginnt gleich.
- „⏳ Leere Merkmal: …“, „✅ Sperrbegriffe aus den Artikelmerkmalen entfernt“ – vorbelegte Merkmale mit gefilterten Wörtern werden geleert.
- „Lade ausgewähltes Bild hoch“, „Lade Bilder hoch“, „Lade Sammelbild hoch!“, „Lade Bild x/y zu eBay hoch“, „Bilder hochgeladen“ – Bilder.
- „Produkt wird eingetragen“, „Knopf „Mehr anzeigen“ gefunden“ / „… geklickt“, „Trage Titel ein“, „Trage GPSR-Angaben ein“, „GPSR gesetzt: …“, „Trage Artikelmerkmale ein“, „⏰ KI erstellt die Artikelmerkmale … bitte warten …“, „⏳ Merkmal „…“: …“ / „✔️ Merkmal „…“: …“ / „❌ Merkmal „…“: …“, „⏳ Eigenes Merkmal „…“: …“, „⏳ Schließe Dialoge“ / „⏳ Dialoge noch offen“ / „✔️ Dialoge geschlossen“, „Trage UPC/EAN ein“, „Trage Preis ein“, „Schalte SKU-Feld ein“, „Trage SKU ein“, „Trage KI-Beschreibung ein“, „Füge GPSR-Angaben zur Beschreibung hinzu“, „Beschreibung: warte auf eBay-Speicherung“, „Beschreibung: geschrieben“, „Richte Anzeige ein (Promoted Listing)“, „Wechsle zu den erweiterten Versandoptionen“, „Trage Zustandsbeschreibung ein“ – das Formular wird gefüllt. („Trage KI-Beschreibung ein“ heißt nur so; die Beschreibung kommt aus deiner Vorlage, nicht von der KI.)
- „Bereit zum Einstellen!“ – fertig ausgefüllt.
- „Angebot eingestellt!“ mit grünem Symbol – eingestellt.
- „Einstellen fehlgeschlagen!“ mit rotem Symbol – nicht eingestellt (auch auf eBays Fehlerseite des Formulars).
- „Beschreibung fehlgeschlagen“, „Abgebrochen: Fehler beim Ausfuellen“ – abgebrochen.
- „Nicht eingestellt: kein Sofort-Kaufen“ – gehört zur Prüfung des Angebotsformats. Zu dieser Prüfung gibt es keine Beschreibung – bei Fragen an den Betreiber wenden.

Während die Extension arbeitet, zeigt der Tab ein bewegtes Symbol.

## 25. Häufige Fragen

**Wo ist der Bulk-Lister?**
Er heißt seit Version 46.0 „Browser-Lister“. Du öffnest ihn über das Dashboard (Karte „Browser-Lister“) oder die Seitenleiste („Browser-Lister“ in der Gruppe „Arbeiten“).

**Wie viele Produkte kann ich auf einmal listen?**
So viele, wie in der Quelle frei sind. Du stellst bei „Wie viele Angebote“ die Zahl der erfolgreichen Angebote ein; eine feste Obergrenze im Browser-Lister gibt es nicht. Wie viel eBay dir erlaubt, hängt von deinem eBay-Konto ab.

**Warum sind Produkte aus meiner Produkt-Datenbank verschwunden?**
Jedes Produkt, das der Lauf bearbeitet, verlässt die Produkt-Datenbank – erfolgreiche, weil sie jetzt auf eBay stehen, fehlgeschlagene, weil sie nicht gelistet werden konnten (die findest du im Statusbericht). Produkte, die der Lauf nur entnommen, aber noch nicht bearbeitet hat, gehen beim Stoppen oder am Laufende zurück. Läuft ein Browser-Lister auf einem anderen deiner Geräte, nimmt der natürlich auch Produkte.

**Was heißt „In Arbeit“?**
Ein Gerät (oder der CSV-Lister) hat das Produkt gerade zum Listen genommen. So lange bekommen andere Geräte es nicht. Siehe [Abschnitt 6](#6-die-produkt-datenbank-beim-listen-entnahme-in-arbeit-server-ausfall).

**Kann ich auf mehreren Rechnern gleichzeitig listen?**
Ja, mit demselben Konto und derselben Produkt-Datenbank. Jedes Gerät bekommt andere Produkte. Siehe [7.7](#77-auf-zwei-geräten-gleichzeitig-listen).

**Was passiert, wenn der Server ausfällt, während ich liste?**
Der Browser-Lister pausiert und macht von selbst weiter, sobald der Server wieder da ist. Siehe [6.5](#65-wenn-der-server-nicht-erreichbar-ist-pause).

**Warum hat der Lauf mehr Produkte verbraucht, als ich Angebote eingestellt habe?**
Fehlgeschlagene Produkte zählen nicht als Angebot; der Lauf holt Ersatz nach, bis die Zahl erreicht ist.

**Wo ist „Standard-List (0.2)“ bzw. „Ohne KI starten“?**
Gibt es seit Version 46.0 nicht mehr. Es gibt nur noch „Starten“; der Titel kommt bei Produkten aus der Produkt-Datenbank immer von der KI.

**Kann ich ohne KI listen?**
Nur Produkte aus dem Konkurrenz-Scanner: Die nehmen den Titel des Konkurrenten. Produkte aus der Produkt-Datenbank brauchen immer einen OpenAI-Schlüssel.

**Kostet das Listen etwas?**
Cash Lister zieht beim Listen nichts ab. Die KI-Kosten laufen über dein eigenes OpenAI-Konto; eBay-Gebühren zahlst du an eBay. Zum Abo von Cash Lister siehe `references/konto-und-installation.md`.

**Brauche ich einen OpenAI-Schlüssel?**
Für Produkte aus der Produkt-Datenbank ja. Für Konkurrenz-Scanner-Funde nicht zwingend – ohne Schlüssel bekommt aber jedes Angebot den Spielzeug-Warnhinweis.

**Kann ich den Spielzeug-Warnhinweis abschalten?**
Nein. Mit OpenAI-Schlüssel erscheint er nur, wenn die KI das Produkt als Spielzeug einstuft oder unsicher ist. Mit dem Platzhalter `_SPIELZEUG_WARNUNG_` in deiner Vorlage bestimmst du, wo er steht.

**Kann ich Promoted Listings abschalten?**
In der Extension nicht. Bietet eBay die Option an, schaltet die Extension sie ein und setzt die Rate aus „Anzeigengebühr (%)“.

**Welche Marke wird eingetragen?**
Immer „Unbranded“.

**Warum steht im Custom Label so eine seltsame Zeichenfolge?**
Das ist die Kennung von Cash Lister (endet auf „==“). Die Extension braucht sie, um dein Angebot dem Amazon-Produkt zuzuordnen. Nicht ändern. Siehe [Abschnitt 13](#13-custom-label--sku).

**Kann ich selbst eine Kategorie festlegen?**
Nein. Die Extension übernimmt eBays ersten Kategorie-Vorschlag.

**Kann ich die Stückzahl festlegen?**
Im Browser-Lister nicht; es gilt eBays Vorbelegung.

**Wo ist „Schedule Listing Time“ (geplante Uhrzeit bei eBay)?**
Gibt es seit Version 46.0 nicht mehr. Angebote gehen sofort online. Um das Listen über den Tag zu verteilen, gibt es die Zeitschaltung ([5.13](#513-karte-zeitschaltung)).

**Wo ist „Optimize for slow computers“?**
Gibt es seit Version 46.0 nicht mehr. Läuft dein Rechner zu langsam, stell bei „Gleichzeitig“ eine kleinere Zahl ein.

**Wo stelle ich den „Erlaubten Bildabstand“ beim Bildabgleich ein?**
Gar nicht mehr – er ist seit Version 46.0 fest eingestellt. Den Bildabgleich selbst schaltest du in den Einstellungen ein oder aus ([Abschnitt 20](#20-doppelte-angebote-vermeiden)).

**Geht es weiter, wenn ich Chrome schließe?**
Nein. Der Lauf endet und startet nicht von selbst neu. Nach dem nächsten Öffnen ist „Starten“ meist grau, weil die Seite sich „läuft“ gemerkt hat: im Browser-Lister „Stoppen & zurücksetzen“ drücken und neu starten. Produkte der Produkt-Datenbank, die beim Schließen „In Arbeit“ waren, werden nach einer Weile von selbst wieder frei ([6.3](#63-was-nach-dem-listen-mit-dem-produkt-passiert)). **Nicht sicher belegt:** was passiert, wenn der Rechner während eines Laufs in den Ruhezustand geht.

**Darf ich die Browser-Lister-Seite während eines Laufs neu laden (F5)?**
Ja. Der Lauf läuft weiter, solange der Tab selbst offen bleibt. Nur Schließen beendet den Nachschub. War der Lauf pausiert, ist nach dem Neuladen „Starten“ wieder aktiv – zum Weitermachen trotzdem „Fortsetzen“ nehmen (siehe [5.14](#514-welche-knöpfe-wann-bedienbar-sind)).

**Kann ich während des Laufs am Rechner arbeiten?**
Ja, aber lass den Browser-Lister-Tab und die Arbeits-Tabs in Ruhe. Bei „GPSR-Angaben übernehmen“ springt der Amazon-Tab kurz nach vorne – dann am besten ein eigenes Chrome-Fenster für den Browser-Lister nehmen.

**Kann ich mehrere Browser-Lister-Tabs gleichzeitig laufen lassen?**
Nicht im selben Chrome-Profil. Die Extension kennt dort nur einen Lauf zur Zeit: Zähler, Statusbericht und Einstellungen gibt es nur einmal. Ein Klick auf „Browser-Lister“ springt deshalb zum schon offenen Tab. Willst du schneller listen, erhöhe „Gleichzeitig“ – oder liste auf einem zweiten Gerät ([7.7](#77-auf-zwei-geräten-gleichzeitig-listen)).

**Werden meine Browser-Lister-Einstellungen gesichert?**
Quelle, „Wie viele Angebote“, „Gleichzeitig“, Zeitschaltung (Haken und Stunden) und „Fehler-Tabs schließen“ gehören zu den Einstellungen, die beim Exportieren als Datei mitkommen und (mit Anmeldung) auf dem Server gesichert werden (Einstellungen → Reiter „Sicherung“). Zähler und Statusbericht werden nicht gesichert. Der OpenAI-Schlüssel kommt nur in die Export-Datei, nicht auf den Server.

**Wird das Angebot sofort online gestellt?**
Ja, wenn „Listing automatisch absenden“ an ist und eBay keine Angebotsgebühr anzeigt (oder „Auch mit Angebotsgebühr einstellen“ an ist).

**Warum bekomme ich so oft „Amazon-Preis zu hoch (Filter „Preis bis“)“, obwohl ich keine Grenze eingestellt habe?**
Siehe [9.4](#94-preis-ab-und-preis-bis): Aus einer älteren Version steht oft noch 100 bei „Preis bis“, und der Schalter ist an.

**Was passiert bei einem Produkt, das ein anderer Kunde schon hat?**
Produkte aus der Produkt-Datenbank kommen gar nicht erst in deine Liste. Funde aus dem Konkurrenz-Scanner werden gar nicht erst geöffnet: „Produkt bereits von einem anderen Nutzer vergeben“.

**Kann ich fehlgeschlagene Produkte automatisch wiederholen lassen?**
Nein, siehe [7.5](#75-fehlgeschlagene-produkte-noch-einmal-versuchen).

**Wie sehe ich mein eBay-Verkaufslimit?**
Im Browser-Lister gar nicht – nur bei eBay selbst.

**Kann ich direkt auf der Amazon-Produktseite ein einzelnes Produkt listen?**
Nein. Gelistet wird über den Browser-Lister. Für ein einzelnes Produkt: Link oder ASIN auf der Seite „Produkt-Datenbank“ in der Karte „Links hinzufügen“ einfügen, „Zur Datenbank hinzufügen“ klicken, dann im Browser-Lister mit „Wie viele Angebote“ 1 starten. Achte darauf, dass das Produkt dann oben in der Reihenfolge steht („Sortierung“ „Neuste zuerst“), sonst nimmt der Lauf ein anderes. Läuft auf einem anderen Gerät oder im CSV-Lister gerade etwas aus derselben Produkt-Datenbank, kann es dort schon „In Arbeit“ sein – dann bekommt dein Lauf ein anderes Produkt.

**Gelten „Mind. Sterne“, „Mind. Bewertungen“ und „Mind. Lagerbestand“ auch beim Listen?**
Nein, nur beim Einsammeln mit dem Produkt-Grabber. Siehe [9.6](#96-was-beim-listen-nicht-geprüft-wird).

**Muss ich in den Einstellungen auf „Speichern“ klicken?**
Nein. Jede Änderung wird gespeichert, sobald du das Feld verlässt (Schalter sofort, die Blacklist beim Tippen). „Speichern“ zeigt nur die Meldung „Einstellungen gespeichert“.

**Welche Version habe ich?**
Unten in der Seitenleiste steht „Version …“.

## 26. Probleme und Lösungen

**„Starten“ ist grau, obwohl kein Lauf läuft.**
Die Seite glaubt, es läuft noch ein Lauf (z. B. nach einem Browser-Absturz oder nach „Fortsetzen“ ohne Lauf). Lösung: „Stoppen & zurücksetzen“ klicken. Ist der Lauf gerade normal zu Ende gegangen, reicht Neuladen (F5).

**Klick auf „Starten“ – Meldung „Nicht angemeldet oder Zugang deaktiviert - bitte im Dashboard anmelden.“**
Du bist nicht angemeldet, dein Zugang ist abgeschaltet oder dein Abo ist gesperrt. Schau in die Seitenleiste unten („Nicht angemeldet“, „Zugang abgeschaltet“ oder „Abo gesperrt“) und melde dich im Dashboard an bzw. kläre das Abo. Klappt die Anmeldung nicht, an den Betreiber wenden. Hinweis: Eine zu alte Version kann sich nicht anmelden – dann erst mit update.bat aktualisieren und Chrome komplett neu starten (siehe `references/konto-und-installation.md`).

**Meldung „Nicht angemeldet oder Sitzung abgelaufen - bitte im Dashboard anmelden, dann starten.“**
Deine Anmeldung gilt nicht mehr. Im Dashboard neu anmelden, dann erneut „Starten“.

**Meldung „Server nicht erreichbar - die Produkt-Datenbank liegt auf dem Server. Bitte später erneut starten.“**
Der Server antwortet gerade nicht. Später erneut versuchen. Bleibt es dabei, an den Betreiber wenden.

**Meldung „Alle … Produkte der Datenbank sind gerade in Arbeit - …“**
Alle übrigen Produkte sind gerade bei einem anderen deiner Geräte oder im CSV-Lister. Warten, bis die dort fertig sind, oder neue Produkte sammeln. Auf der Seite „Produkt-Datenbank“ siehst du in der Spalte „In Arbeit“, welches Gerät sie hat.

**Meldung „Die Produkt-Datenbank ist leer - erst Produkte einsammeln.“ bzw. „Der Konkurrenz-Scanner hat noch keine Funde.“**
Die gewählte Quelle ist leer. Erst Produkte importieren bzw. scannen, oder bei „Produkte aus“ die andere Quelle wählen. Hast du gerade erst auf Version 46.0 aktualisiert und deine alte Liste fehlt: Sie wird nach der Anmeldung von selbst hochgeladen ([6.7](#67-erster-start-nach-dem-update-deine-alte-liste-wird-hochgeladen)); kurz warten und die Seite neu laden.

Siehst du auf der Seite „Produkt-Datenbank“ aber Produkte und neben „Produkte aus“ steht „? verfügbar“: Dann hat die Extension intern keine Antwort bekommen, und „Starten“ meldet nach aktuellem Stand trotzdem „leer“. Seite neu laden (F5) und erneut starten; hilft das nicht, Chrome komplett neu starten.

**Neben „Produkte aus“ steht „⚠ Server nicht erreichbar – Lister pausiert, macht von selbst weiter.“**
Der Lauf wartet auf den Server. Du musst nichts tun, er macht von selbst weiter. Dauert es lange, an den Betreiber wenden. Siehe [6.5](#65-wenn-der-server-nicht-erreichbar-ist-pause).

**Der Lauf endete mit „Browser-Lister beendet: …“.**
Siehe die Tabelle in [6.6](#66-abgemeldet-zugang-abgeschaltet-oder-abo-gesperrt-während-des-laufs): neu anmelden bzw. Abo klären, dann neu starten.

**Es passiert nach dem Start gar nichts, keine Tabs gehen auf.**
1. Prüfe, ob „erfolgreich gelistet“/„fehlgeschlagen“ steigen, und schau in den Statusbericht (Seite neu laden).
2. Steht neben „Produkte aus“ eine Server-Meldung? Dann wartet der Lauf auf den Server ([6.5](#65-wenn-der-server-nicht-erreichbar-ist-pause)).
3. Wurden die ersten Funde des Konkurrenz-Scanners sofort als „Produkt bereits von einem anderen Nutzer vergeben“ verbucht, öffnet die Extension für diese keine Tabs.
4. Läuft die Zeitschaltung gerade in einer Pause (Statuszeile „😴 Schläft – …“)? Dann wartet der Lauf.
5. Sonst: Seite neu laden, „Stoppen & zurücksetzen“, erneut starten.

**Jedes Produkt scheitert mit „Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“.**
Häufige Ursachen:
1. Du bist im Chrome-Profil nicht bei eBay angemeldet → bei eBay anmelden (auf dem Marktplatz aus „Domain“). Eine eigene Meldung dafür gibt es nicht.
2. „Listing automatisch absenden“ ist aus und niemand klickt → in den Einstellungen einschalten.
3. eBay zeigt eine Sicherheitsabfrage → im eBay-Tab lösen, kleinere Zahl bei „Gleichzeitig“.
4. „Domain“ steht auf „Keine“ oder auf dem falschen Land → richtig einstellen. **Nicht sicher belegt:** welche Meldung bei „Keine“ genau im Statusbericht steht.
5. eBay zeigt im Arbeits-Tab eine allgemeine Fehlerseite (nicht die Fehlerseite des Formulars) – auch dann kommt keine eigene Meldung, sondern erst die Zeitüberschreitung. Im Tab nachsehen und später erneut versuchen.
6. Um zu sehen, wo es hängt: „Fehler-Tabs schließen“ ausschalten, 1 Produkt mit „Gleichzeitig“ 1 listen und auf den Titel des eBay-Tabs achten ([Abschnitt 24](#24-tab-titel-und-tab-symbole-während-des-listens)). Den letzten Tab-Titel dem Betreiber mitteilen.

**Jedes Produkt scheitert mit „KI-Titel ist leer“.**
Die KI liefert keinen Titel. Prüfe in den Einstellungen (Reiter „KI“) „OpenAI-API-Schlüssel (für die Titel-Generierung)“, dein Guthaben und dein Konto bei OpenAI. Typisch nach einem Rechnerwechsel oder nach „Einstellungen vom Server holen“: Der Schlüssel wird nicht auf dem Server gesichert und fehlt dann – neu eintragen. Ohne funktionierende KI kannst du nur Funde aus dem Konkurrenz-Scanner listen.

**Viele Produkte scheitern mit „Listen fehlgeschlagen – keine verwertbare Antwort der Amazon-Seite“.**
Der Amazon-Teil liefert kein Ergebnis. Öffne einen der Links aus dem Statusbericht selbst: Zeigt Amazon eine Sicherheitsabfrage, eine Fehlerseite oder lädt die Seite sehr langsam? Kleinere Zahl bei „Gleichzeitig“ verwenden. Bleibt es dabei, an den Betreiber wenden.

**Viele Produkte scheitern mit „Nicht von Amazon versendet (Versand: …)“.**
Das ist der Filter „Nur FBA“ (Standard an). Entweder Produkte mit Versand durch Amazon importieren, oder den Filter in den Einstellungen (Reiter „Produkt-Filter“) ausschalten.

**Viele Produkte scheitern mit „Versender auf der Produktseite nicht erkennbar“.**
Die Extension findet in der Buybox keine Versandangabe. Öffne einen Link selbst und schau, ob die Buybox normal aussieht (z. B. ob ein Kaufkasten da ist). Tritt es bei fast allen Produkten auf, kann sich Amazons Seitenaufbau geändert haben – an den Betreiber wenden.

**Viele Produkte scheitern mit „Produkt hat keinen kostenlosen Versand“.**
Die Extension findet in der Buybox keinen Hinweis auf kostenlose Lieferung. Diese Prüfung lässt sich nicht abschalten. **Nicht sicher belegt:** ob die Anzeige auf Amazon von deiner Lieferadresse oder Anmeldung bei Amazon abhängt.

**Viele Produkte scheitern mit „Produkt ist nicht auf Lager“, obwohl sie lieferbar aussehen.**
Prüfe die Lieferzeit: Liegt das Lieferdatum mehr Tage in der Zukunft als „Max. verlängerte Lieferzeit“ (Standard 20), gilt das Produkt als nicht vorrätig. Zahl in den Einstellungen erhöhen. Siehe [9.5](#95-lagerbestand-und-lieferzeit-produkt-ist-nicht-auf-lager).

**Viele Produkte scheitern mit „Amazon-Preis zu hoch (Filter „Preis bis“)“.**
Siehe [9.4](#94-preis-ab-und-preis-bis): Einstellungen öffnen, Reiter „Produkt-Filter“, Karte „Amazon-Filter“, Schalter bei „Preis bis“ prüfen, Wert anpassen oder Schalter aus.

**Mode-Artikel scheitern mit „Zustand nicht wählbar: Kachel „Neu mit Etikett“ nicht gefunden“.**
Bei Kategorien mit Zustandskacheln sucht die Extension die Kachel „Neu mit Etikett“ (ist „NUR „Neu: Sonstige“ listen“ an und soll das Produkt als „Neu: Sonstige“ gelistet werden, eine Kachel mit „Sonstige“). Gibt es sie nicht, oder ist die eBay-Seite nicht auf Deutsch, scheitert das Produkt (im NUR-Fall mit „„Neu: Sonstige" in dieser Kategorie nicht verfügbar (nur-Neu-Sonstige aktiv)“). Siehe [Abschnitt 16](#16-zustand-neu-oder-neu-sonstige).

**Viele Produkte scheitern mit „Produkt ist schon gelistet (Duplikat)“, obwohl sie nicht (mehr) auf eBay sind.**
Die Doppelt-Liste der Extension merkt sich erfolgreich eingestellte Produkte dauerhaft in deinem Chrome-Profil, auch wenn du das Angebot bei eBay beendet hast. In der Oberfläche lässt sich die Liste nicht leeren. **Nicht sicher belegt:** wie man einzelne Einträge entfernt – an den Betreiber wenden.

**„Nicht eingestellt: eBay verlangt Angebotsgebühren …“ bei jedem Produkt.**
eBay zeigt eine Angebotsgebühr (z. B. weil deine kostenlosen Angebote aufgebraucht sind). Entweder bei eBay klären oder in den Einstellungen (Reiter „eBay & Rahmenbedingungen“, Karte „Beim Einstellen“) „Auch mit Angebotsgebühr einstellen“ einschalten – dann zahlst du die Gebühren.

**Angebote haben weniger Bilder als bei Amazon.**
Bilder, die bei eBay nach zwei Wiederholungen noch fehlerhaft sind, fallen weg; das Angebot geht trotzdem online. Kleinere Zahl bei „Gleichzeitig“ verwenden. Prüfe auch „Nur ein Bild bei eBay einstellen“ in den Einstellungen.

**Es entsteht kein Sammelbild, obwohl der Knopf „Starten“ das verspricht.**
Für das Sammelbild braucht die Extension ein Wasserzeichen-Bild, für das es in der Oberfläche kein Feld gibt. Siehe [Abschnitt 14](#14-bilder). Bei Fragen an den Betreiber wenden.

**Jedes Angebot hat den Spielzeug-Warnhinweis.**
Wahrscheinlich ist kein (gültiger) OpenAI-Schlüssel eingetragen oder dein OpenAI-Guthaben ist leer. Dann fügt die Extension den Hinweis sicherheitshalber immer ein.

**Die Beschreibung sieht anders aus als erwartet / ist ganz schlicht.**
Ist das Feld im Reiter „Beschreibungsvorlage“ leer, baut die Extension eine schlichte Beschreibung. Eigene Vorlage dort einfügen.

**In meiner Beschreibung fehlen Wörter.**
Der eingebaute Wortfilter entfernt Begriffe wie „Original“, „Premium“, „Garantie“, „CE“ ([10.4](#104-eingebauter-wortfilter)). Das lässt sich nicht abschalten.

**Der Preis auf eBay stimmt nicht mit meiner Rechnung überein.**
Prüfe in den Einstellungen (Reiter „Preise & Listing“): Gilt eine variable Preisregel für diesen Amazon-Preis? Ist die Preisendung eingeschaltet und welche Endung steht dort (bei Endungen unter 0.99 kann der Preis durch die Rundung leicht sinken, siehe [15.2](#152-beispiele))? Hat sich der Amazon-Preis seit dem Listen geändert? Hattest du früher eine zweite Preistafel für „Neu: Sonstige“: Die gibt es seit Version 46.0 nicht mehr, es gilt die eine Tafel für alle Zustände.

**Angebote werden als „Neu“ statt „Neu: Sonstige“ eingestellt.**
Die Kategorie bietet „Neu: Sonstige“ nicht an (dann nimmt die Extension „Neu“), oder die passende Preisregel hat den Haken „Neu: Sonstige“ nicht (eine passende Regel hat Vorrang vor dem allgemeinen Schalter). Willst du in solchen Fällen gar nicht listen: „NUR „Neu: Sonstige“ listen“ einschalten.

**In Mode-Kategorien wurde „Neu mit Etikett“ gewählt.**
So arbeitet die Kachel-Auswahl ohne NUR-Schalter – und auch mit NUR-Schalter, wenn das Produkt gar nicht als „Neu: Sonstige“ gelistet werden soll (allgemeiner Schalter „Als „Neu: Sonstige“ listen (Standard)“ aus bzw. die passende Preisregel ohne Haken „Neu: Sonstige“). Soll es „Neu: Sonstige“ werden und „NUR „Neu: Sonstige“ listen“ ist an, sucht die Extension eine „Sonstige“-Kachel oder überspringt das Produkt.

**Der Statusbericht zeigt keine neuen Einträge.**
Die Seite aktualisiert sich nicht von selbst – neu laden (F5). Das gilt auch, wenn der Klick auf „Statusbericht“ nur in den schon offenen Tab gesprungen ist.

**Der Statusbericht ist plötzlich leer.**
Er wird bei jedem Start und bei „Stoppen & zurücksetzen“ geleert, oder jemand hat „Leeren“ gedrückt. Läufe auf einem anderen Gerät stehen nur in dessen Statusbericht.

**„Ändern“ bei den Produkt-Filtern öffnet die Einstellungen, aber ich sehe die Filter nicht.**
Die Einstellungsseite öffnet mit dem Reiter „Preise & Listing“. Klick auf den Reiter „Produkt-Filter“.

**Die Zeitschaltung zeigt beim Start schon „… von 100“, obwohl noch nichts gelistet wurde.**
Der Rundenzähler läuft über Läufe hinweg weiter. Zum Zurücksetzen den Haken „Zeitschaltung an“ aus- und wieder einschalten oder „Stoppen & zurücksetzen“ drücken.

**Der Lauf wartet nach dem Neustart, obwohl ich gerade erst gestartet habe.**
Die vorige Runde der Zeitschaltung war voll, die Restpause läuft noch. „Stoppen & zurücksetzen“ beendet die Pause.

**Nach „Stoppen & zurücksetzen“ wurde trotzdem noch ein Angebot eingestellt.**
Produkte, die schon im eBay-Formular waren, laufen zu Ende. Den eBay-Tab selbst schließen, wenn das nicht passieren soll.

**Ein Produkt steht in der Produkt-Datenbank dauerhaft „In Arbeit“, obwohl kein Browser-Lister läuft.**
Das kann nach einem Chrome-Absturz oder bei einer noch nicht nachgeholten Meldung passieren ([6.3](#63-was-nach-dem-listen-mit-dem-produkt-passiert)). Chrome auf dem genannten Gerät öffnen und dort angemeldet lassen; sonst wird das Produkt nach einer Weile von selbst frei. Wie lange, zeigt die Produkt-Datenbank in der Spalte „In Arbeit“ an der Uhrzeit hinter „bis“. Cash Lister verlangt dabei beim Browser-Lister etwa 30 Minuten (laufend verlängert, solange er arbeitet), beim CSV-Lister etwa 1 Stunde bzw. bis zu 7 Tage für Produkte, die schon in einer hochgeladenen Datei stehen (`references/produkte-finden-und-datenbank.md`, Abschnitt 10.9). **Nicht sicher belegt:** ob der Server diese Zeiten in jedem Fall genau so übernimmt – bei Fragen an den Betreiber wenden. Wie du ein Produkt „In Arbeit“ trotzdem löschst, steht in `references/produkte-finden-und-datenbank.md`.

**Nach einem Update verhält sich der Browser-Lister seltsam (alte Knöpfe, englische Meldungen, Anmeldung klappt nicht).**
Nach jedem Update Chrome **komplett** schließen und neu starten (alle Fenster). Hilft das nicht: `chrome://extensions` öffnen und bei Cash Lister auf „Neu laden“ klicken – damit wird auch der Hintergrunddienst der Extension aktualisiert. Danach im Dashboard prüfen, ob du angemeldet bist. Mehr dazu in `references/konto-und-installation.md`.

**Die violette Lupe erscheint auf meinem eBay-Angebot nicht.**
Sie erscheint nur auf deinen eigenen Angeboten, wenn eBay dir das Custom Label auf der Seite anzeigt, und nur, wenn das Custom Label von der Extension stammt. eBay lädt Teile der Seite nach; die Extension wartet bis zu 10 Sekunden.

## 27. Neu in Version 46.0

Was Kunden, die bisher Version 45.5 (oder älter) hatten, beim Listen jetzt anders finden:

1. **Kein kleines Fenster mehr beim Klick aufs Symbol.** Es öffnet sich das Dashboard. Angemeldet wird im Dashboard. Die früheren Popup-Einstellungen (Preise, Domain, „Auto Submit Listing“, Anzeigenrate, Artikelmerkmale per KI) stehen jetzt in den Einstellungen im Reiter „Preise & Listing“.
2. **Neuer Name und neues Aussehen:** Cash Lister hat ein neues Logo und ein neues Design mit Seitenleiste. Der Bulk-Lister heißt jetzt **„Browser-Lister“**. Module öffnen im eigenen Tab; ist ein Modul schon offen, springt der Klick dorthin.
3. **Nur noch „Starten“:** „Opti-List“ heißt jetzt „Starten“. „Standard-List (0.2)“ (Listen ohne KI-Titel) gibt es nicht mehr – der Titel kommt bei Produkten aus der Produkt-Datenbank immer von der KI. Ohne OpenAI-Schlüssel klappt das Listen aus der Produkt-Datenbank also nicht.
4. **Umbenannt auf der Browser-Lister-Seite:**

   | Bis 45.5 | Seit 46.0 |
   |---|---|
   | „Bulk Poster“ / „Bulk Lister“ | „Browser-Lister“ |
   | „Produkte aus:“ mit „verwalten“ | „Produkte aus“ mit „Verwalten“ |
   | „Opti-List“ | „Starten“ |
   | „Pause“ / „Resume“ | „Pausieren“ / „Fortsetzen“ |
   | „Reset & Terminate“ | „Stoppen & zurücksetzen“ |
   | „Status Report“ (Seite „Bulk List Status“, Knopf „Clear“) | „Statusbericht“ (Knopf „Leeren“) |
   | „Thread Count:“ | „Gleichzeitig“ |
   | „Listing-Timer“ | „Zeitschaltung“ |
   | „Close Errored Listings:“ | „Fehler-Tabs schließen“ |
   | „Successful Listings“ / „Failed Listings“ | „erfolgreich gelistet“ / „fehlgeschlagen“ |

5. **Entfernt:** „Optimize for slow computers“ (Modus für langsame Rechner), „Schedule Listing Time“ (geplante Uhrzeit bei eBay), das Feld „Erlaubter Bildabstand“ beim Bildabgleich (jetzt fest), die zweite Preistafel „Eigene Preise für „Neu: Sonstige““ und die langen Erklärungstexte in den Einstellungen.
6. **Einstellungen neu sortiert** in die Reiter „Preise & Listing“, „Produkt-Filter“, „eBay & Rahmenbedingungen“, „Beschreibungsvorlage“, „KI“ und „Sicherung“, alle Beschriftungen deutsch. Beispiele: „Allow automatic listing when eBay shows insertion fees above 0“ → „Auch mit Angebotsgebühr einstellen“; „Only List One Picture on Ebay“ → „Nur ein Bild bei eBay einstellen“; „Max Extended Delivery Days“ → „Max. verlängerte Lieferzeit“; „Minimum/Maximum Price (€)“ → „Preis ab“ / „Preis bis“; „End Price“ → „Preisendung“; „Promoted Listing Ad Rate“ → „Anzeigengebühr (%)“; „Auto Submit Listing“ → „Listing automatisch absenden“; „GPSR-Angaben holen“ → „GPSR-Angaben übernehmen“. Alles dazu in `references/einstellungen.md`.
7. **Produkt-Datenbank auf dem Server:** Sie gehört jetzt zu deinem Konto. Mehrere Geräte sehen dieselbe Liste, Produkte im Listen sind „In Arbeit“, die Bestandsanzeige zeigt „… verfügbar · … in Arbeit“. Ohne Server pausiert der Browser-Lister und macht von selbst weiter. Beim ersten Start wird deine alte, lokale Liste automatisch hochgeladen. Siehe [Abschnitt 6](#6-die-produkt-datenbank-beim-listen-entnahme-in-arbeit-server-ausfall).
8. **Neue Startprüfung:** „Starten“ meldet jetzt auch „Server nicht erreichbar - …“, „Nicht angemeldet oder Sitzung abgelaufen - …“ und „Alle … Produkte der Datenbank sind gerade in Arbeit - …“.
9. **Meldungen und Tab-Titel deutsch:** z. B. „Erfolgreich gelistet!“ statt „Item Listed Successfully!“ und „Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“ statt „timeout: no response after 15 minutes“. Die vollständige Gegenüberstellung steht in [23.4](#234-alte-meldungen-bis-version-455-und-ihre-neuen-namen).
10. **Dashboard:** zeigt den Stand des Browser-Listers (z. B. „läuft · 12 von 100“, „wartet auf den Server“, „Tab geschlossen“) und „Heute gelistet“ (mit Geräten im Server-Modus auch über mehrere Geräte).
11. **Abo:** Cash Lister läuft jetzt als Monatsabo (ab wann für dich, steht auf deiner Zahlungsseite). Ist das Abo gesperrt, startet „Starten“ keinen Lauf; was mit einem schon laufenden Lauf passiert, steht in [6.6](#66-abgemeldet-zugang-abgeschaltet-oder-abo-gesperrt-während-des-laufs). Details zum Abo: `references/konto-und-installation.md`.
12. **CSV-Lister für alle:** Den CSV-Lister (ein zweiter Lister, der über eine CSV-Datei bei eBay hochlädt) sehen jetzt alle Kunden in der Seitenleiste, nicht mehr nur freigeschaltete Tester. Er nimmt seine Produkte aus derselben Produkt-Datenbank; was er gerade bearbeitet, steht dort ebenfalls als „In Arbeit“. Beschrieben ist er in `references/produktuebersicht-und-csv-lister.md`.

**Schon mit Version 45.5 kam** (falls du direkt von 45.4 oder älter aktualisierst): Der Listing-Bereich oben auf der Amazon-Produktseite (Bildleiste, Titel-Tabelle, „Snipe Title“, „Opti-List“, „Basic-List“, „Sell it for“, „Promoted Listing %“) und „List ASIN“ auf der Amazon-Suche sind entfernt – gelistet wird nur über den Browser-Lister. Ohne eigene Beschreibungsvorlage gibt es eine schlichte Beschreibung statt einer mitgelieferten Vorlage. Der frühere eigene Titel-Generator, der Haken, ob du bei eBay ein Abo hast, und das automatische Captcha-Lösen sind entfernt. Die Blacklist prüft auch die Werte der Produktinformationen. Auf deinen eigenen eBay-Angeboten steht statt „Look up this SKU“ eine violette Lupe.

Unverändert geblieben sind die Prüfungen auf der Amazon-Seite (nur die Meldungen sind deutsch), die Abläufe im eBay-Formular, die Preisberechnung, die Zeitschaltung und die Produktvergabe.

## 28. Was dieser Bereich nicht sicher beantworten kann

Bei diesen Fragen offen sagen, dass es nicht sicher belegt ist, und an den Betreiber verweisen:

- Welche Domain nach einer frischen Installation voreingestellt ist: normalerweise „DE“, ganz sicher ist es nicht – deshalb immer in den Einstellungen bei „Domain“ prüfen. Welche Meldung erscheint, wenn dort „Keine“ steht.
- Ob der Server die Haltezeit „In Arbeit“, die Cash Lister verlangt (Browser-Lister etwa 30 Minuten), in jedem Fall genau so übernimmt. Maßgeblich ist die Uhrzeit hinter „bis“ in der Produkt-Datenbank.
- Ob eBay mehrere gleichzeitige Läufe auf einem eBay-Konto anders behandelt.
- Wie oft die Spalte „eBay-Link“ leer bleibt (das passiert, wenn eBays Erfolgsseite den Erfolg zuerst meldet – ein leeres Feld ist kein Fehler).
- Ob einzelne erfolgreiche Angebote in der eigenen Doppelt-Liste („Produkt ist schon gelistet (Duplikat)“) fehlen, und wie man einzelne Einträge daraus entfernt (in der Oberfläche gar nicht).
- Was eBay bei Stückzahl, Versand, Zahlung und Rücknahme vorbelegt; ob alte, nicht mehr sichtbare Einstellungen zu Artikelstandort und Rücknahme bei dir noch wirken.
- Wie viele Bilder eBay im Einzelfall annimmt; ob bei dir ein Sammelbild entsteht (Wasserzeichen hinterlegt?).
- Ob „Optionale Artikelmerkmale mit KI ausfüllen“ auf den Domains DE, FR, IT, ES und NL überhaupt etwas Sichtbares bewirkt.
- Welche Kategorie eBay vorschlägt und ob eBay ein Katalogprodukt zuordnet.
- Mit welchem Text eBay ein erreichtes Verkaufslimit meldet.
- Ob es nach dem Lösen einer Sicherheitsabfrage bei Amazon oder eBay in jedem Fall weitergeht.
- Welche Meldung eBay zeigt, wenn ein Formular ohne Preis abgeschickt wird (Amazon zeigte keinen Preis).
- Bei welchen eBay-Konten eBay das Mehrwertsteuer-Feld zeigt.
- Ob die Anzeige „kostenloser Versand“ auf Amazon von deiner Lieferadresse oder Amazon-Anmeldung abhängt.
- Ob die Lieferzeit-Grenze beim Listen absichtlich auch bei ausgeschaltetem Schalter gilt.
- Wie sich ein pausierter und dann nur mit „Stoppen & zurücksetzen“ beendeter Lauf beim nächsten Start im Einzelfall auswirkt.
- Was passiert, wenn der Rechner während eines Laufs in den Ruhezustand geht.
- Eine empfohlene Zahl bei „Gleichzeitig“ und wie lange ein Produkt im Durchschnitt dauert.
- Die Prüfung des Angebotsformats (Auktion/Sofort-Kaufen): Zu dieser Prüfung gibt es keine Beschreibung – bei Fragen an den Betreiber wenden.
