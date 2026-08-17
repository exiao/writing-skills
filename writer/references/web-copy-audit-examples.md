# Web Copy Audit — Worked Example

From CPE Research stakeholder page (May 2026). Audience: portfolio manager at a fund evaluating AI research tools.

## Kill Phrase Violations Found & Fixed

### Manufactured drop endings (number drops)
- ❌ "Five phases. Three adversarial checkpoints."
- ✅ "A 5-phase pipeline with adversarial checkpoints"
- ❌ "Three iterations. Zero errors."
- ✅ "68% → 95% citation accuracy in three runs"
- ❌ "Every number, checked."
- ✅ "36 of 36 claims traced to source"

### Formulaic contrasts
- ❌ "treating verification as a first-class feature, not an afterthought"
- ✅ "built verification into the pipeline itself"

### Puffery
- ❌ "institutional-quality equity memos"
- ✅ "one-page equity memos with sourced citations"

### Staccato false drama
- ❌ "Every claim cited. Every number verified. Bull and bear cases stress-tested by adversarial AI."
- ✅ "...with sourced citations, adversarial bear cases, and a built-in fact-checker that catches its own mistakes."

### Generic mechanism descriptions
- ❌ "The system self-corrects: it identifies its own errors and patches the skills that caused them."
- ✅ "After each run, the evaluator flags errors. The pipeline patches the skills that caused them and runs again."

### Setup phrases
- ❌ "Every number has an inline citation. The conviction score includes explicit reasoning for why it's not higher or lower."
- ✅ "Numbers carry inline citations back to raw files. The conviction score explains why 6 and not 7, why not 5."

## Voice Improvements (not kill phrases, but better writing)

### Use domain-specific language the audience knows
- ❌ "never checked the source data"
- ✅ "never opened the 10-K"

### Physical verbs
- ❌ "Numbers without provenance"
- ✅ "Numbers float without provenance"

### Show the mechanism, don't label it
- ❌ "Checks every factual claim against the raw source files. If anything fails, the memo is rewritten."
- ✅ "A separate evaluator traces every factual claim in the memo back to raw source files. Mismatches trigger a rewrite."

## Content Cuts (audience-first editing)

Removed for PM audience (kept in v1, cut in v2):
- Complete PR timeline (17 PRs with dates and line counts)
- Skills grid (15 skill names with emoji icons)
- Data source pills (7 API names)
- Repo stats (commit counts, lines of code)
- Eval scenario coverage (10 ticker names)
- "What's Next" roadmap
- Memo format v2 section structure list

Added for PM audience:
- Actual memo excerpt with inline citations visible
- Verification table showing claim-by-claim auditing
- Persona screen (Value/Growth/Contrarian/Macro PASS/FAIL)
- Expandable full memo text for each run
