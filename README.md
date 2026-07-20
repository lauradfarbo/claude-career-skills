# career-skills

A family of Claude skills for building career assets — CVs, interview
stories, positioning, website copy, case studies, LinkedIn content — all
sourced from one canonical career file instead of being written separately
from scratch each time.

## New here? Start with this

If you've never used this before, here's the fastest path in:

1. **Enable code execution.** In Claude.ai, go to **Settings → Features**
   and turn on **Code execution and file creation**. Skills need this to
   run.
2. **Install each skill.** If you have the **Claude Desktop app**, just
   double-click each `.skill` file after downloading it — it opens
   directly in Claude and installs from there. If you're on **browser-only
   claude.ai**, go to **Settings → Customize → Skills**, click **+**, then
   **+ Create skill**, and upload each `.skill` file instead. Either way,
   do this once per skill — `career-foundation`, `star-story-builder`,
   `cv-builder` — and toggle each one on.
3. **(Optional, recommended) Create a Project** — a normal Claude Project,
   separate from the skills upload above — called something like "Career
   Builder." Skills work in any conversation once uploaded, but a
   dedicated Project gives you one place to keep your career file and
   revisit past sessions, rather than hunting through unrelated chats.
4. **Start a conversation and say:** *"Let's build my career file."* You
   don't need to know which skill does what, or that there even are three
   of them — that first line is enough to kick off `career-foundation`,
   and everything downstream will prompt you toward the right skill when
   you're ready for a CV, interview stories, or anything else in the
   family.

That's it. Everything past this point is background on how it works and
what each piece does — useful once you're in it, not required to start.

## What's a STAR story, and why bother?

STAR stands for **Situation, Task, Action, Result** — a way of structuring
a work story so it actually lands, whether you're telling it in an
interview, writing a case study, or just explaining what you did on a
project to someone who wasn't there.

Most people already have the raw facts sitting somewhere — old CVs,
memory, a deck they once presented — but tell them out of order, bury the
result, or lead with the action before the reader knows why it mattered.
STAR fixes that by forcing a consistent shape: what was going on, what you
were asked to do, what you actually did, and what happened as a result.
It's not a gimmick — it's the format that both interviewers and case-study
readers are already listening for, whether they'd name it that or not.

`star-story-builder`, below, is the skill that produces these.

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
produces. In practice you don't have to remember this — just say "let's
build my career file" and the chain takes care of itself; if you jump
straight to asking for a CV or interview stories with no career file yet,
the relevant skill will send you to `career-foundation` first rather than
guessing at your background.

## Skills in this repo

### `career-foundation`
Builds and maintains the career file. Designed as a multi-session process
— most people can't produce a complete career history in one sitting, so
this skill checks for an existing file and resumes from wherever it left
off, rather than restarting the interview from scratch. Before interviewing
from memory, it asks for any existing source material (old CVs, cover
letters, performance reviews, decks, testimonials, and similar) and skims
that first, so the person is confirming and filling gaps rather than
reconstructing everything from nothing. At the end of every session, it
tells you exactly what to say next time to pick up where you left off.

Handles thin or uncertain material honestly: a missing result gets logged
as missing, not invented. Career gaps and pivots get asked about directly
rather than smoothed over.

### `star-story-builder`
Turns raw wins from the career file into polished STAR stories (see "What's
a STAR story" above) — the format used for behavioral interview prep and
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

## Using these skills day to day

Each skill folder contains a `SKILL.md` and, where relevant, a
`references/` folder with worked examples and formatting guides. Once
uploaded (see "New here?" above), they trigger automatically when relevant
— you don't need to name them by hand. Just describe what you want ("help
me prep for an interview," "update my resume for this role") and Claude
picks the right one, redirecting to `career-foundation` first if there's no
career file yet to work from.

## What's next

More skills are planned for this family, building on the same career file:
an offer/positioning skill, a website content skill, a case study skill,
and a LinkedIn content skill. This README will grow as they're added.

