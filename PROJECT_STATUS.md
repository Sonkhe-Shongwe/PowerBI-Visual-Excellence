# Project Status

**As of:** 2026-11-13  
**Overall progress:** 7% (weighted estimate)  
**Current phase:** P1 — Reference discovery
**Current focus:** REF-002 source-led study documented; REF-001 and REF-002 runtime validation pending  
**Project state:** Research foundation established; two source-level reference studies documented

## Executive status

This repository is a Power BI learning and design-research workspace. Its purpose is to study exceptional reports, understand their structure and implementation, extract transferable principles, and use those lessons to improve the user's separate personal projects.

The external reports are case studies, not the deliverables we are trying to recreate. The user's personal projects remain in their own repositories.

The initial project documentation and research structure have been committed. Two source-led studies are now documented: The World of Peaches and City Sustainability Scorecard. The studies cover page architecture, visual systems, semantic models, DAX, HTML/CSS, interactions, technical dependencies and transferable patterns.

Both public repositories and declared MIT licences were checked. Their report definitions, selected visual configurations, TMDL, DAX and component source were inspected. Neither PBIX has yet been opened and tested in Power BI Desktop. Runtime interactions, performance, service rendering and accessibility therefore remain unverified.

No personal project has been modified through this research workspace.

## Phase scorecard

| Phase | Progress | Status | Evidence |
|---|---:|---|---|
| P1 — Reference discovery | 15% | In progress | Eight initial references recorded; 10-reference and prioritisation gates remain |
| P2 — Structural, visual and technical deconstruction | 20% | In progress | REF-001 and REF-002 source-level studies documented; runtime validation pending |
| P3 — Pattern extraction and design system | 0% | Not started | No validated reusable pattern library |
| P4 — Apply lessons to personal projects | 0% | Not started | No user-selected project application |
| P5 — Validate, refine and document learning | 0% | Not started | No applied-pattern review |

The overall percentage is calculated using phase weights in [PROJECT_ROADMAP.md](PROJECT_ROADMAP.md): 2.25% from P1 plus 5% from P2, or 7.25%, rounded to 7%.

## Verified starting points

| Reference | What is known | What remains to be studied |
|---|---|---|
| The World of Peaches | Public source repository and MIT licence verified; five 1280 × 720 sections, visual configuration, theme, TMDL, DAX and HTML/CSS inspected | Open PBIX in Power BI Desktop; test interactions, accessibility and rendering |
| City Sustainability Scorecard | Public repository and MIT licence verified; six 1280 × 720 sections, 223 DAX files, 74 HTML templates, 29 CSS files, TMDL and selected visual configurations inspected | Open PBIX in Power BI Desktop; verify all six pages, field parameter, interactions and accessibility |
| AstraVale SQL Health | Public Microsoft Fabric Community championship report page and public report link | Inspect report structure and confirm PBIX/source availability |
| Microsoft Power BI samples | Official documentation and official sample repository provide sample artefacts | Select reports that teach useful structure, visual and interaction patterns |

See [REFERENCE_CATALOG.md](research/REFERENCE_CATALOG.md) for links and caveats.

## REF-002 study documents

- [Study notes](reference-studies/city-sustainability-scorecard/STUDY_NOTES.md)
- [Page architecture](reference-studies/city-sustainability-scorecard/PAGE_ARCHITECTURE.md)
- [Visual system](reference-studies/city-sustainability-scorecard/VISUAL_SYSTEM.md)
- [Technical notes](reference-studies/city-sustainability-scorecard/TECHNICAL_NOTES.md)
- [Transferable patterns](reference-studies/city-sustainability-scorecard/TRANSFERABLE_PATTERNS.md)

## Current boundaries

- Do not clone an external report as the default next step.
- Do not treat an attractive screenshot as evidence of implementation details.
- Do not copy a creator's PBIX or assets into this repository without checking the relevant rights.
- Do not move the user's personal project source files into this learning repository.
- Do not choose or change the user's personal project scope without their direction.
- Use isolated experiments only when they answer a specific technical learning question.

## Next action

Complete runtime inspection of REF-001 in Power BI Desktop:
1. Open the PBIX.
2. Test page navigation and filter synchronisation.
3. Test metric and view selectors.
4. Open and close tutorial overlays.
5. Test map interactions and hover states.
6. Check text readability and accessibility at the target display size.
7. Record any differences between source configuration and observed behaviour.

The goal is to close the runtime-evidence gap, not to recreate the report.
