# Recipe B — Nano Banana → Midjourney

The fast-iteration-to-hero pipeline: use Nano Banana for rapid composition and lighting iteration, then promote the winning frame to Midjourney v7 for hero-quality finals. Use this when MJ is the brand-locked final-output model but iteration speed matters during the exploration phase.

## Why This Recipe Exists

Midjourney v7 is the BHIL hero-output default — its specific cinema register is hard to replicate elsewhere, and its `--sref`/`--oref` system gives precise project-level lock. But MJ is *slow* for iteration: each generation takes ~60 seconds, and conversational refinement isn't the model's strength.

Nano Banana (NB2 specifically) is *fast* — sub-15-second generations, conversational refinement, in-thread editing. But its aesthetic register doesn't match the BHIL/MJ hero look exactly.

The recipe combines them: iterate composition and lighting in NB2 at speed, then re-prompt the locked composition in MJ v7 with the brand sref/parameter stack for hero output.

## When to Use This Recipe

- The project's hero deliverable is locked to MJ v7 (sref system, brand register).
- The composition is unsettled and needs fast iteration before committing.
- A character pose, scene staging, or lighting register needs exploration.

## When Not to Use This Recipe

- If both stills and motion are needed → use the [Nano Banana → Veo loop](./nano-banana-veo-loop.md) (single-vendor consistency).
- If MJ alone is fast enough for the project → skip the NB2 iteration step.
- If the deliverable is purely typographic → use [Recipe C](./recipe-c-typography-compositing.md).

## The Pipeline

### Step 1 — Brief Translation

Write the deliverable brief in plain English, not yet in any model's grammar:

> A late-shift analyst at her desk, framed three-quarters from behind, looking at a wall of monitors. Cool screen-glow lighting on her face from the left. Quiet operational atmosphere, mid-shot. Cinematic register, serious.

### Step 2 — Fast Iteration in Nano Banana (NB2)

Translate the brief into a Nano Banana prompt. NB2 prefers natural-language description over parameter-heavy prompts.

```text
A late-shift analyst at her desk, framed three-quarters from behind,
looking at a wall of monitors that fill the right side of the frame
with cool screen-glow light. Practical desk-lamp warmth on the left
side of the scene. Mid-shot, restrained operational atmosphere,
cinematic register. The room is in shadow except for the screen
glow and the desk lamp. Late shift, focused subject, no other
people visible.
```

Generate 8-12 candidates. Use NB2's conversational refinement to lock:
1. **Composition** — framing, subject pose, scene layout.
2. **Lighting register** — direction, color temperature contrast, falloff.
3. **General atmosphere** — busy vs. spare, dim vs. bright, occupied vs. solitary.

Aesthetic register can be approximate at this stage; the MJ promotion step will lock that. The point is to nail composition and lighting fast.

**Checkpoint:** A "winning frame" — the NB2 image that captures the desired composition and lighting. Save this as a reference image.

### Step 3 — Composition Translation to MJ Grammar

Translate the locked composition into Midjourney prompt grammar. Keep the *composition and lighting* of the NB2 frame; replace the *aesthetic* with MJ register language.

```text
A late-shift analyst at her desk, framed three-quarters from behind,
looking toward a wall of monitors filling the right of the frame
with cool screen-glow illumination. Practical desk-lamp warmth on
the left of the scene at 3200K. Mid-shot, the room beyond the desk
in deep shadow. Late shift, focused, single occupant.

Mixed practical lighting: warm tungsten desk lamp 3200K, cool
display-source illumination 4500K, narrow color contrast. Aaton
LTR-54, 35mm prime, T1.4. Shot on Kodak Vision3 500T, low-light
cinema stock.

--ar 3:2 --style raw --s 250 --exp 30 --p [BHIL PROFILE]
--sref [BHIL HERO SREFS] --sw 100 --v 7
```

