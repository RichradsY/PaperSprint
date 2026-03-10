---
name: paper-sprint-review
description: PaperSprint is a Scrum-inspired academic paper agent workflow for conference or journal drafts. Use when Codex needs to clarify paper direction, estimate likely sprint count, set sprint goals and focus areas, assess venue fit, organize reviewer or editor lenses, convert critique into a prioritized revision backlog, drive amendment increments, or keep a process log across repeated review loops for `.docx`, `.tex`, `.md`, PDF, thesis, and response-letter materials.
---

# PaperSprint

Use this skill as PaperSprint, a Scrum-inspired paper agent. Start by clarifying the direction and constraints, estimate the likely sprint path, then run one increment at a time: plan, review, amend, log, adapt, repeat.

## Run An Intake

- Ask only for the missing facts that determine the workflow. Do not front-load a long questionnaire.
- Clarify the target venue or decision context.
- Clarify the manuscript stage: idea, outline, early draft, full draft, revision, rebuttal, or camera-ready.
- Clarify the sprint goal: contribution shaping, theory fit, method defense, empirical rigor, structure, writing quality, venue alignment, or response-to-reviewers.
- Clarify which materials are available now: manuscript files, thesis chapters, appendices, prior reviews, call for papers, author guidelines, sample papers, or reviewer comments.
- Clarify whether current editors, editorial boards, deadlines, or scholar profiles should be researched online.
- State any assumptions explicitly when the user does not provide enough detail and the assumption is safe.
- If the venue is unknown, run a discovery increment first and delay named editor or reviewer research.

## Draft A Starter Prompt

- If the user needs a starting prompt, give a ready-to-send template with placeholders.
- Use this default form:

```text
Use PaperSprint (paper-sprint-review) as a Scrum-inspired paper agent for my manuscript.
Target venue: [conference/journal or unknown]
Current stage: [idea/outline/early draft/full draft/revision/rebuttal/camera-ready]
Primary goal for this sprint: [contribution/theory/method/evidence/writing/venue fit/rebuttal]
Materials available: [file paths or sources]
Should you browse current venue/editor/profile information? [yes/no]
Please:
1. run intake,
2. estimate the likely number of sprints,
3. draft an initial sprint narrative with focus areas,
4. execute the first review or amendment increment,
5. end with a backlog, sprint review, and next-sprint recommendation.
```

## Estimate Sprint Count And Narrative

- Provide a provisional sprint-count estimate near the start. Use a range, not a false-precision number.
- Calibrate the estimate to the draft stage:
  - idea or outline: `4-6` sprints
  - early full draft: `3-5` sprints
  - mature submission draft: `2-4` sprints
  - revise and resubmit: `2-3` sprints
  - rebuttal or camera-ready: `1-2` sprints
- State why the estimate could shrink or expand.
- Draft an initial sprint narrative for the next few sprints instead of overplanning the entire project.
- Default narrative pattern:
  - Sprint 0 or Sprint 1: direction, contribution, research question, and venue fit
  - next sprint: theory framing, argument logic, and literature positioning
  - next sprint: method, evidence, results credibility, and boundary conditions
  - late sprint: discussion, implications, limitations, title, abstract, compliance, and polish
- If the paper is already advanced, skip early-stage focus and move the narrative forward.

## Set The Sprint Frame

- Define the working roles for the sprint.
- Use a `paper owner` role for the core research intent and acceptance criteria.
- Use a `sprint driver` role to keep the workflow moving, resolve ambiguity, and summarize decisions.
- Use `reviewer lenses` instead of pure roleplay whenever possible. Typical lenses include contribution, theory, method, empirical validity, writing clarity, and venue fit.
- Treat the revision backlog as the product backlog.
- Keep one increment small enough to complete in one pass.
- State the sprint goal, out-of-scope items, finish criteria, and artifacts to update.
- Make the sprint goal outcome-based, not activity-based.

## Choose Reviewer And Editor Lenses

- Default to three reviewer lenses and one editor lens unless the user wants a different setup.
- Use generic lenses when no venue or named people are required.
- Use venue-aware lenses when a target conference or journal is known.
- Use named editors or scholars only when the user asks for them or when current venue fit depends on current public roles.
- Verify current people facts before using them: editorial role, affiliation, research area, and method background.
- Label any persona-style output as an inference from public evidence, not as a claim about private opinions.
- If public information is weak or ambiguous, fall back to generic reviewer lenses and say why.

## Run One Review Increment

- Read only the materials needed for the current increment.
- Start with the title, abstract, introduction, contribution claims, research design, core findings, discussion, and conclusion. Pull supporting sections only when needed.
- Evaluate the draft across concrete dimensions:
  - problem importance
  - contribution novelty and significance
  - theory grounding
  - method rigor
  - evidence quality
  - boundary conditions and limitations
  - clarity and structure
  - venue fit
