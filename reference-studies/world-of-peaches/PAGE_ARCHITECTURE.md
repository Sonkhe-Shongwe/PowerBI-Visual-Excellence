# REF-001 — Page Architecture

**Source:** The World of Peaches public repository  
**Status:** Source inventory complete; runtime inspection pending

## Report-level structure

The report file defines five sections, each with a 1280 × 720 canvas.

| Order | Page | Role | Main analytical purpose |
|---:|---|---|---|
| 0 | Welcome | Cover / entry | Introduce the report and direct the reader into the experience |
| 1 | Overview | Global summary | Present global production, trade measures, trend and continental distribution |
| 2 | Production | Analytical detail | Compare production volume, harvested area and yield |
| 3 | Trade | Analytical detail | Explore import/export value, trade flows, country/region comparisons and trade balance |
| 4 | Tabular View | Detail / reference | Provide a table-oriented view of the underlying data |

This means the source has five report sections, of which four are analytical pages. This distinction explains why some public descriptions refer to four pages.

## Shared canvas and shell

- Canvas: 1280 × 720.
- Aspect ratio: 16:9.
- The analytical pages use a consistent left-side navigation region.
- The page navigator is positioned around x=11, y=129, width=217 and height=210–213.
- The How to Read control is positioned near x=11, y=498, width=218 and height=184.
- Main content generally begins around x=240–272.
- Year and continent dropdown slicers sit in the top-right area, around y=53.
- The report source includes page-specific background image resources for the analytical pages.

Coordinates below are taken from the report's visual configuration. They are canvas coordinates, not measurements from a screenshot. Small decimal values are rounded for readability.

## Page 0 — Welcome

**Purpose:** Full-page cover and entry point.

| Visual | Type | Position (x, y) | Size (w × h) | Role |
|---|---|---:|---:|---|
| Cover | HTML Content | 0, 0 | 1280 × 628 | Main cover experience |
| Entry image | Image | 1047, 643 | 202 × 61 | Page navigation to Overview |
| LinkedIn image | Image | 34, 657 | 154 × 34 | External creator link |
| Website image | Image | 205, 657 | 154 × 34 | External creator website |

The cover is built as one large HTML Content visual, with image-based controls along the bottom.

## Page 1 — Overview

**Purpose:** Establish the global picture and let the reader change the headline metric.

| Component | Type | Position (x, y) | Size (w × h) | Role |
|---|---|---:|---:|---|
| KPI row | HTML Content | 272, 141 | 978 × 210 | Headline production/trade KPIs |
| Trend chart | HTML Content | 280, 381 | 566 × 300 | Dynamic trend by selected metric |
| Continental share | HTML Content | 875, 373 | 375 × 296 | Regional distribution component |
| Country map | Shape Map | 883, 498 | 359 × 186 | Geographic comparison |
| Metric selector | Advanced slicer visual | 515, 418 | 319 × 37 | Production / export / import / balance selection |
| Year slicer | Slicer | 952, 53 | 113 × 43 | Year filter |
| Continent slicer | Slicer | 1087, 53 | 163 × 43 | Continent/country filter |
| Page navigator | Page Navigator | 11, 132 | 217 × 210 | Sidebar navigation |
| How to Read control | Image | 11, 498 | 218 × 184 | Opens the tutorial flow |
| Tutorial guide | HTML Content | 239, 121 | 1012 × 599 | Hidden tutorial overlay |

The remaining image visual is used as a bookmark-driven close control. The page also defines a background image resource.

## Page 2 — Production

**Purpose:** Compare production, harvested area and yield through a selectable metric view.

