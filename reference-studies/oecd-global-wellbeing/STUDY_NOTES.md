# REF-006 — OECD Global Well-being: Study Notes

**Creator:** Jonathan (Jon) Sandmann  
**Original source:** https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/winning-report---world-champion---oecd-global-well-being/4643676  
**Official Microsoft announcement:** https://community.fabric.microsoft.com/blog/fbc_pbiupdatesblog/the-first-power-bi-dataviz-world-champion---jon-sandmann/5174221  
**Related Reddit discussion:** https://www.reddit.com/r/PowerBI/comments/1jp3123/  
**Study date:** 2026-11-13  
**Status:** Description-led study; live report and source inspection pending

## Executive finding

OECD Global Well-being is a country-comparison report built around three well-being domains and three measures per domain. Its most distinctive described component is a dynamic SVG progress bar that displays the global average for each measure, paired with a year trend and a country table.

The creator also describes anomaly detection in the trend view, cross-filtering from country selection, domain-specific background colours and accent imagery, and dynamic titles and subtitles. A second page explores gender disparity with small multiples.

This is a useful study of component consistency and dynamic visual identity: the same analytical pattern is repeated across several domains, while its colour, imagery, title and data update with the selection.

## 1. Championship context

Microsoft's official championship announcement confirms Jon Sandmann as the first Power BI DataViz World Champion, winning the 2025 finale in Las Vegas with an OECD Well-being report.

The championship finale required finalists to build their reports live in 20 minutes. The official announcement describes judging around creativity, clarity, insightfulness and accessibility.

## 2. Creator-described report structure

The creator's community post describes two pages.

### Page 1 — Well-being domains

The creator selected three key domains and three measures for each domain.

Each measure includes:
- Global average.
- Dynamic, colour-coordinated SVG progress bar.
- Trend by year.
- Anomaly detection intended to identify possible explanations for deviations from expected values.
- A country table sorted from highest to lowest.

Selecting a country cross-filters the SVG progress bar and trend to that country.

A domain button opens a dropdown for changing the selected domain. Each domain has a dynamic background colour and accent image. Page and visual titles/subtitles update dynamically, with subtitle colour changing to complement the selected background.

### Page 2 — Gender disparity

The second page focuses on selected gender disparities across countries. The creator says the charts use Power BI small multiples and dynamic titles/subtitles to explain the differences between male and female averages.

## 3. Related weighted-composite description

A Reddit post about the live OECD challenge describes a normalised composite score based on six metrics. It says users can adjust metric weights with sliders, then inspect top countries and continents, the percentage of countries improving and country rankings by score or improvement.

This is potentially an important interaction pattern, but it is not fully cross-validated against the creator's Microsoft Fabric Community post, which focuses on three domains, three measures per domain and the gender-disparity page.

**Study rule:** treat the weighted composite and sliders as a related description pending confirmation that they are part of the same published report. Do not silently merge the two descriptions.

## 4. Evidence inspected

| Evidence | What it supports | Confidence |
|---|---|---|
| Microsoft official championship announcement | Winner identity and 2025 finale context | High |
| Creator's Microsoft Fabric Community post | Domains, SVG progress bars, trends, anomaly detection, country tables, cross-filtering, dynamic styling and gender page | High |
| Community replies | Positive comment on clarity; a question about how the progress bar was created | Low / anecdotal |
| Related Reddit post | Six-metric composite, user-adjustable weights, country/continent rankings and improvement share | Medium; report identity/details need cross-validation |
| Power BI embed token in creator post | A report embed reference exists | High |
| Downloadable PBIX/source code | Not confirmed | Not assessed |
| Live report rendering | Not available through current browsing interface | Not assessed |

## 5. Visual design findings supported by the source

The creator explicitly describes:
- Colour-coordinated SVG progress bars.
- Domain-specific background colours.
- Accent images associated with each domain.
- Dynamic page titles and subtitles.
- Subtitle colours chosen to complement the domain background.
- Small multiples for gender-disparity comparisons.

These choices suggest that the selected domain acts as a visual identity as well as a data filter. The underlying page structure remains consistent while colour, image and text adapt to the selected domain.

Exact palette values, fonts, canvas dimensions, grid, card treatment and visual positions are unknown.

## 6. Critical evaluation

### Strengths

- Repeated progress-bar, trend and table components make the domains easy to compare.
- Country selection connects a table to the other visuals through cross-filtering.
- Dynamic titles and subtitles help explain what changes when a domain is selected.
- Domain-specific colours and accent imagery reinforce the selected analytical context.
- Anomaly detection adds a reason to investigate deviations rather than merely displaying a trend.
- Small multiples are an appropriate pattern for comparing gender differences across several countries or measures.

### Questions and trade-offs

- A progress bar needs a clear denominator and scale. The creator's description does not specify whether the bar represents a percentile, normalised value, target attainment or another measure.
- Anomaly detection can flag unusual behaviour, but an anomaly is not itself an explanation or proof of cause.
- Dynamic domain colours need adequate contrast and consistent semantic meaning.
- A country table sorted highest to lowest should explain whether higher values are always desirable.
- The weighted composite described on Reddit requires transparent normalisation, weights and missing-value rules. It should not be treated as verified report functionality until the report itself is inspected.
- The report's technical implementation and actual accessibility cannot be assessed from the current evidence.

## 7. Benchmark status

**No numerical benchmark score assigned.**

The report's information and component patterns can be studied from the creator's description, but the live visual system and technical implementation remain unverified.

## 8. Next action

Inspect the live report or PBIX if a compatible browser or source file becomes available. Verify the domain dropdown, country cross-filtering, SVG progress-bar scale, anomaly behaviour, small multiples, actual styling and whether the weighted composite controls are present.
