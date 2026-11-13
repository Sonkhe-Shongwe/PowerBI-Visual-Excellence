# Project Roadmap

**Last updated:** 2026-11-13  
**Current phase:** P1 — Research and discovery

This roadmap is the project control document. Percentages represent completed, evidenced work, not time spent or optimism.

## Phase plan

| Phase | Weight | Current progress | Weighted contribution | Gate |
|---|---:|---:|---:|---|
| P1 — Research and discovery | 15% | 15% | 2.25% | Reference set is sourced, classified and prioritised |
| P2 — Forensic design analysis | 20% | 0% | 0% | Selected references have completed evidence-backed audits |
| P3 — Design system development | 15% | 0% | 0% | Reusable design rules, tokens and templates are documented and tested |
| P4 — Dashboard reconstruction | 25% | 0% | 0% | At least one original report reconstruction is functionally complete |
| P5 — Visual and functional QA | 15% | 0% | 0% | Visual and interaction acceptance tests pass with recorded evidence |
| P6 — Portfolio-grade original report | 10% | 0% | 0% | Original report is complete, documented and portfolio-ready |
| **Total** | **100%** |  | **2.25%** | **Overall progress: approximately 2%** |

Progress is rounded to the nearest whole percentage in the status summary. The phase percentages are provisional baselines and must be updated when evidence changes.

## P1 — Research and discovery

**Objective:** Build a high-quality, diverse and traceable reference set.

Work:
- Identify strong Power BI reports from championship entries, practitioners, official Microsoft samples and credible portfolios.
- Classify each reference by use case, visual style, complexity and technical inspectability.
- Record direct source links, report access, downloadable artefacts and licence details.
- Avoid treating a screenshot, live report and downloadable PBIX as equivalent evidence.
- Prioritise references that can teach transferable techniques.

Exit criteria:
- At least 10 relevant references recorded.
- Each reference has an original source link and verification status.
- At least 5 high-priority references selected for deeper inspection.
- No reference receives a final score before an audit.

## P2 — Forensic design analysis

**Objective:** Understand selected references at both visual and technical levels.

For each selected report, inspect:
- Page count, page dimensions and page purpose.
- Layout grid, margins, spacing, alignment and visual density.
- Typography, colour, contrast, backgrounds, borders and visual states.
- Visual types, chart encodings, labels, legends, tooltips and conditional formatting.
- Navigation, slicers, bookmarks, drillthrough and responsive behaviour where applicable.
- Theme JSON, semantic model, DAX, SVG, HTML/CSS, Deneb and custom visuals when source files permit inspection.
- Accessibility, performance considerations and maintainability.

Exit criteria:
- At least 3 complete forensic audits.
- Screenshots or evidence references recorded where permitted.
- Reusable patterns separated from one-off design decisions.
- Unknowns and limitations explicitly listed.

## P3 — Reusable design system

**Objective:** Convert research findings into a consistent, reusable Power BI design system.

Deliverables:
- Design principles and page-layout patterns.
- Colour tokens and semantic colour rules.
- Typography scale and hierarchy.
- Spacing, grid and sizing rules.
- Power BI theme JSON files with documented usage.
- Reusable page backgrounds, headers, KPI patterns and navigation patterns.
- Component specifications for native visuals and advanced techniques.
- Accessibility and interaction conventions.

Exit criteria:
- A documented design system.
- At least one theme tested in Power BI Desktop.
- Reusable components tested in more than one report context where practical.
- Clear guidance on when to use native visuals versus custom techniques.

## P4 — Dashboard reconstruction

**Objective:** Recreate selected design patterns in original Power BI work.

Rules:
- Rebuild the design using our own data and assets unless reuse is explicitly licensed.
- State what is being reconstructed: full report, one page, one component or a technique.
- Keep a reference-to-implementation comparison.
- Preserve the analytical meaning of the visuals.
- Do not claim exact reproduction if the original source or behaviour cannot be inspected.

Exit criteria:
- At least one complete multi-page or clearly scoped report reconstruction.
- Source project and implementation notes stored in the repository.
- DAX, theme and custom component sources documented.
- Functional interactions tested.

## P5 — Visual and functional QA

**Objective:** Prove that the report is visually coherent and works correctly.

Checks:
- Compare screenshots at equivalent canvas dimensions.
- Inspect alignment, spacing, typography, colour, chart geometry and visual hierarchy.
- Test every slicer, bookmark, button, tooltip, drillthrough and navigation path.
- Check readability, accessibility, performance and data correctness.
- Record defects, severity, fixes and retest results.

Exit criteria:
- Visual acceptance checklist completed.
- Functional test register passed or exceptions formally documented.
- Before/after evidence retained.
- No critical defects remain.

## P6 — Portfolio-grade original report

**Objective:** Create an original report that demonstrates the strongest techniques without depending on copied branding or a copied dashboard.

Deliverables:
- Clear business question and audience.
- Reliable data model and documented transformations.
- Purposeful multi-page narrative.
- Consistent visual identity and tested interactions.
- Accessibility and QA evidence.
- Screenshots, project documentation and portfolio case study.

Exit criteria:
- Report is complete and reproducible.
- All critical QA checks pass.
- Portfolio explanation communicates the problem, design decisions, implementation and insights.

## Operating cadence

At the end of every work session:
1. Update [PROJECT_STATUS.md](PROJECT_STATUS.md).
2. Update [SESSION_HANDOFF_CURRENT.md](SESSION_HANDOFF_CURRENT.md).
3. Add material changes to [CHANGELOG.md](changelog/CHANGELOG.md).
4. Record new sources and decisions in the relevant register.
5. State the next single action and any dependency.

A phase may remain in progress across multiple sessions. Do not advance a phase merely to make the roadmap look active.
