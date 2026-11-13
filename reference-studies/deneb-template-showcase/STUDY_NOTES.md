# REF-011 — Deneb Template Showcase: Study Notes

**Maintainer:** InsightfulAnalytics / Timothy Osborn  
**Original source:** https://github.com/InsightfulAnalytics/Deneb  
**Licence:** MIT  
**Study date:** 2026-11-13  
**Status:** Source-level technical study documented; runtime rendering pending

## Executive finding

Deneb Template Showcase is a reusable visual library, not simply a dashboard. It contains 21 Deneb templates, each supported by a specification, field contract, sample data, preview image and documentation. A 22-page PBIP showcase demonstrates the templates in Power BI.

The repository is valuable because it exposes the engineering discipline behind custom visuals:
- A typed data contract for each visual.
- Parameters for styling and formatting.
- Theme-aware colours through Deneb helper functions.
- Sample data and previews.
- A validation script and schema.
- A real showcase report.

The showcase itself contains a 1600 × 900 KPI dashboard page with 12 Deneb visual components, plus one page for each template.

## 1. Repository inventory

| Artefact | Observed inventory |
|---|---:|
| Reusable templates | 21 |
| Preview PNGs | 21 |
| Sample-data CSV files | 21 |
| Template README files | 21 |
| Showcase report pages | 22 |
| Custom theme | BI Nexus |
| Base theme | Fluent2-CY26SU07 |
| Custom visual | Deneb |
| Licence | MIT |
| Automated validation | Present |

The 22 showcase pages consist of one KPI Dashboard 2015 page and 21 individual template demonstration pages.

## 2. Template categories

The library covers several analytical jobs:

### KPI components
- KPI Line Card.
- KPI Gap Sparkline Card.
- KPI Bullet Tile.
- KPI Delta Tile.
- KPI Hit/Miss Strip.
- KPI Bar Card.
- KPI Progress Card.
- KPI Ring Progress Card.
- KPI Run Rate Card.
- KPI Scorecard.
- KPI Small Multiples.

### Comparison components
- Bullet Chart.
- Bullet Prior Period.
- Overlap Bar Share Lollipop.
- Overlap Bar Variance Lollipop.

### Time
- Calendar Heatmap.

### Financial
- P&L Accounts Statement.
- P&L Monthly Grid.
- P&L Odd Rows.

### Other analytical visuals
- Half Donut Gauge.
- Australia Choropleth.

The library is deliberately broader than a single dashboard's visual needs.

## 3. Showcase dashboard

The PBIP includes a page named KPI Dashboard 2015 with a 1600 × 900 canvas and a registered SVG background.

The layout specification defines 12 Deneb components.

### Top KPI row

Four cards, each 264 × 235 px, positioned at y=189:
- Revenue.
- On-time delivery.
- Top customer.
- Top product.

Their x positions are 198, 552, 906 and 1260.

### Lower analysis area

Eight analytical visuals are arranged in four columns:
- Revenue against target and previous period.
- Discount rate against target and previous period.
- On-time delivery by shipper.
- Average freight cost per order by shipper.
- Top three customers by revenue.
- Average order value for the top three customers.
- Top three products by revenue.
- Average order value for the top three products.

The first analysis row begins at y=508, with the second at y=736. Each column is approximately 310 px wide.

The dashboard's text explains the reporting month, reporting year, month-over-month change and target definitions. It includes an explicit note that the user can hover for tooltips.

## 4. BI Nexus design system

The report uses:
- Fluent2-CY26SU07 as the base Power BI theme.
- bi-nexus.json as the registered custom theme.
- dashboard-background.svg as a registered image resource.

The custom theme includes:
- A blue primary palette.
- A deeper navy blue.
- A lighter sky blue.
- Amber as a table accent.
- Semantic good, bad and neutral colours.
- Sequential minimum, centre and maximum colours.
- Visual style definitions.

Important theme tokens include:
- Primary blue: #1E6FD9.
- Deep blue: #0B3D91.
- Sky blue: #5DA9E9.
- Amber: #FFB703.
- Good: #1E6FD9.
- Bad: #D62828.
- Neutral: #94A3B8.
- Background: #FFFFFF.

