# Europe in Motion — Reference Study

**Creator:** Paulo Grijó  
**Reference ID:** REF-007  
**Original Microsoft Fabric Community entry:** https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/europe-in-motion-a-dynamic-portrait-of-how-regions-balance-social-and-environmen/4800387  
**Creator's LinkedIn entry:** https://www.linkedin.com/feed/update/urn%3Ali%3Aactivity%3A7363584628982456322/  
**Winner announcement:** https://www.linkedin.com/posts/infosys-americas_our-colleague-paulo-grij%C3%B3-business-intelligence-activity-7389020198965788672-b9F9  
**Status:** Description- and screenshot-led study documented; PBIX/source inspection pending

## Why study this report?

Europe in Motion won the Power BI DataViz World Championship final in Vienna in 2025. It explores European sustainability, well-being and culture through four analytical pages.

The creator describes:
- Overview.
- Reading Between the Regions.
- Contrasts.
- Head-to-Head: Countries.

The report combines native charts and maps with dynamic HTML Content KPI cards, HTML/CSS animation, DAX-driven ranking and contextual summaries. It also uses a customizable scatter plot and independent country filters for direct comparison.

The creator's employer says the winning presentation incorporated a colour-blindness simulator, making accessibility a notable part of the story.

## Study documents

- [STUDY_NOTES.md](STUDY_NOTES.md) — evidence, report narrative and critical evaluation.
- [PAGE_ARCHITECTURE.md](PAGE_ARCHITECTURE.md) — four-page analytical journey.
- [VISUAL_SYSTEM.md](VISUAL_SYSTEM.md) — available screenshot observations, dynamic styling and accessibility.
- [TECHNICAL_NOTES.md](TECHNICAL_NOTES.md) — HTML Content, HTML/CSS, DAX ranking and interactive scatter design.
- [TRANSFERABLE_PATTERNS.md](TRANSFERABLE_PATTERNS.md) — lessons for original reports.

## Main finding

The report's strongest pattern is the combination of a guided overview and progressively more analytical pages. Readers can begin with a broad regional picture, inspect individual indicators, explore trade-offs and finally compare two countries directly.

The report also demonstrates how dynamic cards, titles, colours and summaries can make a single analytical page respond to a selected context without forcing the user to navigate through many separate pages.

## Evidence boundary

The creator's Microsoft Fabric Community entry, page descriptions, selected replies, LinkedIn entry, winner announcement and a landing-page screenshot have been inspected.

The screenshot available in this study is the report's landing page, not a full analytical page. The community thread includes a Power BI embed token, but no downloadable PBIX or source repository was confirmed. The creator confirms the use of HTML Content for KPI cards and HTML/CSS for animated text overlays.

No report JSON, DAX, TMDL, theme JSON, exact analytical-page screenshots, page dimensions or runtime behaviour have been inspected. No numerical benchmark score has been assigned.

## Next action

If the live report or PBIX becomes available, inspect all four analytical pages, the dynamic context switching, head-to-head comparison, scatter plot controls, map, colour-blindness simulator and keyboard accessibility. Keep the current findings clearly labelled as source-described until verified.
