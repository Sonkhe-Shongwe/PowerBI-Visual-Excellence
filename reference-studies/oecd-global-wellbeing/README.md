# OECD Global Well-being — Reference Study

**Creator:** Jonathan (Jon) Sandmann  
**Reference ID:** REF-006  
**Original Microsoft Fabric Community entry:** https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/winning-report---world-champion---oecd-global-well-being/4643676  
**Official Microsoft championship announcement:** https://community.fabric.microsoft.com/blog/fbc_pbiupdatesblog/the-first-power-bi-dataviz-world-champion---jon-sandmann/5174221  
**Related creator discussion:** https://www.reddit.com/r/PowerBI/comments/1jp3123/  
**Status:** Description-led study documented; live report and source inspection pending

## Why study this report?

OECD Global Well-being was the winning report in the first Power BI DataViz World Championship finale in Las Vegas in 2025. It is a useful reference for dynamic SVG progress bars, anomaly-aware trend storytelling, country-level cross-filtering and small-multiple comparisons.

The creator's community post describes:
- Three key well-being domains, each with three measures.
- A global average for each measure, displayed with a dynamic, colour-coordinated SVG progress bar.
- A trend by year, with anomaly detection to highlight deviations from expected values.
- A country table sorted from highest to lowest.
- Country selection that cross-filters the SVG and trend.
- A domain selector that opens a dropdown.
- Domain-specific background colours and accent images.
- Dynamic page titles, subtitles and subtitle colours.
- A second page focused on gender disparity using small multiples.

A related Reddit discussion about the live OECD challenge describes a six-metric normalised composite score with user-adjustable weights. It is not yet confirmed whether that is an additional feature of the same published report or a related live-finale view. That distinction is preserved in the study.

## Study documents

- [STUDY_NOTES.md](STUDY_NOTES.md) — evidence, findings, source discrepancies and limitations.
- [PAGE_ARCHITECTURE.md](PAGE_ARCHITECTURE.md) — two-page structure described by the creator.
- [VISUAL_SYSTEM.md](VISUAL_SYSTEM.md) — dynamic domain identity, SVG progress bars and visual unknowns.
- [TECHNICAL_NOTES.md](TECHNICAL_NOTES.md) — SVG, anomaly detection, cross-filtering and unverified weighting details.
- [TRANSFERABLE_PATTERNS.md](TRANSFERABLE_PATTERNS.md) — lessons for original Power BI work.

## Main finding

The report uses a small number of repeatable components to make a multi-domain country comparison feel dynamic: a progress bar, a trend, a country table and a domain selector. The page changes its visual identity with the selected domain, while the underlying interaction pattern remains familiar.

The strongest transferable lesson is how a consistent component can be reused across different analytical domains while its title, colour, data and supporting context update together.

## Evidence boundary

The official Microsoft championship announcement confirms Jon Sandmann as the 2025 World Champion. The creator's Microsoft Fabric Community post describes the two-page report and its main interactions. A Reddit discussion describes a weighted composite-score interaction, but that detail is not fully cross-validated against the creator's community post.

The community post contains a Power BI embed token, but no separate PBIX download or source repository was confirmed. The live report could not be rendered through the available browsing interface. No report JSON, DAX, TMDL, theme JSON, visual coordinates or actual palette values have been inspected.

This is a description-led study. No numerical benchmark score has been assigned.

## Next action

If the live report or PBIX becomes inspectable, verify the domain selector, country cross-filtering, anomaly detection, small multiples, exact visual design and whether the weighted composite-score controls are part of the same report.
