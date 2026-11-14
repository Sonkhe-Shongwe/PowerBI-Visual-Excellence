# REF-005 | Sales and Returns

**Study status:** Description-led study documented. The official PBIX is available, but its binary contents and Desktop behaviour have not been inspected.
**Evidence type:** Microsoft Learn documentation, the Microsoft Fabric Community report tour, the official GitHub PBIX listing, and one official Microsoft Learn screenshot.
**Date checked:** 2026-11-14
**Study priority:** Medium. This is an interaction and report-journey reference, not a modern visual-design benchmark.

## Sources

- [Microsoft Learn: Explore the Sales and Returns sample report](https://learn.microsoft.com/en-us/power-bi/create-reports/sample-sales-returns)
- [Microsoft Fabric Community: Take a Tour of the New Sales and Returns Sample Report](https://community.fabric.microsoft.com/blog/fbc_pbiupdatesblog/take-a-tour-of-the-new-sales--returns-sample-report/5175940)
- [Official PBIX: Sales & Returns Sample v201912.pbix](https://github.com/microsoft/powerbi-desktop-samples/blob/main/Sample%20Reports/Sales%20%26%20Returns%20Sample%20v201912.pbix)
- [Microsoft sample catalogue](https://learn.microsoft.com/en-us/power-bi/create-reports/sample-datasets)
- [Microsoft sample repository licence](https://github.com/microsoft/powerbi-desktop-samples/blob/main/LICENSE)
- [Official report screenshot on Microsoft Learn](https://learn.microsoft.com/ja-jp/power-bi/create-reports/media/sample-datasets/sales-returns-sample-pbix.png)

## Summary

The sample uses a fictional company selling Microsoft-themed skateboards. Its report is intended to help readers understand the state of sales and returns, investigate product and store performance, explore return-rate scenarios, and connect findings to operational action.

The creator tour documents five main pages: Intro, Net Sales, Returns, Return Rate, and Market Basket Analysis. Additional hidden pages support tooltips and other report elements.

The strongest learning value is the journey from business overview to product-level analysis and scenario-based action. The report demonstrates bookmark-based alternate views, report-page tooltips, drillthrough, What-if analysis, AI-assisted exploration, custom visuals, Power Apps integration, and mobile layout planning.

## Study documents

- [Study notes](STUDY_NOTES.md)
- [Page architecture](PAGE_ARCHITECTURE.md)
- [Visual system](VISUAL_SYSTEM.md)
- [Technical notes](TECHNICAL_NOTES.md)
- [Transferable patterns](TRANSFERABLE_PATTERNS.md)

## Evidence boundaries

The official PBIX is listed in Microsoft's public repository at approximately 6.23 MB. The binary was not opened or parsed during this study, and Power BI Desktop runtime checks were not performed. Technical details below are therefore limited to what Microsoft and the report creators explicitly describe, plus clearly labelled observations from the published screenshot.

No benchmark score is assigned. The available evidence is insufficient for a full visual, functional, accessibility, or performance assessment.

## Licensing and reuse

The Microsoft sample repository contains a root MIT licence. Microsoft's sample documentation separately states that the sample workbooks and related data are the property of obviEnce, LLC, are provided for internal reference purposes, and require the stated attribution. The workbook and visualisations must carry the notice obviEnce ©.

Do not treat the repository-level MIT licence as blanket permission to redistribute the PBIX, reuse the sample data, or publish copied report assets in a portfolio. Keep the PBIX out of this research repository. Verify the applicable terms or obtain permission before any external reuse.

## Next inspection

Open the official PBIX in Power BI Desktop after the REF-004 validation pass. Record the Desktop version, page list, hidden pages, model, custom visual dependencies, bookmark states, drillthrough behaviour, What-if calculations, phone layout, accessibility, and representative performance timings.
