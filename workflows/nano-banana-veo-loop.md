# Nano Banana → Veo 3.1 Loop

The seven-step pipeline for taking a Nano Banana still through Veo 3.1 motion and back into a still, with character and aesthetic consistency preserved across the loop. This is the canonical Google-stack workflow for projects that need both still-image deliverables and short-form motion clips from the same source.

## Why This Loop Exists

Both Nano Banana and Veo 3.1 are Google models that share a common foundation. They speak the same dialect of natural-language prompting, share underlying scene understanding, and produce SynthID-watermarked outputs with C2PA provenance. This makes a still→motion→still loop unusually consistent compared to mixing models from different vendors.

Use this loop when:
- The project needs a hero still **and** a 5–10 second motion clip from the same scene.
- Character consistency across the still and motion is important.
- The deliverable will be embedded with verifiable AI-disclosure provenance (SynthID + C2PA).

Don't use this loop when:
- The brand register requires Midjourney's specific aesthetic (use Recipe A instead).
- The deliverable is purely typographic (use Recipe C).
- Long-form narrative across many shots is needed (use Recipe D).

## The Seven Steps

### Step 1 — Aesthetic Lock in Nano Banana

Generate 8–12 still candidates against a generic-but-directional prompt for the project register. Use NB2 (the daily workhorse) for speed.

```text
[OPENING SCENE PROMPT — directional, register-establishing]

Aesthetic notes: [LIGHTING REGISTER from reference/lighting.md],
[CAMERA/LENS from reference/camera-and-lens.md], [COLOR/STOCK from
reference/color-and-film-stock.md].
```

**Deliverable:** 1–3 finalist still images that share a visual through-line.

**Checkpoint:** Human review. If the register isn't right, regenerate before promoting.

### Step 2 — Character Lock (If Applicable)

If the scene includes a recurring subject, generate the character separately with multiple angles. Use Nano Banana's grounded prompts (see [`frameworks/nano-banana/framework-d-grounded-prompts.md`](../frameworks/nano-banana/framework-d-grounded-prompts.md)) to ensure the character can be referenced consistently.

```text
A composite character study: [archetypal description, no real-person
language]. Generate four reference views: front, three-quarter,
profile, full-body. Same lighting register as the locked aesthetic
in step 1. Same color register.
```

**Deliverable:** Reference image set saved to the project asset library.

**Checkpoint:** The character is recognizable across the four views.

### Step 3 — Hero Still Generation in Nano Banana Pro

Promote to Nano Banana Pro for the hero-quality still. Re-prompt with the aesthetic and character references locked. NB Pro's 4K output is the deliverable register.

```text
[FULL HERO PROMPT for the specific scene]

Reference: [LOCKED AESTHETIC IMAGE from step 1]
Character: [REFERENCE IMAGE SET from step 2]

[LIGHTING + CAMERA + COLOR/STOCK as in step 1]
```

**Deliverable:** Hero still at 4K, with embedded SynthID watermark and C2PA signature.

**Checkpoint:** This is the still deliverable. If it's not right, iterate before moving to motion.

### Step 4 — Motion Brief Construction for Veo 3.1

Translate the still into a Veo 3.1 motion brief. Veo 3.1 accepts both text-only prompts and image-conditioned prompts (an input still image plus a motion description). The image-conditioned mode is canonical for the loop.

```text
Image-conditioned input: [HERO STILL FROM STEP 3]

Motion brief: [5-10 second clip description]
- Camera motion: [SLOW PUSH-IN / LATERAL TRACK / STATIC HOLD WITH
  PRACTICAL MOVEMENT / etc.]
- Subject motion: [SUBJECT BEHAVIOR — e.g., "the analyst lifts her
  gaze from the screen, looks toward the doorway, returns to the
  screen"]
- Atmospheric motion: [DUST DRIFT / STEAM / FLICKERING SCREEN GLOW
  / etc.]

Maintain the lighting register, color register, and character
appearance from the input image. Cinematic motion, no morphing,
no jump cuts.
```

**Deliverable:** A 5-10 second Veo 3.1 motion clip at the project resolution (commonly 1080p or 4K).

