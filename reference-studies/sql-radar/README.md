# SQL Radar — Reference Study

**Creator:** Aanor Le Gouic  
**Reference ID:** REF-008  
**Original Microsoft Fabric Community entry:** https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/bnc---finalist---sql-radar-%C2%B7-find-the-signal-before-the-alarm/5372173  
**Creator's public LinkedIn post:** https://lnkd.in/gmfGS-eX  
**Status:** Description-led study documented; PBIX attachment listed but not downloaded/opened

## Why study this report?

SQL Radar was Aanor Le Gouic's Barcelona finale report for the 2026 Power BI DataViz World Championship. It is a three-page operational monitoring experience built around a clear sequence:
1. Signal — where are the problems?
2. Diagnosis — why is the system drifting?
3. Action — what should be done first, and by when?

The creator explicitly describes a hybrid architecture:
- Native Power BI visuals carry the data and interactions.
- HTML carries the experience, including a site-zooming map, animated timelines, identity cards and the introduction.

The report also includes a page-level assistant with two personas: Mercury in light mode and Glitch in dark mode.

## Study documents

- [STUDY_NOTES.md](STUDY_NOTES.md) — evidence, report narrative and critical evaluation.
- [PAGE_ARCHITECTURE.md](PAGE_ARCHITECTURE.md) — three-page signal-to-action flow.
- [VISUAL_SYSTEM.md](VISUAL_SYSTEM.md) — documented interaction and experience layers; exact styling unknown.
- [TECHNICAL_NOTES.md](TECHNICAL_NOTES.md) — native/HTML split, report-page tooltips, email action and assistant behaviour.
- [TRANSFERABLE_PATTERNS.md](TRANSFERABLE_PATTERNS.md) — reusable operational dashboard lessons.

## Main finding

The most useful lesson is the deliberate separation of analytical and experience layers. Native visuals provide data interactions and report-page tooltips; HTML provides the distinctive map, animated timelines, identity cards and intro.

The report also focuses on drift before a critical threshold is crossed. It asks not only whether a system is currently critical, but how much headroom remains and whether the system is moving away from its normal state.

## PBIX availability

The Microsoft Fabric Community entry lists:
- A 2.1 MB screenshot attachment.
- A 903 KB PBIX attachment named BCN Finale 2026.pbix.

A community commenter explicitly thanks the creator for sharing the PBIX. This confirms that a PBIX attachment was made available on the source page. The file has not been downloaded or opened in this environment, and the exact attachment URL could not be retrieved through the available browsing interface.

No separate source-code repository or reuse licence was confirmed.

## Evidence boundary

The creator's community post, a related public LinkedIn post and a community reply have been inspected. The three-page structure, hybrid native/HTML architecture, assistant personas and PBIX attachment listing are source-supported.

No report JSON, DAX, TMDL, theme JSON, exact page screenshots, page dimensions, model structure or runtime behaviour have been inspected. No numerical benchmark score has been assigned.

## Next action

If the PBIX can be retrieved through a compatible file-download path, inspect the three pages, native/HTML split, map, timeline, assistant, email action, report-page tooltips and theme states. Keep the current study labelled as description-led until that inspection is complete.
