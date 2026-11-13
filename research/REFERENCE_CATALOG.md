# Power BI Reference Catalogue

**Last updated:** 2026-11-13  
**Purpose:** Maintain a traceable list of Power BI reports worth studying.

A reference is a research candidate until it has been inspected. A public screenshot does not prove that a PBIX is downloadable; a PBIX does not prove that every external asset is reusable.

## Priority references

| ID | Reference | Category | Source access | PBIX/source status | Audit status |
|---|---|---|---|---|---|
| REF-001 | The World of Peaches | Championship / editorial data storytelling | Public GitHub source repository and public screenshots | PBIX, DAX, HTML/CSS, TMDL, theme and report JSON inspected; MIT declared | Source study documented; runtime checks pending |
| REF-002 | City Sustainability Scorecard | Championship / executive sustainability | Public GitHub source repository | PBIX and source files listed; MIT declared | Not audited |
| REF-003 | AstraVale SQL Health | Championship / operational intelligence | Public Fabric Community post and report | Public report link; downloadable PBIX not confirmed | Not audited |
| REF-004 | Microsoft 2026 Power BI samples | Official Microsoft reference set | Official documentation and GitHub repository | Multiple PBIX files available | Not audited |
| REF-005 | Sales and Returns sample | Official Microsoft interaction reference | Official Microsoft sample documentation | PBIX listed | Not audited |
| REF-006 | OECD Global Well-being | Championship / country comparison | Fabric Community gallery | Report reference identified; source package requires verification | Candidate |
| REF-007 | Europe in Motion | Championship / accessible data storytelling | Fabric Community gallery | Report reference identified; source package requires verification | Candidate |
| REF-008 | SQL Radar | Championship / operational monitoring | Fabric Community gallery | PBIX attachment reported on source page; verify availability | Candidate |

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
- The repository README lists a PBIX, 223 DAX measures, 74 HTML components, TMDL model source, report layout/bookmarks and a theme.
- The README identifies illustrative city sustainability data held in the model.
- Potential learning areas: scoring and normalisation, reusable HTML cards/panels, radar and sparkline components, accessibility alt text, theme-level design tokens and guided navigation.
- Caution: inspect the bundled third-party visual and its own licence/terms before reusing it.

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

## How to add a reference

1. Assign the next REF ID.
2. Link the original creator or official source, not a copied image gallery where the original is available.
3. Record the date checked.
4. Record what is actually available: screenshot, live report, PBIX, PBIP, source code, theme, documentation.
5. Record the licence and any third-party dependencies.
6. State what can be learned and what remains unknown.
7. Do not assign a final score until the reference has been inspected using the audit template.

Related: [Benchmark scorecard](BENCHMARK_SCORECARD.md) · [Sources and licences](SOURCES_AND_LICENCES.md) · [Forensic audit template](FORENSIC_AUDIT_TEMPLATE.md)
