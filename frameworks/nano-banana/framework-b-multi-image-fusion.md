# Framework B — Reference-Based / Multi-Image Fusion

The Nano Banana pattern for combining multiple reference images into a single output. The whole framework hangs on one principle: **assign every reference an explicit role.**

## The Formula

```text
[Reference images with explicit role assignments] +
[Relationship instruction] +
[New scenario]
```

## The Role-Assignment Principle

The failure mode is ambiguity. If you upload three images without telling the model which is the subject versus the environment versus the moodboard, it will blend all three into slop. Gemini's reasoning step is good but it cannot read your mind about which reference is doing what work.

Assign every reference one of these roles explicitly:

| Role | What the model takes from it |
| :--- | :--- |
| **Subject** | Identity, face, body, clothing details, posture |
| **Environment** | Setting, layout, depth, atmospheric register |
| **Style** | Color grade, lighting register, photographic signature |
| **Texture / Material** | Surface qualities, materiality, finish |
| **Layout** | Composition, framing, element placement |
| **Palette** | Color accents to apply to UI elements, lighting, or wardrobe |

In the prompt, label the references explicitly: *"Image 1 is the subject. Image 2 is the environment. Image 3 is the palette reference."* This is a discipline cost of about 15 words and saves 10 regenerations.

## Reference Limits by Model

| Model | Reference Cap |
| :--- | :--- |
| Nano Banana Pro | 6 objects + 5 characters |
| Nano Banana 2 | 10 objects + 4 characters |
| Nano Banana (2.5) | up to 14 combined |

Treat character references as the binding constraint. Pro's 5-character limit is enough for any briefing-deck scene; NB2's 4-character limit constrains crowd compositions slightly. For multi-character intelligence imagery, 4–5 is rarely the constraint; the constraint is usually wardrobe and environment fidelity, which lives in the object slots.

## Worked Example — Brand Composite

```text
[Image 1: BHIL brand palette swatch card.
 Image 2: Headshot of the BHIL principal.
 Image 3: OSINT dashboard screenshot.]

Combine as follows:

Use the person from Image 2 as the subject — preserve exact facial
features, hair, and wardrobe.

Place them in an environment inspired by Image 3 — dark workstation,
three curved monitors displaying map overlays and node-link graphs.

Apply the color accents from Image 1 (obsidian, ivory, amber) to
UI elements and ambient lighting.

Subject in 3/4 profile, mid-analysis, reaching toward one screen.
Cinematic lighting, one warm key light from desk lamp, cool monitor
fill. 16:9, 2K, slightly desaturated editorial grade.

Subject identity must remain consistent with Image 2.
```

API config: `aspect_ratio: "16:9"`, `image_size: "2K"`. The "subject identity must remain consistent with Image 2" closing line is not redundant — it is the anchor that makes face preservation reliable when the model is also juggling environment and palette references.

## Anchor Lines That Reliably Pay Off

Add one or more of these closing lines depending on what matters most for the deliverable:

- *"Subject identity must remain consistent with Image [N]."*
- *"Preserve exact facial features, hair, and skin tone from Image [N]."*
- *"The environment from Image [N] should be reinterpreted, not copied — same register, different angle."*
- *"Use Image [N] only for color accents, not for layout or composition."*
- *"Ignore the typography in Image [N]; treat it as a moodboard reference only."*

These aren't filler. The model treats explicit "must" / "preserve" / "ignore" instructions as higher-priority than descriptive text earlier in the prompt.

## When the Reference Itself is the Problem

A bad reference produces a bad output. Common reference failures:

- **Low-resolution headshots** — the model inherits the resolution. Use 1K+ source images.
- **Reference with strong text overlays** — the model often tries to render that text into the new scene.
- **Mixed-aesthetic reference set** — combining a *Vogue* portrait with a satellite image as references produces averaged confusion. Match aesthetic registers across references.
- **Real-person headshots** — work mechanically but produce uncanny-valley results far more often than AI-generated references do. The convention across this playbook: anchor on AI-generated portraits when possible, escalate to real-person headshots only when the deliverable specifically requires the actual person.

## Identity Preservation vs Scene Drift

There is an inherent tradeoff between preserving subject identity and giving the model latitude on the environment. Two operating modes:

**High preservation** (use when face-accuracy is critical):

```text
Subject identity from Image 2 is the highest priority. Match facial
features, hair color and texture, and skin tone exactly. The environment
may interpret Image 3 loosely, but the subject must be photorealistic
and indistinguishable from the reference.
```

**High latitude** (use when you want the same person reimagined in a different style):

```text
Use Image 2 as character reference for general likeness — same age,
build, hair length and color. Environmental and stylistic interpretation
should follow Image 3. Acceptable to render the subject in a different
register than the source headshot.
```

Pick one mode per render. Asking for both simultaneously produces drift.

## Failure Modes

- **No role assignments** — the model averages all references.
- **Role conflict** — assigning the same reference to two roles ("Image 2 is subject and environment"). Pick one.
- **Too many references** — using all 14 slots on NB rarely improves output past 4–5. Cap at 5 unless every reference earns its place.
- **Drift across multi-turn editing** — once you've established the references in turn 1, don't re-upload them in turn 3. Turn 1's references persist through the conversation; re-uploading creates a new context.

## Related

- [`framework-a-text-to-image.md`](./framework-a-text-to-image.md) — clean-slate generation without references.
- [`framework-c-conversational-editing.md`](./framework-c-conversational-editing.md) — what to do once Framework B has produced a base image.
- [`workflows/nano-banana-veo-loop.md`](../../workflows/nano-banana-veo-loop.md) — multi-image fusion is how the character pack gets built.
