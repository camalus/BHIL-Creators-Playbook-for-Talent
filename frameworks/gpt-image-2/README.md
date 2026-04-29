# GPT Image 2 (OpenAI)

> Released April 2026. The strongest reasoning-integrated image model in the 2026 lineup. GPT Image 2 plans composition before rendering, which makes it the first-choice engine for complex infographics and dense diagrams — the deliverables where layout coherence matters more than aesthetic defaults.

## When to Choose GPT Image 2

| Use Case | Why GPT-2 Wins |
| :--- | :--- |
| Multi-element framework diagrams | Plans node placement, edge routing, and text spacing as a layout problem before rendering |
| Mock product / SaaS dashboard heroes | Coherent UI hierarchy across panels, navigation, and KPI cards |
| Dense infographics with multiple labeled regions | Holds label-to-element associations that diffusion-only models drop |
| Near-perfect in-image text in technical contexts | Reasoning step catches typos and label-collision before render |
| Edits requiring before-and-after constraint logic | Change / Preserve / Constraints pattern lands cleanly |

## When Not to Use GPT Image 2

- **Photographic editorial register** — Flux.2 Pro and Nano Banana Pro are stronger.
- **Painterly or stylized output** — Midjourney's stylize controls have no equivalent here.
- **Multi-turn brand-locked iteration** — Gemini's chat workflow is purpose-built; GPT Image 2's edit cycle is competent but less conversational.
- **Air-gapped client deployment** — closed model only.

## The Distinctive Operating Pattern: Long Descriptive Prose

GPT Image 2 is the most prose-rewarding model in the 2026 lineup. Comma-soup gets averaged-out worse than on Gemini; long narrative paragraphs get planned-through better than any other model.

Effective prompts often run **120–250 words** — longer than Nano Banana's sweet spot, and longer than any other current flagship rewards. The reasoning step uses the additional context to plan layout, label positioning, and element relationships.

## The Change / Preserve / Constraints Pattern (for Edits)

GPT Image 2's edit prompts work best when structured as three blocks:

```text
CHANGE:
- The headline should now read 'GRAY-ZONE SIGNALS' instead of 'OSINT Brief'
- The accent color should shift from amber to signal-red

PRESERVE:
- The dark navy background
- The world map at 15% opacity in the center
- All typography hierarchy (kicker, headline, subhead, footer)
- The aspect ratio (4:5)

CONSTRAINTS:
- No additional decoration
- No drop shadows or gradients
- All text must remain crisply legible
```

This pattern is more verbose than a Nano Banana edit prompt but produces tighter results on infographic and diagram work where preservation of layout is critical.

## Worked Example — Taxonomy Radial Diagram

```text
Create a 1:1 square radial taxonomy diagram titled 'BHIL Threat
Taxonomy' at top center.

A central circle labeled 'GEOPOLITICAL RISK' with eight branches
radiating outward, each ending in a labeled child node:
'State-Sponsored Cyber',
'Economic Coercion',
'Maritime Disruption',
'Information Warfare',
'Supply Chain Attack',
'Critical Infrastructure',
'Sanctions Evasion',
'Diplomatic Pressure'.

Connect the central node to each child with thin organic curves,
not rigid lines. Each child node is a small circle with the label
in a thin geometric sans-serif placed directly below.

Graphite background (#1A1D21), white nodes, single amber #C9A24A
highlight on the central circle. Generous whitespace; the diagram
should occupy roughly 75% of the canvas.

Flat editorial style, no drop shadows, no gradients, no 3D effects.
All text rendered crisply and legibly.
```

The structured, enumerated style — explicit nodes, explicit connections, explicit constraints — plays directly to GPT Image 2's strengths. A diffusion-only model would drop labels or collide them; GPT Image 2 plans the radial layout first.

## Capabilities Worth Knowing

- **Native text rendering at editorial quality.** Better than Midjourney; comparable to Nano Banana Pro on technical diagrams; slightly behind Pro on dense long-form copy.
- **Reasoning over composition.** The model can be prompted to *"Plan the layout before rendering"* and surface its plan in chat before generating, which gives a checkpoint for course-correction.
- **Strong at iconography sets.** Generating a coherent icon family (8 mono-line icons, same visual register) lands cleanly.
- **Reasonable mask-free editing.** Not as surgical as Flux.1 Kontext, but supports the Change / Preserve / Constraints edit pattern.

## Capability Limits

- **No native vector output.** Use Recraft V3 for true SVG.
- **No transparent-PNG output.** Same limitation as Gemini; key out downstream.
- **Limited multi-image reference fidelity.** Pass references; the model uses them, but Gemini's role-assignment workflow is tighter.
- **No air-gapped deployment.** API only.

## Reasoning-First Prompting

A pattern unique to reasoning-integrated models. Two-stage workflow for high-stakes diagrams:

1. **Plan turn**: *"Before generating, plan the layout for an 8-node radial taxonomy diagram with the labels [list]. Describe node positions, connection routing, and label placement. Don't generate yet."*
2. **Render turn**: *"Now generate the diagram per that plan. Render all labels crisply."*

The plan turn is roughly free in tokens. The reasoning step it triggers makes the eventual render dramatically more accurate. For complex deliverables, the two-turn pattern is fast and reliable.

## Failure Modes

- **Tag-soup prompts** — long prose is what works; tags get averaged.
- **Too-short prompts** — 50-word prompts under-utilize the reasoning step.
- **Asking for painterly aesthetic** — wrong tool. Route to Midjourney.
- **Skipping the Plan turn on complex diagrams** — the model can do it in one turn but fails more often than the two-turn pattern.
- **Expecting transparent PNG** — request white background and key out.

## Related

- [`docs/07-other-models.md`](../../docs/07-other-models.md) — chapter context.
- [`prompts/02-framework-diagrams/07-taxonomy-radial.md`](../../prompts/02-framework-diagrams/07-taxonomy-radial.md) — production prompt using GPT Image 2.
- [`prompts/04-data-intelligence-hero/16-saas-dashboard-hero.md`](../../prompts/04-data-intelligence-hero/16-saas-dashboard-hero.md) — dashboard hero using GPT Image 2.
