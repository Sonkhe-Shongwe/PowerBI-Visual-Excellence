# REF-003 — Transferable Patterns

**Purpose:** Capture decision-architecture lessons from AstraVale SQL Health. These are based on the creator's published description; they are not claims about uninspected implementation details.

## 1. Structure the report around the operator's next question

**Observed:** Overview → Problems → Causes → Connections → Action.

**Why it matters:** The reader is guided through a natural investigation rather than being asked to interpret a page full of unrelated monitoring metrics.

**Apply:** Design pages around the decisions the audience must make. Each page should answer one question and make the next action clear.

## 2. Compare systems with their own baseline

**Observed:** Each SQL database is compared with its own August level.

**Why it matters:** Different systems may have different normal operating patterns. A shared absolute threshold can miss meaningful deterioration that has not yet crossed a critical limit.

**Apply:** Consider per-entity baselines for operational monitoring. Define the reference period, aggregation method, seasonality handling and rules for baseline changes.

## 3. Distinguish new problems from persistent problems

**Observed:** The Problems page is designed to separate new changes from older problems.

**Why it matters:** A new deterioration may need a different response from a known, stable issue.

**Apply:** Track first-seen date, recurrence, duration and recent deviation from baseline. Make the distinction visible instead of relying only on red/amber/green status.

## 4. Combine threshold status with trend evidence

**Observed:** The report uses warning and critical limits as well as comparisons against each system's baseline.

**Why it matters:** Thresholds describe current severity; trends can reveal deterioration before a threshold is breached.

**Apply:** Show both threshold state and recent direction. Avoid treating a system as healthy solely because it has not crossed a critical line.

## 5. Use heatmaps to find patterns across metrics and time

**Observed:** A heatmap is used to review recent changes across every metric.

**Why it matters:** A dense monitoring table is difficult to scan for coordinated or recurring patterns.

**Apply:** Use a heatmap when the user needs to identify where and when changes cluster. Keep scales, labels and threshold meaning explicit.

## 6. Explain a technical cause chain

**Observed:** The report describes a chain from CPU pressure to blocked sessions and deadlocks.

**Why it matters:** Operators need more than a list of symptoms. They need a hypothesis about how one condition may lead to another.

**Apply:** Use a clear, directional cause model only when the underlying evidence supports the relationship. Label correlation and hypothesis appropriately.

## 7. Look beyond the selected entity

**Observed:** The Connections page tests shared physical sites and shared data feeds.

**Why it matters:** A local symptom may be part of a wider dependency issue.

**Apply:** Model important relationships such as location, shared services, data feeds, upstream dependencies and common ownership. Make it possible to explore connected entities without losing the original context.

## 8. Include business impact in technical prioritisation

**Observed:** The dataset includes the value of equipment dependent on each SQL system. The Action page allows the user to shift priority between urgency and equipment protected.

**Why it matters:** The most technically severe issue is not always the issue with the largest business consequence.

**Apply:** Combine severity with impact, asset criticality, service importance and effort. Explain the weighting so users can challenge the ranking.

## 9. Give users a no-action scenario

**Observed:** The Action page includes a view of what happens if nothing is done.

**Why it matters:** It provides a counterfactual against which remediation can be evaluated.

**Apply:** Use scenario analysis when assumptions and future consequences can be modelled responsibly. Clearly distinguish forecast, scenario and observed result.

## 10. Turn the final page into an action plan

**Observed:** The report ends with ranked fixes and scenario controls.

**Why it matters:** A monitoring report should help the operator decide what to do, not merely show what happened.

**Apply:** Include the recommended action, reason, priority, expected impact, effort and deadline where the data supports them.

## What not to copy blindly

- A five-page sequence for a simple dashboard.
- A baseline comparison without understanding seasonality or normal operating variation.
- A heatmap with unclear scales.
- A causal chain that implies proof when only correlation is known.
- A priority slider without transparent assumptions.
- Equipment value as the only business-impact measure.

## Highest-value lessons

1. Design around the decision journey.
2. Use entity-specific baselines when normal behaviour differs.
3. Show trend and threshold status together.
4. Investigate shared dependencies.
5. Connect technical severity to business impact.
6. Finish with an actionable response.

No personal project has been modified by this study.
