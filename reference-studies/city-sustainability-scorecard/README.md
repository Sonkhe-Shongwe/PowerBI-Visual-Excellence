# City Sustainability Scorecard — Reference Study

**Creator:** Gus Bavia  
**Reference ID:** REF-002  
**Original repository:** https://github.com/gusbavia/city-sustainability-scorecard  
**Microsoft Fabric Community entry:** https://community.fabric.microsoft.com/t5/Contests-Gallery/Week-1-Briarport-s-Urban-Performance-Through-an-Executive/m-p/4920850  
**Creator's portfolio:** https://www.gusbavia.com/  
**Repository licence:** MIT  
**Status:** Source-level study documented; Power BI Desktop/runtime inspection pending

## Why this report is useful

This report is a strong contrast to REF-001, The World of Peaches. It is more restrained and executive-oriented, with a consistent navigation shell, a light analytical canvas, a blue accent, metric comparisons, ranking and time-series analysis.

The public repository exposes the full PBIX and a substantial source package:
- 223 standalone DAX measures, organised into 14 folders.
- 74 HTML component templates.
- 29 separate CSS files.
- TMDL semantic-model source.
- Report section and visual configuration.
- 72 bookmark definitions.
- One vendored HTML Content custom visual package.
- A Power BI base theme resource.

The creator describes the report as the 2026 Power BI World Championship Round I entry that carried through to the World Final. It should not be confused with the final championship-winning report, The World of Peaches.

## Study documents

- [STUDY_NOTES.md](STUDY_NOTES.md) — evidence, critical evaluation and study boundaries.
- [PAGE_ARCHITECTURE.md](PAGE_ARCHITECTURE.md) — six report sections and page-by-page structure.
- [VISUAL_SYSTEM.md](VISUAL_SYSTEM.md) — visual language, layout, components and accessibility.
- [TECHNICAL_NOTES.md](TECHNICAL_NOTES.md) — model, DAX, field parameters, HTML/CSS and bookmarks.
- [TRANSFERABLE_PATTERNS.md](TRANSFERABLE_PATTERNS.md) — lessons for original Power BI projects.

## Main finding

The report demonstrates how a relatively simple city-year analytical model can support a polished executive experience through deliberate page architecture, native field parameters, carefully structured DAX, reusable HTML templates and a small set of native visuals.

Its strongest transferable lesson is not the blue-and-white styling. It is the separation of analytical responsibilities across pages, and the discipline of organising measures and components by purpose.

## Evidence boundary

This is a source-level study. The public repository tree, README, MIT licence, report JSON, page section definitions, selected visual configurations, TMDL, DAX, HTML/CSS and custom visual metadata have been inspected.

The PBIX has not been opened in Power BI Desktop in this environment. Actual runtime rendering, filter behaviour, bookmark behaviour, performance, Power BI Service compatibility and screen-reader behaviour remain unverified. No numerical benchmark score has been assigned.

## Important source discrepancy

The creator's portfolio describes the report as four analytical pages: Executive Summary, Performance, Rankings and Temporal Analysis. The current public PBIX source tree contains six sections: Welcome, Executive Summary, Performance, Ranking, Temporal Analysis and 10 Year Overview.

The source therefore exposes an additional 10 Year Overview section beyond the four analytical pages in the portfolio summary. This is recorded as a discrepancy rather than silently reconciled.

## Next action

Open the PBIX in Power BI Desktop when runtime inspection is necessary. Verify the navigation, page states, field parameter selection, filters, notifications, tutorials, ranking behaviour and temporal analysis. Record those observations separately from source-level findings.

The objective is understanding and transferable learning, not recreating the report.
