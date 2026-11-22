---
# Read by the hooks, the review, the evals. Schema: @lernapps/tooling/guidance/plan-front-matter.v1.schema.json
# Written by `lernapps plan` and the hooks. Never change a key or a value by hand.
# Archetype, as in the app's first plan. Allowed values: explainer, interactive, quiz.
archetype: explainer
# Current phase. Allowed values: explore, plan, code, commit.
phase: code
# prePushFailures: failed pre-push runs of this increment, written by the hook.
prePushFailures: 0
# failedChecks: failed rules and runs, written by lernapps check and the hooks.
failedChecks: {}
---

# Increment: increment-02-verbketten-7-8

<!--
For you, the assistant. One increment of a published app: new competencies, chapters, pages, rounds, questions, or a
correction. The process is in AGENTS.md; this plan holds the method.
- `npx --no -- lernapps plan next` prints the task to do now, `plan done` ticks it and prints the next one.
- You write only below Goal, Key decisions, Notes, Answers, Content method and Retrospective, in the creator's
  language. Delete the comment of a section once the section is filled.
- The first version's decisions stand: archetype, content method, content guide. Never change an earlier plan.
- Work on the branch `increment/<NN>-<short name>`. Until Commit everything is local: push nothing.
-->

*Started 2026-11-22. Explore, Plan, Code, Commit.*

## Goal

Lernende der Stufe 7-8 wählen nach einem Verb die richtige Kupplung (to, -ing, Präposition + -ing, be + 3. Form) und bilden Ersatzformen der Modalverben und das Passiv in verschiedenen Zeiten. Sie lesen an jeder Seite ein Lesestück (Chat, Tagebuch, Interview, Zeitungsbericht) und wenden die Regel in Aufgaben in drei Stufen an.

## Key decisions

- Inkrement 02 baut die Kapitel 2 „to oder -ing?“ und 3 „Das Passiv“ des Issues #480 (Stufe 7-8) im Repository `lernapps/englisch-verbketten`; Branch `increment/02-verbketten-7-8`. (Auftrag der Orchestrator-Session)
- `scope` in `src/app.yaml` und auf jeder Seite: unverändert nötig (die Seiten haben `open-task`); `app.yaml` bekommt die neuen Kapitel und nimmt die Ersatzformen, to oder -ing und das Passiv aus `scope.out` heraus.
- Archetype, Strang `englisch/grammatik`, Verbkette (Lok, Kupplung, Wagen) und die Regeln aus Abschnitt 7 und 8 der Konventionen bleiben bestehen.
- Kapitelaufbau: je Kapitel eine Sammel-Wiederholung `recap` am Anfang für Bausteine anderer Explainer (will-future, fragewoerter, present-progressive; unregelmaessige-verben, to-be, present-perfect), dann je Baustein eine Seite mit Lesestück. (Karte, `requires`)
- Figuren: Sophie 13 bis 14, bleibt in England; Form: Chats, Tagebuch, Interview, Zeitungsbericht der Schulzeitung, ein Bild nur wo es etwas zeigt (Konventionen Abschnitt 2 und 8).
- Texte schreibe ich selbst (erfundene Szenen der Figuren), keine Sätze aus fremden Quellen; Faktenangaben nur, wo ich sie mit einer geöffneten Quelle belegen kann. (Abschnitt 8)

## Notes

