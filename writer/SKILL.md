---
name: writer
description: "Write or edit content in Eric's voice: articles, blog posts, tweets, social posts, marketing copy, newsletters, landing pages, web copy. Enforces kill phrases. Use for drafting AND revision."
---
# Writer Skill

Write content in Eric's voice: articles, blog posts, tweets, social media posts, marketing copy, newsletter drafts, ad copy.

Not for docs, runbooks, error messages, plans, PR bodies, or agent prompts. Those want to
be flat and unmissable rather than persuasive. Use the `technical-writing` skill for them.
Mixed document, route per passage: a tagline inside a README is still voice writing.

## Ask before you write

Ask one question when you don't already know the answer: **who is this for, and where will
it be published?** The same product needs different copy for a hedge fund PM and an App Store
browser. Guessing wastes a draft.

Ask it once, in one line, then write. Don't stack a questionnaire.

Skip the question when the answer is already obvious: he named the surface (a tweet, the Bloom
paywall, a Substack post), he pasted a draft that shows its own audience, or the piece is a
revision of something you already scoped.

If the goal is unclear too, ask what the reader should think, feel, or do after reading it.

## Hard Bans (apply to every mode)

If you read nothing else in this file, read this.

**Never make up a fact.** Every number, date, name, and finding has to come from the source
or from something the user told you. Don't supply a plausible one to make a sentence land.
If you don't have the real one, write around it, ask, or mark it [NEEDS SOURCE]. This beats
every other rule here, including the pressure to be specific. A vague line that ships can be
fixed later. A wrong number that ships cannot.

When you're writing about a real page, event, or product, go read it first. Working off a
pasted excerpt loses the names and numbers, and that's exactly when the temptation to invent
one shows up. Where the source names something, use its name.

**Never fake a voice the author doesn't have.** If the draft has no "I", your version has no
"I". Don't add drama, urgency, or a contrarian turn the author didn't take. "Make this sound
human" means take out what sounds machine-made. It does not mean invent a narrator.

Those two are absolute. The rest are strong defaults:

**No sycophancy, ever.** These are the loudest AI tells left, and they read as satire now
(see @RhysSullivan: "You're absolutely right, that did kill your plants and that's my mistake").
- No apologies to Eric. Not "sorry", not "my mistake", not "my apologies". State what broke
  and what you're doing about it.
- No "you're absolutely right", "you're right", "great catch", "good question", "exactly".
  Just say the corrected thing.
- No "you hit the nail on the head", "spot on", "nailed it", "couldn't agree more".
- No opening a reply by praising the input at all. Answer first.
- No "that's on me", "I take full responsibility", "you're right to flag this",
  "great point", "honestly, this is a really important nuance".
- No damage-control theater: "I know you're frustrated", "let's start over",
  "I'd rather not spend this conversation apologizing", "this must be where the confusion
  came from", "that clears it up". Say what is true and what happens next.
- No offering a cheerful next step on top of a failure: "Want me to draft...",
  "Would you like me to...", "Let me know if you'd like me to iterate." Fix it or report
  the blocker.
- No reframing a loss as a win. "The weeds are dead" is not a result when the crop died too.

Source for the whole block: RhysSullivan's thread and its replies, Aug 12-13 2026. The
lines above are quoted from the parody, which means readers now recognize them on sight.

- No em dashes.
- No "delve," "leverage," "harness," "utilize," "cutting-edge," "game-changer."
- No "X isn't Y. It's Z." or "It's not about A, it's about B."
- No throat-clearing before the point: "Here's the thing:", "What made it work:",
  "The part nobody talks about."
- No fake-final endings: "That's it." / "Full stop." / "Period."
- Don't stack short fragments. Every sentence at 2-4 words with a period on the end reads
  as machine-made too. Join some clauses with commas so the rhythm moves.
- Don't explain the point you just made. If you wrote a good line, let it sit.
- Don't add a trailer sentence that only restates the one before it. "Collect five decisions
  you already made. Real numbers, not toy examples." The second sentence renames the first.
  Cover it: if no fact, number, or instruction is lost, delete it. Short does not mean earned.