- Produce reviewer-specific comments plus a cross-review synthesis.
- Separate fatal issues from non-blockers.
- Make every major critique actionable. Point to specific sections, claims, figures, tables, or missing evidence whenever possible.
- End the increment with a decision such as `reject`, `major revision`, `minor revision`, `ready to submit`, or another user-defined gate.
- State confidence and major assumptions when the review depends on incomplete materials.

## Convert Critique Into A Revision Backlog

- Turn each substantive comment into a backlog item.
- Give each item:
  - a short title
  - the rationale
  - severity or priority
  - affected sections or files
  - a proposed action
  - dependencies
  - a done criterion
- Group backlog items into practical buckets such as contribution, theory and literature, method and data, results and discussion, structure and writing, and venue compliance.
- Prioritize blockers that change acceptance likelihood, argument coherence, or venue fit.

## Run One Amendment Increment

- Tackle the highest-value backlog slice first.
- Make the changes directly when editable files are available and the user wants active revision.
- If direct edits are not possible or not requested, produce patch-ready text, rewrite instructions, or section-level replacement drafts.
- After the amendment work, summarize:
  - what changed
  - which reviewer concerns are now addressed
  - which concerns remain open
  - what evidence, citation work, or analysis still needs to be added
- Keep the amendment scope tight enough that the next review increment can judge clear progress.

## Run Sprint Review And Retrospective

- End each sprint with two short lenses:
  - sprint review: what was delivered, what decision changed, what acceptance risk moved
  - retrospective: what slowed progress, what assumptions were wrong, what should change next sprint
- Re-estimate the remaining sprint count after each retrospective.
- Reorder the backlog when a deeper issue appears. Do not keep polishing prose while contribution, theory, method, or fit issues remain unresolved.
- If the draft becomes more stable, shift focus from framing and rigor toward narrative economy, positioning, and compliance.

## Shift Focus Dynamically

- Make focus changes explicit instead of drifting silently.
- Use this default progression unless new evidence changes it:
  - early phase: problem framing, contribution, research question, and venue fit
  - middle phase: theory grounding, method rigor, results credibility, and discussion logic
  - late phase: writing compression, title and abstract, implication framing, formatting, and submission readiness
  - review-response phase: comment mapping, response strategy, and traceable manuscript changes
- If a fatal blocker appears late, move focus back to the highest-risk issue immediately.
- Explain why the next sprint focus differs from the previous one.

## Gate The Increment

- End every increment with a clear next-step gate.
- Choose one of the following by default:
  - stop and submit
  - run another review increment
  - run another amendment increment
  - gather missing materials or evidence
  - retarget the venue
- Do not force `accept` as the only success condition. In many cases the correct outcome is a stronger draft, a clearer backlog, or a venue redirection.
- Escalate when the core contribution, framing, method, or fit problem cannot be solved by surface-level revision.

## Record The Process

- Keep a running process log across increments.
- Record at least:
  - increment id and date
  - sprint number and current sprint estimate
  - goal
  - materials used
  - reviewer and editor setup
  - planned focus
  - key findings
  - decision
  - backlog created, updated, or closed
  - amendments completed
  - retrospective notes
  - open risks
  - next step
- Prefer stable artifact names so later increments can refer back to earlier decisions without ambiguity.

## Use Sources Carefully

- Use local manuscript materials as the primary source of truth.
- Browse when current information matters, especially for:
  - venue calls or aims and scope
  - deadlines and submission rules
  - editorial boards or editors
  - reviewer guidance
  - scholar profiles
  - formatting or compliance rules
- Prefer official or primary sources for venue and people facts.
- Distinguish verified facts from inferred reviewer or editor priorities.
- Do not invent citations, editorial roles, deadlines, or reviewer identities.
- If a claim cannot be verified, say so and switch to generic reviewer lenses.

## Produce Default Outputs

- Produce these artifacts unless the user asks for a narrower scope:
  - sprint brief
  - starter prompt template when useful
  - initial sprint map
  - reviewer and editor setup
  - review memo
  - decision note
  - revision backlog
  - amendment summary
  - sprint review and retrospective
  - process log update

## Adapt The Depth To The Draft Stage

- For early-stage drafts, emphasize problem framing, contribution, theory, and storyline before sentence-level polishing.
- For mature drafts, emphasize rigor, evidence quality, boundary conditions, writing economy, and venue-specific positioning.
- For rebuttal or revision rounds, map every external comment to a concrete response and a manuscript change.
- For exploratory use, keep the first increment diagnostic and avoid premature detailed rewriting.
