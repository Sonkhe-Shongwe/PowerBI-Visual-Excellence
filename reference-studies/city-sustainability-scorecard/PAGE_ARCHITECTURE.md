# REF-002 — Page Architecture

**Source:** City Sustainability Scorecard public PBIX source repository  
**Canvas:** 1280 × 720 for all six sections  
**Status:** Source inventory complete; runtime validation pending

## Report-level structure

| Order | Section | Role | Primary job |
|---:|---|---|---|
| 0 | Welcome | Cover / entry | Introduce the experience and provide entry/navigation |
| 1 | Executive Summary | Executive overview | Establish selected-city position and headline metrics |
| 2 | Performance | Dimension analysis | Compare five performance dimensions in a radar view |
| 3 | Ranking | Peer comparison | Rank cities across five metrics |
| 4 | Temporal Analysis | Time-series analysis | Compare selected-city trends with all-city benchmarks |
| 5 | 10 Year Overview | Historical detail | Consolidate historical values, YoY indicators and peak insights |

The source therefore defines six report sections: one Welcome section and five analytical sections.

The creator's portfolio summary describes four analytical pages: Executive Summary, Performance, Rankings and Temporal Analysis. The source tree includes a further 10 Year Overview page. Keep this discrepancy visible until the live PBIX clarifies the intended published page set.

## Shared page shell

The page background SVG resources are 1280 × 720. The inspected SVGs define:
- A dark left navigation area approximately 281 px wide.
- A pale main canvas.
- A curved edge between the sidebar and content area.
- A consistent top content region.
- Rounded main surface treatment.
- Embedded image textures and page-specific elements.

The report uses recurring navigation icons, a navigation bar, page title/context components, filter controls, notification controls and tutorial entry points.

## Page 0 — Welcome

**Purpose:** Introductory entry page.

| Component | Type | Position | Role |
|---|---|---:|---|
| Welcome Custom Page | HTML Content | 0, 0, 1280 × 720 | Full-canvas video-led introduction and entry experience |
| LinkedIn Button | Source config | Page-level | External creator/profile action |
| Select an area to explore | Source config | Page-level | Entry/navigation prompt |

The main welcome component is generated from the Video_HTML_MP4 DAX measure. The source references remote MP4 and image assets.

## Page 1 — Executive Summary

**Purpose:** Give the reader the selected city's overall position and let them choose a metric for deeper inspection.

The public screenshot shows:
- A persistent dark navigation rail.
- Page title and selected city/metric/year context.
- Headline KPI cards for average livability and city rank.
- A metric-selection area with four image-backed choices.
- A trend chart and peer-comparison content.
- A compact table/ranking view.

The inspected source configuration includes:
- HTML Content KPI cards for livability, rank, strongest dimension and weakest dimension.
- A native clustered column chart.
- A native line chart.
- A native table.
- A native field-parameter selector.
- Filter and notification panels.
- Tutorial and navigation components.

The native chart configurations bind to DAX measures for selected metric, benchmark, tooltip gap and displayed values. The line chart uses City Metrics.Year and selected-city/benchmark measures.

## Page 2 — Performance

**Purpose:** Compare the selected city across five sustainability dimensions.

| Component | Type | Position (x, y) | Size (w × h) |
|---|---|---:|---:|
| City Performance Radar | HTML Content / generated SVG | 215, 201 | 515 × 508 |
| Insight Card | HTML Content | 238, 99 | 471 × 210 |
| Overall Baseline Card | HTML Content | 749, 99 | 222 × 191 |
| Livability Score Card | HTML Content | 1004, 99 | 224 × 191 |
| Housing Affordability Card | HTML Content | 749, 309 | 222 × 191 |
| Transit Score Card | HTML Content | 1004, 309 | 222 × 191 |
| Emissions Card | HTML Content | 749, 507 | 222 × 191 |
| Green Space Card | HTML Content | 1004, 507 | 222 × 191 |
| 10 Year Overview navigation button | Image | 238, 658 | 168 × 46 |

