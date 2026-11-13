# REF-001 — The World of Peaches: Study Notes

**Creator:** Gus Bavia  
**Original repository:** https://github.com/gusbavia/the-world-of-peaches  
**Microsoft Fabric Community entry:** https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/world-champion-winner---the-world-of-peaches-by-gus-bavia/5135424  
**Creator's process notes:** https://www.gusbavia.com/showcase/world-of-peaches-ep01 and https://www.gusbavia.com/showcase/world-of-peaches-ep02  
**Status:** In progress  
**Study type:** Source-led structural, visual and technical study  
**Last updated:** 2026-11-13

## Executive finding

The strongest lesson is not a particular chart or colour palette. It is the way the report is treated as a designed analytics product before it becomes a Power BI file.

The creator describes a process built around a data audit, a written narrative brief, a design system, an annotated wireframe and components developed separately before integration. The public source repository makes that approach unusually inspectable: it contains the PBIX, report layout, TMDL model, theme JSON, DAX measures and HTML/CSS component templates.

The report uses a hybrid architecture. Native Power BI elements handle important analytical and navigation functions, while a custom HTML Content visual renders bespoke cards, charts and narrative components. This allows a highly controlled visual identity, but it also introduces custom-visual, DAX and external-asset dependencies.

**Our objective:** understand the structure and decisions, then extract patterns that can be adapted to our own Power BI work. We are not rebuilding the report.

## 1. What the report is about

The report explores global peach production and international trade using FAOSTAT data.

The analytical subject matter includes:
- Production volume.
- Harvested area.
- Yield and production efficiency.
- Export and import values.
- Trade balance.
- Country and continental comparisons.
- Historical trends from 2010 to 2024.

The creator's public materials describe coverage across 79 countries. The report moves from a global overview into production and trade analysis, with a tabular page for detailed inspection.

## 2. Evidence inspected

| Evidence | What was inspected | Confidence |
|---|---|---|
| GitHub README | Report purpose, file inventory, creator's stated approach, data and reuse notes | High |
| GitHub repository tree | Actual paths for PBIX, DAX, HTML/CSS, TMDL, theme, report sections and bookmarks | High |
| LICENSE | Repository declares MIT | High |
| Report section JSON | Five page names and 1280 × 720 dimensions | High |
| Visual container configuration | Visual types, positions, sizes, tab order and some bindings | High |
| Theme JSON | Palette, text classes and visual style definitions | High |
| TMDL | Model tables, relationships, calculated selector tables and Power Query source paths | High |
| DAX and HTML/CSS examples | KPI row, trend chart, production waffle, trade insight and trade KPI tower | High |
| Public screenshots and creator's process notes | Visible page composition and stated design workflow | Medium to high |

### Important inspection boundary

The PBIX is listed in the public repository, but it has not yet been opened and interacted with in Power BI Desktop during this study. Findings about source structure are stronger than findings about runtime behaviour. Interactions, rendering, performance, responsive behaviour and Power BI Service compatibility remain to be tested.

The public repository declares an MIT licence. This does not automatically settle the reuse rights of every external font, image, video, icon endpoint or other third-party dependency. Check those separately before reusing assets.

## 3. The creator's stated design process

The creator's public Episode 01 describes four foundations before visual construction:

1. **Raw data audit:** establish which fields exist, their structure and what needs reshaping or calculation.
2. **Narrative brief:** define the objective, audience, questions and the role of each page or visual.
3. **Theme and design system:** decide colour roles, typography, imagery direction and spacing rules before styling individual elements.
4. **Wireframe and data mapping:** connect each planned visual to its source fields, measures, aggregation and filter context.

In Episode 02, the creator describes four execution practices:

1. Wireframe in Pencil.dev, kept alongside code in VS Code.
2. Design tokens expressed in CSS and translated into a Power BI theme JSON.
3. HTML components built and refined individually with dummy data before integration.
4. Assets curated for the subject matter, with motion used selectively.

These are the creator's published descriptions of the process, not steps independently observed in a live development session.

**Transferable lesson:** a dashboard should have a clear brief, a data map, a visual system and a layout plan before the report canvas is populated.

## 4. Structural findings

The report source contains five sections:

- Welcome
- Overview
- Production
- Trade
- Tabular View

This is best described as **four analytical pages plus a Welcome/cover page**. Some public descriptions refer to four pages, apparently counting the analytical pages rather than the cover.

All five section definitions specify a 1280 × 720 canvas, a 16:9 aspect ratio.

