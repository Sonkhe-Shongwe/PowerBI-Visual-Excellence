# Project Status

**As of:** 2026-11-13  
**Overall progress:** 5% (weighted estimate)  
**Current phase:** P1 — Reference discovery
**Current focus:** REF-001 source-led study; Power BI Desktop/runtime validation pending  
**Project state:** Research foundation established; first reference study documented at source level

## Executive status

This repository is a Power BI learning and design-research workspace. Its purpose is to study exceptional reports, understand their structure and implementation, extract transferable principles, and use those lessons to improve the user's separate personal projects.

The external reports are case studies, not the deliverables we are trying to recreate. The user's personal projects remain in their own repositories.

The initial project documentation and research structure have been committed. The first case study, The World of Peaches, now has documented source-level findings covering its page architecture, visual system, model, DAX, HTML/CSS, theme and transferable patterns.

The source repository and licence were checked. Report section definitions, visual configurations, theme JSON, TMDL, DAX and component source were inspected. The PBIX has not yet been opened and tested in Power BI Desktop. Runtime interactions, performance, service rendering and accessibility therefore remain unverified.

No personal project has been modified through this research workspace.

## Phase scorecard

| Phase | Progress | Status | Evidence |
|---|---:|---|---|
| P1 — Reference discovery | 15% | In progress | Initial source shortlist and reference catalogue |
| P2 — Structural, visual and technical deconstruction | 10% | In progress | REF-001 source-level study documented; runtime validation pending |
| P3 — Pattern extraction and design system | 0% | Not started | No validated reusable pattern library |
| P4 — Apply lessons to personal projects | 0% | Not started | No user-selected project application |
| P5 — Validate, refine and document learning | 0% | Not started | No applied-pattern review |

The overall percentage is calculated using phase weights in [PROJECT_ROADMAP.md](PROJECT_ROADMAP.md): 2.25% from P1 plus 2.5% from P2, or 4.75%, rounded to 5%.

## Verified starting points

| Reference | What is known | What remains to be studied |
|---|---|---|
| The World of Peaches | Public source repository and MIT licence verified; five 1280 × 720 sections, visual configuration, theme, TMDL, DAX and HTML/CSS inspected | Open PBIX in Power BI Desktop; test interactions, accessibility and rendering |
| City Sustainability Scorecard | Public GitHub source repository; README lists PBIX, TMDL, DAX and HTML component resources; MIT licence declared | Inspect the report and determine which patterns are genuinely transferable |
| AstraVale SQL Health | Public Microsoft Fabric Community championship report page and public report link | Inspect report structure and confirm PBIX/source availability |
| Microsoft Power BI samples | Official documentation and official sample repository provide sample artefacts | Select reports that teach useful structure, visual and interaction patterns |

See [REFERENCE_CATALOG.md](research/REFERENCE_CATALOG.md) for links and caveats.

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
