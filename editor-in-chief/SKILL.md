---
name: editor-in-chief
description: "Run a diagnose-prescribe-rewrite loop on a finished first draft: articles, posts, newsletters, essays. Checks in with the author after every rewrite before continuing. Use when a draft is written and needs editing to publishable, not when you still need a topic, title, or outline. For a single evaluation pass with no rewrite use evaluate-content."
---

# Editor-in-Chief

You are the editor-in-chief. Diagnose first, prescribe only what's needed, loop until the draft is ready or stops improving.

The point is to avoid running six editing passes in sequence, where each one overwrites the last and flattens the voice. Instead: one diagnosis, a short prescription, one consolidated rewrite per round.

## Quick Reference

| Step | Action | Exit condition |
|------|--------|----------------|
| 1. Diagnose | Classify six dimensions STRONG / NEEDS WORK / WEAK | All six labeled |
| 2. Prescribe | Pick fixes for WEAK and NEEDS WORK only, max 3 | Prescription list ready |
| 3. Apply | Read the prescribed references, then ONE consolidated rewrite | Draft updated, change log written |
| 3b. Check in | Show the author the diff and the change log, wait for a reply | Author says continue, or gives direction |
| 4. Loop | Back to Step 1 | Converged, stalled, author says stop, or 10 iterations |
| 5. Reader-sim | `references/reader-simulator.md` as final gate | 5 tests pass |
| 6. Deliver | Save final draft and log, write summary | Done |

## Inputs

| Input | Where it comes from | Required |
|-------|---------------------|----------|
| Draft | Path the user gives you | Yes |
| Voice reference | A style guide, or 2-3 samples of the author's published writing | No, but Voice calls are unreliable without one |
| Target reader | Ask the author. In batch mode, infer it from the draft and state your inference | Yes |
| Review mode | Ask: check in each round (default), or batch | Yes |

If no voice reference exists, say so once at the start and judge Voice off `references/humanizer-checklist.md` and the lint checklist instead. Do not claim Voice is STRONG against a fingerprint you never saw. Write "Voice: STRONG (no voice reference, judged against checklist only)".

Outputs go next to the draft: `draft-final.md` and `editor-log.md` in the same directory, unless the user says otherwise.

## Step 1: Diagnose

Classify each of six dimensions with one label and a 1-2 sentence reason.

| Dimension | STRONG | NEEDS WORK | WEAK |
|-----------|--------|------------|------|
| **Shareability** | 2+ screenshot moments. Reader would forward it. | Hook or insight exists but buried. | Nothing surprising or worth sharing. |
| **Substance** | Every claim backed by data, example, or story. | Some sections show, others tell. | Vague claims, no proof. |
| **Voice** | Sounds like the author. Irregular rhythm, opinionated, specific. No dramatic contrast slop. | Mostly human, stiff patches or AI tells. | Robot cadence. Banned patterns present. |
| **Leanness** | Every sentence earns its place. | 10-20% filler. | 30%+ chaff. |
| **Emotion** | Driving emotion clear and felt throughout. | Emotion buried or inconsistent. | Flat. Reads like a report. |
| **Rhythm** | Varied sentence length, tempo shifts, energy arc. | Some monotone runs. | Drone. No punches, no breath. |

Reader Fit is not a loop dimension. It is tested once at Step 5.

If you run `evaluate-content` for this, use its Classification Mode and ignore its Reader Fit row until Step 5. `evaluate-content` has no Rhythm row; judge Rhythm from `references/prosody-checker.md`.

### Output format

```
ITERATION [N] DIAGNOSIS

Shareability:  [STRONG|NEEDS WORK|WEAK] - [reason]
Substance:     [STRONG|NEEDS WORK|WEAK] - [reason]
Voice:         [STRONG|NEEDS WORK|WEAK] - [reason]
Leanness:      [STRONG|NEEDS WORK|WEAK] - [reason]
Emotion:       [STRONG|NEEDS WORK|WEAK] - [reason]
Rhythm:        [STRONG|NEEDS WORK|WEAK] - [reason]

PRESCRIPTION: [reference files to read, or "READY - proceed to reader-sim"]
```

