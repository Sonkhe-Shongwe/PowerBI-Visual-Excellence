# REF-011 — Page Architecture

**Source:** Deneb repository README, dashboard layout specification and PBIP report definition  
**Status:** Source-level structure verified; Power BI Desktop rendering pending

## Report-level structure

The PBIP showcase contains 22 pages:
- One KPI Dashboard 2015 page.
- 21 individual template demonstration pages.

The individual template pages make the report function as a browsable component library.

## Page 1 — KPI Dashboard 2015

**Canvas:** 1600 × 900  
**Background:** dashboard-background.svg  
**Theme:** Fluent2-CY26SU07 base theme plus bi-nexus.json custom theme  
**Deneb visuals:** 12

### Top row: headline KPIs

| Component | Position (x, y) | Size (w × h) |
|---|---:|---:|
| Revenue KPI | 198, 189 | 264 × 235 |
| On-time delivery KPI | 552, 189 | 264 × 235 |
| Top customer KPI | 906, 189 | 264 × 235 |
| Top product KPI | 1260, 189 | 264 × 235 |

Each card has a white surface and shadow in the layout specification.

### Lower analysis: four columns

| Column | First row | Second row |
|---|---|---|
| Revenue | Revenue vs target/previous period | Discount rate vs target/previous period |
| Delivery | On-time delivery by shipper | Average freight cost per order |
| Customers | Top three customers by revenue | Average order value for top three customers |
| Products | Top three products by revenue | Average order value for top three products |

The first analysis row begins at y=508 with 310 × 156 px visuals. The second begins at y=736 with 310 × 132 px visuals.

### Text hierarchy

The dashboard layout includes:
- Main title: KPI Dashboard | 2015.
- Reporting targets.
- Key definitions for RM, RY and MoM.
- Reporting-month label.
- KPI panel title and description.
- Analysis title and description.
- Section titles/subtitles above each analytical visual.
- Footer attribution.

The text is designed to explain the report's reporting-month and reporting-year logic without requiring the reader to infer the abbreviations.

## Pages 2–22 — Template demonstrations

The remaining 21 pages demonstrate one template each.

The repository groups the templates by analytical purpose:
- KPI.
- Comparison.
- Time.
- Financial.
- Map and other analytical visuals.

Each template directory includes its specification, README, preview, sample data and render configuration. This makes the report a visual catalogue as well as a technical demonstration.

## Architecture lessons

1. A showcase dashboard can demonstrate how reusable components work together in a realistic layout.
2. A separate page for each template makes a large component library easier to browse.
3. Sample data and preview images help users understand a component before binding it to their own model.
4. A common theme allows components from different categories to feel like one coherent product.
5. The main dashboard shows a useful composition: headline KPI cards above supporting analysis, with repeated column widths and clear section labels.

## Unknowns

- Exact rendering in Power BI Desktop and Service.
- Actual interactive behaviour of each template.
- Runtime page navigation and any hidden states.
- Accessibility and keyboard behaviour.
- Whether the layout remains legible at smaller display sizes.
