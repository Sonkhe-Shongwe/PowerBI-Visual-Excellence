# Power BI Basketball Cards — Reference Study

**Creator:** Injae Park  
**Reference ID:** REF-009  
**Original Microsoft Fabric Community entry:** https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/winner-of-week-3--power-bi-basketball-cards/4600448  
**Official Week 3 winner announcement:** https://community.fabric.microsoft.com/blog/community_blog/%F0%9F%8F%86-power-bi-dataviz-world-championships--week-3-winner-%F0%9F%8E%89/4606956  
**Creator walkthrough:** https://www.linkedin.com/posts/injae-park_powerbi-dashboarddesign-sportsanalytics-activity-7345811931527589888-DF7M  
**Status:** Screenshot- and walkthrough-led study documented; PBIX/source inspection pending

## Why study this report?

Power BI Basketball Cards won Week 3 of the 2025 Power BI DataViz World Championships. It is a valuable contrast to the first three reports because the creator describes building the experience entirely with Power BI core visuals, without custom visual add-ons.

The report demonstrates:
- A flippable player card.
- Image-based player/team selection.
- Clean navigation using button slicers or list slicers.
- A shot-location chart made by placing a basketball-court image underneath a scatter plot.
- Filtering by all shots, two-pointers, three-pointers and court zones.
- Player statistics compared with team and NBA averages.

## Study documents

- [STUDY_NOTES.md](STUDY_NOTES.md) — evidence, screenshot observations and critical evaluation.
- [PAGE_ARCHITECTURE.md](PAGE_ARCHITECTURE.md) — navigation, player card and shot-chart structure.
- [VISUAL_SYSTEM.md](VISUAL_SYSTEM.md) — visual hierarchy, card design, imagery and interaction states.
- [TECHNICAL_NOTES.md](TECHNICAL_NOTES.md) — native visuals, measures, layout visibility and scatter-over-image technique.
- [TRANSFERABLE_PATTERNS.md](TRANSFERABLE_PATTERNS.md) — reusable native Power BI interaction patterns.

## Main finding

The strongest lesson is that an application-like experience does not always require a custom visual. A button/list slicer, card visual, layout visibility and a native scatter plot can be combined to create a flippable card and an image-backed shot map.

This is a useful counterbalance to the HTML Content-heavy approaches in REF-001 and REF-002.

## Evidence boundary

The creator's community post, official Microsoft winner announcement, creator walkthrough transcript and a published screenshot have been inspected. The walkthrough explains the main construction techniques.

No downloadable PBIX was confirmed. A community comment asks the creator to share the PBIX, but the inspected public sources do not establish that it was made available. Exact DAX, report JSON, page count, canvas dimensions, visual formatting and accessibility settings remain unverified.

No numerical benchmark score has been assigned.

## Next action

If the PBIX becomes available, inspect the actual card states, button slicer configuration, scatter plot layering, filters, cross-filtering and keyboard accessibility. Do not recreate the report as a deliverable.
