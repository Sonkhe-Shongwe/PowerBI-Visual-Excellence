# REF-002 — Visual System

**Source:** Public screenshots, page background SVGs, theme resource, HTML/CSS templates and report visual configuration  
**Status:** Source-level review complete; runtime rendering pending

## 1. Overall visual direction

City Sustainability Scorecard uses a restrained, executive dashboard aesthetic:
- Dark textured left navigation rail.
- Light neutral analytical canvas.
- White/light content cards.
- Strong blue accent.
- Consistent title and context region.
- Clear metric labels and compact supporting descriptions.
- Subject-specific images in the metric-selection area.

The design is more restrained than the cinematic/editorial direction of REF-001. Its main visual goal is to make peer comparison and metric context easy to scan.

## 2. Canvas and shell

All six page sections specify a 1280 × 720 canvas.

The embedded page SVGs define:
- Base canvas colour around #EFEDED.
- Main content surface around #F7F7F9.
- Dark sidebar area 281 px wide.
- Rounded/curved main surface entering the content area from the sidebar.
- Embedded texture and page-specific elements.

The public screenshots show a dark navy/blue navigation treatment with a white content area. The SVG uses a black base rectangle plus a texture pattern for the navigation region; the rendered visual appearance is therefore influenced by the embedded image resource, not just the literal base fill.

## 3. Colour and typography

The report JSON references the Power BI base theme CY25SU11. The theme JSON contains standard Power BI visual defaults and a standard data-colour sequence.

The source tree does not expose a separate report-specific custom theme JSON. The report's distinct styling is also implemented through:
- Page-specific SVG backgrounds.
- Visual-level configuration.
- HTML/CSS component templates.
- DAX-generated colour and icon logic.

The inspected custom components use a strong blue accent such as #0066CC and dark navy surfaces such as #0A1628 and #0F1C2E. Supporting text uses muted greys and slate tones.

Typography references include system-ui, Segoe UI and Inter in HTML components. The templates generally favour standard UI fonts over decorative display type.

## 4. Layout and hierarchy

The report uses a repeated page shell and a clear hierarchy:
1. Persistent navigation.
2. Page title and selected city/metric/year context.
3. Headline KPI or performance insight.
4. Main analytical visual.
5. Supporting comparison cards, table or historical detail.

The main page layouts use repeatable spacing and component sizes. On the Performance page, the radar occupies the left side and a two-column stack of metric cards occupies the right. On Ranking, five equal-width metric columns create a strong comparison rhythm. Temporal Analysis uses repeated small-multiple line charts.

## 5. Component treatment

### KPI cards

The inspected Livability card template uses:
- White background.
- 10 px corner radius.
- 12–14 px padding.
- System UI typography.
- A primary value/label hierarchy.
- A hover transition that moves the card content away and reveals a contextual tooltip overlay.

This is a custom interaction pattern. It should be tested with keyboard and touch users before reuse; hover-only information can be inaccessible or undiscoverable on some devices.

### Radar chart

The Performance page radar chart is an SVG generated from DAX. The template uses:
- A 500 × 500 SVG viewBox.
- Five metric axes.
- Concentric 25%, 50%, 75% and 100% reference rings.
- A blue linear gradient fill.
- A subtle glow filter.
- Dynamic point coordinates derived from the five metric values.

This is a useful example of when SVG can produce a highly tailored visual while still responding to report filters.

### Insight panel

The Performance insight panel uses a restrained blue left border, rounded corners and a short narrative summary. It calls out strongest and weakest dimensions and gives the reader a sentence explaining the selected city's profile.

### Notifications panel

The notification panel uses a dark blue gradient surface, a stack of alert cards and staggered slide-in animation. This creates a notification centre without permanently adding another full analytical page.

### Navigation and overlays

The report uses a consistent left-side navigation system and bookmark-driven tutorial, filter and notification states. The design gives the reader a stable place to navigate while optional overlays explain the interface.

## 6. Motion

Source-level examples include:
- Hover card transitions.
- Notification cards that slide in with staggered delays.
- Video-led Welcome page.
- Animated interface transitions in HTML/CSS.

Motion can support attention and explain state changes, but should not be added to every component. For operational reporting, static and predictable behaviour may be more appropriate.

## 7. Accessibility and readability

The source includes 24 explicit alt-text measures and tab-order values in report visual configuration. The creator states that the report includes alt text, logical keyboard order and WCAG-compliant contrast.

These claims require runtime verification. In particular:
- Hover-only card details need an accessible alternative.
- Keyboard navigation should expose the same important information.
- Alt text should be concise and meaningful, not just a dump of every data point.
- Contrast should be checked on the actual rendered page.
- Motion should not be essential to understanding the report.
- Colour should not be the only way to communicate positive/negative performance.

## 8. Critical observations

### Strong design decisions

- Consistent shell and page navigation.
- Strong contrast between the dark navigation rail and light content area.
- A repeated layout for five metrics, which helps comparison.
- A radar chart supported by individual metric cards.
- Clear separation of rankings and temporal analysis.
- Contextual insight text rather than relying entirely on chart interpretation.

### Trade-offs

- The sidebar and decorative page backgrounds use embedded SVG/image resources, which are less flexible than fully native layout primitives.
- Hover-revealed card content may not work equivalently on touch or keyboard.
- A video-led welcome page and external image/video URLs introduce media dependencies.
- A large number of custom HTML components can increase maintenance effort.
- The report's base theme is not itself a bespoke visual design system; the report-specific identity is distributed across SVGs, visual settings and HTML/CSS.

## 9. What to carry forward

Adopt the consistent shell, restrained colour hierarchy, metric comparison grid, context-aware insight cards and clear separation of analytical page purposes.

Do not copy the exact city sustainability palette or use a radar chart simply because it looks impressive. Choose visuals based on the comparison task and audience.