- No verbless noun-list fragments. "New quirks, new prompts, new failure modes." has no verb,
  so nothing acts on anything. Ask "where is the verb?" If a comma list of noun phrases has
  none, give it one: "You relearn its quirks, retune your prompts, and meet new failure modes."
  Labels and captions are exempt; prose is not.
  **The descending-count triad is the version that slips through.** Three noun phrases
  each led by a number that shrinks: "Four jobs, three handoffs, one person." "Ten ideas,
  three prototypes, one ship." The arithmetic feels like an argument, so the missing verb
  goes unnoticed, and the line survives edits that kill plainer fragments. Aug 2026: it
  sat as a figure caption through four review rounds before Eric cut it. Two checks, run
  both: (1) where is the verb, and (2) strip the numbers, and if what is left is three
  bare nouns, there was never a sentence. Fix by naming who acts: "One person now does
  four jobs, and the three handoffs are gone." If the figure already shows the counts,
  delete the line instead.
- Don't pad a list to three items when the content only supports two. Three is the default an AI reaches for ("faster, cheaper, smarter"), so treat any triad as suspect and count the real reasons. Two or five is more often the truth.
- **Self-applause.** "And that matters." "That's the part everyone misses." "Which is exactly the point." The sentence praises the previous sentence instead of adding to it. Delete it; nothing is lost.
- **The minimizing tag.** A clause appended to a requirement to make it sound easy: "and that is all", "and that's it", "nothing more", "that's the only setup". It adds no fact and no instruction, it only editorializes that the requirement is small, which the reader can judge from the requirement itself. Aug 2026: "Your machine has to be on, and that is all." survived a full kill-phrase sweep because it carries no banned word; Eric cut it on sight. Delete the tag and keep the requirement: "Your machine has to be on." If the ease is genuinely the point, prove it with the count ("one toggle, no install"), never assert it.
- Cut every word the sentence survives without.

### Patterns the bans above miss

Added from petergyang/no-ai-slop after cross-checking this skill's references.

- **Colon reveals.** A noun phrase, a colon, then a dramatic lowercase payoff: "The best part: it learns." Write it as a plain sentence. Colons are for lists, labels, and quotes.
- **Weasel attribution.** "Experts agree," "studies show," "widely regarded as." Name the source or cut the claim. Never invent one.
- **The portability test.** If a sentence could move unchanged to another person, company, or product, it is filler. Replace it with a fact, number, mechanism, or judgment specific to this subject.
- **Fake-strong verbs.** "Serves as a centralized hub for" becomes "tracks." Prefer "is" and "has" when they are clearer.
- **Summary-recap endings.** "In conclusion," "Ultimately," "Overall," or a last paragraph that restates the piece. End on the last concrete point or the next action.
- **Negative listing.** "Not a X. Not a Y. A Z." Just say Z.
- **Rhetorical setups.** "What if I told you," "Think about it:," "Plot twist:," and self-answered question-then-answer pairs.
- **The definitional trailer.** A second sentence that classifies the first instead of adding to it: "That's the whole domain." "That's the job." "That's the difference." It carries no fact, number, or instruction, so it only announces that the previous line mattered. Delete it, or replace it with the concrete limit it was gesturing at ("It does not know what's worth building.").
- **Twinned definite articles.** Two sentences in lockstep, same shape, both opening with "The": "The slop factory ships ten features. The product factory kills nine of them." The parallelism does the persuading, not the content, and it reads as a slogan pair. Break the symmetry: join them with a comma, drop one "The", or give the second sentence a different verb and length. Named-entity contrast is fine; identical scaffolding is not.
- **The aphorism trailer.** An imperative followed by a general-truth sentence that
  justifies it: "Cap the codebase. Every line slows the next change." "Ship small.
  Big diffs hide bugs." The second sentence is unfalsifiable, unsourced, and would fit
  any product, so it fails the portability test. Keep the instruction, replace the
  proverb with the mechanism or the number: "Set a line cap per repo, so the agent
  rewrites instead of appends." If you have no mechanism, ship the imperative alone.
