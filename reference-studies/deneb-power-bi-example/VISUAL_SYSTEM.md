# Visual System

## Evidence basis

The inspected repository tree contains a README, PBIX and Excel workbook, but no report screenshots or theme file. The PBIX was not opened. This document therefore records only the visual concepts named in the README and does not infer a full design system.

## Creator-described visual components

| Component | Described treatment | What is unknown |
|---|---|---|
| Taxonomy donut | Deneb donut with a taxonomy-style treatment; overlaid with an AI-generated visual | Exact taxonomy hierarchy, arc encoding, palette, labels, layout and overlay construction |
| Horizontal bar | Deneb horizontal bar with a dynamic marker | Marker meaning, position calculation, reference scale and selected-state styling |
| Tolerance spectrum | Deneb spectrum bar | Threshold bands, semantic colours, scale, label treatment and out-of-range behaviour |
| Report-page tooltip | Tooltip functionality is included | Tooltip layout, typography, visual hierarchy and content |
| Drillthrough page | Dedicated drillthrough page is included | Page composition and navigation treatment |

## Visual assessment

The reference is technically interesting because it explores visual forms beyond a standard native donut and bar chart. However, no screenshot was available in the inspected repository tree. We cannot judge whether the report is polished, readable, visually consistent, or aesthetically stronger than native Power BI alternatives.

No exact colour values, font family, type scale, canvas size, spacing, card style, contrast ratio, or accessibility claim is recorded. Those require inspection of the PBIX and screenshots.

## Design questions for Desktop inspection

- Does the taxonomy donut communicate hierarchy clearly, or does the overlaid composition create visual ambiguity?
- Is the dynamic marker labelled and distinguishable from the bar value?
- Are tolerance bands named and understandable without relying on colour alone?
- Are labels and tooltips legible at normal report zoom?
- Do all five pages use consistent typography, spacing and colour semantics?
- Can the visuals be understood by keyboard and screen-reader users?
- Does the report remain readable in Power BI Service and at different zoom levels?

## Do not infer

- Do not assign an aesthetic score from the README.
- Do not assume the AI-generated overlay is a separate visual or a Deneb layer until inspected.
- Do not assume the dynamic marker represents a target, threshold or average until its label and calculation are verified.
- Do not assume the tolerance spectrum uses a particular colour convention or statistical method.
