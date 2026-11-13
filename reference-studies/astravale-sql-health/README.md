# AstraVale SQL Health — Reference Study

**Creator:** Marius Helle  
**Reference ID:** REF-003  
**Original Microsoft Fabric Community entry:** https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/world-champion-winner---live-finale-build---astravale-sql-health-report-by-mariu/5373203  
**Public Power BI report:** https://app.powerbi.com/view?r=eyJrIjoiNjNhYzU4MDEtZDc3ZS00MTQ5LTk1YmEtODE2MjZkODkzOTk5IiwidCI6ImI2ZGEwOTc1LTEwY2EtNDE0ZS04YTZjLTE1ZjgzMzgxZGUzMiJ9  
**Supporting championship context:** https://www.dynug.no/2026/10/31/mot-en-verdensmester-i-power-bi/  
**Status:** Description-led study documented; live report/runtime and source inspection pending

## Why study this report?

AstraVale SQL Health is the 2026 Power BI DataViz World Championship finale-winning report from FabCon Barcelona. It is a useful contrast to the first two references: instead of a lifestyle or executive sustainability dashboard, it turns a technical SQL monitoring dataset into an operational investigation and action plan.

The creator describes a five-stage journey:
1. Overview — which systems need attention?
2. Problems — what changed?
3. Causes — why is it happening?
4. Connections — what related systems could be affected?
5. Action — what should be done first?

The Microsoft Fabric Community post describes the page purpose, controls, dataset and analytical views. A public Power BI report link is available through the creator's employer's public post.

## Study documents

- [STUDY_NOTES.md](STUDY_NOTES.md) — source evidence, findings and critical evaluation.
- [PAGE_ARCHITECTURE.md](PAGE_ARCHITECTURE.md) — five-page decision journey.
- [VISUAL_SYSTEM.md](VISUAL_SYSTEM.md) — what can and cannot be assessed from available visual evidence.
- [TECHNICAL_NOTES.md](TECHNICAL_NOTES.md) — dataset, analytical logic and interaction evidence.
- [TRANSFERABLE_PATTERNS.md](TRANSFERABLE_PATTERNS.md) — reusable operational dashboard lessons.

## Main finding

The most valuable design lesson is the sequence from detection to action. Each page answers the next question an operator would naturally ask, rather than repeating the same KPI layout with different charts.

The report also considers equipment value, site and data-feed relationships, warning/critical thresholds and baseline changes. This gives the dashboard a decision context beyond simply showing which metrics are red.

## Evidence boundary

This study is based on the creator's Microsoft Fabric Community description, a public Power BI report link identified in an employer post, and public championship context.

The live Power BI report could not be rendered or interacted with through the available browsing interface. The public community entry lists a thumbnail but no downloadable PBIX or source repository was confirmed. No TMDL, DAX, visual configuration, page dimensions, theme or exact chart implementation has been inspected.

Accordingly, this is a description-led study, not a complete visual or technical audit. No numerical benchmark score has been assigned.

## Next action

If an interactive report or PBIX becomes inspectable, verify the page layouts, status hierarchy, baseline comparisons, heatmap, cause analysis, connection tests and action-priority sliders. Until then, preserve the distinction between the creator's description and our own inference.
