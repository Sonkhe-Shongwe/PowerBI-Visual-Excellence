# Technical Notes

## Semantic model

The model describes Sales as one row per order line. The relationship inventory is seven active and two inactive relationships.

| From | To | Cardinality | State and filter behaviour |
|---|---|---|---|
| Sales | Customer, Product, Reseller, Sales Territory | Many-to-one each | Active, single direction |
| Sales Order | Sales | One-to-one on SalesOrderLineKey | Active, both directions |
| Sales.OrderDateKey | Date.DateKey | Many-to-one | Active, single direction |
| Sales.DueDateKey and Sales.ShipDateKey | Date.DateKey | Many-to-one each | Inactive, single direction |
| Product.Category | Category.Category | Many-to-one | Active, single direction |

The Date table is categorised as Time. Date is the key-marked calendar column and DateKey is a hidden relationship key. The model exposes hierarchies for customer geography, fiscal dates, products, reseller geography, sales orders and sales territories. Sales contains hidden base columns and exposes measures through Core, Date Role and Time Intelligence folders.

## Measures and calculation groups

The twenty explicit measures include Sales and Cost aggregations, Profit as Sales less Cost, Profit % as Profit divided by Sales, and Orders as a distinct count of sales order identifiers. The Customers % calculation divides the current customer count by a customer count evaluated with ALLSELECTED. The visual definitions use Profit Margin % as a query alias for the Profit % measure.

Date Role has precedence 200 and three items. By Order Date returns the selected measure through the active relationship. By Due Date and By Ship Date use USERELATIONSHIP to evaluate through their respective inactive date relationship. The Date Role slicer has a saved By Order Date selection.

Time Intelligence has precedence 100 and ten items: Current, MTD, QTD, YTD, PY, PY MTD, PY QTD, PY YTD, YoY and YoY %. It applies period logic to the selected measure. The YoY % calculation has a percentage format string. Verify combinations of period and date role in Desktop before copying the implementation.

## Power Query and report behaviour

Seven saved M queries read named tables from the same workbook via a local file path and apply column types. Category is built from an inline compressed JSON table and typed in M. Opening the report can use its embedded model. Refresh from the original local workbook path has not been tested.

The date slicer binds Date.Date in RelativeDatePicker mode and has a visual filter that excludes blank Orders. The matrix has a visual-level exclusion for the reseller business type value [Not Applicable]. The Azure Maps tooltip has a saved sentence template with count and share placeholders. Cross-filtering, geocoding and date mode outcomes require runtime checks.

The [Desktop validation register](DESKTOP_VALIDATION.md#expected-values) records independently reconciled order counts and sales values for each date role. It also documents the embedded calendar range and missing ship-date rows.

Sources: [Pinned PBIX](README.md#source) and [PBIXRay](https://github.com/Hugoberry/pbixray).
