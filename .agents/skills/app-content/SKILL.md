---
name: app-content
description: Use for any content work in this app - researching, writing, extending, correcting or reviewing its competencies, chapters, pages, rounds, questions, exercises, figures, terms or sources. This app's own content decisions; they take precedence over the generic lernapps content skills. Load it before you change any content.
---

# Content guide of this app

Verbketten (Name der App: `englisch-verbketten`). Explainer (Strang `englisch/grammatik`, Stufe 5-6, Sprache Deutsch) zu Issue lernapps/apps#480 „Verbketten: can, to, -ing und das Passiv“. Die erste Version baut Kapitel 1 „Können, müssen, möchten“ (Stufe 5-6). Das Inkrement 02 (`increment/02-verbketten-7-8`) fügt Kapitel 2 „to oder -ing?“ und Kapitel 3 „Das Passiv“ (Stufe 7-8) hinzu.

## Curriculum

Englisch als erste Fremdsprache, Klasse 5-6 (Kapitel 1) und 7-8 (Kapitel 2 und 3). Kein Lehrplan: Reihenfolge und Bausteine kommen aus der Lernlandkarte `https://lernapps.net/apps/map/englisch.json` (Fokus `competency`; die Karte ist ein ungeprüfter Entwurf, ihre Quelle sind die KMK-Bildungsstandards von 2004, Fassung 2023). Die App ist eine Strang-App: `strand: englisch/grammatik`. Gemeinsame Konventionen aller Englisch-Explainer: Epic lernapps/apps#489, Muster `lernapps/hello-millbrook`. Nicht hier: Zeitformen mit have + 3. Form und be + -ing (#472), Partizipien statt Nebensätzen (#481).

## Competencies

Kapitel `koennen-muessen` „Können, müssen, möchten“, eine Seite je Baustein, in dieser Reihenfolge. Alle drei sind Lücken der Karte.

1. `can-must` → `koennen-muessen/can-must`: Ich kann mit can, can’t, must, mustn’t und needn’t Fähigkeit, Erlaubnis, Pflicht und Verbot ausdrücken.
2. `modalverben-could-might-should` → `koennen-muessen/modalverben-could-might-should` (requires `can-must`, steht davor): Ich kann mit could, may, might und should Möglichkeiten, Vermutungen und Ratschläge ausdrücken.
3. `would-like` → `koennen-muessen/would-like`: Ich kann mit „I’d like …“ und „I’d like you to …“ höflich sagen, was ich möchte.

