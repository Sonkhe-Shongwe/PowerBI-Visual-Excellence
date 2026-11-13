# REF-009 — Power BI Basketball Cards: Study Notes

**Creator:** Injae Park  
**Original source:** https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/winner-of-week-3--power-bi-basketball-cards/4600448  
**Official winner announcement:** https://community.fabric.microsoft.com/blog/community_blog/%F0%9F%8F%86-power-bi-dataviz-world-championships--week-3-winner-%F0%9F%8E%89/4606956  
**Creator walkthrough:** https://www.linkedin.com/posts/injae-park_powerbi-dashboarddesign-sportsanalytics-activity-7345811931527589888-DF7M  
**Study date:** 2026-11-13  
**Status:** Screenshot- and walkthrough-led study; PBIX/source inspection pending

## Executive finding

Power BI Basketball Cards is an interactive sports report built around NBA player selection, a flippable player card and a shot-location chart.

The creator says the report uses Power BI core visuals only, without custom visual add-ons. The walkthrough explains the core construction:
- Button slicer or list slicer for navigation.
- Player headshots and team logos for visual selection.
- Two measures in a card visual for front and back states.
- Layout visibility to show only one side of the card at a time.
- Left/right buttons to switch the visible card.
- A half-court image placed underneath a scatter plot.
- X/Y shot coordinates to position each shot.
- Filters for all shots, two-pointers, three-pointers and different zones.

This is a valuable example of how native Power BI visuals can be combined to create a distinctive, app-like experience without relying on third-party custom visuals.

## 1. Competition and data context

Microsoft's official Week 3 announcement names Injae Park as the winner for Power BI Basketball Cards.

The creator's entry states that the report uses 2022–2023 NBA league and shot statistics. The cited source materials include:
- GitHub NBA player data.
- GitHub NBA shot data.
- Kaggle player image data.
- Kaggle NBA logo image data.
- NBA logo image asset.

The exact data model, refresh path and licensing of player images/logos have not been inspected.

## 2. Screenshot observations

The public screenshot shows a light, card-based layout:
- A vertical player-selection list with headshots on the left.
- A selected-player card in the centre.
- A team logo used as a watermark behind the player image.
- Player name, position and headline statistics on the card.
- Supporting KPI cards comparing player performance with team and league benchmarks.
- A half-court shot chart on the right, with individual shot locations represented by points.
- A clear shot-filter state at the top of the chart.

The published screenshot shows Stephen Curry selected, with a 49% field-goal percentage, 1,391 points and 1.23 points per shot. These values are screenshot-specific and should not be treated as a complete player profile.

The screenshot provides evidence of the visible composition, but not the full report's page dimensions, spacing system or responsive behaviour.

## 3. Creator-described interactions

### Player and team navigation

The creator describes using a button slicer or list slicer. Images include team logos and player headshots. The user can choose a team and player, then inspect the selected player's statistics.

### Flippable player card

The creator explains that the card uses two measures in a card visual:
- One measure supplies the front side.
- Another measure supplies the back side.

Only one card is shown at a time through layout visibility. Left and right buttons let the reader switch between the two states.

This is an important distinction: the flip is described as a visibility/state transition, not a custom visual animation.

### Shot-location chart

The creator describes placing an image of half a basketball court underneath a scatter plot. The shot dataset supplies X and Y coordinates, so the points appear in their correct court positions.

The reader can switch between:
- All shots.
- Two-point shots.
- Three-point shots.
- Different court zones.

Statistics update for the selected shot group and its granularity.

### Player comparisons

A later creator walkthrough describes choosing a team and player, then flipping the card to see performance against team or NBA context and different shot preferences. The exact comparison layout is not fully documented in the source material inspected here.

## 4. Evidence inspected

| Evidence | What it supports | Confidence |
|---|---|---|
| Official Microsoft Week 3 announcement | Winner status and judges' recognition of creativity, design and interactivity | High |
| Creator's Microsoft Fabric Community entry | 2022–2023 NBA data, core visual design approach, flippable card, navigation and shot representation | High |
| Creator's LinkedIn walkthrough transcript | Button/list slicer, two card measures, layout visibility, left/right switching and scatter plot over court image | High |
| Published screenshot | Player list, card, KPI comparison and half-court shot-chart composition | High for the shown state |
| Community feedback | Praise for clean navigation; one comment notes player headshots crop foreheads | Anecdotal |
| PBIX and source code | Not confirmed as publicly available | Not assessed |
| Runtime behaviour | Not tested | Not assessed |

## 5. Critical evaluation

### Strengths

- The report has a memorable, subject-appropriate visual metaphor.
- Player selection is image-led and contextual.
- The card flip reveals more information without requiring a separate page.
- The shot chart uses spatial coordinates to communicate where attempts occurred.
- Player performance is compared against team and league context.
- The creator uses native Power BI visuals rather than a third-party visual dependency.
- The visible composition is clean and easy to scan.

### Trade-offs and questions

- Player images can be cropped poorly; one community commenter specifically noted cut-off foreheads in the player cards.
- Image-heavy selection can be harder to navigate for users who do not recognise player faces or team logos.
- The flip interaction needs an obvious state indicator and accessible alternative.
- A scatter plot over a court image requires careful coordinate calibration and consistent aspect ratio.
- Shot filters and player selection can create dense interaction logic; titles and labels must make the current selection obvious.
- Player images, team logos and NBA assets have separate licensing considerations.
- Without the PBIX, exact DAX and layout visibility configuration cannot be confirmed.

## 6. Benchmark status

**No numerical benchmark score assigned.**

The screenshot and walkthrough support a useful study of interaction and composition, but not a complete audit of the report's technical implementation or accessibility.

## 7. Next action

If a PBIX becomes available, verify the front/back card measures, visibility states, button slicer, player selection, shot filters, X/Y coordinate mapping and keyboard operation. The purpose is to understand the technique, not reproduce the sports report.
