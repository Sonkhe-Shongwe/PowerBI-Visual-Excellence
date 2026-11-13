# Project Status

**As of:** 2026-11-13  
**Overall progress:** 28% (weighted estimate)  
**Current phase:** P2 — Structural, visual and technical deconstruction
**Current focus:** Official Microsoft sample audit, beginning with REF-004  
**Project state:** Reference discovery gate complete; eight studies documented, three source-level, four description-led and one screenshot/walkthrough-led

## Executive status

This repository is a Power BI learning and design-research workspace. Its purpose is to study exceptional reports, understand their structure and implementation, extract transferable principles, and use those lessons to improve the user's separate personal projects.

The external reports are case studies, not the deliverables we are trying to recreate. The user's personal projects remain in their own repositories.

The initial project documentation and research structure have been committed. Three source-level studies are documented: The World of Peaches, City Sustainability Scorecard and Deneb Template Showcase. Four description-led studies, AstraVale SQL Health, OECD Global Well-being, Europe in Motion and SQL Radar, and one screenshot/walkthrough-led study, Power BI Basketball Cards, document report architecture and interaction patterns. The studies cover page architecture, visual systems where available, semantic models, DAX, HTML/CSS, interactions, technical dependencies and transferable patterns.

The first two public repositories and declared MIT licences were checked; their report definitions, selected visual configurations, TMDL, DAX and component source were inspected. Their PBIX files have not been opened in Power BI Desktop. AstraVale's public Power BI link was identified but could not be rendered in the available browsing interface; no PBIX or source repository was confirmed. Runtime interactions, performance, service rendering and accessibility therefore remain unverified.

No personal project has been modified through this research workspace.

## Phase scorecard

| Phase | Progress | Status | Evidence |
|---|---:|---|---|
| P1 — Reference discovery | 100% | Complete | Eleven references recorded; seven high-priority candidates selected |
| P2 — Structural, visual and technical deconstruction | 50% | In progress | REF-001, REF-002 and REF-011 source-level studies; REF-003, REF-006, REF-007 and REF-008 description-led studies; REF-009 screenshot/walkthrough study documented |
| P3 — Pattern extraction and design system | 0% | Not started | No validated reusable pattern library |
| P4 — Apply lessons to personal projects | 0% | Not started | No user-selected project application |
| P5 — Validate, refine and document learning | 0% | Not started | No applied-pattern review |

The overall percentage is calculated using phase weights in [PROJECT_ROADMAP.md](PROJECT_ROADMAP.md): 15% from completed P1 plus 12.5% from P2, or 27.5%, rounded to 28%.

## Verified starting points

| Reference | What is known | What remains to be studied |
|---|---|---|
| The World of Peaches | Public source repository and MIT licence verified; five 1280 × 720 sections, visual configuration, theme, TMDL, DAX and HTML/CSS inspected | Open PBIX in Power BI Desktop; test interactions, accessibility and rendering |
| City Sustainability Scorecard | Public repository and MIT licence verified; six 1280 × 720 sections, 223 DAX files, 74 HTML templates, 29 CSS files, TMDL and selected visual configurations inspected | Open PBIX in Power BI Desktop; verify all six pages, field parameter, interactions and accessibility |
| Power BI Basketball Cards | 2025 Week 3 winner; screenshot and creator walkthrough show native-visual flippable card, button/list slicer navigation and shot chart over a court image | PBIX/source access remains unconfirmed; verify the exact card state implementation and accessibility if available |
| Deneb Power BI Example | Public PBIX and README; Deneb donut, dynamic-marker bar, tooltips and drillthrough documented; no licence file found | Secondary technical reference; study only unless reuse permission is confirmed |
| Deneb Template Showcase | MIT-licensed repository with 21 template specs, sample data, previews, custom BI Nexus theme and a 22-page PBIP showcase | Study source-level contracts and selected specs; runtime rendering remains pending |
| AstraVale SQL Health | Creator describes five pages, dataset and operational decision flow; public Power BI URL identified but not rendered | Inspect live report when a compatible browser is available; PBIX/source access remains unconfirmed |
| OECD Global Well-being | Creator describes dynamic SVG progress bars, anomaly-aware trends, country cross-filtering and gender small multiples; official winner status verified | Verify report rendering, progress-bar scale, anomaly behaviour and whether weighted-composite controls are part of the same report |
| Europe in Motion | Four-page report description, landing-page screenshot, HTML/CSS KPI technique and colour-blindness simulator claim verified | PBIX/source not confirmed; inspect full analytical pages and accessibility when available |
| SQL Radar | Three-page Signal/Diagnosis/Action structure; native/HTML split; screenshot and 903 KB PBIX attachment listed on source page | PBIX not downloaded/opened; verify licence, page layout and technical implementation |
| Microsoft Power BI samples | Official documentation and official sample repository provide sample artefacts | Select reports that teach useful structure, visual and interaction patterns |

See [REFERENCE_CATALOG.md](research/REFERENCE_CATALOG.md) for links and caveats.

## REF-008 study documents

- [Study notes](reference-studies/sql-radar/STUDY_NOTES.md)
- [Page architecture](reference-studies/sql-radar/PAGE_ARCHITECTURE.md)
- [Visual system](reference-studies/sql-radar/VISUAL_SYSTEM.md)
- [Technical notes](reference-studies/sql-radar/TECHNICAL_NOTES.md)
- [Transferable patterns](reference-studies/sql-radar/TRANSFERABLE_PATTERNS.md)

## REF-007 study documents

- [Study notes](reference-studies/europe-in-motion/STUDY_NOTES.md)
- [Page architecture](reference-studies/europe-in-motion/PAGE_ARCHITECTURE.md)
- [Visual system](reference-studies/europe-in-motion/VISUAL_SYSTEM.md)
- [Technical notes](reference-studies/europe-in-motion/TECHNICAL_NOTES.md)
- [Transferable patterns](reference-studies/europe-in-motion/TRANSFERABLE_PATTERNS.md)

## REF-011 study documents

- [Study notes](reference-studies/deneb-template-showcase/STUDY_NOTES.md)
- [Page architecture](reference-studies/deneb-template-showcase/PAGE_ARCHITECTURE.md)
- [Visual system](reference-studies/deneb-template-showcase/VISUAL_SYSTEM.md)
- [Technical notes](reference-studies/deneb-template-showcase/TECHNICAL_NOTES.md)
- [Transferable patterns](reference-studies/deneb-template-showcase/TRANSFERABLE_PATTERNS.md)

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

Begin the next source-based audit with REF-004, the official Microsoft Power BI sample set. Select one sample with a clear report architecture and inspect its PBIX/source materials, page structure, visual configuration, navigation and semantic model. Keep this as a learning reference rather than a personal project.

The SQL Radar PBIX attachment is listed publicly but has not been downloaded/opened. The World of Peaches and City Sustainability PBIX files also remain untested in Power BI Desktop.

The goal is to compare native Power BI implementation patterns with the hybrid and custom-visual approaches already studied.