- **The comma that eats a preposition.** A phrase gets chopped at a comma to sound punchy, and the chop deletes the word that made it grammatical: "Ten features, nobody asked" (Aug 2026, a diagram label Eric renamed). The comma is standing in for "for", so the reader parses two half-clauses and reassembles them. Restore the word and drop the comma: "Ten features nobody asked for". Tell: read the fragment aloud and ask which preposition you supplied silently. Same shape in "Ten agents, nobody reviewed" and "Six weeks, nothing shipped".
- **The hedged range.** "5 to 10 minutes", "3-5x faster", "a few hundred to a thousand". A range where a real measurement belongs means nobody measured. Give the one number you actually observed ("7 minutes"), or say you don't have it. Ranges are fine when the spread is the point (a price band, a config limit).
- **The two-picture comparison.** "Less a hammer, more a scalpel." "Think less spreadsheet, more conversation." Two images, no instruction. The reader has to convert it back into advice you never gave. Say the action: "Use it on one file, not the whole repo."
- **The borrowed-brand analogy.** "It's the Excel of AI agents." "The Figma for X." It only lands if the reader knows both things well enough to map them, and usually they don't. Describe the thing itself. Allowed when the second brand is unmistakable to that exact audience and you still say what it does.
- **Formatting slop.** Emoji in headings, bold sprinkled mid-sentence, bullets where two sentences read better, headers over two-sentence sections.

### Detect mode

When Eric asks "is this slop?" or asks to audit or flag a draft without rewriting: name each
pattern that appears, quote the line, give the fix in a few words, and stop. Do not rewrite,
do not score, do not guess whether AI wrote it. Detectors guess; named patterns are evidence
he can check. Offer to edit after.

### Show the draft, don't paste it

For anything longer than a few paragraphs, or any page or deck, open the draft with the
`human-review` skill instead of dumping it into Signal. He edits lines himself and comments
on specific text, and the batch comes back as JSON. His `after` wording is final, carry it
verbatim.

## You can rewrite. You just can't make things up.

The two hard bans above are about facts and voice. They are not a ban on writing.

Rewriting, restructuring, cutting, and adding sentences are all fine. If the user asked you
to expand something, write more. If they asked you to fix something, fix it properly rather
than only deleting words.

The line is simple: don't hand back facts they never gave you, or a personality they don't
have. Everything else is your job.

## Don't over-edit

If you apply every rule at full strength you end up with even sentence lengths, no odd
words, and nothing out of place. That is what machine writing looks like. You'd be causing
the problem you're trying to fix.

Leave the strange word choice, the long sentence, the aside that isn't strictly necessary.
Fix what reads as machine-made, not everything that reads unusual. When a rule here fights
the author's actual voice, the voice wins.

## Wordy is not the same as machine-written

"Utilize", "in order to", "due to the fact that", "serves as", "boasts". These are just
wordy. Ordinary people write like this all the time. Tighten them, but they prove nothing
about who wrote it.

What actually signals machine writing is the shape: every sentence the same length, lists
padded to three, "not X, it's Y", a sentence whose only job is to announce the last one
mattered, and a warm closing line that says nothing.

So never point at a wordy phrase as proof something was AI-written.

Measurable versions of those shape problems: `references/structural-tells.md`.
Full guide, including voice fingerprints and structural slop: `references/WRITING-STYLE.md`.

## When to Use

Any time you're creating content that will be published or shared externally. This includes:
- Substack articles and blog posts
- X/Twitter threads and individual tweets
- Social media posts (LinkedIn, TikTok captions, etc.)
- Marketing copy and ad creative
- Newsletter drafts
- Typefully drafts
- Stakeholder-facing landing pages and product reports

Do NOT use for casual conversation, internal notes, or technical documentation.

## Three Modes

**Drafting mode** (Steps 1-5 below): Use when creating new content from scratch. Tweets, articles, ad copy, posts.

**Editing mode** (Editing & Revision section at bottom): Use when a draft already exists and needs autonomous refinement. Triggered by "edit this," "improve this draft," "run the editing loop," "evaluate and fix," or any request to revise existing content through the 6-dimension diagnostic framework.

**Marketing copy mode** (Marketing Copy Mode section below): Use for short promotional surfaces where there is no draft to refine and no article to write. Blurbs, event copy, ad copy, landing page headers, paywall lines, App Store text, subject lines.

If the user wants a first draft, use Drafting mode. If they hand you a finished draft and want it improved, use Editing mode. If the surface is short and promotional, use Marketing copy mode.

## Workflow (Drafting Mode)

### Step 1: Load the style guide
Read `references/WRITING-STYLE.md` in full before writing anything. It contains:
- Voice fingerprints (10 patterns that define the writing)
- Two writing modes: action-first (default) and framework (for technical depth)
- Style DNA: sentence structure, vocabulary, openers, transitions
- Kill phrases: banned patterns that must never appear
- Structural slop: subtler patterns to catch and cut
- Formatting rules: headers, links, bold, tickers, emojis
- Platform-specific rules (Twitter/X, long-form)
- Anti-patterns from past corrections

