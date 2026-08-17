---
name: technical-writing
description: "Use for docs, runbooks, error messages, plans, PRs."
---

# Technical Writing

For text that has to be understood on one read, by a tired person, possibly not a native
English speaker, possibly at 3am during an incident. Nobody is being persuaded. Flat is
the goal.

Covers: docs, READMEs, runbooks, error messages, API and UI labels, plans, PR bodies,
AGENTS.md, agent prompts, commit messages, issue bodies.

Rules adapted from ASD-STE100 Simplified Technical English, the controlled language
aerospace has used for maintenance manuals since 1983.

## Not for voice writing

If the text has an "I" in it, or its job is to make a reader care, stop and use the
`writer` skill. These rules produce near-identical sentence lengths, which is exactly the
pattern `writer` flags as machine-made. Applied to a blog post or landing page they delete
the persuasion on purpose.

| Surface | Skill |
|---|---|
| Runbooks, docs, READMEs | this one |
| Error messages, API and UI labels | this one |
| Plans, PR bodies, AGENTS.md, agent prompts | this one |
| Articles, tweets, landing pages, marketing | `writer` |
| Anything with a first person or an argument | `writer` |

Mixed document? Route per passage. A tagline inside a README is voice writing.

## First: is this a procedure or a description?

Everything else depends on this.

**A procedure** tells someone to do something. Imperative mood, one instruction per
sentence, 20 words max.

**A description** explains how something works. Simple tenses, 25 words max, one topic per
paragraph.

A note or warning sitting inside a procedure is a description. Treat it as one.

Counting words: a backticked command, an identifier, or a number with its unit counts as
one word. `git rebase --onto main` is one word, not four.

## The rules that matter most

**Say must, not should.** Both people and models read "should" as optional. If it's
required, write "must". If it isn't required, delete the line. Same for "may", "might",
and "could": pick "can" or cut it.

- No: "You should set DB_PASSWORD before running."
- Yes: "Set DB_PASSWORD before you run the command."

**Condition first, then the command.** The reader needs to know whether to keep reading
before they act.

- No: "Read the log if the build fails."
- Yes: "If the build fails, read the log."

**One thing, one name.** Pick one word per concept and never rotate. Synonym variety is a
virtue in prose and a bug here, because the reader has to work out whether "settings" and
"config" are the same thing.

Common rotations to kill: check/verify/confirm/validate, run/execute/invoke/launch,
error/issue/problem/failure, delete/remove/destroy, config/settings/options.

Decide the vocabulary before you draft, not during editing.

**One instruction per sentence.** If a step has an "and" joining two actions, it's two
steps.

Sequenced actions are the exception. When the second action only makes sense right after
the first, "then" keeps them in one sentence: "Generate a new token, then set it in
`BLOOM_API_TOKEN`." Splitting that into two numbered steps loses the ordering.

**Active voice.** Say who does it. Passive is acceptable in a description only when the
actor genuinely isn't known.

**No semicolons.** Two sentences.

## Error messages

Three parts, in order: what failed, the cause if you know it, then the fix as a direct
instruction.

- No: "Oops! Something went wrong. Please ensure your credentials are properly configured."
- Yes: "Connection to the database failed: the password for user `app` was wrong. Set
  `DB_PASSWORD` to the correct value, then connect again."

Never "Oops", never "Please ensure", never an apology in place of a cause. If you don't
know the cause, say what you observed and where to look.

## Incident notes and status updates

Lead with the numbers. Time window, blast radius, cause, current state.

- No: "We have identified an issue that may have impacted some users' ability to access
  the service. We apologize for any inconvenience."
- Yes: "Between 14:02 and 14:31 UTC, 12% of requests failed. A deploy at 14:00 removed the
  cache warmup step. We reverted it at 14:27."

This is the one rule shared with `writer`: real numbers, or say you don't have them. Never
invent one to fill the slot.

## Don't be so terse it's ambiguous

Cutting words is not the goal. Clarity is. Restore the articles and the "that" when they
prevent a misreading.

- Too terse: "Ensure file exists before running."
- Right: "Make sure that the file exists before you run the command."

Note this cuts against the eraser rule in `writer`. Here the tired reader wins.

## Leave these alone

Never rewrite: code, commands, config keys, identifiers, quoted error strings, log lines,
file paths, or anything inside backticks. Copy them exactly. A "cleaned up" command is a
broken command.

## Before you ship it

Search the draft for these and fix each hit:

- `should`, `may`, `might`, `could` (make it must/can, or delete)
- `;` (split into two sentences)
- Sentences over 20 words in a procedure, 25 in a description
- The same concept called two different names
- `Please ensure`, `Oops`, `Simply`, `Just`
- Any command or identifier you paraphrased instead of copying

## Not compliance

This is the useful subset of ASD-STE100, not the standard. Real STE compliance needs the
official dictionary and approved-word list. Don't claim a document is STE-compliant.