The analytical pages share a consistent shell:
- A dark left-side navigation area.
- A page navigator in the sidebar.
- A How to Read entry near the bottom of the sidebar.
- Year and continent filters near the top-right.
- A main content area to the right of the sidebar.
- A hidden tutorial component and bookmark-based open/close states.

See [PAGE_ARCHITECTURE.md](PAGE_ARCHITECTURE.md) for the page-by-page inventory and coordinates.

## 5. Visual and interaction findings

The visual language is warm and editorial rather than a generic corporate template:
- Peach and burnt-orange accents.
- Deep brown and warm neutral surfaces.
- Light, uncluttered content panels.
- Rounded cards and restrained dividers.
- Serif display typography paired with a clean sans-serif interface font.
- Subject-specific photography and selected motion.

The report is not made entirely from custom visuals. The inspected report configuration includes:
- HTML Content visuals for bespoke components.
- A Shape Map for geographic analysis.
- Standard slicers for year and continent.
- An advanced slicer visual for metric or trade-flow selection.
- A page navigator for report navigation.
- Image visuals used for linked or bookmark-driven controls.

The creator's community post states that the report includes alt text, a logical tab order, WCAG-compliant contrast and guided tutorials. The source repository also contains dedicated alt-text measures and tutorial components. Runtime accessibility still needs to be tested.

See [VISUAL_SYSTEM.md](VISUAL_SYSTEM.md) and [PAGE_ARCHITECTURE.md](PAGE_ARCHITECTURE.md).

## 6. Technical findings

The public source repository contains:
- 45 standalone DAX files.
- 17 HTML component templates.
- 16 separate CSS files.
- TMDL semantic-model source.
- A theme JSON.
- Report section and visual configuration.
- Eight bookmark folders: four Tutorial and four Close states.
- The full PBIX file.

The model includes two subject-area fact tables, Peach Production and Peach Trade, with shared Countries and Year dimensions. The Year dimension covers 2010–2024. The model also includes calculated selector tables for report-specific metric and view choices.

Several major components are assembled as HTML strings by DAX measures and rendered through the HTML Content visual. Examples include the dynamic KPI row, overview trend chart, production waffle, trade insight and trade KPI tower.

The creator's README says the dynamic layer uses field parameters. The exposed TMDL selector tables inspected in this study are calculated DATATABLE-based selectors. We should not label these specific tables as native Power BI field parameters without checking the complete model metadata and PBIX.

See [TECHNICAL_NOTES.md](TECHNICAL_NOTES.md).

## 7. Critical evaluation

### What appears especially strong

- Design work is planned before the report canvas is populated.
- The same visual identity is carried across pages.
- Page purpose and analytical sequence are easy to distinguish.
- Native Power BI capabilities and custom HTML components are combined selectively.
- Dynamic measures let components respond to the selected analytical context.
- The report includes tutorial and accessibility considerations rather than treating them as afterthoughts.
- The source repository is organised well enough to learn from individual components.

### Trade-offs and risks to investigate

- Custom HTML visuals add a dependency that must be installed and tested in the target Power BI environment.
- Long DAX measures that generate HTML can become difficult to debug and maintain.
- External fonts, imagery, video and icon endpoints can introduce connectivity, licensing, security and rendering dependencies.
- Motion may improve an editorial experience but can distract in operational reporting or affect users who prefer reduced motion.
- The source model uses local CSV paths for the two FAOSTAT fact tables. The creator explicitly notes that users must repoint those sources to refresh the data.
- Some page-level design is supplied through embedded background image resources. This may make parts of the shell less directly editable than native Power BI shapes; confirm the exact division before adapting the approach.
- Small labels in custom components need to be checked at the actual viewing size.

## 8. Benchmark status

**No numerical benchmark score assigned yet.**

The current evidence is strong for source architecture and component design, but the PBIX has not been opened and tested interactively at its intended size. The scorecard requires more than a thumbnail or source inspection.

A future score should include:
- A full-size visual review of each analytical page.
- Interaction tests for slicers, bookmarks, page navigation and hover states.
- Accessibility and tab-order checks.
- Power BI Desktop and, if relevant, Power BI Service rendering checks.
- Performance and refresh checks.

## 9. Next study action

Open the PBIX in Power BI Desktop and verify the report as a user would experience it. Focus on navigation, filters, dynamic visuals, tutorial overlays, tooltips and rendering. Record any differences between the source configuration and observed behaviour.

The next output should close the runtime-evidence gap. It should not be a full dashboard recreation.
