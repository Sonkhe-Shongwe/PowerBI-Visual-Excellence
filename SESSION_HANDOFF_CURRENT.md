# Current Session Handoff

**Last updated:** 2026-11-13  
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
- The reference catalogue contains eleven candidates, including six high-priority references. P1 is complete.
- The source-led REF-001 study of The World of Peaches is documented in five study files.
- The source-led REF-002 study of City Sustainability Scorecard is documented in five study files.
- The description-led REF-003 study of AstraVale SQL Health is documented in five study files.
- The description-led REF-006 study of OECD Global Well-being is documented in five study files.
- The screenshot- and walkthrough-led REF-009 study of Power BI Basketball Cards is documented in five study files.
- The official screenshot and creator walkthrough show a native-visual player card and shot-chart interaction; PBIX/source access remains unconfirmed.
- The source-level REF-011 Deneb Template Showcase study is documented in six study files. Its MIT-licensed repository contains 21 Vega/Vega-Lite templates, sample data, previews, a custom theme and a 22-page PBIP showcase.
- The description- and screenshot-led REF-007 Europe in Motion study is documented in five study files. The creator describes four pages and confirms HTML Content KPI cards and HTML/CSS animated overlays; the employer says the winning report included a colour-blindness simulator. PBIX/source access remains unconfirmed.
- The OECD creator post includes a Power BI embed token, but the live report could not be rendered and no separate PBIX/source repository was confirmed.
- The public AstraVale Power BI URL has been identified but could not be rendered in the available browsing interface; no PBIX/source repository has been confirmed.
- The World of Peaches and City Sustainability Scorecard PBIX files have not yet been opened and tested in Power BI Desktop; runtime interactions and accessibility remain unverified.
- P2 now contains five documented studies: two source-level, two description-led and one screenshot/walkthrough-led.
- P2 progress is 45%; overall weighted progress is approximately 26%.
- P1 is complete: ten references are recorded and five high-priority study candidates are selected.
- Overall weighted progress is 24%: P1 complete (15 weighted points) plus P2 at 35% (8.75 weighted points), rounded from 23.75%.
- Current phase is P2. The next reference to investigate is REF-008 SQL Radar.
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

The 2025 Week 3 winner uses native Power BI visuals for a flippable player card, navigation and a shot-location view. PBIX availability has not been confirmed.

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

Begin REF-008 SQL Radar as the next operational-monitoring study. Verify the reported PBIX attachment, inspect the source page and any screenshots, and map the report's operational KPI, alert and investigation flow. Confirm file and licence availability before claiming source-level access.

Do not recreate the report. Continue recording transferable lessons only.

## Required end-of-session updates

- Update PROJECT_STATUS.md.
- Update this handoff.
- Update the reference catalogue and relevant study notes.
- Add a concise entry to the changelog.
- Record extracted principles in the design-system or techniques library.
- If a personal project is changed, commit that implementation in its own repository.
- Identify the next learning action and any user-side dependency.
