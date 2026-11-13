# REF-002 — City Sustainability Scorecard: Study Notes

**Creator:** Gus Bavia  
**Original source:** https://github.com/gusbavia/city-sustainability-scorecard  
**Supporting public entry:** https://community.fabric.microsoft.com/t5/Contests-Gallery/Week-1-Briarport-s-Urban-Performance-Through-an-Executive/m-p/4920850  
**Study date:** 2026-11-13  
**Status:** Source-level study documented; runtime validation pending

## Executive finding

City Sustainability Scorecard is an executive-oriented city performance report. It uses a restrained light canvas, a dark textured navigation rail, blue accents, contextual KPI cards, native bar and line charts, a custom SVG radar chart, ranking views and temporal comparisons.

Its technical source package is unusually useful for learning. The repository contains 223 DAX measures in 14 purpose-based folders, 74 HTML templates, 29 CSS files, TMDL model source, report configuration and a vendored HTML Content custom visual.

The strongest lesson is how the report divides the analytical journey into distinct jobs:
- Establish the selected city's position.
- Compare performance across dimensions.
- Rank cities across individual measures.
- Examine historical trends.
- Review a longer-term historical table and peak-period insights.

The report is a useful example of a hybrid Power BI architecture. Native visuals are used where their analytical behaviour is appropriate, while custom HTML/SVG components are used for selected cards, insight panels, radar visualisation and the guided interface.

## 1. Report purpose and data

The report explores urban livability and sustainability across 12 illustrative cities over 2015–2024.

The five metric areas described by the creator are:
- Livability Index / composite.
- Housing Affordability.
- Transit Quality.
- Green Space.
- Emissions.

The creator's public description says the report prioritises visual hierarchy, cognitive efficiency and executive readability, deliberately removing noise rather than adding more visuals. The repository README says the dataset is illustrative and held inside Power Query/model content, with no external data source required to open the PBIX.

The source model's City Metrics table contains City, Year, HousingAffordabilityIndex, TransitScore, GreenSpacePct, EmissionsIndex and LivabilityComposite. City Lookup contains City, State, Country and Region.

## 2. Evidence inspected

| Evidence | Inspection | Confidence |
|---|---|---|
| GitHub README | Report purpose, claimed artefacts, data and reuse instructions | High |
| GitHub repository tree | PBIX, 223 DAX files, 74 HTML templates, 29 CSS files, 9 TMDL files, report sections and bookmark definitions | High |
| LICENSE | MIT licence text | High |
| Report JSON and config | Base theme resource and custom visual reference | High |
| Section JSON | Six sections and 1280 × 720 canvas | High |
| Visual configuration | Selected page visuals, visual types, fields, positions and tab order | High |
| TMDL | Tables, columns, relationships, field parameter metadata and embedded Power Query source | High |
| DAX samples | Normalisation, ranking, trend classification, radar SVG, HTML cards and alt text | High |
| HTML/CSS samples | KPI card, radar, insight, filter and notification components | High |
| Public screenshots | Executive Summary and Performance pages | Medium to high |
| Live PBIX behaviour | Not opened in Power BI Desktop | Not assessed |

### Evidence limitation

The repository contains many visual-container configuration files because the report includes tutorial, filter, notification and state-related elements. A configuration-file count must not be interpreted as the number of simultaneously visible visuals.

The report source tree contains six page sections. The creator's portfolio describes four analytical pages. The extra 10 Year Overview section is present in the public source and is documented separately in [PAGE_ARCHITECTURE.md](PAGE_ARCHITECTURE.md).

## 3. Page architecture and analytical journey

The source defines:
1. Welcome.
2. Executive Summary.
3. Performance.
4. Ranking.
5. Temporal Analysis.
6. 10 Year Overview.

All six sections specify a 1280 × 720 canvas.

The intended analytical journey is coherent:
- The Executive Summary establishes the selected city and its headline position.
- Performance compares the city's dimensions in one radar view, supported by metric cards.
- Ranking places the city against peers across five separate measures.
- Temporal Analysis compares the selected city with all-city benchmarks over time.
- 10 Year Overview consolidates historical values and peak-period insights.

The 10 Year Overview page is an additional section in the PBIX source, beyond the four analytical pages described in the creator's portfolio summary.

See [PAGE_ARCHITECTURE.md](PAGE_ARCHITECTURE.md).

## 4. Visual design findings

The report uses:
- A dark, textured left navigation rail.
- A pale neutral main canvas.
- White/light cards and panels.
- A bright blue accent.
- A rounded main content surface.
- Consistent page titles and context.
- Subject-specific imagery in metric selection cards.
- A small number of recurring card and chart patterns.

