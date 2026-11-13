# REF-009 — Page Architecture

**Source:** Creator's community entry, walkthrough transcript and published screenshot  
**Status:** Main view and interaction structure documented; full page count/runtime pending

## Main report composition

The creator describes three main parts:
1. Navigation and player selection.
2. Player card.
3. Basketball shot chart.

The public screenshot shows these arranged as a coordinated selection-and-analysis view.

The exact report page count and page dimensions are not stated in the inspected source.

## 1. Player and team navigation

**Purpose:** Let the reader choose a team and player.

Creator-described implementation:
- Button slicer or list slicer.
- Team logos.
- Player headshots.
- Selected player state.

The published screenshot shows a vertical list of players on the left, with the selected player highlighted.

## 2. Player card

**Purpose:** Present the selected player's profile and performance.

The screenshot shows:
- Player headshot.
- Team logo watermark.
- Player name.
- Position.
- Field-goal percentage.
- Total points.

The creator describes a front/back interaction using two measures in a card visual. Layout visibility ensures that only one side is shown. Left/right buttons change the visible state.

The reverse-side content and exact measure names are not available from the public walkthrough transcript.

## 3. Shot chart

**Purpose:** Show the spatial distribution of the selected player's shots.

The creator describes:
- A half-court image.
- A scatter plot placed above the image.
- X/Y coordinates from the shot dataset.
- Filters for all shots, two-pointers, three-pointers and court zones.
- Statistics that update with the selected shot group.

The published screenshot shows the shot points overlaid on a half-court diagram.

## 4. Supporting KPIs

The screenshot shows player metrics compared against team and NBA context. The visible example includes field-goal percentage, total points and points per shot.

The exact number and layout of KPI cards are not established.

## Reader journey

1. Choose a team.
2. Choose a player.
3. Inspect the player's front-side profile.
4. Flip the card to reveal additional statistics.
5. Filter shot types or zones.
6. Explore the player's shot distribution.
7. Compare player performance with team and league benchmarks.

## Architecture lessons

- Keep entity selection, player profile and spatial analysis visibly connected.
- Use a compact card state to reveal additional context without creating a new page.
- Use an image as a chart coordinate background only when the spatial data maps reliably to the image.
- Keep the active player, team and shot filter visible so the reader understands the current analytical state.

## Unknowns

- Exact page count and page names.
- Canvas size and visual coordinates.
- Whether the card flip is implemented with bookmarks, selection pane visibility or another state mechanism.
- Exact DAX measures and card visual configuration.
- Whether the shot chart is a native scatter plot with a background image or another supported layering arrangement in the PBIX.
- Filter sync, tooltip and drillthrough behaviour.
- Keyboard navigation and screen-reader output.
