# Deneb Template Showcase — Reference Study

**Maintainer:** InsightfulAnalytics / Timothy Osborn  
**Reference ID:** REF-011  
**Original repository:** https://github.com/InsightfulAnalytics/Deneb  
**Licence:** MIT  
**Status:** Source-level technical study documented; Power BI Desktop/runtime rendering pending

## Why this reference is valuable

This repository is a curated Deneb/Vega/Vega-Lite template library accompanied by a real Power BI Project (PBIP) showcase. It is much richer than a single example PBIX because it exposes reusable specifications, field contracts, sample data, preview images, theme tokens, a showcase report and automated validation.

The repository contains:
- 21 reusable Deneb templates.
- 21 preview images.
- 21 sample-data CSV files.
- Template README files and render configuration.
- A PBIP showcase with 22 report pages: one KPI dashboard page and one page for each template.
- A custom BI Nexus theme.
- Automated template validation.
- MIT licence.

## Study documents

- [STUDY_NOTES.md](STUDY_NOTES.md) — evidence, architecture and critical evaluation.
- [PAGE_ARCHITECTURE.md](PAGE_ARCHITECTURE.md) — showcase report structure and KPI dashboard layout.
- [VISUAL_SYSTEM.md](VISUAL_SYSTEM.md) — BI Nexus theme, visual language and component patterns.
- [TECHNICAL_NOTES.md](TECHNICAL_NOTES.md) — Vega/Vega-Lite, template contracts, Deneb helpers and validation.
- [TRANSFERABLE_PATTERNS.md](TRANSFERABLE_PATTERNS.md) — reusable engineering and design practices.

## Main finding

The most valuable lesson is the complete component lifecycle:
1. Define a visual's data contract.
2. Build a Vega or Vega-Lite specification.
3. Expose parameters for colours, labels, formatting and layout.
4. Provide sample data and a preview.
5. Validate the template automatically.
6. Demonstrate it in a real PBIP report.

This is a strong reference for learning how to build and maintain custom visuals as a reusable library rather than one-off dashboard hacks.

## Showcase dashboard

The PBIP includes a page named KPI Dashboard 2015 with a 1600 × 900 canvas and 12 Deneb visual components. Four KPI cards sit across the top, with eight analytical components arranged in four columns below.

The page combines a custom BI Nexus theme with the Fluent 2 Power BI base theme and a registered SVG background.

## Evidence boundary

The GitHub source tree, MIT licence, README, selected template specifications and READMEs, theme JSON, showcase layout JSON, TMDL model, report definition and selected visual configurations have been inspected.

The PBIP has not been opened and rendered in Power BI Desktop in this environment. The study is therefore source-level: exact runtime rendering, performance, cross-filtering, custom visual compatibility and accessibility remain unverified.

The repository's P&L performance figures are author-reported and have not been independently reproduced.

## Next action

Use the library as a technical reference for Deneb. Select a small number of templates to understand in depth, then decide whether any technique solves a real need in a user's separate Power BI project. Do not copy the showcase dashboard as a personal project.
