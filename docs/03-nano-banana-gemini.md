# 03 · Nano Banana / Gemini Overview

This document is the high-level orientation for Google's Gemini image generation stack — the family of models that ships under the umbrella name "Nano Banana." The full deep-dive lives in [`../frameworks/nano-banana/`](../frameworks/nano-banana/).

---

## The model lineup (April 2026)

| Model | Identifier | Released | Positioning | Cost (approx.) |
| :--- | :--- | :--- | :--- | :--- |
| **Nano Banana** | `gemini-2.5-flash-image` | August 2025 | Fast, cheap, 1K baseline | ~$0.039/image |
| **Nano Banana Pro** | `gemini-3-pro-image-preview` | November 2025 | Professional studio quality. Always-on "thinking," up to 4K, best-in-class text rendering | ~$0.134 (2K) / $0.24 (4K) |
| **Nano Banana 2 (NB2)** | `gemini-3.1-flash-image-preview` | February 2026 | Pro-class quality at ~50% of Pro's cost; default in Gemini app, Search, Lens | (between NB and Pro) |

### The BHIL routing rule

> Ideate in Midjourney, finalize text-heavy deliverables in Nano Banana Pro, and use NB2 as the everyday workhorse.

- **NB2** is the default for almost all BHIL production work, iteration, and conversational editing.
- **Pro** is reserved for: final 4K deliverables, print-resolution covers, long or multilingual in-image text, and any work where maximum fidelity matters.
- **NB (2.5)** is legacy. Use only for very cost-sensitive volume or pre-Pro iteration where 1K is acceptable.

---

## SynthID + C2PA watermarking

All three models carry an invisible **SynthID watermark** on every output. Pro and NB2 also embed **C2PA Content Credentials**.

SynthID cannot be stripped without destructive re-encoding. **Treat it as a feature for an intelligence brand**, because any client auditing with SynthID tooling will be able to verify AI provenance.

The operational consequence: **disclose AI use in methodology notes by default.** The watermark makes non-disclosure untenable anyway, and getting ahead of the disclosure question is a brand-positive position for an intelligence consultancy.

Full guidance in [`../frameworks/nano-banana/synthid-c2pa.md`](../frameworks/nano-banana/synthid-c2pa.md).

---

## What Nano Banana can do that Midjourney cannot

| Capability | Detail |
| :--- | :--- |
| **Up to 14 reference images** | Pro: 6 objects + 5 characters; NB2: 10 objects + 4 characters |
| **Resolutions to 4K** | NB2 only. Pro maxes at 2K for typical use |
| **Extended aspect ratios** | 1:4, 4:1, 1:8, 8:1 banners (NB2) |
| **Google Search grounding** | Pro + NB2 — real-world fact-checking inside the prompt |
| **Google Image Search grounding** | NB2 only, April 2026 |
| **Configurable thinking levels** | NB2: minimal / high |
| **Reasoning-driven world knowledge** | Gemini 3's reasoning gets historical insignia, technical schematics, and geographic details right where pure diffusion models hallucinate |
| **Multi-turn conversational editing** | Mask-free, in-thread, with `thought_signature` preserved across turns |

### Important constraints

- **No transparent-PNG output** on any Gemini image model. Request "pure white background" and key out downstream.
- **Gemini does not accept Midjourney-style parameters.** Use the API's `imageConfig.aspectRatio` and `imageConfig.imageSize` (uppercase strings: `"1K"`, `"2K"`, `"4K"`).
- **Grounded Image Search on NB2 cannot search for people.**

---

## The prompting register

Nano Banana rewards **speech, not tags.**

- Start with a strong verb: `Generate`, `Edit`, `Combine`, `Replace`, `Translate`, `Restore`, `Focus on`.
- Speak in full sentences — narrative paragraphs outperform tag strings in every Google benchmark.
- Leverage world knowledge explicitly. Gemini 3's reasoning is the lever; ignoring it produces output indistinguishable from a smaller model.
- Use multi-turn chat for edits rather than regenerating.
- Quote text you want rendered.
- For long or layered text, converse first to refine the copy, then ask for the image.
- On the raw REST API, preserve `thought_signature` across turns. The official Google GenAI SDK handles this automatically via `chats.create()`.

---

## The five core frameworks

Each framework has a dedicated document with the formula, the worked example, and the failure modes:

| # | Framework | Document |
| :--- | :--- | :--- |
| A | Text-to-image | [`../frameworks/nano-banana/framework-a-text-to-image.md`](../frameworks/nano-banana/framework-a-text-to-image.md) |
| B | Reference-based / multi-image fusion | [`../frameworks/nano-banana/framework-b-multi-image-fusion.md`](../frameworks/nano-banana/framework-b-multi-image-fusion.md) |
| C | Conversational editing (mask-free) | [`../frameworks/nano-banana/framework-c-conversational-editing.md`](../frameworks/nano-banana/framework-c-conversational-editing.md) |
| D | Real-time / grounded prompts | [`../frameworks/nano-banana/framework-d-grounded-prompts.md`](../frameworks/nano-banana/framework-d-grounded-prompts.md) |
| E | Text + typography | [`../frameworks/nano-banana/framework-e-typography.md`](../frameworks/nano-banana/framework-e-typography.md) |

---

## When to choose Nano Banana vs Midjourney

### Choose Midjourney for

- Default beauty
- Cinematic aesthetic
- Mood discovery
- Any work where the Sref or moodboard system is your primary brand lock

### Choose Nano Banana for

- Controllability
- Editability
- Multi-image reference fidelity
- Accurate in-image text
- Real-world grounding
- Multi-turn edits
- Any API-driven production pipeline

---

## Where to go next

- Full Nano Banana framework: [`../frameworks/nano-banana/README.md`](../frameworks/nano-banana/README.md)
- Compare to Midjourney: [`02-midjourney.md`](02-midjourney.md)
- The Nano Banana → Veo 3.1 motion loop: [`../workflows/nano-banana-veo-loop.md`](../workflows/nano-banana-veo-loop.md)
