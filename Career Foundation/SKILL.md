---
name: career-foundation
description: Builds and maintains a person's canonical career history — every role, project, and win, captured with real detail and real numbers, not polished copy. This is the required first step before any CV, STAR story, offer/positioning, website, case study, or LinkedIn content work — those all read from the file this skill produces. Use this whenever someone wants to document their work history, capture their career wins, do a "career audit" or "career archaeology," build a base of material to write a CV or LinkedIn content from, or says anything like "I need to get my career story down" or "help me remember all my wins." Also use it when someone is partway through this process and returning to add more — check for an existing career file before starting fresh. Trigger even if the person's actual goal sounds like the downstream task (e.g. "help me write my CV" or "build my website copy") if no career file exists yet — foundation work comes first.
---

# Career Foundation

Builds a career asset file: a complete, structured, un-polished record of
someone's work history — roles, projects, wins, metrics, skills. This file is
the shared source of truth for a family of skills (STAR builder, CV builder,
offer/positioning, website content, case studies, LinkedIn content). Nothing
downstream should ask the person to re-explain their career from scratch —
that's what this skill is for.

This is explicitly a **multi-session process**. Most people cannot produce a
complete, detailed career history in one sitting — the good material surfaces
in layers, often only after they've warmed up on the easy stuff. Design every
session assuming it will be picked up again later, by this skill or a
different one.

## Step 0: Check for an existing file

Before anything else, ask whether the person has a career file from a
previous session — either uploaded, in their Project files, or otherwise
available. Look for something matching the structure in
`references/career-file-template.md`.

- **File found:** Read it. Check the Open Threads section first — that tells
  you exactly where to resume. Summarize where things stand in one or two
  sentences ("You've got 4 roles mapped and 6 wins detailed, RealWear and
  Augmate still need win capture") and ask if they want to continue there or
  go somewhere else in the file.
- **No file found:** Move to Step 1.

Never restart the interview from scratch if a file exists. Read it fully
before asking anything.

## Step 1: Gather source material before interviewing

If there's no existing career file, don't open with interview questions —
open by asking the person to upload whatever career documentation they
already have. Skimming real source material first produces a far better
skeleton than a blank-page interview, and it means the person spends their
effort confirming and filling gaps instead of reconstructing everything from
memory.

Ask broadly and make clear that partial is fine — most people won't have
most of these, and even one or two items help. Examples to prompt with:

- CV/resume — all versions they have, not just the current one (older
  versions often frame a role differently or list details later drafts cut)
- Cover letters (these reveal how they've pitched their own strengths before)
- Performance reviews — self-written and manager-written, 360 feedback
- Manager or colleague testimonials, LinkedIn recommendations
- Decks they've presented that include project overview + results — QBRs,
  retros, board updates, all-hands presentations
- Case studies already written or published, internal or external
- Award or promotion nomination write-ups
- Kudos, recognition, or "great job" messages (Slack/Teams threads, emails)
- Press mentions or quotes
- Existing portfolio or personal website content
- Prior job offers (useful for comp/scope benchmarking, not just wins)
- Old proposal or pitch decks they authored
- Project retros or postmortems
- Conference talk slides or speaker notes
- For technical roles: commit history, design docs, incident postmortems
- Client or stakeholder thank-you notes, exit interview notes

Once material comes in, read all of it before asking a single interview
question. Extract a draft timeline and draft win entries directly into the
career file, marking each pulled-in item as **raw, unconfirmed** — sourced
from a document, not yet confirmed in conversation. Then move to Step 2 and
use the interview to confirm, correct, and go deeper on what's already
drafted, rather than asking the person to repeat what a document already
says.

If the person has nothing to upload, that's fine — say so plainly and move
straight to Step 2 with a blank file.

## Step 2: Map the timeline first, detail second

Get the skeleton before the depth. Ask for a fast pass through every role —
company, title, dates, employment type — without going deep on any one of
them yet. This does two things: it gives the person a low-effort on-ramp, and
it gives you the full shape of the career so later questions can reference
what's coming ("we'll get to the founder years in a minute").

Use `ask_user_input_v0` for closed/categorical details where it speeds things
up (employment type, whether a role had direct reports, etc.) — but the
timeline itself is usually faster as an open free-text pass ("just list your
roles in order, doesn't need to be tidy").

## Step 3: Go role by role for wins and projects

Once the timeline exists, move through it — usually most recent first, since
that material tends to be freshest, but follow the person's energy if they
want to start somewhere else.

For each role, draw out specific projects or wins using a light S-T-A-R
structure, but keep it conversational — don't interrogate with four labeled
questions in a row. Useful prompts:

- "What's something you did in this role that you're actually proud of?"
- "What was broken or missing when you got there, and what did you do about
  it?"
- "Who else was involved, and what was specifically yours versus the team's?"
- "Do you have numbers for that — even rough ones?"

**On numbers specifically:** push once, gently, if someone says "I don't
remember" or waves it off — "even a rough range is useful, was it closer to
10 or 100?" But accept "I don't have exact numbers" as a real, valid answer
and record it as such rather than leaving it blank or inventing a number.
Never fabricate a metric.

**On career gaps, pivots, or non-linear moves:** don't treat these as
problems to smooth over. Capture what actually happened and ask what the
person did during that time, what they learned, or how it shaped what came
next. A gap becomes an asset when it's specific, not when it's hidden — that
reframing is more honest and more usable than a euphemism.

**Stay in capture mode, not writing mode.** Record what the person tells you
close to how they told it. Resist polishing sentences or tightening bullets
here — that's premature, and it's a different skill's job once the raw
material is complete. If the person starts self-editing out loud ("actually
that's not a big deal, skip it"), gently push back — undersold wins are the
most common failure mode at this stage, not overclaiming.

## Step 4: Skills, tools, and voice

Lighter pass. Ask what tools/platforms they use, any certifications, and
group their skills by theme rather than as a flat list — themes are what
positioning work will need later.

Voice and brand notes are optional at this stage. Capture what comes up
naturally (a phrase they used, a way they described something) but don't run
a full brand exercise here — that belongs to the offer/positioning skill,
once there's enough raw material to find real patterns in.

## Step 5: Save and close the session

Every session, regardless of how much got done:

1. Write or update the career file following
   `references/career-file-template.md`. Use `create_file` and save to the
   outputs directory.
2. Update the **Open Threads** section honestly — what's still raw, what
   still needs metrics, what questions are still open. This is what makes
   the next session (by this skill or a sibling skill) fast to resume.
3. Present the file to the person and tell them plainly: keep this file
   somewhere you can bring back next time — in your Project files if you're
   working in a Claude Project, or just re-upload it next session.
4. If their actual goal was a downstream deliverable (CV, LinkedIn content,
   website, case study, positioning) and the file now has enough material
   for it, say so and point them to the right next skill rather than making
   them ask.

## What "done" looks like

There's no fixed finish line — the file can always grow. But it's usable by
downstream skills once every role has at least one detailed win with a
result, and the skills/tools section is filled in. Tell the person this
threshold plainly if they ask "is this enough," rather than implying it needs
to be exhaustive before it's useful.

## Anti-patterns to avoid

- Don't write polished CV bullets or LinkedIn copy in this skill. That's a
  different job and doing it here creates two competing versions of the
  truth.
- Don't let one big war story crowd out smaller, real wins — the small ones
  are often what CV bullets and case studies actually need.
- Don't invent metrics, dates, or details to fill gaps. Flag uncertainty in
  Open Threads instead.
- Don't discard or overwrite prior content in the file without the person's
  say-so — additive by default.
