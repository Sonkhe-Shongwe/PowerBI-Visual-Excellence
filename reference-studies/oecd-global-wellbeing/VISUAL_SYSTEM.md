# REF-006 — Visual System

**Source:** Creator's Microsoft Fabric Community description  
**Status:** Partial visual-system description; screenshot/runtime review pending

## 1. Known visual language

The creator describes a dynamic visual identity for each selected well-being domain:
- Domain-specific background colour.
- Domain-specific accent image.
- Dynamic page titles and subtitles.
- Subtitle colour that changes to complement the selected background.
- Colour-coordinated SVG progress bars.

This is a state-driven design approach. The domain selection changes both the analytical context and the visual styling.

## 2. Progress-bar component

Each measure displays the global average through a dynamic SVG progress bar.

The creator describes the progress bar as colour-coordinated with the selected domain. The exact scale, denominator, label placement, dimensions and SVG implementation are not available from the community post.

The trend by year is placed below the progress bar, and a country table shows observed values sorted from highest to lowest.

## 3. Repeated component structure

The creator's description implies a repeated component pattern:
1. Measure label.
2. Global-average progress bar.
3. Year trend.
4. Country-level values.

This repetition can help the reader compare different measures without relearning the layout.

## 4. Dynamic domain styling

The selected domain changes:
- Background colour.
- Accent image.
- Page title and subtitle.
- Visual title and subtitle.
- Subtitle colour.

The benefit is a clear sense of context. The risk is that domain colour may become the only cue for selection or meaning. The selected domain should remain explicit in text and controls, and every colour state should preserve adequate contrast.

## 5. Small multiples

The second page uses Power BI small multiples to compare gender-related averages across countries.

Small multiples are useful here because each panel can share a visual grammar while showing a different country, measure or category. The exact small-multiple arrangement and axes are unknown.

## 6. What cannot yet be assessed

No reliable source evidence currently establishes:
- Exact colours or hex values.
- Typography.
- Canvas dimensions.
- Grid and spacing.
- Card borders, shadows or radii.
- Chart and table density.
- Tooltip appearance.
- Navigation design.
- Accessibility settings or contrast ratios.
- Actual report rendering.

## 7. Visual inspection checklist

When the report can be rendered, verify:
- Whether the progress bar's scale and denominator are obvious.
- Whether the global average is distinguishable from a target or country value.
- Whether the selected domain is visible without relying on colour.
- Whether dynamic backgrounds preserve text and chart contrast.
- Whether the trend chart makes anomalies easy to recognise.
- Whether the country table is readable and sortable.
- Whether small multiples use comparable scales where appropriate.
- Whether dynamic title/subtitle updates remain concise and accurate.

## Current assessment

No aesthetic rating assigned. The source supports analysis of the component concept and dynamic styling approach, but not a full visual audit.
