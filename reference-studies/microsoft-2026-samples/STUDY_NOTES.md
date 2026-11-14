# Study Notes

## Evidence

Inspected the pinned Microsoft PBIX using Python's ZIP reader for the report definitions and PBIXRay 0.15.5 for semantic-model metadata. The file matched the Git blob hash listed in the [study index](README.md). The review used saved configuration, DAX and M expressions. Rendering and live behaviour require Power BI Desktop.

| Evidence | Findings |
|---|---|
| Report definitions | One Overview page, ten analytical or filter visuals, seven line shapes, ten saved mobile placements, SoftDark theme and configured data bindings |
| Embedded model | Ten model tables, nine relationships, twenty explicit measures, two calculation groups, eight M queries |
| Microsoft Learn | Describes donut centre values and compact calendar, range and relative-date capabilities for this refresh |
| Desktop validation pending | Rendered appearance, map and filter behaviour, donut centre content, phone layout, accessibility and timings |

## Design assessment

Overview combines geography, territory sales, financial totals, order volume and product/channel profitability in one page. The seven-measure strip forms a common summary across the page, while the bottom row supports detail. The date controls occupy separate positions. Users will need to distinguish the date range above the map from the date basis below the trend.

The funnel shows Sales, Cost and Profit measures as adjacent stages. Those measures describe a financial decomposition, so a reader may need to check whether the funnel implies a conversion process. A waterfall would be an appropriate comparison in an original implementation if the intended reading is revenue less cost equals profit.

The saved map tooltip describes customer share among the selected customers. The underlying measure uses ALLSELECTED, making the current report selection part of the metric definition. Compare the tooltip with the actual filter context during Desktop validation.

Sources: [Pinned PBIX](README.md#source) and [PBIXRay](https://github.com/Hugoberry/pbixray).
