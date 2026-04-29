# Pipeline Pillars

Four foundational concerns that any multi-step image-to-deliverable pipeline must address. Skip a pillar and the pipeline produces inconsistent results, lost assets, or unrepeatable wins.

## Pillar 1 — Aesthetic Lock

The single biggest determinant of pipeline output quality is whether the aesthetic register is *locked* early and reused consistently.

### What "Aesthetic Lock" Means

- A **style reference** that downstream prompts can consume — Midjourney `--sref`, Nano Banana reference image, Ideogram style preset, Flux.2 IP-adapter image.
- A **named parameter stack** that goes onto every Midjourney prompt for a given project (see [`frameworks/midjourney/parameter-stacks.md`](../frameworks/midjourney/parameter-stacks.md)).
- A **moodboard** that is the single source of visual truth for the project (see [`frameworks/midjourney/moodboards.md`](../frameworks/midjourney/moodboards.md)).

### How to Establish It

1. Generate 16–24 candidates against a generic-but-directional prompt for the project register.
2. Pick the 3–5 strongest candidates that share a visual through-line.
3. Either capture their `--sref` codes (Midjourney) or save them as a reference-image set (Nano Banana, Flux.2).
4. From this point forward, *every* prompt in the project carries the locked references. No exceptions.

### Failure Modes

- **Drift across the project.** Hero plates, character portraits, and supporting assets feel like they came from different visual universes. Cause: each prompt was written from scratch without the locked references. Fix: enforce a project-template prompt that always includes the references.
- **Over-locked.** The lock is so tight that nothing varies; every image looks identical. Cause: too few `--sref` codes, too high `--sw`, no creative range. Fix: use 3–5 sref codes and `--sw 50–100`, not a single sref at `--sw 1000`.

## Pillar 2 — Character Library

When the project includes recurring characters, personas, or subjects, those subjects need a reusable reference library — not a re-prompt-from-scratch each time.

### What's in the Library

- **Reference images** for each character (3–8 images per character: front, three-quarter, profile, full body, varying expressions).
- **A short text description** of the character that travels with every prompt ("a woman in her late 30s with short dark hair, neutral expression, dressed in a navy blazer and ivory shirt").
- **The model-specific reference handle**: a Midjourney `--oref` URL with `--ow` value, a Nano Banana reference-image set name, a Flux.2 IP-adapter slot.

### How to Build It

1. Generate the character once, with high-quality output and multiple angles.
2. Save those images to a versioned location with a stable URL (cloud storage, project bucket).
3. Document the model-specific reference handle in a project README.
4. Every subsequent prompt referencing that character pulls from the library.

### Failure Modes

- **Character drift.** Same character looks subtly different in each shot. Cause: re-prompting from text alone. Fix: always use the stored reference image with `--oref` (Midjourney) or grounded prompt (Nano Banana).
- **Real-person leak.** The character starts looking like a recognizable celebrity. Cause: prompt language echoing a public figure. Fix: composite/archetypal language only; never name real people.

See [`frameworks/midjourney/omni-reference.md`](../frameworks/midjourney/omni-reference.md) and [`frameworks/nano-banana/framework-d-grounded-prompts.md`](../frameworks/nano-banana/framework-d-grounded-prompts.md) for model-specific implementations.

## Pillar 3 — Asset Management

Every generated asset, every composite, every motion clip lives in a versioned, traceable location with provenance metadata. No `v3-final-final-v2.png`.

### Minimum Requirements

- **A folder structure per project** with separate directories for raw generations, finalized stills, composites, and motion outputs.
- **Versioned filenames** using semantic notation: `[project]-[asset-name]-v[N]-[YYYY-MM-DD].[ext]`. Example: `bhil-locus-cover-v3-2026-04-15.png`.
- **Per-asset metadata** stored alongside the asset: prompt text, model and parameters used, sref/oref references, generation date, and SynthID/C2PA signature status.
- **A project asset index** (a single CSV or a Notion table) listing every asset with metadata.

### Why It Matters

