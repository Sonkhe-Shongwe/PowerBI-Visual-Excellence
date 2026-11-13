# REF-008 — Technical Notes

**Source:** Creator's Microsoft Fabric Community description and PBIX attachment listing  
**Status:** Descriptive technical analysis; PBIX internals not yet inspected

## 1. Native and HTML responsibilities

The creator explicitly describes a split architecture.

### Native Power BI visuals carry data and interactions

The creator identifies:
- Table that filters the page.
- Charts.
- Criticality-versus-signal matrix.
- Report-page tooltips.

### HTML carries the experience

The creator identifies:
- Map that zooms on the selected site.
- Animated timelines.
- Identity cards.
- Introductory experience.

This is a deliberate separation of analytical interaction and presentation layer.

## 2. Signal logic

The Signal page's pill table contains:
- Threshold.
- Headroom.
- Drift status.

The creator's premise is that systems may be drifting before they cross a critical threshold.

Unknown:
- How normal behaviour is defined.
- How headroom is calculated.
- How drift is classified.
- Whether drift uses slope, deviation, rolling average, control limits or another method.

## 3. Diagnosis logic

The selected-system timeline shows when each metric moved outside its August normal.

The table checks each metric against the last assessment and classifies whether the issue is:
- New.
- Explained.
- Shared with another system.

Unknown:
- Exact baseline calculation.
- How explanations are recorded or matched.
- How shared behaviour is detected.
- How missing assessments are handled.

## 4. Action logic

The creator describes:
- Criticality-versus-signal matrix.
- Runway timeline.
- System ranking.
- Action and deadline plan.
- One-click email brief.

Unknown:
- Matrix dimensions and score formula.
- Runway forecast method.
- Ranking weights.
- Email integration or automation mechanism.
- Whether the brief is generated as HTML, text or an attachment.

## 5. Assistant

The creator describes a page-level assistant that summarises the current page and answers a few questions:
- Mercury in light mode.
- Glitch in dark mode.

The technical implementation is unknown. The community post does not establish whether it uses static DAX responses, a custom HTML interaction, an external service or a generative AI model. Do not assume AI integration.

## 6. PBIX availability

The community entry lists:
- Screenshot attachment: 2.1 MB.
- PBIX attachment: BCN Finale 2026.pbix, 903 KB.

A community commenter explicitly thanks the creator for sharing the PBIX. The PBIX is therefore listed as publicly shared on the source page.

The attachment URL was not retrievable through the available browsing interface. The PBIX has not been downloaded, opened or inspected. No licence or separate source repository was confirmed.

## 7. Future technical verification

If the PBIX becomes available:
1. Inspect the semantic model and relationships.
2. Trace the threshold, headroom and drift calculations.
3. Inspect the timeline baseline and assessment comparison.
4. Identify the native visual and report-page tooltip configuration.
5. Inspect the HTML map, animation, identity cards and intro.
6. Determine how Mercury/Glitch state is controlled.
7. Inspect the matrix, runway and ranking logic.
8. Verify the email brief mechanism.
9. Test keyboard access, accessibility and Power BI Service rendering.