- Strang `englisch/grammatik`, Karte `https://lernapps.net/apps/map/englisch.json` (gelesen 2026-11-22); alle acht Bausteine sind Lücken der Karte (`practisedBy` leer).
- Kapitel 2 „to oder -ing?“ (Stufe 7-8), Reihenfolge nach `requires`:
  1. `modale-ersatzformen` (Schritt 1; requires can-must, will-future): „Ich kann die Ersatzformen have to, be able to und be allowed to verwenden, auch in anderen Zeiten.“
  2. `infinitivkonstruktionen` (Schritt 1; requires would-like, fragewoerter): „Ich kann Infinitive mit to verwenden, zum Beispiel nach in order, nach Fragewörtern und in „It’s easy for me to …“.“
  3. `gerund` (Schritt 1; requires present-progressive): „Ich kann das Gerundium als Subjekt und nach Verben wie like, enjoy und avoid verwenden (Swimming is fun.).“
  4. `gerund-nach-praepositionen` (Schritt 2; requires gerund): „Ich kann nach Präpositionen und Ausdrücken wie interested in oder look forward to das Gerundium verwenden.“
  5. `gerund-oder-infinitiv` (Schritt 2; requires gerund, infinitivkonstruktionen): „Ich kann bei Verben wie stop, remember und try zwischen Gerundium und Infinitiv wählen und den Unterschied in der Bedeutung erklären.“
- Kapitel 3 „Das Passiv“ (Stufe 7-8):
  6. `passiv` (Schritt 1; requires unregelmaessige-verben, to-be): „Ich kann Sätze im Passiv im simple present und simple past bilden und sagen, wer etwas getan hat (by …).“
  7. `passiv-zeiten` (Schritt 2; requires passiv, present-perfect, will-future, can-must): „Ich kann das Passiv auch im present perfect, im will-future und mit Modalverben bilden (It has been sold. It can be done.).“
  8. `passiv-zwei-objekte` (Schritt 3; requires passiv-zeiten): „Ich kann bei Verben mit zwei Objekten das persönliche Passiv bilden (I was given a book.).“
