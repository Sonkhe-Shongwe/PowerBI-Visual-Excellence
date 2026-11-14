# Transferable Patterns

These are candidates for an original design system. Their source configurations are documented and their behaviour should be verified in the intended report context.

| Pattern | Use it when | Check before adoption |
|---|---|---|
| One native card for related metrics | A summary needs consistent metric order and styling across screen sizes | Measure grouping, label contrast, narrow wrapping and phone reading order |
| Separate date range and date basis | Different operational dates can describe the same event | Label both controls clearly and test every supported basis with a known date range |
| Theme surfaces with deliberate overrides | A dark report needs a consistent canvas and visual surface hierarchy | Test actual title, label, grid and status colour combinations at target zoom |
| Measure-driven native formatting | A trend needs one series emphasised or a matrix needs concise in-cell cues | Confirm the intended measure result in filtered and unfiltered states and retain readable labels |
| Map paired with ranked comparison | Geography matters and the user also needs precise category comparison | Verify geocoding, ties, map availability and an accessible way to read the underlying counts |
| Phone layout as a deliberate composition | The desktop page has several side-by-side visuals | Reflow by reading priority, check tab order and keep labels legible at phone size |

Source: [Report layout](PAGE_ARCHITECTURE.md), [visual configuration](VISUAL_SYSTEM.md) and [model inspection](TECHNICAL_NOTES.md).
