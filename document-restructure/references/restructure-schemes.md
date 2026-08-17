# Restructure schemes

Organizing principles to offer when a document needs reorganizing rather than
rewriting. Each one is a genuinely different principle, not a variation. Build
each candidate as a real file so the user can open and diff them.

Worked example throughout: `~/.hermes/SOUL.md`, an operator instruction file whose
original layout was topic sections (Principles, Identity, Workspace, External
Actions, Group Chats, Task Approach, Delegation, Git, Tools, Memory, Security,
Writing Rules).

---

## A. Topic buckets

`Who you are` / `How you work` / `Where things are` / `What you can do` / `How you write`

Familiar, easy to navigate, easy to write. Weakest on the actual failure mode of a
document read repeatedly by an agent: nothing tells it, at the moment it needs to
decide, which bucket the current situation belongs to. Optimized for "where would
a human file this," not "when do I need this."

Best when the document is a reference people consult with a specific question, and
when the user supplied the headers.

## B. The sequence of a working session

`Read the ask` / `Decide where it goes` / `Do it` / `Report back`

Every rule sits at the moment it fires. Vocabulary and scope-reading land in beat
one, the hard gates land inside "do it" where they bite, the length cap and
formatting rules land in beat four. Shaped like the thing it governs.

Costs a little length because gates get restated inside a beat instead of gathered
once. Strongest when the document is read *while* doing the work, not before it.

## C. Force: gates / defaults / reference

`GATES` (never bend) / `DEFAULTS` (bend with judgment, say what you chose) /
`REFERENCE` (mechanics, paths, rosters, syntax)

Sorts by how binding a line is, not what it is about. Never-bend items sit alone at
the top with nothing to dilute them. Judgment calls sit in the middle. Mechanics
drop to the bottom where head/tail truncation is cheapest to lose.

Strongest truncation-safety of the set, and often the only scheme where the
document's own first line is also its table of contents. In the SOUL example the
file already opened with "Rules are gates or defaults," which made this the scheme
the author had already written without using it.

## D. Blast radius

`Go ahead` / `Ask first` / `Never`

The safest possible arrangement, and it makes the agent timid. Much of what an
operator doc governs (voice, compression, when to recommend vs survey) is taste,
not danger, and has nowhere to sit. Offer it; do not lead with it.

## E. By failure mode

Name the way the agent fails, then the fix. "I ask instead of deciding." "I say
done before it ran." "I explain too much." "I widen the job."

Sharp and memorable. The catch: structurally identical to the incident-log
document most people are trying to escape, just better dressed. Works best folded
into scheme B as a callout under each beat, not as the top-level scheme.

---

## Choosing

Ask what the reader is doing at the moment they open the file.

- Looking something up → A
- Executing a task with the doc in context → B
- Deciding whether they are allowed → C or D
- Learning not to repeat a mistake → E

Then check the document's opening paragraph. If it already states an organizing
principle, that principle usually wins, because the reader learns the file's shape
from its first sentence instead of from a heading scan.

## Verification

After any restructure, compare char counts. Within a few hundred of the original
means the words survived. A large drop means you rewrote. Report both numbers in
the reply; it is the cheapest available proof.