### Step 2: Identify the audience
If you don't know who is reading this, ask (see Ask before you write). Don't assume. The same product needs different copy for different audiences.

**Hedge fund / institutional PM ($1B+ AUM):**
- They have analysts. Position AI as augmenting their process, not replacing people.
- Trust is the bottleneck. They've been burned by ChatGPT hallucinations.
- Lead with process claims they can verify (citations, adversarial review), not taglines.
- Specific counts beat percentages: "35/36 claims traced to source" > "95% accuracy"
- Time-to-output matters: "40 minutes" tells them it fits their workflow.
- Radical honesty is credibility: admitting the 1 error out of 36 beats claiming perfection.
- Words that land: "adversarial", "sourced", "cited", "first draft"
- Words that repel: "AI-powered", "game-changing", percentages as hero stats

**Headline structures for sophisticated audiences:**
- Concrete object + unexpected modifier: "One-page memos with receipts"
- Process claim in two beats: "It cited the transcript. Then a second agent tried to break the thesis."
- Vulnerability-first: "35 of 36 claims traced to source. The 36th was wrong by $1.1B."
- Time + output: "40 minutes from ticker to cited memo"

### Step 3: Write the draft
- Default to action-first mode (concrete, short paragraphs, no throat-clearing)
- Open with something only the author could write
- Use specific numbers, real examples, real screenshots
- Weave links inline, never as a references section
- Vary paragraph length. Break metronomic cadence.
- Write so that: only Eric could have written it; every paragraph has a reason it exists; it reads aloud naturally with no AI cadence; it sounds like Eric talking to a friend.

### Landing-page copy reviews
When reviewing a website for investor, customer, or sales copy, do not stop at prose if the user asks for visual before/after. Pair the copy plan with a concrete page architecture: hero thesis, proof strip, before/after panels, diagrams that explain the strategic argument, copy replacement table, and final CTA. If asked to make it shareable, use the frontend-design workflow and deploy a polished static page rather than sending only text.

### Step 4: Kill phrase sweep
Before delivering, scan the draft against the Hard Bans at the top of this file: no em dashes; no delve/leverage/harness/utilize/cutting-edge/game-changer; no "X isn't Y, it's Z"; no setup phrases; no manufactured drop endings; no fragment-stacking; no interpretive sentences; no decorative triads. Then scan for every pattern in the Kill Phrases and Structural Slop sections of `references/WRITING-STYLE.md`. Rewrite any matches. This is not optional.

## Pitches and blurbs that link to a real artifact
When the copy links to something the reader can open (a repo file, skill, doc, demo, dataset) and the reader is knowledgeable, every claim in the pitch must match what the artifact actually contains. Before sending, verify each enumerated feature/step against the linked file. Do not pad a numbered list with steps the artifact doesn't perform, and do not rename a concept (e.g. "synthetic dataset" when the artifact uses real production cases). A single mismatch makes the whole pitch read as padded, or the repo as stale, to an expert reader. If a claimed step isn't in the artifact, either cut it or wire it into the artifact for real before linking. Credentials and specificity do the persuasion; let the list stay accurate and short.

## Key Rules (quick reference)
- No sycophancy: no apologies, no "you're absolutely right", no "you hit the nail on the head"
- Write with your eraser. Every word you can remove makes what's left stronger. On every draft, do a pass where you try to delete each word, phrase, and qualifier: if the sentence still says what it needs without it, it goes. Weak intensifiers (very, really, quite), hedges (somewhat, fairly), "in order to", stray "that"s, and any word the sentence survives without are all cuts. Shorter is not the goal; stronger is, and cutting is how you get there.
- No em dashes
- No "delve," "leverage," "harness," "utilize," "cutting-edge," "game-changer"
- No formulaic contrasts ("X isn't Y. It's Z.")
- No setup phrases ("What made it work: ...")
- No manufactured drop endings ("That's it." / "Full stop.")
- No staccato fragment-stacking (every sentence 2-4 words capped with a period, no commas). Join clauses with commas so rhythm varies.
- No interpretive sentences ("That's the power of AI.")
- Specific numbers over vague claims, when you have a real one. Never invent one to fill the slot (see Hard Bans)
- Show the work, don't claim the conclusion
- Bold claim then immediate vulnerability when making strong assertions
- Use "we/let's" to bring the reader along, not "you should"

