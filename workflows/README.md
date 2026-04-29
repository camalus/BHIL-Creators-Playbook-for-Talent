# Workflows

Cross-platform pipelines that take generated stills and turn them into deliverables. Image generation is a single step in a multi-step production. This directory documents the canonical multi-step pipelines used by BHIL and adapted by every serious creative team working with the current model lineup.

## Files

| File | What's in it |
| :--- | :--- |
| [Pipeline Pillars](./pipeline-pillars.md) | The four foundational concerns of any multi-step image-to-deliverable pipeline: aesthetic lock, character library, asset management, orchestration. |
| [Nano Banana → Veo 3.1 Loop](./nano-banana-veo-loop.md) | The seven-step loop for taking a Nano Banana still into a Veo 3.1 motion deliverable, then back into a still, with consistency. |
| [Recipe A — Midjourney → Runway](./recipe-a-midjourney-runway.md) | Generate stills in Midjourney, animate selected frames in Runway Gen-4. Cinematic-cinema register. |
| [Recipe B — Nano Banana → Midjourney](./recipe-b-nano-banana-to-midjourney.md) | Use Nano Banana for fast iteration and character lock; promote winning frames to Midjourney for hero finals. |
| [Recipe C — Typography Compositing](./recipe-c-typography-compositing.md) | Generate texture in MJ + typography in Ideogram, composite in Figma. The canonical typographic deliverable pipeline. |
| [Recipe D — Long-Form Narrative](./recipe-d-long-form-narrative.md) | Multi-frame narrative work: storyboarding, character lock across shots, sequence delivery. |

## When to Use Which

| If the deliverable is... | Pipeline |
| :--- | :--- |
| Single still hero plate | Single-model pipeline (use the relevant `frameworks/` model directly) |
| Cinematic motion clip from a still | Recipe A (MJ → Runway) or Nano Banana → Veo 3.1 |
| Iterative multi-frame work with character lock | Recipe B (Nano Banana → MJ) or Nano Banana → Veo 3.1 |
| Typographic deliverable (whitepaper hero, poster) | Recipe C (typography compositing) |
| Multi-shot narrative or storyboard | Recipe D (long-form narrative) |

## The Four Pipeline Pillars

Every multi-step pipeline rests on four pillars (detailed in [`pipeline-pillars.md`](./pipeline-pillars.md)):

1. **Aesthetic Lock** — establish the visual register early and lock it (Midjourney `--sref` / Nano Banana reference image / Ideogram style preset).
2. **Character Library** — when characters or recurring subjects appear, store reference images and reuse them via `--oref`, character reference, or grounded prompts.
3. **Asset Management** — every asset (still, motion, composite, brand variant) lives in a versioned location with provenance metadata. No "v3-final-final-v2.png" filenames.
4. **Orchestration** — the human directs the pipeline. The models execute steps. Don't try to make the model orchestrate itself.

## The Daily Workhorse Pattern

For most BHIL projects, the daily pattern is:

1. **Iterate fast in Nano Banana** (NB2 model) — generate 8-12 candidates with conversational refinement, lock the composition and lighting register.
2. **Promote the winner to Midjourney v7** (or Flux.2 Pro for finals) — re-prompt with the locked `--sref`, `--oref`, and parameter stack to produce the hero asset.
3. **Composite in Figma** — overlay typography, brand marks, and any secondary elements.
4. **Animate selected frames in Veo 3.1 or Runway Gen-4** — for motion deliverables.
5. **Archive everything to a versioned asset library** with the prompts, references, and SynthID/C2PA provenance.

## Disclosure & Provenance

Every motion or still output that includes Nano Banana, Veo 3.1, or any C2PA-signing model carries embedded provenance metadata. **Do not strip C2PA signatures during compositing.** When delivering to clients, hand over both the composite and the original generation source, with prompts and reference images, in the asset archive. See [`frameworks/nano-banana/synthid-c2pa.md`](../frameworks/nano-banana/synthid-c2pa.md).

## Related

- [`frameworks/`](../frameworks/) — model-by-model documentation referenced throughout these workflows.
- [`prompts/`](../prompts/) — every prompt indicates which workflow recipe it pairs with.
- [`reference/`](../reference/) — the cinematographer's vocabulary used in every pipeline step.
- [`docs/06-advanced-workflows.md`](../docs/06-advanced-workflows.md) — narrative overview.
