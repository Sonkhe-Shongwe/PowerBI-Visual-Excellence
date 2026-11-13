# REF-009 — Technical Notes

**Source:** Creator's walkthrough transcript, community entry and screenshot  
**Status:** Interaction approach documented; PBIX/DAX inspection pending

## 1. Native-visual approach

The creator explicitly states that the report uses Power BI core visuals with no custom visual add-ons.

The walkthrough identifies:
- Button slicer or list slicer for navigation.
- A card visual for the player profile.
- Two measures for front/back card content.
- Layout visibility to show one card state at a time.
- Left/right buttons to switch between the states.
- A scatter plot for shot locations.
- A half-court image behind the scatter plot.

The exact Power BI visual versions and formatting settings are not confirmed.

## 2. Flippable card pattern

The creator's described pattern:
1. Create a measure for the front side.
2. Create a measure for the back side.
3. Place the two measures into a card visual or paired card components.
4. Use layout visibility so only the intended side is visible.
5. Use left/right buttons to switch the visible state.

This is a visibility/state interaction. The walkthrough does not establish whether the state is managed by bookmarks, selection-pane visibility, a button slicer or another mechanism.

## 3. Image-backed scatter plot

The creator describes placing a half-court image beneath a scatter plot.

The shot data provides X and Y locations. The scatter plot positions each shot on the court.

The technical requirements include:
- Coordinate bounds and scaling.
- Matching image and plot aspect ratio.
- Correct court orientation.
- Axis visibility or suppression as appropriate.
- Point size and transparency for dense areas.
- Filtering by shot type and zone.

The exact formulas and axis settings are not available.

## 4. Filters and measures

The creator describes changing between:
- All shots.
- Two-pointers.
- Three-pointers.
- Different shot zones.

The statistics and shot chart update to reflect the selected granularity. The screenshot shows player metrics compared with team and NBA benchmarks.

The exact DAX measures and filter model are not available.

## 5. Data and image dependencies

The community entry cites:
- GitHub NBA player data.
- GitHub NBA shot data.
- Kaggle player image data.
- Kaggle NBA logo image data.
- NBA logo image asset.

The exact source files and refresh path have not been inspected. Image and logo licensing should be checked independently before reusing assets.

## 6. Source access and unknowns

No downloadable PBIX or source repository was confirmed. A community commenter asked for the PBIX, but the inspected sources do not establish that the file was shared.

Not inspected:
- Semantic model.
- Relationships.
- Power Query.
- DAX.
- Report JSON.
- Theme JSON.
- Bookmark definitions.
- Visual formatting.
- Accessibility settings.
- Runtime performance.

## 7. Future validation

If the PBIX becomes available:
1. Identify the exact card visual and version.
2. Inspect the two measures and layout visibility states.
3. Determine how left/right navigation changes the visible state.
4. Inspect the button/list slicer settings and selected state.
5. Inspect the scatter plot's X/Y bounds and background image configuration.
6. Test all shot-type and zone filters.
7. Check the player/team/NBA comparison measures.
8. Verify keyboard access and alt text.
