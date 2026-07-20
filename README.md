# career-skills

A family of Claude skills for building career assets — CVs, interview
stories, positioning, website copy, case studies, LinkedIn content — all
sourced from one canonical career file instead of being written separately
from scratch each time.

## How it works

Every skill in this family reads from the same file: a structured record of
someone's roles, wins, metrics, and skills, built by `career-foundation`.
Downstream skills consume that file and produce something specific from it
— a CV, a story, eventually a website or a positioning statement — without
re-asking the person to reconstruct their career history each time.

That file stays the single source of truth throughout. Raw capture and any
polished narrative both live in the same entry, in the same file. No skill
in this family maintains a separate, parallel copy of a fact that can drift
out of sync with where it started.

```
career-foundation  →  produces the career file
       ↓
star-story-builder →  turns raw wins into told stories (STAR format)
       ↓
cv-builder         →  compresses wins into CV bullets
```

Start with `career-foundation`. Everything else depends on the file it
produces.

## Skills in this repo

### `career-foundation`
Builds and maintains the career file. Designed as a multi-session process
— most people can't produce a complete career history in one sitting, so
this skill checks for an existing file and resumes from wherever it left
off, rather than restarting the interview from scratch. Before interviewing
from memory, it asks for any existing source material (old CVs, cover
letters, performance reviews, decks, testimonials, and similar) and skims
that first, so the person is confirming and filling gaps rather than
reconstructing everything from nothing.

Handles thin or uncertain material honestly: a missing result gets logged
as missing, not invented. Career gaps and pivots get asked about directly
rather than smoothed over.

### `star-story-builder`
Turns raw wins from the career file into polished STAR stories (Situation,
Task, Action, Result) — the format used for behavioral interview prep and
as source material for case studies. Only works from wins that already have
enough detail; thin entries get flagged and sent back to
`career-foundation` rather than filled in with invented specifics. Writes
the finished story back into the same career file entry it came from.

### `cv-builder`
Compresses the career file into CV bullets — a tighter, scanned register
than a STAR story. Handles career files of any completeness: well-detailed
wins get full, quantified bullets; thin or unconfirmed wins get honest
scope-only lines instead of a manufactured result, with the gap flagged for
a follow-up `career-foundation` pass. Defaults to a clean, single-column,
ATS-safe layout when there's no existing CV to match, or the existing one
uses a two-column/sidebar format — and says so explicitly rather than
silently changing it.

## Using these skills

Each skill folder contains a `SKILL.md` and, where relevant, a
`references/` folder with worked examples and formatting guides. Add the
skill folder to your Claude setup (or use the "Save skill" option if
you're working from a packaged `.skill` file) and it becomes available to
trigger automatically in relevant conversations.

## What's next

More skills are planned for this family, building on the same career file:
an offer/positioning skill, a website content skill, a case study skill,
and a LinkedIn content skill. This README will grow as they're added.
