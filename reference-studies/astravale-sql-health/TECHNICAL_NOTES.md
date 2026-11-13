# REF-003 — Technical Notes

**Source:** Creator's public Microsoft Fabric Community description and public Power BI report link  
**Status:** Descriptive technical analysis only; source implementation unavailable

## 1. Dataset described

The creator states that the report uses hourly monitoring data from:
- 10 Azure SQL databases.
- 7 sites.
- 1 August to 16 September 2026.
- 8 metrics, including CPU, memory, disk load and blocked sessions.

Additional data includes:
- Warning and critical thresholds for each metric.
- Equipment value dependent on each database.
- Shared site relationships.
- Shared data-feed relationships.
- Regular health-check results.

The exact column names, table grain, source systems, refresh strategy and data model are not available from the public description.

## 2. Analytical logic described

### Baseline comparison

The Problems page compares each system with its own August level. This is a system-specific baseline rather than only a single global threshold.

Potential value:
- Distinguishes newly deteriorating behaviour from persistent problems.
- Helps identify drift before a critical threshold is crossed.
- Avoids treating every database as if it has identical normal behaviour.

Unknown:
- Exact baseline calculation.
- Whether the baseline is an average, median, range or another statistic.
- How missing periods and outliers are handled.

### Multi-metric change detection

The creator describes a heatmap of every metric and a view of alarm hours by metric.

Potential value:
- Reveals patterns across metrics and time.
- Helps distinguish a short spike from a persistent problem.
- Provides a way to narrow investigation to the metrics contributing most to alarms.

Unknown:
- Heatmap encoding and colour scale.
- Aggregation window.
- Whether values are raw, normalised or expressed as deviations from baseline.

### Cause investigation

The Causes page includes:
- Memory use across an average day.
- Comparison of self-hosted and Azure SQL servers.
- A chain from CPU to blocked sessions and deadlocks.

The exact implementation and the strength of the causal evidence are not available. A report should avoid presenting correlation as causation unless the underlying analysis supports it.

### Dependency analysis

The Connections page tests whether worsening systems share:
- A physical site.
- A data feed.

The report follows disk load over time and compares it with each system's own August baseline.

### Action prioritisation

The Action page includes a no-action scenario, a forward-time slider and a ranked fix list. A second slider changes the priority balance between urgency and the amount of equipment protected.

Unknown:
- Exact prioritisation formula.
- How equipment value is weighted against urgency.
- Whether effort, downtime, recovery time or service criticality are included.
- How scenario projections are calculated.

## 3. Interaction evidence

The creator explicitly describes:
- Buttons for status groups and analytical views.
- A slider for future scenario exploration.
- A slider for action-priority weighting.

The available source does not establish whether these controls are implemented using bookmarks, field parameters, slicers, what-if parameters, calculation groups or custom visuals. Do not assume a specific Power BI mechanism.

## 4. Public report and source access

A public Power BI report URL was identified in the creator's employer's public post.

The Power BI app did not render through the available browsing interface. The Microsoft Fabric Community post lists a thumbnail but no downloadable PBIX or source repository was confirmed during this study.

No DAX, Power Query, TMDL, model relationships, theme JSON or visual configuration has been inspected.

## 5. Technical questions for a future inspection

1. What is the fact-table grain: database-hour, metric-hour or a pre-aggregated level?
2. How are warning and critical limits stored and applied?
3. How is each system's August baseline calculated?
4. How does the report classify a system as worsening or steady?
5. How are shared sites and data feeds modelled?
6. How is the CPU-to-deadlock chain represented?
7. What formula drives the urgency-versus-equipment-protection slider?
8. Are scenario calculations measures, what-if parameters or precomputed data?
9. How does the report handle missing hours and incomplete monitoring?
10. What accessibility and performance trade-offs arise from the chosen visuals?

## 6. Reuse boundary

No implementation code or visual assets are available to reuse. The current output is an analytical understanding of the described approach. Any future implementation should be independently designed and based on the user's own dataset and operational requirements.
