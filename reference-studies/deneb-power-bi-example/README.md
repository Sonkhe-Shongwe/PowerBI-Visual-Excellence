# REF-010 | Deneb Power BI Example

**Study status:** Description-led technical study documented. The PBIX is listed in the public repository, but its internal report definition and Deneb specifications have not been extracted or opened in Power BI Desktop.
**Evidence type:** Repository metadata and file tree, creator README, and official Deneb documentation/release notes.
**Date checked:** 2026-11-14
**Study priority:** Medium. This is a focused technical learning reference, not a verified visual-design benchmark.

## Sources

### Reference report
- [Creator repository](https://github.com/BruntBroccoli/Deneb-Power-BI-Example)
- [Creator README](https://github.com/BruntBroccoli/Deneb-Power-BI-Example/blob/main/README.md)
- [Deneb PBIX](https://github.com/BruntBroccoli/Deneb-Power-BI-Example/blob/main/Deneb-Dashboard.pbix)

### Official Deneb documentation
- [Getting started](https://deneb.guide/docs/getting-started)
- [Dataset and data roles](https://deneb.guide/docs/dataset)
- [Interactivity overview](https://deneb.guide/docs/interactivity-overview)
- [Tooltips](https://deneb.guide/docs/interactivity-tooltips)
- [Context menu and drillthrough](https://deneb.guide/docs/interactivity-context-menu)
- [Cross-filtering](https://deneb.guide/docs/interactivity-selection)
- [Performance considerations](https://deneb.guide/docs/performance)
- [Field parameters](https://deneb.guide/docs/field-parameters)
- [Deneb change log](https://deneb.guide/docs/changelog)
- [Deneb releases](https://github.com/deneb-viz/deneb/releases)
- [Enterprise and security FAQ](https://deneb.guide/enterprise)

## Summary

BruntBroccoli's Power BI example demonstrates using Deneb, a custom visual powered by Vega-Lite, to create visual treatments the author says were difficult to achieve with native Power BI visuals.

The README identifies a taxonomy-style donut with tooltips and drillthrough, a horizontal bar with a dynamic marker, report-page tooltip functionality, drillthrough navigation, and a tolerance-zone spectrum bar. It names five report pages: How This Dashboard Works, Taxonomy, Drillthrough, Tooltip Page, and Tolerance Zones.

The dataset and visual theme are described as synthetic and flavour-based. The creator says the Deneb specifications were AI-generated.

## Repository inventory and discrepancies

The public GitHub tree contains three files:

| File | Size | What is verified |
|---|---:|---|
| Deneb-Dashboard.pbix | 4,533,410 bytes | PBIX file is present; contents not inspected |
| README.md | 1,418 bytes | Creator's description and page list inspected |
| Spicy_Data.xlsx | 11,956 bytes | Workbook is present; contents not inspected |

The README refers to `Spicy_Data.csv`, but the repository tree contains `Spicy_Data.xlsx`. This is a source-documentation discrepancy and should be checked when opening the report.

The repository metadata does not declare a licence and the inspected tree contains no LICENSE file. Treat the PBIX, workbook and creator-authored specifications as study-only. Do not copy or redistribute their assets or code without permission.

## Evidence boundaries

The report's page names and feature descriptions come from the creator README. They are not independently verified runtime behaviour. The PBIX is available, but its report layout, model, visual configuration, Deneb JSON, tooltip assignments and drillthrough fields remain unknown.

The report repository was last updated in July 2025. The Deneb version embedded in the PBIX is not established. Current Deneb 2.0/2.0.1 capabilities are documented separately as present-day technical context, not attributed to the older example.

Some pages on the current Deneb documentation site still display a Version 1.9 header, while the official change log and release index document Deneb 2.0 and 2.0.1. Use the change log for 2.0-specific behaviour and verify the installed version in Desktop.

No visual benchmark score is assigned. No personal project has been changed.

## Study documents

- [Study notes](STUDY_NOTES.md)
- [Page architecture](PAGE_ARCHITECTURE.md)
- [Visual system](VISUAL_SYSTEM.md)
- [Technical notes](TECHNICAL_NOTES.md)
- [Transferable patterns](TRANSFERABLE_PATTERNS.md)
- [Desktop validation register](DESKTOP_VALIDATION.md)

## Next inspection

Open the PBIX in Power BI Desktop after the REF-004 validation pass. Record the Deneb visual version, inspect every page, capture the actual Vega-Lite specifications, verify tooltip and drillthrough behaviour, test the dynamic marker and tolerance-zone calculations, and record accessibility and performance evidence.
