# REF-004 Desktop Validation

**Run status:** Power BI Desktop tests are pending. The comparison values and source checks below were produced from the pinned PBIX on 2026-11-14.

## Start here

1. Download the [pinned AdventureWorks Sales PBIX](README.md#source) and open it in Power BI Desktop. Record the version and capture the Overview and Model views. The PBIX contains the data required for these tests. The saved source path is relevant only if you refresh.
2. Clear chart selections. Set the date picker to 1–30 June 2020, inclusive. Cycle through **By Order Date**, **By Due Date**, and **By Ship Date**. Record the Orders and Sales cards after each change. Start with V-01 through V-03 in the register.
3. If the range control hides dates or a card abbreviates amounts, use the DAX Query View check below to separate model results from visual behaviour. Capture the UI outcome even if you can verify the model separately.

## Expected values

The reference values come from the embedded Sales, Sales Order, Date and Customer tables. Sales and Sales Order joined one-to-one on SalesOrderLineKey with 121,253 matched rows. Each populated fact date key matched the calendar. The comparison applies the date range to one role at a time and counts distinct sales order identifiers. Pandas and SQLite independently agreed on line counts, distinct order counts, Sales and Cost for the date windows.

| Date window | Date role | Order lines | Orders | Sales |
|---|---|---:|---:|---:|
| All dates, cleared | By Order Date | 121,253 | 31,455 | 109,809,274.20 |
| 1–30 June 2020 | By Order Date | 5,134 | 1,119 | 3,465,240.69 |
| 1–30 June 2020 | By Due Date | 7,736 | 1,851 | 5,226,192.07 |
| 1–30 June 2020 | By Ship Date | 4,771 | 1,111 | 3,448,904.65 |
| 15 June 2020 | By Order Date | 447 | 78 | 373,021.60 |
| 15 June 2020 | By Due Date | 366 | 71 | 266,988.53 |
| 15 June 2020 | By Ship Date | 233 | 82 | 77,455.64 |

The last populated order and ship dates are 15 June 2020, and the last due date is 25 June 2020. The calendar runs through 30 June 2021. July 2020 has zero rows for all roles, which provides a no-data test. Orders is expected to return a DAX blank in an empty filter context. The date picker has its own Orders-is-not-blank filter, so the month may be unavailable in the UI. A relative date test anchored to the current date may also return no data. Record the anchor, resolved window and result.

There are 2,113 lines with no ship date, across 513 distinct order identifiers. That order count includes any orders with at least one such line. The unfiltered Customers measure includes one key for the [Not Applicable] member. Use the rendered map and visual filters to verify whether the United States tooltip denominator includes this member. With all keys included, the embedded counts give 7,819 ÷ 18,485, or 42.30%.

Source: AdventureWorks Sales sample data, obviEnce ©. Only aggregate comparisons are recorded here. [Microsoft sample catalogue](https://learn.microsoft.com/en-us/power-bi/create-reports/sample-datasets) · [DISTINCTCOUNT](https://learn.microsoft.com/en-us/dax/distinctcount-function-dax)

## DAX Query View check

Run this read-only query in the opened sample if you need exact values. It has been prepared for Desktop. The expected values above were computed independently from the embedded rows.

```dax
EVALUATE
CALCULATETABLE(
    SUMMARIZECOLUMNS(
        'Date Role'[Date Role],
        "Orders", [Orders],
        "Sales", [Sales]
    ),
    DATESBETWEEN('Date'[Date], DATE(2020, 6, 1), DATE(2020, 6, 30))
)
ORDER BY 'Date Role'[Date Role]
```

[DAX Query View](https://learn.microsoft.com/en-us/power-bi/transform-model/dax-query-view)

## Test register

| ID | Action | Expected result or evidence to capture | Status |
|---|---|---|---|
| V-01 | Open the pinned PBIX with selections cleared | Overview renders. Capture Overview and Model view, the version, and the baseline Orders and Sales cards. Record any loading message. | Not run |
| V-02 | Select the June 2020 range and switch through the three date roles | Compare Orders and Sales with the reference values. Record which visuals respond, especially the order trend and KPI card. | Not run |
| V-03 | Select 15 June 2020 in calendar mode. Then test relative mode and clear both controls | Check the single-day order counts. Record the relative-date anchor, whether a no-data window is selectable, and the restored values after clearing the date picker and returning to By Order Date. | Not run |
| V-04 | Hover and select the United States bubble from the cleared baseline | Record customer count and share, which visuals update, and whether clearing the bubble restores the baseline. If the map does not render, capture the exact message and record the map test as blocked. | Not run |
| V-05 | Select a donut segment and clear it | Record the centre value before and after selection, visible labels and the responses of the KPI card and matrix. | Not run |
| V-06 | Open Mobile layout and inspect the full scroll | Capture the vertical KPI stack and lower detail visuals. Check title, label and matrix readability and any clipping. | Not run |
| V-07 | Tab through the desktop canvas and check representative visual descriptions | Record focus progression, labels announced by a screen reader if available, and any essential text that relies on low contrast or colour alone. Use the source checks below to select targets. | Not run |
| V-08 | In Optimize, open Performance Analyzer. Start recording, refresh visuals, then repeat a June date-role change | Record per-visual durations and their breakdown. Record machine, Desktop version, filter state, and which timings came after the initial load. | Not run |

For each run, add the date, Desktop version, test IDs, observed values, outcomes and evidence locations. If a step fails, record the actual result before retesting. [Mobile layout](https://learn.microsoft.com/en-us/power-bi/create-reports/power-bi-create-mobile-optimized-report-mobile-layout-view) · [Performance Analyzer](https://learn.microsoft.com/en-us/power-bi/create-reports/performance-analyzer) · [Azure Maps access](https://learn.microsoft.com/en-us/azure/azure-maps/power-bi-visual-manage-access)

## Source checks for the accessibility review

The ten analytical or filter visuals have saved nonnegative tab-order values. In ascending order they are Date Role, channel column, cost donut, orders line, product matrix, KPI card, funnel, territory bar, Azure Maps, and date picker. The seven line shapes have negative tab-order values. Check the actual focus path in Desktop, especially whether readers can reach the visually prominent date picker early enough. The saved visual containers have no explicit alternative-text overrides. Check what the default visual descriptions convey before deciding which need authored text.

| SoftDark token tested against #292929 | Contrast |
|---|---:|
| Main foreground #F0F0F0 | 12.77:1 |
| Secondary foreground #B8B8B8 | 7.33:1 |
| Tertiary foreground #777777 | 3.25:1 |
| Light neutral foreground #666666 | 2.53:1 |

These are calculated token-pair ratios. The 4.5:1 reference applies to normal text and 3:1 to large text. Verify the actual rendered colours, text roles and backgrounds before assessing the report against those thresholds. [W3C contrast criterion](https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum.html) · [Power BI accessibility tools](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-accessibility-creating-tools)
