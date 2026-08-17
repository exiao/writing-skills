---
name: document-restructure
description: "Reorganize a document into new sections while preserving the author's exact words: SOUL.md, constitutions, READMEs, specs, plans, style guides. Use when the user says 'put my words into new sections', 'use the exact same words', 'reorganize this', 'what if the headers were X', 'try a different structure', or rejects your rewrite because the LANGUAGE is bad rather than the idea. Restructure is not editing and not rewriting: not one sentence may change. For improving the prose itself use writer or evaluate-content; for scoring a SOUL.md use soul-md-audit."
---

# Document Restructure

Reorganizing a document is a third mode, separate from drafting and from editing.
The words are fine. The *arrangement* is the problem. Nothing you produce here
may contain a sentence the author did not write.

## When this fires

- "Put my words into new sections."
- "Use the exact same words, just reorganize."
- "Make a version with these headers: ..."
- "Are you sure those are the right sections?"
- The user rejected your rewrite with a complaint about **the language**, not the
  idea. That is a restructure request wearing a critique costume.

## The failure this exists to prevent

The user asks to reorganize a document. You hand back a shorter version in your
own voice. They tell you the language is crap and ask again, this time spelling
out "use the exact same words." You burned two turns producing prose nobody
wanted.

The tell is that you are proud of a sentence. In a restructure you should not
have written any sentences to be proud of. If your output reads better than the
input, you did the wrong job.

## Rules

1. **Copy sentences out of the source verbatim.** Whole, unsmoothed, unmerged,
   unshortened, including the bold, the backticks, the arrows, the parentheticals
   you find ugly. The ONLY thing that changes is which section a sentence lives
   under and in what order.
2. **Verify by char count and report it.** A pure restructure lands within a few
   hundred chars of the original. Print both numbers. Coming back 40% shorter
   means you rewrote and lost constraints; that is a failed restructure, not a
   bonus simplification. This is the single cheapest proof that you obeyed rule 1.
3. **If they hand you headers, use them exactly**, in the order given. Do not
   improve the names, do not add a section, do not merge two.
4. **Ship real files, one per candidate.** Nobody can compare two arrangements
   from a prose description of them. Write `doc.opt1.md`, `doc.opt2.md`, and
   deliver them. Never overwrite the live original without explicit approval.
5. **Name the judgment calls, briefly.** Which section swallowed the contested
   content, and why. In a restructure, that is the *only* real decision you made,
   so it is the only thing worth saying in the reply. Two sentences, not a tour.

## Generating candidate arrangements

When asked for several, run `quick-brainstorm` first, and make each candidate a
different organizing **principle**, not a variation on one. A set of candidates
that are all "topic buckets, slightly regrouped" is a failed brainstorm.

The schemes, and what each one trades:
[references/restructure-schemes.md](references/restructure-schemes.md).

State your pick and why, then build the files. Recommend, do not survey.

**Cross-check against the document's own opening line.** The strongest
arrangement is often already stated in the doc's first paragraph. If a file opens
with "rules are either gates or defaults," then gates/defaults IS the table of
contents, and every other scheme is one the reader has to learn separately. When
the first line can serve as the table of contents, that is usually the answer.

## Diagrams during a restructure conversation

These conversations are structural, so they are diagram-shaped: before/after
section maps, what-moved-where, candidate comparisons. Draw them.

The trap: a diagram about restructuring a doc is itself writing, and the same
plain-language bar applies to the words inside the boxes. Jargon that survives in
a diagram ("attention budget", "monotonic growth", "filing system vs habit")
reads as terrible to a user who just asked for plain words. Before rendering,
read every string in the SVG as if it were a sentence in the reply, and put it
through the same test: would he say "no idea what you mean"?

## Pitfalls

- **Restructuring and simplifying at once.** Two changes the user cannot evaluate
  separately. If they want both, do the restructure, get it accepted, then offer
  the simplify pass as a second step.
- **Silently dropping the section you thought was redundant.** Every line of the
  source lands somewhere in the output. If two lines genuinely duplicate, keep
  both and say so; the dedup is a separate decision they get to make.
- **Describing the layouts instead of building them.** Prose about "four beats vs
  three buckets" is unreadable. Files are cheap. Build them.
- **Improving their header names.** They picked those words. Use those words.
- **Assuming your first sectioning is right.** When a user asks "are you sure
  those are the sections?", the answer is usually no. Treat the first arrangement
  as a draft of the *scheme*, not the deliverable.

## Related

- `writer` for changing the actual prose (drafting and revision).
- `evaluate-content` for scoring copy quality and the Seven Sweeps.
- `soul-md-audit` for scoring a SOUL.md against Hermes loading mechanics; its
  Simplify pass is the *word-changing* counterpart to this skill.
- `quick-brainstorm` for generating the candidate schemes.
