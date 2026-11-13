# Power BI Reference Catalogue

**Last updated:** 2026-11-13  
**Purpose:** Maintain a traceable list of Power BI reports worth studying.

A reference is a research candidate until it has been inspected. A public screenshot does not prove that a PBIX is downloadable; a PBIX does not prove that every external asset is reusable.

## Priority references

| ID | Reference | Category | Source access | PBIX/source status | Study priority | Audit status |
|---|---|---|---|---|---|---|
| REF-001 | The World of Peaches | Championship / editorial data storytelling | Public GitHub source repository and public screenshots | PBIX, DAX, HTML/CSS, TMDL, theme and report JSON inspected; MIT declared | High | Source study documented; runtime checks pending |
| REF-002 | City Sustainability Scorecard | Championship / executive sustainability | Public GitHub source repository and public screenshots | PBIX, DAX, HTML/CSS, TMDL, report config and model source inspected; MIT declared | High | Source study documented; runtime checks pending |
| REF-003 | AstraVale SQL Health | Championship / operational intelligence | Public Fabric Community post and public Power BI report link | Five-page description and public report URL verified; downloadable PBIX/source not confirmed | High | Description-led study documented; runtime inspection pending |
| REF-004 | Microsoft 2026 Power BI samples | Official Microsoft reference set | Official documentation and GitHub repository | Multiple PBIX files available | Medium | Candidate; sample selection pending |
| REF-005 | Sales and Returns sample | Official Microsoft interaction reference | Official Microsoft sample documentation | PBIX listed | Medium | Candidate; source audit pending |
| REF-006 | OECD Global Well-being | Championship / country comparison | Official Microsoft announcement, creator's Fabric Community entry and related Reddit discussion | Creator post includes a Power BI embed token; separate PBIX/source not confirmed | High | Description-led study documented; live/source inspection pending |
| REF-007 | Europe in Motion | Championship / accessible data storytelling | Microsoft Fabric Community entry, creator's LinkedIn post and employer winner announcement | Four-page description, landing-page screenshot, HTML/CSS KPI technique and colour-blindness simulator claim inspected; PBIX/source not confirmed | High | Description- and screenshot-led study documented; runtime pending |
| REF-008 | SQL Radar | Championship / operational monitoring | Fabric Community gallery | PBIX attachment reported on source page; verify availability | Medium | Candidate; download/licence check pending |
| REF-009 | Power BI Basketball Cards | Championship / interactive sports storytelling | Microsoft Fabric Community entry, official winner announcement, creator walkthrough and published screenshot | Core-visual approach and interaction technique documented; PBIX download not confirmed | High | Screenshot- and walkthrough-led study documented; PBIX/source inspection pending |
| REF-010 | Deneb Power BI Example | Technical reference / custom visual engineering | Public GitHub repository | PBIX available (about 4.53 MB); README describes Deneb examples; no LICENSE file found | Medium | Candidate; source review pending |
| REF-011 | Deneb Template Showcase | Technical reference / reusable Deneb component library | Public GitHub repository and PBIP source | MIT; 21 specs, 21 previews, 21 sample datasets, 22-page PBIP showcase, custom theme and validation script | High | Source-level technical study documented; runtime pending |

## Reference details

### REF-001 — The World of Peaches

- Creator: Gus Bavia.
- Source: https://github.com/gusbavia/the-world-of-peaches
- Repository licence: MIT (verify the current LICENSE file before reusing code or assets).
- The repository README lists a full PBIX, 45 DAX measures, 17 HTML/CSS component templates, TMDL semantic-model source, report layout/bookmarks and a theme JSON.
- Source study: five sections (Welcome plus four analytical pages), 1280 × 720 canvas, hybrid native/custom visual architecture, 45 DAX files, 17 HTML templates, 16 CSS files, TMDL model, theme JSON and eight bookmark folders.
- Potential learning areas: design-first workflow, page composition, design tokens, component development, DAX-generated HTML/SVG, guided navigation and accessibility.
- Runtime status: PBIX has not yet been opened in Power BI Desktop; interactions, service rendering and accessibility remain unverified.
- Note: exposed TMDL selector tables are DATATABLE-based selectors; native field-parameter status has not been established.
- Caution: verify any embedded media, external dependencies and data provenance separately. The repository licence does not automatically grant rights to third-party assets.

### REF-002 — City Sustainability Scorecard

- Creator: Gus Bavia.
- Source: https://github.com/gusbavia/city-sustainability-scorecard
- Repository licence: MIT (verify the current LICENSE file before reuse).
- The repository README lists a PBIX, 223 DAX measures in 14 folders, 74 HTML templates, 29 CSS files, TMDL model source, report layout/bookmarks and a theme resource. The current source tree contains 72 bookmark JSON definitions and one HTML Content custom visual package.
- The README identifies illustrative city sustainability data held in the model.
- Source study: six 1280 × 720 sections (Welcome, Executive Summary, Performance, Ranking, Temporal Analysis and 10 Year Overview), native field parameter, hybrid native/custom visual architecture, and 14 purpose-based DAX folders.
- Runtime status: PBIX has not yet been opened in Power BI Desktop; interactions, service rendering and accessibility remain unverified.
- Important discrepancy: the creator's portfolio summary describes four analytical pages, while the public PBIX source contains an additional 10 Year Overview section.
- Caution: external image/video URLs are referenced by DAX even though the analytical data is embedded. Verify third-party visual and asset terms before reuse.