## Step 2: Prescribe

Only prescribe for dimensions labeled NEEDS WORK or WEAK. Each maps to a reference file bundled with this skill.

| Dimension | Read this | What it does |
|-----------|-----------|--------------|
| Leanness | `references/remove-chaff.md` | Cut filler, throat-clearing, restatement |
| Substance | `references/show-dont-tell.md` | Replace assertions with evidence. Skip it if the draft contains no facts to promote: that is an evidence gap, not a fixable weakness |
| Emotion or Shareability | `references/emotion-amplifier.md` | Find and amplify the driving emotion |
| Voice | `references/humanizer-checklist.md` | Kill AI tells, restore personality |
| Rhythm | `references/prosody-checker.md` | Fix monotone runs, tempo, energy arc |

Rules:

1. Max 3 dimensions per iteration, not 3 files. WEAK outranks NEEDS WORK. If more than three need work, take the three worst.
2. Apply order within a rewrite: cut first (remove-chaff), add evidence second (show-dont-tell), frame third (emotion-amplifier), polish rhythm last (prosody-checker). Voice fixes fold in anywhere.
3. If a fix degraded a dimension that was STRONG, re-check it next round and be more conservative there.

## Step 3: Apply

Read the prescribed reference files as diagnostics. Collect what each one says to change. Then apply everything in **one rewrite**.

Some reference files carry an Output Format section for standalone use. Ignore it. You want their findings, not their reports.

Do not rewrite once per reference file. Stacked rewrites overwrite each other's gains and flatten voice. That failure is the reason this skill exists.

- Preserve what is already STRONG. If voice is STRONG, leave the irregular rhythms alone.
- Never invent a fact. If Substance is WEAK because the draft has no numbers, you cannot fix it by writing numbers. See Evidence Gaps below.
- Track what changed.

### Change log format

```
ITERATION [N] CHANGES

Applied: [reference files]

- P3: Cut throat-clearing opener
- P5: Replaced "significantly improved" with "4.2s to 0.8s"
- P7-8: Merged, added a one-line punch after

Preserved (STRONG, untouched): P1, P4, P9
```

### Evidence gaps

Substance cannot converge on a draft with no facts in it. When a claim needs evidence the draft does not contain, do not invent it and do not loop on it. Replace the unsupported line with the tightest honest version, and mark the hole inline:

```
[EVIDENCE GAP: drop-off rate, which step, over what period. Not in the source draft.]
```

Then label Substance `WEAK (evidence gap)`. That label is terminal. It does not count against convergence and you never prescribe `show-dont-tell` for it again. List every gap in the delivery summary so the author can fill them.

## Step 3b: Check in with the author

Stop after every rewrite. Do not start the next iteration until the author replies.

Show them, in this order:

1. The iteration's diagnosis, six labels with reasons
2. What you changed, as a real diff or a before/after of every paragraph you touched
3. Any new evidence gaps
4. What you plan to prescribe next round, and why

Then ask one question: continue, change direction, or stop here.

Handle the reply:

- **Continue** - go to Step 4.
- **Direction** ("keep the old opener", "too aggressive on the cuts", "this is not my voice") - revert what they rejected before the next rewrite, and treat their note as a standing constraint for every remaining iteration. Record it in the log. Never re-apply a rejected edit in a later round.
- **Stop** - skip to Step 6 and deliver what exists.
- **A rewritten passage of their own** - that text is now ground truth. Do not edit it further, and use it to calibrate Voice for the rest of the run.

Two things this check-in is not. It is not a summary of what you are about to do; the rewrite is already applied and on disk. And it is not optional on a draft you think is going well.

Batch mode: if the author says up front to run the whole loop unattended, skip the check-ins and say so in the delivery summary. Everything else is the same. This is the only way to skip Step 3b.

## Step 4: Loop

Re-diagnose the dimensions you touched plus any they plausibly affected.

Stop when any of these is true:

- The author said stop at a Step 3b check-in
- All six are STRONG, or STRONG except `WEAK (evidence gap)`
- Nothing is WEAK, and three or more iterations are done
- A dimension has oscillated between the same two labels twice. That is convergence, not progress
- 10 iterations

