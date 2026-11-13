# REF-001 — Transferable Patterns

**Purpose:** Extract lessons that can be reused in original Power BI projects without copying this report's branding or rebuilding the report.

## 1. Design before building

**Observed pattern:** The creator describes a raw-data audit, written narrative brief, design system and annotated wireframe before report construction.

**Why it matters:** It prevents the report from becoming a collection of visuals that do not answer a defined question. It also exposes missing data before design decisions become expensive to change.

**How to adapt it:** For each personal project, define the audience, business questions, data availability, page purpose and visual-to-measure mapping before opening the report canvas.

## 2. Use a stable page shell

**Observed pattern:** The analytical pages share a left navigation area, top filter location, content start point and How to Read control.

**Why it matters:** Users learn the navigation once and can focus on the changing analytical content.

**How to adapt it:** Establish a reusable page grid and navigation system for a multi-page report. Keep the shell consistent, but do not force every project to use a sidebar if its page count or audience does not justify one.

## 3. Define design tokens once

**Observed pattern:** The creator describes design tokens expressed in CSS and translated into a Power BI theme JSON.

**Why it matters:** It reduces formatting drift and makes global visual refinement faster.

**How to adapt it:** Define semantic colour roles, typography, spacing, corner radius, border and state tokens. Implement native visual defaults in a theme and use equivalent values in any custom components.

## 4. Build components in isolation

**Observed pattern:** The creator describes developing HTML components with mock data before placing them into the report.

**Why it matters:** Component layout can be tested without waiting for the semantic model or DAX to be complete.

**How to adapt it:** Prototype a KPI card, header, filter strip or insight panel separately. Test hierarchy and sizing with realistic placeholder content before connecting live measures.

## 5. Use native and custom visuals deliberately

**Observed pattern:** The report combines native maps, slicers and page navigation with HTML Content components for bespoke cards and charts.

**Why it matters:** Native visuals provide familiar Power BI behaviour, while custom components can support a distinctive visual requirement.

**How to adapt it:** Start with native visuals. Introduce HTML, SVG or Deneb only when a specific design or analytical need cannot be met well with the native option. Document the dependency and test the report in its target environment.

## 6. Use selectors to reduce redundant visuals

**Observed pattern:** Disconnected selector tables allow measures and components to respond to metric, view or trade-flow choices.

**Why it matters:** One visual area can support multiple analytical questions without repeating the same layout several times.

**How to adapt it:** Use a selector when the measures and units remain understandable and the change in context is obvious. Update titles, units, tooltips and labels with the selection. Do not combine fundamentally different measures if doing so makes comparisons confusing.

## 7. Give each page one analytical job

**Observed pattern:** The report separates global overview, production analysis, trade analysis and tabular detail.

**Why it matters:** The reader can move from summary to focused analysis without every page carrying every chart.

**How to adapt it:** Assign each page a question and a reader outcome. Remove visuals that do not contribute to that purpose.

## 8. Add guided explanations for unfamiliar interactions

**Observed pattern:** Tutorial overlays and How to Read controls are available on analytical pages.

**Why it matters:** A visually distinctive report can still be usable when the reader understands how to navigate it.

**How to adapt it:** Add concise instructions for non-obvious controls, advanced selectors or unusual chart interactions. Keep guidance optional and easy to dismiss.

## 9. Treat accessibility as part of component design

**Observed pattern:** The report source includes alt-text measures and tab-order configuration; the creator states that the report uses logical tab order and contrast checks.

**Why it matters:** A report is not finished if important insights are available only to users who can see and operate every visual in the default way.

**How to adapt it:** Include meaningful alt text, logical keyboard order, adequate contrast, clear labels and non-colour cues from the start. Verify the implementation rather than assuming the settings are correct.

## 10. Let motion earn its place

**Observed pattern:** The report uses animated chart drawing, dot transitions, hover overlays and a video-backed narrative panel.

**Why it matters:** Motion can reinforce a story, but it can also compete with the data and increase cognitive load.

**How to adapt it:** Use motion for meaningful state changes or narrative emphasis. Avoid persistent animation in operational reports unless it communicates something important. Test reduced-motion preferences and performance.

## 11. Keep the data model aligned to the questions

**Observed pattern:** Production and trade are separate subject-area fact tables connected to shared country and year dimensions.

**Why it matters:** Separate fact tables preserve different measurement processes while shared dimensions support consistent filtering and comparison.

**How to adapt it:** Identify the grain of each fact table, shared dimensions and relationships before designing the visuals. Do not combine facts with different grains merely to simplify a report.

## 12. Make the refresh path explicit

**Observed pattern:** The source uses local CSV paths for the FAOSTAT fact tables and documents that they must be repointed for refresh.

**Why it matters:** A report that opens but cannot refresh is not fully portable.

**How to adapt it:** Document source locations, credentials, parameters and refresh steps. Prefer a portable source strategy for personal projects intended to be shared.

## What not to copy blindly

- The peach palette and brand identity.
- The image-heavy editorial treatment.
- A persistent video background.
- Custom HTML for every KPI or chart.
- A fixed left sidebar regardless of the report's audience.
- Very small text simply to fit more information.
- Large DAX measures that mix calculation and presentation logic without considering maintainability.

## Highest-value lessons for our future projects

1. Start with a brief and data map.
2. Establish a page grid and visual hierarchy.
3. Create a reusable theme and semantic design tokens.
4. Prototype components before integrating them.
5. Use native Power BI features first and custom components selectively.
6. Make accessibility, refreshability and maintainability part of the definition of done.

These lessons can guide the user's own projects. No personal project has been modified by this study.
