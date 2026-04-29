# Recipe A — Midjourney → Runway

The cinematic-cinema register pipeline: generate stills in Midjourney v7 (locked aesthetic, locked character via `--oref`), then animate selected frames in Runway Gen-4. Use this when the project demands MJ's specific cinema-aesthetic and the motion register needs to match that specific look.

## Why This Recipe Exists

Midjourney v7 produces the most distinctive cinematic-cinema register of any model in the current lineup — *Tinker Tailor Soldier Spy*, *The Insider*, *Zodiac* texture in still form. Runway Gen-4 is the strongest "animate this still" model in production: it preserves the source aesthetic faithfully while adding believable motion. The combination produces motion deliverables that look like they were shot, not generated.

The trade-off: this is a cross-vendor pipeline. SynthID/C2PA provenance from the Google stack is not present. Disclosure metadata must be added manually to delivered assets.

## When to Use This Recipe

- The brand register is "serious cinema" and demands MJ's specific aesthetic.
- A 5-10 second motion clip is needed alongside one or more hero stills.
- Character or subject consistency across the still and motion is required.

## When Not to Use This Recipe

- If SynthID/C2PA provenance is required by the deliverable spec → use the [Nano Banana → Veo loop](./nano-banana-veo-loop.md).
- If the project is purely typographic → use [Recipe C](./recipe-c-typography-compositing.md).
- If the project needs many shots in a continuous narrative → use [Recipe D](./recipe-d-long-form-narrative.md).

## The Pipeline

### Step 1 — Aesthetic Lock in Midjourney

Generate 16-24 candidates against a register-establishing prompt with the `[BHIL COVER SREFS]` (or project-specific sref codes), the project's `--p` profile, and the appropriate parameter stack from [`frameworks/midjourney/parameter-stacks.md`](../frameworks/midjourney/parameter-stacks.md).

Pick 3-5 strongest candidates that share visual through-line. Capture their `--sref` codes; these become the project's locked aesthetic reference.

**Deliverable:** Locked sref code set, parameter stack, `--p` profile.

### Step 2 — Character Lock with `--oref`

If the scene includes a recurring subject, generate the character with high-quality output and capture the URL of the chosen image as `--oref`. Set `--ow` (omni-weight) to 100-200 for character preservation. See [`frameworks/midjourney/omni-reference.md`](../frameworks/midjourney/omni-reference.md).

```text
A composite character study: [archetypal description, no real-person
language]. [LOCKED LIGHTING + CAMERA + STOCK]. [LOCKED PARAMETER
STACK with --sref and --p].
```

Save the chosen image URL. Future prompts include `--oref [URL] --ow 150`.

**Deliverable:** Character reference URL with `--ow` value documented.

### Step 3 — Hero Still Generation

For each scene that needs a hero still, write the full prompt with the locked aesthetic, character reference, and parameter stack. Generate at the project aspect ratio. Iterate in-thread (Vary Region, Pan, Zoom Out) until the hero is right.

```text
[FULL HERO PROMPT — scene, subject, action]

[LIGHTING REGISTER from reference/lighting.md]
[CAMERA + LENS from reference/camera-and-lens.md]
[COLOR/STOCK from reference/color-and-film-stock.md]
[OPTIONAL MATERIALITY from reference/materiality-and-texture.md]

--ar [PROJECT ASPECT] --style raw --s [PARAMETER STACK STYLIZE]
--exp [PARAMETER STACK EXP] --p [BHIL PROFILE]
--sref [LOCKED SREF CODES] --sw [PARAMETER STACK SW]
--oref [CHARACTER URL] --ow 150 --v 7
```

**Deliverable:** Hero still at project aspect ratio.

**Checkpoint:** Aesthetic and character are locked; the still is delivery-quality.

### Step 4 — Frame Selection for Motion

Pick the still that will become the source for motion. Not every hero still is a good motion source — for Runway Gen-4, the strongest sources have:
- A subject that has a believable next motion (looking up, turning, lifting hand).
- Atmospheric elements that can move (steam, dust, screen flicker).
- Background that can hold still while the subject moves slightly.