- **Reproducibility.** Six months later, when a client requests a similar asset for a follow-up project, the prompt and references are recoverable.
- **Provenance.** When a delivery is questioned (legal, AI-disclosure, brand-compliance), the metadata chain proves what was generated, by what model, with what inputs.
- **Composite traceability.** A whitepaper hero composite carries metadata for both the MJ background and the Ideogram typography layer, so any single layer can be regenerated or replaced.

### Failure Modes

- **The "winning" prompt is lost.** A particularly good generation came out of a chaotic in-thread iteration; the exact prompt is buried in chat history; reproducing it later is impossible. Fix: at the moment a frame is selected as a final, copy the full prompt and parameters into the asset metadata.
- **Composites lose their layer sources.** A finalized composite is delivered but the source layers (MJ texture + Ideogram type) are not preserved. Fix: archive every layer with the composite.

## Pillar 4 — Orchestration

The human directs. The models execute. Multi-step pipelines fall apart when the human tries to make a single model do too many steps, or when steps are skipped because they "should be obvious."

### What Good Orchestration Looks Like

- **Explicit step boundaries.** Each step in the pipeline produces a defined deliverable that can be inspected before the next step. Don't chain four model calls and only inspect the final output.
- **Human-in-the-loop checkpoints.** After aesthetic lock, after character generation, after composition lock — the human reviews and confirms before promoting to the next stage.
- **One prompt, one purpose.** Don't try to write a single prompt that produces "a cinematic establishing shot, a portrait of the analyst, and a close-up of the document." Three separate prompts, three separate generations, composited if needed.

### The Orchestration Sequence (Default)

For a typical multi-asset BHIL project:

1. **Concept lock** — moodboard, written brief, brand-direction confirmation.
2. **Aesthetic lock** — generate the style reference, capture `--sref` codes.
3. **Character library** — generate and archive any recurring subject references.
4. **Iterate** — fast iteration in Nano Banana to lock composition and lighting per asset.
5. **Promote** — re-prompt the winning composition in MJ v7 or Flux.2 Pro for hero quality.
6. **Composite** — Figma layer work for typography, brand marks, color correction.
7. **Animate** (optional) — Veo 3.1 or Runway Gen-4 for motion deliverables.
8. **Archive** — every asset and metadata stored to the project library.
9. **Deliver** — composite outputs, plus source layers and metadata, handed to client.

### Failure Modes

- **The pipeline becomes one giant chat session.** Steps blur, the human stops directing, the model leads. Fix: explicit step boundaries, human review at each.
- **The human tries to one-shot.** "Just give me the final hero plate from one prompt." Possible occasionally, but unrepeatable. Fix: trust the multi-step pipeline; the time spent in Nano Banana iteration saves time later in MJ regeneration.
- **The human forgets to write down what they did.** A great asset is delivered but no one can describe how it was made. Fix: pipeline checkpoints with documented metadata.

## Putting the Pillars Together

A mature BHIL project pipeline always demonstrates all four pillars. A signal that a pipeline is healthy:

- The project README documents the locked aesthetic, character library, and folder structure.
- Every generated asset's filename and metadata are traceable to the prompt that produced it.
- The recipes used (A, B, C, or D from this directory) are documented as part of the project plan.
- The human directing the project can answer "show me the source for this hero plate" within thirty seconds.

## Related

- [`workflows/README.md`](./README.md)
- [`workflows/nano-banana-veo-loop.md`](./nano-banana-veo-loop.md)
- [`workflows/recipe-a-midjourney-runway.md`](./recipe-a-midjourney-runway.md)
- [`workflows/recipe-b-nano-banana-to-midjourney.md`](./recipe-b-nano-banana-to-midjourney.md)
- [`workflows/recipe-c-typography-compositing.md`](./recipe-c-typography-compositing.md)
- [`workflows/recipe-d-long-form-narrative.md`](./recipe-d-long-form-narrative.md)
- [`frameworks/midjourney/personalization.md`](../frameworks/midjourney/personalization.md)
- [`frameworks/nano-banana/synthid-c2pa.md`](../frameworks/nano-banana/synthid-c2pa.md)
