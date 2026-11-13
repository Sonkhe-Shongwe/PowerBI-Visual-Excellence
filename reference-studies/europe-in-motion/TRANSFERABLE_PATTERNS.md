# REF-007 — Transferable Patterns

**Purpose:** Capture lessons from Europe in Motion's creator-described report architecture and interactions.

## 1. Move from overview to exploration to comparison

**Observed:** Overview → Reading Between the Regions → Contrasts → Head-to-Head.

**Why it matters:** Users can start with a broad story, inspect a selected indicator, explore relationships and then compare two entities directly.

**Apply:** Structure multi-page reports around a natural analytical journey rather than grouping pages only by chart type.

## 2. Use dynamic cards as context selectors

**Observed:** Dynamic cards on Reading Between the Regions act as context switchers for key indicators.

**Why it matters:** The page can change the analytical question without making the user navigate to a separate page for every measure.

**Apply:** Use a clear selected state and update chart titles, units, benchmarks and summary text whenever the selected indicator changes.

## 3. Use a configurable scatter plot to explore trade-offs

**Observed:** The Contrasts page allows users to change X-axis, Y-axis and bubble-size indicators.

**Why it matters:** A scatter plot can reveal relationships that are not visible in separate ranking charts.

**Apply:** Keep axis names, units and scales visible. Explain what bubble size means. Ensure the selected indicators remain comparable and avoid interpreting correlation as causation.

## 4. Add a balanced-entity summary

**Observed:** The Contrasts page shows the top three most balanced countries per region based on selected metrics.

**Why it matters:** The reader gets a concise shortlist after exploring a multi-dimensional chart.

**Apply:** Define balance mathematically and expose the scoring logic. A balanced entity is not necessarily the highest-performing entity on every metric.

## 5. Use head-to-head comparisons for direct decisions

**Observed:** The final page compares two countries using independent filters and a central chart.

**Why it matters:** It reduces the cognitive effort of remembering values from two separate views.

**Apply:** Keep the two selections visually equal, use consistent scales and show the difference explicitly. Be careful when measures have different units or opposite directions.

## 6. Use dynamic colour as context, not decoration

**Observed:** The creator describes dynamic colours connected to the selected analytical context.

**Why it matters:** Colour can reinforce the selected indicator or dimension.

**Apply:** Define semantic colour roles and preserve them across pages. Make selected context explicit in text and ensure the palette remains accessible.

## 7. Use HTML Content selectively

**Observed:** The creator confirms HTML Content for KPI cards and HTML/CSS for animated text overlays.

**Why it matters:** A custom component can provide presentation control that may be difficult to achieve with a native card.

**Apply:** Use HTML only when the design need justifies the dependency. Keep base calculations in the semantic model and test the custom component's accessibility and rendering.

## 8. Make accessibility visible and testable

**Observed:** The employer says the winning report included a colour-blindness simulator.

**Why it matters:** Users can evaluate how the report communicates information under different colour-vision conditions.

**Apply:** Test the full report under common colour-vision simulations. Do not rely on hue alone; use labels, icons, patterns and contrast.

## 9. Use concise dynamic summaries

**Observed:** Reading Between the Regions includes a summary that updates with the selected context.

**Why it matters:** A chart may show a pattern, but a short summary helps users identify what changed.

**Apply:** Generate summaries from traceable calculations, identify the relevant entity/time/metric and avoid claiming causes without evidence.

## What not to copy blindly

- A configurable scatter plot if the audience only needs a simple ranking.
- A head-to-head page when users need to compare many entities at once.
- Dynamic colours without semantic consistency.
- Animated KPI overlays that obscure values or create distraction.
- A balanced-country ranking without a transparent definition.
- HTML Content when native cards meet the requirement.

## Highest-value lessons

1. Design a clear analytical journey.
2. Use dynamic context cards.
3. Explore trade-offs with configurable scatter plots.
4. Use direct head-to-head comparisons for focused decisions.
5. Make dynamic colour and summaries explain the selected context.
6. Treat accessibility as part of the report experience.

No personal project has been modified by this study.
