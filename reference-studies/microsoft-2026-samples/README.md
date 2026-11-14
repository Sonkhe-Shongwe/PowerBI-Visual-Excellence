# REF-004 | AdventureWorks Sales (2026 refresh)

**Status:** Report definitions and embedded model inspected. Power BI Desktop validation pending.
**Evidence:** Official Microsoft PBIX and Microsoft Learn documentation.
**Progress:** Open audit. P2 remains at 50% with eight completed study records.

## Source

- [Official PBIX at the inspected commit](https://github.com/microsoft/powerbi-desktop-samples/blob/e2f326b09bb7df6890fff0ded9813a0d73677cd6/2026%20Power%20BI%20Samples%20Revamp/AdventureWorks%20Sales.pbix)
- [Microsoft Learn sample catalogue](https://learn.microsoft.com/en-us/power-bi/create-reports/sample-datasets)
- File size: 8,390,782 bytes. Verified Git blob: `97d8172c89c8b0a541e95a4e263391322013a13f`.

## Findings

The sample has one 1920 × 1080 Overview page, ten analytical or filter visuals, seven line shapes and ten saved mobile placements. A native card contains seven measures and changes to a vertical stack in the phone layout. The report applies SoftDark over the Fluent 2 base theme.

The embedded semantic model contains ten tables, nine relationships, twenty explicit measures and two calculation groups. A Date Role calculation group switches the reporting date between order, due and ship date. A separate Time Intelligence calculation group applies period calculations to base measures.

## Study documents

- [Study notes](STUDY_NOTES.md)
- [Page architecture](PAGE_ARCHITECTURE.md)
- [Visual system](VISUAL_SYSTEM.md)
- [Technical notes](TECHNICAL_NOTES.md)
- [Transferable patterns](TRANSFERABLE_PATTERNS.md)

## Desktop validation still to run

1. Open the pinned PBIX. Record the Desktop version, capture Overview and Model view, and inspect the donut centre value, labels and chart spacing.
2. Exercise the date picker's calendar, range and relative modes. Compare counts after switching the Date Role slicer and verify which visuals respond.
3. Select a map bubble and a donut segment, test cross-filtering and tooltip content, then clear the selections. Record the rendered map state and any settings that block it.
4. Review phone layout, contrast, labels, alternative text, focus order and keyboard operation. Record representative Performance Analyzer timings.
5. Capture outcomes and any evidence gaps before closing REF-004 or assigning a benchmark score. A refresh test, if needed, requires an accessible workbook source.

## Licensing and reuse

The Microsoft sample repository has a root MIT licence. However, Microsoft's sample documentation separately states that sample workbooks and related data are the property of obviEnce, LLC, and that use requires the stated attribution, including the `obviEnce ©` notice for workbooks and visualisations.

Do not assume the repository's root MIT licence grants unrestricted rights to every embedded sample asset. Keep the PBIX and extracted sample data out of this research repository. Verify the exact terms before reusing any asset, data or implementation in a personal project.
