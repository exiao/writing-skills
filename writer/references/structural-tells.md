# Shape problems

Banned words are the easy half. The shape of the writing gives it away more reliably. Fix
every word on the list and leave the rhythm alone, and it still reads as machine-made.

Use this on a voice or rhythm pass. Measure first, then fix.

## The numbers

Rough thresholds. A hit means look closer, not that the piece is guilty.

| Measure | How to compute | Flags when |
|---|---|---|
| Sentence-length variance | stdev / mean of sentence word counts | below 0.25, when mean > 10 words |
| Vocabulary repetition | unique words / total words, on 200+ words | below 0.40 |
| Heading density | headings per word | more than 3 in under 300 words |
| Bullet density | bullets per word | more than 8 in under 200 words |
| Verbless bullets | consecutive bullets that are short noun phrases with no verb | 5 or more in a row |
| Em dashes | count | more than one per 1,000 words |

Sentence-length variance is the one worth checking first. People swing between a four-word
sentence and a thirty-word one. Machines stay near the average.

If the piece is long and rhythm is the main problem, stop here and run
`prosody-checker.md` instead. It does tempo, stress placement, and energy arc properly.
This file is the fast lint.

## Two things you can check by hand

**Shuffle the paragraphs.** Move three of them into a different order. If it reads the
same, they were never building an argument, just a list in paragraph form. A real argument
breaks when you reorder it.

**Try cutting half.** Aim to remove 40-60% without losing any information. If you can, most
of the draft was saying the same thing in different words. Make the cut.

## What to look for

Described plainly. No need to memorize labels.

- **Every sentence the same length.** Or every sentence a clipped fragment. Both read as
  machine-made. Join some clauses with commas so the rhythm moves.
- **"Not X, it's Y."** Watch for the version split across two sentences: "The headline
  isn't the speed. The real story is the cost." Same move, easier to miss.
- **Lists padded to three** when the content only supports one or two.
- **A sentence whose only job is to say the last one mattered.**
- **A warm closing line that adds nothing** and exists to leave the reader feeling good.
  Cut it and see whether anything was actually lost.
- **Stacked hedges.** "could potentially possibly". Pick one.
- **Cycling through synonyms** for the same thing to avoid repeating a word. Just repeat
  the clearest one.

## Leave these alone

This is why most cleanup passes make writing worse. Don't touch:

- A sentence that runs long because the thought is genuinely tangled
- A word choice that is odd but precise
- An aside or parenthetical the sentence works without
- Uneven section lengths
- Repeating the same noun instead of reaching for a synonym
- Flat, unadorned statements with no rhetorical shape
- A blunt or unhedged opinion
- Specific detail that reads as excessive

If your edit would remove one of these, don't make it.