Keine Voraussetzung außerhalb der App in der Karte: keine Wiederholungsseite, kein `ahead`. Vorausgesetzt (nicht in `requires`): Personalpronomen (#471) und einige Alltagsverben; die Seite führt jedes Wort mit Bedeutung ein. Übungs-IDs (Präfix = Seite):
- `can-must`: `can-must-start`, `can-must-sortieren` (matching), `can-must-kupplung` (Lücke wählen), `can-must-needn` (single-choice), `can-must-reihenfolge` (ordering), `can-must-schreiben`, `can-must-hoeren`, `can-must-nachsprechen`, `can-must-regeln` (open-task).
- `modalverben-could-might-should`: `modalverben-start`, `modalverben-sortieren`, `modalverben-wahl`, `modalverben-skala` (ordering), `modalverben-schreiben`, `modalverben-hoeren`, `modalverben-nachsprechen`, `modalverben-rat` (open-task).
- `would-like`: `would-like-start`, `would-like-sortieren`, `would-like-kupplung`, `would-like-reihenfolge`, `would-like-schreiben`, `would-like-hoeren`, `would-like-nachsprechen`, `would-like-bestellen` (open-task).
- Selbsteinschätzung (`chapter.yaml`): je Seite `…-sortieren` und das Lückenwählen (`can-must-kupplung`, `modalverben-wahl`, `would-like-kupplung`).

### Kapitel 2 und 3 (Stufe 7-8)

Alle acht sind Lücken der Karte. Jede Seite hat ein Lesestück (Konventionen Abschnitt 8); Sophie ist 13 bis 14.

Kapitel `to-oder-ing` (Ordner `src/to-oder-ing/`, Seiten in dieser Reihenfolge):
- `wiederholung` (`recap`: `englisch/will-future`, `englisch/fragewoerter`, `englisch/present-progressive`; keine Übung).
- `modale-ersatzformen` (Karte: Ich kann die Ersatzformen have to, be able to und be allowed to verwenden, auch in anderen Zeiten.): Lesestück Chat über einen Schulausflug; Übungen `ersatz-start`, `ersatz-zwischendurch-eins`, `ersatz-zwischendurch-zwei`, `ersatz-verstehen`, `ersatz-belegen`, `ersatz-meinung` (open-task), `ersatz-sortieren` (matching), `ersatz-wahl` (Lücke), `ersatz-reihenfolge`, `ersatz-schreiben`, `ersatz-hoeren`, `ersatz-nachsprechen`, `ersatz-schreiben-frei`.
- `infinitivkonstruktionen` (Ich kann Infinitive mit to verwenden, zum Beispiel nach in order, nach Fragewörtern und in „It’s easy for me to …“.): Tagebuch; Präfix `infinitiv-` (`start`, `zwischen-eins`, `zwischen-zwei`, `verstehen`, `belegen`, `meinung`, `sortieren`, `kupplung`, `reihenfolge`, `schreiben`, `hoeren`, `nachsprechen`, `anwenden`).
- `gerund` (Ich kann das Gerundium als Subjekt und nach Verben wie like, enjoy und avoid verwenden (Swimming is fun.).): Chat über Hobbys; Präfix `gerund-` (gleiche Endungen).
- `gerund-nach-praepositionen` (Ich kann nach Präpositionen und Ausdrücken wie interested in oder look forward to das Gerundium verwenden.): Interview der „Millbrook Times“; Präfix `praeposition-`.
- `gerund-oder-infinitiv` (Ich kann bei Verben wie stop, remember und try zwischen Gerundium und Infinitiv wählen und den Unterschied in der Bedeutung erklären.): Blog; Präfix `wahl-`.

Kapitel `das-passiv` (Ordner `src/das-passiv/`):
- `wiederholung` (`recap`: `englisch/unregelmaessige-verben`, `englisch/to-be`, `englisch/present-perfect`).
- `passiv` (Ich kann Sätze im Passiv im simple present und simple past bilden und sagen, wer etwas getan hat (by …).): Bericht der „Millbrook Times“ über ein Herbstfest; Präfix `passiv-` (`start`, `zwischen-eins`, `zwischen-zwei`, `verstehen`, `belegen`, `meinung`, `sortieren`, `wahl`, `reihenfolge`, `umdrehen`, `hoeren`, `nachsprechen`, `anwenden`).
- `passiv-zeiten` (Ich kann das Passiv auch im present perfect, im will-future und mit Modalverben bilden (It has been sold. It can be done.).): Chat der Organisatoren vor dem Schulfest; Präfix `zeiten-` (zusätzlich `zeiten-verneinung`).
- `passiv-zwei-objekte` (Ich kann bei Verben mit zwei Objekten das persönliche Passiv bilden (I was given a book.).): Tagebuch vom 14. Oktober (Sophie wird 14; das Herbstfest war am 19. September, der Chat am 8. Oktober, das Schulfest am 10. Oktober; Sophies Eltern heißen „my mum and dad“, Mrs Parker ist die Gastmutter); Präfix `zwei-objekte-`.

Selbsteinschätzung: je Seite `…-sortieren` und `ersatz-wahl` beziehungsweise das Lückenwählen (`…-kupplung` oder `…-wahl`), ohne Bezug auf den Lesetext.

## Content structure

- Pfad: `src/koennen-muessen/chapter.yaml` (mit `selfAssessment`), Seiten `src/koennen-muessen/<seite>.yaml`, App in `src/app.yaml`.
- Jede Seite hat dieselben Abschnitts-IDs in dieser Reihenfolge: `einstieg` (Szene, erste leichte Aufgabe, „Das kannst du danach“), `neu` (Verbkette, Merke-Kasten, Poster-Tabelle), `uebung` (mindestens vier Übungen, leicht → schwer), `anwenden` (`open-task` oder `speaking-task`), `weiter` (nächster Schritt der Geschichte; auf der letzten Seite der Rückblick auf die Kette). Die Titel sagen, was der Abschnitt tut.
- Jede Seite hat höchstens eine kurze Wörtertabelle „Klassenzimmer-Poster · Neue Wörter“ (Wort, Bedeutung) in `einstieg`, nur mit Wörtern, die Kinder der Stufe vermutlich nicht kennen; einfache A1-Wörter gelten als bekannt. Ein Einstiegs-`single-choice` hat mindestens drei Optionen.
- Seiten von Kapitel 2 und 3 haben die Abschnitte `einstieg` (Vorwissen-Frage mit drei Optionen, „Das kannst du danach“), `lesen` (Lesestück 150 bis 300 Wörter in zwei bis drei Textblöcken, Chat als Zeilen „**Sophie:** …“; schwere Wörter als `vocabulary`-Block „Wörter zum Text“ (Nomen mit Artikel, Verben ohne to) direkt hinter dem Abschnitt, das Randglossar; zwischen den Abschnitten je eine Zwischenfrage `…-zwischen-eins/-zwei`), `verstehen` (drei Stufen: Verstehen, Belegen mit Zitat als `single-choice`, Meinung als `open-task`), `neu` (Regel mit Verbkette-Bild, Poster-Tabelle, danach der Merke-Kasten, damit die Tabelle nicht direkt über der Übung steht), `uebung`, `anwenden`, `weiter`. Wörter-Tabellen und Randglossare sind `vocabulary`-Blöcke (Vorlage 0.14), keine Tabellen oder `definition`-Blöcke; Grammatikbegriffe wären `definition`. Das Lesestück zählt der Check (`explainer-text-load`) mit; der Hinweis ist bekannt und laut Konventionen ausgenommen.
- Länge: höchstens 350 Wörter Text, höchstens 4 Textblöcke hintereinander, Bild oder Übung in den ersten vier Blöcken.
- Geschichte (Figuren und Ort fest nach den Konventionen, Zeichnungen aus `millbrook-klassenzimmer.svg` von hello-millbrook): Sophie (11 bis 12, blond, Zöpfe, grüne Jacke, aus Deutschland, wohnt bei den Parkers), Ellie Parker (11, roter Pferdeschwanz, rote Jacke), Peter Parker (9, kurze braune Haare, gelbe Jacke), Amir (11, schwarze Locken, Brille, blaue Jacke), Mr Hill (Englischlehrer), Mrs Parker (Ellies Mutter und Sophies Gastmutter), Millbrook School. Seite 1: Sophie, Peter und Amir vor zwei Schildern im Flur, Schulregeln; Seite 2: Ellie und Sophie planen das Wochenende, Rat an Peter; Seite 3: Café mit Mrs Parker nach dem Kino. Jede Seite endet mit dem nächsten Schritt. Mrs Parker ist als `<g id="parker">` in `src/images/szene-cafe.svg` gezeichnet (rote Haare #b5501e als Dutt, türkise Strickjacke #2a9d8f, Haut #f1cdb0; verbindlich nach `konventionen.md`); bei weiteren Szenen von dort kopieren.
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
- Audio: `src/audio/<satz-in-kleinbuchstaben>.mp3`, Stimme `bf_emma` (britisch). Nur ganze Sätze. Erzeugen mit `regen_audio.py` (Kopie aus hello-millbrook im Ordner `scripts/` dieses Skills), damit das Ausklingen abgeschnitten wird. Hörsätze bleiben natürliche Sätze: kein Name nur wegen des Klangs anhängen (ein Name steht nur, wo der Satz ihn braucht). Alle 18 Sätze stehen in `.agents/skills/app-content/audio-texte.json` (Datei → Satz); neue Sätze dort eintragen und mit `regen_audio.py audio-texte.json <Satz>` erzeugen.

**Hörliste** (Ersteller:in hört gezielt). Alle 66 Dateien sind mit dem Fehllaut-Schnitt (`valley_cut` in `scripts/regen_audio.py`) erzeugt; geschnitten wurde bei: sophie-cant-cook (65 ms), you-mustnt-shout (25 ms), nobody-told-us-when-to-start (25 ms), my-dad-enjoys-listening-to-old-songs (75 ms), keeping-a-diary-is-a-good-habit (85 ms), he-is-afraid-of-flying-in-small-planes (75 ms), please-remember-to-turn-off-your-phones (95 ms), my-brother-had-to-cook-dinner-last-night (55 ms), the-gate-was-closed-at-night (25 ms), phones-mustnt-be-used-in-the-test (25 ms), were-all-the-children-given-a-present (45 ms), the-museum-is-closed-on-mondays (95 ms). Einsilbig endend (Störlaut möglich): `we-can-walk-to-school`, `sophie-cant-cook`, `must-we-wait-here`, `can-you-write-your-name`, `we-neednt-clean-the-board`, `you-mustnt-shout`, `peter-might-forget-his-bag`, `which-one-would-you-like`, `id-like-you-to-close-the-door-please`, `id-like-a-cup-of-coffee-please`, `would-you-like-to-dance`, `amir-would-like-some-more-bread`, `our-teacher-wasnt-allowed-to-park-here`, `you-will-have-to-bring-a-pencil-case`, `my-brother-had-to-cook-dinner-last-night`, `we-went-to-the-shop-to-buy-some-milk`, `can-you-tell-me-where-to-put-these-books`, `it-is-not-difficult-for-us-to-find-the-way`, `he-opened-the-window-to-let-in-some-fresh-air`, `nobody-told-us-when-to-start`, `my-dad-enjoys-listening-to-old-songs`, `we-avoid-walking-home-alone-after-dark`, `learning-new-words-takes-a-lot-of-time`, `i-dont-mind-carrying-the-bags`, `peter-hates-cleaning-his-room`, `im-tired-of-waiting-for-the-bus`, `after-finishing-her-homework-she-went-to-bed`, `please-check-your-bag-before-leaving-the-room`, `he-is-afraid-of-flying-in-small-planes`, `she-stopped-to-answer-her-phone`, `do-you-remember-visiting-this-museum-last-year`, `he-tried-to-sleep-but-the-music-was-too-loud`, `please-remember-to-turn-off-your-phones`, `the-baby-stopped-crying-and-went-to-sleep`, `the-gate-was-closed-at-night`, `your-bags-will-be-taken-to-your-room`, `nothing-should-be-left-on-the-floor`, `phones-mustnt-be-used-in-the-test`, `we-were-handed-a-map-at-the-door`, `students-are-given-homework-every-day`. Mehrsilbig endend (Risiko, dass eine Silbe angeschnitten wird): `the-museum-is-closed-on-mondays`, `amir-could-bring-his-football`, `you-should-drink-some-water`, `it-might-be-sunny-on-sunday`, `could-we-sit-in-the-garden`, `you-should-go-to-bed-early`, `sophie-would-like-to-call-her-mother`, `were-you-able-to-find-the-library`, `we-dont-have-to-pay-for-the-museum`, `will-you-be-allowed-to-come-to-the-party`, `it-is-good-for-children-to-play-outside`, `keeping-a-diary-is-a-good-habit`, `we-walked-instead-of-waiting-for-a-taxi`, `do-you-dream-of-living-in-a-big-city`, `try-adding-a-little-more-water`, `football-is-played-in-the-park-every-sunday`, `our-class-was-invited-to-the-party`, `my-bike-was-washed-by-my-brother`, `is-this-game-played-in-your-country`, `the-windows-have-been-washed-this-morning`, `our-guests-were-served-a-lovely-dinner`, `were-you-told-the-news-yesterday`, `i-was-sent-a-lot-of-messages-on-my-birthday`, `were-all-the-children-given-a-present`, `how-many-people-have-been-invited`, `everything-will-be-explained-tomorrow`. Kein Satz wurde wegen des Klangs verändert; kein Mensch hat bisher eine Datei angehört.
- Keine Datendateien, keine Komponente: jede Tatsache steht einmal in den Items ihrer Seite.

## Figures

Kapitel 2 und 3: `verbkette-ersatz.svg` (will have to go), `verbkette-ing.svg` (enjoy + -ing + swimming), `verbkette-praeposition.svg` (interested + in + -ing), `verbkette-zwei-wege.svg` (remember to call und remember calling), `verbkette-passiv.svg` (Lok is, Kupplung „3. Form“, Wagen made), `verbkette-passiv-zeiten.svg` (will be, can be, has been), `satz-umdrehen.svg` (Aktiv und Passiv mit Pfeilen), `satz-zwei-objekte.svg` (zwei Passivsätze). Alle in blauer Lok, rosa Kupplung, gelbem Wagen, eigene Zeichnung CC-BY-4.0; dazu `verbkette-um-zu.svg` (in order to, Fragewort + to, easy for me to). Die Kupplung ist überall dieselbe Beschreibung: die Form, die die Lok vom Wagen verlangt (keine, to, -ing, Präposition + -ing, bei be die 3. Form); beim Passiv ist be die Lok und der Wagen steht in der 3. Form. Poster-Tabellen: „Klassenzimmer-Poster · Ersatzformen“, „· Verben und ihre Kupplung“ (Verb, Kupplung, Beispiel) und „· Das Passiv“, höchstens drei Spalten.

- Eigene SVG-Zeichnungen in `src/images/` (Quelle „eigene Zeichnung“, Lizenz `CC-BY-4.0`), keine Fotos, keine Figuren aus Büchern, Filmen oder Marken.
- Verbkette (Zug mit blauer Lok und gelbem Wagen, rote Kupplung): `verbkette-ohne-kupplung.svg` (can swim, nichts dazwischen), `verbkette-kupplung-to.svg` (would like, rote Kupplung to, swim), `verbkette-skala.svg` (Skala fest bis offen: must, should, could, might). Szenen: `szene-schilder.svg` (Seite 1), `szene-wochenende.svg` (Seite 2), `szene-cafe.svg` (Seite 3), `millbrook-klassenzimmer.svg` (aus hello-millbrook kopiert, bisher auf keiner Seite eingebunden). Die Figur zeigt die Form, nie die Lösung einer Aufgabe; die Bildunterschrift sagt, worauf man schaut, `alt` beschreibt die Kette.
- Szenen: `szene-<thema>.svg` mit den Figuren aus hello-millbrook; Beschriftungen innerhalb des `viewBox`; jede Figur funktioniert bei 360 px.
- Tabelle „Klassenzimmer-Poster · Modalverben“ (Ausdruck · Bedeutung): Seite 1 can, can’t, must, mustn’t, needn’t; Seite 2 dazu could, may, might, should (ausgewählte Zeilen von Seite 1 plus die neuen). Seite 3 hat „Klassenzimmer-Poster · Höfliche Wünsche“ mit I’d like. Sie steht nie direkt über der Übung, die sie beantwortet.

## Sources

Karte `https://lernapps.net/apps/map/englisch.json` und die drei Baustein-Seiten (geöffnet 2026-11-21), Issue #480, Konventionen #489, Muster hello-millbrook. Grundwortschatz `https://lernapps.net/apps/map/englisch/grundwortschatz/` (geöffnet 2026-11-21): alle Übungswörter stehen in A1, nur *German* in A2; die Kurzformen can’t, mustn’t, needn’t und I’d sind keine eigenen Listenwörter. Kapitel 2 und 3: Texte sind eigene erfundene Szenen der Figuren, die Grammatik ist Standardgrammatik ohne zitierte Quelle; Fakten über die reale Welt stehen nicht in den Lesestücken. Wörter über A2 im Randglossar der Seiten (nicht gegen die Liste einzeln geprüft: invite, wrap, deliver, speaker, stall, collect, candle, dictionary, worried). Wörter außerhalb von A1, auf den Seiten erklärt: *German* (A2), *might* und *should* (A2); *tennis*, *cinema* und die übrigen Übungswörter stehen in A1 (geprüft 2026-11-21). Draußen bleiben bewusst: Kurzantworten (Yes, I can. / No, I can't.), Verneinung von should, could und would (shouldn't, couldn't, wouldn't) und die Frage nach Erlaubnis mit may; sie folgen in einem späteren Ausbau. Ungeprüft: Wikipedia (HTTP 429), deshalb nur Standardgrammatik ohne Zitate. Die Grammatikfakten (Modalverben ohne -s und ohne to, needn’t, mustn’t, I’d = I would) sind Standardgrammatik, keine zitierten Sätze. Audio: KI-Stimme britisch weiblich, erzeugt mit Skill `lernapps-audio`, als KI-generiert markiert. Millbrook School ist erfunden. Material des Erstellers: keines.

## Adding a chapter or round

1. Baustein auf der Karte wählen (Voraussetzungen müssen auf früheren Seiten stehen). Kapitel 2 und 3 stehen im Issue #480; sie kommen als Inkrement auf einem eigenen Branch `increment/<NN>-<name>`.
2. Kapitelordner `src/<kapitel>/` mit `chapter.yaml` anlegen, in `src/app.yaml` unter `chapters` eintragen; Seiten `<seite>.yaml` mit den Abschnitten `einstieg`, `neu`, `uebung`, `anwenden`, `weiter` und der Competency-ID.
3. Die Verbkette um die neue Kupplung erweitern (Kapitel 2: to und -ing, Kapitel 3: be + 3. Form); Tabelle „Klassenzimmer-Poster · …“ um die Zeilen der Seite ergänzen.
4. Übungen aus den Mustern oben, je mit `mistakes` und `hint`; 1 bis 3 in `selfAssessment` des Kapitels.
5. Hörtexte mit `regen_audio.py` erzeugen und anhören.
6. `npx --no -- lernapps check`, committen.

## Rules learned from mistakes

Übernommen aus hello-millbrook (Konventionen #489, Abschnitt 5):

- Übungen fragen nur Wörter ab, die vorher auf der Seite stehen (einfache A1-Wörter gelten als bekannt).
- Kein Hörsatz (Diktat, Nachsprechen) steht wörtlich oder fast wörtlich (nur Name getauscht) im Einstieg, Poster, Merke, Bildtext oder in einer Übung derselben Seite; ein Skript prüft das vor dem Push.
- Vorlage: `punctuation: ok` setzen (`hint` meldet auch bei richtiger Antwort „Achte auf die Satzzeichen“); `accepted` wirkt nicht, Varianten mit `(a|b)`; im Modus `choice` zeigt die App `mistakes` nicht, die Distraktoren sind echte Lernerfehler (-s-Formen, to nach Modalverb).
- Eine Tabelle, die eine Übung beantwortet, steht nicht direkt darüber.
- Englische Aufgaben enthalten kein deutsches Wort.
- Gleichwertige richtige Antworten mit `(a|b)` zulassen; `case: wrong` nur dort, wo die Seite Großschreibung unterrichtet.
- Audio: das Ausklingen am Satzende abschneiden (`regen_audio.py`); Namen am Satzende zweisilbig.
- Bilder: Beschriftungen innerhalb des `viewBox` halten.
