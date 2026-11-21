---
# Read by the hooks, the review, the evals. Schema: @lernapps/tooling/guidance/plan-front-matter.v1.schema.json
# Written by `lernapps plan` and the hooks. Never change a key or a value by hand.
# Archetype, null until chosen in Explore. Allowed values: explainer, interactive, quiz.
archetype: explainer
# Current phase. Allowed values: explore, plan, code, commit.
phase: code
# prePushFailures: failed pre-push runs, written by the hook.
prePushFailures: 0
# failedChecks: failed rules and runs, written by lernapps check and the hooks.
failedChecks: {}
---

# Plan: englisch-verbketten, first version

<!--
For you, the assistant. The process is in AGENTS.md; this plan holds the method.
- `npx --no -- lernapps plan next` prints the task to do now, `plan done` ticks it and prints the next one.
- You write only below Goal, Key decisions, Notes, Answers, Entry draft, Content method and Retrospective, in the
  creator's language. Delete the comment of a section once the section is filled.
- Work on the branch `work`, locally: push nothing before Commit.
-->

*Started 2026-11-21. Explore, Plan, Code, Commit.*

## Goal

Kinder der Stufe 5-6 lernen, dass ein Verb hinter einem anderen Verb seine Form nach der „Kupplung“ des ersten richtet (Verbkette: Lok, Kupplung, Wagen). Sie benutzen can, must, needn't, could, might, should und would like, um zu sagen, was jemand kann, muss, darf, sollte oder möchte.

## Key decisions