- Voraussetzungen außerhalb der App: will-future, fragewoerter, present-progressive (Kapitel 2); unregelmaessige-verben, to-be, present-perfect (Kapitel 3; will-future steht schon im Kapitel 2). Je eine `recap`-Seite „Das brauchst du hier“ am Kapitelanfang, ohne Übung; `can-must` und `would-like` übt Kapitel 1 dieser App (Link statt Wiederholung).
- Didaktik: Die Verbkette wächst um die Kupplungen to, -ing, Präposition + -ing und be + 3. Form. Ersatzformen (have to, be able to) setzen eine Lok vor die Modalverben, damit sie in andere Zeiten fahren können. Die Kinder sortieren Verbkarten nach ihrer Kupplung (Issue #480). Passiv: Das Objekt kommt nach vorn, der Täter wird klein (by …) oder verschwindet; be + 3. Form passt in jede Zeit und hinter jedes Modalverb.
- Form je Seite (Abschnitt 8): Lesestück 150 bis 300 Wörter (nicht in den 350 Wörtern Erklärtext), Vorwissen-Frage, Text in Abschnitten mit Randglossar (`definition`-Blöcke), Aufgaben in drei Stufen (Verstehen, Belegen mit Zeile, Meinung), dann Schreib- oder Sprechauftrag; höchstens ein Lesestück, höchstens etwa 25 Items je Seite.
- Scope: drin: have to, be able to, be allowed to (in present, past, will-future, present perfect), Infinitiv mit to (in order to, Fragewort + to, It's easy for me to …), Gerundium als Subjekt und nach like, enjoy, avoid, finish, mind, Präposition + -ing (interested in, look forward to, good at, thinking of), stop/remember/try mit -ing oder to, Passiv in simple present und past, present perfect, will-future und mit Modalverben, persönliches Passiv (I was given …). Draußen: Partizipien statt Nebensätze (#481), Passiv Progressive und Passiv im past perfect (Stufe 9-10), die Zeitformen selbst (#472), alle weiteren Verben mit -ing oder to (Auswahl der häufigsten).
- Neue Art von Inhalt: Lesestück als Kern der Seite (Abschnitt 8). Es gibt keinen eigenen Block; geplant mit `section` + `text`/`quote`-Blöcken für den Text in Abschnitten, `definition`-Blöcke als Randglossar, Aufgaben in drei Stufen mit `single-choice`, `ordering`, `language-task`, `open-task`. Der Plan hält fest, was die Vorlage nicht kann (kein Zeilenbeleg-Block): „Belegen mit Zeile“ als `single-choice` mit Zitat aus dem Text.
- Quellen: Karte und Issue #480, Konventionen #489 (Abschnitt 7 und 8). Grammatikregeln sind Standardgrammatik ohne zitierte Sätze; Wikipedia und Grundwortschatz-Liste zur Prüfung der Wörter (Stufe A1/A2, höhere Wörter im Randglossar).

## Explore

<!--
- All content questions belong here; Plan maps the answers onto the app. Ask; write no code.
- Skip what earlier answers or the app already tell. At most 2 questions per message, one topic each.
-->

### Tasks

- [x] Read the README of the archetype's template (its path is in skill `lernapps-app`): what the app can do now.
      Tell the creator what is new, if it matters for this increment.
- [x] Load the content guide `.agents/skills/app-content/SKILL.md` and read the earlier plans in `.vibe/plans/`: what
      the app teaches, how its content is made, what is open.
- [x] Interview, one topic per question, the creator's words under "Answers": which competencies, chapters or rounds,
      for which school years; hurdles and examples; the amount; any change of look and feel or of terms. No answer:
      ask once more, then write your assumption with "(guess)".
- [x] Load skill `lernapps-content-research`. Research what the content guide does not cover. Write under "Notes":
      the new competencies by chapter with their ids, the sources you opened.
- [x] Write under "Notes" the didactic approach per competency and the scope (in, out, data range).
- [x] The increment needs a kind of content the guide does not cover (a new page structure, screen, component or kind
      of exercise): load skills `lernapps-explainer-design` and `lernapps-exercise-patterns`. Else skip this task.
- [x] **Checkpoint:** research. Show in plain words: the new competencies by chapter, the didactic approach, the
      scope, every "(guess)", the sources and what is unchecked. Stop and wait. Changes: change them, then ask again.
      Creator: Ja, passt: zwei Wiederholungsseiten und Seiten ohne Szenenbilder (Chats und Texte) sind richtig für 7-8; die Verbkette bleibt als Bild, wo sie etwas zeigt. Weiter zum Plan. Push und zweiter Vorschau-PR erst nach Erlaubnis der Ersteller:in, bis dahin lokal.

### Answers

- (Auftrag der Orchestrator-Session, in der Rolle der Ersteller:in) Kapitel 2 „to oder -ing?“ und 3 „Das Passiv“, Stufe 7-8, als Inkrement in dasselbe Repository; Lesestücke als Kern der Seite, Eigentexte nach Fakten, Figuren 13 bis 14, Abschnitt 7 und 8 der Konventionen.
- Amount: alle acht Bausteine (5 + 3) mit je einer Seite und einer Sammel-Wiederholung je Kapitel.
- Look and feel, Terms: unverändert (Verbkette, Lok, Kupplung, Wagen; „Ausdruck“; „Klassenzimmer-Poster · …“, „Schulkalender · …“).
- Hurdles: (guess, aus der Grammatik) to oder -ing nach dem falschen Verb (*enjoy to swim*, *I want swimming*), -ing nach Präposition vergessen (*interested in to learn*), stop/remember/try (Bedeutungsunterschied), Passiv: *is build*, *was broke*, Täter mit *from* statt *by*, persönliches Passiv (*I was given* statt *it was given to me*).

## Plan

<!--
- Map the new content onto the app with the guide's patterns. The creator confirms the plan in one read.
- After the yes you work on your own.
-->

### Tasks

- [x] Load skill `lernapps-content-growth`. Add the tasks of Code as slices, one per competency, in the guide's
      order, one call each: `npx --no -- lernapps plan add --at slices "<task>"`. Say in each which sub-agent may
      write it in parallel, if any.
- [x] Write "Content method": the guide's patterns, figures and components per slice. Anything new: map it as skill
      `lernapps-explainer-design` says, and say why the guide's patterns do not fit.
- [x] (skipped: keine neue Komponente und keine interaktive Übung, nur die Seitenskizze im Markdown) Draw a sketch of each new component or interactive exercise, in `.vibe/sketches/`.
- [x] Show the creator, short: goal, new competencies by chapter, slices; in plain words what learners see and do and
      what is new. At most 2 questions.
- [x] **Checkpoint:** confirm the plan and the content method. Stop and wait for an explicit yes. Changes: change
      them, then ask again.
      Creator: Ja, Plan bestätigt. Lokale Worktrees für die Sub-Agenten sind ok, kein Push. Weiter mit der Musterseite modale-ersatzformen.

### Content method

<!-- One line each: the guide's patterns, figures and components used, and where; anything new, what it does and
cannot. Something new goes into the guide in the slice that adds it. -->
<!-- An explainer: per figure, model and component its learning action in two to four sentences
(`explainer-representation-explained`); per page its prerequisites the app does not practise, and which get a recap
page, which a link. -->

- **Neue Seitenform (Abschnitt 8):** Ein Lesestück trägt die Seite. Das Muster aus Kapitel 1 (Einstieg, neu, Übung, anwenden, weiter) bleibt, mit festen Abschnitts-IDs auf jeder Seite von Kapitel 2 und 3: `einstieg` (Vorwissen-Frage als `single-choice` mit drei Optionen, kurze Einführung der Szene und „Das kannst du danach“), `lesen` (Lesestück 150 bis 300 Wörter in zwei bis drei `text`-Blöcken, Chat als Zeilen „**Sophie:** …“, Tagebuch oder Artikel als Absätze; schwere Wörter als `definition`-Blöcke direkt hinter dem Abschnitt: das Randglossar), `verstehen` (drei Stufen: 1 Verstehen `single-choice` oder `true-false`, 2 Belegen: `single-choice` „Welcher Satz aus dem Text zeigt …?“ mit Zitat, 3 Meinung als `open-task`), `neu` (Regel mit der Verbkette als Bild, Merke-Kasten, Poster-Tabelle), `uebung` (Kupplung wählen, sortieren, Kette bauen, Passiv umdrehen), `anwenden` (Schreibauftrag, Sprechauftrag), `weiter`. Höchstens ein Lesestück und etwa 25 Items je Seite; das Lesestück zählt nicht zu den 350 Wörtern Erklärtext.
- **Warum die Muster aus Kapitel 1 nicht reichen:** Dort gab es nur kurze Szenen. Neu sind Lesestück und Randglossar (kein eigener Block in der Vorlage: `text` und `definition` reichen), und „Belegen mit Zeile“ (kein Zeilenbeleg-Block: `single-choice` mit Zitat). Alles andere bleibt: `language-task` (choice, write, gap), `ordering`, `matching`, `open-task`, `speaking-task`, Diktat.
- **Verbkette (Bild):** Kapitel 1 hat die Kupplungen „keine“ und „to“. Neu `verbkette-ing.svg` (enjoy + -ing + swimming), `verbkette-praeposition.svg` (interested + in + swimming), `verbkette-passiv.svg` (was + 3. Form + built: Lok be, Kupplung 3. Form). Jedes Bild gleicher Stil (blaue Lok, rote Kupplung, gelber Wagen), eigene Zeichnung, `alt` und Bildunterschrift sagen, wohin man schaut, die Figur zeigt nie die Lösung einer Aufgabe.
- **Tabelle:** „Klassenzimmer-Poster · Verben und ihre Kupplung“ (Verb · Kupplung · Beispiel) wächst von Seite zu Seite, höchstens drei Spalten; steht nie direkt über der Übung, die sie beantwortet; Beispiele des Posters stehen nicht in den Übungen.
- **Verbkarten sortieren:** `matching` Verb ↔ Kupplung („enjoy“ ↔ „-ing“, „want“ ↔ „to“, „can“ ↔ „keine“) als Sortierübung auf `gerund` und `gerund-oder-infinitiv`.
- **Figuren:** Sophie 13 bis 14, Ellie, Peter (11), Amir (13), Mr Hill, Mrs Parker (rote Haare als Dutt, türkise Strickjacke); Chats mit Namen und Uhrzeit, kein Szenenbild, nur wo ein Bild etwas zeigt (Verbkette). Neue Nebenfiguren nur nach Rückfrage.
- **Wiederholungsseiten** (`wiederholung` in jedem der zwei Kapitel): `recap` mit Liste der Bausteine, Text nennt jede Kompetenz mit ihrem „Ich kann …“-Satz, kein Bild, keine Übung.
- **Regeln Abschnitt 7:** Hörsätze (3 Diktat, 3 Nachsprechen je Seite) stehen nicht wörtlich oder fast wörtlich im Text derselben Seite (Fuzzy-Prüfung durch mich); ein Hörsatz bleibt der natürliche Satz; Audio nur mit `regen_audio.py` (Fehllaut-Schnitt); Hörliste und `audio-texte.json` im Inhaltsführer; Distraktoren nur echte Lernerfehler; höchstens eine kurze Wörtertabelle je Seite; `punctuation: ok`; Varianten mit `(a|b)`; Einstiegs-`single-choice` mit mindestens drei Optionen; im Modus `choice` zeigt die Vorlage keine `mistakes`.
- **Selbsteinschätzung:** Kapitel 2 und 3 je eine pro Kapitel, je Seite zwei Übungen, die ohne den Lesetext verständlich sind (also keine Textfragen).
- **Sub-Agenten:** A schreibt die vier Seiten von Kapitel 2 nach meinem Muster (`modale-ersatzformen`), B die drei Seiten und die Wiederholung von Kapitel 3, jeder in einem eigenen Worktree, nur seine Seitendateien und Bilder; ich ergänze `chapter.yaml`, `app.yaml`, Selbsteinschätzung und Inhaltsführer und prüfe jede Seite mit einem Skript.

## Code

<!--
- Build locally on the branch, on your own. After each task: `plan done`, then one commit with the work and this
  plan. The hooks check each commit; a failing check is fixed from its message, as skill `lernapps-cli` says.
- What you cannot decide: choose, write it under "Key decisions" with "(guess)", go on.
- The creator asks for a change: say your reading in one sentence first.
-->

### Tasks

- [x] `git switch -c increment/<NN>-<short name>` from `main`. Commit this plan on it.
- [x] Load skill `lernapps-cli`. Update the app as its section "Update" says. Commit the update alone and fix its
      findings before any content. The update replaces the `lernapps-*` skills: read again those you use.
- [x] Load skill `lernapps-explainer` and the content guide.
- [x] Load skill `lernapps-content-questions`. Read whole, with your file tool:
      `.agents/skills/lernapps-explainer/references/blocks.md` and
      `.agents/skills/lernapps-explainer/references/exercises.md`. A foreign language: also
      `references/language-tasks.md` in the same folder. A component in the plan: also `references/components.md`.
- [x] Decide whether the app needs `scope`, as "`scope`" in
      `.agents/skills/lernapps-explainer/references/structure.md` says. Write the choice under "Key decisions".
- [x] Kapitel 2 (Ordner src/to-oder-ing): chapter.yaml, Wiederholungsseite wiederholung (recap: will-future, fragewoerter, present-progressive) und Seite modale-ersatzformen als Muster mit Lesestück (Chat Sophie und Ellie), Randglossar, drei Aufgabenstufen, Audio; zeigt have to, be able to, be allowed to in mehreren Zeiten. Ich schreibe sie selbst (Muster).
- [ ] Seite infinitivkonstruktionen (src/to-oder-ing/infinitivkonstruktionen.yaml): Lesestück Tagebuch oder Blog (in order to, Fragewort + to, It is easy for me to); Sub-Agent A (Kapitel 2), nach dem Muster.
- [ ] Seite gerund (src/to-oder-ing/gerund.yaml): Lesestück Chat über Hobbys (Swimming is fun, enjoy, avoid, like + -ing); Sub-Agent A.
- [ ] Seite gerund-nach-praepositionen (src/to-oder-ing/gerund-nach-praepositionen.yaml): Lesestück Interview (interested in, look forward to, good at + -ing); Sub-Agent A.
- [ ] Seite gerund-oder-infinitiv (src/to-oder-ing/gerund-oder-infinitiv.yaml): Lesestück Blogeintrag (stop, remember, try mit -ing oder to, Bedeutungsunterschied); Sub-Agent A.
- [ ] Kapitel 3 (Ordner src/das-passiv): chapter.yaml, Wiederholungsseite wiederholung (recap: unregelmaessige-verben, to-be, present-perfect) und Seite passiv (Lesestück Bericht der Schulzeitung, simple present und past, by …); Sub-Agent B.
- [ ] Seite passiv-zeiten (src/das-passiv/passiv-zeiten.yaml): Lesestück Nachrichten/Chat (present perfect, will-future, mit Modalverben: It has been sold, It can be done); Sub-Agent B.
- [ ] Seite passiv-zwei-objekte (src/das-passiv/passiv-zwei-objekte.yaml): Lesestück Geburtstagsbericht oder Chat (I was given a book, persönliches Passiv); Sub-Agent B.
<!-- tasks: slices (8 added): one per competency, as written in Plan -->
- [ ] **Checkpoint:** the pattern page, after the first slice. A slice in a pattern the app already has: show it to
      the creator and go on. A new pattern: load skill `lernapps-learner-check`, do its learner check, fix what it
      finds, then ask the creator whether the others may follow it, and wait.
- [ ] Update the content guide so that it describes the app as it is now (`app-content-matches`).
- [ ] Run `npx --no -- lernapps check` until it passes.
- [ ] Look at every changed screen, at 360 px and on a desktop, as "Look at the app" of skill `lernapps-cli` says.

## Commit

<!--
- Publish with the creator's yes. A push to `main` publishes.
- Open the pull requests (to `main`, to the catalog) without asking: they publish nothing.
-->

### Tasks

- [ ] If pages or exercises changed, load skill `lernapps-explainer-self-assessment` and update the self-assessment
      as it says. Commit.
- [ ] Load skill `lernapps-github`. Push the branch, open the preview pull request and see its checks to green, as it
      says.
- [ ] **Checkpoint:** publish. Show what the increment adds and the preview link. Ask whether it may go online. Stop
      and wait for the yes.
- [ ] Load skill `lernapps-commit`. Publish as skill `lernapps-github` says: the pull request squash-merged into
      `main`, the run of `Pages` watched to its end.
- [ ] Open the address the job `deploy` printed and confirm the new content. Never use a derived address.
- [ ] The app is listed and its entry changes (school years, summary): load skill `lernapps-listing` and write the
      changed entry. Else skip this task.
- [ ] Fill the retrospective.
- [ ] Commit this plan on `main` and push it. A push of only `.vibe/` publishes nothing.
- [ ] **Checkpoint:** list. The entry changed: open the pull request to the catalog as skill `lernapps-listing`
      says, without asking first, see it to "bestanden", then show the creator the pull request and its result. The
      entry did not change: tell the creator that the catalog updates the app by itself.
- [ ] If the plan changed since its last push, commit it on `main` and push again.

## Retrospective

<!-- At the end of Commit. Facts, short, no names. Read by review and evals. -->

### Phases reached

<!-- Last phase completed, checkpoints passed. E.g. "commit; confirmed, published". -->

### Creator turns after the plan

<!-- Number of creator messages after the confirmation, topic of each. Target: at most 3. -->

### Where I had to guess

<!-- Each gap in plan, skills, content guide, messages or answers, and your choice. "None" if none. -->
