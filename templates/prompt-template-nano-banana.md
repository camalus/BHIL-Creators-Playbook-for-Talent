# Prompt Template — Nano Banana (NB / NB Pro / NB2)

A fill-in-the-blank template for Nano Banana prompts. Nano Banana speaks natural-language description; it doesn't take parameter flags. Density and specificity are the levers.

For the model lineup and frameworks, see [`frameworks/nano-banana/`](../frameworks/nano-banana/). For toolkit references, see [`reference/`](../reference/).

## The Template — Text-to-Image (Framework A)

```text
[SCENE — what the camera sees, in natural-language description.
Two or three sentences. Specific subject, specific action, specific
environment.]

[SUBJECT DETAIL — archetypal description of any people (no real-
person language); material composition of any objects; named period
or register of any settings.]

[ATMOSPHERE — mood, time of day, weather, sense of the moment.]

[LIGHTING REGISTER from reference/lighting.md — name one register
in cinematographer terms.]

[CAMERA + LENS from reference/camera-and-lens.md — name one
combination.]

[COLOR / FILM STOCK from reference/color-and-film-stock.md — name
one stock.]

[OPTIONAL MATERIALITY from reference/materiality-and-texture.md —
name one if relevant.]

Aspect ratio: [3:2 / 2:3 / 16:9 / 1:1].
Resolution: [Standard / Pro 4K — depending on which model].
```

Submit to NB2 for fast iteration; submit to NB Pro for hero-quality 4K finals.

## The Template — Multi-Image Fusion (Framework B)

When you have 2-4 reference images and want to compose a scene that combines them.

```text
Combine these reference images into a single scene:

Image 1: [DESCRIBE WHAT IMAGE 1 IS — e.g., "the project's locked
aesthetic reference"]
Image 2: [DESCRIBE WHAT IMAGE 2 IS — e.g., "the character reference
front-view"]
Image 3: [DESCRIBE WHAT IMAGE 3 IS — e.g., "the setting reference"]

Composition: [Where each image's contribution should appear in the
scene. Be explicit about subject placement, scene geography.]

[LIGHTING + CAMERA + STOCK as text-to-image template]

Aspect ratio: [SET].
Maintain the visual register of image [1 / 2 / 3] as the dominant
aesthetic.
```

## The Template — Conversational Editing (Framework C)

After an initial generation, refine in-thread:

```text
[REFERENCE TO PREVIOUS GENERATION]: "Take the previous image and..."

[SPECIFIC EDIT]:
- "...adjust the lighting to be slightly cooler on the left side"
- "...reposition the subject's gaze toward the camera"
- "...remove the second monitor on the right"
- "...add a paper document on the desk in the foreground"

Maintain everything else: [LIST WHAT MUST NOT CHANGE — composition,
character, lighting register, color register].
```

Conversational editing is one of NB's strengths. Use it for in-thread refinement; don't restart from scratch when you can adjust.

## The Template — Grounded Prompt (Framework D)

When you have a specific reference image (character, location, object) that the model must respect:

```text
Reference image: [URL OR ATTACHED IMAGE]

Scene: [WHAT THE NEW IMAGE SHOULD SHOW]

Maintain from the reference: [WHAT MUST CARRY OVER — character
appearance, specific object, specific location features].

Change in the new image: [WHAT'S DIFFERENT — pose, scene, lighting,
time of day, etc.].

[LIGHTING + CAMERA + STOCK as in the text-to-image template.]

Aspect ratio: [SET].
```

Grounded prompts are how NB delivers character and asset consistency across multi-frame work.

## The Template — Typography (Framework E)

For typography-forward generations (though Ideogram is typically stronger for typography):

```text
A [DELIVERABLE TYPE] hero with the following typographic hierarchy:

Top: [KICKER TEXT] in [FONT REGISTER] uppercase, [COLOR], small.
Center: [TITLE TEXT] in [FONT REGISTER] heavy, [COLOR], dominant.
Below: [SUBHEAD TEXT] in [FONT REGISTER] italic, [COLOR].
Bottom: [FOOTER TEXT] in mono uppercase, [COLOR].

Layout: [LEFT-ALIGNED / CENTERED], generous margins, restrained
hierarchy.

Background: [DESCRIBE THE BACKGROUND TEXTURE OR FIELD].

Color palette: [BG HEX], [TYPE HEX], [ACCENT HEX] only.

Aspect ratio: [SET].
```

For brand-precise typography, the canonical pipeline is the [typography compositing recipe](../workflows/recipe-c-typography-compositing.md) using Ideogram for type and MJ for texture. Use NB's Framework E for cases where rapid in-thread iteration of typographic layout is needed before committing to a final.

## Filled Example — Text-to-Image, Late-Shift Analyst

```text
A late-shift analyst at her desk, framed three-quarters from behind,
looking at a wall of monitors that fill the right of the frame with
cool screen-glow light. Practical desk-lamp warmth on the left.

A composite character: a woman in her late 30s, short dark hair,
neutral expression, in a navy blazer over an ivory shirt.

Quiet operational atmosphere, the room is empty except for her,
late-evening hush.

Mixed practical lighting: warm tungsten desk lamp at 3200K, cool
display-source illumination at 4500K, narrow color contrast.

Aaton LTR-54, 35mm prime, T1.4.

Shot on Kodak Vision3 500T, low-light cinema stock.

Aspect ratio: 3:2.
Resolution: Pro 4K (final hero).
```

## Filled Example — Grounded Prompt, Same Analyst in New Scene

```text
Reference image: [URL OF THE ANALYST PORTRAIT FROM PRIOR GENERATION]

Scene: The same analyst, now standing at a window looking out at a
city at dusk, three-quarters back-view, a leather portfolio in her
left hand. Mid-shot.

Maintain from the reference: the character's face, hair, and dress.
The lighting register (mixed practical, warm + cool, narrow
contrast).

Change in the new image: the setting (window, city dusk view), the
pose (standing, back-view), and the subject's stance (a portfolio
in hand).

Cinematic backlight from the dusk window, with practical desk-lamp
warmth from the room behind her at 3200K.

Cooke S4/i 32mm, T2.8.

Shot on Kodak Vision3 500T.

Aspect ratio: 3:2.
Resolution: Pro 4K.
```

## Discipline Reminders

- **Density beats word count.** A specific cinematographer-language phrase ("Aaton LTR-54, 35mm prime, T1.4") carries more signal than a paragraph of vague description.
- **Use grounded prompts for character lock.** Don't text-prompt the same character into multiple scenes; pass the reference image and describe the change.
- **Use conversational editing for refinement.** Don't restart; adjust in-thread.
- **NB2 for iteration, NB Pro for finals.** NB2 is faster; NB Pro produces hero-quality 4K.
- **SynthID and C2PA travel with NB outputs.** Don't strip the metadata in compositing.

## Related

- [`templates/prompt-template-midjourney.md`](./prompt-template-midjourney.md)
- [`templates/prompt-template-flux.md`](./prompt-template-flux.md)
- [`templates/deliverable-spec-template.md`](./deliverable-spec-template.md)
- [`frameworks/nano-banana/`](../frameworks/nano-banana/) — frameworks A through E.
- [`frameworks/nano-banana/synthid-c2pa.md`](../frameworks/nano-banana/synthid-c2pa.md) — provenance.
- [`reference/`](../reference/) — toolkit references.
- [`workflows/nano-banana-veo-loop.md`](../workflows/nano-banana-veo-loop.md) — still-to-motion loop.
