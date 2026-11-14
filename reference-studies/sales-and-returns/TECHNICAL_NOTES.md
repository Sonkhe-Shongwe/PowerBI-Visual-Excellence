# Technical Notes

## Documented implementation techniques

| Technique or feature | What the source describes | Current verification status |
|---|---|---|
| Bookmark-driven alternate views | Category Breakdown can switch to a table; Store Breakdown can switch to a map | Creator-described; bookmark definitions not inspected |
| Report-page tooltips | Hovering over a category bar opens a tooltip with more product information | Creator-described; tooltip page not inspected |
| Mapbox custom visual | Store map uses a Mapbox visual from AppSource | Creator-described; visual package and version not checked |
| Cross-highlighting and filtering | The Mapbox visual can interact with core Power BI visuals | Creator-described; not tested |
| Q&A visual | Readers can ask questions and explore additional details | Creator-described; not tested |
| Key Influencers | A button opens a customer-demographic analysis view | Creator-described; not tested |
| Decomposition Tree | A button opens a visual for drilling into dimensions that drive a metric | Creator-described; not tested |
| AI distribution insight | Find where this distribution is different opens an interactive analysis view | Creator-described; not tested |
| Drillthrough | Category bars open Return Rate or Market Basket Analysis pages | Creator-described; fields and filter context not inspected |
| What-if analysis | A return-rate control changes forecast values and the Extra Profit view | Creator-described; not tested |
| Cluster map | Market Basket Analysis uses a custom visual to show product relationships | Creator-described; package and data mapping not inspected |
| Power Apps integration | Open Power App illustrates an operational ordering workflow | Creator-described; public sample uses a video demonstration due organisation access limitations |
| Animated tooltips | Visual-header help icons show animated guidance about interactions | Microsoft Learn and creator-described; tooltip assets not inspected |
| Phone layout | Net Sales and Returns are described as mobile-optimised | Creator-described; phone layout not inspected |

## Important implementation considerations

### Bookmarks and alternate views

The report uses bookmarks to switch between a chart and a table, and between a store visual and a map. This is a useful interaction pattern when two representations answer different questions but do not need to be visible simultaneously.

For an original report, the buttons should clearly communicate the available view, show which state is active, and preserve relevant filters. The actual bookmark configuration in this sample has not been inspected.

### Drillthrough and filter context

The report uses right-click drillthrough from category bars to product-level analytical pages. A production implementation should make the destination clear, retain the intended product and date context, provide a visible way back, and avoid silently dropping filters. These are implementation recommendations, not verified features of this sample.

### What-if scenario analysis

The Return Rate page demonstrates a parameter-driven scenario. The reader changes the assumed return rate and sees forecast values update. The Extra Profit view communicates the potential financial consequence.

A reusable design should distinguish:
- The observed baseline.
- The changed assumption.
- The forecast under the scenario.
- The incremental outcome.

The PBIX DAX, parameter table, calculation logic, and treatment of uncertainty have not been inspected.

### Custom visual and Power Apps dependencies

The report tour identifies Mapbox and a custom cluster-map visual. It also describes a Power Apps integration. Before adopting similar dependencies, check current AppSource availability, visual certification and privacy terms, tenant restrictions, user permissions, and mobile support.

The source article says the public sample demonstrates the Power Apps workflow with an embedded video because the actual Power Apps visual is only viewable by users in the same organisation. Do not assume the public sample includes a working ordering application.

### Preview features and version sensitivity

Microsoft Learn instructs users to enable preview features in Power BI Desktop for the full experience. The older creator article specifically describes Decomposition Tree as a preview feature at publication time. Feature status and configuration can change. Record the current Desktop version and preview settings during the eventual runtime inspection.

## PBIX and source status

The official Microsoft repository lists Sales & Returns Sample v201912.pbix at approximately 6.23 MB. The file is available for download, but its binary contents were not inspected in this study. No DAX, Power Query, semantic-model, bookmark, or visual-configuration details are claimed beyond the published creator documentation.

## Runtime validation still required

- Open the PBIX and record the Desktop version and any required preview settings.
- Record all visible and hidden pages.
- Inspect the model, relationships, measures, calculated tables, and Power Query steps.
- Inspect bookmarks and verify that alternate views preserve filter state.
- Test tooltips, Q&A, Key Influencers, Decomposition Tree, and AI insights.
- Test drillthrough from both Net Sales and Returns.
- Reconcile the What-if parameter and forecast outputs against the DAX.
- Check custom visual names, versions, availability, and permissions.
- Inspect the Power Apps visual and identify the actual organisation-specific boundary.
- Inspect phone layout, accessibility, and Performance Analyzer timings.
