# REF-009 — Transferable Patterns

**Purpose:** Capture interaction and visual-composition techniques from Power BI Basketball Cards. These are ideas to adapt when a project needs them, not a template to copy.

## 1. Make selection feel like navigation

**Observed:** The creator uses a button slicer or list slicer with team logos and player headshots.

**Why it matters:** A slicer can become a navigation surface when the selected entity is the main context for the page.

**Apply:** Use image-backed buttons when the images genuinely help recognition. Keep text labels visible and provide search or list alternatives for large selections.

## 2. Reveal additional information with a card state

**Observed:** A front/back player card uses two measures and layout visibility so only one side appears at a time.

**Why it matters:** The report can show additional context without adding more permanent visual clutter.

**Apply:** Use state-based card views for profile/detail or summary/diagnostic content. Make the current state obvious and ensure the transition is keyboard accessible.

## 3. Use a background image as a coordinate plane

**Observed:** A half-court image sits beneath a scatter plot whose X/Y values locate each shot.

**Why it matters:** A familiar spatial background gives meaning to numeric coordinates and turns a scatter plot into a contextual map.

**Apply:** This technique can work for floor plans, site layouts, process maps or equipment diagrams. Calibrate the coordinate bounds and aspect ratio carefully. Do not use a background image if the coordinates cannot be mapped accurately.

## 4. Let the same selection drive the whole analytical view

**Observed:** Player selection updates the card, KPI comparisons and shot chart.

**Why it matters:** The reader can explore one entity without losing context across disconnected visuals.

**Apply:** Define the intended interaction model before building the page. Ensure the selected entity, active metric and filter state remain visible.

## 5. Provide meaningful comparison context

**Observed:** Player statistics are compared with team and NBA benchmarks.

**Why it matters:** A raw value becomes more useful when the reader can judge whether it is above or below a relevant reference.

**Apply:** Choose a benchmark appropriate to the question, label it clearly and ensure the denominator/population is correct.

## 6. Use native visuals before custom visuals

**Observed:** The creator describes the report as built entirely with Power BI core visuals and no add-ons.

**Why it matters:** Native visuals can reduce deployment dependencies and improve compatibility in controlled Power BI environments.

**Apply:** Start with native slicers, cards, scatter plots and layout states. Introduce a custom visual only when the requirement cannot be met well with native capabilities.

## 7. Treat image cropping as part of quality assurance

**Observed:** A community commenter noted that some player headshots cropped foreheads.

**Why it matters:** A small image-fitting issue can make a polished report feel unfinished.

**Apply:** Test every image in its final container, define crop position, preserve focal points and provide a graceful fallback for missing assets.

## What not to copy blindly

- A flip interaction when a simple tooltip would be clearer.
- Image-only navigation that depends on users recognising faces or logos.
- A scatter plot over an image without reliable coordinate mapping.
- Excessive animations or transitions.
- Player images and logos without appropriate usage rights.
- A sports-card visual metaphor in a business report where it does not fit the audience.

## Highest-value lessons

1. Use native slicers as clear navigation surfaces.
2. Use layout states to reveal additional detail without permanent clutter.
3. Overlay scatter plots on images only when the coordinate system is calibrated.
4. Keep one entity selection connected across cards, KPIs and charts.
5. Treat image crop and accessibility as part of the component definition of done.

No personal project has been modified by this study.