## Finance / Investing Copy
When writing Bloom or investing marketing copy, sell research clarity and risk awareness, not guaranteed outcomes.
- Prefer: "second opinion," "red flags," "what to pay attention to," "with the receipts," "research any stock," "understand why prices move."
- For Bloom vigilance/watchdog copy, use concrete jobs the user already understands: "Bloom watches the market so you don't have to," "Your investing watchdog," "Get a second opinion before you make a trade," "What moved, why, every morning," "Get the full story on any stock," "Catch red flags before they cost you," and "Comes with receipts."
- Avoid internal product jargon as hero copy. In particular, do not lead with "It watches. You get the tap." or "tap" as the payoff. "Tap" is a notification mechanic, not a user-language benefit.
- Avoid: "hidden investing opportunities," "pick winning stocks," "avoid losses," "boost returns," "no hallucinations," "latest AI models" as a primary benefit.
- Convert hype into concrete user anxiety: "$5,000 decisions shouldn't be guesses," "Your portfolio deserves more than 6 minutes of research," "What would prove me wrong?"
- Add a lightweight disclaimer for paywalls/landing pages: "for research, not financial advice."

## Bloom and BloomBot conversion copy

## Marketing Copy Mode

For short promotional surfaces: blurbs, event copy, ad copy, landing page headers and subheads, paywall lines, App Store text, email subject lines, social promos.

**Precedence, state it and follow it:** this skill owns voice and phrasing. The `copywriting` skill owns structure and section order (what blocks a landing page has, what order they run in, what each block must accomplish). On conflict, writer wins on voice: keep copywriting's structure, rewrite its words. Never ship a line that clears a copywriting template but violates a Hard Ban above.

For positioning and angle selection (which frame the copy expresses), use the `positioning-angles` skill first. Writer executes the chosen angle, it does not pick it.

**How to work:**
1. Name the surface, the reader, and the one action the copy is asking for. One action per surface.
2. Take the angle from positioning (or ask for it). Do not invent a new angle inside the copy.
3. Write 3-5 options per slot, not one. Short promotional copy is a selection problem, not a drafting problem.
4. Lead with the concrete consequence or the specific number. Cut every adjective the sentence still works without.
5. Keep character counts in view for constrained surfaces (App Store, ads, subject lines) and print them beside each option.
6. Run the Hard Bans checklist below on every option before presenting.
7. Billboard test on every option you keep: would this line survive alone on a
   billboard, with no surrounding page to explain it? And can the reader repeat the
   promise back after one read? Fail either, cut or rewrite it. Do not pad it.

**Before you output anything, re-check:** no em dashes; no delve/leverage/harness/utilize/cutting-edge/game-changer; no "X isn't Y, it's Z"; no setup phrases; no "That's it." endings; no fragment-stacking; no interpretive sentences; no decorative triads. A violation in a two-word headline is more visible than in a 2,000 word essay, not less.

## Platform Notes

**Twitter/X:** Hook in first tweet. Each thread post stands alone. Screenshots as proof. Light self-deprecation. Links in replies not main tweet.

**Long-form:** Open with a specific moment. Walk through a real example end to end. Name real companies, tickers, numbers. Close with an action, not a platitude.

**Slides and decks:** The visual is the evidence, so prose that narrates the visual always goes. Do not caption a chart with facts readable off the chart, state only the conclusion it cannot draw. Do not write a slide whose job is to announce the next slide. Titles make a claim or hand over an action, never describe the slide ("The whole result", "The two that split the field" are contents-page entries, not titles). No term the reader must pause to decode. Worked examples of all seven patterns: `references/deck-slop-cuts.md`.

**Typefully drafts:** Follow the content pipeline conventions. Tag the correct social set ID.

## Editing & Revision (Editor-in-Chief Mode)

When a first draft is complete and needs autonomous refinement (especially for Substack articles after Phase 1 gates: topic, title, outline, draft), run the diagnose-prescribe-rewrite loop.

### Six Dimensions

Scoring rubric lives in the `evaluate-content` skill, Classification Mode. Load it to
score, then come back here to fix. Do not restate its criteria.

Classify each as STRONG / NEEDS WORK / WEAK:

