# REF-008 — SQL Radar: Study Notes

**Creator:** Aanor Le Gouic  
**Original source:** https://community.fabric.microsoft.com/discussions/pbi_contestsgallery/bnc---finalist---sql-radar-%C2%B7-find-the-signal-before-the-alarm/5372173  
**Creator's LinkedIn post:** https://lnkd.in/gmfGS-eX  
**Study date:** 2026-11-13  
**Status:** Description-led study; PBIX attachment listed but not downloaded/opened

## Executive finding

SQL Radar is a three-page operational monitoring report that moves from early signal detection to diagnosis and then action.

The creator starts with a key premise: no SQL system has crossed a critical threshold, but several are drifting. The report therefore focuses on threshold, headroom and drift status rather than waiting for a system to become critical.

Its three pages are:
1. Signal — where are the problems?
2. Diagnosis — why is it moving?
3. Action — what do we do first?

The creator explicitly separates the architecture:
- Native Power BI visuals carry the data and interactions.
- HTML carries the experience: the zooming map, animated timelines, identity cards and intro.

A page-level assistant appears on every page. In light mode it is Mercury, a drop of liquid metal; in dark mode it becomes Glitch, a pixel bug. Both are described as summarising the page and answering a few questions.

## 1. Competition context

The community entry identifies SQL Radar as Aanor Le Gouic's Barcelona finale report. In a public LinkedIn post, the creator says the report was developed over one week and rebuilt live on stage in 20 minutes.

The community post lists a 2.1 MB screenshot and a 903 KB PBIX attachment named BCN Finale 2026.pbix. A community commenter explicitly thanks the creator for sharing the PBIX.

The PBIX attachment listing is confirmed, but the file has not been downloaded or opened in this environment. No licence or separate source-code repository was confirmed.

## 2. Report purpose

The report is built around three operational questions:
- Where are the problems?
- Why is the system drifting?
- What should be done first, and by when?

The opening premise is important: a system can remain below its critical threshold while still moving away from normal. SQL Radar is designed to surface that drift early.

## 3. Page 1 — Signal

**Question:** Where are the problems?

The creator describes:
- A pill table showing each system's threshold, headroom and drift status.
- Three charts showing what is moving.
- A map showing where the systems are located.

The purpose is to identify which systems deserve investigation before they cross a critical threshold.

The exact chart types and map implementation are not specified beyond the creator's statement that HTML is used for a map that zooms to the selected site.

## 4. Page 2 — Diagnosis

**Question:** Why is it moving?

For the selected system:
- A timeline shows when each metric moved outside its August normal.
- A table compares every metric with the last assessment.
- The table checks whether the change is new, explained or shared with another system.
- Native visuals include report-page tooltips.
- The selected system and its context remain connected to the page.

This page moves from identifying drift to investigating its timing and possible context.

The creator does not specify the exact method used to define August normal or classify a deviation as explained/shared.

## 5. Page 3 — Action

**Question:** What should we do first, and by when?

The creator describes:
- A criticality-versus-signal matrix.
- A runway timeline.
- A ranking of systems.
- A plan with an action and deadline for each system.
- A one-click action that sends the brief by email.

The page turns the diagnostic findings into an operational response.

The exact ranking formula, runway calculation and email implementation are unknown.

## 6. Hybrid visual architecture

The creator deliberately splits the work in two.

### Native visuals

Native Power BI visuals handle:
- Data presentation.
- The table that filters the page.
- Charts.
- The criticality-versus-signal matrix.
- Report-page tooltips.

### HTML experience layer

HTML is used for:
- Map that zooms to the selected site.
- Animated timelines.
- Identity cards.
- Introductory experience.

This is an explicit architectural decision, not an assumption based on screenshots.

## 7. Mercury and Glitch assistant

The creator describes an assistant on every page:
- Mercury appears in light mode and summarises the page in one sentence and answers a few questions.
- Glitch appears when the light is switched off, presenting the same insights with a different personality.

The implementation is not available. Do not assume the assistant uses a generative AI model; the post does not describe its technical mechanism.

## 8. Evidence inspected

| Evidence | What it supports | Confidence |
|---|---|---|
| Microsoft Fabric Community entry | Three pages, table, charts, map, timeline, matrix, action plan and HTML/native split | High |
| Community attachment listing | 2.1 MB screenshot and 903 KB PBIX named BCN Finale 2026.pbix | High |
| Community reply | A commenter thanks the creator for sharing the PBIX | High |
| Creator's public LinkedIn post | One-week development and 20-minute live rebuild; public report link | High |
| PBIX internals | Not downloaded/opened | Not assessed |
| Screenshot contents | Attachment listed, but image not visually inspected | Not assessed |
| Runtime behaviour | Not tested | Not assessed |

## 9. Critical evaluation

### Strengths

- Detects drift before critical thresholds are crossed.
- Makes headroom and drift status explicit.
- Separates signal detection, diagnosis and action.
- Uses a selected-system timeline and assessment history for investigation.
- Combines native visuals for data interactions with HTML for a distinctive experience.
- Report-page tooltips add detail without permanently crowding the page.
- Ends with actions and deadlines rather than leaving the operator with a list of alerts.
- Mercury/Glitch personas give the assistant a recognisable identity.

### Trade-offs and questions

- Drift needs a clearly defined baseline and a defensible tolerance.
- The table must explain threshold, headroom and drift status in plain language.
- The criticality-versus-signal ranking needs transparent logic.
- The runway timeline needs clear assumptions and a readable time scale.
- An email action should be traceable and should not send an incomplete or misleading brief.
- A page-level assistant should distinguish source-backed information from its own interpretation.
- HTML components and animation introduce a custom visual/rendering dependency.
- Light/dark mode should preserve contrast and not change the meaning of status colours.

## 10. Benchmark status

**No numerical benchmark score assigned.**

The creator's description is rich enough to study the report's information architecture and implementation philosophy. The actual visual system, PBIX implementation, accessibility and runtime behaviour remain unverified.

## 11. Next action

Retrieve and inspect BCN Finale 2026.pbix if a compatible file-download path is available. Verify the page layouts, native visual interactions, HTML components, map zoom, animated timelines, Mercury/Glitch state, email action and report-page tooltips.
