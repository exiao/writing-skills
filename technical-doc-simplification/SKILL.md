---
name: technical-doc-simplification
description: Use when a technical doc is too long or jargon-heavy.
---

# Simplifying internal technical docs

Covers architecture pages, system explainers, runbooks, README internals, design
docs: anything written by the people who built the thing. Trigger phrasings:
"too long", "too technical sounding", "simplify the language across the board",
"shorten this", or a named non-builder audience ("for a technical PM", "so a new
hire can read it").

For marketing/blog copy use `writer` or `evaluate-content`. For reorganizing
without changing any words use `document-restructure`.

The failure mode here is NOT hype or AI-slop. It is the opposite: a doc written
by the builders drifts into reading like **source comments pasted into prose**.
Every sentence is true and almost none of it tells the reader what the thing
does or why they should care.

## Rule 0: two flagged blocks means sweep the whole doc

Trimming one section at a time across separate turns makes the user drive the
sweep. Real sequence from a CPE architecture page: I trimmed one card, then
another the next turn, and the third turn was the user generalizing it for me
("there's too much text and too technical sounding in ALL of these boxes").

**When a second block is flagged for the same reason, sweep every block**, or ask
once whether to. One long section is a section problem; two is a document
standard problem, and every remaining section is about to be flagged too.

## Establish the reader, then apply one test

Ask (or infer) who reads this. The common answer is a **technical PM**: fluent in
systems, NOT fluent in your identifiers.

Then one test per sentence: **would the reader act differently knowing this?**
If not, cut it or leave it to the code.

## The five tells

1. **Identifiers standing in for behavior.** `SKIP LOCKED`, `analyze_slot`,
   `promoted_label`, `run.contradictions`, `StrictUndefined`, `artifact_key = NULL`.
2. **Internal state vocabulary assumed shared.** "fail-soft", "citation-locked",
   "bounded receipt", "advisory lock", "idempotent per ticker+day", "manifest".
3. **Arrow-chains as prose.** `raw manifest → materiality policy → durable event
   → exact-source update job`.
4. **Route/endpoint lists doubling as an explanation**, then paragraphs of
   qualifiers about each.
5. **Plumbing with no consequence.** Three sentences on how a secret is seeded,
   none on what breaks when it lapses.

## The rewrite rule, with worked swaps

**Say what it does and why it matters. Drop how it's wired unless the wiring IS
the point.**

- `Advisory-lock cap across containers; analyze_slot within a process.`
  → `Two limits on how many model calls run at once: one across the whole
  cluster, one inside each worker.`
- `POST /ask files a question (dedup: a redundant ask onto a still-live
  open/researching question collapses onto it, no extra row/spend)`
  → `Duplicate asks fold into the question already in flight, and a second run
  request for the same company that day is ignored, so nobody double-spends by
  clicking twice.`
- A paragraph on OAuth secret seeding → `That tier signs in with OAuth rather
  than an API key, so its credential is re-seeded weekly by a script; if it
  lapses, titles come back blank and nothing else breaks.` (The consequence is
  the only part the reader needs.)
- `hash fresh raw payloads for no-LLM change detection`
  → `fingerprint the raw data so the next sweep can tell "changed" from
  "unchanged" without a model call.`
- `after its post-persist tail work (corpus hashes, R2 mirror, wiki publish,
  follow-up seeding) has run`
  → `after its cleanup work (mirroring raw files, publishing the wiki page,
  seeding follow-ups) finishes`.

## What to KEEP

- The file path / module name under each heading. That is how a reader finds the
  code, and removing it makes the doc unverifiable.
- Diagrams. They are usually the least verbose part of the page.
- Fail-closed / gate / retry-cap language where it IS the product behavior, not
  an implementation detail. "Nothing persists unless it passes" is a promise; the
  lock mechanism behind it is not.
- Named constants the reader might tune (a coverage floor, an attempt cap).

## Split, don't only shorten

When one paragraph does three jobs, break it into three short ones rather than
compressing it into one dense one. A route-list block in this session became
three short paragraphs (the routes / what the notable pages do / how everything
traces to a source) and lost ~70% of its characters as a side effect.

## Mechanics: sweeping 20 blocks in one file

Do NOT fire twenty separate patch calls.

**Audit lengths first, so you fix the actual worst offenders rather than the ones
you happened to scroll past.** The user's screenshots arrive in scroll order, not
severity order; measuring finds the 2,600-char wall you haven't reached yet.

```python
import re, pathlib
s = pathlib.Path("docs/architecture.html").read_text()
for m in re.finditer(r'<p[^>]*>(.*?)</p>', s, re.S):
    t = re.sub(r'<[^>]+>', '', m.group(1))
    if len(t) > 240:
        print(len(t), t[:90].replace("\n", " "))
```

For markdown, split on blank lines and measure the same way. Re-run after the
sweep: anything still over ~240 chars is a miss. Inline SVG `<text>` runs show up
as giant fake hits (one 1,907-char "paragraph" that is really diagram labels);
ignore those. Sibling blocks in one row should land within ~30% of each other,
unequal siblings are the fastest visual tell that a section rotted.

1. Write a throwaway `trim.py` next to the file holding a list of
   `sub(old, new)` exact-string replacements, then run it once.
2. Make `sub` **skip-and-print on a miss, never assert**. A hard assert aborts on
   one stale string and silently loses every later replacement; this session it
   died at replacement #4 over one drifted word. Pattern:
   ```python
   def sub(old, new):
       global s
       if old not in s:
           print("SKIP(already):", old[:60]); return
       s = s.replace(old, new, 1)
   ```
   Then handle each printed skip individually with a normal patch call.
3. Copy `old` strings out of a fresh read of the actual file, not an earlier grep
   snippet. HTML entities (`&#8594;`, `&#183;`, `&mdash;`) and smart quotes must
   match byte for byte.
4. For a block too long to paste twice, address it by line index: read the lines,
   assert the target line starts with the expected prefix, assign the
   replacement, join back.
5. Delete the script when done. Never commit it.

## Diagrams are not exempt: "make this easier to understand"

The KEEP rule above ("diagrams are usually the least verbose part") holds for
prose density, NOT for legibility. The entity-relationship / "how these
components point at each other" diagram is reliably the block that draws the next
screenshot after the text sweep lands.

What makes it unreadable is not the boxes. It is that arrows fly in every
direction with a floating label near each one, and there is no reading order. A
CPE table map had ten labels crossing the body and no entry point.

The fix: **impose left-to-right lanes with column headers naming each stage.**
`WHAT STARTS WORK` -> `THE QUEUE` -> `THE UNIT OF WORK` -> `WHAT IT PRODUCES`.
Then:

- Every trigger box stacks in column 1, every artifact in column 4. Arrows run
  strictly left-to-right between adjacent columns, so no arrow crosses a box.
- **Collapse N near-identical labels into one group caption.** Three arrows
  labeled "material event enqueues" / "ask enqueues (dedupe_key)" / "idea
  enqueues" become one caption under the group: "each one enqueues a job".
- Say relationships in words, not identifiers. `parent_run_id` becomes "a
  revision points back at the run it came from"; `dedupe_key` disappears into the
  group caption.
- **Delete any box that is not actually in the flow.** A bare registry table sat
  mid-diagram with one dashed line to nothing; cutting it removed a crossing for
  free.
- The two genuinely non-linear edges (a self-loop for revisions, a feedback path
  back to the trigger column) get one wide, clearly-routed path along the bottom
  with a single caption each. Two exceptions read fine; ten do not.
- Rewrite the caption above the diagram to state the reading order ("work flows
  left to right: something triggers a job, the job produces a run, the run
  produces artifacts"), and drop the legend entries for things you deleted.

Result: 10 crossing labels down to 4, zero arrow-over-box crossings.

**Verify by scrolling to the block, not by whole-page screenshot.** A 600-line
page screenshot is useless for judging one diagram:

```js
var h = [...document.querySelectorAll('h3')].find(e => e.textContent == 'What writes what');
var r = h.parentElement.getBoundingClientRect(); JSON.stringify({top: r.top + scrollY});
```
then `window.scrollTo(0, top - 50)` and vision-check with a role-specific
question ("are any labels overlapping boxes or arrows?"), not "how does this
look".

## Verify before shipping

- HTML: `python3 -c "import html.parser,pathlib; html.parser.HTMLParser().feed(pathlib.Path(P).read_text()); print('ok')"`
  catches an unbalanced tag from a bad replacement.
- `git diff --stat` should show a plausible insert/delete count. Suspiciously
  small means replacements silently skipped.
- Em-dash sweep on the NEW copy. A plain-language pass is exactly where they
  creep back in.
- If the doc is deployed (Surge, docs site), redeploy in the same pass and
  confirm the live bytes changed.
- **A `docs/` dir with no `index.html` publishes a 404 while the CLI says
  "Success!".** `surge docs <domain>` serves `index.html` at `/`, so a repo with
  only `docs/architecture.html` deploys "successfully" to a page-not-found root,
  and can sit broken for a long time because nothing errors. `cp
  docs/<page>.html docs/index.html` before deploying, and confirm the ROOT url's
  `<title>` in a browser rather than trusting the deploy CLI's output.

## Ship it as a PR

A copy-only pass is still a normal PR off `origin/<default>` in a worktree. Title
names the symptom in under 8 words ("Architecture page reads like source
comments, not an explanation"); body under 150 words leading with who was hurt
(the reader who has to parse implementation trivia to learn what a component
does) and what was cut vs kept.

Repos often have a rule tying the doc to code changes (cpe's `AGENTS.md`: any PR
that changes the architecture must update `docs/architecture.html` in the same
PR, deployed to cpe-architecture.surge.sh). Read `AGENTS.md` before touching a
maintained doc so you also redeploy where required.

**One PR carries every pass.** The user sends successive screenshots over several
turns; push each round to the SAME branch rather than opening a PR per
screenshot. In each reply, state the RULE you applied and what you deliberately
cut ("kept every fail-closed and spend-control fact, dropped table names and env
vars"), so the user can veto the rule once instead of vetoing block by block.

