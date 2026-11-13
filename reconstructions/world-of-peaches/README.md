# The World of Peaches — Forensic Workspace

**Reference:** [gusbavia/the-world-of-peaches](https://github.com/gusbavia/the-world-of-peaches)  
**Reference ID:** REF-001  
**Status:** Not audited  
**Planned role:** First deep forensic study

## Known from the public source repository

The creator's README describes this as the 2026 Power BI World Championship winning report and lists:
- A downloadable PBIX.
- 45 DAX measures organised by report page.
- 17 HTML component templates with separate CSS.
- TMDL semantic-model source.
- Report layout and bookmark definitions.
- A theme JSON containing design tokens and visual defaults.
- An MIT licence.

These are source-repository claims. They are not a substitute for opening and inspecting the PBIX.

## Audit objectives

1. Verify the current repository tree and licence.
2. Download the PBIX from the original creator's repository.
3. Open it in Power BI Desktop.
4. Record report page names, page purpose and canvas dimensions.
5. Capture page screenshots at a consistent resolution, where permitted.
6. Inspect theme JSON and identify its design tokens.
7. Inspect the DAX measures and identify reusable visual patterns.
8. Inspect the HTML/CSS templates and map each component to its use.
9. Inspect bookmarks, navigation and interactive states.
10. Record dependencies, limitations and reuse conditions.

## Planned audit outputs

- FORENSIC_AUDIT.md — completed audit using the shared template.
- PAGE_INVENTORY.md — page-by-page purpose and visual inventory.
- COMPONENT_INVENTORY.md — reusable component analysis.
- TECHNICAL_NOTES.md — theme, DAX, TMDL and custom visual findings.
- screenshots/ — only screenshots we are permitted to publish.

## Important boundary

Do not commit the creator's PBIX, extracted code, images or media into this repository unless the exact licence and asset conditions have been checked. Link to the original source and retain required notices when adapting permitted code.

## Current next action

Open the original PBIX and complete the page inventory. No visual score or reconstruction claim has been made yet.
