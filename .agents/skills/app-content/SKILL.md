---
name: app-content
description: Use for any content work in this app - researching, writing, extending, correcting or reviewing its competencies, chapters, pages, rounds, questions, exercises, figures, terms or sources. This app's own content decisions; they take precedence over the generic lernapps content skills. Load it before you change any content.
---

# Content guide of this app

Verbketten (Name der App: `englisch-verbketten`). Explainer (Strang `englisch/grammatik`, Stufe 5-6, Sprache Deutsch) zu Issue lernapps/apps#480 „Verbketten: can, to, -ing und das Passiv“. Die erste Version baut nur Kapitel 1 „Können, müssen, möchten“. Kapitel 2 „to oder -ing?“ und Kapitel 3 „Das Passiv“ (Stufe 7-8) kommen später als Inkrement `increment/<NN>-<name>`.

## Curriculum

Englisch als erste Fremdsprache, Klasse 5-6. Kein Lehrplan: Reihenfolge und Bausteine kommen aus der Lernlandkarte `https://lernapps.net/apps/map/englisch.json` (Fokus `competency`; die Karte ist ein ungeprüfter Entwurf, ihre Quelle sind die KMK-Bildungsstandards von 2004, Fassung 2023). Die App ist eine Strang-App: `strand: englisch/grammatik`. Gemeinsame Konventionen aller Englisch-Explainer: Epic lernapps/apps#489, Muster `lernapps/hello-millbrook`. Nicht hier: Zeitformen mit have + 3. Form und be + -ing (#472), Partizipien statt Nebensätzen (#481).

## Competencies

Kapitel `koennen-muessen` „Können, müssen, möchten“, eine Seite je Baustein, in dieser Reihenfolge. Alle drei sind Lücken der Karte.

1. `can-must` → `koennen-muessen/can-must`: Ich kann mit can, can’t, must, mustn’t und needn’t Fähigkeit, Erlaubnis, Pflicht und Verbot ausdrücken.
2. `modalverben-could-might-should` → `koennen-muessen/modalverben-could-might-should` (requires `can-must`, steht davor): Ich kann mit could, may, might und should Möglichkeiten, Vermutungen und Ratschläge ausdrücken.
3. `would-like` → `koennen-muessen/would-like`: Ich kann mit „I’d like …“ und „I’d like you to …“ höflich sagen, was ich möchte.

