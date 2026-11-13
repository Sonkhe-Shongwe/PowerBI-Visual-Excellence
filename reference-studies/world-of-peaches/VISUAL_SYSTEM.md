# REF-001 — Visual System

**Source:** The World of Peaches theme JSON, component HTML/CSS, report configuration and public screenshots  
**Status:** Source-level analysis complete; runtime rendering pending

## 1. Overall visual direction

The report uses an editorial, warm, subject-specific identity rather than a generic corporate dashboard style.

Its visual language combines:
- Peach, burnt-orange and muted gold accents.
- Deep brown and taupe navigation/surface colours.
- Warm off-white and white content surfaces.
- Dark, restrained text.
- Serif display typography with a clean sans-serif interface font.
- Photography and selected motion to reinforce the subject matter.

The identity is consistent across the overview, production and trade pages.

## 2. Core palette

The first colours in the theme's data colour sequence are:

| Role / use | Colour |
|---|---|
| Primary peach accent | #C96A3A |
| Light peach accent | #E8906A |
| Warm gold accent | #D4892A |
| Deep brown | #3D2F28 |
| Taupe | #8C7B6B |
| Muted green | #6B8F5E |
| Theme background | #FCFCFC |
| Theme foreground | #202020 |
| Table accent | #CECECE |

The component DAX also uses supporting colours such as #6B5D52, #F0EBE4, #F5EFE6, #D5CEC7, #4A7A3B and #C44B3F.

The palette is not just decorative. Green and red are used for positive/negative movement in selected KPI components, while the peach accent marks the report identity and important controls.

## 3. Typography

The HTML components reference:
- **Jost** for interface text, labels and body copy.
- **Cormorant Garamond** for selected display headings and prominent values.

The theme's native Power BI text classes use Segoe UI. This is an important implementation distinction: custom HTML components can load their own web fonts, while native visuals follow the Power BI theme's font settings.

### Transferable typography lesson

Use a small, deliberate type system:
- Display face for a limited number of high-emphasis elements.
- Sans-serif face for labels, controls, data and explanatory copy.
- Stable hierarchy for page title, component title, KPI, label and supporting text.

Do not introduce several display fonts or use decorative typography for dense analytical labels.

## 4. Layout and component treatment

The report uses a 1280 × 720 canvas with a stable sidebar and a main analytical area.

Observed component styling includes:
- 12–16 px rounded corners on major HTML cards.
- 16 px gap in the KPI row.
- 24 px internal padding in prominent components.
- Light dividers instead of heavy borders.
- Layered image overlays to keep text legible over photography.
- Restrained shadows and subtle hover treatments.
- Consistent spacing between headings, labels and values.

The overview uses a prominent KPI row above lower analytical content. Production uses a wide KPI row above two main analysis panels. Trade uses a three-column editorial composition: narrative insight, central chart/map and a right-side KPI tower.

## 5. Theme JSON as a reusable component system

The theme is named Peach.Themee.

The inspected JSON contains 28 visual-style groups, including actionButton, pageNavigator, slicer, advancedSlicerVisual, cardVisual, lineChart and shapeMap.

The action-button styles include named variants such as Brand, Surface and Brand Soft, with separate default, hover, selected and disabled states. The page navigator includes styles such as Sidebar Navigation and Underline.

This is a valuable design-system lesson: a Power BI theme can define more than a categorical colour list. It can establish repeatable defaults and component treatments for native visuals.

## 6. Custom component examples

### KPI row

The KPI row uses a larger image-backed hero card and smaller supporting cards. Its HTML/CSS uses a 16 px gap, rounded surfaces, hover overlays and a controlled hierarchy between label, main value and contextual change.

### Overview trend chart

The trend chart is rendered as HTML/SVG. Its source includes an animated line-draw effect, a subtle pulse and a custom tooltip treatment. It can change the displayed metric based on the report's metric selector.

### Production waffle

The production component uses a 10-column dot grid, with each dot representing a percentage of a whole. The CSS defines separate active and inactive dots, a pager and hover overlays. The component supports a Waffle/Table view concept.

### Trade insight

The trade insight component combines a video background, dark overlay, narrative headline, contextual explanation and hover treatment. The moving background is part of the editorial storytelling rather than a standard chart.

## 7. Motion and imagery

Observed source patterns include:
- Trend-line drawing.
- Pulsing chart markers.
- Dot entrance animation in the waffle component.
- Hover overlays.
- Image fade and slow drift.
- A video background in the trade insight component.

The creator's public process note says motion should be earned and should not compete with the data. This is a useful principle to retain.

For our own reports, motion should be used only when it explains a transition, highlights a meaningful change or reinforces a narrative. It should not be added merely to make a report look more advanced.

## 8. Accessibility and readability

The creator's community post states that the report includes alt text on visuals, logical tab order, WCAG-compliant contrast and guided tutorials. The source contains alt-text measures for visual components and tab-order values in visual configuration.

These are positive design signals, but actual accessibility must be verified in Power BI Desktop:
- Inspect alt text in the Selection/Accessibility settings.
- Navigate the report using the keyboard.
- Check reading order.
- Test text contrast and font sizes at the target display size.
- Confirm that meaning is not communicated through colour alone.
- Consider users who prefer reduced motion.

## 9. Critical observations

### Strong decisions

- One recognisable visual identity across pages.
- A consistent sidebar and filter position.
- Clear contrast between display typography and analytical typography.
- Component-level styling rather than ad hoc formatting.
- A small number of deliberate accent colours.
- Subject-specific imagery that reinforces the report topic.

### Trade-offs to keep in mind

- Custom HTML visuals need a supported renderer and may not behave like native visuals in every environment.
- External web fonts, images, video and icons can fail when offline or blocked.
- Small labels need careful testing at realistic display sizes.
- Heavy image use can make a report more editorial but may be unsuitable for operational reporting.
- Motion can create distraction or accessibility issues when used without purpose.

## 10. What we should carry forward

Adopt the discipline of a shared design system, consistent page shell, restrained palette, purposeful type hierarchy and reusable component specifications.

Do not copy the peach palette, imagery or branding into unrelated projects. The transferable lesson is the design method and consistency, not the subject-specific skin.
