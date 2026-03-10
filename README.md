# Paper Sprint Review

[English](./README.md) | [简体中文](./README.zh-CN.md) | [Français](./README.fr.md)

A Scrum-inspired paper agent skill for Codex.

This skill turns manuscript polishing into a repeatable Scrum-style loop: clarify the direction, estimate the likely sprint path, run a focused increment, convert critique into a backlog, amend the draft, review the sprint, adjust the next focus, and repeat only as needed.

<a id="quick-navigation"></a>

## Quick Navigation

- [Use This Skill Now](#use-now)
- [Workflow](#workflow)
- [Starter Prompt Template](#starter-prompt)
- [Sprint Estimate Heuristics](#sprint-estimates)
- [Typical Prompts](#typical-prompts)
- [简体中文](./README.zh-CN.md)
- [Français](./README.fr.md)

<a id="who-this-is-for"></a>

## Who This Is For

- PhD students turning thesis material into a paper
- Authors preparing a conference or journal submission
- Authors handling a revise-and-resubmit cycle
- Researchers who want structured critique instead of generic editing

<a id="use-now"></a>

## Use This Skill Now

Copy this into a Codex session and replace the placeholders:

```text
Use paper-sprint-review as a Scrum-inspired paper agent for my manuscript.
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

If you only want a fast first run, use:

```text
Use paper-sprint-review to run intake and sprint 1 for my draft. Estimate sprint count first and focus on the highest-risk issue.
```

## What It Does

- Clarify the paper goal, target venue, draft stage, and available materials before starting work.
- Estimate the likely number of sprints and set an initial sprint narrative instead of improvising from round to round.
- Build reviewer and editor lenses that are grounded in venue fit rather than loose roleplay.
- Run review increments that produce actionable critique instead of generic feedback.
- Convert critique into a revision backlog with priorities, dependencies, and done criteria.
- Drive amendment increments that directly revise the draft or produce patch-ready rewrite instructions.
- Keep a stable process log, sprint review, and retrospective across multiple loops.

<a id="workflow"></a>

## Workflow

```mermaid
flowchart LR
    A["Intake<br/>venue, stage, goal, materials"] --> B["Sprint Planning<br/>estimate sprint count and initial focus"]
    B --> C["Reviewer / Editor Lenses<br/>generic or venue-aware"]
    C --> D["Sprint Increment<br/>review and/or amendment work"]
    D --> E["Backlog Refinement<br/>priorities, actions, dependencies"]
    E --> F["Sprint Review<br/>what changed and what risk remains"]
    F --> G["Retrospective<br/>what to shift next sprint"]
    G --> H["Dynamic Replanning<br/>update focus and remaining sprint estimate"]
    H --> I{"Another sprint needed?"}
    I -->|"Yes"| C
    I -->|"No"| J["Stop or Submit"]
```

<a id="starter-prompt"></a>

## Starter Prompt Template

```text
Use paper-sprint-review as a Scrum-inspired paper agent for my manuscript.
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

<a id="sprint-estimates"></a>

## Sprint Estimate Heuristics

| Draft stage | Likely sprint count | Default focus |
| --- | --- | --- |
| idea or outline | `4-6` | contribution, framing, research question, venue fit |
| early full draft | `3-5` | theory logic, structure, method credibility |
| mature submission draft | `2-4` | evidence strength, discussion, polish, compliance |
| revise and resubmit | `2-3` | comment mapping, argument repair, response strategy |
| rebuttal or camera-ready | `1-2` | targeted fixes, traceability, final readiness |

These are starting estimates, not commitments. The skill should revise them after each sprint review and retrospective.

## How Focus Shifts Across Sprints

| Phase | Primary attention |
| --- | --- |
| early | contribution, problem importance, theory anchor, venue fit |
| middle | method rigor, evidence quality, results credibility, discussion logic |
| late | writing economy, title and abstract, implications, formatting, compliance |
| response round | reviewer comment mapping, response letter logic, traceable manuscript changes |

If a fatal blocker appears late, the next sprint should move back to that blocker instead of continuing superficial polish.

## Default Outputs

| Artifact | Purpose |
| --- | --- |
| `starter prompt template` | Kick off the workflow with the right setup fields |
| `sprint brief` | Align the current goal, scope, and assumptions |
| `initial sprint map` | Estimate sprint count and initial focus sequence |
| `reviewer and editor setup` | Define the lenses used in this increment |
| `review memo` | Capture reviewer-specific findings and synthesis |
| `decision note` | Record the current gate outcome |
| `revision backlog` | Turn critique into concrete next actions |
| `amendment summary` | Show what changed and what remains open |
| `sprint review and retrospective` | Explain progress, blockers, and focus shifts |
| `process log update` | Preserve continuity across increments |

<a id="typical-prompts"></a>

## Typical Prompts

```text
Use paper-sprint-review as a Scrum-inspired paper agent for my MISQ resubmission. The materials are draft.tex, reviewer-comments.md, and response-letter.md. Estimate sprint count first.
```

```text
Use paper-sprint-review to run sprint 1 for my conference draft. Focus on contribution, theory fit, and venue alignment. Browse official venue sources if needed.
```

```text
Use paper-sprint-review to convert the latest review memo into a backlog, run one amendment increment on the introduction and discussion, and finish with a retrospective.
```

## Why Users Can Find And Use It Quickly

- The repository homepage now exposes direct jump links to the main sections and the Chinese and French versions.
- The top of the README includes a copy-ready prompt so users do not need to interpret the full skill before trying it.
- The workflow diagram explains the operating model in one screen.
- The sprint heuristics give users an immediate expectation of effort and progression.

## Repository Structure

```text
paper-sprint-review/
├── SKILL.md
└── agents/
    └── openai.yaml
```

## Skill Files

- [`SKILL.md`](./SKILL.md): core workflow and operating rules
- [`agents/openai.yaml`](./agents/openai.yaml): display name, short description, and default prompt

## Design Notes

- Use local manuscript materials as the primary source of truth.
- Verify people, venue, deadline, and policy facts from primary sources when they may have changed.
- Prefer reviewer lenses over fictional personas unless named editors or scholars are explicitly needed.
- Treat each increment as small, inspectable work with a clear sprint goal, review, and retrospective.
- Re-estimate the remaining sprint count as the manuscript risk profile changes.
