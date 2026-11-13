# Functional Test Register

Use this register for every report reconstruction and original portfolio report.

## Test status definitions

- **Not run:** no test evidence yet.
- **Pass:** expected behaviour was observed and evidence recorded.
- **Fail:** behaviour did not match expectation.
- **Blocked:** test could not be completed because of a dependency.
- **N/A:** not applicable, with a reason.

## Test matrix

| ID | Area | Test | Expected result | Status | Evidence / notes |
|---|---|---|---|---|---|
| F-001 | Navigation | Open every report page | Each page loads and navigation is consistent | Not run | |
| F-002 | Slicers | Change each slicer selection | Relevant visuals update correctly | Not run | |
| F-003 | Filter state | Combine multiple filters | Filter context is correct and understandable | Not run | |
| F-004 | Reset | Use clear/reset control | Report returns to documented default state | Not run | |
| F-005 | Cross-filter | Select a data point | Related visuals respond as intended | Not run | |
| F-006 | Drillthrough | Drill to detail page | Correct context is passed to target page | Not run | |
| F-007 | Bookmarks | Trigger each bookmark | Intended state is restored | Not run | |
| F-008 | Tooltips | Hover or select tooltip targets | Correct contextual information appears | Not run | |
| F-009 | Buttons | Activate buttons and links | Correct action occurs; no dead controls | Not run | |
| F-010 | Parameters | Change field / what-if parameter | Visual or measure responds correctly | Not run | |
| F-011 | Data correctness | Reconcile headline KPIs | Values match the underlying model and definitions | Not run | |
| F-012 | Formatting | Change filters and periods | Number formats, titles and labels remain correct | Not run | |
| F-013 | Accessibility | Review alt text and contrast | Key information remains accessible | Not run | |
| F-014 | Performance | Navigate and interact | No unacceptable delay or rendering failure | Not run | |
| F-015 | Layout | Inspect target canvas sizes | No clipping, overlap or unreadable labels | Not run | |

## Execution record

For each test run, record:
- Report name and version:
- Power BI Desktop version:
- Date:
- Tester:
- Test IDs executed:
- Pass / fail / blocked summary:
- Defects raised:
- Retest date:
- Evidence location:

A report is not functionally accepted while critical tests remain failed or untested.
