# REF-006 — Transferable Patterns

**Purpose:** Capture reusable ideas from the creator's description of OECD Global Well-being. These are design patterns, not claims about uninspected source implementation.

## 1. Reuse one component grammar across multiple domains

**Observed:** Three domains use repeated measure components containing a global average, SVG progress bar, trend and country table.

**Why it matters:** Readers can compare different domains without learning a new layout for every metric.

**Apply:** Define a reusable component contract: metric name, value, unit, scale, trend series, anomaly annotation and country-level values. Keep the component consistent while the selected measure changes.

## 2. Show global context before country detail

**Observed:** Each measure begins with the global average, then provides a trend and country table.

**Why it matters:** The reader gets a reference point before examining individual countries.

**Apply:** Use a benchmark or global average when it helps users interpret a selected entity. Label the benchmark and its population clearly.

## 3. Use SVG for compact, state-driven visuals

**Observed:** The report uses dynamic, colour-coordinated SVG progress bars.

**Why it matters:** SVG can provide precise control over a small repeated visual that may be difficult to style consistently with standard visuals.

**Apply:** Use SVG when a simple custom shape or compact indicator adds value. Keep labels and exact values accessible outside the SVG, and test scaling and screen-reader behaviour.

## 4. Connect the country table to the visual story

**Observed:** Selecting a country cross-filters the progress bar and trend.

**Why it matters:** The table is not just a static reference. It becomes a navigation and exploration control.

**Apply:** Configure interactions intentionally so selecting an entity updates the relevant visuals without unexpectedly filtering unrelated context.

## 5. Treat anomaly detection as a prompt for investigation

**Observed:** The trend uses anomaly detection to highlight deviations from expected values.

**Why it matters:** A trend can reveal unusual periods that deserve attention.

**Apply:** Explain the expected pattern, the detected deviation and the relevant time period. Do not imply that the anomaly detector has identified the cause.

## 6. Use domain-specific colour as contextual identity

**Observed:** Each domain has a dynamic background colour and accent image; titles and subtitles adapt to the selected domain.

**Why it matters:** The user can recognise a change in analytical context.

**Apply:** Use a small set of semantic domain styles, but keep text labels and selected states explicit. Maintain contrast and do not rely on colour alone.

## 7. Use small multiples for repeated comparisons

**Observed:** The gender-disparity page uses small multiples and dynamic titles/subtitles.

**Why it matters:** Repeated panels support comparison across countries or categories while preserving a common chart grammar.

**Apply:** Keep scales comparable when the purpose is direct comparison. If scales differ, label them clearly and avoid misleading visual comparisons.

## 8. Make dynamic titles explain the selected context

**Observed:** Page and visual titles/subtitles update with the selected domain.

**Why it matters:** A visual remains understandable when its data changes.

**Apply:** Include the selected metric, entity, time period or comparison context in the title where needed. Keep the wording concise and avoid repeating information already obvious from the control.

## 9. Make composite weighting transparent

**Related, not yet confirmed in the published report:** A Reddit post about the live OECD challenge describes sliders that let users adjust six metric weights in a normalised composite score.

**Why it matters:** User-controlled weighting can expose how priorities change a ranking, but it also makes the score dependent on subjective choices.

**Apply:** If using weighted composites, show the active weights, normalisation method and score formula. Validate weight constraints and explain that different preferences can produce different rankings.

## What not to copy blindly

- A progress bar without a meaningful denominator.
- A dynamic colour scheme that sacrifices contrast.
- An anomaly marker that implies causal explanation.
- A weighted score without a clear normalisation and weighting model.
- Small multiples with incompatible scales presented as directly comparable.
- SVG components that hide the exact value or accessible description.

## Highest-value lessons

1. Use repeatable components for comparable measures.
2. Give users a global reference before country detail.
3. Connect table selection to relevant visual updates.
4. Use SVG selectively for compact custom indicators.
5. Make anomalies and composite scores explainable.
6. Keep dynamic visual styling accessible and semantically clear.

No personal project has been modified by this study.
