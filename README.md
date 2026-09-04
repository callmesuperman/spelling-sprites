# Spelling Sprites

A spelling practice app for a 9-year-old, built as a single self-contained HTML
file. No build step, no dependencies to install, no server required. Photograph
this week's spelling list, check the words, and practise them in a loop designed
around what actually makes spelling stick.

## Two ways to run it

**As a hosted page (recommended).** Enable GitHub Pages on this repo —
Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
The app appears at `https://<your-username>.github.io/<repo-name>/` a minute
later. On the phone, open that URL and use *Share → Add to Home Screen*; it then
launches full-screen like an app.

**As a plain file.** Download `index.html`, open it, done. Everything runs
locally.

Either way the data lives in that browser's local storage on that device. The
two are separate origins, so progress does not transfer between them — move it
with Export / Restore in Grown-ups.

## Getting the spelling list in

The list her teacher sends home is the assignment, so every route ends at the
same place: exactly those words, checked by you, and nothing added. Five routes,
under **Words → Add**:

- **Photo** — the default. Take a picture of the list and the app reads it on
  the device. The image is converted to grayscale, contrast-stretched and
  upscaled before it is read, which makes a real difference on a phone snap of a
  printed handout. It downloads its OCR engine the first time, so it needs a
  connection once.
- **Paste** — better for handwriting. Photograph the list, open it in Photos,
  tap the text-select button, drag over the words, *Copy*, then paste here.
  Apple's Live Text reads handwriting far better than any in-browser OCR.
- **Speak** — for when there is no list to photograph. Tap the microphone and
  say the words one at a time; each one appears as a chip you can remove. Note
  that dictation writes the *common* spelling of what it hears, so it cannot
  tell **their** from **there** — check every word on the next screen. If the
  browser cannot listen, use **Type** and the microphone key on the iPhone
  keyboard, which is the same dictation by another route.