**Checkpoint:** Character and aesthetic survived the still→motion transition. If the character morphs or the lighting register shifts, regenerate.

### Step 5 — Frame Extraction (For Looping Back)

If the project needs additional stills derived from the motion, extract specific frames from the Veo 3.1 output. Veo 3.1's per-frame quality is high enough that extracted frames are usable as still deliverables.

Common frame-extraction targets:
- The opening frame (matches the input still).
- A mid-clip frame (a moment of subject motion or expression change).
- The closing frame (a different beat than the opening).

**Deliverable:** Additional still frames extracted at the project resolution.

**Checkpoint:** Each extracted frame holds up at full size. If frames are soft or motion-blurred, regenerate the Veo clip with different motion specifications.

### Step 6 — Refinement Loop (Optional)

If an extracted frame from step 5 is the candidate for a *new* hero still — distinct from step 3 — feed it back into Nano Banana Pro for refinement and re-rendering at hero quality.

```text
Reference image: [EXTRACTED VEO FRAME]

Re-render at Nano Banana Pro hero quality, preserving the
composition, character, and lighting. Refine: [specific cleanups
— e.g., "sharpen background detail, restore micro-contrast, adjust
color register if drifted"].
```

**Deliverable:** A second hero still derived from the motion clip.

**Checkpoint:** The refined frame is a distinct deliverable, not just a slightly cleaner duplicate of step 3.

### Step 7 — Provenance Archival

Archive the full chain:
- The locked aesthetic reference (step 1).
- The character reference set (step 2).
- The hero still (step 3) with prompt and SynthID/C2PA metadata.
- The motion clip (step 4) with prompt, source still, and SynthID/C2PA metadata.
- The extracted/refined frames (steps 5–6) with their derivation chain.

All assets land in the project asset library with versioned filenames and provenance metadata. See [Pillar 3 in `pipeline-pillars.md`](./pipeline-pillars.md#pillar-3--asset-management).

## Failure Modes

- **Character morphs across the still→motion transition.** Cause: motion brief drifted from the input image. Fix: lock the input image more aggressively in the Veo 3.1 prompt; reduce motion intensity; or generate a more stable character reference set in step 2.
- **The motion clip looks like generated motion** (too smooth, too perfect, dreamlike artifacts). Cause: motion brief was abstract. Fix: name the motion in cinematographer terms — "slow lateral track at 0.5 ft/sec," "static hold with practical hand-flicker," not "she moves."
- **SynthID is stripped during compositing.** Cause: re-encoding through naive image tools removes the watermark. Fix: composite in tools that preserve metadata (Figma, Photoshop with appropriate settings); never re-encode through lossy intermediates.
- **Color register drifts** between the still and motion. Cause: Veo 3.1 occasionally applies a slight grade. Fix: color-correct the motion in post (DaVinci, Premiere) to match the still register.
- **The motion is technically successful but feels generic.** Cause: too short on specificity. Fix: name the motion register the way you'd name lighting or stock — "slow Steadicam push-in" not "camera moves forward."

## When the Loop Doesn't Apply

If the still register is locked to Midjourney (you need MJ's specific cinema-aesthetic), the still→motion transition has more drift because the models don't share a foundation. In that case use Recipe A (MJ → Runway) instead. See [`recipe-a-midjourney-runway.md`](./recipe-a-midjourney-runway.md).

## Related

- [`workflows/README.md`](./README.md)
- [`workflows/pipeline-pillars.md`](./pipeline-pillars.md)
- [`workflows/recipe-a-midjourney-runway.md`](./recipe-a-midjourney-runway.md) — MJ-stack alternative.
- [`frameworks/nano-banana/README.md`](../frameworks/nano-banana/README.md)
- [`frameworks/nano-banana/framework-d-grounded-prompts.md`](../frameworks/nano-banana/framework-d-grounded-prompts.md)
- [`frameworks/nano-banana/synthid-c2pa.md`](../frameworks/nano-banana/synthid-c2pa.md)
- [`docs/06-advanced-workflows.md`](../docs/06-advanced-workflows.md)
