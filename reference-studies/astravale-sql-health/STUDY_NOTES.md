# REF-003 — AstraVale SQL Health: Study Notes

**Creator:** Marius Helle  
**Original source:** https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/world-champion-winner---live-finale-build---astravale-sql-health-report-by-mariu/5373203  
**Public Power BI report:** https://app.powerbi.com/view?r=eyJrIjoiNjNhYzU4MDEtZDc3ZS00MTQ5LTk1YmEtODE2MjZkODkzOTk5IiwidCI6ImI2ZGEwOTc1LTEwY2EtNDE0ZS04YTZjLTE1ZjgzMzgxZGUzMiJ9  
**Study date:** 2026-11-13  
**Status:** Description-led study; live report and source inspection pending

## Executive finding

AstraVale SQL Health is an operational monitoring report that guides the reader from a broad system overview to a prioritised remediation plan.

The creator describes five pages: Overview, Problems, Causes, Connections and Action. Each page narrows the investigation:
- Identify systems that need attention.
- Separate new problems from existing problems.
- Investigate likely causes.
- Test whether related systems share the same pattern.
- Prioritise fixes and examine what happens if nothing is done.

This is a strong example of decision-oriented dashboard storytelling. The report is not merely a collection of SQL performance metrics. It is designed around the sequence of decisions an operator needs to make.

## 1. Competition and report context

The creator's community post identifies AstraVale SQL Health as the 2026 Power BI DataViz World Championship finale-winning report at FabCon Barcelona.

A supporting company post says the final challenge involved building a report live in 20 minutes and presenting it in three minutes. It describes the main difficulty as translating a highly technical SQL monitoring dataset into something judges and an audience could understand quickly.

This context is relevant to the report's emphasis on narrative and visual communication, but it does not tell us how the report was originally developed outside the live final.

## 2. Dataset described by the creator

The report uses hourly monitoring data from:
- 10 SQL databases.
- 7 Azure sites.
- 1 August to 16 September 2026.
- 8 monitoring metrics, including CPU, memory, disk load and blocked sessions.

The dataset also includes:
- Warning and critical limits for each metric.
- Equipment value dependent on each database.
- Shared site relationships.
- Shared data-feed relationships.
- Results from regular health checks.

The inclusion of equipment value and dependency information is important. It allows the report to consider operational impact and connected risk, not just raw metric severity.

## 3. Evidence inspected

| Evidence | What it supports | Confidence |
|---|---|---|
| Creator's Microsoft Fabric Community post | Five-page sequence, purpose, controls, dataset and analytical views | High |
| Employer's public post | Public Power BI report URL and championship context | High |
| Public championship context | Finale winner status and competition setting | High |
| Public thumbnail reference | A 308 KB thumbnail is listed on the community post | Low for full visual assessment |
| Live Power BI report | URL identified but not rendered/interacted with in this environment | Not assessed |
| PBIX/source repository | No downloadable PBIX or source repository confirmed from the inspected post | Not assessed |

### Evidence boundary

The page descriptions are source-derived. The following have not been verified:
- Exact page dimensions and visual coordinates.
- Theme, colours, typography and spacing.
- Exact chart types beyond the creator's descriptions of maps, tables, heatmaps and trend views.
- DAX, Power Query, semantic model and relationships.
- Whether controls use bookmarks, field parameters, slicers or another mechanism.
- Runtime interactions, performance, accessibility and Power BI Service behaviour.

Do not fill these gaps with assumptions.

## 4. The decision journey

### Overview — Which systems need attention?

The creator describes a map and a table of all systems, coloured by status, with equipment value and alarms. Buttons filter the view to all systems, systems getting worse, or systems that are steady.

This page establishes the initial situation and helps the operator decide where to start.

### Problems — What changed?

Each system is compared with its own August baseline. The page separates new problems from older ones.

The creator describes three alternative views:
- Where to start: equipment value compared with rising metrics.
- Recent changes: a heatmap covering every metric.
- Where alarms come from: alarm hours by metric.

This is more informative than showing only whether a metric has crossed a static warning threshold.

### Causes — Why is it happening?

The creator describes three analytical views:
- Memory usage across an average day.
- Comparison of self-hosted servers with Azure SQL.
- A chain showing how strain builds from CPU to blocked sessions and deadlocks.

The purpose is to move from symptom detection toward a plausible technical explanation.

### Connections — Could related systems also be affected?

The page follows disk load day by day for worsening systems and compares it with each system's August baseline.

Buttons test two possible relationships:
- Systems at the same site.
- Systems using the same data feed.

This introduces dependency analysis into the operational investigation.

### Action — What should happen first?

The page turns the analysis into a plan. The creator describes:
- A view of what happens if nothing is done.
- A slider that moves the scenario forward in time.
- A ranked list of fixes.
- A slider that shifts priority between the most urgent issue and the action that protects the most equipment.

This makes the dashboard a decision-support tool rather than only a monitoring display.

## 5. Critical evaluation

### Strong design and analytical ideas

- Each page answers a distinct operational question.
- The sequence moves from detection to diagnosis and then action.
- Baseline comparisons help distinguish new deterioration from old or persistent issues.
- Equipment value adds business impact to technical severity.
- Shared site and data-feed relationships help reveal correlated risk.
- The final page converts analysis into a prioritised response.
- The dataset contains thresholds, history, dependencies and assessment results, enabling more than a simple KPI dashboard.

### Questions and trade-offs

- A five-stage investigation may be powerful for technical operators but could be too complex for an executive audience without a concise summary layer.
- The report needs clear definitions for warning, critical, worsening and steady states.
- Equipment value is one impact dimension; operational criticality, service impact and recovery effort may also matter. The available description does not establish how these are weighted.
- Baseline selection is important. August is the reference period, but we have not inspected how the report handles seasonality or unusual baseline conditions.
- The priority slider needs a transparent explanation so users understand what is being traded off.
- Without live inspection, visual density, hierarchy, chart readability and accessibility cannot be judged.

## 6. Benchmark status

**No numerical benchmark score assigned.**

The available evidence is sufficient to study the report's narrative and analytical architecture, but not enough to score its visual system or technical implementation.

## 7. Next action

Inspect the public Power BI report when a compatible browser can render it. Record actual screenshots, page dimensions, visual types, layout, theme, navigation, filters, sliders and accessibility. Keep those observations separate from the current creator-described findings.