- **Type** — one word per line.
- **Build** — the app writes the list itself, to boundaries you set: how many
  words, which grade level (2–5 or mixed), and which spelling rule to focus on.
  It draws from a built-in bank of 472 words, never picks a word already in one
  of her lists, and widens the grade band on its own rather than silently
  returning a short list. A rule-focused list is the one worth choosing —
  twelve words that share a pattern teach a rule that transfers; twelve
  unrelated words are twelve things to memorise. Homophones generate in proper
  sets (there / their / they're together), because that is the only way they
  teach anything.

All five land on the same review screen. **Check the words there.** Headers
like "Spelling List Week 5", "Name:" and list numbering are stripped
automatically, and any word in the built-in bank of 472 common grade 2–5 words
arrives with a sentence already attached. A word saved with a typo gets
practised with the typo, so this screen is not optional.

## Practice uses this week's list and nothing else

The most recently added list is marked **practising**, and practice draws only
from it. A word from an older list is never quietly mixed in, and the built-in
word bank is only ever used to *suggest* a list under **Build** — it never adds
words to a list you scanned, pasted, spoke or typed.

To switch weeks, open a list and tap **Practise this list**, or use *change* on
the home screen. Adding a new list makes it the active one automatically, which
is usually what you want on a Monday.

There is a trade-off worth knowing. Spelling decays without review, and locking
practice to the current week means last week's words stop coming back. If you
would rather she kept older lists warm at the cost of spending part of each
session off this week's test, turn on **Also review older lists** in
Grown-ups → Settings. It is off by default, because the weekly test is the
thing that actually has a deadline.

## How much each session covers

**Grown-ups → Settings → Each session covers** has two modes.

**The whole list, every time** is the classic weekly routine: all twelve words
come up in every session, cover the list daily, test on Friday. Each word still
appears at whatever level it has reached, so a word she has never met is
introduced properly while one she nearly owns is straight dictation. Twelve
words is roughly a six to nine minute session.

**A few words at a time** is the adaptive default: the app picks what is due
plus a few new ones. Gentler, but a twelve-word list takes several sessions to
introduce, and the list screen will warn you when that runs past the test date.

Either way the box rules are untouched — seeing a word more often does not
promote it faster, because promotion past box 2 still requires a correct answer
on a different day. Over a Monday-to-Friday week in whole-list mode a word
reaches box 4; mastery lands the following Monday.

## How practice works

Every word carries a Leitner box, 0 to 5. A session mixes words that are due
with at most a few new ones, and the amount of support on screen depends on how
well she knows the word:

| Box | Stage | What she sees |
|-----|-------|---------------|
| new | Meet the word | Word, sound chunks, the spelling rule, read aloud — then she copies it |
| new | Fill the gaps | Word with half its letters hidden |
| 1–2 | Look, cover, write | Word shown for four seconds, then hidden |
| 3+  | Listen and spell | Audio only — word, sentence, word again |

Wrong answers are never just marked wrong. She sees her attempt with the wrong
letters struck through, the correct word with the fixed letters highlighted, the
rule that governs it, and then has to write it correctly before moving on. That
word also comes back later in the same session.

Reviews expand across days: 1, 2, 4, 7, 14. **Past box 2 a word can only be
promoted on a different day**, so mastery takes at least five separate sessions
on separate days and cannot be manufactured in one long sitting.

Two side games unlock as words get solid: **Speed Sprint** (60-second fluency
round on words she already owns) and **Pattern Sort** (group words by the rule
they follow).

Gems are awarded when a word actually becomes durable — one when it reaches box
3, two more at mastery, one for finishing a session — and five gems hatch one of
24 sprites. Rewards track real progress rather than time spent, on purpose.

## Weekly lists and the Friday test

A list can carry a **test day** (it defaults to the coming Friday). That changes
three things:

- Nothing is ever scheduled past the test. A word that would normally be parked
  for fourteen days gets pulled back to the test date instead.
- As the test approaches, that list's shakiest words jump the queue — within
  three days, they are pulled into practice even if the schedule had not
  surfaced them yet.
- The home screen shows a countdown and how many of the words are actually solid.

The list screen also does the arithmetic: at 3 new words a session, a 12-word
list takes 4 sessions to introduce. If that is more sessions than there are days
left before the test, it says so and tells you to raise *new words per session*
— otherwise she meets some of the words for the first time on test day.

## The research behind the design

- **Self-corrected testing.** Test, compare against the correct form, fix it
  immediately. Horn (1947) on spelling instruction; Schoephoerster (1962) on
  test-study plans. This is the core loop, not a feature.
- **Cover-Copy-Compare.** Long-standing evidence as a low-cost spelling
  intervention — Skinner, McLaughlin & Logan (1997) review. The middle scaffold.
- **Retrieval over rereading.** Roediger & Karpicke (2006). Only unsupported
  retrieval moves a word forward; copying a visible word does not count.
- **Distributed practice.** Cepeda, Pashler, Vul, Wixted & Rohrer (2006). Hence
  expanding intervals and the different-day rule.
- **Pattern over rote.** Bear, Invernizzi, Templeton & Johnston, *Words Their
  Way*. Every word is tagged with its orthographic pattern; a rule transfers to
  words that were never on the list.
- **She is never shown a misspelling.** Reading an incorrect spelling measurably
  degrades later accuracy (Brown, 1988; Jacoby & Hollingshead, 1990). There is
  deliberately **no "pick the correct spelling" game** here, though nearly every
  spelling app has one. The only wrong spelling she ever sees is the one she just
  wrote, on the compare screen, which is the mechanism self-correction depends on.
- **Rewards follow mastery, not activity.** Deci & Ryan; Lepper, Greene &
  Nisbett (1973) on over-justification.

These are summarised in-app under **Grown-ups → Method**.

## Notes for editing

`index.html` has four sections, each behind a banner comment: CSS in `<style>`,
then markup, then the modules (`LEX`, `ART`, `SPEAK`, `HEAR`, `SFX`, `OCR`),
then the application logic.

- **Sprites are generated, not stored.** `ART` draws all 24 creatures with one
  renderer from the `SPRITES` parameter table — body shape, topper, pattern, eye
  style and a three-colour palette — so stroke weight, proportion and style stay
  consistent automatically and 24 creatures cost a few hundred bytes. Body
  outlines come from `blob()`, a wobbly closed spline, which is why none of them
  look like plain ellipses. Add a row to the table to add a sprite.
- **Word analysis lives in `LEX`.** `chunks()` splits a word for writing:
  affixes first, then VCCV, then VCV, keeping digraphs and a final silent e
  intact. English cannot be syllabified reliably without a pronunciation
  dictionary, so this is a *writing aid* and is approximate by design — it
  returns the whole word whenever it is not confident. `PATTERNS` is the rule
  table; each entry needs a test, a label, and a child-facing explanation.
- **The word bank** (`BANK_RAW`) is 472 common grade 2–5 words in
  `word|sentence|grade|flags` form, where flags mark homophones (`h`) and
  compound words (`c`). It does double duty: a scanned word matched against it
  gets a sentence for free, and `generate()` builds lists from it. Add rows to
  extend it; a pattern needs 10+ matching words before it is offered as a focus.
- **Pattern tests are conservative on purpose.** CVCe alone over-claims silent
  e — *sure*, *measure*, *machine*, *have* and *give* all fit the shape without
  the e doing a magic-e job — so `NOT_MAGIC_E` excludes them, along with
  anything ending `-ure`. Likewise a trailing `-er` is stripped before the
  bossy-r test, so *teacher* and *water* do not end up in a list beside *star*
  and *first*. If you add patterns, err the same way: a wrong rule is worse than
  no rule.
- **`practicePool()` is the exclusivity guarantee.** Everything that chooses
  words — `dueWords()`, `freshWords()`, the session builder — goes through it,
  so there is one place to look if a word ever appears that should not have.
- **`HEAR` restarts itself.** Safari ends a recognition session at every pause,
  so `onend` starts it again while the user still wants it listening; it stops
  for good on `not-allowed`, and whenever the add flow is left.
- **Speech** uses the browser's own voice, so it works offline once cached. iOS
  will not speak until a real user gesture has happened, which is what the
  first-touch primer handles. If audio fails there is a "Can't hear it?" link
  that reveals the word — and an attempt made with the word visible is recorded
  as practice but deliberately does **not** advance the schedule.
- **Colours** are CSS custom properties in `:root`. Body text uses `--muted`,
  which is 6.1:1 on the background. Don't lighten it past 4.5:1.
- **Storage keys** are prefixed `spell.` so they can't collide with the workout
  apps on the same `github.io` origin.
- **Autocorrect is disabled** on every answer box (`autocorrect`, `autocapitalize`,
  `spellcheck` all off). If that ever gets dropped, iOS will silently fix her
  spelling and the app stops measuring anything.

## Settings worth knowing

Under **Grown-ups → Settings**: her name, how much each session covers, reading
speed, sound, rule hints, whether to review older lists, and larger text. In the
adaptive mode the two number fields underneath control session size and how many
new words are introduced at once; they are hidden in whole-list mode because it
uses neither.

**Export regularly.** The data exists only in local storage, so clearing site
data or browsing history wipes it.
