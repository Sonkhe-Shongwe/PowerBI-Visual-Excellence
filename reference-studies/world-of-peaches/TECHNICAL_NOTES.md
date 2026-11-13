# REF-001 — Technical Notes

**Source:** Public GitHub source repository  
**Status:** Source-level review complete; PBIX runtime validation pending

## 1. Repository inventory

The public source repository includes:

| Artefact | Observed inventory |
|---|---:|
| PBIX | 1 file listed |
| Standalone DAX files | 45 |
| HTML component templates | 17 |
| Separate CSS files | 16 |
| TMDL model source | Present |
| Report section and visual configuration | Present |
| Theme JSON | Present |
| Bookmark folders | 8 |
| Static image resources | Present |
| Custom visual package metadata | 2 HTML Content visual package references |

The counts above are based on the current public repository tree. The README describes 17 curated HTML components; the tree contains 16 CSS files, so at least one template does not have a matching separate stylesheet.

## 2. Semantic model

The model includes these main analytical tables:

- Peach Production
- Peach Trade
- Countries
- Year

The two subject-area tables are Peach Production and Peach Trade. Countries and Year are shared dimensions.

The TMDL relationship file contains four relationships:
- Peach Production.Year to Year.Year.
- Peach Trade.Year to Year.Year.
- Peach Production.Area Norm to Countries.Country Official.
- Peach Trade.Area Normalized to Countries.Country Official.

This is a two-fact/shared-dimension pattern, often described as a fact constellation or galaxy model. It is not simply one fact table with several dimensions.

The Year table is generated from 2010 through 2024. It is a year dimension, not a full daily calendar table.

The Countries table includes country names, ISO codes, region/sub-region, flag URL and derived country/continent fields.

## 3. Selector tables

The model contains calculated selector tables for report-specific choices:

- Page 1 - Metrics Slicer: Production, Export Value, Import Value, Trade Balance.
- Page 2 - Production Slicer: Production, Harvested, Yield.
- Page 2 - View Mode Slicer: Waffle, Table.
- Page 3 - Trade Flow Slicer: trade-flow selection.

The first three inspected selector tables use DATATABLE expressions. They are disconnected selection tables that can be read by DAX measures using SELECTEDVALUE.

The README describes the dynamic layer as field-parameter-driven. The exposed TMDL selector definitions inspected here are not sufficient to establish that these specific tables are native Power BI field parameter tables. Verify the complete PBIX metadata before using that label.

## 4. DAX and HTML rendering pattern

The report uses DAX measures to assemble dynamic HTML strings. The HTML Content visual renders those strings.

The inspected examples show:

| Component | DAX file | Observed role |
|---|---|---|
| KPI row | Page 1 - 001 - KPI Row | Dynamic production/trade KPIs, values, changes, icons and HTML cards |
| Overview trend | Page 1 - 002 - Overview Trend Chart | Builds a metric-dependent trend and SVG chart |
| Production waffle | Page 2 - 001 - Production Waffle | Builds dot-grid comparisons and table-oriented output |
| Volume efficiency | Page 2 - 002 - Volume Efficiency | Contextual insight panel |
| Trade insight | Page 3 - 001 - Trade Insight | Contextual country/region narrative and video-backed panel |
| Trade KPI tower | Page 3 - 005 - KPI Trade Tower | Stacked KPIs, comparisons and rankings |

The DAX measures use functions such as SELECTEDVALUE, CALCULATE, FILTER, ADDCOLUMNS, TOPN, MAXX, SUMX, DIVIDE, FORMAT and CONCATENATEX. Some measures generate long HTML/CSS strings directly.

The overview trend component uses a generated year series and concatenated values to produce an SVG trend. The production waffle component creates a dot-grid representation and supports a Waffle/Table mode. The trade insight component builds contextual text and uses a video element as its background.

### Engineering trade-off

This approach gives the creator precise control over component appearance and behaviour. However, a long DAX measure that generates HTML combines analytical calculation, string construction and presentation logic. This can become difficult to maintain and debug. For our projects, keep calculation logic, presentation tokens and component templates as separated as the chosen Power BI architecture allows.

## 5. Custom visual dependency

The report configuration references an HTML Content custom visual type. The repository includes two custom visual package metadata entries with closely related GUIDs.

The analytical pages use this custom visual for bespoke cards, charts and tutorial content. Native Shape Map, standard slicers and Page Navigator visuals remain in use.

Before adapting the pattern:
- Identify the exact custom visual name, publisher, version and licence.
- Confirm it is available in the target Power BI environment.
- Test rendering in Power BI Desktop and Power BI Service if both matter.
- Check export, printing, mobile and accessibility behaviour.
- Understand any HTML sanitisation, JavaScript or external-resource restrictions.

## 6. Theme and design tokens

The report includes a theme JSON named Peach.Themee.

The inspected theme includes:
- An extended data colour sequence.
- Text classes.
- Named visual-style groups for native visuals and controls.
- Action-button presets.
- Page navigator styles.
- Slicer and advanced-slicer styles.
- Chart, map and card formatting defaults.

The creator's public Episode 02 says the design tokens are expressed in CSS and translated into the Power BI theme JSON. The theme is intended to keep native visuals and HTML components visually consistent.

## 7. Report configuration and interaction

The report source includes:
- Five section definitions.
- Visual layout and configuration JSON.
- Page navigation.
- Eight bookmark folders: Tutorial 1–4 and Close 1–4.
- Hidden tutorial HTML components on the analytical pages.
- Image-based controls linked to page navigation, bookmarks or external URLs.
- Tab-order values in visual configuration.

The source suggests a guided tutorial layer that can be opened and closed while the reader remains on the current analytical page. Runtime behaviour still needs to be checked.

## 8. Data sources and refresh

The creator's README states that production and trade figures come from FAOSTAT and that the two CSV sources need to be repointed in Power Query to refresh.

The inspected TMDL confirms:
- Peach Production uses a local File.Contents path to a FAOSTAT CSV.
- Peach Trade uses a second local File.Contents path to a FAOSTAT CSV.
- Countries uses a Web.Contents URL for an ISO country/region CSV.
- Year is generated from a fixed 2010–2024 range.

The Power Query source for Peach Production filters out China, mainland and China, Taiwan Province of. The Peach Trade query filters out China, mainland, China, Taiwan Province of, China, Hong Kong SAR, China, Macao SAR and Sudan (former). The reason for each exclusion should be checked against the data definitions before adapting the logic.

## 9. External dependencies and unknowns

The source references or component examples indicate dependencies on:
- Google Fonts for Jost and Cormorant Garamond.
- Public image and video URLs.
- External icon URLs.
- The HTML Content custom visual.
- The local FAOSTAT CSV files.

Unknown or not yet verified:
- Exact custom visual publisher/version and current support status.
- Whether every external asset remains available.
- Power BI Service behaviour.
- Mobile layout behaviour.
- Rendering and export performance.
- Whether the report's accessibility claims pass a keyboard and screen-reader review.
- Exact refresh behaviour after replacing the local CSV paths.

## 10. Next technical verification

Open the PBIX in Power BI Desktop and:
1. Inspect the model view and validate relationships.
2. Inspect the complete theme and visual settings.
3. Test every selector and bookmark.
4. Verify the custom visual dependencies.
5. Refresh after repointing the CSV sources only if a refresh test is needed.
6. Check visual performance and accessibility.
7. Record observed behaviour separately from source-level inference.
