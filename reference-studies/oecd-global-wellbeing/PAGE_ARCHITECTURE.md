# REF-006 — Page Architecture

**Source:** Creator's Microsoft Fabric Community description  
**Status:** Two-page purpose and interaction structure documented; runtime inspection pending

## Report-level structure

The creator describes two pages:
1. A domain-oriented well-being overview.
2. A gender-disparity analysis.

## Page 1 — Well-being domains

**Purpose:** Compare selected OECD well-being domains and inspect country-level results.

The creator describes three key domains with three measures each.

For each measure, the report presents:
- Global average.
- Dynamic colour-coordinated SVG progress bar.
- Trend by year with anomaly detection.
- Country table sorted highest to lowest.

### Interaction

- A domain button opens a dropdown to change the selected domain.
- Each domain changes the background colour and accent image.
- Page and visual titles/subtitles update dynamically.
- Selecting a country cross-filters the SVG progress bar and trend to that country.

### Page architecture lesson

The report reuses the same component pattern for multiple measures and domains. The selected domain changes the context and visual identity, while the reader continues to recognise the same progress/trend/table structure.

## Page 2 — Gender disparity

**Purpose:** Compare selected gender-related measures across countries.

The creator says the page uses:
- Small multiples.
- Dynamic titles.
- Dynamic subtitles.

The intention is to make differences between male and female averages easier to compare across countries.

The exact number of charts, measures, layout and axes are not specified in the available description.

## Related weighted-composite interaction

A related Reddit discussion about the live OECD challenge describes:
- A composite normalised score based on six metrics.
- User-adjustable metric weights through sliders.
- Top countries and continents.
- Share of countries improving.
- Country ranking by composite score or improvement.

The creator's community post does not describe this interaction explicitly. It may be another part of the same report or a related live-finale view. Keep it outside the confirmed page map until verified.

## Analytical flow

The source supports this reader journey:
1. Select a well-being domain.
2. Compare the global average and trend for each measure.
3. Select a country.
4. Inspect that country's progress and trend.
5. Move to gender-disparity analysis and compare country differences.

## Unknowns

Not available from the inspected source:
- Exact page names and page dimensions.
- Canvas layout and visual coordinates.
- Exact measures and their units.
- Progress-bar denominator and scale.
- Anomaly detection method and settings.
- Exact colour palette and accent images.
- Filter synchronisation and navigation behaviour.
- Whether weighted composite sliders are part of the published report.
- PBIX, DAX, TMDL and theme implementation.

Do not infer these details from the text description alone.
