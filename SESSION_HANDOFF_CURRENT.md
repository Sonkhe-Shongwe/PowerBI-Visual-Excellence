# Current Session Handoff

**Last updated:** 2026-11-14  
**Project:** Power BI Visual Excellence  
**Repository:** https://github.com/Sonkhe-Shongwe/PowerBI-Visual-Excellence  
**Branch:** main

## Mission

This is a **learning, research and design-reference workspace**. We study exceptional Power BI reports to understand their structure, visual design, information architecture, reusable components and technical implementation. We extract transferable principles and use them to improve the user's own personal projects.

External dashboards are case studies, not the deliverables to recreate. The user's personal projects remain separate and keep their own repositories, goals and implementation history.

This project is about Power BI, not PilotODIN.

## Decisions confirmed

- GitHub is the durable source of truth for reference research, study notes, design principles and technique documentation.
- The repository is not intended to become a collection of cloned external dashboards.
- The main learning targets are report structure, page architecture, visual hierarchy, composition, typography, colour, chart design, interactions, reusable components and technical implementation.
- Research findings should be distilled into transferable patterns, not copied blindly.
- The user's personal projects are the actual implementation destinations.
- Personal project source files and deliverables remain in their own repositories.
- The user chooses which personal project to work on and which lessons to apply.
- Small isolated proof-of-concepts are allowed only when needed to understand a specific technique.
- Do not claim a report or technique has been inspected or tested until evidence exists.
- Respect source licences and creator attribution.

## Current state

- Repository existence, public visibility, default branch and write permissions were verified.
- Foundation documentation, roadmap, research catalogue, audit template and QA guidance have been committed.
- The reference catalogue contains eleven candidates, including seven high-priority references. P1 is complete.
- The source-led REF-001 study of The World of Peaches is documented in five study files.
- The source-led REF-002 study of City Sustainability Scorecard is documented in five study files.
- The description-led REF-003 study of AstraVale SQL Health is documented in five study files.
- The description-led REF-006 study of OECD Global Well-being is documented in five study files.
- The screenshot- and walkthrough-led REF-009 study of Power BI Basketball Cards is documented in five study files.
- The official screenshot and creator walkthrough show a native-visual player card and shot-chart interaction; PBIX/source access remains unconfirmed.
- The source-level REF-011 Deneb Template Showcase study is documented in six study files. Its MIT-licensed repository contains 21 Vega/Vega-Lite templates, sample data, previews, a custom theme and a 22-page PBIP showcase.
- The description- and screenshot-led REF-007 Europe in Motion study is documented in five study files. The creator describes four pages and confirms HTML Content KPI cards and HTML/CSS animated overlays; the employer says the winning report included a colour-blindness simulator. PBIX/source access remains unconfirmed.
- The description-led REF-008 SQL Radar study is documented in five study files. Its community page lists a 903 KB PBIX attachment and a 2.1 MB screenshot; the PBIX has not been downloaded or inspected.
- The description-led REF-005 Sales and Returns study is documented in five study files. Microsoft documents five main pages and interactions including bookmarks, tooltips, drillthrough, What-if analysis, custom visuals, Power Apps and mobile layout. The official 6.23 MB PBIX listing is verified but the binary has not been opened or source-inspected.
- The description-led REF-010 Deneb Power BI Example study is documented in six study files plus a Desktop validation register. The creator README names five pages and describes a taxonomy donut, dynamic-marker bar, report-page tooltip, drillthrough and tolerance-zone spectrum. The 4.53 MB PBIX is present but its internal specs have not been inspected; the repository has no declared licence or LICENSE file. The README's Spicy_Data.csv reference does not match the Spicy_Data.xlsx file in the repository tree.
- The OECD creator post includes a Power BI embed token, but the live report could not be rendered and no separate PBIX/source repository was confirmed.
- The public AstraVale Power BI URL has been identified but could not be rendered in the available browsing interface; no PBIX/source repository has been confirmed.
- The World of Peaches and City Sustainability Scorecard PBIX files have not yet been opened and tested in Power BI Desktop; runtime interactions and accessibility remain unverified.
- P2 now contains ten documented studies: three source-level, six description-led and one screenshot/walkthrough-led.
- P2 progress is 60%; overall weighted progress is 30%.
- REF-004 AdventureWorks Sales (2026 refresh) has a documented source audit covering its single Overview page, SoftDark theme, phone placements, ten model tables and two calculation groups. Power BI Desktop validation remains pending.
- No full dashboard recreation has been started.
- No personal project has been modified.

