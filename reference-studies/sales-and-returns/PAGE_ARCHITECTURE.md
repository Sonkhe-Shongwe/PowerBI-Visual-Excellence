# Page Architecture

## Report structure

Microsoft and the report creators describe five main pages. Additional hidden pages support tooltips and other report elements.

| Sequence | Page | Documented purpose | Main elements and interactions |
|---:|---|---|---|
| 1 | Intro | Introduce the data story and explain that the report is interactive | Download PBIX button in the Service; animated demonstration; dotted sequence revealing Audience, Platform, UI/UX and Analysis design factors |
| 2 | Net Sales | Show the current state of sales | Net Sales and Units Sold KPI cards; Category Breakdown; Store Breakdown; Q&A; report-page tooltip; bookmark alternate views; Key Influencers and Decomposition Tree entry points |
| 3 | Returns | Show the current state of returns | Same general structure as Net Sales, with return-focused measures and visuals |
| 4 | Return Rate | Investigate the return rate for a selected product and test a changed assumption | Product-level drillthrough; What-if return-rate control; forecast and extra-profit views |
| 5 | Market Basket Analysis | Explore product combinations and related purchasing behaviour | Selected-product context; custom cluster-map visual; Open Power App action concept |

The article says additional hidden pages are used to construct tooltips and other parts of the five main pages. Their names, count, and individual configurations were not independently inspected.

## Reader journey

The documented journey moves through four levels:

1. **Orientation:** The Intro page explains the report's audience, platform, UI/UX considerations, and analytical features.
2. **Business state:** Net Sales and Returns provide a repeatable overview of the two sides of performance.
3. **Diagnosis and scenario:** Drillthrough opens product-level Return Rate or Market Basket Analysis. The What-if control lets the reader test a different return-rate assumption.
4. **Operational action:** The Market Basket Analysis page demonstrates how a product relationship could inform stock ordering through a Power Apps workflow.

This journey is inferred from the creator's described page purposes and interactions. It is not a claim about a tested navigation sequence.

## Net Sales and Returns page composition

The creator describes the Net Sales page as having two KPI cards at the top for Net Sales and Units Sold. Below them are three elements:

- Category Breakdown.
- Store Breakdown.
- Q&A visual.

A report-page tooltip appears when the reader hovers over a product category bar. Buttons below Category Breakdown switch between the visual and a tabular view. Buttons below Store Breakdown switch between the visual and a map. The alternate views are described as bookmark-driven.

The Returns page is described as using the same general structure, with returns information replacing sales information.

## Analysis paths

### Distribution insight

From Net Sales, a reader can right-click a data bar and choose Find where this distribution is different. The resulting analysis view contains suggested explanations and interactive visuals. Readers can select data points and use segment buttons to slice the analysis.

### Drillthrough

From a category bar on Net Sales, the reader can drill through to Return Rate or Market Basket Analysis. The article also describes drillthrough from the Category Breakdown visual on the Returns page.

### Return-rate scenario

Selecting a product such as OneNote through drillthrough opens the product-specific Return Rate page. The article gives a 55% return-rate example. A What-if control changes the assumed rate and updates forecast values. A separate view labelled Extra Profit shows the potential additional profit by month.

### Market-basket action

The Market Basket Analysis page shows selected-product information and a custom cluster map. The creator's example explains that buyers of one skateboard product may also buy a related product. An Open Power App action illustrates a possible stock-ordering workflow. In the public sample, an embedded video demonstrates the concept because the Power Apps visual is organisation-dependent.

## Mobile layout

The creator article says the Net Sales and Returns pages were designed for a mobile experience and points readers to Power BI Desktop's Phone layout view. The actual phone layout was not inspected. Do not infer that all five pages have equivalent mobile layouts.

## What remains unknown

- Exact page dimensions and aspect ratios.
- Full visual positions, margins, grid and spacing.
- Hidden page count and tooltip-page layout.
- Whether page navigation uses buttons, tabs, or a combination beyond the described controls.
- Actual bookmark names and saved states.
- Actual drillthrough fields and filter-retention configuration.
- Full phone layout composition.
- Whether the five-page structure is unchanged in the current PBIX file.