Avoid as motion sources:
- Stills with multiple subjects in complex poses (motion will compromise one or more).
- Stills with extreme depth-of-field (motion can produce focal-plane artifacts).
- Stills with text, schematics, or dense data visualization (motion will distort).

### Step 5 — Runway Gen-4 Motion Generation

Upload the selected still to Runway Gen-4 as the source image. Write a motion brief in cinematographer language.

```text
Source image: [HERO STILL FROM STEP 3]

Camera motion: [SLOW PUSH-IN / SLOW LATERAL TRACK / STATIC HOLD /
SUBTLE HANDHELD] at [SLOW / MEDIUM / fast not recommended] speed.

Subject motion: [DESCRIBE THE BEAT — e.g., "the analyst lifts her
gaze from the screen toward the room, holds for 2 seconds, returns
to the screen"].

Atmospheric motion: [STEAM DRIFT / DUST IN BEAMS / SCREEN FLICKER /
PRACTICAL LIGHT WAVER].

Duration: [5 / 8 / 10] seconds. Maintain source image's lighting,
color, and aesthetic. Cinematic motion, no morphing, no warping.
```

**Deliverable:** A 5-10 second Runway Gen-4 motion clip at project resolution.

**Checkpoint:** Aesthetic preserved; motion is believable and not "generated-looking."

### Step 6 — Color Match (Optional but Common)

Runway sometimes shifts color slightly during motion generation. If the motion clip's grade has drifted from the still, color-correct the motion in DaVinci, Premiere, or your NLE of choice to match the still's grade. Use the still as the reference frame.

**Deliverable:** Color-matched motion clip.

### Step 7 — Audio Layer (Optional)

Runway can generate sound or you can layer in licensed audio in post. For BHIL-register work, the convention is restrained ambient room tone or score, not aggressive sound design. License audio appropriately; document the source.

**Deliverable:** Final delivered motion file (still + motion clip).

### Step 8 — Provenance and Disclosure

This pipeline does not produce automatic SynthID/C2PA signatures. For client deliveries:
- Manually add C2PA disclosure metadata using a tool like the C2PA CLI or Adobe's Content Credentials.
- Include in the deliverable's documentation: which models produced what, the prompts used, the reference images, and the sref/oref codes.
- Tag motion clips with "AI-generated motion" disclosure if required by client or platform policy.

**Deliverable:** Final assets with disclosure metadata and full prompt/parameter archive.

## Failure Modes

- **Aesthetic drift across hero stills.** Cause: sref codes weren't locked, or each prompt was written from scratch. Fix: enforce the locked sref + parameter stack on every prompt.
- **Character morphs across hero stills.** Cause: `--oref` wasn't used, or `--ow` was too low. Fix: always use `--oref` for recurring characters; set `--ow 150-200` for tight preservation.
- **Motion clip looks "generated."** Cause: motion brief was vague. Fix: cinematographer language; specify the camera move, the subject beat, the atmospheric layer.
- **Subject morphs in motion.** Cause: source still was too complex, or motion intensity was too high. Fix: pick a simpler-pose source still; reduce motion duration or intensity.
- **Color shift between still and motion.** Cause: Runway grade drift. Fix: color-correct in NLE.
- **The motion clip is technically clean but uninteresting.** Cause: the motion brief was conservative. Fix: be specific about the *narrative beat* the motion captures — what's the subject doing, why does it matter for this five seconds?

## Related

- [`workflows/README.md`](./README.md)
- [`workflows/pipeline-pillars.md`](./pipeline-pillars.md)
- [`workflows/nano-banana-veo-loop.md`](./nano-banana-veo-loop.md) — Google-stack alternative.
- [`workflows/recipe-b-nano-banana-to-midjourney.md`](./recipe-b-nano-banana-to-midjourney.md) — when MJ is the final, NB is the iteration tool.
- [`frameworks/midjourney/parameter-stacks.md`](../frameworks/midjourney/parameter-stacks.md)
- [`frameworks/midjourney/omni-reference.md`](../frameworks/midjourney/omni-reference.md)
- [`frameworks/midjourney/sref-library.md`](../frameworks/midjourney/sref-library.md)
- [`prompts/05-character-personas/17-vigil-analyst.md`](../prompts/05-character-personas/17-vigil-analyst.md) — example still source.