The radar uses five dimensions: Transit, Livability, Green Space, Housing and Emissions. The surrounding cards provide individual values and contextual performance information.

## Page 3 — Ranking

**Purpose:** Compare city positions across five separate metric rankings.

The source positions five native clustered bar charts in a horizontal row. Each is paired with an HTML rank card below it.

| Metric | Chart position (x, y) | Chart size | Rank card position (x, y) |
|---|---:|---:|---:|
| Livability | 238, 148 | 180 × 362 | 238, 506 |
| Housing affordability | 440, 148 | 180 × 362 | 440, 506 |
| Transit | 644, 148 | 180 × 362 | 640, 506 |
| Emissions | 846, 148 | 180 × 362 | 846, 506 |
| Green space | 1050, 148 | 180 × 362 | 1051, 506 |

The source configurations use explicit city categories and metric-specific DAX measures. Tooltips include benchmark gaps and percentage gaps.

## Page 4 — Temporal Analysis

**Purpose:** Show how each of the five dimensions changes over time and compare each selected-city trend with an all-city benchmark.

Five native line charts use a two-column grid:

| Metric | Position (x, y) | Size (w × h) |
|---|---:|---:|
| Livability | 256, 106 | 464 × 174 |
| Housing affordability | 761, 106 | 464 × 174 |
| Transit | 256, 308 | 464 × 174 |
| Emissions | 761, 308 | 464 × 174 |
| Green space | 256, 512 | 464 × 174 |

An HTML overall-performance insight card sits in the lower-right region at approximately x=756, y=510, width=461 and height=149.

Each chart uses City Metrics.Year, a selected-city metric measure and an all-city benchmark measure.

## Page 5 — 10 Year Overview

**Purpose:** Provide a denser historical view with year-over-year indicators and peak-performance context.

| Component | Type | Position (x, y) | Size (w × h) |
|---|---|---:|---:|
| Historical Performance Data | Native table | 243, 82 | 1009 × 402 |
| Livability Peak Card | HTML Content | 242, 480 | 184 × 213 |
| Housing Peak Card | HTML Content | 445, 480 | 184 × 213 |
| Transit Peak Card | HTML Content | 649, 480 | 184 × 213 |
| Emissions Peak Card | HTML Content | 852, 480 | 184 × 213 |
| Green Space Peak Card | HTML Content | 1055, 480 | 184 × 213 |
| Back Button | Native action button | 1144, 33 | 29 × 27 |

The table configuration includes year, metric measures, YoY pill measures and an overall trend sparkline measure.

## Navigation, filters and guided states

The source tree contains 72 bookmark definitions. Names indicate open/close states for:
- Tutorial steps across multiple pages.
- Filter panes.
- Notification panes.
- Other guided navigation states.

The source also contains tutorial HTML templates for Executive Summary, Performance, Ranking and Temporal Analysis. This supports the creator's stated goal of guiding readers through unfamiliar controls and report logic.

## What this structure teaches us

1. Separate executive summary, dimensions, peer ranking and temporal analysis rather than forcing every analytical question onto one page.
2. Use a stable navigation shell to reduce orientation cost.
3. Use one consistent grid for repeated metric cards.
4. Use small multiples when users need to compare the same measure across several dimensions.
5. Pair rankings with explicit rank cards so bar length is not the only source of information.
6. Provide a historical table when users need exact values beyond the visual summary.
7. Keep tutorials and filter/notification overlays optional rather than permanently occupying the analytical canvas.

## Runtime checks required

- Confirm all six sections are visible and intentionally navigable.
- Verify the extra 10 Year Overview page and its relationship to Performance.
- Test field parameter selection and city/year filter interactions.
- Test ranking chart interactions and pagination.
- Verify temporal chart benchmark behaviour.
- Open and close tutorial, filter and notification states.
- Confirm keyboard tab order and actual screen-reader descriptions.
