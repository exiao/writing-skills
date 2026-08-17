# Deck slop: a worked session of real cuts

Every line below was written by an AI (me), shipped into a real conference deck, and then cut
by Eric during one editing session. The cuts are grouped by the pattern they share. Use this
file when writing or reviewing slides, step lists, chart captions, and any surface where text
sits beside a visual.

The through-line: **on a slide, the visual is the evidence. Prose that narrates the visual is
always the thing to cut.** Nearly every failure below is a sentence doing a job the chart,
the number, or the title already did.

---

## 1. The narrator caption (telling the reader what the chart says)

The chart is right there. A sentence restating it makes the reader parse the same fact twice.

- CUT: "Top of the list: pick anything, they all get there. Bottom: the choice decides whether
  you ship a bug. The question is not which model is best. It is where your job sits on this
  list." → slide is now title + chart, nothing else.
- CUT: "Kimi wrote 2,049 words and got 10 of 14. Opus wrote half as much and got 14." → the
  bar chart already plots words against score. Kept only the conclusion the chart cannot
  draw: "Longer answers were not better answers, and they cost you the time to read them."
- CUT: "Two models started killing on a number that does not exist." → the card above it
  already quotes the model saying *"Kill the other 40 ads immediately."*

**Rule:** a caption may state the *conclusion* the visual cannot draw. It may not restate the
data the visual already shows. If your caption's facts are all readable off the chart, delete it.

---

## 2. The announcement slide (a slide whose only job is to say a slide is coming)

- CUT, whole slide: "I ran the eval. Here is the whole answer on one slide." → the next slide
  *was* the answer. The transition slide announced a result the audience was one keypress from
  seeing.
- CUT: "Three questions, in order. Stop at the first no." → sitting under the title
  "How to decide on a model" above three numbered questions. The numbers say "in order."

**Rule:** if a line describes the structure the reader can already see (three items, a list,
what comes next), it is scaffolding left in after the build. Numbered items announce their own
order. Charts announce their own existence.

---

## 3. The restated trailer (echo gloss)

Covered in WRITING-STYLE.md under Structural Slop. Examples from this session:

- CUT: "Collect five decisions you already made this month. **Real numbers, not toy examples.**"
- CUT: "Write the answer key. **What actually turned out to be true, before any model sees it.**"
- CUT: "Not the leaderboard's tasks." from "Not the leaderboard's tasks. If you cannot answer
  this, the rest is noise."
- KEPT: "Run it a week. If you never reach for it, you have your answer." The trailer adds a
  decision rule, so it earns the second sentence.

---

## 4. The setup that delays the point

The sentence before the good sentence, doing nothing but clearing its throat.

- CUT: "Neither looks like a failure. Both are fast, confident, well formatted." Kept: "That is
  why a benchmark score cannot warn you."
- CUT: "Availability is a capability." Rewritten to "Showing up is a feature," which is the
  same idea without the abstract noun pair.
- CUT: "Twenty words, instantly. Next run, that rule throws away the user's own correction."
  Kept: "This job runs at 1am with nobody watching." The kept line is the stake; the cut line
  re-explained the quote directly above it.

**Rule:** find the strongest sentence in the block, then check whether everything before it is
just walking up to it. Start at the strong sentence.

---

## 5. Autobiography where the audience needs a rule

Detail that is true, specific, and about the author rather than the reader.

- CUT: "My own system prompt says VERIFY BEFORE CLAIMING in capital letters. On this model that
  line is now costing me money." → kept only the link to the prompting guide.
- REPHRASED: "At 1am it reads yesterday's sessions and traces, decides what you will need to
  remember, and rewrites your memory while you sleep." → "You trust it to do work in the
  background on a schedule, such as nightly memory cleanup, or a daily fetch of new jobs to
  apply for." The first version is a tour of the author's setup. The second is a category the
  listener can put their own job into.
- REPHRASED: chart label "memory-gc, 1am daily, nobody watching" → "Run it on a schedule."

**Rule:** specificity earns its place when the reader can act on it. A specific detail about
*your* config that they cannot copy is decoration. Name the category, then give your instance
as the example if there's room.

---

## 6. Titles that describe the slide instead of making a claim

- "The whole result" → **"Some examples."** The first oversells; five tasks is not the whole
  result of anything.
- "The two that split the field" → **"Wrong answers only."**
- "Both wrong answers look like decisiveness." → **"LLMs are confidently wrong."** Shorter,
  and it states the general law instead of describing the two cards below it.
- "Fourteen checks. I wrote them before I ran anything." → **"Our AI-generated eval."** The
  original was a process brag; the checks are visible in the chart.
- "Build the same thing in an afternoon." → **"Build your evaluation suite in an afternoon."**
  "The same thing" points backward at the speaker's work. The fix points at the listener's.
- "Five real tasks beat any leaderboard." → **"You can ask your AI to do your vibe check."**
  The original restates the deck's thesis at the audience. The fix hands them an action.

**Rule:** a title should make a claim, name the thing, or hand over an action. "The whole
result" / "The two that split the field" are table-of-contents entries, not titles. Test:
would this line survive as the only text on the slide?

---

## 7. Jargon the four-word explanation cannot save

Cut in favor of plain words that a PM audience reads without stopping.

| Cut | Kept |
|---|---|
| "cache key," "the limit in the key" | "The saved copy is labelled by user but not by how many rows were asked for" |
| "delivery floor," "attribution," "retrieve" | "the tracking broke," "nothing out there mentions us" |
| "Nothing in that diff is an attack. It is a cache lookup." | "Nothing in that code is an attack. It saves a copy of a database result." |
| "that lane does not parallelize" | "the queue in front of me gets longer" |
| "Availability is a capability" | "Showing up is a feature" |

**Rule:** on a slide the reader cannot pause to decode. If a term needs a gloss, it needs a
replacement.

---

## 8. The verbless noun-list fragment

Eric caught this one himself, and it is the sharpest tell in the whole file: **the fragment has
no verb.** It is a comma-separated pile of nouns wearing the rhythm of a sentence.

- CUT: "New quirks, new prompts, new failure modes. That is the real price." →
  "You relearn its quirks, retune your prompts, and meet new failure modes."
- Note what happened to the trailer. "That is the real price" existed only to supply the verb
  the fragment never had. Fix the fragment and the trailer deletes itself. These two patterns
  travel together.
- Same shape found elsewhere in the deck: "Same feature, same skills, same harness." /
  "Ten panels, a validity gate, three judge families, a frozen test set."
- The repeated head word (new / same / no / every) is the fingerprint. It gives the list a
  cadence that feels composed, which is exactly why it slips past a read-aloud check.

**Exempt:** labels and captions under charts and headshots ("VP of Product, Series C"), dates,
credits, table cells, code. Those are labels, not prose. The tell only fires where a sentence
was intended.

**Rule:** ask "where is the verb?" If a comma list of noun phrases has none, name an actor and
give them something to do.

---

## The single test that caught most of these

Cover the sentence with your thumb. If the slide still delivers the same fact, the same number,
the same instruction, and the same stake, the sentence was never doing work. Length is not the
signal. Two of the worst offenders here were under ten words.