## Research facts to preserve

### The World of Peaches

Source: https://github.com/gusbavia/the-world-of-peaches

The public repository README describes this as the 2026 Power BI World Championship winning report. It lists a PBIX, 45 DAX measures, 17 HTML/CSS component templates, TMDL semantic-model source, report layout/bookmarks and a theme JSON. The repository declares an MIT licence.

### City Sustainability Scorecard

Source: https://github.com/gusbavia/city-sustainability-scorecard

The public repository declares an MIT licence and lists the full PBIX, 223 DAX measures in 14 folders, 74 HTML templates, 29 CSS files and TMDL model source. The current source tree contains six 1280 × 720 sections, 72 bookmark JSON definitions and one HTML Content custom visual package. The report's data is illustrative and embedded. The portfolio summary describes four analytical pages, while the PBIX source also includes a 10 Year Overview section.

### AstraVale SQL Health

Source: https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/world-champion-winner---live-finale-build---astravale-sql-health-report-by-mariu/5373203

Public Power BI report: https://app.powerbi.com/view?r=eyJrIjoiNjNhYzU4MDEtZDc3ZS00MTQ5LTk1YmEtODE2MjZkODkzOTk5IiwidCI6ImI2ZGEwOTc1LTEwY2EtNDE0ZS04YTZjLTE1ZjgzMzgxZGUzMiJ9

The creator describes five stages: Overview, Problems, Causes, Connections and Action. The dataset covers 10 Azure SQL databases across 7 sites, eight metrics, warning/critical thresholds, equipment value, shared dependencies and health-check results. The public report URL could not be rendered in the available browsing interface; no PBIX/source repository has been confirmed.

Study files: STUDY_NOTES.md, PAGE_ARCHITECTURE.md, VISUAL_SYSTEM.md, TECHNICAL_NOTES.md and TRANSFERABLE_PATTERNS.md under reference-studies/astravale-sql-health/.

### OECD Global Well-being

Source: https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/winning-report---world-champion---oecd-global-well-being/4643676

Official winner announcement: https://community.fabric.microsoft.com/blog/fbc_pbiupdatesblog/the-first-power-bi-dataviz-world-champion---jon-sandmann/5174221

The creator describes three domains with three measures each, dynamic SVG progress bars, trends with anomaly detection, country cross-filtering, domain-specific styling and a second gender-disparity page using small multiples. The post includes a Power BI embed token, but no PBIX/source repository was confirmed and the live report was not rendered.

Study files: STUDY_NOTES.md, PAGE_ARCHITECTURE.md, VISUAL_SYSTEM.md, TECHNICAL_NOTES.md and TRANSFERABLE_PATTERNS.md under reference-studies/oecd-global-wellbeing/.

### Power BI Basketball Cards

Source: https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/winner-of-week-3--power-bi-basketball-cards/4600448

Creator walkthrough: https://www.linkedin.com/posts/injae-park_powerbi-dashboarddesign-sportsanalytics-activity-7345811931527589888-DF7M

The creator says the report uses core Power BI visuals only. The walkthrough describes a button/list slicer, two card measures for front/back content, layout visibility to show one side at a time, and a scatter plot layered over a half-court image using X/Y shot coordinates. The published screenshot shows a player list, player card, KPI comparisons and shot chart. No PBIX download was confirmed.

Study files: STUDY_NOTES.md, PAGE_ARCHITECTURE.md, VISUAL_SYSTEM.md, TECHNICAL_NOTES.md and TRANSFERABLE_PATTERNS.md under reference-studies/powerbi-basketball-cards/.

