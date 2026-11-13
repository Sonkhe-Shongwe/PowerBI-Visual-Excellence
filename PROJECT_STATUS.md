# Project Status

**As of:** 2026-11-13  
**Overall progress:** 2% (weighted estimate)  
**Current phase:** P1 — Research and discovery  
**Project state:** Foundation established; research register seeded

## Executive status

The public repository has been created and the initial project structure and governance documents are being established. A preliminary reference shortlist exists. Two public source repositories and Microsoft's official sample resources have been verified at source level.

No dashboard has yet been forensically audited or reconstructed in this project. No Power BI theme or reusable component has yet been built or tested here.

## Phase scorecard

| Phase | Progress | Status | Evidence |
|---|---:|---|---|
| P1 — Research and discovery | 15% | In progress | Initial source shortlist and reference catalogue |
| P2 — Forensic design analysis | 0% | Not started | No completed audit |
| P3 — Design system development | 0% | Not started | No tested theme or component library |
| P4 — Dashboard reconstruction | 0% | Not started | No reconstruction |
| P5 — Visual and functional QA | 0% | Not started | No QA execution |
| P6 — Portfolio-grade original report | 0% | Not started | No original report |

The overall percentage is calculated using phase weights in [PROJECT_ROADMAP.md](PROJECT_ROADMAP.md). It is not a measure of time elapsed.

## Verified starting points

| Reference | What is verified | What is not yet done |
|---|---|---|
| The World of Peaches | Public GitHub repository; MIT licence; PBIX and source files are described in the repository; DAX, HTML/CSS, TMDL and theme resources are present | Local download, page-by-page inspection, interaction audit and reproduction |
| City Sustainability Scorecard | Public GitHub repository; MIT licence; PBIX, TMDL, DAX and HTML component resources are described in its README | Local download, page-by-page inspection, interaction audit and reproduction |
| AstraVale SQL Health | Public Microsoft Fabric Community championship report page and public report link | Confirm PBIX/source availability and complete a technical audit |
| Microsoft Power BI samples | Official documentation and official sample repository provide downloadable sample artefacts | Select and inspect individual reports |

See [REFERENCE_CATALOG.md](research/REFERENCE_CATALOG.md) for links and caveats.

## Current blockers / dependencies

- Selected PBIX files need to be downloaded and opened in Power BI Desktop for hands-on inspection.
- Some public reports may be viewable but may not expose their PBIX or underlying model.
- Custom visuals, external media and embedded assets may have separate licensing or availability conditions.
- Pixel-perfect reproduction may not be possible when the original visual assets, fonts, dimensions or interaction logic are unavailable.

## Next action

Complete the first forensic audit of **The World of Peaches**:
1. Verify the repository contents and MIT licence.
2. Obtain and open the PBIX in Power BI Desktop.
3. Capture each report page at a consistent canvas size.
4. Inspect the theme, source folders, DAX measures and HTML/CSS components.
5. Document the page layout and reusable patterns in the reconstruction workspace.

Do not mark P1 or P2 complete until the relevant exit criteria are met.
