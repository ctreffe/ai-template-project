# AI Project Template

[![Status](https://img.shields.io/badge/status-stable-green)](VERSION)
[![Version](https://img.shields.io/github/v/tag/ctreffe/ai-template-project?label=version)](CHANGELOG.md)
[![License](https://img.shields.io/github/license/ctreffe/ai-template-project)](LICENSE)

> [!NOTE]
> **KI-Zusammenarbeit**
>
> Dieses Repository pflegt das generische AI Project Template.
>
> Das Template dokumentiert Praktiken für KI-gestützte Zusammenarbeit, Kontextübergaben, Decision Records und Repository-Konventionen für strukturierte Projektarbeit.
>
> Der Kollaborationsvertrag wird in [COLLABORATION.md](COLLABORATION.md) gepflegt.

<br>

**[Link to the English README](README.md)**

<br>

## Inhalt

- [Überblick](#überblick)
- [Kernprinzip](#kernprinzip)
- [AI Templateverse](#ai-templateverse)
- [Wann dieses Template geeignet ist](#wann-dieses-template-geeignet-ist)
- [Projektinitialisierung](#projektinitialisierung)
- [Skills für die Zusammenarbeit](#skills-für-die-zusammenarbeit)
- [Externe Dateien und Quellen](#externe-dateien-und-quellen)
- [Temporäre Arbeitsdateien](#temporäre-arbeitsdateien)
- [Projektmaterialien](#projektmaterialien)
- [Empfohlener Workflow](#empfohlener-workflow)
- [Git-Index und geschützte Git-Aktionen](#git-index-und-geschützte-git-aktionen)
- [Decision Records](#decision-records)
- [Repository-Struktur](#repository-struktur)
- [Template- und abgeleitete Projektdateien](#template--und-abgeleitete-projektdateien)
- [Verwendung dieses Templates](#verwendung-dieses-templates)
- [Tool-Setup für Maintainer](#tool-setup-für-maintainer)
- [Kontinuierliche Verbesserung](#kontinuierliche-verbesserung)
- [Lizenz](#lizenz)

## Überblick

Das AI Project Template ist ein generischer Ausgangspunkt für Projekte, die von strukturierter Zusammenarbeit, explizitem Kontext, dokumentierten Entscheidungen und zuverlässiger Übergabe zwischen Arbeitssitzungen profitieren. Es ist bewusst nicht auf Softwareentwicklung beschränkt: Es unterstützt Forschung, Planung, Konzeptarbeit, Prozessgestaltung, operative Projekte und gemischte Projekttypen.

Das Template stellt ein Repository-zentriertes Kollaborationsmodell, lokale Codex-Regeln, abgegrenzte Kollaborations-Skills, erhaltene Setup-Leitlinien, einen aktuellen Projektkontext, Dokumentations- und Repository-Standards, Leitlinien für Decision Records und optionale Arbeitsordner bereit. Es ist eine Projektmethode und Repository-Grundlage, kein domänenspezifisches Framework.

## Kernprinzip

Der Maintainer verantwortet Projektintention und -richtung. Der Assistant kann Informationen strukturieren, Lücken erkennen, Projektdateien und Ergebnisse vorbereiten, Konsistenz prüfen und Projektwissen bewahren, darf aber den gewünschten Endzustand nicht erfinden, folgenreiche Entscheidungen nicht stillschweigend treffen und Arbeit nicht als abgeschlossen ausgeben, wenn sie nicht existiert.

Das Repository ist das dauerhafte Projektgedächtnis. Künftige Maintainer, Mitwirkende oder Assistants sollen den aktuellen Zustand verstehen und die Arbeit fortsetzen können, ohne auf private Chatverläufe angewiesen zu sein.

## AI Templateverse

Die öffentlichen AI-Templates bilden ein kleines Templateverse: eine Familie verwandter Templates, die ein Repository-zentriertes, vom Maintainer geführtes Modell der Mensch-KI-Zusammenarbeit teilen und es für unterschiedliche Projekttypen spezialisieren.

- Das [AI Project Template](https://github.com/ctreffe/ai-template-project) ist der generische Ausgangspunkt für strukturierte Projektarbeit, Forschung, Planung, Konzeptarbeit, Prozessgestaltung und gemischte Projekte.
- Das [AI Dev Template](https://github.com/ctreffe/ai-template-dev) ist für entwicklungsorientierte Projekte gedacht, in denen Code, Skripte, Automatisierung, Validierung, Architektur oder Release-Workflows zentral sind.
- Das [AI Documentation Template](https://github.com/ctreffe/ai-template-docs) ist für technische Dokumentationsprojekte wie Benutzer- und Administrationshandbücher, Betriebsanweisungen, Tutorials, Migrationsleitfäden und Dokumentationswebsites gedacht.

## Wann dieses Template geeignet ist

Verwende das Project Template, wenn die Projektform noch offen ist oder mehrere Arbeitsarten ein gemeinsames Projektgedächtnis benötigen. Es eignet sich gut für Discovery, Planung, Forschung, Koordination, Prozessgestaltung und Projekte, die später stärker spezialisiert werden können.

Beginne mit einem spezialisierten Template, wenn die primäre Arbeit bereits feststeht:

- das Dev Template für Implementierung, Tests, Automatisierung und Releases;
- das Documentation Template für zielgruppenorientierte technische Dokumentation und Veröffentlichung;
Wenn ein generisches Projekt später entwicklungsorientiert wird, dokumentiere den Übergang und übernimm das Dev Template oder migriere bewusst dorthin.

## Projektinitialisierung

Nach dem Erzeugen des Repositorys ruft der Maintainer `$start-project` auf. Der
Skill liest das Repository, wendet `PROJECT_SETUP.md` an und führt die
vollständige Initialisierung. Der Maintainer muss die Setup-Dateien nicht
separat öffnen oder ausführen.

Die einfachste Anweisung an den Agenten lautet:

> `$start-project`

Es muss kein Initialisierungs-Prompt geöffnet oder in die Unterhaltung kopiert werden.
Vor dem normalen Frageblock bietet der Agent eine knappe Wahl zwischen dem
üblichen schlanken Weg und dem expliziten `$grill-me`-Weg für detaillierte
Planung an. Die Wahl des detaillierten Wegs erteilt keine Zugriffs- oder
Aktionsbefugnis.

Der Agent:

1. liest die Kollaborations-, Setup-, Dokumentations-, Repository- und Entscheidungsregeln;
2. prüft die Repository-Baseline, ohne die Git-Historie zu verändern;
3. folgt dem gewählten Initialisierungsweg und stellt auf dem schlanken Weg
   höchstens sechs unbeantwortete Grundfragen zu Identität und Zweck, Zielgruppe
   und Nutzung, erstem nützlichem Ergebnis und dessen Nachweis, aktuellem
   Umfang und Nicht-Zielen, Quellen- oder Materialzugriff und Sensitivität sowie
   nur den Bedingungen, die vor Arbeitsbeginn feststehen müssen;
4. fragt jede folgenreiche Entscheidung ab, statt Projektrichtung zu erfinden,
   und lässt nicht wesentliche Entscheidungen ausdrücklich offen;
5. passt nach den Antworten README-Dateien, Projektkontext, Arbeitsordner und laufende Projektregeln an;
6. dokumentiert Template-Baseline und Initialisierungsprovenienz in [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md);
7. wendet sichere Standardwerte an und hält erforderliche Platzhalter und ungelöste Setup-Entscheidungen sichtbar; und
8. übergibt den initialisierten Repository-Zustand mit angemessenen Validierungsergebnissen, Einschränkungen und vorgeschlagenen Commit-Metadaten.

`PROJECT_SETUP.md` bleibt die detaillierte Initialisierungscheckliste des Agenten
und ein Provenienznachweis. `$start-project` ist der einzige ausführbare
Einstiegspunkt, der diese Checkliste aktiviert.

Soll ein Projekt lokal bleiben und keinen Remote erhalten, rufe in diesem
ausgecheckten Template ausdrücklich `$create-local-project` auf. Der Skill
prüft das Ziel, erzeugt einen unabhängigen lokalen Clone ohne Remote und ruft
anschließend `$start-project` auf; er ist keine zweite Initialisierung.
Nach erfolgreicher Initialisierung wird die geerbte Template-Historie in
`CHANGELOG.md` und `TASK_HANDOFF.md` durch projektspezifischen Zustand ersetzt.
Das reine Template-`IDEAS.md`, die Projektkopie von `$create-local-project` und
ihre Verweise werden entfernt, sofern der Maintainer nicht bewusst einen
projekteigenen Ideenbestand einrichtet. Die Initialisierungsdateien bleiben als
Provenienz erhalten.

Bei der Initialisierung werden die geerbten `README.md` und `README.de.md`
zu `TEMPLATE_README.md` und `TEMPLATE_README.de.md`. Sie bleiben als angepasste
Anleitungen für Workflows, Skills und Repository-Konventionen erhalten. Neue
Projekt-READMEs in beiden Sprachen stellen das konkrete Projekt vor und verlinken
früh unter "Workflows und Skills" auf die zugehörige Anleitung. Jedes Paar hat
eigene Sprachlinks; die Anleitungen verlinken zurück zur Projektbeschreibung.

Die Anleitungen beschreiben die verbleibenden Dateien und Skills, enthalten
keine geerbten Badges und unterscheiden Template-Provenienz von Projektidentität
und Lizenzierung. Spätere ausgewählte `$sync-template`-Aktualisierungen bilden
die Quell-READMEs auf diese Anleitungen ab und bewahren Projektanpassungen sowie
Projektbeschreibungen. Bestehende Projekte übernehmen diese Struktur nur durch
bewusste Pflege. Dieses Quell-Repository behält sein ursprüngliches README-Paar.
[PROJECT_SETUP.md](PROJECT_SETUP.md) beschreibt die Initialisierung und die
Fortsetzung nach unterbrochenem Setup.

## Skills für die Zusammenarbeit

Skills sind abgegrenzte Arbeitsabläufe in [`.agents/skills/`](.agents/skills/).
Sie führen den Agenten durch eine bestimmte Aufgabe und laden dafür die
passenden Repository-Leitlinien. Rufe einen Skill im Chat mit `$skill-name`
auf, zum Beispiel `$review-project`. Die verlinkten Skill-Dateien beschreiben
den vollständigen Ablauf.

- **Agent oder explizit:** Der Agent darf den Skill bei einer passenden
  Aufgabe selbst auswählen; du kannst ihn auch direkt aufrufen.
- **Explizit:** Der Skill braucht einen bewussten Aufruf oder eine
  ausdrückliche Auswahl durch den Maintainer. Ein Vorschlag des Agenten
  aktiviert ihn noch nicht.

Die Auswahl eines Skills erteilt keine zusätzliche Freigabe für geschützte
Git-Aktionen, Installation, externe Übertragung oder Veröffentlichung. Die
lokalen Zugriffs- und Fachregeln gelten für jeden Ablauf.

In `commit-changes` und `commit-milestone` umfasst eine explizite
Commit-Freigabe für dieses Repository standardmäßig den normalen Push zu
seinem verifizierten bestehenden Upstream. Mit „nur Commit“ oder „kein Push“
schließt du den Push aus. Andere Git-Aktionen, Tags und Release-Publikation
brauchen weiterhin eine eigene Freigabe.

`reuse-fixes` liest und ergänzt ausschließlich das Fehlerwissen dieses
Repositorys. Der Skill sammelt keine Erfahrungen über Repositories hinweg
und führt kein globales Fehlergedächtnis.
Aktive Lösungen stehen mit 4–8 Zeilen pro Fall in `TROUBLESHOOTING.md`.
[Ausführliche Belege](TROUBLESHOOTING_DETAILS.md) bleiben getrennt erhalten;
lies bei Bedarf nur den passenden Detailabschnitt.

| Skill | Aufruf | Zweck |
| --- | --- | --- |
| [`start-task`](.agents/skills/start-task/SKILL.md) | Agent oder explizit | Rekonstruiert nur den Kontext für eine neue abgegrenzte Aufgabe. |
| [`handoff-task`](.agents/skills/handoff-task/SKILL.md) | Agent oder explizit | Sichert Ergebnis, Evidenz und nächsten Schritt kompakt in `TASK_HANDOFF.md`. |
| [`commit-changes`](.agents/skills/commit-changes/SKILL.md) | Agent oder explizit | Erstellt einen regulären abgegrenzten Commit und führt den normalen Upstream-Push mit expliziter Commit-Freigabe aus, sofern der Push nicht ausgeschlossen wurde. |
| [`record-decision`](.agents/skills/record-decision/SKILL.md) | Agent oder explizit | Dokumentiert eine dauerhafte Entscheidung im passenden Record-Typ; Entscheidungen des Quelltemplates werden an Governance geroutet. |
| [`reuse-fixes`](.agents/skills/reuse-fixes/SKILL.md) | Agent oder explizit | Verwendet bestätigte Lösungen dieses Repositorys wieder, hält knappe Vorbeugung fest und fragt nur bei fehlender Freigabe oder blockierenden Entscheidungen nach. |
| [`start-project`](.agents/skills/start-project/SKILL.md) | Explizit | Initialisiert ein neues, noch nicht eingerichtetes abgeleitetes Projekt anhand der erhaltenen Setup-Leitlinien. |
| [`review-project`](.agents/skills/review-project/SKILL.md) | Explizit | Erstellt eine umfassende neutrale Bestandsaufnahme des Projektzustands und der Evidenzlücken. |
| [`sync-template`](.agents/skills/sync-template/SKILL.md) | Explizit | Vergleicht ein abgeleitetes Projekt mit seinem verifizierten Quelltemplate und übernimmt ausgewählte Änderungen unter Erhalt der Projektanpassungen. |
| [`check-consistency`](.agents/skills/check-consistency/SKILL.md) | Explizit | Diagnostiziert interne Widersprüche zwischen Intention, Roadmap, Entscheidungen, Inhalten und Dokumentation und entwickelt abgegrenzte Optionen. |
| [`perform-retrospective`](.agents/skills/perform-retrospective/SKILL.md) | Explizit | Wertet Zusammenarbeitsevidenz aus und trennt Projektbefunde von wiederverwendbaren Template- oder Familienkandidaten. |
| [`create-local-project`](.agents/skills/create-local-project/SKILL.md) | Explizit | Erzeugt ein lokales abgeleitetes Repository aus diesem Quelltemplate und übergibt es an die Initialisierung; wird nach erfolgreichem Projektsetup entfernt. |
| [`commit-milestone`](.agents/skills/commit-milestone/SKILL.md) | Explizit | Schließt einen geprüften Milestone mit Metadaten, umfassenden anwendbaren Prüfungen, Commit und normalem Upstream-Push ab, sofern der Push nicht ausgeschlossen wurde. |

### Optionale Planungsskills

`grill-me` und `grilling` sind übernommene MIT-lizenzierte Skills von Matt
Pocock. Sie ergänzen die eigenen Repository-Skills und werden ausschließlich
nach ausdrücklicher Auswahl verwendet. Der normale schlanke
Initialisierungsweg bleibt verfügbar.

| Skill | Aufruf | Zweck |
| --- | --- | --- |
| [`grill-me`](.agents/skills/grill-me/SKILL.md) | Explizit | Startet das optionale intensive Planungsinterview und leitet an `grilling` weiter. |
| [`grilling`](.agents/skills/grilling/SKILL.md) | Explizit | Prüft einen Plan, eine Entscheidung oder Idee in ausführlichen Interviewrunden; nur nach ausdrücklicher Auswahl. |

## Externe Dateien und Quellen

Verwende `input/` für Dateien, die der Maintainer bereitstellt oder die aus
externen Quellen stammen. Neue oder noch unklare Dateien beginnen unter
`input/intake/`; bereits eindeutig klassifizierte Dateien können direkt nach
`restricted/`, `local/` oder `versioned/` gelegt werden.

- **`input/intake/`** enthält Dateien, deren Zugriffs-, Git- und
  Weitergaberegeln noch nicht entschieden sind. Assistants dürfen sie
  standardmäßig weder auflisten noch lesen.
- **`input/restricted/`** enthält ignorierte lokale Dateien unter
  Maintainer-kontrolliertem Zugriff.
- **`input/local/`** enthält ignorierte lokale Dateien, die im dokumentierten
  Umfang für Assistant-Zugriff, aber nicht für Git freigegeben sind.
- **`input/versioned/`** enthält externe Dateien, die bewusst für Git und
  Assistant-Zugriff freigegeben wurden.

Dokumentiere unbedenkliche Metadaten, Provenienz und Handhabungsentscheidungen
in `input/CATALOG.md`. Verwende das ignorierte `input/CATALOG.local.md`,
wenn Dateinamen, Pfade oder Quellenangaben selbst sensibel sind. Externe Quellen,
die außerhalb des Repositorys verbleiben, gehören ohne Kopie ihrer Inhalte in
den Katalog. Nutze stabile öffentliche URLs direkt und löse logische private
oder gerätespezifische Orte über die ignorierte `input/PATHS.local.md` auf.

Assistant-Zugriff, Git-Versionierung und Veröffentlichung oder externe
Weitergabe bleiben getrennte Maintainer-Entscheidungen. Das Verschieben einer
Datei autorisiert weder Lesen noch Staging, Commit, Push oder Weitergabe. Eine
klassifizierte Datei kann später in einen spezifischeren Projektordner wechseln,
wenn sie zu gepflegtem Projektinhalt wird.

Für große, nicht in Git versionierte Dateien, die auf mehreren Rechnern
verfügbar bleiben müssen, gilt der anbieterneutrale Workflow in
[SYNCHRONIZED_STORAGE.md](SYNCHRONIZED_STORAGE.md). Synchronisierte Dateien
bleiben externer Speicher; Synchronisierung ist weder Git-Versionierung,
Backup, Assistant-Zugriff noch Publikationsfreigabe.

## Temporäre Arbeitsdateien

Verwende `temp/` für wegwerfbare Zwischendateien. Alle Inhalte außerhalb von
`temp/restricted/` sind für den Assistant lesbar; dieses Restricted-Verzeichnis
darf weder aufgelistet noch gelesen werden. Sämtliche temporären Inhalte werden ignoriert
und dürfen niemals versioniert werden. Sie werden nicht katalogisiert. Überführe
alles dauerhaft Benötigte nach `materials/` und katalogisiere es dort.

## Projektmaterialien

Dateien in `input/` bleiben inhaltlich unverändert: Sie sind ursprüngliche
externe Dateien und feste Quellenverweise. Jede inhaltliche Änderung – etwa
Konvertierung, OCR, Schwärzung, Zuschnitt, Annotation, Normalisierung oder
Zusammenführung – erzeugt eine neue Datei im Projektmaterial-Workflow, statt
den Input zu verändern.

`materials/` enthält dauerhafte Arbeitsdateien, die im Projekt erzeugt oder aus
Input abgeleitet wurden. Jedes registrierte Material ist für den Assistant
freigegeben; Git-Versionierung und externe Weitergabe bleiben getrennte
Entscheidungen. Erfasse jede Datei in `materials/CATALOG.md` mit Zweck,
Erstellung oder Transformation, Speicherzustand und Provenienz über `Based on`
mit Input- oder Material-IDs.

- **`local`** liegt in dem ignorierten Ordner `materials/local/`.
- **`versioned`** liegt in `materials/versioned/` und darf versioniert werden.
- **`external`** bleibt außerhalb des Repositorys an einem stabilen logischen
  Ort im Katalog. Löse ihn je Rechner in der ignorierten
  `materials/PATHS.local.md` auf, ausgehend von der versionierten Beispieldatei.

Verwende `materials/` nicht für Caches, wegwerfbare temporäre Dateien oder
finale Ergebnisse; Outputs bleiben in `output/`. Hinterlege keine Zugangsdaten,
privaten Freigabe-Tokens oder gerätespezifischen absoluten Pfade in
versionierten Dateien.

Nicht die Erzeugungsweise, sondern die aktuelle Projektrolle bestimmt den
Ablageort. Bewahre eine erzeugte Datei in `materials/` auf, wenn sie als
dauerhafte Arbeits- oder Quelldatei in weitere Projektschritte eingeht. Lege sie
in `output/` ab, wenn sie als Projektergebnis zur Nutzung, Prüfung, Übergabe,
Veröffentlichung oder Auslieferung bestimmt ist. Wegwerfbare
Erzeugungszwischenstände bleiben in `temp/`; domänenspezifische maßgebliche
Dateien behalten ihre gepflegten Orte.

## Empfohlener Workflow

Projekte entwickeln sich von der Maintainer-Intention aus in kleinen, prüfbaren Projektschleifen:

```text
Intention -> Roadmap -> Erzeugen -> Prüfen -> Abgleichen -> Festhalten -> Fortsetzen
```

1. Ermittle oder bestätige die Repository-Baseline.
2. Prüfe Maintainer-Intention, gewünschten Endzustand und aktuelle Roadmap.
3. Wähle den kleinsten sinnvollen Schritt, der Unsicherheit reduziert oder ein prüfbares Ergebnis erzeugt.
4. Erzeuge oder überarbeite die relevante Projektdatei, das Ergebnis oder andere Projektinhalte.
5. Prüfe oder validiere das Ergebnis und mache Einschränkungen sichtbar.
6. Aktualisiere betroffenen Kontext, Dokumentation und Decision Records.
7. Bereite einen regulären Arbeits-Commit mit passendem Conventional-Commit-Präfix vor.
8. Fahre fort, bis das Milestone-Ziel erreicht ist.
9. Schließe den Milestone separat ab, indem aktueller Zustand, Versionierung und Historie abgeglichen werden.

Reguläre neue Aufgaben verwenden den schlanken Skill `start-task`. Rufe
`$review-project` für eine umfassende neutrale Bestandsaufnahme,
`$sync-template` für Quelltemplate-Aktualisierungen, `$check-consistency` für
interne Diagnose und `$perform-retrospective` für eine Zusammenarbeitsschau auf.

## Git-Index und geschützte Git-Aktionen

Der Maintainer kontrolliert die Git-Historie. Assistants dürfen Status, Diffs und Logs prüfen sowie Working-Tree-Änderungen und Commit-Metadaten vorbereiten.

Staging und Unstaging sind Indexoperationen. Sie benötigen kein Kontrollwort, dürfen aber nur nach einer konkreten Maintainer-Anweisung oder Autorisierung des zugehörigen Commits erfolgen. Bestehende Staging-Auswahlen und nicht zusammenhängende Änderungen müssen erhalten bleiben.

Geschützte Aktionen umfassen Commits, Amendments, Tags, Pushes, Pulls, Merges, Rebases, Resets, Branch-Wechsel, Stash-Manipulationen und andere Operationen an der Git-Historie. Ein Assistant darf eine bestimmte geschützte Aktion nur ausführen, wenn die Anweisung für genau diese Aktion `explicit` oder `explicitly` auf Englisch oder die deutsche Wortfamilie `explizit` enthält. Die Freigabe von Dateiänderungen autorisiert keine Änderung der Git-Historie; andere geschützte Aktionen brauchen weiterhin eine eigene Freigabe, mit dem oben beschriebenen Commit-und-Push-Ablauf als gezielter Ausnahme.

Wenn diese Regel eine Autorisierung verlangt, schlägt der Assistant eine
minimal abgegrenzte, kopierfertige Anweisung vor, die genaue Aktion,
Repository und wesentliche Konsequenz benennt. Der Vorschlag selbst ist keine
Autorisierung.

Reguläre Arbeits-Commits verwenden Conventional-Commit-Präfixe wie `feat:`, `fix:`, `docs:` oder `chore:`. Milestone-Commits verzichten auf das Präfix, verwenden eine lesbare Zusammenfassung mit abgeschlossener Version und schließen bereits geprüfte Arbeit ab.

## Decision Records

Decision Records bewahren, warum folgenreiche Entscheidungen getroffen wurden. Wähle das Präfix nach dem Entscheidungsgegenstand, nicht nur nach dem Repository-Typ:

- **PDR — Project Decision Record:** Projektrichtung, Umfang, Roadmap, Zusammenarbeit, Governance, Datenschutzgrenzen, Review-Modelle oder Repository-Beziehungen.
- **ADR — Architecture Decision Record:** technische Architektur, Tooling, Formate, Automatisierung oder eine andere dauerhafte technische Struktur in einem abgeleiteten Projekt.
- **DDR — Documentation Decision Record:** Dokumentationsstruktur, Terminologie, zielgruppenorientiertes Material, Veröffentlichungsregeln oder Dokumentations-QA.

Das generische Template verwendet standardmäßig PDRs und erklärt das Modell in [DECISIONS.md](DECISIONS.md). Verwende [decisions/](decisions/) nur für Entscheidungen, deren Begründung für zukünftige Mitwirkende relevant bleibt; kleine Routineentscheidungen benötigen keinen Record.

## Repository-Struktur

### Einstiegspunkte und Projektgedächtnis

- **`README.md` und `README.de.md`** führen auf Englisch und Deutsch in das Projekt ein, erklären den Einstieg und verlinken die vertiefenden Regeln.
- **`PROJECT_CONTEXT.md`** ist der primäre Wiedereinstiegspunkt. Die Datei hält aktuelle Intention, Status, Roadmap, Baseline, Validierungsstand, offene Entscheidungen und den nächsten sinnvollen Schritt fest, statt die vollständige Projekthistorie zu duplizieren.
- **`CHANGELOG.md` und `VERSION`** beschreiben abgeschlossene Zustände und die Versionshistorie. Sie werden aktualisiert, wenn ein versionierter Milestone abgeschlossen ist, nicht bereits bei Arbeitsbeginn.

### Zusammenarbeit und Betriebsregeln

- **`AGENTS.md`** ist der kompakte, automatisch residente Sicherheitskern und Kontext-Router für KI-Agenten.
- **`COLLABORATION.md`** definiert den anbieterneutralen Kollaborationsvertrag, Autoritätsgrenzen, das Evidenzmodell und Erfolgskriterien. Die Datei wird nur geladen, wenn ihr breiterer Kontext relevant ist.
- **`TROUBLESHOOTING.md`** hält bestätigte Korrekturen und knappe Vorbeugung
  für `reuse-fixes` in diesem Repository fest. Hostfakten bleiben ignoriert in
  `TROUBLESHOOTING.local.md`. Andere Repositories werden nicht einbezogen.
- **`PHILOSOPHY.md`** hält die Werte hinter der Projektmethode fest, darunter Intention vor Struktur, Nachvollziehbarkeit, leichtgewichtiger Prozess und Integrität vor Außendarstellung.

### Setup, Fortsetzung und Review

- **`PROJECT_SETUP.md`** leitet die erste Initialisierung an und bewahrt ihre methodische Provenienz. `$start-project` ist der explizite ausführbare Einstiegspunkt.
- **`.agents/skills/`** enthält die im Abschnitt
  [Skills für die Zusammenarbeit](#skills-für-die-zusammenarbeit) beschriebenen
  Arbeitsabläufe und ihre Aufrufregeln.
- **`TASK_HANDOFF.md`** ist der kompakte versionierte Checkpoint für eine
  abgeschlossene, pausierte oder blockierte Aufgabe und unterstützt den
  Wechsel auf einen anderen Rechner.
- **`IDEAS.md`** ist ein Source-Template-Backlog für wiederverwendbare
  Kandidaten. Normale abgeleitete Projekte entfernen ihn bei erfolgreicher
  Initialisierung, sofern sie nicht bewusst einen eigenen Ideenbestand führen.

### Repository-Leitlinien und Entscheidungen

- **`DOCUMENTATION.md`** definiert Dokumentrollen, die Trennung von aktuellem Zustand und Historie sowie Qualitätsanforderungen. Die Datei bleibt nach der Initialisierung eine laufende Projektregel.
- **`REPOSITORY.md`** definiert Repository-Organisation, Git-Konventionen, Quellen- und Output-Behandlung, Versionierung und repository-fertige Übergaben. Abgeleitete Projekte passen die Datei an ihren tatsächlichen Workflow an, statt sie als vorübergehendes Setup-Material zu behandeln.
- **`DECISIONS.md` und `decisions/`** erklären Decision Records und speichern dauerhafte Entscheidungsbegründungen. Das Template bietet wiederverwendbare PDR-Leitlinien und gegenstandsbezogene Record-Vorlagen.

### Externe Dateien und Projektoutputs

- **`input/`** wendet die gemeinsamen Klassifikationen Intake, Restricted,
  Local und Versioned auf externe Dateien und Quellen an. Die Kataloge bewahren
  unbedenkliche Provenienz- und Handhabungsentscheidungen.
- **`materials/`** katalogisiert dauerhafte, für den Assistant lesbare
  Arbeitsdateien und trennt lokale, versionierte und externe Speicherung von
  der Zugriffsfreigabe.
- **`temp/`** enthält ignorierte, niemals versionierte Zwischenstände;
  `temp/restricted/` bildet die nicht zugängliche Ausnahme.
- **`output/`** enthält Projekt-Deliverables oder erzeugte Ergebnisse. Projekte
  legen fest, ob Outputs versionierte Milestones, Review-Dateien oder
  reproduzierbare lokale Produkte sind, und prüfen sie vor der Weitergabe.

## Template- und abgeleitete Projektdateien

In einem abgeleiteten Projekt:

- fülle `PROJECT_CONTEXT.md` aus und pflege sie als aktuellen Projektzustand;
- passe beide README-Dateien, `DOCUMENTATION.md` und `REPOSITORY.md` an das konkrete Projekt an;
- behalte und passe `AGENTS.md`, `COLLABORATION.md` und `PHILOSOPHY.md` an, sofern kein dokumentierter Projektbedarf eine Änderung erfordert;
- behalte `PROJECT_SETUP.md` als Initialisierungsprovenienz;
- behalte die anwendbaren Repository-Skills für wiederholbare spätere Abläufe;
- passe Input- und Output-Ordner an den konkreten Workflow an und bewahre ihre
  dokumentierten Handhabungsregeln;
- ersetze Template-Decision-Records nur dann durch echte Records, wenn folgenreiche Entscheidungen vorliegen.

Halte Source-Template-Version und -Commit, Initialisierungsstatus, letzte Harmonisierungs-Baseline und beabsichtigte Abweichungen in `PROJECT_CONTEXT.md` fest. Ein abgeleitetes Projekt ist für seine eigene Intention und akzeptierten Entscheidungen maßgeblich; Template-Updates werden geprüft und angepasst statt blind kopiert.

## Verwendung dieses Templates

1. Erzeuge ein Repository aus dem Template und rufe `$start-project` auf.
2. Wähle den normalen schlanken Weg oder ausdrücklich `$grill-me`; beantworte
   auf dem schlanken Weg höchstens sechs unbeantwortete Grundfragen, während
   der Agent die übrigen Setup-Dateien automatisch anwendet.
3. Prüfe den initialisierten Repository-Zustand, die Validierungsergebnisse und den vorgeschlagenen ersten Commit.
4. Lasse den Agenten `PROJECT_CONTEXT.md` während der späteren Arbeit als kompakte Projektübergabe aktuell halten.
5. Arbeite in kleinen Dateien, Ergebnissen oder Änderungen, die aus der vom Maintainer definierten Intention, Grenzen und Erfolgskriterien abgeleitet sind.
6. Unterscheide Rohinputs, geprüfte Derivate und erzeugte Outputs, bevor Zugriff, Versionierung oder Veröffentlichung freigegeben werden.
7. Dokumentiere folgenreiche Entscheidungen in `decisions/` und validiere Ergebnisse, bevor sie als abgeschlossen dargestellt werden.
8. Beginne eine abgegrenzte neue Aufgabe über `start-task`; rufe
   `$review-project` nur auf, wenn eine umfassende Bestandsaufnahme nötig ist.
9. Halte `$sync-template`, `$check-consistency` und `$perform-retrospective` als
   getrennte ausdrückliche Abläufe mit unterschiedlichen Ergebnissen.
10. Schließe Milestones mit kohärentem Kontext, Dokumentation, Changelog und Versionsmetadaten ab.

## Tool-Setup für Maintainer

Das generische Template hat keine verpflichtende domänenspezifische Toolchain. Eine praktische lokale Baseline ist:

- [Git](https://git-scm.com/downloads) und ein vom Maintainer kontrollierter Client wie [GitHub Desktop](https://desktop.github.com/download/);
- ein Text- oder Markdown-Editor wie [Visual Studio Code](https://code.visualstudio.com/download);
- [PowerShell](https://learn.microsoft.com/powershell/scripting/install/installing-powershell-on-windows) unter Windows oder eine gleichwertige lokale Shell;
- [ripgrep (`rg`)](https://github.com/BurntSushi/ripgrep/releases) oder ein anderes schnelles Suchwerkzeug;
- projektspezifische Werkzeuge, die nur installiert werden, wenn die konkrete Arbeit sie benötigt.

Bevorzuge projektlokale Umgebungen wie `.venv/` oder `node_modules/` gegenüber globalen Änderungen. Paketinstallationen, externe Dienste und Netzwerknutzung sollten einen klaren Projektzweck haben; private Repository-Materialien bleiben standardmäßig lokal.

## Kontinuierliche Verbesserung

Nutze `$sync-template`, um ein konkretes Projekt mit einer verifizierten Source-Template-Baseline zu vergleichen und ausgewählte Entwicklungen zu übernehmen. Verwende `$check-consistency` getrennt für interne Widersprüche und `$perform-retrospective` für Kollaborationspraktiken, Übergaben, Entscheidungsfindung und Arbeitsrhythmus. Gemischte Projekte können sowohl generische Verbesserungen als auch Hinweise darauf liefern, dass ein stärker spezialisiertes Template langfristig besser geeignet ist.

Behandle Beobachtungen aus einem abgeleiteten Projekt als Kandidaten und nicht als automatische Template-Regeln. Prüfe, ob sie wiederholt auftreten, außerhalb ihres ursprünglichen Kontexts nützlich bleiben und in das generische Template oder eine Domänenspezialisierung gehören. Abgeleitete Projekte und ihre Decision Records bleiben für projektspezifische Entscheidungen maßgeblich.

Der Maintainer koordiniert die templateübergreifende Weiterentwicklung in einem privaten Governance-Repository namens `ai-templateverse`. Es dokumentiert gemeinsame Konventionen, bewusste Spezialisierungen und Evidenz aus abgeleiteten Projekten. Das Repository wird bewusst nicht verlinkt, da Template-Nutzer:innen keinen Zugriff darauf benötigen.

Die Governance-Koordination erzeugt keine verborgenen Anforderungen. Jede Änderung, die dieses Template betrifft, muss hier durch gepflegte Leitlinien, gegebenenfalls Decision Records, den Changelog und die Release-Historie abgebildet werden. Template-Änderungen sollen betroffene Dokumente kohärent aktualisieren, statt isolierte Notizen anzuhängen.

## Lizenz

Dieses Projekt steht unter der [MIT-Lizenz](LICENSE).
