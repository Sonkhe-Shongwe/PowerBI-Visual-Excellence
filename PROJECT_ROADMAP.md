# Project Roadmap

**Last updated:** 2026-11-13  
**Current phase:** P2 — Structural, visual and technical deconstruction

This roadmap governs a research and learning programme. Percentages represent completed, evidenced work, not time spent or optimism.

The objective is to understand excellent Power BI work and transfer the strongest lessons into the user's own personal projects. External dashboard recreation is not a project phase or primary deliverable.

## Phase plan

| Phase | Weight | Current progress | Weighted contribution | Gate |
|---|---:|---:|---:|---|
| P1 — Reference discovery | 15% | 100% | 15% | A varied, sourced and prioritised reference set exists |
| P2 — Structural, visual and technical deconstruction | 25% | 30% | 7.5% | Selected reports have evidence-backed studies |
| P3 — Pattern extraction and design system | 25% | 0% | 0% | Transferable principles, patterns and technique notes are documented |
| P4 — Apply lessons to personal projects | 25% | 0% | 0% | User-selected lessons are applied in the user's own project repositories |
| P5 — Validate, refine and document learning | 10% | 0% | 0% | Applied patterns are reviewed and lessons captured |
| **Total** | **100%** |  | **22.5%** | **Overall progress: approximately 23%** |

Progress is rounded to the nearest whole percentage in the status summary. Phase weights are provisional and may be revised with a documented reason.

## P1 — Reference discovery

**Objective:** Build a high-quality, diverse and traceable collection of reports worth learning from.

Work:
- Identify strong reports from championship entries, practitioners, official Microsoft samples and credible portfolios.
- Classify each by use case, style, complexity and technical inspectability.
- Record original source links, access type, downloadable artefacts and licence details.
- Distinguish a screenshot, live report, PBIX and source repository.
- Select references that teach different skills rather than collecting visually similar examples.

Exit criteria:
- At least 10 relevant references recorded.
- Each reference has an original source link and verification status.
- At least 5 high-priority references selected for deeper study.
- No reference receives a final score before an adequate study.

**Status:** Exit criteria met on 2026-11-13. Ten references are recorded, with five marked high priority. The priority labels select learning candidates; they are not quality scores.

## P2 — Structural, visual and technical deconstruction

**Objective:** Understand how selected reports are organised, designed and engineered.

For each selected report, study:
- Page count, page dimensions, page purpose and narrative sequence.
- Layout grid, margins, spacing, alignment, grouping and visual density.
- Typography, colour, contrast, backgrounds, borders and visual states.
- Visual types, chart encodings, labels, legends, tooltips and conditional formatting.
- Navigation, slicers, bookmarks, drillthrough and responsive behaviour where inspectable.
- Theme JSON, semantic model, DAX, Power Query, SVG, HTML/CSS, Deneb and custom visuals when source files permit.
- Accessibility, performance and maintainability.
- What works well, what does not, and why.

Exit criteria:
- At least 3 complete reference studies.
- Page architecture and component inventories recorded.
- Findings supported by screenshots, source files or live-report observations where available.
- Inferences and unknowns explicitly labelled.
- Each study identifies transferable lessons rather than proposing a full clone.

## P3 — Pattern extraction and design system

**Objective:** Turn observations into a reusable knowledge base.

Deliverables:
- Page architecture patterns for common reporting needs.
- Layout, grid, spacing and hierarchy rules.
- Colour tokens and semantic colour guidance.
- Typography scale and hierarchy.
- Power BI theme JSON examples where useful.
- Reusable component specifications for KPI cards, headers, filters, navigation, tables and charts.
- DAX, SVG, HTML/CSS, Deneb and interaction technique notes.
- Accessibility, maintainability and performance guidance.
- Clear explanation of when a pattern is useful and when it is not.

Exit criteria:
- A documented set of reusable design principles and patterns.
- Technique notes include implementation context, limitations and sources.
- Any code or theme example is tested before being labelled as tested.
- Patterns are generic enough to adapt to different datasets and business problems.

## P4 — Apply lessons to personal projects

**Objective:** Use the research to improve the user's own projects, without replacing their original goals or forcing them into an external dashboard's design.

Rules:
- The user decides which personal project is the target.
- The personal project's own repository remains the source of truth for its implementation.
- Apply only patterns that solve a real design, usability or analytical need.
- Adapt patterns to the project's audience, data and business question.
- Do not copy another creator's branding, assets or report wholesale.
- Keep this repository focused on learning records and reusable guidance; do not duplicate personal project source files here.

Exit criteria:
- A user-selected project has benefited from one or more documented patterns.
- The reason for each adopted pattern is clear.
- The implementation is recorded in the personal project's own repository.
- Any design choices rejected or modified are briefly explained.

## P5 — Validate, refine and document learning

**Objective:** Check whether the lessons improve the user's actual work.

Review:
- Does the page hierarchy make the report easier to understand?
- Is the visual design more consistent and intentional?
- Are charts appropriate and readable?
- Are interactions predictable and useful?
- Are accessibility and performance preserved?
- Did the applied pattern genuinely improve the report, or did it add unnecessary complexity?

Exit criteria:
- Applied patterns reviewed in their actual project context.
- Useful improvements and failed experiments recorded.
- Design-system guidance updated based on what was learned.
- Next research or application priority identified.

## Operating cadence

At the end of every work session:
1. Update [PROJECT_STATUS.md](PROJECT_STATUS.md).
2. Update [SESSION_HANDOFF_CURRENT.md](SESSION_HANDOFF_CURRENT.md).
3. Add material changes to [CHANGELOG.md](changelog/CHANGELOG.md).
4. Record sources and study findings in the relevant reference folder.
5. Capture transferable lessons in the design system or techniques library.
6. If a personal project was changed, keep its implementation and commit history in that project's own repository.
7. State the next single action and any dependency.

Do not advance a phase merely to make the roadmap look active. Do not create reconstruction work just to demonstrate activity.