The background SVG resources are 1280 × 720 and define a 281-pixel left navigation area, a pale main surface and a curved transition into the content area. The source includes multiple page-specific SVG backgrounds.

The report JSON references the Power BI base theme CY25SU11. The source tree does not expose a separate report-specific custom theme JSON. The branded look is also implemented through page background SVGs, visual formatting and custom HTML/CSS. This distinction matters: the visual identity is not simply the result of importing a custom theme.

See [VISUAL_SYSTEM.md](VISUAL_SYSTEM.md).

## 5. Technical architecture

The source includes:
- 223 DAX files in 14 folders.
- 74 HTML component templates.
- 29 CSS files.
- TMDL model source.
- 72 bookmark definitions.
- One HTML Content custom visual package, version 1.6.0.0.

The model contains City Metrics, City Lookup, City Slicer, Page Parameter, Parameter and _Measures tables. City Metrics and City Lookup have an active city relationship. City Metrics and City Slicer also have an inactive relationship.

The Parameter table has native field-parameter metadata and uses NAMEOF references to five measures. This is a genuine Power BI field parameter, not merely a disconnected DATATABLE selector.

The report combines native clustered bar charts, line charts and tables with custom HTML Content visuals. The radar chart is generated as SVG through a DAX measure. Cards, insight panels, notifications and tutorial content are also generated through DAX/HTML.

See [TECHNICAL_NOTES.md](TECHNICAL_NOTES.md).

## 6. Scoring and metric directionality

The DAX source demonstrates min-max normalisation:
- Transit, green space and livability use a higher-is-better scale.
- Housing affordability and emissions are inverted so lower raw values produce higher normalised scores.

The inspected normalisation measures use fixed minimum and maximum constants based on the supplied illustrative dataset. This is understandable for a fixed demonstration dataset, but a reusable implementation should define how bounds behave when the data range changes.

The General Performance Score measure averages five normalised dimensions equally and divides by 100. Separately, the displayed Avg Livability Score measure is simply the average of City Metrics[LivabilityComposite]. These two measures must not be treated as interchangeable. The source inspection did not establish that General Performance Score drives a visible report visual.

## 7. Accessibility and interaction

The source contains 24 explicit alt-text measures and tab-order values in visual configuration. The creator's public description states that alt text is provided across visuals, keyboard order is logical and colour contrast is WCAG-compliant.

The repository contains 72 bookmark definitions and HTML tutorial templates. Source names show open/close states for tutorial steps, filters and notifications. The creator's public description also refers to a contextual alert system.

These are positive implementation signals. Actual screen-reader operation, keyboard navigation, contrast ratios and bookmark behaviour must still be tested in Power BI Desktop.

## 8. Critical evaluation

### Strengths

- Clear separation of summary, dimension analysis, peer ranking and temporal analysis.
- Stable navigation and repeated page shell.
- Strong combination of native analytical charts and selected custom components.
- Native field parameter for metric selection.
- Purpose-based DAX folder structure.
- Separate HTML templates and CSS files.
- Explicit handling of metric directionality.
- Dynamic alt-text measures and tab-order configuration.
- Embedded illustrative data makes the PBIX easier to open and study.

### Trade-offs and questions

- A 223-measure codebase is substantial; folder organisation helps, but measure dependencies and naming still need careful maintenance.
- The HTML Content visual is a third-party dependency.
- HTML/CSS generated by DAX combines calculation and presentation; this can increase debugging and maintenance effort.
- Seventy-two bookmarks support guided tutorials and interface states, but state management should be kept understandable.
- Hardcoded normalisation bounds need review if the dataset is expanded or refreshed.
- External image and video URLs appear in the DAX source even though the analytical data is embedded. The report is therefore self-contained with respect to data refresh, but not completely independent of external media availability.
- The report source has an extra 10 Year Overview page not reflected in the creator's four-page portfolio summary.
- A source-level study cannot establish runtime performance, responsive behaviour or full accessibility.

## 9. Benchmark status

**No numerical benchmark score assigned.**

The report has not been opened in Power BI Desktop. The visual rubric requires inspection of the actual experience and its interactions. A screenshot and source code alone are not enough for a final score.

## 10. Next study action

If runtime validation becomes available, open the PBIX and test:
1. Sidebar page navigation.
2. Metric field parameter.
3. City and year filters.
4. Radar and card updates.
5. Ranking charts and ranking pagination.
6. Temporal line charts and benchmark comparisons.
7. Filter and notification panes.
8. Tutorial steps and close states.
9. Tab order, alt text and contrast.
10. Rendering and performance in the intended Power BI environment.

The learning objective remains to understand the design and implementation decisions, then adapt useful principles to original work.
