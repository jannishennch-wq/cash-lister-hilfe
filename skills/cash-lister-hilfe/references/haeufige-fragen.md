# Häufige Fragen – schnelle Antworten

Die wahrscheinlichsten Kundenfragen mit einer kurzen Antwort und dem Verweis auf die Stelle, an der alles ausführlich steht. Stand: Version 46.3.

**So benutzt du diese Datei:** Die Antworten hier sind bewusst knapp. Passt die Frage des Kunden nicht genau, oder will er mehr wissen, lies die genannte Stelle und antworte von dort. Steht bei einer Antwort **Nicht sicher belegt**, gib den Punkt nicht als Tatsache weiter, sondern sag offen, dass es nicht sicher bekannt ist, und verweise an den Betreiber. Benutzt der Kunde alte Namen aus Version 45.x (Popup, Bulk-Lister, CSV Tracker, Opti-List, End Price …), hilft Abschnitt 1 und das Glossar.

Abkürzungen der Dateien (alle im Ordner `references/`):

| Kürzel | Datei |
|---|---|
| **Dash** | `dashboard.md` |
| **Konto** | `konto-und-installation.md` |
| **Einst** | `einstellungen.md` |
| **Listen** | `listen-auf-ebay.md` |
| **Produkte** | `produkte-finden-und-datenbank.md` |
| **Tracker** | `tracker.md` |
| **Übersicht/CSV** | `produktuebersicht-und-csv-lister.md` |
| **Meldungen** | `meldungen-und-fehler.md` |
| **Glossar** | `glossar.md` |

Zahlen hinter dem Kürzel sind Abschnittsnummern (z. B. „Konto 5.8“).

## Inhalt

