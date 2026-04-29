# 04 · The Universal Creative Director Toolkit

This document is the orientation for [`../reference/`](../reference/), the four model-agnostic vocabulary tables that operationalize [Rule 3 — Talk like a cinematographer](01-foundational-rules.md#rule-3--talk-like-a-cinematographer).

The tables are:

| Table | Path | Options |
| :--- | :--- | :--- |
| **Lighting** | [`../reference/lighting.md`](../reference/lighting.md) | 8 |
| **Camera + Lens** | [`../reference/camera-and-lens.md`](../reference/camera-and-lens.md) | 10 |
| **Color + Film Stock** | [`../reference/color-and-film-stock.md`](../reference/color-and-film-stock.md) | 8 |
| **Materiality + Texture** | [`../reference/materiality-and-texture.md`](../reference/materiality-and-texture.md) | 9 |

---

## How to use the toolkit

### The mix-one-from-each rule

When constructing any prompt:

1. Pick **one lighting option**.
2. Pick **one camera + lens option**.
3. Pick **one color + film stock option**.
4. Pick **one materiality + texture option** (where the visual has a tangible surface — this can be skipped for purely typographic or vector work).

This is the fastest way to produce professional-grade results across every model in this playbook. Four constrained choices outperform four open-ended adjectives every time.

### Example

| Slot | Choice |
| :--- | :--- |
| Lighting | Cool monitor glow + warm practical |
| Camera | 35mm documentary, f/2.8 |
| Color | Muted teal-and-amber cinematic |
| Materiality | Brushed steel / anodized aluminum |

Prompt assembly:

> "An intelligence analyst at a workstation, three monitors casting cool glow on her face from camera-right, a single warm desk lamp behind her on a brushed-steel arm, shot on 35mm documentary lens at f/2.8, muted teal-and-amber cinematic grade."

Compare to the underwritten alternative — "An analyst at a desk, cinematic lighting, professional photo." — and the difference is exactly the four toolkit slots.

---

## Why this works across models

The four tables describe **technique categories that exist in the real world.** Every flagship has been trained on millions of images annotated with these technique labels — Rembrandt lighting, Kodak Portra 400, anamorphic 2.39:1, brushed steel — because that is how professional photography and cinematography indexes itself.

The toolkit therefore acts as a translation layer between BHIL's brand register and any image model's latent space. The vocabulary is portable, and that portability is what lets us route the same prompt across Midjourney, Nano Banana, Flux, and GPT Image with minimal rewriting.

---

## Common BHIL combinations

These four combinations cover roughly 80% of BHIL deliverables. They are documented in full in the prompt library; this is just the routing reference.

| Combination | Use Case |
| :--- | :--- |
| Chiaroscuro × 85mm portrait, f/1.8 × Kodak Portra 400 × Navy tweed | Executive portraits |
| Cool monitor glow + warm practical × 35mm doc, f/2.8 × Bleach bypass × Brushed steel | Analyst-at-workstation hero |
| Overhead key, no fill × 50mm × Muted teal-and-amber × Matte paper with registration marks | OSINT report cover |
| Volumetric haze + golden hour × Drone wide-angle × Fuji Velvia 50 × Hand-cast concrete | Geospatial / location intelligence |

---

## Where to go next

- The four tables themselves: [`../reference/README.md`](../reference/README.md)
- The 24-prompt library, where each combination is worked into a deliverable: [`../prompts/README.md`](../prompts/README.md)
