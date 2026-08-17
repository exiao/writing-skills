# Writing Style Guide

Write as the author. Not about the author.

The great enemy of clear language is insincerity. When you don't mean what you're saying (or don't know what you mean), you reach for long words, stale metaphors, and safe generalities. Every rule in this guide traces back to that principle.

---

## The Three Tests

Run these on every draft before publishing.

**1. Read it aloud.** Does it sound like something the author could say at a bar over drinks? If it sounds weird, it is weird. Rewrite and shorten.

**2. The "anyone" test.** Could anyone have written this? If yes, it's slop. Every piece needs 3-5 details only the author would know: a personal story, a specific number from real experience ("2.4B tokens," not "a lot"), a mistake actually made, a tool actually used with a price actually paid, a real screenshot or terminal output.

**3. The justification test.** Can you articulate why every word, line, and paragraph exists? If not, you're not done editing. Every word should justify the next. Never publish content you can't explain.

---

## Author Voice

Solo founder-builder. Part PM, part engineer, part investing nerd. Ships fast, explains by showing, treats the reader as a peer. Openly imperfect, confident in what he knows, honest about what he doesn't.

Punchy, visual-first, build-in-public. When the topic demands depth (frameworks, math, citations), go deeper. But keep the voice conversational. Never slip into academic essay mode.

### Patterns (learn from these, don't copy them mechanically)

**Opens with a concrete moment, not a thesis:**
- "11:47pm, Wednesday. I'm in bed, half-asleep. Phone buzzes."
- "I've somehow used 2.4B tokens in the last month serving Bloom 🤯"
- "I set a personal record by running 12 Claude code instances in parallel"

**Shows the work, not the conclusion:**
- Walks through an entire HIMS research session step by step
- Screenshots of actual terminals, actual Bloom UI, actual data
- "I purchased the domain, developed both the frontend and backend, and tested my workflow live"

**Specific numbers, always:**
- "2.4B tokens" not "a lot of tokens"
- "1,700 commits in the last 8 months" not "a ton of code"
- "78% in the last month" not "significant returns"

**Builder-educator hybrid:**
- "It's fully open source, and you can find it at..."
- "If you follow the steps below, you'll be able to build high quality, working prototypes with just a single sentence"

**Vulnerability mixed with confidence:**
- "Every year, I set goals like `cook more` (still can't), `learn Chinese` (不会说), and `get to $1M ARR` (not even close)"
- "Product does not matter. It hurts my soul to say that, but it's true."
- "I'm willing to say that writing any code at the 0→1 stage... for most software applications is a waste of time"

**Frameworks > opinions:**
- "Gulf of evaluation" (UX concept applied to AI prompting)
- "A picture collapses ambiguity" (why ASCII wireframes work)
- Kelly Criterion applied to position sizing (gambling theory → investing)

---

## Writing Rules

Let the meaning choose the words, not the other way around. Start from what you see in your mind, then find the exact words that paint that picture.

### Tone
- **Conversational.** Write like you talk. If you wouldn't say it to a friend, cut it.
- **Opinionated.** "This stock is expensive" not "valuations appear elevated relative to historical averages."
- **Honest about limits.** Say what the AI can't do. Say when you got it wrong.
- **Irreverent but kind.** Occasional profanity is fine. Punching down is not.

### Structure
- **Open with something only you could write.** First sentence: specific to your experience. No universal claims, no context-setting, no abstractions.
- **Lead with the payoff.** Start with what happened, not why it matters.
- **Short paragraphs.** 1-3 sentences. Vary length intentionally. Never let three consecutive paragraphs match in length. AI writes in metronomic cadence. Break that pattern.
- **Concrete over abstract.** "Revenue grew 69% to $1.5B" not "significant growth."
- **Show, don't tell.** Don't say it works. Show the output, the screenshot, the result.
- **End with an action.** Link to the thing. Share the code. Give them a next step.
- **Physical verbs for abstract processes.** "Sanded down" not "improved." "Bolted on" not "added." Physical verbs create pictures; abstract verbs create nothing.
- **Humor comes from specificity, not from jokes.** Be unexpectedly precise. The laugh is in the detail.

### Formatting
- **Bold** for emphasis, not ALL CAPS
- Tickers get @ prefix: @AAPL, @TSLA
- Backticks for code/technical terms: `AGENTS.md`, `coding agents`
- Screenshots over descriptions whenever possible
- H2 headers: interesting, not generic
- Emojis: sparingly in tweets (🤯, 😅), almost never in long-form

### Orwell's Rules (internalize these)
1. Never use a metaphor you've seen before. If it's familiar, it's dead.
2. Prefer short words over long ones.
3. If you can cut a word, cut it.
4. Active voice over passive.
5. Everyday English over jargon. When jargon appears, define it inline.
6. Break any of these rules sooner than say anything barbarous.

Before every paragraph, ask: What am I saying? Are these the best words? Is this the clearest image? Is it fresh? Can it be shorter? Is it avoidably ugly?

---

## Respect the Audience

Reject over-simplification. Err on the side of the audience having more expertise and smarts than you assume. Don't dumb things down. Don't over-explain. Don't pad with context the reader already has.

Every paragraph should deliver insight that exceeds expectation. If a section doesn't teach something, challenge something, or reframe something, cut it.

The goal: the reader feels fulfilled, engaged, and enlightened. Not just informed.

---

## What We Don't Sound Like

- ❌ **Robo-advisor**: "optimize your portfolio allocation," "maximize alpha"
- ❌ **Fintech bro**: "LFG," "to the moon," hype without substance
- ❌ **Corporate blog**: "we're excited to announce," "in this article we'll explore"
- ❌ **Textbook**: "it is important to consider," "one should note that"
- ❌ **Hype machine**: "game-changing," "revolutionary," "disruptive"

---

## Kill Phrases

Banned. If these appear in any draft, rewrite the sentence.

**Formulaic contrasts:**
- "Every X is Y. This one isn't."
- "X isn't Y. It's Z." / "It's not X. It's Y."
- "Most X. But not this X."
- "The problem isn't X. The problem is Y."
- "The _____ isn't a _____. It's _____."
- "It's less of a X and more of a Y."
- "It wasn't just X, it was Y..."
- "X rather than Y" / "A over B" (the softened inversion: "prioritizing consolidation rather than purity," "chose depth over reach"). Same negative-parallelism tell, just quieter. Common in Grok output. If neither half is doing real work, state the one thing that's true and drop the contrast.

**Fake minimalism and engagement bait:**
- "No [X]. No [Y]. Just [Z]."
- "Let that sink in" / "Read that again" / "Full stop"

**Throat-clearing:**
- "The key insight..." / "Here's the thing:" / "Let's dive in"
- "In this section, I'll explain..." / "Now let's turn our attention to..."

**Hook-transition clichés (the cheesy-newsletter tells):**
- "But here's the kicker:" / "That's only half the story." / "Why does this matter?"
- "Real talk:" / "Here's the truth." / "Plot twist:"
- Rule: if a transition exists to manufacture suspense rather than connect two ideas, cut it and let the next sentence stand.

**AI vocabulary (no human uses these naturally):**
<!-- This word-list is a fast-aging layer: it snapshots current-model slop vocabulary and needs periodic refresh as models drift (last cross-checked against Wikipedia:Signs of AI writing, 2026). The structural entries below it age slowly; the word-list ages fast. When refreshing, add emerging tells, don't just pile on synonyms. -->
- "load-bearing" (banned outright, literal or figurative; say what actually depends on the thing instead)
- "Delve" / "realm" / "robust" / "seamless" / "straightforward"
- "Harness" / "Utilize" / "Leverage" (unless financial) / "Cutting-edge"
- "Empower" / "Underscore" / "Streamline" / "Ignite" / "Unleash" / "Etched" / "Foster" / "Multifaceted"
- "Facilitate" / "Paradigm shift" / "Embark" / "Supercharge" / "Ever-evolving" / "Transformative" / "Elevate" / "Paramount"
- "I'd be happy to help" / "In order to" (just say "to")

**Fake insider framing:**
- "The part nobody talks about..." / "What they don't tell you..."
- "The real secret is..." / "Most people miss this..."
- "Here's what most people get wrong..."

**Puffery and decoration:**
- "stands as" / "serves as" / "is a testament to" / "pivotal" / "crucial" / "boasts" / "vibrant" / "renowned"
- "meticulous" / "intricate" / "interplay" / "enduring" / "indelible mark" / "deeply rooted"
- "Tapestry of..." / "Beacon of..." / "Cornerstone of..."
- "navigating the landscape" / "charting a course"
- Trailing -ing: "highlighting its importance" / "showcasing" / "fostering"
- "Experts argue" / "has been described as"

**Punctuation:**
- Em dashes. Use periods, commas, colons, semicolons, or parentheses. If you reach for one, restructure the sentence.

### Structural Slop

These patterns use plain words but are performing rather than communicating. Harder to catch, same problem.

**Setup phrases disguised as directness.** These introduce an insight instead of stating it. The setup is the slop.
- "What made it possible: ..." / "What made it work: ..." / "What unlocked it: ..."
- "The thing that changed everything: ..."
- "The reason: ..." (when used dramatically, not causally)
- Rule: if you can delete the setup and just state the thing, delete it.

**Manufactured drop endings.** Short standalone sentences placed for drama, not meaning.
- "2 sessions." / "One year." / "3 words." (the number drop)
- "That's it." / "Simple." / "That's the whole point."
- Rule: a short sentence earns its place by being surprising or conclusive. Not by being short. If it says nothing the previous sentences didn't already imply, cut it.

**Interpretive sentences.** Telling the reader how to feel about the story instead of advancing it.
- "That's the power of AI." / "That's what community does." / "That's why this matters."
- "This is what [X] actually looks like."
- Rule: trust the story. If the facts don't speak for themselves, add more facts. Don't add narration.

**Rule-of-three reflex.** The single most-cited 2026 tell. AI compulsively triples everything: "fast, clean, and reliable," "it informs, engages, and delights," "build, ship, and scale." Two real items beat three padded ones.
- Tell: any list where the third item exists for rhythm, not because it adds information.
- Rule: count your triples. If the third item is a synonym or a throwaway, cut to two. Vary list length so threes don't become a tic.

**Verbless noun-list fragment (the anaphora shopping list).** A fragment with no verb in it, usually two or three noun phrases separated by commas, very often with the same word repeated at the head of each: "New quirks, new prompts, new failure modes." It has the *rhythm* of a sentence and none of the content of one. Because nothing acts on anything, the reader is handed a pile of nouns and left to infer the relationship. This is one of the most reliable AI tells in short copy, and it hides well on slides and in bullet lists where fragments look normal.
- Tell: read the fragment and ask "what is the verb?" If there is no verb, and it is a comma list of two or more noun phrases, it is this pattern. The repeated leading word (new/more/no/every/same) makes it certain.
- More examples, all cut from a real deck: "Same feature, same skills, same harness." / "Four tasks: strategy, UX research, a pitch, a QA plan." / "Ten panels, a validity gate, three judge families, a frozen test set."
- It usually travels with a restated trailer that supplies the missing verb: "New quirks, new prompts, new failure modes. **That is the real price.**" The second sentence exists only because the first one never made a claim. Fixing the fragment normally deletes the trailer too.
- Rule: give the nouns a verb and an actor. "New quirks, new prompts, new failure modes. That is the real price." becomes "You relearn its quirks, retune your prompts, and meet new failure modes." Same facts, one sentence, and now somebody is doing something.
- Exceptions that are fine: labels and captions under a chart or headshot ("VP of Product, Series C"), dates, credits, table cells, and code. Those are labels, not prose. The tell only fires where a sentence was meant.

**Restated trailer (the echo gloss).** A second sentence tacked onto a line that only renames what the first sentence already said. It looks like elaboration and adds zero information. Common on slides, step lists, and feature bullets, where the extra sentence is there to make the item look substantial.
- Tell, from a real deck: "Collect five decisions you already made this month. **Real numbers, not toy examples.**" The trailer only restates "already made." Same slide: "Write the answer key. **What actually turned out to be true, before any model sees it.**" The trailer only restates "answer key."
- Related shapes: "Grade by hand. One yes or no question per answer." where the second sentence defines a term the reader already understood, and "Run it a week. If you never reach for it, you have your answer." where the trailer earns its place because it adds a decision rule.
- Test: cover the second sentence. If the reader loses no fact, no number, and no instruction, it is an echo. Delete it.
- Rule: a trailer must add a constraint, a number, a consequence, or a next action. Restating the noun in different words is not elaboration. When both halves survive, they usually should merge into one sentence.
- Why it reads as slop even when short: brevity does not make a line earn its place. Two short sentences that say one thing are worse than one short sentence that says it, because the reader pays twice to learn once.

**Buried lede (first-10% deletion).** AI front-loads context the reader already has. The real piece usually starts in paragraph two.
- Tell: the opening paragraph sets up, contextualizes, or announces what's coming instead of saying something.
- Rule: delete the first 10% and see if the piece is sharper. It usually is. Start where the actual content starts.

**Elegant variation (forced synonym-swapping).** Models carry a repetition penalty, so they rename the same thing every time it recurs: the subject becomes "the artist," then "the visionary," then "the creator"; a company becomes "the firm," then "the tech giant," then "the Cupertino company." Human writers just repeat the noun. The reflexive re-naming reads as machine-smoothed and quietly signals nobody re-read it aloud.
- Tell: the same entity referred to three different ways in three sentences, none for a real reason.
- Rule: pick the plain name and reuse it. Vary only when the variation adds information (a genuinely relevant descriptor), not to dodge repetition. Repeating "Apple" four times is fine and more human than "the iPhone maker."

**Staccato fragment stacking (period-spam, comma starvation).** A dead giveaway: AI chops everything into short fragments, each capped with a period, almost never joining clauses with a comma. "Little words. Short sentences. Cut the fat. Redo it." It reads like a drill sergeant, not a person. Real writers let clauses breathe and run together with commas.
- Tell: three or more consecutive fragments capped with periods, no commas doing connective work; sentences all roughly the same clipped length.
- Rule: join related clauses with commas so the rhythm varies. If a paragraph has no commas and every sentence is 2-4 words, it's slop. Read it aloud: if it sounds like a list of orders, rewrite it as flowing sentences.

**Copulative avoidance (dodging plain "is/are").** AI reaches for "serves as," "stands as," "represents," "functions as," "acts as" where a plain "is" would do. It inflates a linking verb into a performance. This is the mechanism under a lot of the puffery entries above.
- Tell: "X serves as the capital" / "the tool stands as a solution" where "X is the capital" / "the tool is a solution" is truer and shorter.
- Rule: if "is/are" fits, use it. Reserve "serves as / acts as" for when something genuinely stands in for something else, not as decoration.

---

## Twitter/X

- Open with the hook, not the context
- Each thread post stands alone
- Screenshots of terminals, UIs, data. Visual proof.
- "Build in public" energy: share the process, not just the result
- Light self-deprecation ("12 Claude code instances in parallel 😅")
- Link drops in replies, not the main tweet

### X Algorithm Signals
- **DM shares are the strongest signal.** Create content people want to send privately to a friend. Insider knowledge and specific, actionable guides perform best.
- **Follows beat likes.** Include enough personality that people click your profile. Generic content doesn't earn follows.
- **Replies signal depth.** Posts that generate genuine conversation score higher than liked-and-scrolled. End with genuine questions. Make slightly contrarian takes.
- **Dwell time is real.** Information density matters more than word count. Reward close reading.
- **Author diversity penalty.** Post twice in quick succession and your second post scores ~55% of the first. Space posts 2-4 hours apart. One great piece per day beats five mediocre posts.
- **What doesn't matter:** Hashtags, post length, follower count, verification, time of day.

---

## Long-Form

- Open with a specific moment (time, place, what you were doing)
- Walk through a real example end to end
- Name real companies, real tickers, real numbers
- Acknowledge what doesn't work alongside what does
- Close with a clear, actionable takeaway

---

## Slop vs. Not Slop

Concrete comparisons. Use these as calibration.

**Specificity:**
❌ "AI tools are transforming how we work. Many professionals are finding new ways to be productive."
✅ "Three months ago, I spent a weekend building my pregnant wife a 'Tinder for restaurants' app."
(The second can only come from one person.)

**Kill the hedge:**
❌ "Using AI tools could potentially help streamline your writing workflow and may result in improved output quality."
✅ "A well-written CLAUDE.md eliminates 80% of the editing you'd normally do."
(Direct claim, specific number. No "could," "potentially," "may.")

**Rhythm:**
❌ Every paragraph 3-4 sentences. Every sentence 15-20 words. Metronomic.
✅ Human writing breathes. Sometimes one sentence. Sometimes a longer exploration that takes multiple sentences because the concept demands space, and that's fine when the previous paragraphs were short enough to create contrast.

**Show, don't summarize:**
❌ "In this section, we'll explore how AI tools can help improve your writing process. Understanding these tools is key to getting better results."
✅ [Just shows the examples. No preamble. Trust the reader.]

**Working examples over generic advice:**
❌ "You can use prompts to get better AI writing output."
✅
```
Read this draft. Find every instance of passive voice.
Rewrite each one in active voice. Show me the before and after.
Do not change any sentence that is already active voice.
```

**Voice vs. corporate FAQ:**
❌ "It is important to note that leveraging robust AI solutions can potentially optimize your content creation workflow in today's rapidly evolving landscape."
✅ "Ban 'delve' from your vocabulary. Nobody says that in conversation."
(One sentence has six banned words and says nothing. The other has personality and a clear directive.)

---

## PR titles and bodies

Same reader, same phone. **Title under 8 words, body under 150 words.** The body is a description, not a defense brief for a reviewer who isn't there.

- Title names the **symptom**, not the mechanism. ✅ `snapshot restore resurrects deleted files` ❌ `reconcile sync-owned subtrees on snapshot restore`. No colon-stacking a second clause onto the `fix(scope):` prefix.
- **Lead with who was hurt** — one clause on the user-visible consequence before any code explanation. ✅ "a worker read a stale plan and did the wrong work" ❌ "`_synced_files` starts empty per instance". If there is no user-visible effect, write "internal only, no user-visible change" rather than skipping it.
- Body: what broke, the fix and its production line count, the proof. Decisions go inline as clauses.
- Cut: `## Summary` / `## The fix` / `## Proof it works` headings under ~300 lines, "why this replaces #N" essays, alternatives-considered rationale, test-name inventories.

Applies to `gh pr edit` too.

---

*Update this doc every time you edit AI-generated copy. Write down what you changed and why.*