### Europe in Motion

Source: https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/europe-in-motion-a-dynamic-portrait-of-how-regions-balance-social-and-environmen/4800387

Winner announcement: https://www.linkedin.com/posts/infosys-americas_our-colleague-paulo-grij%C3%B3-business-intelligence-activity-7389020198965788672-b9F9

The creator describes four pages: Overview, Reading Between the Regions, Contrasts and Head-to-Head: Countries. He confirms HTML Content for KPI cards and HTML/CSS animated overlays. The employer says the winning presentation included a colour-blindness simulator. No downloadable PBIX or source repository was confirmed.

Study files: STUDY_NOTES.md, PAGE_ARCHITECTURE.md, VISUAL_SYSTEM.md, TECHNICAL_NOTES.md and TRANSFERABLE_PATTERNS.md under reference-studies/europe-in-motion/.

### Deneb Power BI Example

Source: https://github.com/BruntBroccoli/Deneb-Power-BI-Example

The repository tree contains Deneb-Dashboard.pbix (4,533,410 bytes), README.md and Spicy_Data.xlsx (11,956 bytes). The README describes a taxonomy-style Deneb donut with tooltips and drillthrough, a horizontal bar with a dynamic marker, report-page tooltip functionality, a tolerance-zone spectrum bar, and five pages: How This Dashboard Works, Taxonomy, Drillthrough, Tooltip Page and Tolerance Zones. The README refers to Spicy_Data.csv, which does not match the XLSX file in the tree. The creator says the specs are AI-generated and the data is synthetic. No LICENSE file or declared repository licence was found. The PBIX internals and embedded Deneb version remain unknown.

Official Deneb context: the release index lists version 2.0.1 (2026-10-18). Version 2.0 adds field-parameter support, continuous view data patching for eligible datasets, compiled-Vega inspection, and rendering/debug improvements. These are current product features, not verified features of the 2025 sample.

Study files: README.md, STUDY_NOTES.md, PAGE_ARCHITECTURE.md, VISUAL_SYSTEM.md, TECHNICAL_NOTES.md, TRANSFERABLE_PATTERNS.md and DESKTOP_VALIDATION.md under reference-studies/deneb-power-bi-example/.

### Deneb Template Showcase

Source: https://github.com/InsightfulAnalytics/Deneb

Licence: MIT.

The repository contains 21 Vega/Vega-Lite templates, 21 preview PNGs, 21 sample-data CSVs, a template metadata schema, automated validation, a custom BI Nexus theme and a 22-page PBIP showcase. The main KPI Dashboard 2015 page is 1600 × 900 with 12 Deneb components. The source-level study covers KPI Line Card, Bullet Chart, Calendar Heatmap, KPI Small Multiples and P&L Accounts Statement.

Study files: STUDY_NOTES.md, PAGE_ARCHITECTURE.md, VISUAL_SYSTEM.md, TECHNICAL_NOTES.md and TRANSFERABLE_PATTERNS.md under reference-studies/deneb-template-showcase/.

### Deneb Power BI Example

Source: https://github.com/BruntBroccoli/Deneb-Power-BI-Example

The public repository contains a PBIX and README describing Deneb donut and bar visuals, tooltips and drillthrough. No LICENSE file was found in the inspected repository tree.

### Microsoft samples

Official documentation: https://learn.microsoft.com/en-us/power-bi/create-reports/sample-datasets  
Official sample repository: https://github.com/microsoft/powerbi-desktop-samples

Microsoft's sample resources provide examples for studying report design and implementation. Each sample's own licensing and attribution conditions must be checked before reuse.

### Sales and Returns

Microsoft Learn: https://learn.microsoft.com/en-us/power-bi/create-reports/sample-sales-returns  
Creator tour: https://community.fabric.microsoft.com/blog/fbc_pbiupdatesblog/take-a-tour-of-the-new-sales--returns-sample-report/5175940  
Official PBIX: https://github.com/microsoft/powerbi-desktop-samples/blob/main/Sample%20Reports/Sales%20%26%20Returns%20Sample%20v201912.pbix

