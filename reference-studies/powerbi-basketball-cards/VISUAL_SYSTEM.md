# REF-009 — Visual System

**Source:** Published screenshot, creator's walkthrough and community entry  
**Status:** Screenshot-level visual review; full theme and layout system unknown

## 1. Overall visual direction

The visible report uses a clean, light sports-card aesthetic:
- White/light canvas.
- Rounded rectangular cards.
- Thin blue outlines and selected-state borders.
- Player headshots and team logos.
- Team logo watermark inside the player card.
- Blue shot markers over a half-court image.
- Compact KPI comparison cards.

The visual metaphor is clear: the player card resembles a collectible sports card, while the shot chart provides a spatial analytical view.

## 2. Composition

The screenshot shows three main visual zones:
- Left: player selection list with headshots.
- Centre: selected-player card.
- Right: KPI comparisons and half-court shot chart.

This arrangement connects selection, player context and spatial analysis without requiring the reader to navigate between separate pages.

## 3. Player card design

The player card uses a large headshot, a team-logo watermark, name and position, plus key statistics. The two-sided card concept gives the creator a way to separate profile information from additional performance detail.

A community commenter noted that some player images crop the forehead. This is a useful reminder that image fitting and crop position are part of visual quality, not just asset selection.

## 4. Shot chart

The shot chart layers blue scatter points over a half-court image. The points use X/Y coordinates, so the chart's visual accuracy depends on:
- Correct coordinate scaling.
- Correct court image aspect ratio.
- Correct axis orientation.
- Consistent placement of the background image and scatter plot.
- Appropriate clipping and point sizing.

The screenshot shows a dense set of shot locations while preserving the court context.

## 5. Navigation and selected states

The creator describes button slicer or list slicer navigation. Images provide immediate context, and the selected state helps the reader identify the current team/player.

The card flip is a state change that shows one side at a time. The user should always be able to tell which side is active and how to return.

## 6. Accessibility and usability questions

- Do player names remain visible and searchable without relying on headshots?
- Are player/team images given useful alt text?
- Can the card be flipped with keyboard input?
- Is the active card side announced or clearly labelled?
- Are selected and hover states distinguishable without colour alone?
- Are shot filters keyboard accessible?
- Does the chart have an alternative description or table for users who cannot interpret the spatial plot?
- Are image crops consistent across different aspect ratios?

## 7. What cannot yet be assessed

The screenshot and walkthrough do not establish:
- Exact palette values.
- Font family and type scale.
- Canvas dimensions.
- Spacing tokens and grid.
- Theme JSON.
- Shadow and border settings beyond the visible screenshot.
- Mobile or responsive behaviour.
- Tooltip styling.
- Runtime performance.
- Accessibility implementation.

## Current assessment

The screenshot supports a positive assessment of the main composition and interaction concept, but no overall aesthetic score is assigned without the full report and runtime inspection.
