# REF-003 — Page Architecture

**Source:** Creator's public Microsoft Fabric Community description  
**Status:** Page purposes and decision sequence documented; runtime inspection pending

## Report-level structure

The creator describes five pages. Each page answers a new question in the operator's investigation.

| Order | Page | Main question | User outcome |
|---:|---|---|---|
| 1 | Overview | Which systems need attention? | Select a system or group to investigate |
| 2 | Problems | What changed? | Distinguish new deterioration from older problems |
| 3 | Causes | Why is it happening? | Examine likely technical causes |
| 4 | Connections | What related systems may be affected? | Test shared-site and shared-data-feed relationships |
| 5 | Action | What should we do first? | Compare scenarios and prioritise fixes |

## Page 1 — Overview

**Purpose:** Establish system health and identify where to begin.

Creator-described elements:
- Map of all systems.
- Table of systems.
- Status colours.
- Equipment value.
- Alarm information.
- Buttons to show all systems, worsening systems or steady systems.

**Design questions for runtime inspection:**
- Is the map the primary entry point or a supporting visual?
- How are status categories defined and labelled?
- Does the table expose the reason for each system's priority?
- Is equipment value visible enough to influence the first investigation choice?

## Page 2 — Problems

**Purpose:** Compare each system with its own August baseline and separate new problems from existing ones.

The creator describes three views:
1. Where to start: equipment value against rising metrics.
2. Recent changes: a heatmap of all metrics.
3. Alarm sources: alarm hours by metric.

**Design questions for runtime inspection:**
- How does the report communicate the August baseline?
- How are new and persistent problems distinguished?
- Does the heatmap use consistent metric and time axes?
- Are warning and critical limits visible in context?

## Page 3 — Causes

**Purpose:** Investigate the mechanisms behind the observed problems.

The creator describes three views:
- Memory use across an average day.
- Self-hosted server versus Azure SQL comparison.
- A dependency chain from CPU to blocked sessions and deadlocks.

**Design questions for runtime inspection:**
- How are the cause relationships explained?
- Can the reader distinguish correlation from a proven causal relationship?
- Does the chain view identify the direction of dependency clearly?
- Can the operator move from an aggregate pattern to a selected system?

The exact chart types are not confirmed by the available description.

## Page 4 — Connections

**Purpose:** Determine whether worsening systems share a site or data feed.

The creator describes:
- Disk load over time for worsening systems.
- Comparison against each system's own August baseline.
- A control to test same-site relationships.
- A control to test shared-data-feed relationships.

**Design questions for runtime inspection:**
- How are related systems grouped or connected?
- Can the reader distinguish a shared location from a shared data dependency?
- Is the baseline comparison clear for each system?
- Does the report avoid implying that shared location alone proves a common cause?

## Page 5 — Action

**Purpose:** Convert investigation into a prioritised response.

The creator describes:
- A no-action scenario.
- A slider that advances the scenario through time.
- A ranked list of fixes.
- A slider that changes the priority balance between urgency and equipment protection.

**Design questions for runtime inspection:**
- Are scenario assumptions visible?
- Does the slider clearly explain its two ends?
- Are priority scores transparent and interpretable?
- Does each recommended action include an owner, effort or deadline?
- Can the user understand why a fix is ranked above another?

## Analytical flow

The report's structure can be represented as:

1. Detect — find systems that need attention.
2. Compare — establish what has changed relative to baseline.
3. Diagnose — examine possible causes.
4. Correlate — test whether related systems share the same pattern.
5. Decide — choose and prioritise actions.

This is the strongest architectural lesson currently supported by the source description.

## Unknowns

Not available from the inspected source:
- Canvas dimensions and page coordinates.
- Exact visual inventory and chart types.
- Navigation mechanism.
- Filter synchronisation.
- Tooltip and drillthrough configuration.
- Bookmark or field-parameter usage.
- Model relationships and DAX.
- Runtime and accessibility behaviour.

Do not infer these from the page descriptions alone.
