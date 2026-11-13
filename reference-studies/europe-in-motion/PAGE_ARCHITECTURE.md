# REF-007 — Page Architecture

**Source:** Creator's Microsoft Fabric Community entry and selected replies  
**Status:** Four-page purpose and interaction structure documented; runtime validation pending

## Report-level structure

The creator describes four pages:

| Order | Page | Main question | Reader outcome |
|---:|---|---|---|
| 1 | Overview | What is happening across Europe? | Understand the continental and regional picture |
| 2 | Reading Between the Regions | How do regions perform on selected indicators? | Explore indicator trends, extremes and country rankings |
| 3 | Contrasts | How do regions balance different priorities? | Explore relationships and trade-offs between indicators |
| 4 | Head-to-Head: Countries | Which of two countries performs better? | Compare two selected countries directly |

## Page 1 — Overview

**Purpose:** Present a continental summary and orient the reader.

Creator-described components:
- Population growth line chart from 2004 to 2023.
- Bar chart comparing regional performance across three dimensions.
- Map dividing Europe into Eastern, Western, Southern and Northern regions.

The page is designed as a dynamic visual summary of continental trends.

## Page 2 — Reading Between the Regions

**Purpose:** Let the reader explore one indicator at a time and compare regional performance.

Creator-described components:
- Dynamic cards that act as context switchers for key indicators.
- Native charts showing maximum and minimum values.
- Line chart comparing regional trends against the European average.
- DAX-powered country ranking bar chart.
- Dynamic summary based on the selected context.

The context-switcher cards change which indicator the reader is analysing while keeping the page's analytical structure familiar.

## Page 3 — Contrasts

**Purpose:** Explore how regions balance selected dimensions.

Creator-described components:
- Dynamic scatter plot.
- Customisable X-axis indicator.
- Customisable Y-axis indicator.
- Customisable bubble-size indicator.
- Side panel showing the three most balanced countries per region.

This page supports exploratory analysis of trade-offs and relationships between dimensions.

## Page 4 — Head-to-Head: Countries

**Purpose:** Compare two countries across the same three dimensions.

Creator-described components:
- Two independent country filters.
- Central chart showing which country performs better on each indicator.
- Dynamic calculations to keep the comparison context-aware.

The page is intended to make direct comparison easier than switching repeatedly between separate country views.

## Landing page

The creator's LinkedIn post shows a Home/landing page with:
- Home.
- Overview.
- Between Regions.
- Contrasts.
- Head-to-Head.

The screenshot uses a circular illustration of European landmarks and a clear entry point. This is the only full screenshot-level evidence available in the current study.

## Reader journey

1. Start with the continental overview.
2. Select an indicator and inspect regional trends and country rankings.
3. Explore trade-offs using a configurable scatter plot.
4. Compare two countries directly.

## Architecture lessons

- Move from broad context to focused analysis.
- Use dynamic cards as context selectors.
- Use a scatter plot when the question is about trade-offs across multiple dimensions.
- Use head-to-head comparison when users need to compare two selected entities directly.
- Keep the page purpose distinct so each analytical view earns its place.

## Unknowns

- Exact page dimensions and coordinates.
- Full analytical-page layouts and visual inventory.
- Navigation and filter implementation.
- Cross-filtering and drillthrough behaviour.
- Tooltip design.
- DAX and model architecture.
- Exact definition of regional balance.
- Colour-blindness simulator implementation.
- Runtime and accessibility behaviour.
