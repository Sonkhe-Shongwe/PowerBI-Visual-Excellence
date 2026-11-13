# REF-007 — Europe in Motion: Study Notes

**Creator:** Paulo Grijó  
**Original source:** https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/europe-in-motion-a-dynamic-portrait-of-how-regions-balance-social-and-environmen/4800387  
**Creator's LinkedIn entry:** https://www.linkedin.com/feed/update/urn%3Ali%3Aactivity%3A7363584628982456322/  
**Winner announcement:** https://www.linkedin.com/posts/infosys-americas_our-colleague-paulo-grij%C3%B3-business-intelligence-activity-7389020198965788672-b9F9  
**Study date:** 2026-11-13  
**Status:** Description- and screenshot-led study; PBIX/source inspection pending

## Executive finding

Europe in Motion is a four-page interactive data-storytelling report about how European regions balance sustainability, well-being and culture.

The report's page sequence moves from a broad overview to regional indicator analysis, multi-variable exploration and direct country comparison:
1. Overview.
2. Reading Between the Regions.
3. Contrasts.
4. Head-to-Head: Countries.

The creator describes dynamic indicator cards, a regional map, historical trends against the European average, a DAX-powered country ranking, a configurable scatter plot and independent filters for comparing two countries.

The creator also confirms that KPI cards use the HTML Content custom visual and that animated text overlays were created with HTML and CSS. The creator's employer says the championship-winning presentation included a colour-blindness simulator.

## 1. Championship context

The creator submitted Europe in Motion to the Power BI DataViz World Championship EU Edition, whose theme was Life in Europe.

Infosys Americas later announced Paulo Grijó as the Power BI DataViz World Champion. The company says he was selected for the Final Four in Vienna and won with Europe in Motion, an interactive and inclusive solution that incorporated a colour-blindness simulator.

This is a stronger credential than a generic community showcase: the report was the winning final presentation.

## 2. Data and analytical subject

The report explores three dimensions:
- Sustainability.
- Well-being.
- Culture.

The overview description includes population growth from 2004 to 2023 and regional comparisons across the three dimensions. The map divides Europe into four regions:
- Eastern.
- Western.
- Southern.
- Northern.

The report supports exploration at continental, regional and country levels.

The exact data source, table grain, country coverage, measure definitions and refresh process have not been inspected.

## 3. Evidence inspected

| Evidence | What it supports | Confidence |
|---|---|---|
| Creator's Microsoft Fabric Community entry | Four pages, report purpose, analytical views and interactions | High |
| Community replies | HTML Content use for KPI cards; HTML/CSS animated text; dynamic colours; positive feedback on map and interactions | High |
| Creator's LinkedIn entry | Report title, competition theme and landing-page screenshot | High |
| Employer winner announcement | Championship win and colour-blindness simulator claim | High |
| Landing-page screenshot | Introductory visual identity and navigation labels | High for the shown landing state |
| Full analytical page screenshots | Not available in inspected sources | Not assessed |
| PBIX/source repository | Not confirmed | Not assessed |
| Live report runtime | Not rendered/interacted with | Not assessed |

## 4. Four-page analytical journey

### Overview

The page presents:
- A line chart of population growth from 2004 to 2023.
- A bar chart comparing regional performance across three dimensions.
- A map dividing Europe into four regions.

This is the broad continental summary.

### Reading Between the Regions

The page uses dynamic cards as context switchers for key indicators.

The creator describes:
- Native charts showing maximum and minimum values.
- A line chart comparing regional trends against the European average.
- A DAX-powered bar chart ranking countries.
- A dynamic summary that changes with the selected context.

This page moves from overview to indicator-specific interpretation.

### Contrasts

The page uses a dynamic scatter plot to explore how regions balance their priorities.

The reader can customise:
- X-axis indicator.
- Y-axis indicator.
- Bubble size.

A side panel summarises the three most balanced countries in each region based on the selected metrics.

This is a useful pattern for exploring trade-offs rather than simply ranking countries on one measure.

### Head-to-Head: Countries

The page compares two countries across three dimensions using independent filters.

A central chart highlights which country performs better in each indicator. The creator notes that the page uses detailed logic and dynamic calculations despite its simple visual layout.

This is a direct comparison experience rather than a static country ranking.

## 5. Visual and interaction findings

The available landing-page screenshot shows:
- Dark blue top navigation.
- A light background.
- A circular illustration of European landmarks.
- A central World Champs EU Edition title.
- A small row of navigation/social icons.
- A clear Home, Overview, Between Regions, Contrasts and Head-to-Head navigation sequence.

This is evidence about the landing page only; it should not be treated as a full representation of the analytical-page styling.

The community discussion provides additional interaction evidence:
- Dynamic colours are deliberately connected to the selected analytical context.
- Animated text overlays on KPI cards use HTML and CSS.
- KPI cards on the Overview page use HTML Content.
- Users praised the map, tooltips, animations and head-to-head comparison.

## 6. Accessibility

The creator's employer says the winning solution incorporated a colour-blindness simulator.

This is an interesting design decision because it makes accessibility something the reader can actively explore, not just a behind-the-scenes compliance statement.

The community discussion also includes positive comments about accessibility. However, the actual simulator implementation, colour palette, keyboard navigation, screen-reader behaviour and contrast have not been inspected.

## 7. Critical evaluation

### Strengths

- Clear four-page progression from overview to comparison.
- Dynamic cards act as context switchers rather than static decoration.
- Regional and country views support different analytical levels.
- The scatter plot exposes trade-offs across three dimensions.
- Head-to-head comparison is more direct than asking users to compare two countries in separate charts.
- Dynamic summaries help interpret selected contexts.
- HTML/CSS adds controlled motion and contextual KPI presentation.
- A colour-blindness simulator is a distinctive accessibility feature.

### Trade-offs and questions

- Dynamic colours must remain semantically consistent and accessible.
- Configurable axes and bubble sizes need clear labels and units.
- The definition of a balanced country should be transparent.
- Head-to-head comparisons should use consistent scales and explain whether higher or lower values are desirable.
- Animated text must not obscure the KPI or distract from its value.
- The report uses HTML Content, which adds a custom visual dependency.
- No PBIX or source repository was confirmed, so implementation details and performance cannot be judged.

## 8. Benchmark status

**No numerical benchmark score assigned.**

The report has strong evidence of analytical storytelling and interaction design, but the full analytical pages and technical implementation have not been inspected.

## 9. Next action

Inspect the live report or PBIX when available. Capture each analytical page, record actual layout and visual types, test dynamic card states and axis controls, and verify the colour-blindness simulator and keyboard accessibility.
