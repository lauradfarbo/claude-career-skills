---
name: star-story-builder
description: Turns raw wins captured in a career file into polished, tellable STAR stories (Situation, Task, Action, Result) — the format used for interview prep, application materials, and as source material for case studies and LinkedIn posts. Use this whenever someone wants to prepare interview stories, build a "story bank," practice behavioral interview answers, or turn their documented career wins into something they could actually say out loud. Requires a career file produced by the career-foundation skill — if one doesn't exist yet or the relevant win entries are still raw/unconfirmed, direct the person to career-foundation first rather than inventing detail to fill the gap. Trigger this even if the person asks for something narrower like "help me answer 'tell me about a time you...'" — that's exactly what this skill produces.
---

# STAR Story Builder

Takes raw win entries from a career file and turns them into polished,
tellable STAR stories — the kind of narrative someone could actually say out
loud in an interview, or hand to a case-study writer as source material.
This is the first "writing" stage in the skill family; everything before it
(`career-foundation`) is deliberately raw, and everything after it (CV,
case studies, LinkedIn content) builds on what this skill produces.

**If this is the person's first time using this skill, briefly explain what
STAR is before diving in** — don't assume the term is familiar. One or two
sentences is enough: "STAR stands for Situation, Task, Action, Result — a
structure for telling a work story so it actually lands, whether that's in
an interview, a case study, or just explaining what you did on a project.
Most people have the facts but tell them out of order or skip the part that
matters — STAR fixes that." Skip this explanation if the person's own
language shows they already know the format (they use the term unprompted,
or ask for "behavioral interview" prep specifically).

Read `references/worked-example.md` before writing any stories — it shows
the exact bar to hit: connected prose, nothing invented, specific detail
kept intact rather than smoothed into generalities.

## Step 0: Confirm there's a career file to work from

This skill does not run standalone. Ask for the person's career file (from
`career-foundation`) if it isn't already available. If it doesn't exist yet,
say so plainly and point them to `career-foundation` first — don't try to
shortcut it by interviewing them from scratch here, the two skills would end
up maintaining separate, drifting versions of the same facts.

## Step 1: Pick which wins to build into stories

Skim the career file's Wins & Projects section. Sort what you find into
three buckets:

- **Ready** — capture status is "detail complete" or "metrics confirmed."
  These have enough raw material to build a story from now.
- **Thin** — capture status is "raw" or "raw, unconfirmed (from uploaded
  document)." These are missing a Situation, a Result, or both. Don't build
  a story from these yet — flag them and suggest a quick round of
  `career-foundation`-style follow-up questions instead, or skip for now.
- **Already polished** — has a narrative field from a prior run of this
  skill. Ask if they want to leave it, or revise it.

Ask the person which wins they want turned into stories this session —
default to their most recent or most relevant role if they don't have a
preference, since that's usually what's freshest for interview prep.

## Step 2: Light confirmation pass, not a full re-interview

Before writing, do a quick check rather than a deep interview:

- If a raw entry has enough for all four STAR elements, you often don't
  need to ask anything — go straight to writing.
- If something is ambiguous (e.g. "Action" reads like a to-do list with no
  sense of what was hardest or most consequential), ask one or two targeted
  questions rather than working through the full S-T-A-R sequence again —
  the career file already did that work.
- Never invent a missing Situation, Task, Action, or Result. If something's
  genuinely missing after this light pass, mark the story as not ready and
  return to it after a `career-foundation` follow-up.

## Step 3: Write the story

Structure, per `references/worked-example.md`:

- **Topic** — short label
- **Goal** — one line, what the story is ultimately about achieving
- **Situation / Task / Action / Result** — connected prose, not bullet
  fragments. Each section should read like something a person would
  actually say, not a report.
- **Skills demonstrated** — tags at the end, useful for downstream skills
  and for the person to scan quickly when picking a story to tell.

Craft notes:

- Target roughly 150–300 words total — long enough to hold the real shape
  of what happened, short enough to say out loud without notes.
- Keep the single most specific, most human detail in the raw entry —
  don't smooth it into generic "successfully delivered" language. Specific
  beats impressive.
- Every claim must trace back to something in the raw entry. If polishing
  requires inventing a transition or connective detail, keep it generic
  enough that it isn't asserting a new fact (e.g. "I started by mapping
  the process" is fine scaffolding; "which took three weeks" is not, if no
  timeframe was given).
- Match the person's own voice where the career file has voice notes
  (Section 5). If there are none yet, default to plain, direct language —
  short sentences, no corporate buzzwords, no invented urgency.
- Don't editorialize about how impressive the result is — let the numbers
  and specifics do that work. Avoid words like "significant," "robust," or
  "seamless" doing the work a real number or detail should be doing.

## Step 4: Write the polished story back into the career file

For each win turned into a story, add the polished narrative into that
win's entry in the career file — don't replace the raw S-T-A-R notes,
append the story alongside them — and update capture status to "polished."
The career file stays the single source of truth for every layer: raw
capture and polished narrative both live in the same entry, so there's
never a second copy of a story that can drift out of sync with the facts
it's based on.

If the person wants a portable copy for a specific use (printed for an
interview, pasted into an email to someone else), generate that on request
as a one-off, but don't create a standing separate file that has to be kept
in sync — the career file is what gets updated and referenced going
forward.

## Step 5: Close the session

Note in the career file's Open Threads which wins still need a
`career-foundation` follow-up before they're ready for a story, and which
ones are done. Tell the person plainly what's in the story bank and what
still needs raw material before it can be turned into one.

## Anti-patterns to avoid

- Don't run a full `career-foundation`-style interview here — this skill
  assumes that work already happened. If it hasn't, send them back rather
  than duplicating it.
- Don't invent Situations, Tasks, Actions, Results, or metrics to complete
  a thin entry. A thin entry stays thin until confirmed.
- Don't let polish erase specificity — a generic-sounding story is a worse
  outcome than a slightly rough one that's still concrete.
- Don't create a standing standalone story file that duplicates what's in
  the career file — that's a second source of truth waiting to drift out
  of sync. One-off exports on request are fine; a maintained duplicate
  file is not.
