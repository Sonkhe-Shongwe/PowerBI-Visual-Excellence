# REF-008 — Page Architecture

**Source:** Creator's Microsoft Fabric Community description  
**Status:** Three-page purpose and interaction flow documented; PBIX/runtime inspection pending

## Report-level structure

The report is built around three pages, each answering one operational question.

| Order | Page | Main question | User outcome |
|---:|---|---|---|
| 1 | Signal | Where are the problems? | Identify systems drifting from normal |
| 2 | Diagnosis | Why is it moving? | Investigate timing, novelty, explanation and shared behaviour |
| 3 | Action | What should we do first, and by when? | Prioritise systems, assign actions and deadlines |

## Page 1 — Signal

**Purpose:** Detect early system drift before critical thresholds are breached.

Creator-described components:
- Pill table with threshold, headroom and drift status for each system.
- Three charts showing what is moving.
- Map showing where the systems are located.
- The HTML map zooms to the selected site.

The creator does not identify the exact chart types in the community post.

## Page 2 — Diagnosis

**Purpose:** Investigate why a selected system is drifting.

Creator-described components:
- Timeline showing when each metric left its August normal.
- Table comparing every metric with the last assessment.
- Classification of whether the deviation is new, explained or shared with another system.
- Report-page tooltips on native visuals.

The selected system provides the context for the investigation.

## Page 3 — Action

**Purpose:** Convert diagnosis into a prioritised response.

Creator-described components:
- Criticality-versus-signal matrix.
- Runway timeline.
- Ranked systems.
- Action plan with an action and deadline for each system.
- One-click email brief.

The exact matrix axes, runway definition and ranking calculation are not available from the description.

## Shared experience layer

The creator describes:
- Animated timelines.
- Identity cards.
- Introductory HTML experience.
- Mercury assistant in light mode.
- Glitch assistant in dark mode.

The assistant is present on every page and is described as summarising the page and answering a few questions.

## Reader journey

1. Identify a system with abnormal drift.
2. Select it and inspect when metrics moved away from normal.
3. Determine whether changes are new, explained or shared.
4. Compare criticality and signal.
5. Rank the response, assign an action and deadline.
6. Send the brief by email.

## Architecture lessons

- Keep the report focused on a clear three-step operational workflow.
- Separate early warning from critical threshold breach.
- Use a system selection to maintain context across pages.
- Keep diagnostic details available through tooltips and supporting tables.
- End with action, ownership/deadline and a communication step.

## Unknowns

- Canvas dimensions and visual coordinates.
- Exact chart types and map implementation.
- Navigation and page-state design.
- DAX and model structure.
- Baseline calculation.
- Criticality and signal formula.
- Runway timeline definition.
- Email implementation.
- Assistant implementation.
- Keyboard and screen-reader behaviour.
