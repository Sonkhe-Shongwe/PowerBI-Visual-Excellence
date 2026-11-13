# REF-006 — Technical Notes

**Source:** Creator's Microsoft Fabric Community description and a related Reddit discussion  
**Status:** Descriptive technical analysis only; PBIX/source inspection pending

## 1. Confirmed from creator description

The report includes:
- Three well-being domains.
- Three measures per domain.
- Dynamic SVG progress bars for global averages.
- Year trends with anomaly detection.
- Country tables sorted highest to lowest.
- Country selection that cross-filters the SVG and trend.
- A domain button that opens a dropdown.
- Dynamic domain background colour and accent image.
- Dynamic page and visual titles/subtitles.
- A second page using small multiples for gender disparities.

## 2. SVG progress bars

The creator explicitly describes the progress bars as dynamic SVGs.

This confirms that SVG is part of the visual approach. It does not establish:
- Whether the SVG is generated in DAX.
- Whether it is returned from a measure or column.
- Whether an HTML custom visual is used.
- Whether the SVG is rendered through a native image URL or another technique.
- How the progress-bar scale is calculated.

Do not assume a specific implementation until the PBIX or source code is available.

## 3. Trend and anomaly detection

The creator describes a trend by year that uses anomaly detection to find possible explanations for deviations from expected values.

The exact implementation is unknown. It may use a Power BI visual capability, a custom calculation or another analytical method. The community post does not specify which.

An anomaly can identify an unusual observation, but it does not prove the cause of the deviation.

## 4. Cross-filtering

The creator states that selecting a country cross-filters the SVG and trend to the selected country.

This confirms a coordinated interaction between the country table and other components. The precise filter relationships and interaction settings are not available.

## 5. Dynamic domain styling

The selected domain changes the background colour, accent image and title/subtitle styling. The exact method for applying these changes is unknown.

Potential implementation approaches include measures and conditional formatting, bookmarks or visual-level state changes, but none should be assumed without inspecting the PBIX.

## 6. Related weighted-composite description

A Reddit post about the live OECD challenge describes a normalised composite score based on six metrics and user-adjustable sliders that amplify or reduce each metric's contribution.

It also describes:
- Top countries and continents.
- Percentage of countries improving.
- Rankings by score or improvement.

This is not fully corroborated by the creator's Microsoft Fabric Community post. Treat it as a related reported capability, not a confirmed technical feature of the published report.

If verified, the important technical questions would be:
- How are the six metrics normalised?
- Are weights constrained to sum to 100%?
- How are blank metrics handled?
- Can users set all weights to zero?
- Are ranks recalculated dynamically?
- How are ties resolved?
- Does the composite score remain interpretable when weights change?

## 7. Source access and unknowns

The creator's community post contains a Power BI embed token, indicating a report embed reference. A separate PBIX download and source repository were not confirmed.

Not inspected:
- Semantic model.
- DAX measures.
- Power Query.
- TMDL.
- Relationships.
- Theme JSON.
- SVG source.
- Visual configuration.
- Bookmark states.
- Runtime performance.
- Accessibility.

## 8. Next technical verification

If the report or PBIX becomes available:
1. Inspect the domain selector and its state.
2. Identify the SVG generation method.
3. Inspect the anomaly detection implementation.
4. Verify country cross-filtering.
5. Inspect small-multiple settings.
6. Confirm whether the weighted composite is part of the same report.
7. Test dynamic titles, colours and accessibility.
