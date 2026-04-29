# Recipe D — Long-Form Narrative

The pipeline for projects that require many shots in a continuous visual narrative — storyboards, sequence keyframes, multi-shot briefing decks, episodic content. Character lock and aesthetic lock must hold across dozens of frames, not just one.

## Why This Recipe Exists

Single-asset pipelines (Recipe A, B, C, the NB→Veo loop) optimize for a single hero deliverable. When the brief is "twelve frames of a recurring analyst across multiple scenes" or "a full storyboard for a five-minute briefing video," the consistency requirements scale up: every frame must feel like it came from the same project, the same character, the same lighting register.

This recipe formalizes the multi-frame discipline. It assumes the four [pipeline pillars](./pipeline-pillars.md) are already in place; the work here is the orchestration of repeated single-asset pipelines under a unified brief.

## When to Use This Recipe

- The deliverable is **multi-shot**: storyboard, briefing-deck visual sequence, episodic content frames, narrative report illustration set.
- A **recurring character** appears across multiple scenes.
- A **consistent lighting and aesthetic register** must hold across the set.
- The set is **3+ frames**; for 1-2 frames, single-asset recipes are simpler.

## When Not to Use This Recipe

- Single-asset deliverables → use Recipe A, B, C, or the NB→Veo loop.
- Animated/motion narratives that need shot-to-shot motion continuity → use Veo 3.1's longer-form modes (with the [NB→Veo loop](./nano-banana-veo-loop.md) as the per-shot pipeline).
- Narratives where characters change every shot → no character lock needed, treat as independent assets.

## The Pipeline

### Step 1 — Story Spine

Before generating any image, write the story spine in plain English. This is the document the project will return to whenever a shot question arises.

```text
SPINE — [PROJECT NAME]

Scene 1: [Scene description, who is in it, what happens]
Scene 2: [...]
Scene 3: [...]
...
Scene N: [...]

Through-lines:
- Subject(s): [who recurs across scenes]
- Setting register: [what kind of world]
- Lighting register: [from reference/lighting.md]
- Camera register: [from reference/camera-and-lens.md]
- Color/stock register: [from reference/color-and-film-stock.md]
- Brand palette: [hex values]
- AR: [aspect ratio for the set]
```

The spine is the source of truth. Every prompt later in this recipe will reference this document.

### Step 2 — Aesthetic Lock

Generate the project's locked aesthetic reference *before* generating any character or shot. The lock is the visual through-line for the entire set.

In MJ v7:
- Generate 16-24 candidates against a register-establishing scene.
- Pick 3-5 that share a coherent through-line.
- Capture sref codes; document in the project README.
- Document the parameter stack and `--p` profile.

In NB Pro / NB2:
- Generate the establishing scene at hero quality.
- Save the chosen image as the project's aesthetic reference image.
- Document the prompt and lighting/lens/stock register language.

**Deliverable:** A locked-aesthetic reference (sref codes + parameter stack, or reference image set).

### Step 3 — Character Library

For each recurring subject, generate a multi-angle reference set:

```text
A composite character study: [archetypal description]. Generate four
reference views: front, three-quarter, profile, full-body. Same
locked lighting register, same color register, neutral expression.
```

In MJ v7, save the chosen front-view URL for `--oref` use. Generate additional poses by re-prompting with the `--oref` plus the new pose description.

In Nano Banana, save the reference image set for grounded-prompt use (see [`frameworks/nano-banana/framework-d-grounded-prompts.md`](../frameworks/nano-banana/framework-d-grounded-prompts.md)).

Repeat for every recurring subject. Each gets its own reference set.

**Deliverable:** Per-character reference library, documented in the project README.

### Step 4 — Shot List from Spine

Translate the story spine into a shot list. For each scene:

```text
SHOT [#]
Description: [What's in the frame, what's happening]
Subject(s): [Which characters from the library, in what pose/position]
Setting: [Where, what time, what register]
Camera: [Framing, lens, angle]
Light: [Direction, register, color temp]
Aspect: [If different from the project default]
```

The shot list is the bridge between the spine and the prompts. A shot list of 12 entries means 12 separate generation tasks.

### Step 5 — Per-Shot Prompt Generation

For each shot in the list, write the prompt using the locked aesthetic, the locked character references, and the shot's specific scene.

In MJ v7:

```text
[SHOT-SPECIFIC SCENE PROMPT]

[LIGHTING REGISTER from reference/lighting.md — locked across the set]
[CAMERA + LENS — varies per shot but stays within project register]
[COLOR/STOCK — locked across the set]
[OPTIONAL MATERIALITY]

--ar [PROJECT ASPECT] --style raw --s [STACK] --exp [STACK]
--p [BHIL PROFILE] --sref [LOCKED SREFS] --sw [STACK]
--oref [CHARACTER URL] --ow 150 --v 7
```