Keine Voraussetzung außerhalb der App in der Karte: keine Wiederholungsseite, kein `ahead`. Vorausgesetzt (nicht in `requires`): Personalpronomen (#471) und einige Alltagsverben; die Seite führt jedes Wort mit Bedeutung ein. Die Übungs-IDs haben als Präfix die Seite (`can-must-…`, `modalverben-…`, `would-like-…`) und stehen in den Seitendateien.

## Content structure

- Pfad: `src/koennen-muessen/chapter.yaml` (mit `selfAssessment`), Seiten `src/koennen-muessen/<seite>.yaml`, App in `src/app.yaml`.
- Jede Seite hat dieselben Abschnitts-IDs in dieser Reihenfolge: `einstieg` (Szene, erste leichte Aufgabe, „Das kannst du danach“), `neu` (Verbkette, Merke-Kasten, Poster-Tabelle), `uebung` (mindestens vier Übungen, leicht → schwer), `anwenden` (`open-task` oder `speaking-task`), `weiter` (nächster Schritt der Geschichte; auf der letzten Seite der Rückblick auf die Kette). Die Titel sagen, was der Abschnitt tut.
- Länge: höchstens 350 Wörter Text, höchstens 4 Textblöcke hintereinander, Bild oder Übung in den ersten vier Blöcken.
- Geschichte (Figuren und Ort fest nach den Konventionen, Zeichnungen aus `millbrook-klassenzimmer.svg` von hello-millbrook): Sophie (11 bis 12, blond, Zöpfe, grüne Jacke, aus Deutschland, wohnt bei den Parkers), Ellie Parker (11, roter Pferdeschwanz, rote Jacke), Peter Parker (9, kurze braune Haare, gelbe Jacke), Amir (11, schwarze Locken, Brille, blaue Jacke), Mr Hill (Englischlehrer), Mrs Parker (Ellies Mutter und Sophies Gastmutter), Millbrook School. Seite 1: Sophie liest Schilder im Flur und schreibt Schulregeln; Seite 2: Wochenende planen, Rat an Peter; Seite 3: Kiosk und Café mit Mrs Parker. Jede Seite endet mit dem nächsten Schritt.
- Verbkette: die Idee, die alle Kapitel trägt. Das erste Verb ist die Lok, das zweite der Wagen, dazwischen sitzt die Kupplung, die die Lok bestimmt: keine (can swim), to (would like to swim), später -ing und be + 3. Form (Kapitel 2 und 3).

## Terminology

- Anrede „du“. Wörter: „Verbkette“, „Lok“, „Kupplung“, „Wagen“, „Ausdruck“ (fester Ausdruck, nie „Wendung“), „Klassenzimmer-Poster · Modalverben“ (Tabelle, wächst von Seite zu Seite). Fachbegriffe noun, verb, adjective, sentence, tense.
- Britisches Englisch (favourite, colour). Englische Sätze ohne deutsche Wörter. Englische Wörter immer mit deutscher Bedeutung.
- Modalverben nehmen nie ein -s und nie to; needn’t heißt „nicht müssen“ (keine Pflicht), mustn’t heißt „nicht dürfen“ (Verbot); *don’t must* gibt es nicht.
- Aussprache: Lesehilfe nur wo nötig, in deutscher Annäherung, betonte Silbe in Großbuchstaben (`aim`, `FENK ju`); keine Lautschrift (gehört in #482).

## Exercise patterns

Aufbau je Seite: leicht → schwer: sortieren → Kupplung wählen → Kette bauen → hören → anwenden. Mindestens vier Übungen je Seite, nicht überwiegend Raten, je typischem Fehler eine eigene Rückmeldung.

- `sortieren`: `matching` Satz ↔ Bedeutung (Fähigkeit, Erlaubnis, Pflicht, Verbot; Rat, Vorschlag, Vermutung; höflich, direkt); `ordering` für die Skala must, should, could, might.
- `kupplung-waehlen`: `language-task` mode `choice` mit `distractors` (Lücke vor dem Wagen); Fehler *cans*, *must to*, *Can you to help me?*, *I’d like go*, *I’d like that you help*.
- `kette-bauen`: `language-task` mode `write` mit `cue` oder `ordering` der Wörter; Meldungen nennen die Regel; gleichwertige Antworten mit `(a|b)` (`can’t|cannot`).
- `neednt-oder-mustnt`: `true-false` mit Begründung und `single-choice` an Schildern.
- `hoeren-schreiben` (`<seite>-hoeren`) und `nachsprechen` (`<seite>-nachsprechen`): Diktat und `speaking-task`, nur ganze Sätze.
- `anwenden`: `open-task` mit Punkten der Form.
- Selbsteinschätzung: je Seite zwei Übungen, die ohne die Seite verständlich sind (Skill `lernapps-explainer-self-assessment`).
- Audio: `src/audio/<satz-in-kleinbuchstaben>.mp3`, Stimme `bf_emma` (britisch). Nur ganze Sätze. Erzeugen mit `regen_audio.py` (Kopie aus hello-millbrook im Ordner `scripts/` dieses Skills), damit das Ausklingen abgeschnitten wird. Namen am Satzende zweisilbig (Sophie, Peter, Ellie, Amir).
- Keine Datendateien, keine Komponente: jede Tatsache steht einmal in den Items ihrer Seite.

## Figures

- Eigene SVG-Zeichnungen in `src/images/` (Quelle „eigene Zeichnung“, Lizenz `CC-BY-4.0`), keine Fotos, keine Figuren aus Büchern, Filmen oder Marken.
- Verbkette: `verbkette-ohne-kupplung.svg` (Lok can, Wagen swim, ohne Kupplung), `verbkette-kupplung-to.svg` (Lok would like, Kupplung to, Wagen swim), `verbkette-skala.svg` (Skala fest bis offen: must, should, could, might). Die Figur zeigt die Form, nie die Lösung einer Aufgabe; die Bildunterschrift sagt, worauf man schaut, `alt` beschreibt die Kette.
- Szenen: `szene-<thema>.svg` mit den Figuren aus hello-millbrook; Beschriftungen innerhalb des `viewBox`; jede Figur funktioniert bei 360 px.
- Tabelle „Klassenzimmer-Poster · Modalverben“ (Ausdruck · Bedeutung): Seite 1 can, can’t, must, mustn’t, needn’t; Seite 2 dazu could, may, might, should; Seite 3 dazu I’d like. Sie steht nie direkt über der Übung, die sie beantwortet.

## Sources

Karte `https://lernapps.net/apps/map/englisch.json` und die drei Baustein-Seiten (geöffnet 2026-11-21), Issue #480, Konventionen #489, Muster hello-millbrook. Ungeprüft: Wikipedia (HTTP 429) und die Seite `grundwortschatz` der Karte (HTTP 503/404). Deshalb nur A1-Wörter aus dem Alltag der Kinder, jedes auf der Seite erklärt. Die Grammatikfakten (Modalverben ohne -s und ohne to, needn’t, mustn’t, I’d = I would) sind Standardgrammatik, keine zitierten Sätze. Audio: KI-Stimme britisch weiblich, erzeugt mit Skill `lernapps-audio`, als KI-generiert markiert. Millbrook School ist erfunden. Material des Erstellers: keines.

## Adding a chapter or round

1. Baustein auf der Karte wählen (Voraussetzungen müssen auf früheren Seiten stehen). Kapitel 2 und 3 stehen im Issue #480; sie kommen als Inkrement auf einem eigenen Branch `increment/<NN>-<name>`.
2. Kapitelordner `src/<kapitel>/` mit `chapter.yaml` anlegen, in `src/app.yaml` unter `chapters` eintragen; Seiten `<seite>.yaml` mit den Abschnitten `einstieg`, `neu`, `uebung`, `anwenden`, `weiter` und der Competency-ID.
3. Die Verbkette um die neue Kupplung erweitern (Kapitel 2: to und -ing, Kapitel 3: be + 3. Form); Tabelle „Klassenzimmer-Poster · …“ um die Zeilen der Seite ergänzen.
4. Übungen aus den Mustern oben, je mit `mistakes` und `hint`; 1 bis 3 in `selfAssessment` des Kapitels.
5. Hörtexte mit `regen_audio.py` erzeugen und anhören.
6. `npx --no -- lernapps check`, committen.

## Rules learned from mistakes

Übernommen aus hello-millbrook (Konventionen #489, Abschnitt 5):

- Übungen fragen nur Wörter ab, die vorher auf der Seite stehen.
- Eine Tabelle, die eine Übung beantwortet, steht nicht direkt darüber.
- Englische Aufgaben enthalten kein deutsches Wort.
- Gleichwertige richtige Antworten mit `(a|b)` zulassen; `case: wrong` nur dort, wo die Seite Großschreibung unterrichtet.
- Audio: das Ausklingen am Satzende abschneiden (`regen_audio.py`); Namen am Satzende zweisilbig.
- Bilder: Beschriftungen innerhalb des `viewBox` halten.
