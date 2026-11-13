# Project Status

**As of:** 2026-11-13  
**Overall progress:** 2% (weighted estimate)  
**Current phase:** P1 — Reference discovery  
**Project state:** Research foundation established; reference catalogue seeded

## Executive status

This repository is a Power BI learning and design-research workspace. Its purpose is to study exceptional reports, understand their structure and implementation, extract transferable principles, and use those lessons to improve the user's separate personal projects.

The external reports are case studies, not the deliverables we are trying to recreate. The user's personal projects remain in their own repositories.

The initial project documentation and research structure have been committed. A preliminary reference shortlist exists. Two public source repositories and Microsoft's official sample resources have been identified at source level.

No complete reference study has yet been performed. No reusable theme or component has yet been built and tested. No personal project has been modified as part of this work.

## Phase scorecard

| Phase | Progress | Status | Evidence |
|---|---:|---|---|
| P1 — Reference discovery | 15% | In progress | Initial source shortlist and reference catalogue |
| P2 — Structural, visual and technical deconstruction | 0% | Not started | No completed reference study |
| P3 — Pattern extraction and design system | 0% | Not started | No validated reusable pattern library |
| P4 — Apply lessons to personal projects | 0% | Not started | No user-selected project application |
| P5 — Validate, refine and document learning | 0% | Not started | No applied-pattern review |

The overall percentage is calculated using phase weights in [PROJECT_ROADMAP.md](PROJECT_ROADMAP.md). It is not a measure of time elapsed.

## Verified starting points

| Reference | What is known | What remains to be studied |
|---|---|---|
| The World of Peaches | Public GitHub source repository; README lists PBIX, DAX, HTML/CSS, TMDL and theme resources; MIT licence declared | Open and inspect the report; map page architecture, components and design decisions |
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

Complete the first structured study of **The World of Peaches**:
1. Verify the current source tree and licence.
2. Inspect the available report artefacts.
3. Map page names, purposes, sequence and layout.
4. Study the theme, component organisation, DAX and HTML/CSS where available.
5. Record design decisions, strengths, limitations and unknowns.
6. Extract lessons that could transfer to the user's own Power BI work.

The output is a reference study and a set of transferable lessons, not a cloned dashboard.
