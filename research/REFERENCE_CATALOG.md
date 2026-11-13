# Power BI Reference Catalogue

**Last updated:** 2026-11-13  
**Purpose:** Maintain a traceable list of Power BI reports worth studying.

A reference is a research candidate until it has been inspected. A public screenshot does not prove that a PBIX is downloadable; a PBIX does not prove that every external asset is reusable.

## Priority references

| ID | Reference | Category | Source access | PBIX/source status | Study priority | Audit status |
|---|---|---|---|---|---|---|
| REF-001 | The World of Peaches | Championship / editorial data storytelling | Public GitHub source repository and public screenshots | PBIX, DAX, HTML/CSS, TMDL, theme and report JSON inspected; MIT declared | High | Source study documented; runtime checks pending |
| REF-002 | City Sustainability Scorecard | Championship / executive sustainability | Public GitHub source repository and public screenshots | PBIX, DAX, HTML/CSS, TMDL, report config and model source inspected; MIT declared | High | Source study documented; runtime checks pending |
| REF-003 | AstraVale SQL Health | Championship / operational intelligence | Public Fabric Community post and report | Public report link; downloadable PBIX not confirmed | High | Candidate; source audit pending |
| REF-004 | Microsoft 2026 Power BI samples | Official Microsoft reference set | Official documentation and GitHub repository | Multiple PBIX files available | Medium | Candidate; sample selection pending |
| REF-005 | Sales and Returns sample | Official Microsoft interaction reference | Official Microsoft sample documentation | PBIX listed | Medium | Candidate; source audit pending |
| REF-006 | OECD Global Well-being | Championship / country comparison | Fabric Community gallery and creator discussion | Report reference identified; source package requires verification | High | Candidate; source audit pending |
| REF-007 | Europe in Motion | Championship / accessible data storytelling | Fabric Community gallery | Report reference identified; source package requires verification | Medium | Candidate; source audit pending |
| REF-008 | SQL Radar | Championship / operational monitoring | Fabric Community gallery | PBIX attachment reported on source page; verify availability | Medium | Candidate; download/licence check pending |
| REF-009 | Power BI Basketball Cards | Championship / interactive sports storytelling | Microsoft Fabric Community entry and creator walkthrough | Public post/video; PBIX download not confirmed | High | Candidate; runtime/source audit pending |
| REF-010 | Deneb Power BI Example | Technical reference / custom visual engineering | Public GitHub repository | PBIX available (about 4.53 MB); README describes Deneb examples; no LICENSE file found | Medium | Candidate; source review pending |

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
- The community post identifies it as the 2026 Power BI DataViz World Championship finale winner.
- The post describes a guided sequence: overview, problems, causes, connections and recommended actions.
- Potential learning areas: operational KPI hierarchy, heatmaps, prioritisation, analytical storytelling and decision-oriented page sequencing.
- Unknowns: PBIX availability, source code, model structure, exact page dimensions and licence. Do not assume source access.

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

- Community source: https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/winning-report---world-champion---oecd-global-well-being/4643676
- The creator's post describes dynamic, colour-coordinated SVG progress bars, anomaly-detection trends, country cross-filtering, domain selection and small-multiple comparisons.
- Candidate learning areas: country comparison, dynamic SVG, domain selection and analytical storytelling.
- Status: source identified; verify report availability, author details, downloadable artefacts and reuse permissions during audit.

### REF-007 — Europe in Motion

- Community source: https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/europe-in-motion-a-dynamic-portrait-of-how-regions-balance-social-and-environmen/4800387
- The report presents regional comparisons across social and environmental dimensions. The creator's community discussion describes animated HTML/CSS content over KPI cards and use of the HTML Content visual. An employer post identifies the report as the winning entry in the 2025 Vienna final and mentions a colour-blindness simulator.
- Candidate learning areas: accessible data storytelling, dynamic KPI components, HTML/CSS and regional comparisons.
- Status: public report reference verified; downloadable PBIX has not been confirmed.

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
- PBIX status: no downloadable PBIX was confirmed in the inspected public source pages. Treat this as a visual/interaction reference until the source file is located.
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

## How to add a reference

1. Assign the next REF ID.
2. Link the original creator or official source, not a copied image gallery where the original is available.
3. Record the date checked.
4. Record what is actually available: screenshot, live report, PBIX, PBIP, source code, theme, documentation.
5. Record the licence and any third-party dependencies.
6. State what can be learned and what remains unknown.
7. Do not assign a final score until the reference has been inspected using the audit template.

Related: [Benchmark scorecard](BENCHMARK_SCORECARD.md) · [Sources and licences](SOURCES_AND_LICENCES.md) · [Forensic audit template](FORENSIC_AUDIT_TEMPLATE.md)
