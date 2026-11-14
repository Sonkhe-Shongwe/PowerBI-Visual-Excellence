# Technical Notes

## 1. Reference implementation claims

The creator README describes a Deneb donut, a horizontal bar with a dynamic marker, a report-page tooltip, drillthrough navigation and a tolerance-zone spectrum bar. It says the visuals use Deneb with AI-generated specifications.

The PBIX's actual JSON specifications, data roles, DAX, model, custom visual version and settings have not been inspected. The implementation mechanisms below are official Deneb product behaviour and technical guidance, not claims about the exact construction in this example.

## 2. Deneb data pipeline

1. The report author adds columns and measures to Deneb's Values data role.
2. Power BI generates the query using the current filter context and supplies the resulting rows to Deneb.
3. Deneb exposes the supplied data as an internal dataset named `dataset`.
4. The Vega or Vega-Lite specification references that dataset and maps its fields to visual encodings.
5. Deneb renders the specification inside the Power BI visual and integrates eligible interactions with Power BI.

The specification must reference `data: { "name": "dataset" }` (or the equivalent named dataset entry). Field references use the display names in the Values data role. The dataset grain depends on the combination of unique values across the columns and measures supplied. Only fields needed by the visual should be added.

Official reference: [Dataset](https://deneb.guide/docs/dataset) and [Interactivity overview](https://deneb.guide/docs/interactivity-overview).

## 3. Power BI interaction integration

### Tooltips

A Vega-Lite mark can use a tooltip property, with Deneb's Power BI tooltip handler enabled. Default tooltips can be built from the datum's values. Report-page tooltips require Deneb to resolve the mark back to its original Power BI row context.

Transforms that aggregate or mutate the original row context can prevent report-page tooltip resolution. A default tooltip may still work because it can display key/value data without resolving the original row.

Official reference: [Tooltips](https://deneb.guide/docs/interactivity-tooltips).

### Drillthrough and context menu

The Power BI context menu can be displayed on right-click. When data-point resolution is enabled and a mark represents a resolvable original row, Deneb can delegate row context to Power BI for data-specific actions such as drillthrough.

The context menu only accepts a single datum/row. If a mark aggregates multiple source rows, the original row context may not be resolvable for data-specific menu actions.

Official reference: [Context menu](https://deneb.guide/docs/interactivity-context-menu).

### Cross-filtering

Cross-filtering from Deneb marks is disabled by default. When enabled, Deneb exposes a `__selected__` field to indicate selection state. The specification author must decide how selected and unselected marks should look, for example by changing opacity or colour. Selection is only reliable when a mark can be reconciled with the original dataset.

The documented data-point limit defaults to 50 and is configurable from 1 to 250. Large selections can increase Power BI's state-management workload.

Official reference: [Cross-filtering](https://deneb.guide/docs/interactivity-selection).

## 4. Performance and rendering

- SVG is the default renderer and generally provides crisp vector output.
- Large numbers of SVG marks can reduce performance.
- Canvas can be better for high mark counts, but can look softer at high zoom. Deneb 2.0 added Canvas scaling to report zoom.
- Reduce the number of fields and measures supplied to the visual.
- Use aggregation, binning or line marks where appropriate to reduce on-screen mark count.
- Applying changes manually can be faster than recompiling a complex specification on every keystroke.
- Deneb 2.0 continuous view can patch eligible dataset updates into the existing Vega view instead of recompiling. It is off by default. The default row threshold is 500, configurable up to 5,000, and the specification must be compatible. Complex/wide datasets can still be expensive, so test realistic filter changes.

Official reference: [Performance considerations](https://deneb.guide/docs/performance) and [Change log](https://deneb.guide/docs/changelog).

## 5. Deneb version context

The official release index identifies Deneb 2.0.1, released 2026-10-18, as the latest listed release at the time of this study. The 2.0 release introduced:
- Field-parameter support and parameter consolidation.
- Per-field supporting-field configuration.
- Continuous view/data patching for eligible datasets.
- A rewritten parsing and rendering pipeline.
- Viewing and converting compiled Vega from Vega-Lite.
- Canvas scaling to report zoom.
- Improved context-menu controls and debug-pane inspection.

Version 2.0.1 includes fixes related to enter-encoded Vega sizing, date display in debug/tooltips, and cross-highlight status. The release notes say 2.0.1 passed certification and was undergoing deployment to reports. Verify the actual installed version in Desktop.

The reference repository dates from July 2025. Its embedded Deneb version is unknown; do not attribute 2.0 features to the sample without inspection.

## 6. Security and distribution

The Deneb AppSource edition is Microsoft-certified and runs in the Power BI custom visual sandbox. The certified build cannot fetch external resources such as remote images or external datasets. The standalone build can enable remote resources, but it is not certified and requires manual updates. Use the AppSource edition for normal governed work unless there is a clear, approved reason for a different build.

Official references: [Getting started](https://deneb.guide/docs/getting-started), [Enterprise and security FAQ](https://deneb.guide/enterprise), and [Deneb releases](https://github.com/deneb-viz/deneb/releases).

## 7. AI-generated specification caution

The creator says the report's specifications were AI-generated. This is a statement about the author's workflow, not evidence that the specifications are correct, maintainable, secure or performant.

Any AI-generated specification should be reviewed for:
- Correct field names and types.
- Correct aggregation and grain.
- Scale domains, units and sorting.
- Missing, blank and zero values.
- Tooltip and drillthrough row-context preservation.
- Filter and cross-filter state.
- Responsiveness, accessibility and rendering cost.
- Reproducibility and clear comments.

## 8. Source and licence boundary

The public repository contains no LICENSE file and its metadata does not declare a licence. The Deneb visual itself is MIT-licensed, but that does not grant rights to the example author's PBIX, workbook, specifications or report assets. Treat the example as study-only unless the creator grants permission.

## 9. Runtime validation still required

Use [DESKTOP_VALIDATION.md](DESKTOP_VALIDATION.md) before calling any of the report's features tested.
