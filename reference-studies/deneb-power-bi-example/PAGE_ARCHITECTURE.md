# Page Architecture

## Report structure

The creator README names five pages. Their names are verified from the README, but their actual layout, canvas dimensions, navigation and content have not been inspected in Power BI Desktop.

| Sequence | Page | Creator-described purpose | Evidence boundary |
|---:|---|---|---|
| 1 | How This Dashboard Works | Explains report functionality | Detailed content and layout unknown |
| 2 | Taxonomy | Contains a Deneb donut visual overlaid with an AI-generated visual | Visual construction, data mapping and page composition unknown |
| 3 | Drillthrough | Demonstrates drillthrough navigation | Source page, destination context and drillthrough fields unknown |
| 4 | Tooltip Page | Demonstrates report-page tooltip functionality | Tooltip assignment, dimensions and contents unknown |
| 5 | Tolerance Zones | Contains a Deneb spectrum bar | Threshold definitions, visual encodings and calculations unknown |

## Known report journey

The README suggests a learning sequence: explain how the report works, show a specialised taxonomy visual, demonstrate drillthrough and tooltips, and then present a tolerance-zone visual. This is a reasonable interpretation of the page names, not a verified navigation sequence.

## Visual components named by the creator

### Taxonomy donut
A Deneb donut chart with tooltips and drillthrough. The README says it overlays an AI-generated visual. The exact relationship between the two visual elements is not described.

### Drillthrough
The report includes a page dedicated to drillthrough. The README does not identify the originating visual, destination fields, retained filters or return-navigation method.

### Tooltip page
A report-page tooltip is included. The README does not state which visual invokes it, what fields are passed, or whether the tooltip uses a detail layout or a narrative explanation.

### Tolerance-zone spectrum bar
A Deneb spectrum bar is shown on the Tolerance Zones page. The README does not define the lower/upper limits, target zone, out-of-tolerance state, marker semantics or calculation logic.

## What remains unknown

- Actual page count and hidden-page count.
- Page dimensions, aspect ratio and mobile layout.
- Canvas background, grid, spacing and component positions.
- Navigation buttons and saved bookmark states.
- Model tables, relationships, measures and calculated columns.
- Deneb visual count and which specification is used on each page.
- Actual drillthrough fields and filter retention.
- Tooltip page assignments and tooltip content.
- Dynamic marker calculation and tolerance thresholds.
- Whether the README's five-page description matches the PBIX as currently stored.