### REF-003 — AstraVale SQL Health

- Creator: Marius Helle.
- Source: https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/world-champion-winner---live-finale-build---astravale-sql-health-report-by-mariu/5373203
- Public Power BI report: https://app.powerbi.com/view?r=eyJrIjoiNjNhYzU4MDEtZDc3ZS00MTQ5LTk1YmEtODE2MjZkODkzOTk5IiwidCI6ImI2ZGEwOTc1LTEwY2EtNDE0ZS04YTZjLTE1ZjgzMzgxZGUzMiJ9
- The community post identifies it as the 2026 Power BI DataViz World Championship finale winner.
- The creator describes five stages: Overview, Problems, Causes, Connections and Action.
- The described dataset covers 10 Azure SQL databases across 7 sites from 1 August to 16 September 2026, with eight metrics, warning/critical thresholds, equipment value, shared sites/data feeds and health-check results.
- Description-led study completed: the five-page decision architecture and transferable patterns are documented in reference-studies/astravale-sql-health/.
- Runtime status: the public Power BI link was identified but could not be rendered/interacted with in the available browsing interface. A downloadable PBIX and source repository were not confirmed.
- Potential learning areas: per-system baselines, deterioration detection, cause investigation, dependency analysis, equipment-value-based prioritisation and scenario planning.

### REF-004 — Microsoft 2026 Power BI samples

- Official guide: https://learn.microsoft.com/en-us/power-bi/create-reports/sample-datasets
- Official sample repository: https://github.com/microsoft/powerbi-desktop-samples
- Microsoft documents downloadable PBIX and other sample formats. Its 2026 refresh includes AdventureWorks Sales, Artificial Intelligence and Competitive Marketing Analysis.
- Potential learning areas: modern Microsoft visual defaults, dark-theme treatment, Azure Maps, card and donut styling, AI visuals, decomposition trees and anomaly detection.
- Use the individual sample's source and licence details when redistributing or adapting any files.

### REF-005 — Sales and Returns sample

- Official guide: https://learn.microsoft.com/en-us/power-bi/create-reports/sample-datasets
- The official Microsoft sample catalogue lists a downloadable PBIX and describes buttons, drillthrough, conditional formatting, what-if parameters and customised tooltips.
- Potential learning areas: report interactions and navigation patterns.
- Use the official sample catalogue to locate the current download and inspect the PBIX before scoring.

### REF-006 — OECD Global Well-being

- Creator: Jon Sandmann.
- Source: https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/winning-report---world-champion---oecd-global-well-being/4643676
- Official Microsoft winner announcement: https://community.fabric.microsoft.com/blog/fbc_pbiupdatesblog/the-first-power-bi-dataviz-world-champion---jon-sandmann/5174221
- Related Reddit discussion: https://www.reddit.com/r/PowerBI/comments/1jp3123/
- The official Microsoft announcement confirms Jon Sandmann as the 2025 Power BI DataViz World Champion.
- The creator describes three well-being domains with three measures each, dynamic SVG progress bars for global averages, yearly trends with anomaly detection, country tables, country cross-filtering, domain-specific colours/images and a second gender-disparity page using small multiples.
- Description-led study completed in reference-studies/oecd-global-wellbeing/.
- The community post includes a Power BI embed token, but the live report could not be rendered through the available browsing interface. No separate PBIX or source repository was confirmed.
- A related Reddit post describes a six-metric weighted composite with user-adjustable sliders. It is not fully cross-validated against the creator's report description and remains a related, unconfirmed detail.

### REF-007 — Europe in Motion

- Creator: Paulo Grijó.
- Source: https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/europe-in-motion-a-dynamic-portrait-of-how-regions-balance-social-and-environmen/4800387
- Creator's LinkedIn entry: https://www.linkedin.com/feed/update/urn%3Ali%3Aactivity%3A7363584628982456322/
- Employer winner announcement: https://www.linkedin.com/posts/infosys-americas_our-colleague-paulo-grij%C3%B3-business-intelligence-activity-7389020198965788672-b9F9
- The employer announcement confirms Paulo Grijó as the 2025 Power BI DataViz World Champion and says the winning solution included a colour-blindness simulator.
- The creator describes four pages: Overview, Reading Between the Regions, Contrasts and Head-to-Head: Countries.
- The creator confirms HTML Content for Overview KPI cards and HTML/CSS for animated text overlays. The report also uses a configurable scatter plot, DAX-powered country ranking and independent country filters.
- Description- and screenshot-led study completed in reference-studies/europe-in-motion/.
- PBIX/source status: the community thread contains an embed token, but no downloadable PBIX or source repository was confirmed. Full analytical-page rendering remains unverified.