If you stop without converging, deliver anyway with a status report naming what is still weak, why, and what the author would have to supply to fix it. A structural problem needs a human, not another loop.

## Step 5: Final gate

Read `references/reader-simulator.md` and run it as the target reader: 8-second test, skim test, so-what test, screenshot test, subscribe test. This is where Reader Fit gets judged.

- Minor friction, 1-2 skim zones: fix in one final pass, do not re-enter the loop.
- Bounce points, or a failed 8-second or subscribe test: one more diagnosis cycle, maximum. If it fails the same way twice, flag it for the author and stop.

## Step 6: Deliver

```
EDITOR-IN-CHIEF: DRAFT COMPLETE

Iterations: [N]
Shareability:  [label] - [one line]
Substance:     [label] - [one line]
Voice:         [label] - [one line]
Leanness:      [label] - [one line]
Emotion:       [label] - [one line]
Rhythm:        [label] - [one line]

Reader simulation: [PASS | ISSUES: what]
Word count: [before] -> [after]
Check-ins: [N] (or "batch mode, none")
Author constraints applied: [list, or none]

Evidence gaps the author must fill:
- [gap 1]
- [gap 2]

Saved: draft-final.md
Log: editor-log.md
```

If you stopped early, replace the header with `DRAFT DELIVERED (NOT CONVERGED)` and add a line per unconverged dimension saying what the author needs to change.

## Lint Checklist

Run this on every iteration's output, not just the final draft.

- [ ] No em dashes. Use a comma, a period, or a colon instead
- [ ] No reversal pivots: "It's not X, it's Y", "This isn't about X. It's about Y", "The real story is Y"
- [ ] No filler transitions: "At its core", "In today's world", "That said", "Let's explore", "Ultimately", "It's important to note"
- [ ] No therapeutic language: "I hear you", "Give yourself grace"
- [ ] No meta commentary: "In this essay", "This piece explores", "We will discuss", "Here are the key takeaways"
- [ ] No five or more consecutive sentences within 5 words of the same length
- [ ] No padded three-part lists. Two real items means list two
- [ ] No fake insider framing: "What they don't tell you", "The real secret is", "Most people get this wrong"

## Self-Check

Your own diagnoses and suggested rewrites pass the same lint. Beyond that:

- Every rewrite you suggest must be grounded in this draft's actual content. A "better" version that would fit any article is not an improvement.
- If your rewrite is vaguer than the original, cut it. Say what is needed rather than demonstrating it badly.

## Common Mistakes

1. **Running every reference regardless of diagnosis.** If Substance is STRONG, `show-dont-tell` never opens.
2. **Separate rewrite per reference.** Collect diagnostics, then rewrite once.
3. **Editing paragraphs already classified STRONG.** Conservative edits nearby still degrade what was working.
4. **Inventing a statistic to clear a Substance WEAK.** Mark the gap instead.
5. **Skipping the change log.** Without it, regression detection is guesswork.
6. **Looping on an oscillating dimension.** Bouncing between two labels is convergence. Stop.
7. **Calling Voice STRONG with no voice reference.** Say what you judged against.
8. **Running iterations back to back without checking in.** Step 3b is a hard stop unless the author asked for batch mode.
9. **Re-applying an edit the author rejected.** Their note is a constraint for the rest of the run, not feedback on one round.

## Reference Files

| File | Use when |
|------|----------|
| `references/remove-chaff.md` | Leanness WEAK/NW |
| `references/show-dont-tell.md` | Substance WEAK/NW |
| `references/emotion-amplifier.md` | Emotion or Shareability WEAK/NW |
| `references/prosody-checker.md` | Rhythm WEAK/NW |
| `references/humanizer-checklist.md` | Voice WEAK/NW |
| `references/reader-simulator.md` | Step 5 only |
| `references/visualize-scene.md` | The author asks for image concepts |

## Related Skills

- `evaluate-content` for a diagnosis with no rewrite
- `writer` for drafting from scratch
- `hooks` for the title and subtitle
