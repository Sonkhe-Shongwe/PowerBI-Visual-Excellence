# REF-011 — Technical Notes

**Source:** Public GitHub repository, TMDL, PBIP report definition, theme and template specifications  
**Status:** Source-level technical study complete; runtime validation pending

## 1. Repository structure

The repository includes:
- 21 Vega/Vega-Lite template specifications.
- 21 README files.
- 21 preview images.
- 21 sample-data CSV files.
- Render configuration.
- A template metadata schema.
- Automated validation script.
- A PBIP showcase.
- A custom theme and background SVG.
- MIT licence.

## 2. PBIP showcase

The PBIP contains 22 pages:
- KPI Dashboard 2015.
- One page for each of the 21 templates.

The model TMDL references the individual template tables and the dashboard's Deneb datasets. The report definition registers:
- Fluent2-CY26SU07 base theme.
- BI Nexus custom theme.
- Dashboard background SVG.
- Deneb custom visual.

The inspected main dashboard page is 1600 × 900 and contains 12 Deneb visual placements. The Deneb visual configuration references version 1.9.1.0 and Vega-Lite 6.4.1 for the inspected component.

## 3. Template contract

Each specification includes user metadata describing:
- Name.
- Description.
- Author.
- Provider (Vega or Vega-Lite).
- Provider version.
- Dataset fields.
- Field types and kinds.
- Interactivity settings.

The repository includes a JSON schema for this metadata. The template README explains the required field mapping and the intended grain of each field.

This is a strong engineering pattern: the visual contract is documented next to the spec rather than left implicit in the code.

## 4. Deneb helper functions

The templates use Deneb helper functions such as:
- pbiColor() — read a colour from the Power BI theme or semantic colour role.
- pbiFormat() — use Power BI formatting context where supported by the template.

The exact availability and syntax depend on the Deneb version and provider. These helpers are not general Vega-Lite functions and should not be copied into a non-Deneb chart.

## 5. Representative specifications

### KPI Line Card

Provider: Vega-Lite 6.4.1.

Data contract:
- Month: date column.
- Value: numeric measure.
- Target: numeric measure.
- Is Reporting Month: numeric flag.

The spec calculates reporting-month value, month-over-month change, gap to target and reporting-year aggregate. It renders a target line, monthly trend and good/bad markers. A higherIsBetter parameter handles metrics where lower values are desirable.

### Bullet Chart

Provider: Vega-Lite 6.4.1.

Data contract:
- Category.
- Actual.
- Budget.
- Last Year.

The spec calculates variances, status, label positions and tooltip values. It layers a prior-year bar, actual bar and budget tick. Labels adapt their position depending on bar width and available space.

### Calendar Heatmap

Provider: Vega 6.2.0.

Data contract:
- Date.
- Sales (or another non-negative measure).

The spec builds a calendar grid, five colour steps, empty-day and filtered-out-day states, a peak-day ring and date-range selection. Optional target mode changes the visual from a sequential intensity scale to good/bad target status.

### KPI Small Multiples

Provider: Vega-Lite 6.4.1.

Data contract:
- Category.
- Date.
- Value.

The spec calculates latest value and change, creates sparklines, sorts categories and computes the number of panels that fit. It supports independent or shared scales.

### P&L Accounts Statement

Provider: Vega-Lite 6.4.1.

Data contract:
- Line.
- LineKey.
- LineClass.
- Actual.
- Budget.
- LY.
- YTD Actual.
- YTD Budget.
- YTD LY.

The spec derives variance, percentage variance, formatting, subtotal/total styling and row layout. The README reports a 165 ms Deneb render versus 4,978 ms for a SWITCH-based matrix on a 74.9-million-row fact table. The result is author-reported and not independently reproduced.

## 6. Automated validation and previews

The repository includes a validation script and metadata schema. Each template has sample data and a preview image. This makes it possible to check:
- Metadata completeness.
- Expected dataset fields.
- Provider/version information.
- Template documentation.
- Sample-data presence.
- Preview/render configuration.

The README documents a check command. The exact script should be reviewed before extending the library.

## 7. Calculation placement

The templates demonstrate that some visual calculations can be performed in the Vega/Vega-Lite spec rather than DAX:
- Variances.
- Status classification.
- Label formatting.
- Subtotals and row styling.
- Latest value and change.
- Normalised coordinates and layout.

This can make a visual self-contained, but it also moves business logic into the visual specification. Use it carefully:
- Keep core business definitions in the semantic model where they must be reused across the report.
- Keep visual-specific geometry and presentation calculations in the spec.
- Document the boundary so users know where a number is calculated.

## 8. Licensing and attribution

The repository declares MIT. Individual templates also credit source designers and inspirations. Retain those notices and attribution when adapting a template. The MIT licence does not remove the need to check third-party assets or external datasets used by a particular implementation.

## 9. Runtime validation still required

Not yet tested:
- PBIP rendering in Power BI Desktop.
- Deneb custom visual compatibility.
- Cross-filter and cross-highlight behaviour.
- Tooltips and context menus.
- Selection mode and date-range drag behaviour.
- Performance on a real user dataset.
- Accessibility and screen-reader behaviour.
- Export and Power BI Service compatibility.

## 10. Next technical action

Study the five representative templates in this order:
1. KPI Line Card.
2. Bullet Chart.
3. Calendar Heatmap.
4. KPI Small Multiples.
5. P&L Accounts Statement.

For each, understand the data contract, key transforms, parameter set, theme helpers, interaction metadata and limitations before considering a proof-of-concept.