Include the NB2 winning frame as `--cref` if MJ accepts it for compositional reference, or describe the composition in detail in text. (Direct image-to-image transfer is not always available; rely on textual composition description.)

### Step 4 — MJ Generation and Refinement

Generate in MJ. Use Vary Region or Pan/Zoom Out to adjust details against the composition you locked in NB2. Iterate in-thread.

**Checkpoint:** Hero still with MJ register, NB2-locked composition, locked sref/profile.

### Step 5 — Final Composite or Direct Use

If the hero still goes straight to deliverable, archive with metadata. If it needs typography, brand marks, or color correction, composite in Figma. See [Recipe C](./recipe-c-typography-compositing.md) for the typography-compositing pattern.

### Step 6 — Provenance Archival

Archive the chain:
- The NB2 iteration set (the candidates and the winning frame), with prompts.
- The MJ hero still, with full prompt, parameter stack, sref/oref references.
- Any composite layer outputs.

Note that the NB2 iteration outputs carry SynthID/C2PA; the MJ hero does not. Document this in the asset metadata so disclosure language can be applied appropriately.

## A Common Variant — Character Pose Lock

A specific use of this recipe: when a recurring character (already in the [character library](./pipeline-pillars.md#pillar-2--character-library)) needs to be staged in a *specific new pose or scene*, NB2 is much faster at conversational pose iteration. Generate the pose in NB2 first, then promote to MJ with `--oref` for character lock and `--cref` (if available) or textual composition description for pose lock.

```text
NB2 prompt:  "[CHARACTER REFERENCE IMAGE] standing at a window,
              looking out at the city at dusk, three-quarters back-
              view, a leather portfolio in her left hand, mid-shot,
              cinematic register."

[Iterate 6-8 candidates, lock the pose.]

MJ prompt:   [Composition described in text from the NB2 winner]
             [Lighting + lens + stock as before]
             --oref [STORED CHARACTER URL] --ow 150
             --sref [BHIL PORTRAIT SREFS] --sw 100
             [other parameters]
```

## Failure Modes

- **NB2 composition doesn't translate to MJ.** The NB2 winning frame uses staging that MJ can't reproduce in text alone. Cause: NB2's conversational placement is more flexible than MJ's prompt-from-text approach. Fix: simplify the staging, or use MJ's Pan/Zoom Out tools to recreate the spatial relationship.
- **MJ register doesn't match NB2 lighting.** The lighting in the NB2 winner had a specific feel that MJ misses. Cause: each model has its own light-rendering tendencies. Fix: name the lighting register in cinematographer terms (use [`reference/lighting.md`](../reference/lighting.md)); accept some drift between models.
- **Time savings disappear because MJ iteration is also long.** If MJ doesn't get there in 2-3 generations, the recipe's time math breaks. Fix: tighten the NB2 lock first; ensure the composition is *truly* settled before promoting.
- **Disclosure metadata gap.** The MJ hero lacks SynthID/C2PA. Fix: manually add C2PA metadata to the final hero (Adobe Content Credentials or C2PA CLI), and document the chain in the asset library.

## Related

- [`workflows/README.md`](./README.md)
- [`workflows/pipeline-pillars.md`](./pipeline-pillars.md)
- [`workflows/nano-banana-veo-loop.md`](./nano-banana-veo-loop.md) — single-vendor still-to-motion alternative.
- [`workflows/recipe-a-midjourney-runway.md`](./recipe-a-midjourney-runway.md) — MJ-first still-to-motion alternative.
- [`frameworks/nano-banana/README.md`](../frameworks/nano-banana/README.md)
- [`frameworks/midjourney/README.md`](../frameworks/midjourney/README.md)
- [`frameworks/midjourney/omni-reference.md`](../frameworks/midjourney/omni-reference.md)
- [`prompts/05-character-personas/17-vigil-analyst.md`](../prompts/05-character-personas/17-vigil-analyst.md) — analyst portrait example.