### REF-008 — SQL Radar

- Community source: https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/bnc---finalist---sql-radar-%C2%B7-find-the-signal-before-the-alarm/5372173
- Candidate learning areas: operational monitoring, timeline storytelling, maps and custom visual composition.
- The community post describes a three-page Signal / Diagnosis / Action report, native visuals for data and interactions, and HTML for a zooming map, animated timelines, identity cards and an intro. A 903 KB PBIX attachment is listed on the post.
- Status: source page and attachment listing verified; download and licence still need checking.

### REF-009 — Power BI Basketball Cards

- Creator: Injae Park.
- Official contest entry: https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/winner-of-week-3--power-bi-basketball-cards/4600448
- Creator walkthrough: https://www.linkedin.com/posts/injae-park_powerbi-dashboarddesign-sportsanalytics-activity-7345811931527589888-DF7M
- Microsoft Community winner announcement: https://community.fabric.microsoft.com/blog/community_blog/%F0%9F%8F%86-power-bi-dataviz-world-championships--week-3-winner-%F0%9F%8E%89/4606956
- The report uses 2022–2023 NBA player and shot data. The creator describes a flippable player card, clean navigation and a shot-location view, built with Power BI core visuals and no custom visual add-ons.
- The creator walkthrough explains a two-state card approach using two measures in one KPI card visual, with layout visibility controlling which side is shown. It also describes overlaying a basketball-court image beneath a scatter plot using shot X/Y coordinates.
- Potential learning areas: native-only interaction design, state switching, image-backed scatter plots, player selection, visual layering and interaction-led storytelling.
- PBIX status: a community commenter asked for the PBIX, but no downloadable file was confirmed in the inspected public sources. Treat this as a screenshot- and walkthrough-led interaction study until the source file is located.
- Study documents: reference-studies/powerbi-basketball-cards/.
- Licence/reuse status: not confirmed. Do not reuse player images, logos or other assets without checking their rights.

### REF-010 — Deneb Power BI Example

- Creator: BruntBroccoli.
- Source: https://github.com/BruntBroccoli/Deneb-Power-BI-Example
- The public repository contains a 4.53 MB PBIX, a README and a synthetic data workbook.
- The README describes a Deneb donut chart with tooltips and drillthrough, a horizontal bar with a dynamic marker, report-page tooltip functionality and drillthrough navigation.
- The report has five named pages: How This Dashboard Works, Taxonomy, Drillthrough, Tooltip Page and Tolerance Zones.
- Potential learning areas: Deneb/Vega-Lite specifications, custom chart encodings, tooltips, drillthrough and when a custom visual can solve a limitation of native visuals.
- Licence status: no LICENSE file was present in the inspected repository tree. Treat the PBIX and its implementation as study-only unless reuse permission is confirmed.
- This is a focused technical reference, not yet a benchmark for overall dashboard aesthetics.

### REF-011 — Deneb Template Showcase

- Maintainer: InsightfulAnalytics / Timothy Osborn.
- Source: https://github.com/InsightfulAnalytics/Deneb
- Licence: MIT.
- The repository contains 21 reusable Vega/Vega-Lite templates, 21 preview PNGs, 21 sample-data CSV files, template READMEs, render configuration and automated validation.
- The PBIP showcase contains 22 pages: one KPI Dashboard 2015 page and one page for each template.
- The showcase uses the Fluent2-CY26SU07 base theme plus the registered BI Nexus custom theme and a registered SVG background.
- The KPI Dashboard 2015 page is 1600 × 900 and contains 12 Deneb components: four headline KPI cards and eight supporting analysis visuals.
- Source-level study completed in reference-studies/deneb-template-showcase/.
- Potential learning areas: Vega/Vega-Lite data contracts, theme-aware pbiColor/pbiFormat helpers, responsive sizing, dynamic labels, bullet charts, calendar heatmaps, KPI small multiples, P&L statements and automated visual-library validation.
- Caution: Deneb is a custom visual dependency. The author-reported P&L performance comparison has not been independently reproduced. Preserve attribution to original visual designers.

## How to add a reference

1. Assign the next REF ID.
2. Link the original creator or official source, not a copied image gallery where the original is available.
3. Record the date checked.
4. Record what is actually available: screenshot, live report, PBIX, PBIP, source code, theme, documentation.
5. Record the licence and any third-party dependencies.
6. State what can be learned and what remains unknown.
7. Do not assign a final score until the reference has been inspected using the audit template.

Related: [Benchmark scorecard](BENCHMARK_SCORECARD.md) · [Sources and licences](SOURCES_AND_LICENCES.md) · [Forensic audit template](FORENSIC_AUDIT_TEMPLATE.md)
