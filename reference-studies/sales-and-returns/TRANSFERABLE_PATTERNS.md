# Transferable Patterns

These are candidate patterns derived from the creator's report description. They are not tested implementations.

| Pattern | Use it when | Design and engineering checks |
|---|---|---|
| State, diagnosis, scenario, action | A report must move from an overview to investigation and then support a decision | Keep each stage focused; make the next analytical step discoverable; do not force every detail onto the overview |
| Mirrored summary pages | Two related business subjects need the same reading pattern, such as sales and returns | Keep layout and navigation consistent while changing metric definitions and semantic labels |
| Bookmark-driven alternate views | A chart and a table, or a chart and a map, answer related questions | Label both states, show the active state, preserve filters, and ensure keyboard users can reach the controls |
| Product-level drillthrough | A reader needs to move from a category result to a product investigation | Preserve selected product and date context, make the destination explicit, and provide a clear route back |
| What-if scenario control | A user needs to understand the effect of changing an assumption | Show baseline, assumption, scenario result, and incremental impact together; state units and avoid presenting a scenario as a forecast certainty |
| Contextual report-page tooltips | A chart needs additional detail without permanently increasing page density | Keep tooltip content concise, avoid making essential information hover-only, and test keyboard and touch alternatives |
| Guided interaction hints | A report has controls or interactions that may not be self-evident | Explain the interaction where it is used; make the help discoverable and avoid long animated instructions that delay access |
| Insight-to-workflow connection | A report identifies an operational opportunity that can trigger a business process | Make permissions, ownership, validation, and audit trail explicit; keep the action separate from the analytical evidence |
| Dedicated phone composition | A desktop report has several side-by-side analytical components | Reorder by decision priority, not by simply shrinking the desktop canvas; inspect the full phone scroll |

## Patterns to apply cautiously

- **Custom visuals:** use them only when their analytical value justifies the dependency. Check licensing, certification, privacy, tenant policy, mobile support, and fallback behaviour.
- **AI visuals:** treat Key Influencers, Decomposition Tree, and distribution insights as optional exploration. They should not replace a clear primary narrative or validated analysis.
- **Power Apps:** integrate an action only when the target organisation has a working app, correct permissions, and a defined operational owner.
- **Animated tooltips:** use them to explain a genuinely non-obvious interaction, not as decoration or a substitute for clear labels.

## What not to copy

- Do not copy the Microsoft/obviEnce branding, skateboard product artwork, logos, report assets, or sample data.
- Do not assume that a 2019 sample's preview-feature dependencies represent current Power BI defaults.
- Do not adopt a custom visual just because it appears in the sample.
- Do not use an untested What-if measure as a financial forecast.
- Do not treat the creator's description of mobile or accessibility intent as proof of a successful accessibility audit.

## Potential use in original projects

The strongest transferable lesson is the report journey, not the skateboard theme. An original analytics report can use a concise overview, a focused diagnostic page, a controlled scenario, and a clearly owned action step. The exact pages and interactions must be chosen for the user's dataset, audience, and decision.
