# The World of Peaches — Reference Study

**Reference:** [gusbavia/the-world-of-peaches](https://github.com/gusbavia/the-world-of-peaches)  
**Reference ID:** REF-001  
**Status:** Source-level study documented; Power BI Desktop/runtime inspection pending  
**Role:** First structured case study

## Why study this report?

The public repository appears to provide unusually rich source material for understanding not just the final report appearance, but also how its design and components are organised.

The creator's README describes this as the 2026 Power BI World Championship winning report and lists:
- A downloadable PBIX.
- 45 DAX measures organised by report page.
- 17 HTML component templates with separate CSS.
- TMDL semantic-model source.
- Report layout and bookmark definitions.
- A theme JSON containing design tokens and visual defaults.
- An MIT licence.

These are source-repository claims. They are not a substitute for inspecting the actual report and files.

## Learning questions

1. How is the report divided into pages, and what is the purpose of each page?
2. What is the narrative or information journey from one page to another?
3. How are margins, spacing, alignment, grids and visual groupings used?
4. How does the report establish typography and visual hierarchy?
5. How are colour, backgrounds, cards, borders and other surfaces used?
6. Which visual components are native Power BI visuals, and which use HTML/CSS or other techniques?
7. How are DAX measures organised and what roles do they serve?
8. What does the theme JSON control?
9. How are bookmarks, navigation and interactive states structured?
10. Which decisions are useful principles that can transfer to other reports?

## Planned study outputs

- STUDY_NOTES.md — evidence-backed findings and critical evaluation.
- PAGE_ARCHITECTURE.md — page-by-page purpose and information structure.
- VISUAL_SYSTEM.md — layout, typography, colour and component observations.
- TECHNICAL_NOTES.md — theme, DAX, TMDL, HTML/CSS and interaction findings.
- TRANSFERABLE_PATTERNS.md — reusable lessons and where they may be useful.

## Study procedure

1. Verify the current repository tree and licence.
2. Confirm which artefacts are available for inspection.
3. Open the PBIX in Power BI Desktop if available.
4. Record page names, purposes, sequence and layout.
5. Inspect the theme JSON and source organisation.
6. Study representative DAX and HTML/CSS components.
7. Explain the structural, visual and technical decisions.
8. Record strengths, limitations and unknowns.
9. Extract transferable patterns.

## Licensing and attribution

Do not commit the creator's PBIX, extracted code, images or media into this repository unless the exact licence and asset conditions have been checked. Link to the original source and retain required notices when adapting permitted code.

## Current findings

The source defines five sections: Welcome, Overview, Production, Trade and Tabular View. This is four analytical pages plus a cover/entry page. All five use a 1280 × 720 canvas.

The report combines native Power BI elements with a custom HTML Content visual. The public source includes 45 DAX files, 17 HTML templates, 16 CSS files, TMDL model source, a theme JSON and report configuration.

The strongest learning opportunity is the creator's design-first workflow: data audit, narrative brief, design system, annotated wireframe and isolated component development before Power BI integration.

## Current next action

Open the PBIX in Power BI Desktop and verify the actual experience: page navigation, year/continent filters, metric selectors, map interactions, tutorial overlays, hover states and rendering. Record runtime observations separately from source-level findings.

The output remains understanding and transferable knowledge, not a cloned dashboard.
