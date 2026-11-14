# Transferable Patterns

These are candidate patterns derived from the creator README and official Deneb documentation. They are not tested implementations from the reference PBIX.

| Pattern | When it is useful | Design and engineering checks |
|---|---|---|
| Taxonomy-style donut | A categorical composition needs a more deliberate visual hierarchy than a basic donut | Verify whether the data is hierarchical or flat; label categories clearly; avoid decorative overlays that obscure proportions |
| Dynamic marker on a horizontal bar | A value needs comparison against a moving target, benchmark or reference point | Define the marker's meaning and calculation; show units and baseline; ensure it remains visible under filters and zero/blank states |
| Tolerance-zone spectrum | A value must be positioned against acceptable, warning and critical bands | Document thresholds and units; label every zone; do not encode status by colour alone; test boundary values |
| Report-page tooltip | A mark needs contextual detail without permanently occupying page space | Preserve row context; keep essential information available outside hover; test touch and keyboard alternatives |
| Drillthrough from custom marks | A bespoke chart should retain Power BI's analytical navigation | Keep the original row resolvable; verify the right-click context menu; confirm target filters and a clear return path |
| Explain-the-dashboard page | A report contains interactions that are not obvious to first-time users | Explain the purpose and how to interact; keep instructions concise and discoverable |
| AI-assisted specification drafting | A visual is complex enough that an initial JSON draft can accelerate exploration | Treat generated JSON as a draft; inspect fields, aggregation, transforms, interactions, accessibility and performance before acceptance |

## Native visual versus Deneb decision

Prefer native Power BI visuals when they already communicate the analytical message clearly and provide the required interactions. Native visuals are usually easier to maintain and are more familiar to report authors and consumers.

Consider Deneb when a specific requirement cannot be met cleanly with native visuals, such as:
- A specialised tolerance spectrum or reference-marker composition.
- A distinctive taxonomy or radial layout.
- A custom visual grammar with precise control over labels, layering, scales or annotation.
- A reusable chart specification that needs consistent styling across multiple reports.

Do not use Deneb simply to make a standard bar chart look different. A custom specification creates additional maintenance, validation, accessibility and performance responsibilities.

## Failure-prevention checklist

- Define the chart's analytical purpose before writing JSON.
- Confirm the dataset grain and only add required fields.
- Validate field display names and types.
- Keep original row context if Power BI tooltip or drillthrough is required.
- Test filters, cross-highlighting and selected/unselected visual states.
- Check zero, blank, negative, missing and outlier values.
- Test the visual at normal report zoom and in the target Power BI environment.
- Measure performance with realistic data volumes.
- Keep a readable, commented copy of each approved specification.
- Record the Deneb version and visual dependency.

## What not to copy

- Do not reuse the creator's PBIX, workbook, visual assets or JSON specifications without permission.
- Do not assume the reference's dynamic marker is a target or threshold until the label and logic are inspected.
- Do not assume the tolerance-zone bar uses any particular statistical method.
- Do not treat AI-generated specifications as verified or production-ready.
- Do not replace native visuals with Deneb when no meaningful capability is gained.
