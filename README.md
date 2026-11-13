# Power BI Visual Excellence

> Research, reverse-engineer, design and build exceptional Power BI reports through evidence-led visual engineering.

**Owner:** [Sonkhe-Shongwe](https://github.com/Sonkhe-Shongwe)  
**Repository:** [PowerBI-Visual-Excellence](https://github.com/Sonkhe-Shongwe/PowerBI-Visual-Excellence)  
**Status:** Foundation established · Research and discovery in progress  
**Last updated:** 2026-11-13

## Mission

Build a durable research and engineering programme for creating polished, professional, portfolio-grade Power BI reports.

We will study outstanding real-world reports, inspect downloadable Power BI Desktop files and Power BI Project sources where available, deconstruct their visual systems and implementation techniques, and apply the strongest ideas to original reports.

The goal is not to copy a screenshot blindly. The goal is to understand **why a report works, how it was built, what can be reproduced responsibly, and how to improve the result for a real business audience.**

## Scope

- Visual research and reference benchmarking.
- Report layout, composition, spacing and information hierarchy.
- Typography, colour systems, themes and reusable design tokens.
- Native Power BI visuals and advanced visual techniques.
- DAX patterns for dynamic titles, formatting, SVG and HTML-driven elements.
- Deneb / Vega-Lite and other custom visuals where justified.
- Navigation, bookmarks, drillthrough, tooltips, slicers and interactions.
- Accessibility, readability, performance and quality assurance.
- Original dashboard reconstruction and portfolio development.

**Scope distinction:** Our main build target is Power BI Desktop reports (PBIX, and PBIP when useful). A Power BI report can contain multiple interactive pages. A Power BI Service dashboard is a different, single-canvas artefact made from pinned tiles. We may study both, but we will label them correctly.

## Working principles

1. **Evidence before opinion.** Every reference has a source link and a recorded inspection status.
2. **Design before formatting.** Establish page purpose, hierarchy and layout before styling individual visuals.
3. **Native-first, not native-only.** Prefer maintainable native features; introduce SVG, HTML, Deneb or custom visuals when they solve a real design or analytical problem.
4. **Reproduce responsibly.** Learn from public work, respect licences and attribution, and do not redistribute assets or PBIX files without permission.
5. **Separate appearance from usability.** A visually impressive report must still be understandable, accessible and useful.
6. **Test every interaction.** Screenshots alone cannot prove that filters, bookmarks, drillthrough or tooltips work.
7. **Document decisions and failures.** The repository is the source of truth for project continuity.
8. **No unsupported completion claims.** A phase or deliverable is complete only when its acceptance evidence exists.

## Roadmap at a glance

| Phase | Focus | Status |
|---|---|---|
| P1 | Research and discovery | In progress |
| P2 | Forensic design analysis | Pending |
| P3 | Reusable design system | Pending |
| P4 | Dashboard reconstruction | Pending |
| P5 | Visual and functional QA | Pending |
| P6 | Original portfolio-grade report | Pending |

See [PROJECT_ROADMAP.md](PROJECT_ROADMAP.md) and [PROJECT_STATUS.md](PROJECT_STATUS.md) for progress, gates and evidence.

## Repository map

- **research/** — reference catalogue, audits and scoring.
- **design-system/** — design principles, themes and reusable patterns.
- **reconstructions/** — reference-specific analysis and original rebuilds.
- **techniques/** — DAX, SVG, HTML/CSS, Deneb and interaction notes.
- **quality-assurance/** — visual acceptance and functional test records.
- **changelog/** — chronological project history.

See [DOCUMENTATION_INDEX.md](DOCUMENTATION_INDEX.md) for the full navigation guide.

## First research references

These are initial candidates, not endorsements or completed audits:

- [The World of Peaches](https://github.com/gusbavia/the-world-of-peaches) — public MIT-licensed project with PBIX, TMDL source, DAX measures and HTML/CSS components.
- [City Sustainability Scorecard](https://github.com/gusbavia/city-sustainability-scorecard) — public MIT-licensed project with PBIX, TMDL source, DAX measures and HTML components.
- [AstraVale SQL Health](https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/world-champion-winner---live-finale-build---astravale-sql-health-report-by-mariu/5373203) — 2026 Power BI DataViz World Championship finale-winning report; public report inspection is available.
- [Microsoft Power BI samples](https://learn.microsoft.com/en-us/power-bi/create-reports/sample-datasets) — official sample reports and downloadable files.
- [Microsoft Power BI Desktop sample repository](https://github.com/microsoft/powerbi-desktop-samples) — official source repository for sample PBIX files and related resources.

The [reference catalogue](research/REFERENCE_CATALOG.md) records what is known, what remains unverified and what each reference may teach us.

## How we work

Each research item follows this sequence:

1. Find and cite the original source.
2. Verify what is actually available: live report, PBIX, PBIP, screenshots, source code, theme or documentation.
3. Inspect the report and record evidence.
4. Score it using the shared rubric only after inspection.
5. Extract reusable design and implementation patterns.
6. Build an original implementation with a clearly stated scope.
7. Compare, test and document the result.

## Current next action

Begin the forensic review of **The World of Peaches**. Verify the available files and licence, inspect the report pages and theme/source structure, then record page-level layout and component findings before attempting a reconstruction.

---

This repository documents learning and original implementation work. External projects remain the property of their respective creators and are linked for research and attribution.
