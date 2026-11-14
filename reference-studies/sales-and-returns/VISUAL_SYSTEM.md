# Visual System

## Evidence basis

This is a partial visual review based on the Microsoft Learn screenshot and the page descriptions in the Microsoft Fabric Community tour. The PBIX has not been opened. The screenshot is evidence of one Returns-page state, not a complete report-wide visual audit.

Screenshot source: [Microsoft Learn Sales and Returns sample image](https://learn.microsoft.com/ja-jp/power-bi/create-reports/media/sample-datasets/sales-returns-sample-pbix.png)

## Observed visual characteristics

The published Returns-page screenshot shows:

- A dark navy application/report header across the top.
- A light report canvas with distinct visual panels.
- Blue-toned feature bars for Key Influencers and Decomposition Tree.
- A horizontal Store Breakdown bar chart with red bars for the return-focused metric.
- A time-series visual to the right, using multiple lines to compare stores over time.
- Visible controls for switching between Visual, Tabular, and Map views.
- Report-page navigation and tooltip-related tabs visible along the lower edge of the captured Desktop window.

These are observations from one screenshot. Exact colour values, font families, font sizes, margins, panel dimensions, and page canvas dimensions have not been verified.

## Documented component language

| Component | Documented treatment | Evidence limitation |
|---|---|---|
| KPI cards | Two prominent cards for Net Sales and Units Sold | Exact card style and values not inspected |
| Category Breakdown | Visual with a bookmark-driven tabular alternative | Full chart type and formatting not inspected |
| Store Breakdown | Visual with a bookmark-driven map alternative | Full chart type and map layout not inspected |
| Q&A | Included as a report exploration visual | Runtime behaviour not tested |
| Report-page tooltip | Appears on hover over a product category bar | Tooltip page and visual design not inspected |
| Key Influencers and Decomposition Tree | Accessed through buttons | Button states and view layouts not inspected |
| Market Basket Analysis | Custom cluster-map visual with selected-product context | Exact visual encoding and package not inspected |
| Return Rate scenario | Forecast and Extra Profit views | Full visual configuration not inspected |

## Critical visual assessment

The report appears to prioritise functional grouping and guided exploration. The repeated Net Sales and Returns structure gives the reader a consistent mental model. The visible alternate-view controls also make it possible to offer different representations without placing every representation on the page at once.

The screenshot uses a recognisable dark header, light content surfaces, and strong accent colours. That is enough to identify a broad visual direction, but not enough to extract a production colour palette or typography system.

The PBIX name identifies the file as v201912. It should therefore be treated as a legacy interaction reference, not as a definitive example of current Power BI visual styling. The 2026 AdventureWorks sample and more recent championship studies remain stronger candidates for modern visual-system comparison.

## Accessibility and responsive design

The creator article says the report considers accessibility and cross-platform use and that Net Sales and Returns were designed for mobile. These are design intentions reported by the source, not independently verified outcomes.

No contrast ratios, screen-reader descriptions, tab order, keyboard sequence, or phone layout were tested. A full review must be completed in Power BI Desktop before making an accessibility or responsive-design judgement.

## Do not infer

- Do not assign exact hex values from the screenshot.
- Do not identify a font family without inspecting the PBIX or a reliable source.
- Do not infer the full canvas size from a cropped screenshot.
- Do not conclude that the report passes accessibility standards because accessibility is mentioned in the article.
- Do not treat the visual style as a reusable theme until it is independently inspected and tested.
