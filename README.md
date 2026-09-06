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

**The whole list, every time** is the classic weekly routine: every word on the
list comes up in every session, cover the list daily, test on Friday. Each word
still appears at whatever level it has reached, so a word she has never met is
introduced properly while one she nearly owns is straight dictation.

List length is not capped anywhere — 12, 20 or 30 words all work, and the home
screen shows an estimate of how long the session will take so a long list is
not a surprise. The first day is always the longest, because every word is
being introduced; it drops by a third once they are familiar:

| Words | First session | Later sessions |
|-------|---------------|----------------|
| 12    | ~11 min       | ~7 min         |
| 20    | ~18 min       | ~12 min        |
| 30    | ~27 min       | ~18 min        |

Past about fifteen minutes the list screen suggests either splitting it into two
goes with a break, or using the adaptive mode with *new words per session*
raised instead. Both are fine; a long unbroken sitting is the thing to avoid.

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

**Grown-ups → Settings → Before she spells a word** decides whether she ever
sees it first.

**She only hears it (Grade 3 and up, the default).** The word is never on screen
before she attempts it. She hears it read in a sentence, can replay it — either
the whole sentence or *just the word*, said slower — types her answer, and only
then does the spelling appear. Attempting first and being corrected immediately
beats studying first: the pretesting effect (Richland, Kornell & Kao, 2009)
holds even when the first attempt is wrong, as long as the correction follows
straight away, which it does. It is also simply how the real test works. A word
she has never met is labelled *New word — have a go* and tells her the spelling
comes up right after, so a wrong first guess is framed as expected rather than
as failure.

**Show her the word to copy (Kindergarten to Grade 2).** The older ladder, for a
child still learning letter shapes rather than spellings:

| Box | Stage | What she sees |
|-----|-------|---------------|
| new | Meet the word | Word, sound chunks, the spelling rule, read aloud — then she copies it |
| new | Fill the gaps | Word with half its letters hidden |
| 1–2 | Look, cover, write | Word shown for four seconds, then hidden |
| 3+  | Listen and spell | Audio only — word, sentence, word again |

Either way, the moment she has answered, the correct spelling appears along with
its sound chunks and the rule behind it.

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

## Handwriting

The test at school is written by hand, and forming letters is motor learning
that typing does not touch. **Grown-ups → Settings → Handwriting** has three
states:

- **Off** — typing only.
- **Offered, but she can skip it** — the default.
- **Required — type it, then write it** — she writes a spelling she has already
  got right, so the pen never practises a mistake.
- **Required — write it first, then type it** — she hears the word, writes it
  from memory, then types the same word. Closest to the real test: the writing
  is a genuine attempt rather than copying. The typed answer is still what gets
  marked, because it is the one that can be checked reliably, and the correct
  spelling appears afterwards so she can compare her writing against it.

It comes *after* she has already typed the word correctly, so she is only ever
practising the right letters. She writes with a finger on ruled guide lines —
top line, dashed x-height, a darker baseline to sit the letters on — then the
correct spelling appears above what she drew and she says whether it matches.
Saying "not quite" gives her one rewrite with the word visible to copy, then
moves on rather than trapping her.

**Turn the phone sideways for a much bigger area.** In landscape the writing
screen becomes two columns — the pad takes the full height on the left, the
prompt and buttons sit beside it — which is about 2.6x the writing area and a
shape that actually suits a word. Strokes are stored as proportions rather than
pixels, so rotating mid-word keeps what she has already written.

**What the app checks automatically.** When she taps Done, the stroke geometry
is analysed and she gets immediate feedback: how many separate letter shapes she
drew versus how many letters the word has, whether the letters sit on the
baseline or float above it, and whether any are wildly out of size. So writing
three shapes for *caught* comes back as "That looks like 3 letter shapes, and
this word needs 6. Count them as you write." The findings are also recorded per
word for the parent view.

**It does not read the word, and no browser choice changes that.** Every browser
on iOS — Chrome and Firefox included — is required to use Apple's WebKit engine,
so they all expose exactly the same web APIs as Safari. The W3C Handwriting
Recognition API is a Chromium feature and is not available in any iOS browser;
switching browsers would gain nothing and would cost the clean Add to Home
Screen install, which is a Safari strength. Cloud recognition (Google Vision,
Azure, MyScript) would work but needs an API key, and in a single client-side
file that key is public to anyone who views source — it would also mean sending
a child's handwriting to a third party and running a proxy server to hide the
key, which is the whole no-server design gone. A model small enough to embed
would misread a child's finger-writing often enough to be worse than useless — marking a
correctly written word wrong would do real damage to a child who already finds
spelling hard. What stroke geometry *can* measure reliably is letter formation,
which is the reason to write by hand in the first place. The final say stays
with her own comparison against the correct spelling, which is the mechanism
Cover-Copy-Compare uses on paper anyway.

For the same reason the self-check does **not** move a word up or down its
Leitner box — a child's self-report is not evidence, and the schedule stays
driven by the typed answer, which is graded objectively. The self-checks are
recorded and shown to you instead, under Grown-ups → Progress → *Her
handwriting*, along with the most recent sample of each word as she drew it and
what the automatic check found — "fewer shapes than letters", "letters off the
line", "uneven sizes". Letter reversals still need your eyes; the app cannot see
those.

Handwriting adds roughly 25 seconds a word (32 when she writes first), which the
session estimate accounts for: a 20-word list is about 18 minutes typing only, and about 28 minutes with
handwriting required. That is a long sitting — splitting it into two goes is
usually better than pushing through.

Samples are stored as small JPEGs, one per word, about 3 KB each. If the browser
ever runs out of storage the samples are dropped rather than her progress.

## Stopping part way through

A twenty-word list is a long sitting, so a session does not have to be finished
in one go. The ✕ during practice shows a score card — how many words she got
through, how many she got right, how many are left — and offers **Keep going**
or **Stop here**. Stopping banks the gems she has already earned, counts the day
towards her streak, and saves the rest of the session.

Next time, the home screen offers **Carry on — 7 words left** instead of Start
practice, and picks up exactly where she stopped rather than restarting the
list. *Start the list again instead* is there if you would rather. Finishing a
list clears the saved remainder, and so does switching to a different week's
list — a new week always starts fresh.

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
then markup, then the modules (`LEX`, `ART`, `PAD`, `SPEAK`, `HEAR`, `SFX`,
`OCR`), then the application logic.

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
- **`PAD` stores strokes, not pixels.** Each stroke is an array of points and
  the canvas is redrawn from them, which is what makes undo and the guide lines
  work. Only a 300px JPEG is ever persisted, via `keepShot()`, which rolls back
  and purges every sample if the write throws a quota error.
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