1. [Umstellung auf Version 46.0](#1-umstellung-auf-version-460) (Fragen 1–14)
2. [Einrichtung und Anmeldung](#2-einrichtung-und-anmeldung) (Fragen 15–25)
3. [Abo und Zahlung](#3-abo-und-zahlung) (Fragen 26–40)
4. [Konto, Kosten, Zugang](#4-konto-kosten-zugang) (Fragen 41–46)
5. [Updates, Versionen, Chrome](#5-updates-versionen-chrome) (Fragen 47–54)
6. [Einstellungen sichern und umziehen](#6-einstellungen-sichern-und-umziehen) (Fragen 55–59)
7. [Produkte finden und Produkt-Datenbank](#7-produkte-finden-und-produkt-datenbank) (Fragen 60–69)
8. [Listen mit dem Browser-Lister](#8-listen-mit-dem-browser-lister) (Fragen 70–87)
9. [Preise](#9-preise) (Fragen 88–92)
10. [Tracker](#10-tracker) (Fragen 93–102)
11. [Weitere Module](#11-weitere-module) (Fragen 103–107)
12. [Wenn nichts mehr hilft](#12-wenn-nichts-mehr-hilft) (Frage 108)

---

## 1. Umstellung auf Version 46.0

**1. Beim Klick auf das Symbol geht kein kleines Fenster mehr auf, sondern eine ganze Seite. Ist das richtig?**
Ja. Seit Version 46.0 gibt es das kleine Fenster (Popup) nicht mehr. Der Klick auf das Cash-Lister-Symbol öffnet das **Dashboard** in einem eigenen Tab; ist es schon offen (auch in einem anderen Chrome-Fenster), springt der Klick dorthin. Das Dashboard bleibt offen wie eine normale Webseite.
→ Dash 1, 2; Konto 4

**2. Nach dem Update öffnet sich immer noch das kleine Fenster.**
Dann hat Chrome noch die alte Fassung geladen, meist weil Chrome nach dem Update nicht komplett geschlossen war. Chrome komplett schließen (auch unten rechts im Infobereich) und neu starten, sonst in `chrome://extensions` bei Cash Lister auf den Kreispfeil („Neu laden“) – in jedem Chrome-Profil. Danach muss sich das Dashboard öffnen und unten in der Seitenleiste „Version 46.0“ oder eine höhere Nummer stehen (z. B. „Version 46.3“). Steht dort noch eine alte Nummer, war das Update nicht erfolgreich: `update.bat` noch einmal ausführen und die Meldungen lesen.
→ Konto 17, 18 („Statt des Dashboards öffnet sich ein kleines Fenster“); Dash 19

**3. Wo melde ich mich jetzt an und ab?**
Im Dashboard. Solange du nicht angemeldet bist, steht oben die Anmeldekarte mit „Benutzername“, „Passwort“ und „Anmelden“, rechts „Einrichtungsdatei einlesen“ (früher „Einstellungen importieren“ im Anmeldefenster). Abmelden: oben rechts auf das Kontofeld (dein Name) → „Abmelden“.
→ Konto 5, Dash 8, 9

**4. Wo stelle ich jetzt Preise, „End Price“, „Domain“ und die anderen Felder aus dem kleinen Fenster ein?**
In den Einstellungen: Seitenleiste → „Einstellungen“ → Reiter „Preise & Listing“. Dort heißen sie „% Aufschlag“, „Fester Aufschlag (€)“, „Preisendung“ (früher „End Price“), „Domain“ („None“ heißt jetzt „Keine“), „Listing automatisch absenden“ (früher „Auto Submit Listing“), „Anzeigengebühr (%)“ (früher „Promoted Listing Ad Rate“) und die beiden Schalter der Karte „Artikelmerkmale (KI)“. „Min Price (AutoList)“/„Max Price (AutoList)“ heißen jetzt „Preis ab“/„Preis bis“ im Reiter „Produkt-Filter“. „Schedule Listing Time“ gibt es nicht mehr.
→ Konto 20, Einst 26

**5. Wo sind „Einstellungen exportieren“, „Einstellungen importieren“ und die Server-Sicherung hin?**
Einstellungen → Reiter „Sicherung“: Karte „Als Datei“ (Export und Import) und Karte „Auf dem Server“ („Einstellungen vom Server holen“, bei einem Konflikt „Dieses Gerät auf den Server sichern“).
→ Konto 9, 10; Einst 16

**6. Wo finde ich die Versionsnummer?**
Ganz unten in der Seitenleiste, z. B. „Version 46.0“ (früher oben im kleinen Fenster). Ist das Chrome-Fenster schmal, steht die Seitenleiste oben und die Nummer ist ausgeblendet – das Fenster breiter ziehen oder maximieren.
→ Konto 4, Dash 4.4

**7. Wo ist der Bulk-Lister, wo der CSV Tracker?**
Umbenannt: Der Bulk-Lister heißt jetzt „Browser-Lister“, der CSV Tracker heißt „Tracker“. Beide findest du in der Seitenleiste in der Gruppe „Arbeiten“ oder als Karte im Dashboard unter „Vorgänge“. Jedes Modul öffnet in seinem eigenen Tab; ist es schon offen, springt der Klick dorthin.
→ Listen 4, Tracker 3, Dash 5

**8. Wo sind „Opti-List“ und „Standard-List (0.2)“? Kann ich ohne KI listen?**
Es gibt nur noch „Starten“ (früher „Opti-List“). Bei Produkten aus der Produkt-Datenbank schreibt immer die KI den Titel; den Start ohne KI-Titel („Standard-List (0.2)“) gibt es nicht mehr. Ohne gültigen OpenAI-Schlüssel scheitern solche Produkte mit „KI-Titel ist leer“. Nur Funde aus dem Konkurrenz-Scanner nehmen den Titel des Konkurrenten.
→ Listen 5.6, 27

**9. Wo sind „Schedule Listing Time“, „Optimize for slow computers“ und „Erlaubter Bildabstand“?**
Alle drei gibt es seit Version 46.0 nicht mehr. Angebote gehen sofort online; zum Verteilen über den Tag gibt es die „Zeitschaltung“ im Browser-Lister. Bei einem langsamen Rechner bei „Gleichzeitig“ eine kleinere Zahl nehmen. Der Bildabstand beim Bildabgleich ist fest eingestellt.
→ Listen 25, 27; Einst 26

**10. Meine Produkt-Datenbank ist nach dem Update leer oder zeigt „… werden noch auf den Server übertragen“.**
Seit Version 46.0 liegt die Produkt-Datenbank je Konto auf dem Server. Beim ersten Start lädt die Extension deine alte Liste von selbst hoch, sobald du angemeldet bist; bei einer großen Liste dauert das etwas. Angemeldet bleiben und warten. Ohne Anmeldung ist keine Liste zu sehen („nach der Anmeldung sichtbar“). Produkte, die laut deinen Google Sheets schon gelistet sind oder einem anderen Kunden gehören, werden dabei aussortiert.
→ Konto 8, Produkte 10.6, Dash 10.2

**11. Ich sehe plötzlich den CSV-Lister. Brauche ich dafür eine Freischaltung?**
Nein. Seit Version 46.0 steht der CSV-Lister allen Kunden zur Verfügung (Seitenleiste → „Arbeiten“ → „CSV-Lister“ oder Karte „CSV-Lister“ im Dashboard). Den Browser-Lister kannst du weiter benutzen, auch beide gleichzeitig.
Vor dem ersten Lauf: In den Einstellungen, Reiter „eBay & Rahmenbedingungen“, die Namen deiner drei Rahmenbedingungen („Versand“, „Zahlung“, „Rücknahme“) genau so eintragen wie im Seller Hub, dazu den „Artikelstandort (Ort oder PLZ)“. Im selben Chrome-Profil bei eBay angemeldet sein. Den ersten Lauf mit nur 1 Produkt machen: Stimmt ein Name nicht, lehnt eBay ab, und abgelehnte Produkte sind danach aus der Produkt-Datenbank raus.
→ Übersicht/CSV B2, B3, B5, B18

**12. Warum sind die Einstellungen jetzt in Reiter aufgeteilt und alles deutsch?**
Neues Design in Version 46.0: sechs Reiter „Preise & Listing“, „Produkt-Filter“, „eBay & Rahmenbedingungen“, „Beschreibungsvorlage“, „KI“, „Sicherung“. Die alten englischen Namen und ihre neuen Entsprechungen stehen in Einst 26. Deine Einstellungen bleiben beim Update erhalten. Die langen Erklärtexte sind entfallen, es gibt nur noch kurze graue Hinweise.
→ Einst 4, 26

**13. Wo ist die zweite Preistafel „Eigene Preise für „Neu: Sonstige““?**
Gibt es nicht mehr – eine Preistafel für alle Zustände. Willst du für „Neu: Sonstige“ andere Aufschläge, lege in „Variable Preise (nach Preisspanne)“ Regeln mit dem Haken „Neu: Sonstige“ an.
→ Einst 5.5, 5.6

**14. Was muss ich nach dem Update auf 46.0 unbedingt tun?**
1. Chrome komplett neu starten – beim Wechsel von 45.x Pflicht.
2. Auf das Symbol klicken: Das Dashboard muss aufgehen, unten in der Seitenleiste „Version 46.0“ oder höher stehen.
3. Angemeldet? Sonst im Dashboard anmelden.
4. Einstellungen → Reiter „Preise & Listing“: Preise und „Domain“ prüfen. Reiter „Produkt-Filter“: „Preis bis“ prüfen (aus älteren Versionen steht dort oft noch 100).
5. Abwarten, bis deine alte Produkt-Datenbank übertragen ist.
6. Im Dashboard die Karte „Dein Abo“ ansehen.
→ Konto 11, 20

---

## 2. Einrichtung und Anmeldung

**15. Wie installiere ich Cash Lister?**
Paket entpacken (am besten nach `C:\LeckAtakan`), Einrichtungsdatei neben `update.bat` legen, in Chrome `chrome://extensions` öffnen, „Entwicklermodus“ einschalten, „Entpackte Erweiterung laden“ und den Ordner `extension` wählen. Dann auf das Cash-Lister-Symbol klicken – das Dashboard öffnet sich – und mit „Einrichtungsdatei einlesen“ anmelden. Den Ordner danach nicht verschieben und den Entwicklermodus anlassen.
→ Konto 2 (Mac: Konto 3)

**16. Wie melde ich mich an?**
Auf das Cash-Lister-Symbol oben rechts in Chrome klicken, das Dashboard öffnet sich. Am bequemsten rechts in der Anmeldekarte „Einrichtungsdatei einlesen“ und deine Einrichtungsdatei wählen – dann meldet die Extension dich gleich an. Oder „Benutzername“ und „Passwort“ eintippen und „Anmelden“ klicken. Klappt es, verschwindet die Anmeldekarte, oben steht „Guten Morgen“, „Guten Tag“ oder „Guten Abend“ mit deinem Namen, und die Module in der Seitenleiste werden anklickbar.
→ Konto 5.2, 5.3; Dash 9.2, 9.3

**17. Ich klicke auf „Anmelden“, aber nichts passiert.**
Bis zu 30 Sekunden warten. Kommt „Keine Antwort vom Hintergrunddienst – bitte noch einmal versuchen.“, antwortet der Hintergrunddienst nicht – typisch nach einem Update. Chrome komplett schließen (auch unten rechts im Infobereich) und neu starten oder in `chrome://extensions` bei Cash Lister auf den Kreispfeil klicken, danach neu anmelden. Kommt nach etwa 20 Sekunden „Server nicht erreichbar (…). Adresse prüfen oder später erneut versuchen.“: Internet prüfen und in den Einstellungen (Reiter „eBay & Rahmenbedingungen“, Karte „Server & Produkt-Vergabe“) nachsehen, ob bei „Server-Adresse“ etwas steht – hat der Betreiber nichts anderes gesagt, das Feld leeren.
→ Konto 18 („Anmelden tut nichts“), Konto 5.4

**18. Es kommt „Name oder Passwort falsch.“**
Groß- und Kleinschreibung prüfen, keine Leerzeichen davor oder dahinter. Am sichersten mit „Einrichtungsdatei einlesen“ anmelden. Klappt auch das nicht, beim Betreiber nachfragen (vielleicht wurde das Passwort geändert).
→ Konto 5.5

**19. Es kommt „Deine Version der Extension ist veraltet …“.**
Die Version, die gerade im Hintergrund von Chrome läuft, ist älter als die Mindestversion. Unten in der Seitenleiste die Nummer prüfen. Ist sie alt: mit `update.bat` aktualisieren, Chrome neu starten, neu anmelden – das Update-Programm funktioniert auch mit einer veralteten Version. Ist sie schon neu: Es läuft noch der alte Hintergrunddienst – Chrome komplett neu starten bzw. „Neu laden“, in jedem Chrome-Profil. **Nicht sicher belegt:** welche Version gerade die Mindestversion ist – frag den Betreiber.
→ Konto 15, Dash 9.8

**20. Ich habe mein Passwort vergessen oder will es ändern.**
Dafür gibt es in der Extension keine Funktion. Das Passwort steht in deiner Einrichtungsdatei; ändern kann es nur der Betreiber. Nach einer Änderung brauchst du eine neue Einrichtungsdatei, sonst klappt das Update nicht mehr.
→ Konto 5 (Häufige Fragen)

**21. Wo finde ich die Einstellungen?**
Seitenleiste links → Gruppe „System“ → „Einstellungen“ (geht auch ohne Anmeldung). Oder Rechtsklick auf das Cash-Lister-Symbol → „Optionen“. Die Seite heißt „Cash Lister – Einstellungen“ und öffnet immer mit dem Reiter „Preise & Listing“. Gespeichert wird von selbst, sobald du ein Feld verlässt; „Speichern“ bestätigt nur.
→ Konto 4, Einst 2, 3

**22. Was muss ich nach der ersten Anmeldung einstellen?**
Kurz: Einstellungen öffnen. Reiter „Preise & Listing“: „Domain“ auf deinen Marktplatz, „% Aufschlag“ prüfen (Vorgabe nach Neuinstallation 120!) und einmal einen Wert eintippen. Reiter „Produkt-Filter“: Filter prüfen, besonders „Preis bis“. Reiter „KI“: OpenAI-Schlüssel eintragen. Für den CSV-Lister im Reiter „eBay & Rahmenbedingungen“ die Karte „Rahmenbedingungen“ ausfüllen. Reiter „Sicherung“: einmal „Einstellungen exportieren“. Im Dashboard die Karte „Dein Abo“ ansehen.
→ Konto 11 (vollständige Checkliste)

**23. Was soll im Feld „Server-Adresse“ stehen?**
Normalerweise nichts. Die Extension nimmt die richtige Adresse automatisch. Nur ändern, wenn der Betreiber es ausdrücklich sagt.
→ Konto 5.4, Einst 12.2, Dash 9.4

**24. Muss ich auch bei eBay oder Amazon angemeldet sein?**
Bei eBay ja: Browser-Lister, Tracker und CSV-Lister arbeiten über deine eBay-Anmeldung im **selben Chrome-Profil**. Die Extension meldet sich nicht selbst bei eBay an. Ist die eBay-Anmeldung abgelaufen, laufen Produkte beim Listen meist erst nach 15 Minuten mit „Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“ aus. Eine Anmeldung bei Amazon braucht die Extension nicht.
→ Listen 3, Tracker 3, Übersicht/CSV B4

**25. Warum sind die Module in der Seitenleiste grau?**
Du bist nicht angemeldet, dein Zugang ist abgeschaltet oder dein Abo ist gesperrt. Was zutrifft, steht unten im Kasten der Seitenleiste („Nicht angemeldet“, „Zugang abgeschaltet“, „Abo gesperrt“) und im Dashboard. Dashboard und Einstellungen bleiben immer anklickbar.
→ Konto 5.6, 18; Dash 4.2

---

## 3. Abo und Zahlung

**26. Was kostet Cash Lister?**
Laut AGB 150 € pro Monat für den ersten Shop und 50 € für jeden weiteren, jeweils netto zzgl. 19 % USt (also z. B. 178,50 € bei einem Shop, 238,00 € bei zwei Shops). Nicht enthalten sind die OpenAI-Kosten über deinen eigenen Schlüssel und Gebühren von eBay, Amazon und anderen Anbietern. Deinen Betrag zeigt die Karte „Dein Abo“ unter „Monatlich“. Individuelle Absprachen kennt diese Hilfe nicht – dafür den Betreiber fragen.
→ Konto 7.1, Dash 14.3

**27. Wie schließe ich das Abo ab?**
1. Der Betreiber schickt dir deinen persönlichen Zahlungslink.
2. Link öffnen und auf der Seite „Zahlung einrichten“ Shops, Betrag und den Tag der ersten Abbuchung prüfen, dann „Weiter zur Zahlung“.
3. Beim Zahlungsdienst Stripe Karte oder SEPA-Lastschrift hinterlegen.
4. Den Pflicht-Haken setzen („Ich handle als Unternehmer (§ 14 BGB) und stimme den AGB von Cash Lister (…) zu.“) und abschließen.
5. Im Dashboard zeigt die Karte „Dein Abo“ danach „eingerichtet“ oder „aktiv“.

Abschließen können laut AGB nur Unternehmer. Den Zahlungslink nicht weitergeben.
→ Konto 7.2

**28. Ab wann muss ich zahlen?**
Den Tag deiner ersten Abbuchung nennt deine persönliche Zahlungsseite (danach auch die Karte „Dein Abo“ bei „Erste Abbuchung“). Laut AGB werden Zeiträume, die du nach einer bisherigen Vereinbarung schon bezahlt hast, nicht noch einmal berechnet.
→ Konto 7.1

**29. Wo sehe ich mein Abo?**
Im Dashboard ganz unten in der Karte „Dein Abo“ (nur angemeldet und wenn für dich ein Abo abgerechnet wird): Marker (z. B. „aktiv“, „eingerichtet“, „Zahlung offen“), Statuszeile, „Shops“, „Monatlich“ und je nach Stand „Erste Abbuchung“, „Gekündigt zum“ oder „Zugang bis“. Fehlt die Karte dauerhaft, obwohl du zahlst: Chrome komplett neu starten, sonst den Betreiber fragen.
→ Konto 7.3, Dash 14.1, 14.3

**30. Wo bekomme ich meine Rechnungen? Wie ändere ich Karte oder Bankkonto?**
Dashboard → Karte „Dein Abo“ → „Abo verwalten“. Das Kundenportal öffnet sich in einem neuen Tab; dort rufst du die Rechnungen ab (laut AGB als PDF) und änderst die Zahlungsart. Rechnungen kommen laut AGB außerdem per E-Mail.
→ Konto 7.4, Dash 14.4

**31. Wie kündige ich?**
Dashboard → Karte „Dein Abo“ → „Abo verwalten“ → im Kundenportal kündigen, oder per E-Mail an die Adresse im Impressum auf https://cash-lister.de. Laut AGB geht das jederzeit zum Ende des laufenden Abrechnungszeitraums; bis dahin arbeitest du normal weiter. Die Karte zeigt danach „gekündigt“ und „Gekündigt zum“ mit dem Datum. Für den laufenden Zeitraum gezahlte Beträge werden bei einer normalen Kündigung nicht anteilig erstattet.
→ Konto 7.7

**32. Wie buche ich einen weiteren Shop dazu oder bestelle einen ab?**
Nicht im Kundenportal, sondern laut AGB per E-Mail beim Betreiber. Jeder Shop hat einen eigenen Zugang mit eigenem Anmeldenamen; die Zugangsdaten für einen neuen Shop bekommst du vom Betreiber. Für den Rest des laufenden Zeitraums wird anteilig verrechnet.
→ Konto 7.7, Konto 5 (Häufige Fragen)

**33. Im Dashboard steht „Zahlung offen“ oder „Zahlung überfällig“. Was muss ich tun?**
In der Warnleiste oben auf „Jetzt bezahlen“ klicken und auf der Zahlungsseite die Zahlung erledigen (z. B. „Offene Rechnung bezahlen“, falls angezeigt). Hat eine Abbuchung nicht geklappt (Karte abgelaufen, Konto nicht gedeckt), im Kundenportal („Abo verwalten“) die Zahlungsart prüfen bzw. ändern. Bis zu welchem Tag dein Zugang ohne Zahlung noch läuft, steht in der Leiste („Ohne Zahlung wird dein Zugang nach dem … gesperrt.“). Fehlt der Knopf, kennt das Dashboard deinen Link nicht – Betreiber fragen.
→ Konto 7.5, Dash 14.2

**34. Was heißt „Zahlung unterwegs“?**
Eine SEPA-Lastschrift läuft noch; bei Lastschrift steht erst einige Werktage nach dem Einzug fest, ob sie geklappt hat. Du musst nichts tun, sorge nur dafür, dass dein Konto gedeckt ist.
→ Konto 7.3, Dash 18

**35. Mein Abo ist gesperrt. Was heißt das und wie werde ich wieder frei?**
Bei einer Sperre sind alle Module außer Dashboard und Einstellungen grau, die Anmeldung wird abgelehnt („Anmeldung abgelehnt: Abo gesperrt.“), „Starten“ im Browser-Lister startet keinen Lauf, und auch `update.bat` kann sich nicht anmelden. Erhalten bleiben laut AGB dein Konto, deine gesicherten Einstellungen und die Zuteilungen der Produkte, die du schon bei eBay anbietest. So wirst du wieder frei:
1. Im Dashboard auf „Zur Zahlungsseite“ klicken (oder deinen Zahlungslink öffnen).
2. Die offene Zahlung erledigen.
3. Danach im Dashboard neu anmelden.
4. Kommt weiter „Anmeldung abgelehnt: Abo gesperrt.“, ist die Zahlung noch nicht angekommen – etwas später erneut versuchen, sonst den Betreiber fragen.

**Nicht sicher belegt:** wie schnell die Sperre nach der Zahlung aufgehoben ist (laut AGB „in der Regel automatisch“).
→ Konto 7.6, Dash 9.7, 14.6

**36. Kann die Hilfe meine Sperre aufheben, eine Frist verlängern oder einen anderen Preis zusagen?**
Nein. Das entscheidet nur der Betreiber. Rechtlich verbindlich sind die AGB auf https://cash-lister.de.
→ Konto 7

**37. Kann ich das Abo pausieren?**
**Nicht sicher belegt:** Eine Pause ist weder in der Extension noch in den AGB beschrieben. Frag den Betreiber.
→ Konto 7 (Häufige Fragen zum Abo)

**38. Ich habe meinen Zahlungslink verloren.**
Ist er dem Dashboard bekannt, findest du ihn in der Karte „Dein Abo“ („Zahlungsseite“), in der Warnleiste („Jetzt bezahlen“ bzw. „Abo einrichten“) oder bei einer Sperre („Zur Zahlungsseite“). Sonst den Betreiber fragen.
→ Konto 7 (Häufige Fragen zum Abo)

**39. „Abo verwalten“ öffnet nichts.**
Die Meldung neben dem Knopf lesen: Bei „Kundenportal im neuen Tab geöffnet.“ in der Tab-Leiste nach dem neuen Tab schauen. Bei „Noch kein Abo eingerichtet – das geht über die Zahlungsseite.“ erst das Abo einrichten. Kommt „Kundenportal gerade nicht erreichbar …“ immer wieder: Chrome komplett neu starten, sonst den Betreiber fragen.
→ Konto 7.4, Dash 14.4, 19

**40. Wo stehen AGB, Datenschutz und Impressum?**
Auf der Webseite https://cash-lister.de, unten auf der Seite unter „Impressum“, „Datenschutz“ und „AGB“. Die bei deinem Abschluss gültige Fassung der AGB ist im Bestellvorgang verlinkt.
→ Konto 7.8

---

## 4. Konto, Kosten, Zugang

**41. Habe ich Guthaben oder Credits? Kostet ein Listing etwas?**
Nein. In der Extension gibt es kein Guthaben und keine Credits; beim Listen wird nichts abgezogen. Bezahlt wird das monatliche Abo. Die KI kostet über deinen eigenen OpenAI-Schlüssel (OpenAI rechnet direkt mit dir ab), eBay-Gebühren zahlst du an eBay. Das Tageskontingent des CSV-Listers ist eine Tagesgrenze, kein Guthaben.
→ Konto 6

**42. Was heißt „Für den Tracker brauchst du die Ultimate-Mitgliedschaft.“? Gibt es Abo-Stufen?**
Trotz des Wortlauts: Du bist nicht angemeldet, dein Zugang ist abgeschaltet oder dein Abo gesperrt. Es gibt keine Stufen; mit aktivem Zugang und gültigem Abo sind alle Module frei. Im Dashboard nachsehen und anmelden, dann den Tracker über die Seitenleiste neu öffnen.
→ Konto 5.9, 6; Meldungen 20

**43. Brauche ich einen OpenAI-Schlüssel, und wo trage ich ihn ein?**
Ja, für alle Produkte aus der Produkt-Datenbank – der Titel kommt immer von der KI. Eintragen: Einstellungen → Reiter „KI“ → „OpenAI-API-Schlüssel (für die Titel-Generierung)“. Einen Schlüssel bekommst du bei OpenAI unter platform.openai.com (eigenes Konto nötig). Er wird nie auf den Server gesichert – nach einer Neuinstallation neu eintragen oder aus deiner Export-Datei holen.
→ Einst 15.1, Konto 6

**44. Darf ich mich auf mehreren Rechnern oder Chrome-Profilen mit demselben Konto anmelden?**
Technisch ist das vorgesehen: Die Produkt-Datenbank ist für alle Geräte eines Kontos gemeinsam, und jedes Gerät bekommt beim Listen andere Produkte („In Arbeit“). In der Extension ist keine Grenze für die Zahl der Geräte zu sehen. **Nicht sicher belegt:** ob der Betreiber sie trotzdem begrenzt – frag ihn im Zweifel. Laut AGB darfst du deine Zugangsdaten nicht an Dritte weitergeben (Mitarbeiter, die für deine Shops arbeiten, gelten nicht als Dritte). Die Einstellungen der Geräte gleichen sich nicht von selbst ab (Abschnitt 6).
→ Konto 5 (Häufige Fragen), Konto 9

**45. Brauche ich für jeden Shop einen eigenen Zugang?**
Ja. Im Abo zählt jeder Shop als eigener Zugang mit eigenem Anmeldenamen; Produkt-Datenbank und Einstellungs-Sicherung gelten je Zugang.
→ Konto 5 (Häufige Fragen)

**46. Was heißt „Zugang abgeschaltet“?**
Der Betreiber hat deinen Zugang abgeschaltet („Dieser Zugang ist abgeschaltet.“ bzw. „Zugang abgeschaltet – bitte beim Betreiber melden.“). Das lässt sich nur über den Betreiber lösen. Es ist etwas anderes als eine Abo-Sperre.
→ Konto 6, Dash 9.6

---

## 5. Updates, Versionen, Chrome

**47. Wie mache ich ein Update?**
Chrome **komplett** schließen (auch im Infobereich unten rechts), im Programmordner auf `update.bat` doppelklicken (Mac: `update.command`), warten bis „Fertig. Chrome jetzt wieder starten.“ oder „Du hast bereits die neueste Version.“ erscheint, dann Chrome starten, auf das Symbol klicken und unten in der Seitenleiste die Versionsnummer prüfen. Einstellungen bleiben erhalten, die Produkt-Datenbank liegt auf dem Server.
→ Konto 12 (Mac: Konto 13)

**48. Woher weiß ich, dass es ein Update gibt?**
Die Extension zeigt keinen Hinweis und aktualisiert sich nicht von selbst. Starte `update.bat`; gibt es nichts Neues, sagt das Programm das. **Nicht sicher belegt:** auf welchem Weg der Betreiber neue Versionen ankündigt – frag ihn.
→ Konto 12

**49. Nach dem Update geht nichts mehr: Anmelden tut nichts, Knöpfe reagieren nicht, „veraltet“, obwohl die neue Nummer dasteht, oder das kleine Fenster erscheint.**
Im Hintergrund läuft noch die alte Version. Chrome komplett schließen und neu starten bzw. in `chrome://extensions` auf den Kreispfeil klicken – in **jedem** Chrome-Profil, das Cash Lister benutzt. Merksatz: Nach jedem Update Chrome komplett neu starten.
→ Konto 17, 18

**50. Das Update-Fenster sagt „Chrome laeuft noch.“**
Chrome vollständig schließen (auch im Infobereich unten rechts → Rechtsklick → „Beenden“), dann im Fenster eine Taste drücken. Hilft das nicht: Task-Manager (Strg+Umschalt+Esc) → Reiter „Details“ → alle `chrome.exe` beenden. Auf dem Mac Chrome mit Cmd+Q beenden und `update.command` erneut starten.
→ Konto 12 („Wenn Chrome noch läuft“), Konto 13

**51. Das Update meldet „Server nicht erreichbar“, obwohl mein Internet geht.**
Mögliche Ursachen: VPN, Firewall oder Virenscanner; ein alter Updater (steht oben „Melde an bei …“ statt einer Zeile „Server: …“, dann den Updater einmalig erneuern); oder dein Abo ist gesperrt – das Update-Programm zeigt eine Abo-Sperre unter Windows ebenfalls als „Server nicht erreichbar (…)“ an. Im Dashboard nachsehen, ob „Abo gesperrt“ steht; dann erst bezahlen.
→ Konto 12 (Meldungen), 14, 7.6

**52. Das Update hat einen anderen Fehler gemeldet.**
Bei Fehlern vor dem Tausch bleibt dein Ordner unverändert – einfach noch einmal versuchen. Häufige Ursachen: Chrome lief noch, Einrichtungsdatei fehlt oder ist veraltet, Ordner liegt nicht auf Laufwerk C:, kein Internet, alter Updater, Abo gesperrt. Die genaue Meldung steht in der Tabelle.
→ Konto 12 („Alle Meldungen des Windows-Updates“), Konto 13, 18

**53. Kann ich zur vorherigen Version zurück?**
Ja, solange der Ordner `extension_alt_…` neben `extension` liegt. Achtung beim Zurückgehen auf 45.x: Dort ist die Produkt-Datenbank leer (die Produkte liegen auf dem Server und sind mit 46.0 wieder da), und es erscheint wieder das kleine Fenster. Ist die alte Version zu alt, kann der Server sie abweisen. Nur nach Rücksprache mit dem Betreiber zurückgehen.
→ Konto 16

**54. Die Extension ist plötzlich weg oder grau.**
Nicht vorschnell auf „Entfernen“ klicken. In `chrome://extensions` prüfen, ob der „Entwicklermodus“ an ist. Ist die Karte grau: einschalten und prüfen, ob der Ordner `extension` noch am alten Ort liegt. Ist die Karte ganz weg: Extension neu laden und im Dashboard anmelden – die Server-Sicherung holt die Einstellungen zurück, die Produkt-Datenbank liegt ohnehin auf dem Server; den OpenAI-Schlüssel neu eintragen oder aus deiner Export-Datei holen. **Nicht sicher belegt:** warum das bei manchen Kunden passiert.
→ Konto 18 („Extension verschwunden“)

---

## 6. Einstellungen sichern und umziehen

**55. Werden meine Einstellungen gesichert?**
Ja, mit Anmeldung automatisch je Konto auf dem Server – aber **ohne** OpenAI-Schlüssel, ohne die Filter „Mind. Sterne“, „Mind. Bewertungen“, „Mind. Lagerbestand“, ohne die Ein/Aus-Schalter der Amazon-Filter und ohne den Server-Modus. Die Produkt-Datenbank liegt ohnehin auf dem Server. Für eine Kopie mit Schlüssel zusätzlich regelmäßig „Einstellungen exportieren“ (Einstellungen → Reiter „Sicherung“). Die Export-Datei enthält deinen Schlüssel – nicht weitergeben.
→ Konto 9, 10; Einst 16

**56. Ich habe zwei Rechner. Gleichen sich die Einstellungen automatisch ab?**
Nein. Ein frisch installierter Rechner holt beim ersten Anmelden die Server-Sicherung. Danach gilt auf dem Server, was zuletzt gesichert wurde. Änderst du später etwas auf Rechner A, holst du es auf Rechner B mit „Einstellungen vom Server holen“ (Reiter „Sicherung“) oder stellst es dort von Hand ein. Die Produkt-Datenbank ist dagegen immer für beide dieselbe.
→ Konto 9 („Wichtig bei zwei Geräten“), Einst 22

**57. Meine Einstellungen sind weg.**
Prüfen: angemeldet? Richtiges Chrome-Profil? Dann Einstellungen → Reiter „Sicherung“ → Statuszeile lesen; bei einem Konflikt entscheiden, sonst „Einstellungen vom Server holen“. Für den OpenAI-Schlüssel deine Export-Datei importieren. Danach offene Cash-Lister-Tabs neu laden.
→ Konto 18 („Einstellungen weg“), Konto 9

**58. Im Reiter „Sicherung“ steht „Achtung: Auf dem Server liegt eine Sicherung … Bitte entscheiden“, oder die Glocke meldet „Einstellungen: zwei Geräte“.**
Das ist ein Konflikt zwischen zwei Geräten. Sind die Server-Einstellungen richtig: „Einstellungen vom Server holen“. Sind die Einstellungen dieses Geräts richtig: „Dieses Gerät auf den Server sichern“. Bis du entscheidest, wird nichts überschrieben.
→ Konto 9 („Konflikt lösen“), Einst 16.5

**59. Wie ziehe ich auf einen neuen Rechner um?**
Auf dem alten Rechner „Einstellungen exportieren“. Auf dem neuen installieren und im Dashboard mit der Einrichtungsdatei anmelden (die Server-Sicherung holt die Einstellungen meist automatisch, die Produkt-Datenbank ist auf dem Server). Dann im Reiter „Sicherung“ die Export-Datei importieren, damit der OpenAI-Schlüssel mitkommt. Danach „Domain“, Preise und Amazon-Filter prüfen.
→ Konto 10 („Rechnerwechsel“), Einst 16.7

---

## 7. Produkte finden und Produkt-Datenbank

**60. Wie bekomme ich Produkte in die Produkt-Datenbank?**
Drei Wege, alle nur angemeldet und mit erreichbarem Server: auf einer Amazon-Suchseite den blauen Knopf unten rechts („📦 … → Datenbank“); im Verkäufer-Schaufenster „📚 Ganzer Shop → Datenbank“; oder in der Produkt-Datenbank in der Karte „Links hinzufügen“ Links bzw. ASINs einfügen und „Zur Datenbank hinzufügen“ klicken.
→ Produkte 1, 3, 5, 10.7

**61. Der blaue Knopf auf Amazon erscheint nicht.**
Er erscheint nur auf Amazon-Suchseiten mit Suchbegriff (in der Adresse steht `k=`) und im Verkäufer-Schaufenster (`me=`) – nicht auf Kategorie-Seiten ohne Suchbegriff, Marken-Shops oder Produktseiten.
→ Produkte 3.1, 3.7

**62. Beim Import kommt „❌ Bitte zuerst in Cash Lister anmelden – nichts importiert.“ oder eine Meldung „Server nicht erreichbar“.**
Seit Version 46.0 liegt die Produkt-Datenbank auf dem Server; ohne Anmeldung oder Server wird nichts importiert. Im Dashboard anmelden bzw. später erneut versuchen. Die Anmelde-Meldung kann auch bei abgeschaltetem Zugang oder gesperrtem Abo kommen – dann im Dashboard nachsehen.
→ Produkte 3.5, 10.7

**63. Warum sind viele Produkte „von anderen Kunden belegt“?**
Das ist die Produkt-Vergabe: Ein anderer Kunde hat das Produkt vorher übernommen; so listet ihr nicht dasselbe Produkt. Welcher Kunde es ist, siehst du nicht.
→ Produkte 13

**64. Sehe ich auf meinen zwei PCs dieselben Produkte?**
Ja, wenn beide mit demselben Zugang angemeldet sind. Beim Listen bekommt jedes Gerät andere Produkte. Die „Sortierung“ der Produkt-Datenbank und die Einstellung „Domain“ gelten aber je Gerät – „Domain“ deshalb auf allen Geräten gleich einstellen.
→ Produkte 10.1, 10.15

**65. Was heißt „In Arbeit“?**
Ein Lister (auf irgendeinem deiner Geräte, auch der CSV-Lister) hat das Produkt gerade zum Listen genommen; andere Geräte bekommen es so lange nicht. In der Spalte „In Arbeit“ steht, wer es hat und bis wann (z. B. „Server-1 bis 14:32“). Stürzt ein Gerät ab, wird das Produkt nach dieser Uhrzeit von selbst frei – beim Browser-Lister nach etwa einer halben Stunde. Willst du nicht warten, kannst du es mit „✕“ löschen (mit Rückfrage; nur, wenn das Gerät wirklich nicht mehr daran arbeitet). **Nicht sicher belegt:** ob der Server die Zeiten in jedem Fall genau so übernimmt.
→ Produkte 10.9, 10.10

**66. „Alle löschen“ hat nicht alles gelöscht.**
Richtig so: Produkte „In Arbeit“ bleiben stehen („… bleiben stehen (einzeln mit ✕ löschbar).“). „Alle löschen“ gilt für alle Geräte deines Kontos und lässt sich nicht rückgängig machen – vorher bei Bedarf „Als TXT exportieren“.
→ Produkte 10.11

**67. Warum wird meine Produkt-Datenbank kleiner, obwohl ich nichts lösche?**
Jedes Produkt, das ein Lauf bearbeitet, verlässt die Datenbank – auch wenn das Listen scheitert. Fehlgeschlagene Produkte stehen im „Statusbericht“; willst du sie erneut versuchen, füge den Link wieder hinzu. Läuft auf einem anderen deiner Geräte oder im CSV-Lister ein Lauf, nimmt der auch Produkte.
→ Listen 6.3, 7.5, 25

**68. Wie übernehme ich einen ganzen Amazon-Shop?**
Schaufenster des Händlers öffnen (Adresse mit `me=`), auf der **ersten** Ergebnisseite bleiben, Häkchen prüfen, „📚 Ganzer Shop → Datenbank“ klicken und warten (höchstens 30 Seiten pro Klick). Wer nicht auf Seite 1 startet, verliert Seite 1.
→ Produkte 5.2, 5.3

**69. Was macht der Konkurrenz-Scanner?**
Er nimmt die Produkte eines eBay-Verkäufers und sucht per Bildvergleich auf amazon.de die passende Amazon-Quelle. Funde werden für dich reserviert und unter „Gefundene Produkte“ gespeichert (nur in diesem Chrome-Profil). Der Browser-Lister kann sie mit dem Titel des Konkurrenten listen („Produkte aus“ → „Konkurrenz-Scanner“). Ausgelegt auf eBay.de und amazon.de.
→ Produkte 12, Listen 6.9

---

## 8. Listen mit dem Browser-Lister

**70. Wie liste ich meine ersten Produkte?**
1. Checkliste prüfen: im Dashboard angemeldet, Abo in Ordnung, im selben Chrome-Profil bei eBay angemeldet, „Domain“ und Preise eingestellt, OpenAI-Schlüssel eingetragen, „Listing automatisch absenden“ an, Filter geprüft.
2. Produkte in die Produkt-Datenbank holen (Abschnitt 7).
3. Browser-Lister öffnen (Seitenleiste oder Dashboard-Karte „Browser-Lister“).
4. „Produkte aus“ = „Produkt-Datenbank“; daneben muss mehr als 0 „verfügbar“ stehen.
5. „Wie viele Angebote“ klein anfangen, z. B. 3; „Gleichzeitig“ auf 1; „Fehler-Tabs schließen“ für den Test aus.
6. „Starten“ klicken.
7. Danach den „Statusbericht“ öffnen und ein fertiges Angebot prüfen (Titel, Preis, Bilder, Beschreibung, Zustand, Versand).
→ Listen 3, 7.1

**71. „Starten“ ist grau.**
Ist gerade ein Lauf zu Ende gegangen: Seite neu laden (F5). Glaubt die Seite, es läuft noch ein Lauf (z. B. nach einem Absturz): „Stoppen & zurücksetzen“ klicken. War der Lauf pausiert: zum Weitermachen „Fortsetzen“ nehmen.
→ Listen 5.14, 26

**72. „Starten“ meldet „Die Produkt-Datenbank ist leer …“ oder „Alle … Produkte der Datenbank sind gerade in Arbeit …“.**
Leer: erst Produkte einsammeln. Alle in Arbeit: Ein anderes Gerät oder der CSV-Lister hat gerade alle übrigen Produkte – warten, deine anderen Geräte prüfen oder neue Produkte sammeln.
→ Listen 5.6, 6.4; Meldungen 21

**73. Der Server ist weg – was passiert mit meinem Lauf?**
Der Browser-Lister pausiert („⚠ Server nicht erreichbar – Lister pausiert, macht von selbst weiter.“) und macht von selbst weiter, sobald der Server wieder antwortet; du musst nichts tun. Ohne Server listet er nichts aus der Produkt-Datenbank. Einen neuen Lauf aus der Produkt-Datenbank kannst du ohne Server nicht starten („Server nicht erreichbar - die Produkt-Datenbank liegt auf dem Server. Bitte später erneut starten.“).
→ Listen 6.5, 5.6

**74. Viele Produkte scheitern mit „Amazon-Preis zu hoch (Filter „Preis bis“)“, obwohl ich keine Grenze eingestellt habe.**
Aus einer älteren Version steht bei „Preis bis“ oft noch 100 (früher hat das kleine Fenster diesen Wert eingetragen). Einstellungen → Reiter „Produkt-Filter“ → Karte „Amazon-Filter“ → „Preis bis“: Wert erhöhen oder den Schalter ausschalten.
→ Listen 9.4, Einst 8.6

**75. „Produkt ist nicht auf Lager“, obwohl das Produkt auf Amazon lieferbar ist.**
Häufig ist die Lieferzeit zu lang: Liegt sie über „Max. verlängerte Lieferzeit“ (Reiter „Produkt-Filter“, Standard 20 Tage), gilt das Produkt als nicht vorrätig. Zahl erhöhen – den Schalter davor auszuschalten reicht beim Listen nicht.
→ Listen 9.5, Einst 8.2

**76. Jedes Produkt scheitert mit „Zeitüberschreitung: 15 Minuten keine Rückmeldung vom Listing“.**
Häufigste Ursachen: nicht bei eBay angemeldet, „Listing automatisch absenden“ aus, eBay zeigt eine Sicherheitsabfrage, „Domain“ falsch oder „Keine“, eBay zeigt eine Fehlerseite. Zum Eingrenzen „Fehler-Tabs schließen“ ausschalten, ein Produkt mit „Gleichzeitig“ 1 listen und auf den Titel des eBay-Tabs achten.
→ Listen 26

**77. Jedes Produkt scheitert mit „KI-Titel ist leer“.**
Die KI hat keinen Titel geliefert: OpenAI-Schlüssel, Guthaben und Konto bei OpenAI prüfen (Einstellungen → Reiter „KI“). Typisch nach einem Rechnerwechsel, weil der Schlüssel nicht auf dem Server gesichert wird. Ohne funktionierende KI wird aus der Produkt-Datenbank nichts gelistet.
→ Listen 26, Einst 15, Meldungen 18

**78. Was bedeutet „Nicht eingestellt: eBay verlangt Angebotsgebühren (…)“?**
eBay hat im Formular eine Gebühr über 0 angezeigt, und deshalb wurde nicht eingestellt. Willst du trotzdem automatisch einstellen: Einstellungen → Reiter „eBay & Rahmenbedingungen“ → Karte „Beim Einstellen“ → „Auch mit Angebotsgebühr einstellen“ einschalten (die Gebühren zahlst du an eBay).
→ Listen 18.1, Einst 11.1

**79. Ich sehe „Produkt bereits von einem anderen Nutzer vergeben“.**
Ein anderer Kunde hat das Produkt zuerst übernommen; die Extension listet es nicht. Such dir ein anderes Produkt.
→ Listen 19, Produkte 13

**80. Kann ich Promoted Listings (Anzeigen) abschalten?**
Über die Extension nicht. Bietet eBay die Option an, schaltet die Extension sie ein und setzt die Rate aus „Anzeigengebühr (%)“ (Reiter „Preise & Listing“, Standard 2,3).
→ Listen 15.5, Einst 6.3

**81. Warum steht als Marke immer „Unbranded“, und was ist die seltsame Zeichenfolge im Custom Label?**
Der Browser-Lister trägt als Marke immer „Unbranded“ ein. Im Custom Label (SKU, auf eBay.de „Bestandseinheit“) steht eine Kennung von Cash Lister (endet auf „==“). Daran erkennen Tracker und Produkt-Vergabe dein Angebot – **nicht ändern**.
→ Listen 13, 25

**82. In meinen Beschreibungen steht ein Spielzeug-Warnhinweis.**
Er erscheint, wenn die KI das Produkt als Spielzeug einstuft, unsicher ist, keine Antwort kommt oder kein OpenAI-Schlüssel eingetragen ist. Abschalten lässt er sich nicht; mit dem Platzhalter `_SPIELZEUG_WARNUNG_` in deiner Beschreibungsvorlage bestimmst du, wo er steht.
→ Listen 11.3, Einst 14.2

**83. Warum fehlen Wörter wie „Leder“, „Garantie“ oder „CE“ in Titel oder Beschreibung?**
Ein eingebauter Wortfilter entfernt beim Listen bestimmte Werbe-, Prüfzeichen- und Garantie-Begriffe – das Produkt wird trotzdem gelistet. Die Liste ist fest und nicht einstellbar.
→ Einst 9.3; Listen 10.4

**84. Wie verhindere ich, dass bestimmte Marken gelistet werden (z. B. wegen VeRO)?**
Eine automatische VeRO-Prüfung gibt es nicht. Trag die Marken in deine Blacklist ein: Einstellungen → Reiter „Produkt-Filter“ → Karte „Blacklist“ → „Meine Liste“, ein Eintrag pro Zeile. Treffer werden beim Listen übersprungen („Produkt enthält ein Wort aus der Blacklist: …“). Schon gelistete Angebote werden nicht nachträglich geprüft.
→ Einst 9.1, 9.2

**85. Wie liste ich fehlgeschlagene Produkte noch einmal?**
Einen „Wiederholen“-Knopf gibt es nicht. „Statusbericht“ öffnen, die Ursache in der Spalte „Meldung“ beheben, den Link aus der Spalte „Amazon-Link“ kopieren, in der Produkt-Datenbank bei „Links hinzufügen“ einfügen, „Zur Datenbank hinzufügen“ klicken und einen neuen Lauf starten.
→ Listen 7.5

**86. Wie viel „Gleichzeitig“ soll ich nehmen, und darf ich Chrome während eines Laufs schließen?**
**Nicht sicher belegt:** Eine empfohlene Zahl gibt es nicht. Mehr gleichzeitig ist schneller, belastet aber Rechner, Amazon, eBay und dein OpenAI-Konto. Chrome und den Browser-Lister-Tab während des Laufs offen lassen – geschlossen läuft nichts weiter, auch nicht bei der Zeitschaltung.
→ Listen 5.5, 5.13, 25

**87. Wie verteile ich das Listen über mehrere Tage?**
Mit der Karte „Zeitschaltung“ im Browser-Lister: „Zeitschaltung an“ setzen und bei „danach … Stunden Pause, dann weiter“ z. B. 24 eintragen. Die Zahl bei „Wie viele Angebote“ ist dann die Menge pro Runde. Chrome und der Tab müssen offen bleiben.
→ Listen 5.13, 7.2

---

## 9. Preise

**88. Wo stelle ich den Preisaufschlag ein, und wie rechnet die Extension?**
Einstellungen → Reiter „Preise & Listing“ → Karte „Preise“. Verkaufspreis = Amazon-Preis + Amazon-Preis × „% Aufschlag“ ÷ 100 + „Fester Aufschlag (€)“. Ist die „Preisendung“ an (Vorgabe 0,99), wird auf den nächsten vollen Euro aufgerundet und auf die Endung gesetzt. Beispiel: 18,40 € + 30 % + 2 € = 25,92 € → 25,99 €. eBay-Gebühren rechnet die Extension nicht ein. Dieselbe Rechnung gilt beim Listen und im Tracker.
→ Einst 5.4, Listen 15

**89. Ändert eine Preisänderung meine schon gelisteten Angebote?**
Nicht von selbst. Bestehende Angebote bekommen neue Preise erst, wenn der Tracker sie nachpreist und hochlädt.
→ Tracker 10, Einst 5.6 (Häufige Fragen)

**90. Der Tracker preist zum Amazon-Preis ohne Aufschlag nach.**
Nach einer Neuinstallation ist die Preis-Einstellung erst vollständig gespeichert, wenn du in der Karte „Preise“ einmal etwas eintippst. Bis dahin rechnet nur das Listen mit den 120 %, der Tracker ohne Aufschlag. In „% Aufschlag“ deinen Wert neu eintippen (auch wenn er schon dasteht), dann den Tracker-Tab neu laden.
→ Einst 5.1, Tracker 10

**91. Wie stelle ich andere Aufschläge je nach Preis ein?**
„Variable Preise (nach Preisspanne)“ einschalten, mit „Regel“ Zeilen anlegen und immer „ab €“ **und** „bis €“ ausfüllen. Es zählt die erste passende Regel; passt keine, gelten die Werte oben in der Karte.
→ Einst 5.5

**92. Ich will die ,99-Endung nicht.**
Den Schalter neben „Preisendung“ ausschalten – nicht das Feld leeren (ein leeres Feld ergibt keinen gültigen Preis). In das Feld nur Werte von 0 bis 0,99 eintragen.
→ Einst 5.3

---

## 10. Tracker

**93. Was macht der Tracker?**
Er holt die Liste deiner aktiven eBay-Angebote, prüft für jedes die Amazon-Seite (lieferbar? versendet von Amazon? Preis?), rechnet deinen eBay-Preis mit den Aufschlägen aus den Einstellungen und lädt Preis- und Mengenänderungen am Ende jedes vollständigen Laufs automatisch zu eBay hoch. Nicht mehr kaufbare Produkte setzt er auf Menge 0 oder beendet sie. Titel, Bilder und Beschreibung fasst er nicht an; er bearbeitet nur Angebote, die Cash Lister eingestellt hat.
→ Tracker 1

**94. Wie mache ich einen Tracker-Lauf?**
1. Seitenleiste → „Tracker“.
2. Karte „Filter“: „Lieferant“ = „Amazon“, „eBay-Seite“ = dein Land.
3. „Upload-Einstellungen“ prüfen (z. B. „Menge auf 0 setzen“ oder „Angebot beenden“, „Feste Menge“).
4. „Angebote von eBay laden“ klicken und warten, bis bei „Bericht:“ eine Zahl steht.
5. Bei „Ab Artikel“ „0“ eintragen.
6. „Lauf starten“. Am Ende wird automatisch hochgeladen.

Beim allerersten Lauf nach einigen Dutzend Artikeln „Pausieren“ und die Vorschau im Fenster „Upload-Einstellungen“ prüfen.
→ Tracker 21.1, 21.2

**95. Wo sind „Get Listings From Ebay“, „Update Listings“, „Export CSV“ und „Retry Failed Listings“?**
„Get Listings From Ebay“ heißt jetzt „Angebote von eBay laden“. Die anderen Knöpfe gibt es schon seit Version 45.5 nicht mehr: Hochgeladen wird automatisch am Ende jedes vollständigen Laufs (der Haken zum Abschalten ist seit 46.0 weg), und „ERROR_503“-Zeilen prüft der Tracker beim Fortsetzen von selbst noch einmal.
→ Tracker 26

**96. „Lauf starten“ ist grau.**
Entweder sind noch keine Angebote geladen, oder ein Lauf ist gerade fertig geworden. „Angebote von eBay laden“ klicken – danach ist „Lauf starten“ wieder klickbar.
→ Tracker 7.7

**97. Der Tracker prüft nur die letzten paar Angebote.**
„Ab Artikel“ stand noch auf der Zahl vom letzten Lauf. Vor jedem kompletten Lauf von Hand „0“ eintragen.
→ Tracker 7.4

**98. „Upload zu eBay fehlgeschlagen: unbekannt“ – ist wirklich nichts hochgeladen?**
Oft doch. Der Tracker wartet nur 90 Sekunden auf die Bestätigung; der Upload läuft meist trotzdem durch. Bei eBay auf der Upload-Seite im Seller Hub (`/sh/reports/uploads`) nachsehen, bevor du etwas wiederholst.
→ Tracker 12.4

**99. Was bedeuten „⏳ Kurz warten!“ und „⛔ Notbremse“?**
„Kurz warten!“ (früher „Hold Tight!“): Amazon sperrt kurz oder Seiten laden nicht – der Tracker wartet 120 Sekunden und macht dann von selbst weiter. „Notbremse“: 200 Artikel hintereinander galten als nicht kaufbar, oder von mindestens 200 bewerteten Artikeln hatten mehr als 70 % kein „Success“; der Lauf hält an und lädt nichts hoch, damit nicht massenhaft gesunde Angebote auf 0 gesetzt werden. Beides ist ein Schutz, kein Defekt.
→ Tracker 16

**100. Viele Zeilen „Error: Artikel bei Amazon nicht verfügbar“, obwohl die Produkte lieferbar sind.**
„eBay-Seite“ prüfen (richtiges Land?), „Max. verlängerte Lieferzeit“ in den Einstellungen prüfen (zu lange Lieferzeit zählt als nicht verfügbar), einige Links selbst öffnen. Beim ersten Lauf vor dem Ende pausieren und die Vorschau prüfen.
→ Tracker 9.2, 23; Meldungen 21

**101. Wird ein Angebot beendet, wenn Amazon gerade nicht erreichbar ist?**
Nein. Abrufprobleme (Sperre, Zeitüberschreitung, Internet weg) ändern nichts. Nur wenn der Tracker die Seite gelesen und „nicht kaufbar“ festgestellt hat, wird je nach Einstellung auf 0 gesetzt oder beendet. Dass fast jeder Status mit „Error: “ beginnt, heißt nicht, dass etwas kaputt ist.
→ Tracker 9.2, 22; Meldungen 15.3

**102. Muss der Tracker-Tab offen bleiben? Läuft er weiter, wenn der Server weg ist?**
Der Tracker-Tab und Chrome müssen offen bleiben, das Dashboard nicht. Zeigt die Seitenleiste „Server nicht erreicht“, prüft und lädt der Tracker trotzdem; nur der Abgleich der Produkt-Vergabe meldet dann einen Fehler.
→ Tracker 3, 22

---

## 11. Weitere Module

**103. Was ist der CSV-Lister, und wie unterscheidet er sich vom Browser-Lister?**
Der CSV-Lister nimmt Produkte aus derselben Produkt-Datenbank, baut daraus **eine Datei** und lädt sie selbst im eBay Seller Hub hoch; danach holt er eBays Ergebnis ab. Der Browser-Lister füllt dagegen für jedes Produkt das eBay-Formular im Browser aus. Der CSV-Lister ist auf eBay.de ausgelegt, braucht die Karte „Rahmenbedingungen“ (Einstellungen → Reiter „eBay & Rahmenbedingungen“) und hat ein Tageskontingent. Beide können gleichzeitig laufen.
→ Übersicht/CSV B1–B5

**104. Was ist das Tageskontingent, und kann es erhöht werden?**
So viele Produkte darfst du pro Tag mit dem CSV-Lister bearbeiten (Anzeige neben „Produkte“: „Heute noch … von …“), für alle deine Geräte zusammen; ab Mitternacht ist es wieder frei. Jedes angefangene Produkt zählt. Die Höhe legt der Betreiber fest, ob sie erhöht werden kann, entscheidet er.
→ Übersicht/CSV B8

**105. Was ist die Verkaufs-Übersicht (Produktübersicht)?**
Sie liest deinen eBay-Angebotsbericht und Bestellberichte ein und zeigt, welche Angebote lange nichts verkauft haben (Ladenhüter, mit „Beenden-CSV für markierte erstellen“) und wie lange es bis zum ersten Verkauf dauert. Öffnen: Seitenleiste → „Auswerten“ → „Verkaufs-Übersicht“. Achtung: Mit „Produktübersicht“ kann auch die Produkt-Datenbank gemeint sein – im Zweifel nachfragen.
→ Übersicht/CSV A1, A6, A7

**106. Ich sehe „Format geprüft …“ in meinen Meldungen. Was heißt das?**
Zu dieser Prüfung gibt es keine Beschreibung – bei Fragen an den Betreiber wenden.
→ Meldungen 10.5

**107. Was ist ein Server-Gerät („Server-Modus“)?**
Ein weiterer Rechner mit Cash Lister (z. B. ein gemieteter Server), auf dem Tracker oder Browser-Lister laufen. Schaltest du dort in Einstellungen → Reiter „eBay & Rahmenbedingungen“ → Karte „Server-Modus“ „Dieses Gerät ist ein Server“ ein, zeigt das Dashboard deiner anderen Geräte, was dort läuft, und zählt es bei „Heute gelistet“ mit. Das Gerät muss mit demselben Zugang angemeldet sein.
→ Dash 13, Einst 13

---

## 12. Wenn nichts mehr hilft

**108. Was soll ich dem Betreiber schicken?**
1. Version (ganz unten in der Seitenleiste, z. B. „Version 46.0“)
2. Welche Seite bzw. welcher Bereich (bei den Einstellungen auch der Reiter)
3. Was du gemacht hast, Schritt für Schritt
4. Den genauen Wortlaut der Meldung oder einen Screenshot – ohne Passwörter, Schlüssel und Zahlungsdaten im Bild
5. Ungefähr wann es passiert ist
6. Ob du Chrome schon komplett neu gestartet bzw. die Extension in `chrome://extensions` neu geladen hast

Die Kontaktangaben des Betreibers stehen auch im Impressum auf https://cash-lister.de.
→ Meldungen 21 („Eine Meldung ist hier nicht aufgeführt“), Konto 18
