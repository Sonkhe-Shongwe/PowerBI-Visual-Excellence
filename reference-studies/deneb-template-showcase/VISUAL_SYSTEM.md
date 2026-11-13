# REF-011 — Visual System

**Source:** BI Nexus theme JSON, dashboard layout JSON and selected template specifications  
**Status:** Source-level visual system documented; runtime rendering pending

## 1. Overall direction

The showcase uses a clean enterprise KPI dashboard style:
- White page background and card surfaces.
- Deep navy/ink text.
- Blue as the primary accent.
- Amber for emphasis and table accents.
- Muted slate text.
- Thin borders and subtle card shadows.
- Consistent section titles and supporting captions.

The main dashboard uses a 1600 × 900 canvas, with four headline cards across the top and four analytical columns below.

## 2. Theme architecture

The report combines:
- Fluent2-CY26SU07 as its base Power BI theme.
- bi-nexus.json as a custom registered theme.
- dashboard-background.svg as a registered image resource.

The custom theme exposes semantic colours:
- Primary blue #1E6FD9.
- Deep blue #0B3D91.
- Sky blue #5DA9E9.
- Amber #FFB703.
- Good #1E6FD9.
- Bad #D62828.
- Neutral #94A3B8.
- Sequential minimum #D6E7F7, centre #5DA9E9 and maximum #0B3D91.
- White background.

This is more useful than a palette with unnamed colours because it defines roles for sentiment and sequential scales.

## 3. Dashboard layout

The 12 visual components use a repeated grid:
- Four equally sized KPI cards at the top.
- Four analysis columns below.
- Two analytical components in each column.
- Repeated 310 px column widths.
- Text headings and captions aligned to the component columns.

This creates a consistent visual rhythm and makes the page easier to scan.

## 4. Template-level styling

### KPI Line Card

- Header band using the theme's primary colour.
- Large headline value.
- Three concise status lines.
- Monthly line chart.
- Target line and good/bad markers.
- Responsive sizing based on visual width and height.

### Bullet Chart

- Light previous-year comparison bar behind the actual bar.
- Actual bar coloured according to performance against budget.
- Budget tick.
- Value label that moves inside or outside the bar depending on available space.
- Tooltips with values and variances.

### Calendar Heatmap

- Calendar grid with weeks as columns and weekdays as rows.
- Five sequential theme-colour steps.
- Distinct empty-day treatment.
- Peak-day ring.
- Optional target-met/target-missed mode.

### KPI Small Multiples

- Repeated mini-panels.
- Latest value and change.
- Sparkline per category.
- Reflowing grid.
- Optional shared scale for direct comparison.

### P&L Accounts Statement

- Account label gutter.
- Current period and year-to-date groups.
- Detail/subtotal/total row hierarchy.
- Zebra banding.
- Dividers between statement groups.
- Conditional variance colour.

## 5. Design-system engineering

The templates expose parameters for:
- Colour.
- Text.
- Formatting.
- Labels.
- Sorting.
- Dimensions.
- Spacing.
- Behaviour.

Theme helper functions let the spec reuse the Power BI theme's data and sentiment colours. This reduces one-off hardcoded styling and makes the template easier to adapt.

## 6. Accessibility and usability

The showcase layout includes alt text on visual placements and explanatory text for abbreviations. Template metadata includes tooltip and context-menu settings, with selection/highlight enabled only where appropriate.

However, the source-level presence of metadata does not prove that the visuals are fully accessible. Runtime testing should cover:
- Keyboard navigation.
- Screen-reader output.
- Tooltip content.
- Colour contrast.
- Selected/focus states.
- Dense labels and small text.
- Behaviour when the visual is resized.

## 7. Critical observations

### Strong decisions

- Semantic theme tokens.
- Consistent card and chart parameters.
- Responsive component sizing.
- Clear separation between page-level layout and reusable visual templates.
- A repeatable visual grammar across 21 different visual types.

### Trade-offs

- The custom theme and template styles need to be maintained together.
- Some components use complex custom labels and SVG/Vega marks that may need careful accessibility alternatives.
- A consistent template library can encourage visual sameness if used without regard to the analytical task.
- A 1600 × 900 showcase page may need adaptation for smaller report viewports.

## 8. What to carry forward

Adopt semantic design tokens, consistent component contracts, reusable layout patterns and deliberate parameterisation. Do not copy the exact BI Nexus colour palette or force Deneb into a project where native visuals already solve the problem well.
