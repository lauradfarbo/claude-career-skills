---
name: cv-builder
description: Builds or updates a CV/resume from a career file, compressing raw wins and STAR stories into scannable, quantified bullets tailored to a role, audience, or application. Use whenever someone wants to write, update, tailor, or shorten a CV or resume, or says "help me apply for this role" or "I need a version of my CV for X." Requires a career file from career-foundation — if none exists, send the person there first rather than interviewing from scratch. Handles career files at any level of completeness — rich roles get full bullets, thin roles get honest scope-only lines or get flagged for follow-up rather than inflated. Never manufactures results or metrics absent from source material. Defaults to a clean single-column, ATS-safe layout (see references/default-style-guide.md) when there's no existing CV to match, or the existing one uses a two-column/sidebar layout.
---

# CV Builder

Compresses a career file into a CV — a different, tighter register than the
`star-story-builder` output. A STAR story is told; a CV bullet is scanned.
Same underlying facts, much shorter shape, always led by a verb and a
number where a number exists.

Read `references/worked-example.md` before writing bullets — it shows the
compression pattern for well-detailed wins, and, just as importantly, the
right and wrong way to handle a thin one. Handling thin material honestly
is not an edge case for this skill — it's a core, expected scenario. Real
career files are uneven: some roles will have rich detail, others will be
a single scope line with nothing confirmed yet. This skill has to produce
a usable, honest CV either way, for anyone, on any given day of their
career-file's completeness.

## Step 0: Confirm there's a career file to work from

Ask for the person's career file if it isn't already available. If it
doesn't exist, point them to `career-foundation` first rather than
re-running an interview here — this skill consumes the file, it doesn't
build it.

## Step 1: Clarify what this CV is for

A CV changes shape depending on its audience. Ask (use `ask_user_input_v0`
for the closed parts):

- **Purpose:** a specific job application, a general-purpose CV to keep on
  hand, or a tailored version for a particular type of client/audience
  (e.g. a consulting one-pager aimed at a certain kind of buyer)?
- **If tailored:** what's the target role, posting, or audience? Ask for
  the actual job description or a description of the audience if one
  exists — relevance selection in Step 2 depends on this.
- **Length/format constraint:** one page, two pages, no constraint? Any
  required format (a specific template, a company's application portal
  fields, plain text for an ATS)?

Don't skip this step even if the person just says "update my CV" — a
general-purpose CV and a tailored one make different selection and
ordering decisions, and guessing wrong means redoing the work.

## Step 2: Select what goes in, based on relevance not just recency

Work through the career file's Timeline and Wins & Projects sections.

- Recent and directly relevant roles get full treatment: multiple bullets,
  drawn from their best-detailed wins.
- Older or less relevant roles typically compress to the role's one-line
  scope description rather than full bullets — this is normal CV practice,
  not a shortcut. Don't pad an irrelevant older role with bullets just
  because material exists for it.
- If the request is tailored to a specific role/audience (Step 1), weight
  selection toward wins whose skills-demonstrated tags match what that
  audience cares about, even if a more impressive but less relevant win
  exists elsewhere in the file.
- A role with only thin/raw wins is not a reason to skip the role — the
  role still belongs in the timeline with its scope line. It's a reason to
  keep that role's bullets minimal and honest rather than inventing depth
  it doesn't have. See Step 3 and the worked example for exactly how.

## Step 3: Compress into CV bullets

For each win selected in Step 2, follow `references/worked-example.md`:

- **Ready material** (capture status "detail complete," "metrics
  confirmed," or "polished"): compress into one strong sentence, verb
  first, number in the first clause if one exists. Add a second
  sub-bullet only if the role warrants extra depth.
- **Thin material** (capture status "raw" or "raw, unconfirmed"): never
  write a bullet that implies a result the source doesn't contain. Offer
  the person the choice laid out in the worked example — a scope-only
  bullet with no invented outcome, or omit the win from this CV and flag
  it in the career file's Open Threads for a `career-foundation` pass.
  Make this an explicit, visible choice in your response, not a silent
  default — the person should see that a bullet was softened or dropped
  and why.
- Never invent a verb-forward, confident-sounding bullet from a vague
  scope description. "Managed X" describing what the person was
  responsible for is fine; "Drove significant improvement in X" describing
  an unconfirmed outcome is not.

## Step 4: Assemble and format

- Group by role under company, most recent first, per standard CV
  convention, unless the person's target format requires otherwise.
- Pull contact info, education, and skills/tools sections directly from
  the career file's Snapshot and Skills & Tools Inventory.
- **Default layout:** if the person has no existing CV to model from, or
  their existing CV uses a two-column/sidebar layout, use
  `references/default-style-guide.md` as the default — a clean,
  single-column, ATS-safe structure. Say plainly when this default is
  being applied and why (e.g. "your current CV uses a two-column layout,
  which can get garbled by applicant tracking systems — I've used a
  single-column structure instead"), rather than silently overriding
  their existing format.
- If the person has an existing single-column CV already, match its
  established structure rather than reapplying the default guide over
  it — the guide is a fallback, not a mandate.
- For output format: a plain-text or markdown draft is usually the right
  first pass so the person can review content before formatting is locked
  in. If they want an actual downloadable Word document, check for and
  follow the `docx` skill's guidance rather than hand-rolling formatting —
  CVs have real formatting conventions (margins, consistent heading
  styles) that skill handles properly.
- Don't finalize formatting before the person has signed off on content —
  bullet selection and wording are the real decisions here, formatting is
  secondary.

## Step 5: Close the loop with the career file

This skill reads from the career file; it doesn't need to write the CV
itself back into it. But if Step 3 surfaced wins that got softened or
dropped for being too thin, add or update those items in the career file's
Open Threads so a future `career-foundation` session picks them up — the
same way `star-story-builder` does. This is what keeps thin spots from
staying invisible just because a CV got produced despite them.

## Anti-patterns to avoid

- Don't manufacture a metric, outcome, or confident verb from source
  material that doesn't support it — this is the single most damaging
  failure mode for a CV builder, since a CV is read as a factual claim
  about the person, more than a STAR story or a website bio is.
- Don't treat a thin career file as a blocker — produce the best honest
  CV possible from what exists, and be transparent about what got left
  thin or left out, rather than declining to help until every entry is
  perfect.
- Don't silently drop a win for being thin — say so, so the person can
  decide whether to go fill it in first.
- Don't write STAR-story-length prose into a bullet. If content still
  reads like a paragraph, it hasn't been compressed enough.
- Don't reorder or reweight a general-purpose CV as if it were tailored,
  or vice versa, without confirming which one was actually requested.
