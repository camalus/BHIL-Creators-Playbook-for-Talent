# Prompt Template — Flux.2 (Schnell / Dev / Pro)

A fill-in-the-blank template for Flux.2 prompts. Flux.2 sits between MJ's parameter-driven workflow and NB's natural-language workflow — it speaks long, structured natural-language prompts but exposes specific control via API parameters and IP-adapter reference images.

For the model lineup, see [`frameworks/flux/`](../frameworks/flux/). For toolkit references, see [`reference/`](../reference/).

## The Template — Standard Prompt

```text
[SCENE — what the camera sees, in dense natural-language description.
Two to four sentences. Specific subjects, specific actions, specific
environments. Flux.2 rewards more detail than NB and less compression
than MJ.]

[SUBJECT DETAIL — archetypal description of any people; material
composition of any objects; named period/register of any settings.]

[ATMOSPHERE — mood, time of day, weather, sense of the moment.]

[LIGHTING REGISTER from reference/lighting.md.]

[CAMERA + LENS from reference/camera-and-lens.md.]

[COLOR / FILM STOCK from reference/color-and-film-stock.md.]

[OPTIONAL MATERIALITY from reference/materiality-and-texture.md.]

Composition: [DESCRIBE THE FRAMING AND COMPOSITION EXPLICITLY —
"subject framed three-quarters from behind, monitors fill the right
two-thirds of the frame, desk lamp on the left, document spread in
the foreground." Flux.2 takes well to explicit composition language.]

Avoid: [NEGATIVE PROMPT — text overlay, watermark, modern digital
interface, neon, etc. Use this list instead of MJ's --no flag.]
```

API parameters (when calling Flux.2 Pro via API):

```json
{
  "model": "flux-2-pro",
  "prompt": "[FULL PROMPT TEXT FROM ABOVE]",
  "negative_prompt": "[NEGATIVES]",
  "width": [WIDTH IN PIXELS],
  "height": [HEIGHT IN PIXELS],
  "num_inference_steps": 28,
  "guidance_scale": 3.5,
  "seed": [OPTIONAL SEED FOR REPRODUCIBILITY]
}
```

## The Template — IP-Adapter (Reference Image)

When using an image reference for character or aesthetic lock:

```text
[FULL PROMPT TEXT — same structure as the standard template]

Reference: the attached image is [DESCRIBE THE REFERENCE — "the
locked aesthetic for this project" / "the character reference for
this person" / "the setting reference"].

Maintain from the reference: [SPECIFIC ELEMENTS — character
appearance, lighting register, color register, etc.].

Adapt for this scene: [WHAT'S DIFFERENT — pose, scene, action].
```

API call with IP-adapter:

```json
{
  "model": "flux-2-pro",
  "prompt": "[FULL PROMPT TEXT]",
  "ip_adapter": {
    "reference_image": "[BASE64 OR URL OF REFERENCE]",
    "weight": 0.7
  },
  "negative_prompt": "[NEGATIVES]",
  "width": [WIDTH], "height": [HEIGHT],
  "num_inference_steps": 28,
  "guidance_scale": 3.5
}
```

IP-adapter weights:
- `0.4-0.5` — light influence, mostly text-prompt-driven.
- `0.6-0.8` — balanced reference and prompt (default for character lock).
- `0.9-1.0` — heavy reference adherence (close to image-to-image).

## The Template — Schnell (Fast Iteration)

Flux.2 Schnell is the speed-optimized variant — much faster than Pro, less hero quality. Use for iteration like you'd use NB2.

Same prompt structure, but:
- Use `flux-2-schnell` instead of `flux-2-pro` in API calls.
- Reduce `num_inference_steps` to 4-8 (Schnell is fast because it converges in fewer steps).
- Lower `guidance_scale` to 1.0-2.0 (Schnell prefers low guidance).
- Generate 8-12 candidates rapidly to lock composition; then promote the winner to Flux.2 Pro for hero quality.

## Filled Example — Standard Prompt, Hero Plate

```text
A 35-year-old field operator standing on a flat industrial rooftop
at dusk, three-quarters back-view, looking out toward a distant city
skyline silhouetted against an indigo sky. The rooftop is cluttered
with HVAC equipment, a single rooftop access door behind her on the
right.

A composite character: athletic build, mid-length dark hair pulled
back, dressed in a charcoal field jacket over neutral layers, a
small leather satchel on her right hip.

Quiet operational atmosphere, end-of-shift hush, the city
indifferent.

Cinematic backlight from the dusk sky behind her, rim light along
her silhouette, single warm practical light from the rooftop access
door at 3200K filling the lower right of the frame.

Aaton LTR-54, 35mm prime, T1.4.

Shot on Kodak Vision3 500T.

Composition: subject placed in the left third of the frame, looking
toward the right; the city skyline occupies the right two-thirds at
mid-frame height; rooftop equipment and the access door anchor the
foreground.

Avoid: text overlay, watermark, modern digital interface, neon,
heroic stance, dramatic gesture.
```

## Discipline Reminders

- **Composition descriptions matter in Flux.2.** Unlike MJ (where composition is largely emergent) and NB (where composition is conversational), Flux.2 takes explicit composition direction well — and produces better output when given it.
- **Negative prompts go in the negative-prompt field.** Don't list negatives in the main prompt body; Flux.2 has a dedicated negative-prompt parameter.
- **Schnell for iteration, Pro for hero.** Same logic as NB2/NB Pro.
- **IP-adapter for character and aesthetic lock.** Flux.2's IP-adapter is the cleanest cross-model character-lock mechanism available; use it instead of trying to text-prompt-only the character into multiple scenes.
- **Provenance.** Flux.2 outputs do not carry SynthID or C2PA by default. Add C2PA metadata manually for client deliveries that require disclosure.

## When to Use Flux.2 vs. MJ vs. NB

| Goal | Best Choice |
| :--- | :--- |
| BHIL hero cinema register, brand-locked sref system | Midjourney v7 |
| Fast iteration with conversational refinement | Nano Banana NB2 |
| Hero-quality with image reference for character lock | Flux.2 Pro |
| Document/dossier subjects with high realism | Flux.2 Pro |
| Multi-format brand deployment | (depends — see workflow recipes) |

## Related

- [`templates/prompt-template-midjourney.md`](./prompt-template-midjourney.md)
- [`templates/prompt-template-nano-banana.md`](./prompt-template-nano-banana.md)
- [`templates/deliverable-spec-template.md`](./deliverable-spec-template.md)
- [`frameworks/flux/README.md`](../frameworks/flux/README.md) — Flux.2 lineup overview.
- [`reference/`](../reference/) — toolkit references.
- [`prompts/01-intelligence-report-covers/03-due-diligence-briefing.md`](../prompts/01-intelligence-report-covers/03-due-diligence-briefing.md) — Flux.2 Pro example.
- [`prompts/05-character-personas/17-vigil-analyst.md`](../prompts/05-character-personas/17-vigil-analyst.md) — Flux.2 Pro character example.
