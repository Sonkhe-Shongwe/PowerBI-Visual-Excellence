# Power BI Design Principles

**Status:** Initial principles; to be refined through forensic research and testing.

These principles guide our original reports. They are not a fixed theme or a substitute for understanding the audience and business problem.

## 1. Design for a decision

Before opening the canvas, define:
- Who will use the report?
- What decision or question must it support?
- What is the most important insight?
- What context is needed to interpret that insight?
- What action should the reader be able to take?

Every page and visual must earn its space.

## 2. Establish hierarchy before decoration

- Give each page one clear purpose.
- Put the most decision-relevant information where it is easiest to find.
- Group related information.
- Use consistent alignment and spacing.
- Avoid making every visual equally prominent.
- Use whitespace deliberately; do not fill the canvas just because space exists.

## 3. Build a coherent visual language

A report should have consistent rules for:
- Page backgrounds and surface layers.
- Typography and text hierarchy.
- Colour and semantic meaning.
- Margins, gaps and alignment.
- Card, border and corner treatments.
- Chart titles, labels, legends and tooltips.
- Selected, hover, focus and disabled states.

These rules should be documented as design tokens where possible and implemented through reusable themes and components.

## 4. Use colour with meaning

- Keep the palette controlled.
- Reserve semantic colours for meaningful status or change.
- Do not use colour as the only way to encode information.
- Check contrast and colour-vision accessibility.
- Ensure labels remain readable on every surface.
- Avoid arbitrary gradients and decorative colour that competes with the data.

## 5. Choose visuals for the analytical task

- Use a chart because its encoding answers a question, not because it looks impressive.
- Prefer clear comparisons and trends over novelty.
- Label units and time periods.
- Use appropriate scales and sorting.
- Avoid unnecessary 3D effects and misleading axis choices.
- Keep legends and labels close to the data they explain.
- Provide context for outliers, targets and meaningful changes.

## 6. Treat interactions as part of the design

Filters, bookmarks, buttons, drillthrough and tooltips should be discoverable and predictable.

- Make filter state visible.
- Provide a clear way to reset or return.
- Keep navigation consistent.
- Avoid hidden interactions with no visual cue.
- Do not make a static screenshot the only evidence of functionality.

## 7. Accessibility is not optional

- Maintain readable text sizes and contrast.
- Provide meaningful alternative text where appropriate.
- Do not rely on colour alone.
- Use logical reading and tab order where supported.
- Ensure charts communicate their key message in text.
- Consider keyboard, screen-reader and colour-vision needs.

## 8. Prefer maintainable engineering

Use the simplest technique that meets the design requirement.

1. Native Power BI visuals and formatting.
2. Report themes, shapes, buttons, bookmarks and field parameters.
3. DAX-driven SVG or HTML components where they provide real value.
4. Deneb / Vega-Lite or third-party visuals for specialised visualisation needs.

Advanced techniques must be documented, tested and justified. Avoid introducing a custom visual merely to imitate a small decorative detail.

## 9. Design for the actual canvas

- Record page dimensions and aspect ratio.
- Test the report at the expected display size.
- Check text wrapping and visual clipping.
- Avoid tiny labels that only work when zoomed in.
- Consider how the report behaves in Desktop and in the Service if both are target environments.

For phone layouts, reflow summary and detail components by reading priority. Check which desktop labels and controls need different treatment at phone width. [AdventureWorks Sales phone layout](../reference-studies/microsoft-2026-samples/PAGE_ARCHITECTURE.md#phone-layout)

## 10. Measure quality

A report is not complete because it looks attractive to its creator. It must pass visual, functional, accessibility and analytical checks.

Related: [Visual acceptance criteria](../quality-assurance/VISUAL_ACCEPTANCE.md) and [Benchmark scorecard](../research/BENCHMARK_SCORECARD.md).
