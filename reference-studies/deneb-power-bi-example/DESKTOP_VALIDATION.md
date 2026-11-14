# REF-010 Desktop Validation Register

**Status:** Pending. No test in this register has been run.
**Purpose:** Verify the creator-described report and capture the actual implementation rather than infer it from the README.

## Before opening

- [ ] Download the PBIX from the [creator repository](https://github.com/BruntBroccoli/Deneb-Power-BI-Example).
- [ ] Record Power BI Desktop version and build.
- [ ] Record Deneb visual version for every instance.
- [ ] Confirm whether the visual is AppSource-certified or standalone.
- [ ] Note any missing visual, migration, or compatibility warnings.
- [ ] Check the workbook discrepancy: README says `Spicy_Data.csv`; repository tree contains `Spicy_Data.xlsx`.

## Report and model inspection

- [ ] Confirm actual page count, names, hidden pages and canvas dimensions.
- [ ] Capture each page at 100% zoom.
- [ ] Inspect model tables, relationships, measures and Power Query steps.
- [ ] Record the number of Deneb visual instances and the provider used (Vega or Vega-Lite).
- [ ] Export/copy each Deneb specification to a local study file for analysis; do not publish or reuse it without permission.
- [ ] Record the Values data role and dataset grain for each Deneb visual.

## Visual behaviour

- [ ] Taxonomy donut: verify categories, aggregation, labels, legend, sorting and overlay construction.
- [ ] Taxonomy donut: verify default tooltip and report-page tooltip.
- [ ] Taxonomy donut: verify drillthrough from a resolvable mark.
- [ ] Dynamic-marker bar: identify the marker's exact measure/field, calculation and scale.
- [ ] Dynamic-marker bar: test filters, slicers, zero, blank, negative and outlier cases.
- [ ] Tolerance-zone spectrum: identify threshold source, units, band definitions and boundary behaviour.
- [ ] Tolerance-zone spectrum: test values below, at, inside and above each boundary.
- [ ] Tooltip page: identify invoking visuals, fields, page size and tooltip content.
- [ ] Drillthrough page: verify retained filter context and navigation back.

## Power BI integration

- [ ] Test slicer/filter changes and visual refresh.
- [ ] Test right-click context menu and data-point resolution.
- [ ] Test cross-filtering only if configured; record selected and unselected styling.
- [ ] Test bookmark restoration if the report uses bookmarks.
- [ ] Verify behaviour after switching pages and returning.

## Quality and performance

- [ ] Check visual labels, contrast, colour semantics and readability at normal zoom.
- [ ] Check keyboard focus, tab navigation and tooltip alternatives.
- [ ] Record SVG or Canvas rendering mode.
- [ ] Capture Performance Analyzer timings for representative interactions.
- [ ] Test with the report's normal data volume and a larger test selection if possible.
- [ ] Record clipping, text overflow, slow updates and visual errors.

## Evidence record

For every test, record:
- Result: Pass / Fail / Blocked / Not applicable.
- Screenshot or exact observation.
- Deneb and Desktop versions.
- Relevant specification or model field.
- Defect, cause and proposed correction.

Do not mark the study source-level or runtime-validated until the PBIX internals and the relevant tests have actually been inspected.