In Nano Banana:

```text
[SHOT-SPECIFIC SCENE PROMPT, natural language]

Reference: [LOCKED AESTHETIC IMAGE]
Character: [REFERENCE IMAGE SET]

[LIGHTING + CAMERA + COLOR/STOCK described in cinematographer terms]
```

Generate per-shot. Iterate per-shot in-thread until the shot is locked. Move to the next.

**Deliverable:** A locked still per shot.

### Step 6 — Set-Level QA

After all shots are generated, lay them out side-by-side (in Figma, in a Notion gallery, in Adobe Bridge — whatever tool surfaces the full set at once). Check for:

- **Character drift.** Does the character look like the same person across shots? Where they don't, regenerate with stronger character lock.
- **Aesthetic drift.** Do the shots feel like they came from the same project? Where they don't, look at the parameter stack and sref usage on the off-shot — usually one of those was loosened.
- **Color drift.** Is the palette consistent across shots? Where shifts appear, color-correct in Figma.
- **Pacing.** Does the set tell the story? Are there narrative gaps where a missing shot should sit?

Iterate until the set holds together as a *set*, not just as N independent images.

### Step 7 — Set Composite (If Applicable)

If the deliverable is a single layout (storyboard panel, briefing-deck slide, narrative report illustration), composite the locked stills into the deliverable in Figma or InDesign. Add typography, scene labels, framing rules per the brand spec.

If the deliverable is per-shot stills (each frame is a standalone deliverable), prepare each for delivery — typography overlays per [Recipe C](./recipe-c-typography-compositing.md) if needed.

### Step 8 — Provenance Archival

Archive at three levels:

1. **Project level:** the spine, the shot list, the locked aesthetic references, the character library, the project README.
2. **Per-shot level:** each shot's prompt, parameter stack, references, generation date, model and version.
3. **Set level:** the final composite or per-shot deliverables, with provenance metadata.

The audit trail must support "show me how shot 7 was made" within a minute.

## A Common Variant — Episodic Continuity

For projects where the same set of characters recurs across multiple separate deliverables over weeks or months (a regular briefing series, an episodic content schedule):

- Keep the project-level documentation as the *master*. The aesthetic lock and character library survive across episodes.
- Each new episode reuses the locks. The shot list grows but the discipline doesn't reset.
- Periodically (every 6–12 episodes) review whether the aesthetic register still serves the project, or whether to do a controlled register update.

## Failure Modes

- **Character drift across the set.** Cause: `--oref` or character reference wasn't used consistently, or `--ow` was too low. Fix: stricter character lock; regenerate offending shots.
- **Aesthetic drift across the set.** Cause: per-shot prompts varied the parameter stack or sref. Fix: enforce the locked stack on every prompt; the spine is the source of truth.
- **The set technically holds together but feels lifeless.** Cause: too much lock, not enough variation per scene. Fix: vary lighting *direction*, camera angle, distance — the project register stays the same, but the per-shot specifics should give each scene character.
- **Shot list bloats during execution.** Cause: scope creep. Fix: protect the shot list; new ideas go to a follow-up shot list, not into the active set.
- **Time blows up.** Cause: per-shot iteration is slow. Fix: use the [Recipe B fast-iteration pattern](./recipe-b-nano-banana-to-midjourney.md) per shot — NB2 to lock composition, MJ to render hero. Across 12 shots, the time savings add up.
- **The spine becomes outdated mid-project.** Cause: shots evolved beyond the original spine. Fix: update the spine document. The spine is the source of truth, and the truth changes.

## Related

- [`workflows/README.md`](./README.md)
- [`workflows/pipeline-pillars.md`](./pipeline-pillars.md)
- [`workflows/recipe-a-midjourney-runway.md`](./recipe-a-midjourney-runway.md) — per-shot motion option.
- [`workflows/recipe-b-nano-banana-to-midjourney.md`](./recipe-b-nano-banana-to-midjourney.md) — per-shot fast iteration.
- [`workflows/nano-banana-veo-loop.md`](./nano-banana-veo-loop.md) — per-shot Google-stack option.
- [`frameworks/midjourney/personalization.md`](../frameworks/midjourney/personalization.md) — `--p` profile management.
- [`frameworks/midjourney/omni-reference.md`](../frameworks/midjourney/omni-reference.md) — character lock with `--oref`.
- [`frameworks/midjourney/sref-library.md`](../frameworks/midjourney/sref-library.md) — sref management.
- [`prompts/05-character-personas/`](../prompts/05-character-personas/) — character prompt examples.
