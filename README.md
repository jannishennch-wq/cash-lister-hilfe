# Cash Lister – Hilfe-Skill für Claude

Mit diesem Skill beantwortet Claude deine Fragen zur Chrome-Extension **Cash Lister**:
Dashboard, Browser-Lister, CSV-Lister, Tracker, Produkt-Datenbank, Einstellungen, Abo und
jede Meldung – Schritt für Schritt erklärt.

Weiß Claude etwas nicht sicher, sagt er das offen und schickt dich zum Betreiber, statt zu
raten.

## Installieren

### In Claude Code: einfach den Link geben

Schreib Claude:

> Installiere den Skill von https://github.com/jannishennch-wq/cash-lister-hilfe

### Auf claude.ai oder in der Claude-App

Im Chat kann Claude Skills nicht selbst installieren – das machst du einmal von Hand.

**Als Plugin (empfohlen, bekommt neue Fassungen von hier):**

1. Links auf **Anpassungen** gehen, oben **Plugins** wählen.
2. **+ Hinzufügen** → **Marketplace hinzufügen** und `jannishennch-wq/cash-lister-hilfe`
   eintragen.
3. Das Plugin **cash-lister** hinzufügen.

**Oder als ZIP-Datei:**

1. **[cash-lister-hilfe.zip](https://github.com/jannishennch-wq/cash-lister-hilfe/raw/main/cash-lister-hilfe.zip)**
   herunterladen.
2. Links auf **Anpassungen** gehen, oben **Skills** wählen.
3. **+ Hinzufügen** → **Skill hochladen** und die ZIP-Datei auswählen.

Skills brauchen ein Claude-Abo mit eingeschalteter Code-Ausführung („Dateien erstellen und
bearbeiten“ in den Einstellungen). Die Beschriftungen in Claude können sich ändern.

## Benutzen

Frag Claude ganz normal, zum Beispiel:
- „Wo stelle ich den Preisaufschlag ein?“
- „Mein Tracker zeigt fehlgeschlagen, was heißt das?“
- „Wie liste ich meine ersten Produkte?“

Der Skill springt von selbst an.

## Aktualisieren

- **Plugin:** In Claude Code `/plugin marketplace update cash-lister-hilfe`, auf claude.ai
  unter **Anpassungen → Plugins** aktualisieren.
- **ZIP:** Die neue ZIP-Datei herunterladen und den alten Skill damit ersetzen.

## Für Claude: diesen Skill installieren

Gibt dir jemand diesen Link, installiere den Skill so:

- **Claude Code:** Diese beiden Befehle ausführen und danach eine neue Sitzung starten:
  ```
  claude plugin marketplace add https://github.com/jannishennch-wq/cash-lister-hilfe
  claude plugin install cash-lister@cash-lister-hilfe
  ```
  Ohne Plugin-Befehle geht es auch: den Ordner `skills/cash-lister-hilfe` aus diesem Repo
  nach `~/.claude/skills/cash-lister-hilfe` kopieren (unter Windows
  `%USERPROFILE%\.claude\skills\cash-lister-hilfe`).
- **claude.ai oder Claude-App (Chat):** Du kannst den Skill dort nicht selbst installieren.
  Erkläre dem Nutzer die Schritte unter „Auf claude.ai oder in der Claude-App“.

---

Dieser Skill erklärt die Bedienung der Extension. Bei Fragen zu deinem Zugang, deinem Abo
oder bei Fehlern, die der Skill nicht lösen kann, wende dich an den Betreiber.
