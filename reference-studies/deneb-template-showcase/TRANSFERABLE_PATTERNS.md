# REF-011 — Transferable Patterns

**Purpose:** Capture reusable engineering and visual-design lessons from the Deneb Template Showcase.

## 1. Treat each custom visual as a component with a contract

**Observed:** Each template declares its expected fields, data types, grain, provider and interactivity metadata.

**Why it matters:** Users can bind the right data without reverse-engineering the entire specification.

**Apply:** Document each custom component's required columns/measures, grain, units, null behaviour and expected interactions.

## 2. Parameterise presentation instead of hardcoding every style

**Observed:** Templates expose parameters for colours, labels, formats, spacing, dimensions and behaviour.

**Why it matters:** A single spec can adapt to multiple metrics and report themes.

**Apply:** Expose a small set of meaningful parameters. Avoid making every internal calculation configurable.

## 3. Use semantic theme roles

**Observed:** BI Nexus defines good, bad, neutral and sequential colours, and the specs use theme helpers.

**Why it matters:** The same semantic state can look consistent across different visuals.

**Apply:** Define semantic tokens for status, accent, surface, text and sequential scales. Use theme functions where the visual platform supports them.

## 4. Separate core business logic from visual geometry

**Observed:** Some specs calculate visual-specific variance, status and layout, while the model supplies base measures.

**Why it matters:** A visual can be reusable without making the semantic model responsible for pixel-level presentation.

**Apply:** Keep shared business definitions in DAX/model logic. Put chart-specific geometry, label placement and presentation calculations in Vega/Vega-Lite. Document the boundary.

## 5. Build visual fallbacks and missing-data states

**Observed:** Calendar Heatmap distinguishes empty days from zero values and filtered-out days. KPI components show n/a when a figure cannot be calculated.

**Why it matters:** Missing, zero and filtered-out are different states.

**Apply:** Design and test each state explicitly. Never let missing data silently look like a zero or a healthy status.

## 6. Make labels adapt to available space

**Observed:** Bullet Chart dynamically moves value labels inside or outside bars, wraps category labels and suppresses labels when rows are too thin.

**Why it matters:** Fixed labels can overlap or disappear when data or visual size changes.

**Apply:** Test the component at small and large sizes, with long labels and extreme values. Prefer a clear omission or tooltip to overlapping text.

## 7. Use responsive sizing

**Observed:** KPI Line Card and KPI Small Multiples calculate layout dimensions from the visual container.

**Why it matters:** Reusable components should remain legible when placed in different report grids.

**Apply:** Define a reference size, then scale margins, fonts, marks and layout from width/height. Set minimum readable sizes.

## 8. Use small multiples with explicit scale policy

**Observed:** KPI Small Multiples supports independent or shared scales.

**Why it matters:** Independent scales reveal local shape; shared scales support direct magnitude comparison.

**Apply:** Choose the scale based on the question and label the choice. Do not compare visual heights if each panel uses a different scale.

## 9. Use selection and highlight only when they serve the task

**Observed:** Template metadata enables selection/highlight for the Calendar Heatmap, while other templates disable them.

**Why it matters:** Interactivity should be deliberate, not switched on by default.

**Apply:** Specify which interactions the component supports and test the effect on other visuals.

## 10. Provide a preview and sample dataset

**Observed:** Every template has a README, sample data and preview image.

**Why it matters:** Users can understand a visual before connecting their own model.

**Apply:** For reusable components, provide a realistic sample dataset and a known-good preview state.

## 11. Validate the library automatically

**Observed:** The repository includes a metadata schema and template-check script.

**Why it matters:** A library of custom visuals can drift as templates, fields and provider versions change.

**Apply:** Validate required metadata, dataset contracts, file presence, preview generation and spec parsing as part of each update.

## 12. Preserve design attribution

**Observed:** Template documentation credits the designers and sources that inspired several components.

**Why it matters:** Reusable visual design is often built on prior work.

**Apply:** Preserve attribution and licence notices when adapting permitted templates. Check third-party assets separately.

## What not to copy blindly

- Deneb for a visual that native Power BI already handles well.
- A 1600 × 900 page size without considering the report's intended display.
- Complex calculations inside every visual.
- Independent scales when the reader needs direct magnitude comparison.
- Good/bad colours without checking metric direction.
- A template's defaults without adapting units, labels and business meaning.

## Highest-value lessons

1. Define data contracts for custom visuals.
2. Parameterise design and formatting.
3. Use semantic theme roles.
4. Separate business logic from visual geometry.
5. Handle missing data and responsive labels.
6. Include sample data, previews and automated validation.
7. Use custom visuals only when they add clear value.

No personal project has been modified by this study.
