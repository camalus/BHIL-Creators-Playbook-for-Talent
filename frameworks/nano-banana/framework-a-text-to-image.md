# Framework A — Text-to-Image (Narrative Paragraph)

The default Nano Banana generation pattern. A single descriptive paragraph that reads like a shot list.

## The Formula

```text
[Subject] + [Action] + [Location/Context] + [Composition] + [Style]
```

The guiding principle from Google's official prompting guide: **describe the scene, don't list keywords.** A narrative paragraph outperforms a tag string in every benchmark Google has published. This is the inverse of v6-era Midjourney prompting and a frequent failure mode for operators bringing comma-soup habits across.

## Why Prose Beats Tags on Gemini

The model parses prose through the same reasoning stack that handles long-context document analysis. A sentence like *"a composed woman in her late 40s stands in three-quarter profile at a glass-walled situation room, leaning forward to point at a map node"* gives the model: subject identity, age, posture, framing, location, action, and implicit lighting inference (situation rooms are dim). The same content as tags — *"woman, 40s, three-quarter, situation room, pointing, map"* — discards the structural relationships the model uses to plan composition.

The thinking step (always-on in Pro, configurable in NB2) treats the prompt as a brief, plans the layout, and then renders. Prose provides the brief; tags don't.

## Anatomy of a Working Prompt

Start with **subject and action**, then layer downward. The first sentence anchors what the image is "about" — anything later refines.

| Layer | Example |
| :--- | :--- |
| Subject + Action | "An intelligence analyst in her late 30s reviews three large translucent world maps projected on glass." |
| Location / Context | "She is at a dimly lit workstation, leaning forward, index finger pointing at a node over the Black Sea." |
| Lighting | "Cool monitor glow on her left cheek, single warm desk lamp behind her, dramatic chiaroscuro." |
| Camera / Lens | "Shot on Fujifilm medium-format with a 50mm lens, f/2.0, shallow depth of field, faint film grain." |
| Color / Style | "Muted teal-and-amber color grade, documentary-realism aesthetic." |
| Composition | "16:9 horizontal, 2K, subject centered with negative space to her right." |

Stitched together, this becomes a single 80–120 word paragraph that produces a consistent, on-brand result on the first or second render.

## Default BHIL Style Block

Every text-to-image prompt for a BHIL deliverable should land in roughly this register. Adapt the subject and scene; keep the style register stable.

```text
... shot on a [Hasselblad medium-format / Fujifilm X-T5 / Leica Q3] with
a [50 / 85 / 35]mm lens, f/[1.9–2.8], natural depth of field, [muted
teal-and-amber / bleach-bypass / desaturated editorial] color grade,
documentary realism. [16:9 / 4:5 / 2:3] aspect, 2K. Editorial restraint
— no oversaturation, no HUD chrome, no text overlays unless specified.
```

## Length and Token Discipline

The effective sweet spot is **80–150 words per prompt**. Under 50 words, the model invents details inconsistently. Over 200 words, late content gets attenuated and you start contradicting earlier instructions without realizing.

If a prompt naturally wants to go past 150 words, split into two: a generation prompt and a follow-up edit prompt. This is faster, cheaper, and produces more controllable output than one mega-prompt.

## Strong Verbs at the Front

Lead with one of: **Generate, Create, Produce, Render**. The model is more reliable when the prompt's intent is unambiguous from the first three words. *"A woman stands at a desk..."* is technically a description; *"Generate a photograph of a woman standing at a desk..."* is an instruction. The instruction form performs better.

For edit operations, see [Framework C](./framework-c-conversational-editing.md) — the verb set there is `Edit, Replace, Translate, Restore, Focus on, Combine`.

## Worked Example — Executive Briefing Hero

```text
Generate a high-contrast editorial portrait of an intelligence analyst
in her late 30s at a dimly lit workstation, reviewing three large
translucent world maps projected on glass. She is leaning forward,
index finger pointing at a node over the Black Sea. The scene is
illuminated by cool monitor glow and a single warm desk lamp,
creating dramatic chiaroscuro. Shot on a Fujifilm medium-format
camera with a 50mm lens, f/2.0, shallow depth of field, faint film
grain. Muted teal-and-amber color grade. Documentary-realism
aesthetic. 16:9 horizontal.
```

API config: `aspect_ratio: "16:9"`, `image_size: "2K"`, model: `gemini-3.1-flash-image-preview` for iteration / `gemini-3-pro-image-preview` for the finalized hero.

## Failure Modes

- **Generic register** — *"a beautiful woman"* / *"professional photo"*. Specificity is leverage; the playbook's Rule 1 applies harder on Gemini than on Midjourney.
- **Implicit assumptions** — *"a typical analyst at work"*. Whose definition of "typical"? Replace with concrete description.
- **Listing rather than narrating** — comma-soup tags from a different model's habits. Rewrite as prose.
- **Over-specifying contradictions** — *"shallow depth of field with everything in focus"* / *"dramatic chiaroscuro under softbox lighting."* The model resolves contradictions by averaging, which is rarely what you wanted.

## When This Framework Is Wrong

If the deliverable already has reference images (a real headshot, a brand palette card, an environmental reference), use [Framework B — Multi-Image Fusion](./framework-b-multi-image-fusion.md) instead. Framework A is for clean-slate generation.

If you're 80% of the way to a finished image and need to make a small change, use [Framework C — Conversational Editing](./framework-c-conversational-editing.md). Don't regenerate.

## Related

- [`framework-b-multi-image-fusion.md`](./framework-b-multi-image-fusion.md) — multi-reference generation.
- [`framework-c-conversational-editing.md`](./framework-c-conversational-editing.md) — multi-turn editing.
- [`framework-e-typography.md`](./framework-e-typography.md) — text-rendering specifics.
- [`prompts/02-framework-diagrams/06-pipeline-framework.md`](../../prompts/02-framework-diagrams/06-pipeline-framework.md) — production prompt using this pattern.
