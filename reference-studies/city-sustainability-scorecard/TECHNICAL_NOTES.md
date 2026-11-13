# REF-002 — Technical Notes

**Source:** Public GitHub repository  
**Status:** Source-level review complete; PBIX runtime validation pending

## 1. Repository inventory

| Artefact | Observed count/status |
|---|---:|
| PBIX | 1, approximately 3.58 MB |
| DAX files | 223 |
| DAX purpose folders | 14 |
| HTML templates | 74 |
| CSS files | 29 |
| TMDL files | 9 |
| Bookmark JSON definitions | 72 |
| Custom visual package | 1 HTML Content visual |
| Page sections | 6 |

The repository tree also contains hundreds of visual-container configuration files. Many are associated with tutorial, filter, notification and state elements; this is not the count of simultaneously visible visuals.

## 2. Semantic model

The TMDL source defines these tables:
- City Metrics
- City Lookup
- City Slicer
- Page Parameter
- Parameter
- _Measures

### City Metrics

The table contains:
- City
- Year
- HousingAffordabilityIndex
- TransitScore
- GreenSpacePct
- EmissionsIndex
- LivabilityComposite

The table is populated in Power Query using Table.FromRows and embedded compressed data. The creator describes the dataset as illustrative and held in the model.

### City Lookup

The city lookup contains City, State, Country and Region. It is also populated through embedded Power Query rows.

### Relationships

The relationship file contains:
- An active relationship from City Metrics.City to City Lookup.City.
- An inactive relationship from City Metrics.City to City Slicer.City.

The reason for the disconnected/inactive City Slicer relationship and its intended use should be confirmed from runtime behaviour and the complete measure dependencies before adapting it.

### Parameter tables

The Parameter table has native field-parameter metadata (ParameterMetadata, kind 2) and uses NAMEOF references to five measures:
- Avg Livability Score.
- Avg Housing Affordability.
- Avg Transit Score.
- Avg Green Space.
- Avg Emissions.

This is a genuine native Power BI field parameter. It drives metric selection without requiring a separate copy of every visual or using bookmarks for each metric.

The Page Parameter table is a separate calculated DATATABLE with page labels 1-5, 6-10 and 11-12. It appears to support paginated ranking/display logic; verify the interaction in Power BI Desktop.

## 3. DAX organisation

The 223 standalone DAX files are grouped into 14 folders:

| Folder | Measures | Purpose |
|---|---:|---|
| 01-accessibility-alt-text | 24 | Screen-reader descriptions |
| 02-tutorial-walkthrough | 23 | Guided tutorial steps |
| 03-field-parameters | 2 | Dynamic metric icon/description |
| 04-html-panels | 4 | Filter, notification and insight panels |
| 05-html-cards | 16 | KPI and ranking cards |
| 06-html-visuals | 7 | Radar, sparklines, headers and video intro |
| 07-normalisation-scoring | 7 | Metric normalisation and composite scoring |
| 08-dimensions-strongest-weakest | 6 | Strongest/weakest dimension analysis |
| 09-ranking | 18 | City ranking, gaps and ranking display |
| 10-temporal-analysis | 47 | Trends, YoY, peak/lowest year and period change |
| 11-colours-and-icons | 16 | Conditional colour and icon selection |
| 12-titles-and-text | 24 | Dynamic titles, subtitles and context |
| 13-metrics-and-aggregates | 19 | Base measures, averages and metric selection |
| 14-helpers | 10 | Supporting utility measures |

The folder structure is an important learning point: a large measure library becomes easier to navigate when organised by purpose rather than stored as one unstructured list.

## 4. Metric normalisation and directionality

The source includes min-max normalisation measures.

Higher-is-better dimensions:
- Transit Score: range 43.63–89.19.
- Green Space: range 27.73–55.05.
- Livability: range 48.00–68.54.

Lower-is-better dimensions, so the formula is inverted:
- Housing Affordability Index: range 24.58–53.39.
- Emissions Index: range 30.29–66.89.

The General Performance Score measure takes the five normalised values, averages them equally and divides by 100.

