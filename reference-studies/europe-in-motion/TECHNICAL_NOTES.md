# REF-007 — Technical Notes

**Source:** Creator's Microsoft Fabric Community post, replies, LinkedIn entry and employer announcement  
**Status:** Descriptive technical analysis; PBIX/source inspection pending

## 1. Confirmed technical elements

The creator confirms:
- HTML Content custom visual for KPI cards on the Overview page.
- HTML and CSS for animated text overlays on KPI cards.
- Dynamic colour treatment across the report.
- DAX-powered bar chart for country rankings.

The report description also identifies:
- Native line chart.
- Regional bar chart.
- Map.
- Dynamic cards.
- Scatter plot with configurable axes and bubble size.
- Independent filters for two-country comparison.
- Dynamic summary text.

## 2. HTML Content and CSS animation

The creator states that the KPI cards use the HTML Content custom visual and that animated text overlays are built with HTML/CSS.

This suggests that the report combines native analytical visuals with custom HTML components for presentation.

Unknown:
- Exact HTML structure.
- Whether CSS is embedded in DAX measures or stored separately.
- How the animated text responds to hover, selection or filter changes.
- How the visual behaves in Power BI Service and export.

## 3. Dynamic context and colours

The creator describes dynamic colours that are connected to report elements and selected context.

Unknown:
- Exact semantic colour mapping.
- Whether colour changes are driven by DAX measures, conditional formatting, bookmarks or another mechanism.
- How colour states are tested for contrast and colour blindness.

## 4. Scatter plot controls

The Contrasts page allows the reader to customise:
- X-axis indicator.
- Y-axis indicator.
- Bubble size.

The exact implementation is not available. It could use a field parameter, disconnected selector tables, dynamic measures or another design. Do not assume a particular mechanism until the PBIX is inspected.

## 5. Head-to-head comparison

The Head-to-Head page uses independent filters for two countries and a central chart to compare three dimensions.

Unknown:
- How the two country selections are stored.
- Whether disconnected slicer tables or field parameters are used.
- How missing country values and ties are handled.
- How the comparison chart normalises or displays measures with different units.

## 6. Accessibility

The employer's announcement says the winning solution incorporated a colour-blindness simulator.

The implementation could be a visual mode or an interactive control, but the source does not specify the method. Do not assume it is a standard Power BI feature or a specific custom visual.

## 7. Source access and unknowns

The community post includes a Power BI embed token. A separate downloadable PBIX or source repository was not confirmed in the inspected discussion. A commenter requested the PBIX, and the creator replied that they were beginning to share tutorials about HTML/CSS components.

Not inspected:
- Semantic model.
- Relationships.
- Power Query.
- DAX measures.
- Theme JSON.
- Report JSON.
- Bookmark definitions.
- Exact custom visual version.
- Runtime rendering and performance.

## 8. Future technical verification

If the PBIX or source code becomes available:
1. Inspect the HTML Content visual and its version.
2. Trace the KPI card measures and CSS animation.
3. Identify the dynamic colour mechanism.
4. Inspect the map visual and its data binding.
5. Determine how X/Y/bubble-size selection works.
6. Inspect the independent country filters and comparison measures.
7. Test the colour-blindness simulator.
8. Verify keyboard, screen-reader and Power BI Service behaviour.
