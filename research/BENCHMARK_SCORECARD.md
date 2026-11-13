# Dashboard Benchmark Scorecard

**Purpose:** Evaluate the quality of Power BI reports consistently, rather than choosing references based on personal taste alone.

## Weighted rubric

| Dimension | Weight | What is evaluated |
|---|---:|---|
| Visual craftsmanship | 25 | Composition, polish, alignment, spacing, visual finish and intentional detail |
| Layout and information hierarchy | 15 | Page structure, grouping, scan path, emphasis and cognitive load |
| Data storytelling | 15 | Whether the report frames a question, reveals meaning and supports a decision |
| Chart quality and presentation | 10 | Appropriate encodings, labels, scales, legends, annotation and readability |
| Interaction and navigation | 15 | Slicers, bookmarks, drillthrough, tooltips, navigation and interaction feedback |
| Design consistency | 10 | Repeated patterns, typography, colour, component behaviour and visual states |
| Accessibility and readability | 10 | Contrast, legibility, alternative text, colour use, keyboard and screen-reader considerations |
| **Total** | **100** | |

## Rating scale

Rate each dimension from 0 to 5:

- **0 — Not assessable:** insufficient evidence or feature not inspectable.
- **1 — Weak:** substantial issues; little evidence of deliberate design.
- **2 — Developing:** partially effective but inconsistent or difficult to use.
- **3 — Competent:** clear and functional, with some refinement.
- **4 — Strong:** highly considered and consistently executed.
- **5 — Exceptional:** exemplary execution with clear transferable value.

A score of 0 for insufficient evidence must not be interpreted as poor quality. Mark the dimension N/A where the reference cannot be inspected and calculate a provisional score only when enough dimensions are assessable. Record the coverage percentage.

## Calculation

For a fully assessable report:

**Weighted score = sum of (dimension rating / 5 × dimension weight).**

For a partially assessable report, calculate a provisional score using only assessable dimensions and renormalise their weights to 100. Always display the evidence coverage beside the score.

## Additional technical metadata

Record separately from the visual score:

- Live report available: Yes / No / Unknown.
- PBIX available: Yes / No / Unknown.
- PBIP available: Yes / No / Unknown.
- Theme JSON available: Yes / No / Unknown.
- DAX source available: Yes / No / Unknown.
- HTML/CSS or SVG source available: Yes / No / Unknown.
- Deneb / Vega-Lite available: Yes / No / Unknown.
- Third-party custom visuals: list and verify.
- Licence verified: Yes / No / Partial.
- Reproducibility: High / Medium / Low / Unknown.

## Decision bands

| Score | Interpretation |
|---:|---|
| 90–100 | Exceptional benchmark |
| 80–89 | Strong reference |
| 70–79 | Useful reference |
| 60–69 | Selective learning value |
| Below 60 | Lower priority, unless it demonstrates a unique technique |

These bands are internal prioritisation aids, not an external industry certification.

## Scoring rules

1. Never score from a thumbnail alone.
2. Inspect the report at a usable size.
3. Record evidence for every rating.
4. Separate visual excellence from analytical correctness and technical quality.
5. A complex report is not automatically a good report.
6. A beautiful report is not automatically usable.
7. Revisit scores when a PBIX or source code becomes available.
8. Keep the original score and the reason for any later revision in the audit record.
