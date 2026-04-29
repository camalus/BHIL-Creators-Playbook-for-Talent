# 06 · Advanced Workflows Overview

The 2026 competitive edge is not the model — it is the pipeline. Every flagship now produces broadcast-grade output. The studios that beat any single tool are the ones that route each task to its strongest engine and keep brand discipline intact across the chain.

This document is the orientation for [`../workflows/`](../workflows/), where the four pillars and the cross-platform recipes live in detail.

---

## The four pillars of a repeatable pipeline

A production pipeline has four pillars. Without all four, you have an ad-hoc creative practice that uses AI; with all four, you have a production system.

| Pillar | What It Is | Why It Matters |
| :--- | :--- | :--- |
| **Aesthetic Lock** | The Midjourney Sref and moodboard library, treated as an approved design system — versioned, named, access-controlled | Without this, every consultant renders in a slightly different register. Brand coherence dies in the prompt. |
| **Character Library** | 4–8 archetypal figures BHIL uses across deliverables (analyst, briefing client, field operator, board chair). Each with a Nano Banana character sheet, a Midjourney `--oref` URL, a Runway saved reference, and voice/persona notes | Every deliverable that features a recurring figure needs the same figure. Ad-hoc character generation creates visual fragmentation. |
| **Asset Management** | All images tagged by scene type, character, sref code, and aspect ratio. Video clips named `BHIL_[deliverable]_[scene#]_[model]_[take#]_v[N]`. Prompts, seeds, references, and model versions retained in metadata. | The unglamorous differentiator. Six months later, a different team member must be able to reproduce any deliverable from the archive. |
| **Orchestration** | A node-based pipeline built once as a Runway Workflow (or equivalent) and reused per deliverable | Repeatability turns AI from a creative tool into a production system. |

> **The archive is the differentiator.**
> Every finished deliverable should be reproducible from the pipeline, six months later, by a different team member. That is the difference between a consultancy that uses AI and one that has operationalized it.

Full detail in [`../workflows/pipeline-pillars.md`](../workflows/pipeline-pillars.md).

---

## The headline workflow — Nano Banana → Veo 3.1

The Nano Banana → Veo Loop collapses the traditional storyboard → key art → animatic → final pipeline into seven repeatable steps. Nano Banana locks composition, lighting, and identity as still frames (cheap, fast to iterate). Veo handles only motion interpolation and audio between two already-correct anchor frames.

This is the **highest-leverage division of labor** currently available for intelligence-brand short-form video — LinkedIn explainer reels, embedded briefing videos, conference presentation cutaways.

### The seven steps

1. Establish the character sheet (NB Pro / NB2)
2. Generate the START keyframe
3. Generate the END keyframe
4. Feed both frames to Veo 3.1 "First and Last Frame"
5. Draft, select, refine
6. Chain clips via Scene Extension
7. Polish and brand-finish (Runway Aleph)

Each step is documented in [`../workflows/nano-banana-veo-loop.md`](../workflows/nano-banana-veo-loop.md), including the Veo motion-prompt formula and audio directive conventions.

---

## The video model lineup (April 2026)

| Model | Status | Use |
| :--- | :--- | :--- |
| **Google Veo 3.1** | Flagship | First / last-frame conditioning, audio, the BHIL motion default |
| **Veo 3.1 Lite** | Released April 3, 2026 | Cost-efficient drafting |
| **Runway Gen-4.5** | Released December 2025 | When MJ stylistic register is needed; image-to-video |
| **Kling 3.0** | Released February 2026 | 15-second continuous, native 4K, strong physics |

> **DO NOT BUILD ON SORA 2.**
> OpenAI announced shutdown on March 24, 2026. The app closes April 26, 2026; the API closes September 24, 2026. Any pipeline that depends on Sora 2 is on a clock.

---

## The four cross-platform recipes

| Recipe | When to use | Path |
| :--- | :--- | :--- |
| **A — Midjourney → Runway** | When MJ's distinctive aesthetic is needed and Nano Banana can't match it. Editorial illustration, painterly realism, fine-art registers. | [`../workflows/recipe-a-midjourney-runway.md`](../workflows/recipe-a-midjourney-runway.md) |
| **B — Nano Banana → Midjourney** | When you want NB's rapid conversational iteration for composition, but MJ's final aesthetic polish | [`../workflows/recipe-b-nano-banana-to-midjourney.md`](../workflows/recipe-b-nano-banana-to-midjourney.md) |
| **C — Ideogram + MJ Compositing** | Deliverables requiring legible on-image typography. Ideogram for type, MJ for scene, compositing in Figma or Photoshop | [`../workflows/recipe-c-typography-compositing.md`](../workflows/recipe-c-typography-compositing.md) |
| **D — Long-form Narrative (Kling + Veo)** | Deliverables longer than 8 seconds where physics realism and dialogue both matter | [`../workflows/recipe-d-long-form-narrative.md`](../workflows/recipe-d-long-form-narrative.md) |

---

## Where to go next

- Pipeline pillars in detail: [`../workflows/pipeline-pillars.md`](../workflows/pipeline-pillars.md)
- The headline NB → Veo loop: [`../workflows/nano-banana-veo-loop.md`](../workflows/nano-banana-veo-loop.md)
- The other 2026 flagships at a glance: [`07-other-models.md`](07-other-models.md)
