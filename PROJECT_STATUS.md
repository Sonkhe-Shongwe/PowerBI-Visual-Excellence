# Project Status

**As of:** 2026-11-13  
**Overall progress:** 24% (weighted estimate)  
**Current phase:** P2 — Structural, visual and technical deconstruction
**Current focus:** Technical reference study, beginning with REF-010 Deneb Power BI Example  
**Project state:** Reference discovery gate complete; five reference studies documented, two source-level and three screenshot/description-led

## Executive status

This repository is a Power BI learning and design-research workspace. Its purpose is to study exceptional reports, understand their structure and implementation, extract transferable principles, and use those lessons to improve the user's separate personal projects.

The external reports are case studies, not the deliverables we are trying to recreate. The user's personal projects remain in their own repositories.

The initial project documentation and research structure have been committed. Two source-level studies are documented: The World of Peaches and City Sustainability Scorecard. A third and fourth description-led study, AstraVale SQL Health and OECD Global Well-being, and a fifth screenshot/walkthrough-led study, Power BI Basketball Cards, document report architecture and interaction patterns. The studies cover page architecture, visual systems where available, semantic models, DAX, HTML/CSS, interactions, technical dependencies and transferable patterns.

The first two public repositories and declared MIT licences were checked; their report definitions, selected visual configurations, TMDL, DAX and component source were inspected. Their PBIX files have not been opened in Power BI Desktop. AstraVale's public Power BI link was identified but could not be rendered in the available browsing interface; no PBIX or source repository was confirmed. Runtime interactions, performance, service rendering and accessibility therefore remain unverified.

No personal project has been modified through this research workspace.

## Phase scorecard

| Phase | Progress | Status | Evidence |
|---|---:|---|---|
| P1 — Reference discovery | 100% | Complete | Ten references recorded; five high-priority candidates selected |
| P2 — Structural, visual and technical deconstruction | 35% | In progress | REF-001 and REF-002 source-level studies; REF-003 and REF-006 description-led studies; REF-009 screenshot/walkthrough study documented |
| P3 — Pattern extraction and design system | 0% | Not started | No validated reusable pattern library |
| P4 — Apply lessons to personal projects | 0% | Not started | No user-selected project application |
| P5 — Validate, refine and document learning | 0% | Not started | No applied-pattern review |

The overall percentage is calculated using phase weights in [PROJECT_ROADMAP.md](PROJECT_ROADMAP.md): 15% from completed P1 plus 8.75% from P2, or 23.75%, rounded to 24%.

## Verified starting points

| Reference | What is known | What remains to be studied |
|---|---|---|
| The World of Peaches | Public source repository and MIT licence verified; five 1280 × 720 sections, visual configuration, theme, TMDL, DAX and HTML/CSS inspected | Open PBIX in Power BI Desktop; test interactions, accessibility and rendering |
| City Sustainability Scorecard | Public repository and MIT licence verified; six 1280 × 720 sections, 223 DAX files, 74 HTML templates, 29 CSS files, TMDL and selected visual configurations inspected | Open PBIX in Power BI Desktop; verify all six pages, field parameter, interactions and accessibility |
| Power BI Basketball Cards | 2025 Week 3 winner; screenshot and creator walkthrough show native-visual flippable card, button/list slicer navigation and shot chart over a court image | PBIX/source access remains unconfirmed; verify the exact card state implementation and accessibility if available |
| Deneb Power BI Example | Public PBIX and README; Deneb donut, dynamic-marker bar, tooltips and drillthrough documented; no licence file found | Study Vega-Lite specs in the PBIX if opened; keep reuse permissions unassumed |
| AstraVale SQL Health | Creator describes five pages, dataset and operational decision flow; public Power BI URL identified but not rendered | Inspect live report when a compatible browser is available; PBIX/source access remains unconfirmed |
| OECD Global Well-being | Creator describes dynamic SVG progress bars, anomaly-aware trends, country cross-filtering and gender small multiples; official winner status verified | Verify report rendering, progress-bar scale, anomaly behaviour and whether weighted-composite controls are part of the same report |
| Microsoft Power BI samples | Official documentation and official sample repository provide sample artefacts | Select reports that teach useful structure, visual and interaction patterns |

See [REFERENCE_CATALOG.md](research/REFERENCE_CATALOG.md) for links and caveats.

## REF-009 study documents

- [Study notes](reference-studies/powerbi-basketball-cards/STUDY_NOTES.md)
- [Page architecture](reference-studies/powerbi-basketball-cards/PAGE_ARCHITECTURE.md)
- [Visual system](reference-studies/powerbi-basketball-cards/VISUAL_SYSTEM.md)
- [Technical notes](reference-studies/powerbi-basketball-cards/TECHNICAL_NOTES.md)
- [Transferable patterns](reference-studies/powerbi-basketball-cards/TRANSFERABLE_PATTERNS.md)

## REF-006 study documents

- [Study notes](reference-studies/oecd-global-wellbeing/STUDY_NOTES.md)
- [Page architecture](reference-studies/oecd-global-wellbeing/PAGE_ARCHITECTURE.md)
- [Visual system](reference-studies/oecd-global-wellbeing/VISUAL_SYSTEM.md)
- [Technical notes](reference-studies/oecd-global-wellbeing/TECHNICAL_NOTES.md)
- [Transferable patterns](reference-studies/oecd-global-wellbeing/TRANSFERABLE_PATTERNS.md)

## REF-003 study documents

- [Study notes](reference-studies/astravale-sql-health/STUDY_NOTES.md)
- [Page architecture](reference-studies/astravale-sql-health/PAGE_ARCHITECTURE.md)
- [Visual system](reference-studies/astravale-sql-health/VISUAL_SYSTEM.md)
- [Technical notes](reference-studies/astravale-sql-health/TECHNICAL_NOTES.md)
- [Transferable patterns](reference-studies/astravale-sql-health/TRANSFERABLE_PATTERNS.md)

## REF-002 study documents

- [Study notes](reference-studies/city-sustainability-scorecard/STUDY_NOTES.md)
- [Page architecture](reference-studies/city-sustainability-scorecard/PAGE_ARCHITECTURE.md)
- [Visual system](reference-studies/city-sustainability-scorecard/VISUAL_SYSTEM.md)
- [Technical notes](reference-studies/city-sustainability-scorecard/TECHNICAL_NOTES.md)
- [Transferable patterns](reference-studies/city-sustainability-scorecard/TRANSFERABLE_PATTERNS.md)

## Reference discovery gate

P1 is complete: the catalogue now contains ten references, each with a source link and verification status, and five high-priority candidates have been selected. Priority labels are study sequencing, not benchmark scores.

## Current boundaries

- Do not clone an external report as the default next step.
- Do not treat an attractive screenshot as evidence of implementation details.
- Do not copy a creator's PBIX or assets into this repository without checking the relevant rights.
- Do not move the user's personal project source files into this learning repository.
- Do not choose or change the user's personal project scope without their direction.
- Use isolated experiments only when they answer a specific technical learning question.

## Next action

Begin the next technical reference study with REF-010 Deneb Power BI Example. Review the public PBIX and README for Deneb/Vega-Lite specifications, custom chart encodings, tooltips, drillthrough and report-page tooltips. The repository has no LICENSE file, so treat its contents as study-only unless reuse permission is confirmed.

Runtime inspection of REF-001 and REF-002 remains a separate user-side option when Power BI Desktop is available. AstraVale and OECD report links are recorded, but their live rendering remains unverified.

The goal is to understand the technical options and trade-offs of custom visuals, not to recreate the report.