- Archetype: `explainer`: Kinder lesen Seiten, die erklären, mit Übungen auf jeder Seite; Hören und Sprechen mit KI-Stimme `bf_emma` sind möglich. Ein Spiel oder Timer wird nicht gebraucht.
- Strang: `englisch/grammatik`, Format 2 (laut Issue #480).
- Nur Kapitel 1 „Können, müssen, möchten“ (Stufe 5-6); Kapitel 2 und 3 (7-8) kommen später als Inkrement `increment/<NN>-<name>` (Auftrag der Orchestrator-Session).
- Keine Wiederholungsseite `recap` nötig: `can-must` und `would-like` haben kein `requires`, `modalverben-could-might-should` verlangt nur `can-must` (dieselbe App). (Karte vom 2026-11-21)
- `scope` in `src/app.yaml` und auf jeder Seite: ja, weil die Seiten `open-task` haben (der Tutor beurteilt freie Antworten nur nach dem Scope).
- Figuren und Ort aus den Konventionen: Sophie, Ellie, Peter, Amir, Mr Hill, Mrs Parker in Millbrook School, Zeichnungen aus `millbrook-klassenzimmer.svg` von hello-millbrook.

## Notes

- Quelle des Auftrags: Issue lernapps/apps#480 und Konventionen (Epic #489), Kopien in `lernapps/start` (`orchestrierung/`). Der Orchestrator antwortet als Ersteller.
- Strang `englisch/grammatik`; Karte `https://lernapps.net/apps/map/englisch.json` (gelesen 2026-11-21).
- Kapitel 1 „Können, müssen, möchten“, Stufe 5-6, Kompetenzen (Karte, nicht umformuliert):
  1. `can-must` (Schritt 1, öffnet 4): „Ich kann mit can, can’t, must, mustn’t und needn’t Fähigkeit, Erlaubnis, Pflicht und Verbot ausdrücken.“
  2. `would-like` (Schritt 1, öffnet 4): „Ich kann mit „I’d like …“ und „I’d like you to …“ höflich sagen, was ich möchte.“
  3. `modalverben-could-might-should` (Schritt 2, öffnet 0, requires `can-must`): „Ich kann mit could, may, might und should Möglichkeiten, Vermutungen und Ratschläge ausdrücken.“
- Didaktik: Verbkette. Erstes Verb = Lok, zweites = Wagen, dazwischen die Kupplung, die die Lok bestimmt: keine (can swim), to (would like to swim). Modalverben nehmen nie ein -s und nie to. Eine Skala ordnet die Modalverben von sicher bis vielleicht (must, can, should, could, might). Would like ist die erste Lok mit Kupplung to.
- Übungsmuster (Fremdsprachen-Referenz): Form wählen (`choice`), Lücken (`gap`), Satz bilden aus Cue (`write`), Wortstellung (`ordering`), Zuordnen/Skala sortieren, Hören und Schreiben (Diktat, `audio`), Anwenden mit `open-task`. Leicht nach schwer, je Seite mindestens vier Übungen.
- Typische Fehler (je eine eigene Rückmeldung): *He cans swim*; *She must to go*; *Can you to help me?*; *I want a drink* statt *I'd like a drink* (Höflichkeit); mustn't mit needn't verwechselt (deutsch „nicht müssen“ = needn't, „nicht dürfen“ = mustn't); *I'd like go*; *I'd like that you help* (statt I'd like you to help).
- Umfang: drin: die drei Bausteine, Aussage, Verneinung, Frage, Kurzantworten; draußen: Ersatzformen (have to, be able to), Passiv, Gerund (Kapitel 2 und 3), Zeitformen (#472). Wörter: Grundwortschatz Stufe A1/A2 (Seite `grundwortschatz` der Karte, noch zu öffnen).
- Hidden prerequisites: Personalpronomen (#471, hier als bekannt vorausgesetzt, Figuren kommen mit Namen), Verben im simple present (Wörter wie swim, help, play kommen mit Bedeutung auf der Seite).
- Quellen (geöffnet am 2026-11-21): die Karte `englisch.json` und die drei Baustein-Seiten (`.../englisch/c/can-must/`, `.../modalverben-could-might-should/`, `.../would-like/`; Quelle der Karte: KMK-Bildungsstandards 2004/2023, die Karte ist ein Entwurf, nicht von einer Lehrkraft geprüft), Issue #480, Konventionen #489, Muster hello-millbrook. Nicht geprüft: Wikipedia `English modal verbs` (HTTP 429, nicht erneut versucht) und die Seite `grundwortschatz` der Karte (HTTP 503/404): Wörter daher aus dem Alltag der Figuren, einfach und bekannt (A1), jedes mit Bedeutung auf der Seite eingeführt; Grammatikfakten (Modalverben ohne -s und ohne to, needn't = nicht müssen, mustn't = nicht dürfen, I'd = I would) sind Standardgrammatik ohne zitierte Sätze.
- Kompetenz für Kompetenz, wie die Kinder dorthin kommen und welcher Irrtum abgefangen wird:
  - `can-must`: Kinder sortieren Szenenkarten (Schild, Aussage) nach Fähigkeit, Erlaubnis, Pflicht, Verbot und leiten daraus die Kette Lok + Wagen ohne Kupplung ab; Rückmeldung fängt *cans*, *must to*, *don't must* (statt mustn't/needn't) und *can you to*.
  - `modalverben-could-might-should`: Kinder stellen die Modalverben auf einer Skala von sicher bis vielleicht (must, can, should, could, might) und wählen nach Szene; Rückmeldung fängt *should to*, *might* als Vergangenheit/Zeit verwechselt und „should = muss“.
  - `would-like`: Kinder vergleichen *I want* (direkt) mit *I'd like* (höflich) im Café/Kiosk und finden die Kupplung `to`; Rückmeldung fängt *I'd like go*, *I like to* (mag) gegen *I'd like to* (möchte) und *I'd like that you help* statt *I'd like you to help*.
- Reihenfolge der Seiten: 1 `can-must`, 2 `modalverben-could-might-should`, 3 `would-like` (Karte: Schritt 1, 2, 1; die Kupplung to kommt zuletzt, weil sie in Kapitel 2 weitergeführt wird). Vorschlag: mehr Seiten nur, wo es didaktisch besser wird.
- Kapitel 1 „Können, müssen, möchten“ besteht aus den Seiten 1 bis 3 oben. Prerequisites, die die App nicht übt: Seite 1 braucht Personalpronomen (I, you, he, she, we, they) und einige Alltagsverben; Seite 2 braucht `can-must` (steht davor); Seite 3 braucht Personalpronomen und das Verb *like*. Die Seiten erklären diese Wörter beim ersten Auftauchen.
- **Wörter gegen den Grundwortschatz geprüft (2026-11-21, Liste `https://lernapps.net/apps/map/englisch/grundwortschatz/`, 2423 Wörter):** Alle Übungswörter von Seite 1 stehen in A1 (swim, run, play, sing, help, speak, ask, wear, uniform, coat, here, question, football, must, can, need), nur *German* steht in A2. Die Kurzformen can't, mustn't und needn't sind keine eigenen Listenwörter (Formen von can, must, need). Die Wörter für Seite 2 (could, may, might, should, bike, weekend, …) und Seite 3 (would, like, tea, sandwich, biscuit, juice, drink, waiter, café) werden beim Bau der Seiten geprüft; *might* und *should* stehen in A2, *thirsty* und *menu* in A2. Der Plan ändert sich nicht.
- **Stand (Pause auf Wunsch des Orchestrators, 2026-11-21):** Plan bestätigt. Code-Aufgaben 1 bis 6 erledigt: App angelegt, Inhaltsführer, Musterseite `src/koennen-muessen/can-must.yaml` mit Szene, Verbkette ohne Kupplung (SVG), Poster-Tabelle und sieben Übungen, sechs Audiodateien (bf_emma, mit `regen_audio.py`, noch von keinem Menschen angehört); `lernapps check` ohne Funde. Der Lerner-Check der Musterseite ist gelaufen (Funde unten, noch nicht behoben). Behoben bisher: Verbkette-SVG zeigte eine dunkle Verbindung, die wie eine Kupplung aussah (jetzt ohne). Offen: Fund-Auswertung des Lerner-Checks, Checkpoint „Musterseite“, dann Push von `work`, die Seiten 2 und 3, Kapitel mit Selbsteinschätzung. Nichts gepusht. Wiederaufnahme nach „weiter“ vom Orchestrator.
- **Lerner-Check `can-must` (Sub-Agent, Kind 5-6), Funde noch nicht behoben (Pause):**
  1. Szene: Schilder nicht übersetzt, wirken wie Sprechblasen; Wörter uniform, run, here, wear, mustn't, „Verb“ vor Gebrauch unerklärt; erste Übung (I can swim) hat mit dem Bild nichts zu tun, Rückmeldung „Muss heißt must, nicht can“ verrät can = kann.
  2. Verbkette: nicht erklärt, dass es ein Zug ist; Farben unerklärt; Kupplung nie gezeigt (kein Fall mit Kupplung), „kein to und kein -s“ sind zwei Dinge.
  3. Verrat vor „Prüfen“: Poster-Tabelle direkt über dem Matching mit gleichen Sätzen; Merke nennt drei der vier Lückenantworten; „Can“ als einzig groß geschriebene Option; „Vorsicht“-Kasten beantwortet die Mantel-Aufgabe.
  4. Aufgaben ohne Einführung: can't für Unfähigkeit (Lücke 4, Tabelle sagt nur „nicht erlaubt“); Ellie, Mr Hill, speak, German, ask, help; „Du darfst hier nicht rennen“ hat zwei richtige Sätze (can't, mustn't) ohne Unterschied; „Grundform“, „do“, „Modalverben“, „Verneinung“, „Fähigkeit/Erlaubnis/Pflicht“ zu schwer oder unerklärt.
  5. Rückmeldung: Lückenaufgabe und Matching ohne Hinweis bei falscher Antwort; Standardmeldung „Deine Fassung kann trotzdem richtig sein“ (Vorlagenproblem, an lernapps/app-templates melden); „Achte auf die Satzzeichen: swim.“ kryptisch; Diktat „You must not run here“ wird ohne Grund abgelehnt (`mustn't`-Variante mit `(mustn't|must not)` zulassen).
  6. Doppelt: Titel erscheint zweimal; die Regel „kein to, kein -s“ steht viermal. Ein Bild ohne Gedankenarbeit: Matching und Lücken sind Abschreiben.
  7. Technik: Audio-Player zeigt „0:00 / 0:00“ bis zum Laden (Vorlage); „KI“-Kennzeichen unerklärt (Vorlage). Kein englischer Sprachfehler gefunden. Beide Breiten ohne Seitwärts-Scroll.
 mit Stimme `bf_emma` (Skill `lernapps-audio`), nur ganze Sätze; Sprechen wird nicht beurteilt.
- Was die App nicht kann: keine Sprachbeurteilung, nur gelistete Antworten gelten (alle richtigen Varianten mit `(a|b)`), kein Timer und kein Spiel.
- Keine `recap`-Seite in dieser Version: keine Voraussetzung außerhalb der App im Kapitel (`personalpronomen` aus #471 und simple present stehen nicht in `requires`; vorausgesetzt, siehe Hidden prerequisites).
- Datenbereich: alle Modalverben der Kompetenzen (can, can't, must, mustn't, needn't, could, may, might, should, would like); `shall`, `ought to` und `have to` bleiben draußen (Kapitel 2 beziehungsweise außerhalb der Karte).

## Explore

<!--
- Find out what the app teaches, for whom, how much and how it looks. Ask; write no code, run no `create`.
- An answer counts only in the creator's words under "Answers". At most 2 questions per message, one topic each.
-->

### Tasks

- [x] Check the start: the folder `.agents/skills/lernapps-app` exists (else stop and tell the creator that the folder
      was not started with `init`), and `git branch --show-current` prints `work` (else `git switch -c work`).
- [x] Load skill `lernapps-app`. Tell the creator in two sentences what a lernapps app is and where it will live: at
      their own address, free and public, and once listed as a copy on lernapps.net. Say that the technical part
      (GitHub) comes at the end and that you do it.
- [x] Interview: ask the topics "Goal" and "Learners" of "Answers".
- [x] Load skill `lernapps-map-assignment` and read the learning map of the subject as it says. The creator brings
      the content themselves (material, a word list, the pages): note under "Notes" which competencies of the map it
      covers. Else write the skill's assignment, with its story; the creator's yes answers the topics Content and
      Amount. A subject without a map: skip this task and say so.
- [x] Load skill `lernapps-exercise-patterns` and read its reference for the subject. Note under "Notes" how learners
      will practise what the goal names.
- [x] Choose the archetype as skill `lernapps-app` says: read the README of each archetype in question, then tell the
      creator in plain words what the chosen one can and cannot do. Write the archetype and its reason under "Key
      decisions".
- [x] Run `npx --no -- lernapps skills --archetype <name>` with the chosen archetype. It installs the archetype's
      skills and adds the archetype's tasks to this plan.
- [x] Load skill `lernapps-explainer-design`. An explainer has the look of the runtime: write "fixed by the
      archetype" under the topic "Look and feel" of "Answers".
- [x] Interview: ask every other topic of "Answers", in order. Leave out only a topic that an answer of the creator
      already covers, and note which answer. A topic nobody answered is asked once before you write an assumption
      with "(guess)".
- [x] Load skill `lernapps-content-research` and research as it says. Write under "Notes": the strand or subject, the
      competencies by chapter with their ids, the sources you opened.
- [x] Write under "Notes" which competency goes on which page and which pages form a chapter, as "Map the content" of
      skill `lernapps-explainer-design` says. Per page, name the prerequisites the app does not practise.
- [x] Write under "Notes", one line per competency: how learners get there (they derive it, they do not only read it
      off), and which misconception the feedback catches.
- [x] Write under "Notes" the scope: what is in, what is out and why, the data range (for example "all main-group
      elements", never a silent "1–20"), the languages.
- [x] **Checkpoint:** research. Show in plain words: the strand or why none, the competencies by chapter, the didactic
      approach, the scope, every "(guess)", the sources and what is unchecked, the archetype and its reason. Stop and
      wait. Changes: change them, then ask again.
      Creator: Ja, passt. Reihenfolge can-must, modalverben-could-might-should, would-like. needn't üben. Ungeprüfte Quellen im Inhaltsführer als ungeprüft. Fehlerliste und Suchwörter als (guess) ok. Weiter in Plan.

### Answers

<!-- The interview: per topic the creator's answer, in their words. Keep the topics. -->

- Goal: (aus dem Issue #480, Leitidee) „Ich weiß, in welcher Form ein Verb hinter einem anderen Verb steht, und kann so Fähigkeiten, Pflichten, Wünsche, Vorlieben und das Passiv ausdrücken.“ Kapitel 1: „Ich kann mit can, must, needn't, could, might und should sagen, was jemand kann, muss, darf oder sollte, und mit would like höflich Wünsche äußern.“
- Learners: (aus dem Issue und den Konventionen) Englisch, Stufe 5-6, Kinder von 11 bis 12, erstes Schuljahr in Millbrook; Vorwissen aus dem Explainer #470 (Hello, Millbrook!) und Personalpronomen.
- Model and focus: Vorbild ist `lernapps/hello-millbrook` (Konventionen, Abschnitt Referenz); Schwerpunkt Übungen mit eigener Rückmeldung je typischem Fehler und eine Verbkette als Bild (Lok, Kupplung, Wagen). (aus den Konventionen)
- Hurdles: (guess, aus der Grammatik) -s und to an Modalverben (*He cans*, *must to*), needn't gegen mustn't, would like gegen want, *I'd like that you…*. Das Issue nennt: „Modalverben nehmen nie ein -s und nie to“.
- Content: ich schreibe die Seiten selbst nach dem Auftrag und der Karte; eigenes Material des Erstellers gibt es nicht; Fakten aus geöffneten Quellen, keine Sätze.
- Amount: erste Version nur Kapitel 1 (drei Bausteine, je eine Seite, wenn möglich zwei bis drei Seiten mit Verbkette); Kapitel 2 und 3 (Stufe 7-8) später als Inkrement.
- Languages: Deutsch (Erklärtexte) und britisches Englisch (Beispiele); eine Seitenstruktur, wie bei hello-millbrook. (aus den Konventionen)
- Look and feel: fixed by the archetype (Aussehen der Laufzeit, ruhig wie ein Arbeitsblatt, Dunkelmodus folgt dem Gerät). Gezeichnete Kinder, eine Szene je Seite.
- Terms: Verbkette, Lok (erstes Verb), Kupplung (keine, to, -ing, 3. Form), Wagen (zweites Verb); „Ausdruck“ statt „Wendung“; Tabellen „Klassenzimmer-Poster · …“ und „Schulkalender · …“; Fachbegriffe noun, verb, adjective, sentence, tense. (aus Issue und Konventionen)
- Finding the app: Suchwörter: can must could might should would like, Modalverben Englisch Klasse 5 6, höfliche Wünsche Englisch, Verbkette. (guess)

## Plan

<!--
- Map the confirmed content onto the archetype. No new content questions: a gap in the content goes back to Explore.
- The creator confirms the plan in one read. After the yes you work on your own.
-->

### Tasks

- [x] Map the content as "Map the content" of skill `lernapps-explainer-design` says, and write the result under
      "Content method".
- [x] Choose a pattern per competency as skill `lernapps-exercise-patterns` says, and add it to "Content method".
- [x] Add to "Content method" one line per page, as "Engagement" of skill `lernapps-explainer-design` says: the
      opening task, the change of activity, the reward, the story.
- [x] Add the tasks of Code, each one a piece of work that ends in a commit. First the pattern: one complete page or
      screen, `npx --no -- lernapps plan add --at pattern "<task>"`. Then the others, one call each:
      `npx --no -- lernapps plan add --at pages "<task>"`. Each task says what it builds and what it shows.
- [x] Draw a sketch of each screen, component or interactive exercise: a static SVG or image, or the steps with what
      learners see after each. Keep the files in `.vibe/sketches/`.
- [x] Show the creator, short: goal, competencies by chapter, the Code tasks, the sketches, and the content method in
      plain words (what learners see and do, what the app cannot do). At most 2 questions.
- [x] **Checkpoint:** confirm the plan and the content method. Stop and wait for an explicit yes. Changes: change
      them, then ask again.
      Creator: Ja, bestätigt. Musterseite can-must bauen, danach Checkpoint Musterseite. Selbsteinschätzung in die erste Version, je Seite zwei Übungen. Poster nicht direkt über der Übung. Work nach dem Lerner-Check pushen. Audio mit regen_audio.py, keine einsilbigen Namen am Satzende. Im Plan unter Notes aufschreiben, was geprüft und behoben wurde.

### Content method

<!-- One line each: the patterns and where; the figures and how they are made; the data files; each component, what it
checks and what it cannot; how a later agent adds a chapter. It becomes the content guide in Code. -->
<!-- An explainer: per figure, model and component its learning action in two to four sentences
(`explainer-representation-explained`); per page its prerequisites the app does not practise, and which get a recap
page, which a link. -->

- **App:** `format: 2`, `strand: englisch/grammatik`, `languages: [de]`, ein Kapitel `koennen-muessen` mit den Seiten `can-must`, `modalverben-could-might-should`, `would-like` (Dateien `src/koennen-muessen/<seite>.yaml`); Muster ist hello-millbrook. Wörter: keine Wortliste als Quelle (Grundwortschatz-Seite nicht erreichbar); A1-Wörter aus dem Alltag der Figuren, jedes mit Bedeutung vor der ersten Übung.
- **Abschnitte** (gleiche IDs auf jeder Seite wie in hello-millbrook): `einstieg` (Szene, erste leichte Aufgabe, „Das kannst du danach“), `neu` (Verbkette, Merke-Kasten, Poster-Tabelle), `uebung` (mindestens vier Übungen, leicht nach schwer), `anwenden` (`open-task` oder `speaking-task`), `weiter` (nächster Schritt der Geschichte; auf der letzten Seite der Rückblick auf die Kette).
- **Figur Verbkette** (eigene SVG-Zeichnung, `explainer-representation-explained`): eine Lok (erstes Verb), eine Kupplung (leer oder `to`), ein Wagen (zweites Verb). Lernhandlung: Kinder lesen am Bild ab, ob zwischen den Verben etwas sitzt, und setzen dann die Kette selbst zusammen. Dateien `src/images/verbkette-ohne-kupplung.svg` (can swim), `verbkette-kupplung-to.svg` (would like to swim), `verbkette-skala.svg` (Skala von fest bis offen: must, should, could, might/may). Die Figur zeigt die Form, nie die Lösung einer Aufgabe; die Bildunterschrift sagt, worauf man schaut, `alt` beschreibt die Kette. Szenenbilder `szene-<thema>.svg` mit den Figuren aus `millbrook-klassenzimmer.svg` von hello-millbrook (kopiert, gleich gelassen).
- **Tabelle** „Klassenzimmer-Poster · Modalverben“ (Ausdruck · Bedeutung), wächst von Seite zu Seite: can, can't, must, mustn't, needn't; dann could, may, might, should; dann I'd like …. Steht nie direkt über der Übung, die sie beantwortet.
- **Muster `kupplung-waehlen`** (Seiten 1 und 3): `language-task` mode `choice` mit `distractors`; Fehler *He cans swim*, *She must to go*, *Can you to help me?*, *I'd like go*.
- **Muster `sortieren`**: `matching` Satz und Bedeutung (Fähigkeit, Erlaubnis, Pflicht, Verbot; Rat, Vorschlag, Vermutung; höflich oder direkt) und `ordering` für die Skala.
- **Muster `kette-bauen`**: `language-task` mode `write` mit `cue` und `ordering` von Wörtern; je Fehler eine Meldung, die die Regel nennt; gleichwertige Antworten mit `(a|b)` (`can't|cannot`).
- **Muster `needn't-oder-mustn't`** (Seite 1): `true-false` mit Begründung und `single-choice` an Schildern (Pflicht, Verbot, keine Pflicht). Meldung: deutsch „nicht müssen“ ist needn't, „nicht dürfen“ ist mustn't; *don't must* gibt es nicht.
- **Muster `hoeren-schreiben` und `nachsprechen`**: je Seite ein Diktat (`<seite>-hoeren`) und eine `speaking-task` (`<seite>-nachsprechen`), nur ganze Sätze, Stimme `bf_emma`, erzeugt mit `regen_audio.py` aus hello-millbrook; Namen am Satzende zweisilbig (Sophie, Peter, Amir, Ellie).
- **Muster `anwenden`**: `open-task` mit Punkten der Form (Schulregeln mit can, must und mustn't; Rat mit should und Vorschlag mit could; Bestellung mit I'd like).
- **Engagement je Seite** (Opening, Change, Reward, Story, Repeat):
  - `can-must`: Opening: Sophie liest Schilder im Flur, die Kinder ordnen drei Sätze der Bedeutung zu, bevor etwas erklärt wird. Change: sortieren, Kette bauen, hören, schreiben. Reward: „Du kannst jetzt Regeln für deine Schule schreiben.“ Story: Sophies erste Schulregeln; Schluss: Ellie fragt, was Sophie am Wochenende kann. Repeat: die Kette in anderer Form (Bild, Tabelle, Satz).
  - `modalverben-could-might-should`: Opening: Ellie und Sophie planen das Wochenende, drei Antworten werden der Skala zugeordnet. Change: Skala ordnen, wählen, schreiben. Reward: Ratschläge an Peter geben. Story: Peter hat ein Problem; Schluss: Sophie lädt zum Kiosk ein.
  - `would-like`: Opening: Kiosk, zwei Sätze (*I want a tea*, *I'd like a tea*), welcher ist höflich. Change: vergleichen, Kupplung to finden, Bestellung bauen, hören. Reward: eine höfliche Bestellung. Story: Café mit Mrs Parker; Rückblick auf die Kette (Lok ohne Kupplung, Lok mit to) und Ausblick auf weitere Kupplungen.
- **Selbsteinschätzung** (`selfAssessment` des Kapitels): je Seite zwei Übungen, die ohne die Seite verständlich sind.
- **Prerequisites ohne Übung in der App:** Seite 1 braucht Personalpronomen und einige Alltagsverben (Wörter werden eingeführt), Seite 3 braucht dazu das Verb *like*; beide Links statt `recap` (`personalpronomen` steht nicht in `requires`).
- **Keine Komponente** (`prefer-built-in-block`): alles geht mit Blöcken, Bildern und `language-task`; die Verbkette ist ein statisches SVG.
- **Spätere Kapitel:** Kapitel 2 (Ersatzformen, to und -ing) und 3 (Passiv) kommen als Inkrement `increment/<NN>-<name>`: neue Kapitelordner, die Kette wächst um die Kupplungen to, -ing und be + 3. Form; der Inhaltsführer sagt, wie.

## Code

<!--
- Build the app, locally on `work`, on your own. After each task: `plan done`, then one commit with the work and this
  plan. The hooks check each commit; a failing check is fixed from its message, as skill `lernapps-cli` says.
- What you cannot decide: choose, write it under "Key decisions" with "(guess)", go on.
- The creator asks for a change: say your reading in one sentence first, then change every place it holds for
  (`feedback-applied-everywhere`).
-->

### Tasks

- [x] Load skill `lernapps-cli`. Create the app as its section "Create" says:
      `npx --no -- lernapps create --archetype explainer`.
- [x] Fill the content guide `.agents/skills/app-content/SKILL.md` from "Notes" and "Content method": every heading,
      no "FILL IN" left. Commit it before any content.
- [x] Load skill `lernapps-explainer`.
- [x] Load skill `lernapps-content-questions`. Read whole, with your file tool:
      `.agents/skills/lernapps-explainer/references/blocks.md` and
      `.agents/skills/lernapps-explainer/references/exercises.md`. A foreign language: also
      `references/language-tasks.md` in the same folder. A component in the plan: also `references/components.md`.
- [x] Decide whether the app needs `scope`, as "`scope`" in
      `.agents/skills/lernapps-explainer/references/structure.md` says. Write the choice under "Key decisions".
- [x] Musterseite (src/koennen-muessen/can-must.yaml): Szene Schilder im Flur, Verbkette ohne Kupplung (SVG), Poster-Tabelle Modalverben, mindestens sechs Übungen leicht nach schwer (sortieren, Kupplung wählen, needn't oder mustn't, Kette bauen, Diktat, Nachsprechen), Anwenden: Schulregeln schreiben; Audio mit regen_audio.py; zeigt can, can't, must, mustn't, needn't
<!-- tasks: pattern (1 added): the one page or screen that is the pattern for the others -->
- [ ] **Checkpoint:** the pattern page. Load skill `lernapps-learner-check` and do its learner check on the page. Fix
      what it finds. Then show the creator the page and ask whether the others may follow it. Stop and wait. A
      change: change the pattern first.
- [ ] Seite : Szene Wochenende planen, Skala fest bis offen (SVG), Poster-Tabelle erweitert, Übungen (Skala ordnen, wählen, Kette bauen, Diktat, Nachsprechen), Anwenden: Rat an Peter; zeigt could, may, might, should
- [ ] Seite : Szene Kiosk und Café, Verbkette mit Kupplung to (SVG), Poster-Tabelle I'd like, Übungen (höflich oder direkt, Kupplung wählen, I'd like you to, Bestellung bauen, Diktat, Nachsprechen), Anwenden: höfliche Bestellung; Rückblick auf die Kette
- [ ] Kapitel (chapter.yaml mit Selbsteinschätzung, je Seite zwei Übungen), src/app.yaml (format 2, strand englisch/grammatik, scope), Figuren-SVG aus hello-millbrook kopiert, Medienübersicht und Audio-Markierung prüfen
- [ ] Seite modalverben-could-might-should (src/koennen-muessen/modalverben-could-might-should.yaml): Szene Wochenende planen, Skala fest bis offen (SVG), Poster-Tabelle erweitert, Übungen (Skala ordnen, wählen, Kette bauen, Diktat, Nachsprechen), Anwenden: Rat an Peter; zeigt could, may, might, should
- [ ] Seite would-like (src/koennen-muessen/would-like.yaml): Szene Kiosk und Café, Verbkette mit Kupplung to (SVG), Poster-Tabelle I'd like, Übungen (höflich oder direkt, Kupplung wählen, I'd like you to, Bestellung bauen, Diktat, Nachsprechen), Anwenden: höfliche Bestellung; Rückblick auf die Kette
- [ ] Kapitel koennen-muessen (src/koennen-muessen/chapter.yaml mit Selbsteinschätzung, je Seite zwei Übungen) und src/app.yaml (format 2, strand englisch/grammatik, scope); Medienübersicht und Audio-Markierung prüfen
<!-- tasks: pages (6 added): the other pages or screens, after the pattern -->
- [ ] Update the content guide so that it describes the app as built (`app-content-matches`).
- [ ] Run `npx --no -- lernapps check` until it passes.
- [ ] Look at every screen and state, at 360 px and on a desktop, as "Look at the app" of skill `lernapps-cli` says.
      Compare each with its sketch.
- [ ] Do the whole-app check of skill `lernapps-learner-check`. Fix what it finds and write under "Notes" what you
      fixed.

## Commit

<!--
- Put the app on GitHub, publish it with the creator's yes, then list it. A push to `main` publishes.
- Open the pull requests (to `main`, to the catalog) without asking: they publish nothing.
- The creator asked to stop before publishing (a trial): stop here and say so.
-->

### Tasks

- [ ] Load skill `lernapps-explainer-self-assessment`. Add the self-assessment as it says, or write under "Key
      decisions" why the app has none. Commit.
- [ ] Load skill `lernapps-github`. Set up the repository and Pages as it says. Ask for the repository's name and
      every click only the creator can make, in one message.
- [ ] Push `work`, open the preview pull request and see its checks to green, as skill `lernapps-github` says.
- [ ] **Checkpoint:** publish. Show what the app does and the preview link from the comment "Vorschau der App". Ask
      whether it may go online. Stop and wait for the yes.
- [ ] Load skill `lernapps-commit`. Publish as skill `lernapps-github` says: `work` into `main` as one squash commit,
      the run of `Pages` watched to its end.
- [ ] Open the address the job `deploy` printed and confirm that the app shows. Never use a derived address.
- [ ] Load skill `lernapps-listing`. Write the entry under "Entry draft" as it says, with the creator's answer to
      "Finding the app".
- [ ] Fill the retrospective.
- [ ] Commit this plan on `main` and push it: the listing check and the review read it there.
- [ ] **Checkpoint:** list. Open the listing pull request as skill `lernapps-listing` says, without asking first: the
      pull request is the review. See it to "bestanden", then show the creator the pull request and its result.
- [ ] If the plan changed since its last push, commit it on `main` and push again.

### Entry draft

<!-- YAML valid against the entry schema the listing skill names. Only known values, never invented. -->

```yaml
```

## Retrospective

<!-- At the end of Commit, before the listing pull request. Facts, short, no names. Read by review and evals. -->

### Phases reached

<!-- Last phase completed, checkpoints passed. E.g. "commit; confirmed, published". -->

### Creator turns after the plan

<!-- Number of creator messages after the confirmation, topic of each. Target: at most 3. -->

### Where I had to guess

<!-- Each gap in plan, skills, messages or answers, and your choice. "None" if none. -->
