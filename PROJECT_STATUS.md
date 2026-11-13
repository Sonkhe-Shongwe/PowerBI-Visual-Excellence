# Project Status

**As of:** 2026-11-13  
**Overall progress:** 20% (weighted estimate)  
**Current phase:** P2 — Structural, visual and technical deconstruction
**Current focus:** Third reference study, beginning with REF-003 AstraVale SQL Health  
**Project state:** Reference discovery gate complete; two source-level reference studies documented

## Executive status

This repository is a Power BI learning and design-research workspace. Its purpose is to study exceptional reports, understand their structure and implementation, extract transferable principles, and use those lessons to improve the user's separate personal projects.

The external reports are case studies, not the deliverables we are trying to recreate. The user's personal projects remain in their own repositories.

The initial project documentation and research structure have been committed. Two source-led studies are now documented: The World of Peaches and City Sustainability Scorecard. The studies cover page architecture, visual systems, semantic models, DAX, HTML/CSS, interactions, technical dependencies and transferable patterns.

Both public repositories and declared MIT licences were checked. Their report definitions, selected visual configurations, TMDL, DAX and component source were inspected. Neither PBIX has yet been opened and tested in Power BI Desktop. Runtime interactions, performance, service rendering and accessibility therefore remain unverified.

No personal project has been modified through this research workspace.

## Phase scorecard

| Phase | Progress | Status | Evidence |
|---|---:|---|---|
| P1 — Reference discovery | 100% | Complete | Ten references recorded; five high-priority candidates selected |
| P2 — Structural, visual and technical deconstruction | 20% | In progress | REF-001 and REF-002 source-level studies documented; runtime validation pending |
| P3 — Pattern extraction and design system | 0% | Not started | No validated reusable pattern library |
| P4 — Apply lessons to personal projects | 0% | Not started | No user-selected project application |
| P5 — Validate, refine and document learning | 0% | Not started | No applied-pattern review |

The overall percentage is calculated using phase weights in [PROJECT_ROADMAP.md](PROJECT_ROADMAP.md): 15% from completed P1 plus 5% from P2, or 20%.

## Verified starting points

| Reference | What is known | What remains to be studied |
|---|---|---|
| The World of Peaches | Public source repository and MIT licence verified; five 1280 × 720 sections, visual configuration, theme, TMDL, DAX and HTML/CSS inspected | Open PBIX in Power BI Desktop; test interactions, accessibility and rendering |
| City Sustainability Scorecard | Public repository and MIT licence verified; six 1280 × 720 sections, 223 DAX files, 74 HTML templates, 29 CSS files, TMDL and selected visual configurations inspected | Open PBIX in Power BI Desktop; verify all six pages, field parameter, interactions and accessibility |
| Power BI Basketball Cards | 2025 Week 3 winner; creator walkthrough describes native-visual flippable cards, navigation and a shot-location chart | Locate PBIX or inspect the public walkthrough and report interaction details |
| Deneb Power BI Example | Public PBIX and README; Deneb donut, dynamic-marker bar, tooltips and drillthrough documented; no licence file found | Study Vega-Lite specs in the PBIX if opened; keep reuse permissions unassumed |
| AstraVale SQL Health | Public Microsoft Fabric Community championship report page and public report link | Inspect report structure and confirm PBIX/source availability |
| Microsoft Power BI samples | Official documentation and official sample repository provide sample artefacts | Select reports that teach useful structure, visual and interaction patterns |

See [REFERENCE_CATALOG.md](research/REFERENCE_CATALOG.md) for links and caveats.

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

Begin the third reference study with REF-003 AstraVale SQL Health. Establish the report's page sequence, information hierarchy, visual types, operational monitoring patterns and decision flow from the public source. Verify whether a public live report, downloadable PBIX or source files are actually available before claiming deeper inspection.

Runtime inspection of REF-001 and REF-002 remains a separate user-side option when Power BI Desktop is available. The next research step does not depend on the user opening either PBIX.

The goal is to understand a contrasting operational dashboard and extract transferable lessons, not to recreate it.