The creator documents five main pages: Intro, Net Sales, Returns, Return Rate and Market Basket Analysis. The report demonstrates bookmark-driven alternate views, report-page tooltips, Mapbox, Q&A, Key Influencers, Decomposition Tree, AI distribution insights, drillthrough, What-if analysis, a custom cluster map, Power Apps integration and phone layout planning. The study is description-led because the PBIX has not been opened. Microsoft's sample terms separately identify the workbook and related data as obviEnce property and require the obviEnce © notice. Do not assume the repository's root MIT licence grants unrestricted rights to the sample data or assets.

Study files: README.md, STUDY_NOTES.md, PAGE_ARCHITECTURE.md, VISUAL_SYSTEM.md, TECHNICAL_NOTES.md and TRANSFERABLE_PATTERNS.md under reference-studies/sales-and-returns/.

## REF-001 source findings

- Five sections: Welcome, Overview, Production, Trade and Tabular View.
- All five sections specify a 1280 × 720 canvas; this is four analytical pages plus a Welcome/cover page.
- The model contains Peach Production and Peach Trade fact tables with shared Countries and Year dimensions.
- The report uses native Shape Map, slicers and Page Navigator elements alongside a custom HTML Content visual.
- The theme contains named visual styles, action-button presets and page navigator styles.
- Eight bookmark folders exist: Tutorial 1–4 and Close 1–4.
- The creator's public process notes describe data audit, narrative brief, design system, wireframe/data mapping, CSS/theme tokens and isolated component development.

Study files: STUDY_NOTES.md, PAGE_ARCHITECTURE.md, VISUAL_SYSTEM.md, TECHNICAL_NOTES.md and TRANSFERABLE_PATTERNS.md under reference-studies/world-of-peaches/.

## REF-002 source findings

- Six sections: Welcome, Executive Summary, Performance, Ranking, Temporal Analysis and 10 Year Overview.
- All six sections specify a 1280 × 720 canvas.
- The model contains City Metrics, City Lookup, City Slicer, Page Parameter, Parameter and _Measures tables.
- The Parameter table is a native field parameter using NAMEOF references to five measures.
- The report combines native clustered bar charts, line charts and tables with HTML Content components, including a DAX-generated SVG radar chart.
- DAX is organised into 14 folders; the repository contains 223 DAX files, 74 HTML templates, 29 CSS files and 72 bookmark definitions.
- Five analytical page roles cover executive summary, performance, ranking, temporal analysis and a 10-year historical view.
- The source includes 24 alt-text measures and tab-order settings, but live accessibility remains untested.

Study files: STUDY_NOTES.md, PAGE_ARCHITECTURE.md, VISUAL_SYSTEM.md, TECHNICAL_NOTES.md and TRANSFERABLE_PATTERNS.md under reference-studies/city-sustainability-scorecard/.

## Immediate next session

Run the [REF-004 Desktop validation register](reference-studies/microsoft-2026-samples/DESKTOP_VALIDATION.md) on Windows. Start with Overview and Model view, then reconcile Orders and Sales for the three June 2020 date roles. Expected values, a DAX Query View check and the remaining interaction, mobile, accessibility and performance tests are recorded in the register. All eight Desktop tests are pending. After that pass, open the Sales and Returns PBIX and verify the creator-described bookmark, drillthrough, What-if, custom-visual and phone-layout behaviour. Then use the [REF-010 Desktop validation register](reference-studies/deneb-power-bi-example/DESKTOP_VALIDATION.md) to inspect the actual Deneb specifications and test the custom interactions.

Do not recreate the report. Continue recording transferable lessons only.

## Required end-of-session updates

- Update PROJECT_STATUS.md.
- Update this handoff.
- Update the reference catalogue and relevant study notes.
- Add a concise entry to the changelog.
- Record extracted principles in the design-system or techniques library.
- If a personal project is changed, commit that implementation in its own repository.
- Identify the next learning action and any user-side dependency.