The showcase layout uses additional semantic tokens for white, amber, ink, body and muted text.

## 5. Template engineering

Each template exposes a documented data contract:
- Field key.
- Display name.
- Data type.
- Column or measure kind.
- Description of the expected grain and meaning.

The specifications use user metadata to identify:
- Template name and description.
- Author and attribution.
- Vega or Vega-Lite provider.
- Provider version.
- Expected dataset fields.
- Interactivity settings.

The template library uses parameterised specifications. Parameters control titles, labels, formats, colours, dimensions, sorting and layout behaviour without rewriting the full specification.

The specs use Deneb helper functions such as pbiColor() and pbiFormat() to align visuals with the Power BI theme.

## 6. Representative template findings

### KPI Line Card

Inputs: Month, Value, Target and Is Reporting Month.

The specification calculates:
- Reporting-month value.
- Month-over-month change.
- Gap to target.
- Reporting-year figure.
- Target line and monthly good/bad markers.

A higherIsBetter parameter handles measures such as cost where lower values are desirable. Layout sizes scale from the container dimensions.

### Bullet Chart

Inputs: Category, Actual, Budget and Last Year.

The visual layers:
- A wide previous-year bar.
- An actual bar.
- A budget tick.
- Value and variance labels.
- A tooltip with absolute and percentage variances.

The variance calculations are performed in the Vega-Lite spec, so separate DAX variance measures are not required for this template.

### Calendar Heatmap

Inputs: Date and Sales.

The visual:
- Displays week columns by weekday rows.
- Uses five sequential theme-colour steps.
- Draws empty days distinctly from zero values.
- Rings the peak day.
- Supports click or drag selection to cross-filter a date range.
- Supports an optional target mode.

### KPI Small Multiples

Inputs: Category, Date and Value.

The grid:
- Reflows based on visual width and height.
- Sorts by latest value, change, name or incoming order.
- Displays a latest value, change and sparkline per category.
- Supports independent or shared sparkline scales.

### P&L Accounts Statement

Inputs: Line, LineKey, LineClass, Actual, Budget, LY, YTD Actual, YTD Budget and YTD LY.

The spec derives variances, percentage variances, subtotals, number formats and conditional colours from the base fields. The author says this reduces the work done by the semantic model and can outperform a matrix implementation.

The README reports a Performance Analyzer result of 165 ms for the Deneb build versus 4,978 ms for a SWITCH-based matrix on a 74.9-million-row fact table. These are author-reported figures, not independently reproduced in this study.

## 7. Automated validation

The repository includes:
- A template metadata schema.
- A script to check the template library.
- Sample data.
- Preview images.
- Render configuration.

This creates a repeatable way to validate and demonstrate each template. It is an important difference between a one-off custom visual and a maintainable visual library.

## 8. Critical evaluation

### Strengths

- Complete template data contracts.
- Consistent design tokens and theme-aware colours.
- Parameterised specifications.
- Sample data and preview images for each template.
- Automated validation.
- A full PBIP showcase.
- Good coverage of KPI, comparison, temporal, financial and geographic visuals.
- Clear attribution to source designers where templates are inspired by existing work.

### Trade-offs

- Deneb is a custom visual dependency that must be available and approved in the target environment.
- Complex Vega/Vega-Lite specifications require technical skill and maintenance.
- Moving calculations into a visual spec can make the visual self-contained, but may move business logic away from the semantic model.
- Custom visuals need independent performance, accessibility and Power BI Service testing.
- The author-reported P&L performance result needs reproduction on another dataset and environment before using it as a general claim.
- The 1600 × 900 showcase is a design demonstration; it should not be treated as a universal page-size recommendation.

## 9. Benchmark status

This is a technical component-library study, not a standalone dashboard aesthetic benchmark. No numerical dashboard score is assigned.

## 10. Next action

Select a small number of templates for deeper technical learning:
1. KPI Line Card.
2. Bullet Chart.
3. Calendar Heatmap.
4. KPI Small Multiples.
5. P&L Accounts Statement.

Understand their data contracts, parameters, transformations and interaction metadata before considering any use in a personal project.
