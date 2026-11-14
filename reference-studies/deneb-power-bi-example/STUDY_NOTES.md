# Study Notes

## 1. Reference identity

- **Reference ID:** REF-010
- **Report:** Deneb Power BI Example
- **Creator:** BruntBroccoli
- **Repository:** https://github.com/BruntBroccoli/Deneb-Power-BI-Example
- **Scenario:** Synthetic flavour-themed dataset and visuals
- **Report file:** Deneb-Dashboard.pbix
- **Study date:** 2026-11-14
- **Study type:** Description-led technical study
- **Priority:** Medium

## 2. Purpose

The creator says the report demonstrates how Deneb, a custom visual powered by Vega-Lite, can overcome limitations of native Power BI visuals.

The README positions the report as an educational example. It describes Deneb visuals, tooltips, drillthrough and AI-generated specifications. It does not provide a detailed business decision brief or identify a real operational audience.

## 3. Verified repository evidence

The public repository metadata and recursive file tree were inspected. The repository contains:
- Deneb-Dashboard.pbix (4,533,410 bytes).
- README.md (1,418 bytes).
- Spicy_Data.xlsx (11,956 bytes).

The README says the data file is `Spicy_Data.csv`, while the actual tree lists `Spicy_Data.xlsx`. The workbook contents have not been inspected.

The repository metadata has no declared licence and no LICENSE file appears in the inspected tree. Do not reuse the report's specifications, data or assets outside study without permission.

## 4. Creator-described contents

The README identifies:
- A Deneb donut chart with a taxonomy-style treatment, tooltips and drillthrough.
- A Deneb horizontal bar with a dynamic marker.
- Report-page tooltip functionality.
- Drillthrough navigation.
- A tolerance-zone spectrum bar.
- Five named report pages.
- Deneb visuals with AI-generated specifications.
- A synthetic flavour-based dataset.

The creator describes the Taxonomy page as a Deneb donut visual overlaid with an AI-generated visual. The README does not explain the overlay's exact visual construction, layering, or data mapping.

## 5. Evidence classification

| Claim | Evidence | Status |
|---|---|---|
| Five named report pages | Creator README | Verified as a README claim; page count not checked in PBIX |
| Taxonomy-style Deneb donut | Creator README | Described; visual not opened |
| Donut tooltip and drillthrough | Creator README | Described; not tested |
| Horizontal bar with dynamic marker | Creator README | Described; marker logic unknown |
| Tolerance-zone spectrum bar | Creator README | Described; thresholds and encoding unknown |
| Report-page tooltip | Creator README | Described; target page and fields unknown |
| AI-generated specifications | Creator README | Creator-reported; prompts and generated JSON not supplied |
| Synthetic flavour-based data | Creator README | Creator-reported; workbook not inspected |
| Deneb version inside PBIX | Not supplied | Unknown |
| Actual DAX/model and visual specifications | PBIX binary not inspected | Unknown |

## 6. Technical interpretation

The report is useful as a set of focused Deneb use cases:
- A specialised categorical composition visual.
- A bar visual with a reference marker that can move with data or a selected parameter.
- A spectrum-style bar for positioning a value against tolerance zones.
- Power BI tooltip and drillthrough integration.

These are candidate techniques, not verified implementations. The README does not disclose whether the dynamic marker is a DAX measure, a separate data row, a Vega-Lite rule layer, or another construction.

## 7. Current Deneb context

The official release index identifies Deneb 2.0.1, released on 2026-10-18, as the latest listed release at the time of this study. The 2.0 release introduced field-parameter support, configurable supporting fields, continuous view data patching, a rewritten parsing/rendering pipeline, compiled-Vega inspection, Canvas scaling to report zoom and improved context-menu controls. Version 2.0.1 lists bug fixes for enter-encoded Vega sizing, date handling and cross-highlight status.

These are current product capabilities, not features confirmed in the 2025 reference PBIX. Check the installed visual version before following version-specific instructions.

## 8. Benchmark decision

No numerical score is assigned. There are no report screenshots in the inspected repository tree and the PBIX has not been opened. Aesthetic quality, page composition, readability, accessibility, performance and runtime functionality cannot be scored from the README alone.

## 9. Sources

- [Creator repository and README](https://github.com/BruntBroccoli/Deneb-Power-BI-Example)
- [Official Deneb documentation](https://deneb.guide/)
- [Deneb change log](https://deneb.guide/docs/changelog)
- [Deneb release index](https://github.com/deneb-viz/deneb/releases)
