# 02 · Midjourney v7 Overview

This document is the high-level orientation for Midjourney as a BHIL production engine. The full deep-dive — parameter tables, Sref library curation, Omni-Reference workflow, moodboards, personalization, and BHIL default parameter stacks — lives in [`../frameworks/midjourney/`](../frameworks/midjourney/).

---

## Production baseline

| Version | Status (April 2026) | Use |
| :--- | :--- | :--- |
| **v7** | Default since June 17, 2025 | The BHIL production baseline |
| **v8 alpha / v8.1 alpha** | Web-only (March 2026 / April 2026) | Not production-stable. Do not use for client deliverables. |
| **v6.1** | Legacy | Only when you need `--cref` character reference or older `--sref` codes authored against the v4 style interpreter |

Pin `--v 7` explicitly in shared prompts. Treating "current version" as "current version" creates silent drift the moment Midjourney promotes a new default.

---

## What changed from v6

V7 is **not a keyword engine.** V6 rewarded comma-soup ("beautiful, cinematic, 8k, masterpiece, trending on artstation"). V7 punishes it.

V7 parses prompts as full natural-language sentences organized into a descriptive hierarchy. Writing for Midjourney now means writing like a cinematographer drafting a shot list, not like an SEO copywriter stacking keywords.

The practical implication: lift-and-shifted v6 prompts will work in v7, but they will not approach v7's ceiling. Rewriting old prompts as natural-language paragraphs is the highest-ROI single intervention you can make on a legacy MJ workflow.

---

## The core formula

```text
[SUBJECT] [SUBJECT DETAILS], [CONTEXT], [STYLE/MEDIUM],
[TECHNICAL — camera / lens / lighting / medium]
--parameters
```

**Descending weight hierarchy:** Subject → Subject Details → Context → Style/Medium → Technical → Parameters.

- Lead with what you see, not what you want.
- Medium at the start or end of the prompt carries more weight than medium in the middle.
- The effective attention window is roughly 30–80 tokens; anything past 150 tokens rarely changes the output.
- Avoid: actor names (uncanny valley), quality filler ("8k, masterpiece"), and contradictory modifiers.

The full parameter deep-dive is in [`../frameworks/midjourney/parameters.md`](../frameworks/midjourney/parameters.md).

---

## Where Midjourney wins for BHIL

- **Default beauty** — the v7 model has the strongest aesthetic prior of any 2026 flagship.
- **Cinematic register** — chiaroscuro, anamorphic, editorial-realism prompts produce extremely consistent results.
- **Mood discovery** — the four-grid output is a generative mood-board engine.
- **Sref / moodboard system** — the only flagship with a first-class persistent style system. This is the operational spine of any brand-consistent practice.

---

## Where Midjourney is the wrong tool

- **In-image typography of any complexity.** Use Ideogram v3 or Nano Banana Pro and composite in.
- **Real-world grounding.** No web search; no fact-checked geographical detail. Use NB2 + Google Search grounding for anything that has to be right about real places.
- **Multi-image fusion with role assignment.** Sref does style only. For "use Image 1 as subject, Image 2 as environment, Image 3 as palette" — go to Nano Banana.
- **Strict edit fidelity.** MJ's vary and remix tools are blunt instruments compared to Nano Banana's mask-free conversational editing.
- **Air-gapped / on-prem workflows.** Use Flux.2 [dev] or [klein].

---

## The four BHIL default parameter stacks

Defined in full in [`../frameworks/midjourney/parameter-stacks.md`](../frameworks/midjourney/parameter-stacks.md):

| Use Case | Stack (abbreviated) |
| :--- | :--- |
| Report cover | `--v 7 --style raw --s 75 --ar 2:3 --p [bhil] --no text, watermark, logo` |
| Editorial punch | `--v 7 --s 200 --exp 15 --ar 3:2 --p [bhil] --sref [codes] --sw 120` |
| Framework diagram | `--v 7 --s 300 --exp 15 --ar 16:9 --p [bhil-framework] --sref [codes] --sw 150` |
| Portrait | `--v 7 --style raw --s 100 --ar 4:5 --p [bhil-portrait] --oref [URL] --ow 150` |

Replace `[bhil]`, `[bhil-framework]`, `[bhil-portrait]`, and `[codes]` with the live values from the BHIL brand vault before running.

---

## Key workflows

| Workflow | Document |
| :--- | :--- |
| Character consistency (V7) | [`../frameworks/midjourney/omni-reference.md`](../frameworks/midjourney/omni-reference.md) |
| Character consistency (V6.1 fallback) | Same document, V6.1 section |
| Style consistency / Sref library | [`../frameworks/midjourney/sref-library.md`](../frameworks/midjourney/sref-library.md) |
| Moodboards | [`../frameworks/midjourney/moodboards.md`](../frameworks/midjourney/moodboards.md) |
| Personalization (`--p`) | [`../frameworks/midjourney/personalization.md`](../frameworks/midjourney/personalization.md) |

---

## Where to go next

- Full Midjourney framework: [`../frameworks/midjourney/README.md`](../frameworks/midjourney/README.md)
- Compare Midjourney to Nano Banana: [`03-nano-banana-gemini.md`](03-nano-banana-gemini.md)
- Universal cinematographer's vocabulary: [`../reference/README.md`](../reference/README.md)
