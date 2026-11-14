# REF-004 - Microsoft 2026 Power BI samples

**Status:** Sample selected; Power BI Desktop inspection pending  
**Selected report:** AdventureWorks Sales (2026 refresh)  
**Study type:** Official documentation and repository-metadata review so far  
**Current P2 progress:** 50%; this selection note does not count as a completed study

## Source links

- [Microsoft Power BI sample catalogue](https://learn.microsoft.com/en-us/power-bi/create-reports/sample-datasets)
- [Microsoft Power BI Desktop sample repository](https://github.com/microsoft/powerbi-desktop-samples)
- [AdventureWorks Sales (2026 refresh) PBIX](https://github.com/microsoft/powerbi-desktop-samples/blob/main/2026%20Power%20BI%20Samples%20Revamp/AdventureWorks%20Sales.pbix)

## Why this sample was selected

AdventureWorks Sales is a useful first report for the current visual-design audit because Microsoft specifically documents these features in the 2026 refresh:

- Dark report theme.
- Donut centre values.
- Series labels.
- Azure Maps.
- Date picker supporting compact calendar, range and relative-date filtering.

The wider 2026 refresh is also intended to demonstrate modern Power BI report and semantic-model practices. Microsoft describes improvements such as a larger default canvas, mobile-optimised layouts, report-page tooltips, newer native visuals, clearer table/column/measure names and descriptions, consistent formats, sort-by columns, hidden technical columns, relationship review and calculation groups. These collection-wide statements are audit prompts, not proof that every item appears in AdventureWorks Sales.

## Confirmed file evidence

- Repository: `microsoft/powerbi-desktop-samples`
- Branch: `main`
- Path: `2026 Power BI Samples Revamp/AdventureWorks Sales.pbix`
- GitHub tree metadata size: 8,390,782 bytes (about 8.39 MB).
- The PBIX is available from the official GitHub repository.

## Evidence boundary

**Verified from public sources:** sample identity, PBIX file presence, file size metadata and the features described by Microsoft.

**Not yet verified:** actual page count, page names, canvas dimensions, visual positions, spacing, typography, exact theme colours, data model tables and relationships, DAX implementation, Power Query steps, mobile layout, accessibility, performance and interactive behaviour.

The PBIX has not yet been opened in Power BI Desktop. Do not describe any of the unverified items as inspected or tested.

## Desktop inspection protocol

### 1. Establish the report structure

- Open the downloaded PBIX in Power BI Desktop.
- Record the Power BI Desktop version and inspection date.
- List every report page in order.
- Record canvas dimensions and page background for each page.
- Capture a full-page screenshot at a consistent zoom and resolution.
- Identify each page's purpose and how it contributes to the report narrative.

### 2. Audit the visual system

For each page, record:

- Layout grid, margins, spacing, alignment and grouping.
- Heading, KPI, body and annotation typography.
- Backgrounds, surfaces, borders, shadows and colour roles.
- KPI card hierarchy, number formats and contextual labels.
- Donut centre-value treatment and label placement.
- Series labels, axis treatment, legend use and chart density.
- Map placement, geographic encoding, labels and controls.
- Consistency of selected, hover, focus and disabled states.

Do not assign a visual score until the pages have been inspected using the project's forensic audit template.

### 3. Test interactions

- Test compact calendar, range and relative-date modes.
- Confirm how date selections affect each page and visual.
- Test Azure Maps selection, cross-filtering and drill behaviour.
- Test donut selection and cross-highlighting.
- Check report-page tooltips and navigation.
- Inspect the phone layout separately from the desktop canvas.
- Record unexpected behaviour and any interaction that cannot be tested.

### 4. Inspect the semantic model

Record:

- Tables, columns, measures and their descriptions.
- Primary keys, foreign keys and relationship cardinality.
- Active/inactive relationships and filter direction.
- Date-table configuration and sort-by columns.
- Data types, default summarisation and hidden technical columns.
- Calculation groups and their intended reuse.
- Measure folders, display folders and formatting conventions.
- Any model objects that are unclear, redundant or difficult to maintain.

### 5. Review implementation quality

- Inspect representative DAX measures and trace their filter context.
- Inspect Power Query transformations and data types.
- Check whether visual calculations or model measures are used appropriately.
- Use Performance Analyzer for representative pages if practical.
- Review contrast, text size, alternative text, reading order and keyboard behaviour.
- Separate observed behaviour from assumptions about the underlying implementation.

## Acceptance criteria

REF-004 is ready to close only when:

- All pages have a documented purpose and component inventory.
- The visual system and report hierarchy are recorded with screenshot evidence.
- The documented date-picker and map interactions have been tested.
- The semantic model structure and important relationships are recorded.
- DAX and Power Query findings are supported by inspected evidence.
- Accessibility and performance limitations are documented, including any tests not performed.
- Findings are labelled as observed, source-documented, inferred or unknown.
- Transferable patterns are written without copying the report wholesale.

## Licensing and reuse

The Microsoft sample repository has a root MIT licence. However, Microsoft's sample documentation separately states that sample workbooks and related data are the property of obviEnce, LLC, and that use requires the stated attribution, including the `obviEnce ©` notice for workbooks and visualisations.

Do not assume the repository's root MIT licence grants unrestricted rights to every embedded sample asset. Keep the PBIX and extracted sample data out of this research repository. Verify the exact terms before reusing any asset, data or implementation in a personal project.

## Next action

Download the [official AdventureWorks Sales (2026 refresh) PBIX](https://github.com/microsoft/powerbi-desktop-samples/blob/main/2026%20Power%20BI%20Samples%20Revamp/AdventureWorks%20Sales.pbix), open it in Power BI Desktop and capture the report page screenshots plus the Model view. Use those observations to complete the forensic audit.