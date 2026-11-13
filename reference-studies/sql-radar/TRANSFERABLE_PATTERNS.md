# REF-008 — Transferable Patterns

**Purpose:** Capture operational dashboard design and engineering lessons from SQL Radar.

## 1. Detect drift before critical failure

**Observed:** The creator's premise is that no system has crossed a critical threshold, yet several are moving away from normal.

**Why it matters:** Threshold-only monitoring can miss deterioration until a system is already in a critical state.

**Apply:** Show current threshold, remaining headroom and recent drift together. Define baseline and drift rules explicitly.

## 2. Put threshold, headroom and drift in one compact row

**Observed:** A pill table presents threshold, headroom and drift status for every system.

**Why it matters:** Users can scan current risk and direction without opening several charts.

**Apply:** Keep the three values together and provide clear definitions in tooltips or a help panel.

## 3. Separate signal detection from diagnosis

**Observed:** Signal identifies where the problems are; Diagnosis investigates why a selected system is moving.

**Why it matters:** An overview should help choose where to investigate, while a diagnostic page should provide enough depth to explain the behaviour.

**Apply:** Keep the summary concise and use a selected entity to carry context into detailed analysis.

## 4. Compare against a known normal period

**Observed:** The Diagnosis page shows when metrics left their August normal.

**Why it matters:** A trend becomes more meaningful when the expected range or baseline is visible.

**Apply:** Document the baseline period, aggregation method, tolerance and rules for exceptions. Do not label a deviation as a failure automatically.

## 5. Classify changes, not just values

**Observed:** The assessment table asks whether each change is new, explained or shared.

**Why it matters:** The same metric value can imply different action depending on whether it is new, known or part of a wider issue.

**Apply:** Track issue novelty, explanation, recurrence and shared dependencies where the data supports it.

## 6. Combine criticality with signal

**Observed:** The Action page uses a criticality-versus-signal matrix to rank systems.

**Why it matters:** The strongest technical signal is not always the most important business risk.

**Apply:** Combine likelihood/severity with operational criticality and make the axes and ranking logic transparent.

## 7. Use a runway timeline for action urgency

**Observed:** The report uses a runway timeline to rank systems and show when action is needed.

**Why it matters:** A priority list without time context does not tell the operator how quickly to respond.

**Apply:** Include deadline, expected time-to-impact or remaining runway only when the underlying calculation is defensible.

## 8. Separate native analysis from custom experience

**Observed:** Native visuals handle data and interactions; HTML handles the map, animated timelines, identity cards and intro.

**Why it matters:** The architecture uses native Power BI behaviour for core analysis and custom code for the elements that need distinctive presentation.

**Apply:** Start with native visuals for filtering, cross-highlighting and tooltips. Add HTML/SVG only where the experience benefit justifies the dependency.

## 9. Use report-page tooltips for depth without clutter

**Observed:** The creator says the native charts and matrix use report-page tooltips.

**Why it matters:** Detailed context can be available on demand without permanently expanding the main page.

**Apply:** Use tooltips for definitions, supporting metrics and secondary detail. Keep essential conclusions visible on the canvas.

## 10. Make the action plan operational

**Observed:** The Action page gives each system an action and a deadline, with a one-click email brief.

**Why it matters:** The report is designed to produce an operational response rather than just a monitoring insight.

**Apply:** Include owner, action, priority and deadline where supported. Make outbound communication traceable and reviewable.

## 11. Use persona to make an assistant memorable, but keep answers grounded

**Observed:** Mercury and Glitch provide the same page summary and answers with different personalities in light and dark modes.

**Why it matters:** A distinctive assistant can make a complex report feel more approachable.

**Apply:** Keep personality separate from factual content. Ensure answers are grounded in the visible data, identify uncertainty and provide a non-chat alternative for essential information.

## What not to copy blindly

- Drift detection without a stable baseline.
- A criticality matrix with opaque weights.
- A runway forecast without validated assumptions.
- Animated HTML where a static native visual is clearer.
- An assistant that gives untraceable answers.
- One-click email actions without a review step or audit trail.

## Highest-value lessons

1. Show drift before threshold breach.
2. Put threshold, headroom and trend in one compact view.
3. Separate detection, diagnosis and action.
4. Prioritise by both signal and criticality.
5. Use native visuals for core interactions and HTML for the experience layer.
6. End with action, deadline and a communication path.

No personal project has been modified by this study.