| Component | Type | Position (x, y) | Size (w × h) | Role |
|---|---|---:|---:|---|
| KPI row | HTML Content | 272, 135 | 978 × 198 | Production context and headline metrics |
| Production waffle | HTML Content | 272, 352 | 578 × 339 | Dot-based comparison and table view |
| Volume/efficiency panel | HTML Content | 869, 351 | 381 × 337 | Contextual explanatory panel |
| Metric selector | Advanced slicer visual | 571, 393 | 220 × 35 | Production / harvested / yield |
| View icon selector | Advanced slicer visual | 501, 393 | 66 × 35 | Waffle / table view |
| Year slicer | Slicer | 952, 53 | 113 × 43 | Year filter |
| Continent slicer | Slicer | 1087, 53 | 163 × 43 | Geographic filter |
| Page navigator | Page Navigator | 11, 129 | 217 × 213 | Sidebar navigation |
| How to Read control | Image | 11, 498 | 218 × 184 | Opens the tutorial flow |
| Tutorial guide | HTML Content | 241, 122 | 1010 × 598 | Hidden tutorial overlay |

The remaining image visual is used as a close control. The production waffle component contains a Waffle/Table view concept and a multi-slide layout in its HTML/CSS source.

## Page 3 — Trade

**Purpose:** Explain where peach trade value and volume flow, with country/region context.

| Component | Type | Position (x, y) | Size (w × h) | Role |
|---|---|---:|---:|---|
| Trade insight | HTML Content | 273, 140 | 283 × 550 | Narrative insight panel |
| Trade bar chart | HTML Content | 571, 141 | 469 × 284 | Export/import comparison |
| Map/header component | HTML Content | 571, 438 | 469 × 252 | Geographic and contextual panel |
| Trade KPI tower | HTML Content | 1054, 140 | 197 × 550 | Stacked trade KPIs and rankings |
| Trade flow selector | Advanced slicer visual | 941, 176 | 94 × 33 | Import / export selection |
| Country map | Shape Map | 592, 533 | 190 × 144 | Geographic comparison |
| Year slicer | Slicer | 953, 53 | 113 × 43 | Year filter |
| Continent slicer | Slicer | 1087, 53 | 163 × 43 | Geographic filter |
| Page navigator | Page Navigator | 11, 132 | 217 × 210 | Sidebar navigation |
| How to Read control | Image | 11, 498 | 218 × 184 | Opens the tutorial flow |
| Tutorial guide | HTML Content | 240, 122 | 1011 × 598 | Hidden tutorial overlay |

The remaining image visual is used as a close control. The Trade Insight component includes a video background in its HTML output.

## Page 4 — Tabular View

**Purpose:** Provide a detail-oriented table view.

| Component | Type | Position (x, y) | Size (w × h) | Role |
|---|---|---:|---:|---|
| Tabular view | HTML Content | 271, 140 | 979 × 550 | Main table-oriented view |
| Year slicer | Slicer | 952, 53 | 113 × 43 | Year filter |
| Continent slicer | Slicer | 1087, 53 | 163 × 43 | Geographic filter |
| Page navigator | Page Navigator | 11, 129 | 217 × 213 | Sidebar navigation |
| Tutorial guide | HTML Content | 271, 140 | 979 × 550 | Hidden tutorial overlay |

The remaining image visuals are used for the How to Read and close controls.

## Navigation and guided learning

The source contains eight bookmark folders:
- Tutorial 1, Tutorial 2, Tutorial 3 and Tutorial 4.
- Close 1, Close 2, Close 3 and Close 4.

The analytical pages contain hidden tutorial HTML components and image-based controls linked to bookmark states. This suggests a guided reading layer that can be opened and closed without adding a separate report page.

The report also uses a Page Navigator visual for the main sidebar navigation.

## What this structure teaches us

1. Keep a stable page shell so readers do not need to relearn navigation.
2. Give each page a distinct analytical purpose.
3. Keep global filters in a consistent location.
4. Use a detail page when users need a denser table-oriented view.
5. Use guided overlays to explain complex report logic without crowding the default view.
6. Combine custom components with native map, slicer and navigation capabilities where each is appropriate.

## Runtime checks still required

- Confirm page navigation and selected states.
- Test whether Year and Continent selections synchronise across pages.
- Open and close each tutorial overlay.
- Test metric and view selectors.
- Check cross-filtering between map and other visuals.
- Verify table behaviour and scrolling.
- Confirm the page shell at actual display size and in Power BI Service if applicable.
