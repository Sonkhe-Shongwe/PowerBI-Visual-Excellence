# Page Architecture

The saved page metadata contains a single page, **Overview**, which is the active and landing page. The 1920 × 1080 canvas uses Fit to Page. Visual labels below describe purpose and bindings. Coordinates are rounded from saved top-left positions.

| Desktop band | Visual | Primary fields | X, Y |
|---|---|---|---:|
| Filter above map | Date picker | Date | 36, 18 |
| Upper left | Azure Maps | Customer country/region, customer count and customer share | 36, 62 |
| Upper middle | Clustered bar | Sales by sales territory group and region | 811, 62 |
| Upper right | Funnel | Sales, Cost, Profit | 1397, 62 |
| Middle | Card | Products, Customers, Orders, Sales, Cost, Profit, Profit Margin % | 36, 482 |
| Lower left | Matrix | Category, Subcategory, Model and Product with Products, Profit and Profit Margin % | 36, 645 |
| Lower middle | Line chart | Orders by month name and year | 521, 645 |
| Below line chart | Advanced slicer | Date Role | 521, 982 |
| Lower right | Donut | Cost by product category | 1101, 645 |
| Far lower right | Clustered column | Profit Margin % by sales channel | 1609, 645 |

Seven separately configured line shapes sit between the three upper visuals, the card band and the four lower analytical visuals. Their saved positions suggest visual connectors. Their effect on the rendered hierarchy is pending review.

## Phone layout

The saved phone layout spans 324 units across the full-width placements. The date picker sits at the top. The KPI card becomes a 113-unit-wide stack of seven rows with the map, territory bar and channel chart to its right. The matrix, orders trend, Date Role selector, funnel and donut use the full width below, in that order. The seven line shapes have no saved mobile overrides. Phone readability and scrolling still need a rendering check.
