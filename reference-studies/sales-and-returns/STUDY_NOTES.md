# Study Notes

## 1. Reference identity

- **Reference ID:** REF-005
- **Report:** Sales and Returns sample
- **Creators:** Miguel Myers and Chris Hamill, acknowledged by the Microsoft Fabric Community tour article
- **Publisher:** Microsoft Power BI sample collection
- **Scenario:** A fictional company selling Microsoft-themed skateboards
- **Report file:** Sales & Returns Sample v201912.pbix
- **Evidence date:** 2026-11-14
- **Study type:** Description-led, supported by a limited official screenshot
- **Priority:** Medium

## 2. Purpose and audience

The report is described as a way to understand the current state of sales and returns and analyse how the company should modify its operations.

The report is designed for multiple audiences. The creator article explicitly describes an operations user who can use a product-combination insight to prepare for increased demand and initiate an ordering workflow. The report also supports consumers who need to explore sales, returns, products, stores, and customer patterns.

The primary business question is how sales and returns are performing and where further investigation or operational action may be useful. This is a synthesis of the report description, not a quoted report requirement.

## 3. Evidence and access

| Evidence | Status | What it supports |
|---|---|---|
| Microsoft Learn report article | Inspected | Scenario, five main pages, feature summary, preview-feature instruction |
| Microsoft Fabric Community tour | Inspected | Page purposes, page-level visuals, bookmarks, tooltips, drillthrough, What-if, Power Apps and mobile design |
| Official GitHub PBIX listing | Verified | File existence and approximate size of 6.23 MB |
| Official Microsoft Learn screenshot | Inspected | One partial visual example of the Returns page and its layout |
| PBIX internal structure | Not inspected | Model, DAX, Power Query, bookmarks, visual configuration and hidden-page inventory remain unknown |
| Power BI Desktop runtime | Not tested | Rendering, interactions, accessibility, mobile behaviour and performance remain unverified |

## 4. Main documented capabilities

- Five main report pages: Intro, Net Sales, Returns, Return Rate, and Market Basket Analysis.
- Hidden pages used for tooltips and other report elements.
- KPI cards for Net Sales and Units Sold on the Net Sales page.
- Category and store breakdowns, plus a Q&A visual.
- Report-page tooltips on product category bars.
- Bookmark-driven alternate views for category and store breakdowns.
- A Mapbox custom visual from AppSource.
- Buttons that expose Key Influencers and Decomposition Tree analysis views.
- A Returns page that follows the same structure as Net Sales.
- Right-click AI insights using the option labelled Find where this distribution is different.
- Drillthrough from sales or returns categories to Return Rate and Market Basket Analysis.
- A What-if control that changes a product return-rate assumption and updates forecast results.
- A custom cluster-map visual for product-combination analysis.
- A Power Apps workflow concept for stock ordering.
- Animated tooltips and phone-layout design.

These capabilities are documented by Microsoft and the report creators. They have not been independently tested in Desktop.

## 5. Critical interpretation

The strongest feature is the separation of report roles. Net Sales and Returns communicate business state. Return Rate and Market Basket Analysis support deeper analysis. The What-if control turns a diagnostic result into a scenario that can be considered operationally.

The repeated structure of Net Sales and Returns is useful because readers can reuse the same navigation and visual expectations while changing the subject of analysis.

The report is also a useful example of Power BI as more than a collection of charts. Bookmarks, drillthrough, tooltips, AI visuals, custom visuals, and Power Apps are combined to support exploration and action.

## 6. Limitations and caution

- The PBIX is a legacy v201912 sample. Treat it primarily as an interaction and information-architecture reference rather than evidence of current default Power BI design conventions.
- The creator article asks users to enable preview features for the full Desktop experience. The Decomposition Tree was described as a preview feature at the time of publication. Availability and configuration may differ in current Desktop versions.
- The Mapbox and cluster-map visuals are custom visual dependencies. Their exact package names, versions, licensing, tenant policies, and current availability have not been checked.
- The Power Apps visual is organisation-dependent. The article says the public sample uses an embedded video to demonstrate an example because the actual Power Apps visual is only viewable by users in the same organisation.
- Mobile optimisation is described for Net Sales and Returns, but no phone layout was tested.
- The screenshots are partial. They do not establish exact page dimensions, typography, spacing, theme tokens, contrast ratios, or accessibility quality.

## 7. Benchmark decision

No numerical benchmark score is assigned. The report has useful interaction evidence, but the available material does not support a complete visual or functional audit. Missing evidence is not treated as poor quality.

## 8. Sources

- [Microsoft Learn report article](https://learn.microsoft.com/en-us/power-bi/create-reports/sample-sales-returns)
- [Microsoft Fabric Community creator tour](https://community.fabric.microsoft.com/blog/fbc_pbiupdatesblog/take-a-tour-of-the-new-sales--returns-sample-report/5175940)
- [Official PBIX listing](https://github.com/microsoft/powerbi-desktop-samples/blob/main/Sample%20Reports/Sales%20%26%20Returns%20Sample%20v201912.pbix)