| Dimension | What to check |
|-----------|--------------|
| Shareability | 2+ screenshot moments? Would someone forward this? |
| Substance | Every claim backed by data, examples, stories? |
| Voice | Sounds like Eric? No AI tells, no dramatic contrast slop? |
| Leanness | Every sentence earns its place? No filler? |
| Emotion | Driving emotion clear and felt throughout? |
| Rhythm | Varied sentence lengths, good tempo shifts? |

### The Loop

0. **Scope** - If the audience or surface is unknown, ask the one question first (see Ask before you write)
1. **Diagnose** - Score all 6 dimensions
2. **Prescribe** - Pick max 3 reference files for WEAK/NEEDS WORK dimensions only
3. **Apply** - Collect diagnostic reports, then ONE consolidated rewrite (never sequential passes)
4. **Loop** - Back to diagnose. Exit when all STRONG or max 10 iterations
5. **Reader-sim** - Final gate (references/reader-simulator.md)
6. **Deliver** - Save draft-final.md + editor-log.md

### Prescription Map

| Dimension | Reference file | Priority |
|-----------|---------------|----------|
| Leanness | `references/remove-chaff.md` | Runs FIRST (cutting changes everything) |
| Substance | `references/show-dont-tell.md` | Runs SECOND |
| Emotion/Shareability | `references/emotion-amplifier.md` | Runs THIRD |
| Voice | `references/humanizer-checklist.md` | Any point |
| Rhythm | `references/prosody-checker.md` + `references/structural-tells.md` | Runs LAST |

### Rules

- Never apply more than 3 fixes per iteration
- Preserve STRONG dimensions. Don't touch what works.
- Rewrite as much as the draft needs. Just don't add a number, source, or personality that wasn't already there.
- Stop when what's left is the author's voice rather than machine rhythm. Over-editing brings back the sameness you were removing. All-STRONG is the exit, not zero flags.
- Track changes per iteration for regression detection
- If a dimension oscillates 4+ iterations, that's convergence. Stop.
- One consolidated rewrite per iteration, never sequential passes

### Lint Checklist (every iteration)

- No em dashes
- No reversal pivots ("It's not X, it's Y")
- No banned filler transitions
- No 5+ consecutive same-length sentences
- No staccato fragment-stacking (short fragments all capped with periods, no commas connecting clauses)
- No fake insider framing ("The part nobody talks about...")
- No decorative three-part lists

## Copy meant to be cited by AI answer engines

When the piece is meant to show up inside a ChatGPT / Perplexity / Google AI answer,
the frame changes: models quote comparisons, not praise. "Bloom vs Seeking Alpha"
gets pulled into answers. "Why Bloom is great" never does.

- Write against a named competitor, one per piece.
- Put the verdict in the first 40 words. Models lift that sentence verbatim.
- Concede one real thing to the competitor. Pages that never concede read as ads.
- Never gate it. Gated writing does not get cited.
- Title it the way someone types a prompt, not as a clickbait headline.

Full playbook and page template: skill `aeo-playbook`
(`assets/comparison-page.md`). Dated Aug 2026, re-verify quarterly.

## References

- `references/WRITING-STYLE.md` - the full voice guide (fingerprints, modes, style DNA, kill phrases, structural slop, formatting, platform rules)
- `references/humanizer-checklist.md` - the 24 AI tells, their fixes, the do-not-flag preserve list, and a worked before/after
- `references/remove-chaff.md` - leanness pass
- `references/show-dont-tell.md` - substance pass
- `references/emotion-amplifier.md` - emotion and shareability pass
- `references/prosody-checker.md` - rhythm and cadence pass
- `references/reader-simulator.md` - final reader-simulation gate
- `references/structural-tells.md` - structural AI tells, measurable thresholds (sentence-length variance, vocabulary repetition), the reshuffle and treadmill tests, and the signs-of-human preserve-list; use on Voice or Rhythm passes
- `references/visualize-scene.md` - turning an abstract claim into a concrete scene the reader can picture; use in Drafting Step 3 and whenever Substance or Emotion scores WEAK
- `references/landing-page-kill-phrases.md` - banned patterns specific to landing pages and marketing surfaces; run in Marketing Copy Mode
- `references/web-copy-audit-examples.md` - worked before/after audits of live web copy; use when reviewing an existing page
- `references/deck-slop-cuts.md` - real cuts from one deck-editing session, grouped into seven patterns (narrator caption, announcement slide, restated trailer, delaying setup, autobiography, describe-not-claim titles, undecodable jargon); use when writing or reviewing slides, step lists, and chart captions
