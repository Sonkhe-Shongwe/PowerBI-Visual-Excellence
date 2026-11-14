# Visual System

## Theme and surfaces

The saved report references the Fluent2-CY26SU08 base theme and the embedded SoftDark theme. These values are theme definitions. The rendered result can vary where a visual overrides the theme or applies transparency.

| Theme role | Saved value |
|---|---|
| Page fill | #242424 with 14% transparency |
| Outer background | #1B1B1B |
| Default visual surface | #292929 |
| Main and secondary foreground | #F0F0F0, #B8B8B8 |
| Visual border and gridline defaults | #494949 |
| Accent and table accent | #75B7FF, #4DA6FF |
| Good, neutral and bad tokens | #5BD667, #E6C84F, #FF6B76 |

## Visual formatting

- The KPI card uses per-measure callout and label colour overrides. Readability of the subdued labels against the actual card surface needs checking.
- The orders line chart explicitly enables series labels on desktop. The phone override hides the series labels and value axis. The colour rule uses a measure named Latest year, whose saved DAX returns the minimum year in the evaluated context. Check which series the rule emphasises after filtering.
- Azure Maps uses a dark grayscale base with bubbles sized by customer count. Bubble fill uses a customer-count gradient. The filled-map and heatmap layers are disabled in the saved configuration.
- The donut uses a cost-based colour gradient and a dark border between segments. Microsoft describes a centre value for the sample. The saved donut definition contains no explicit centre-value override. Verify the displayed value and how it reacts to selection in Desktop.
- The profit-by-channel chart uses a labelled reference line and conditional colour. The matrix has data-bar formatting for Profit Margin % and icon rules for Products.
- Several phone title/subtitle overrides use sizes of 10 and 8, and the mobile matrix grid uses 8. Check these on a phone-sized canvas before using the sizes as a reference.

Source: [Pinned PBIX](README.md#source) and [Microsoft Learn](https://learn.microsoft.com/en-us/power-bi/create-reports/sample-datasets).