The displayed Avg Livability Score measure is separate: it averages City Metrics[LivabilityComposite]. Do not assume the two measures are interchangeable. Code search did not establish that General Performance Score is bound to a visible report visual.

The min/max values are hardcoded in the normalisation measures. This can be acceptable for a fixed illustrative dataset, but a reusable solution needs an explicit policy for updating the bounds when the data range changes.

## 5. Temporal analysis

The DAX folder includes measures for:
- Year-on-year change.
- Period change.
- Trend direction.
- Peak and lowest year.
- Biggest drop.
- Years above average.
- Current gap against a benchmark.

Directionality matters. For Housing and Emissions, a decrease can represent improvement. The source includes trend classification that treats a sufficiently negative percentage change as improving and a sufficiently positive change as declining.

Review generic and metric-specific period-change measures before reusing them: some source variants use fixed 2015/2024 boundaries, while dimension-specific measures derive the first and last visible year from the current context.

## 6. HTML/CSS component architecture

The repository contains 74 HTML templates and 29 CSS files. The templates use <!--{DAX}--> markers to identify dynamic values that are injected by DAX when the report renders the component.

Examples include:
- Executive Summary KPI cards.
- Rank cards.
- Metric selection and icon elements.
- Filter panel.
- Notification panel.
- Performance radar.
- Performance insight panel.
- Tutorial steps.
- Historical peak cards and YoY pills.
- Welcome video intro.

The report's _Measures table contains the working DAX that assembles the dynamic HTML strings. The separate templates are extracted references, not a complete standalone component runtime.

## 7. Custom visual dependency

The report configuration references one custom visual:
- Name: HTML Content.
- Publisher/author in package metadata: Daniel Marsh-Patrick.
- Version: 1.6.0.0.
- Purpose: render column or measure values as HTML in Power BI.

The report also uses native Power BI visuals, including:
- Clustered bar charts.
- Line charts.
- Tables.
- Action buttons.

The custom visual should be checked for availability, version compatibility, licensing and Power BI Service behaviour before adapting the approach.

## 8. Theme and page resources

The report JSON references the Power BI base theme CY25SU11. The public source tree does not expose a separate report-specific custom theme JSON.

The page backgrounds are embedded SVG resources, each 1280 × 720, with a dark navigation rail and light main surface. Component styling is distributed across the HTML/CSS templates and visual-level settings.

This is a useful distinction: a report can have a strong visual identity without relying on a bespoke theme JSON alone.

## 9. Bookmarks and interaction

The repository contains 72 bookmark definitions. The bookmark names show open/close states for:
- Tutorials.
- Filter panes.
- Notification panes.
- Page-specific guided states.

The metric selection layer is driven by a native field parameter. Bookmarks are used for interface states and guided walkthroughs, rather than creating a bookmark for every metric variation.

## 10. External dependencies

Although the data is embedded, the DAX source includes external media URLs:
- Image assets hosted on an R2 domain.
- An Unsplash image URL.
- MP4 video URLs hosted on an R2 domain.

Therefore, the report is self-contained with respect to its illustrative data, but not entirely independent of external media availability.

The repository includes one third-party custom visual package. Verify its current version, licence and deployment support separately.

## 11. Unknowns and runtime validation

Not yet verified:
- Actual PBIX rendering and all interactive states.
- Whether all six sections are intended to be visible in the published version.
- City Slicer inactive relationship usage.
- Ranking pagination behaviour.
- Filter and notification pane interactions.
- Actual tab-order and screen-reader behaviour.
- Contrast ratios and touch/keyboard alternatives to hover interactions.
- Performance in Power BI Desktop and Service.
- External asset availability and failure handling.

## 12. Next technical verification

When Power BI Desktop inspection is available:
1. Open the PBIX and confirm the page list.
2. Inspect model relationships and the native field parameter.
3. Test metric selection and filters.
4. Test ranking pagination and city ranking.
5. Test the 10 Year Overview page.
6. Test bookmarks and overlays.
7. Check accessibility and keyboard operation.
8. Record rendering and performance separately from source inspection.
