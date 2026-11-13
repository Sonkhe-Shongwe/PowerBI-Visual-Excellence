# REF-002 — Transferable Patterns

**Purpose:** Capture techniques that can improve original Power BI projects. These are lessons to adapt, not a specification to clone.

## 1. Give each page one analytical responsibility

**Observed:** Executive Summary, Performance, Ranking and Temporal Analysis have distinct purposes. The source also includes a 10 Year Overview detail page.

**Why it matters:** Users can move from headline context to dimensions, peer comparisons and historical patterns without every visual competing on one page.

**Apply:** Write one sentence for each report page: what question does it answer and what should the reader understand or decide? Remove visuals that do not serve that purpose.

## 2. Use a stable page shell

**Observed:** A consistent navigation rail, title/context region and light analytical canvas recur across pages.

**Why it matters:** Readers learn the navigation once and spend less effort reorienting themselves.

**Apply:** Define the report grid, navigation, title position, filter location and page background before designing each individual page. Adapt the shell to the number of pages and audience.

## 3. Use a native field parameter for metric switching

**Observed:** The Parameter table uses native field-parameter metadata and NAMEOF references to five metric measures.

**Why it matters:** A reader can switch the metric being analysed without requiring a separate copy of each visual or a bookmark for every metric.

**Apply:** Use a field parameter when measures have compatible meaning, units and visual behaviour. Make the selected metric clear in the title, axis, unit, tooltip and supporting text.

## 4. Treat metric directionality as part of the model

**Observed:** Housing affordability and emissions use inverted normalisation because lower values represent better performance. Transit, green space and livability use higher-is-better normalisation.

**Why it matters:** A generic positive/negative colour rule can communicate the wrong conclusion when a lower raw value is desirable.

**Apply:** Store or document the preferred direction of every KPI. Build the measure, trend classification, conditional colour and tooltip from the same business rule. Test both improving and declining examples.

## 5. Normalise only when comparison requires it

**Observed:** The report maps metrics with different scales onto a common 0–100 range before creating a general performance score.

**Why it matters:** It can make unlike measures comparable, but the result is only meaningful when the bounds, directionality and weighting are defensible.

**Apply:** Define min/max bounds, direction, weighting, missing-value handling and update policy. Explain the composite score to users. Do not average unrelated measures simply because they can be converted to percentages.

## 6. Pair a summary visual with context cards

**Observed:** The Performance page uses a five-dimension radar alongside cards for individual metrics and an overall baseline.

**Why it matters:** The radar provides a shape/pattern overview, while the cards expose exact values and explanatory context.

**Apply:** If using a radar chart, keep the number of dimensions modest and provide exact values elsewhere. Do not use radar charts for precise ranking or close comparisons.

## 7. Use repeated small multiples for repeated questions

**Observed:** Temporal Analysis uses five line charts with the same basic structure, one for each metric, and a benchmark line.

**Why it matters:** Readers can compare trends across dimensions without repeatedly learning a new chart layout.

**Apply:** Use small multiples when the question and scale are sufficiently consistent. If scales differ, label them clearly and avoid implying that visual slope magnitudes are directly comparable.

## 8. Make ranking explicit

**Observed:** The Ranking page uses five native clustered bar charts and dedicated rank cards.

**Why it matters:** Bar length communicates relative magnitude; the explicit rank card communicates position without forcing the reader to count bars.

**Apply:** Use a consistent sort order, clear labels and a visible benchmark. Make rank direction and tie handling explicit.

## 9. Organise DAX by responsibility

**Observed:** The report's 223 DAX measures are divided into 14 purpose-based folders: accessibility, tutorial, field parameters, HTML panels/cards/visuals, scoring, dimensions, ranking, temporal analysis, colours, titles, metrics and helpers.

**Why it matters:** Measure discovery and maintenance are easier when developers can navigate by intent.

**Apply:** Use consistent prefixes and folders or display folders. Separate base calculations, business logic, presentation measures and accessibility text as far as practical.

## 10. Separate HTML templates from DAX assembly

**Observed:** The repository exposes HTML templates with DAX insertion markers and separate CSS files. The full report measures assemble the dynamic output.

**Why it matters:** A template is easier to inspect and style when its markup and styles are visible outside a very long DAX string.

**Apply:** Keep component markup, styling and calculation responsibilities as separate as the chosen implementation allows. Document the data contract between a component and its measures.

## 11. Use contextual insight text sparingly

**Observed:** The Performance page contains a narrative insight card that names strongest and weakest dimensions and explains the selected city's profile.

**Why it matters:** A chart may show a pattern but not explain why it matters. A concise insight can help executives understand the implication.

**Apply:** Generate text only from defensible calculations. Keep it specific, concise and traceable to visible evidence. Avoid generic AI-sounding summaries or claims unsupported by the data.

## 12. Design accessibility alongside the component

**Observed:** The source includes explicit alt-text measures and tab-order settings; the creator states that the report was designed with accessibility in mind.

**Why it matters:** Custom visuals and visual effects can hide important information from keyboard and screen-reader users.

**Apply:** Include concise alt text, keyboard access, logical order, adequate contrast and non-colour cues. Ensure hover content has a keyboard/touch alternative and verify the live result.

## 13. Use bookmarks for interface states, not every analytical choice

**Observed:** The report uses a native field parameter for metric switching and bookmarks for tutorial, filter and notification states.

**Why it matters:** This separates analytical selection from interface-state management and avoids unnecessary bookmark duplication for each metric.

**Apply:** Use field parameters or slicers for data choices. Reserve bookmarks for meaningful interface states, guided sequences and navigation.

## 14. Treat media as a dependency

**Observed:** The report embeds illustrative data but references external image and MP4 URLs in DAX.

**Why it matters:** A report can open without external data connections and still depend on the internet for media.

**Apply:** Record external assets, licence, availability and fallback behaviour. Prefer embedded or approved assets when a report must work offline or in restricted environments.

## What not to copy blindly

- A 281-pixel sidebar on every report.
- A radar chart for every multi-metric comparison.
- A 0–100 composite score without defensible normalisation and weights.
- Hover-only cards that hide essential information.
- 223 measures or 74 HTML components when a smaller design would solve the problem.
- A video intro for a routine operational dashboard.
- Hardcoded metric bounds without a data maintenance policy.
- The exact blue palette and embedded background artwork.

## Highest-value lessons

1. Separate page responsibilities.
2. Use native field parameters for compatible metric switching.
3. Handle KPI directionality correctly.
4. Use repeated small multiples for repeated comparisons.
5. Organise DAX and HTML components by responsibility.
6. Make accessibility and external dependencies part of component acceptance.
7. Keep complexity proportional to the analytical need.

No personal project has been modified by this study.
