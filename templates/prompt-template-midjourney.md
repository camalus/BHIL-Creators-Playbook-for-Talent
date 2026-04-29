# Prompt Template — Midjourney v7

A fill-in-the-blank template for writing new Midjourney v7 prompts. Copy this template, replace the bracketed fields with project-specific values, and you have a prompt that follows BHIL discipline.

For the parameter philosophy behind this template, see [`frameworks/midjourney/parameter-stacks.md`](../frameworks/midjourney/parameter-stacks.md). For the toolkit references, see [`reference/`](../reference/).

## The Template

```text
[SCENE — what the camera sees, in plain declarative description.
One or two sentences. The subject, the action, the immediate
environment. No vague modifiers; specific nouns and verbs.]

[SUBJECT DETAIL — if a person, the archetypal description (no real-
person language). If an object, what it's made of. If a setting,
its named period and register. One sentence.]

[ATMOSPHERE — the mood, the time of day, the weather, the sense of
the moment. One sentence.]

[LIGHTING REGISTER from reference/lighting.md — name one of the
eight registers explicitly: "low-key chiaroscuro", "soft north-
window", "volumetric atmospheric", "cinematic backlight", "mixed
practical lighting at 3200K and 4500K", "top-down overhead light",
"underlit display glow", or "overcast soft-diffuse".]

[CAMERA + LENS from reference/camera-and-lens.md — name one
combination: "Aaton LTR-54, 35mm prime, T1.4", "Cooke S4/i 50mm
anamorphic, T2.8", "Hasselblad 503CW, 80mm Zeiss Planar, f/4",
etc.]

[COLOR / FILM STOCK from reference/color-and-film-stock.md — name
one stock: "shot on Kodak Vision3 500T, low-light cinema stock",
"shot on Fuji Pro 400H, soft pastel palette", "bleach-bypass color
treatment, desaturated, lifted shadows", etc.]

[OPTIONAL MATERIALITY from reference/materiality-and-texture.md —
name one if relevant: "engraved brass plate, patina visible",
"raw board-formed concrete, cool gray", "atmospheric haze, dust
in beams", etc. Skip this line if materiality isn't part of the
brief.]

--ar [PROJECT ASPECT — 3:2 / 2:3 / 16:9 / 21:9 / 1:1 / 4:5]
--style raw
--s [STYLIZE — see parameter stacks; default 250 for editorial]
--exp [EXPOSURE — see parameter stacks; default 30]
--no [NEGATIVE LIST — typical: "text, watermark, logo, modern
digital interface, neon"; for typography composites: add "focal
point"]
--p [PROFILE — your project's personalization profile]
--sref [SREF CODES — your project's locked aesthetic refs]
--sw [SREF WEIGHT — default 100; raise to 200-300 for tighter lock]
--oref [CHARACTER URL if a recurring person — otherwise omit]
--ow [OREF WEIGHT — default 150 if --oref used]
--v 7
```

## Filled Example — Late-Shift Analyst Portrait

```text
A late-shift analyst at her desk, framed three-quarters from behind,
looking at a wall of monitors that fill the right of the frame.

A composite character: a woman in her late 30s, short dark hair,
neutral expression, dressed in a navy blazer over an ivory shirt.

Quiet operational atmosphere, the room is empty except for her, the
hum of a building after hours.

Mixed practical lighting: warm tungsten desk lamp at 3200K, cool
display-source illumination at 4500K, narrow color contrast.

Aaton LTR-54, 35mm prime, T1.4.

Shot on Kodak Vision3 500T, low-light cinema stock.

--ar 3:2 --style raw --s 250 --exp 30
--no text, watermark, logo, modern digital interface, neon
--p [BHIL PROFILE] --sref [BHIL HERO SREFS] --sw 100
--oref [STORED CHARACTER URL] --ow 150 --v 7
```

## Filled Example — Architectural Hero Plate

```text
A modernist civic building exterior at midday, a single-story
horizontal mass of board-formed concrete, set against a neutral
overcast sky, the entrance plaza in the foreground.

A serious institutional building from the late 1960s, brutalist
discipline, no ornamentation.

Quiet civic atmosphere, no people in frame, restrained midday.

Overcast soft-diffuse natural light, no shadows, restrained
midtones, archival neutrality.

Hasselblad 503CW, 50mm Distagon, f/5.6.

Shot on Kodak Ektar 100, saturated landscape, fine grain.

Raw board-formed concrete, cool gray, faint texture from formwork
lines.

--ar 16:9 --style raw --s 200 --exp 25
--no text, watermark, logo, neon, modern digital
--p [BHIL PROFILE] --sref [BHIL HERO SREFS] --sw 100 --v 7
```

## Discipline Reminders

- **One register per layer.** One lighting register, one camera/lens, one stock, one (optional) materiality. Stacking two of any of these confuses the model.
- **Specificity beats verbosity.** "Aaton LTR-54, 35mm prime, T1.4" is denser signal than "shot on a film camera with a wide aperture lens for shallow depth of field."
- **Positive framing.** Describe what to render. Use `--no` for what to suppress, but spend most of the prompt on what should be there.
- **Project locks travel with every prompt.** `--sref`, `--p`, parameter stack, `--oref` for recurring characters. These are not optional once locked.
- **Iterate in-thread.** Don't rewrite the prompt to refine; use Vary Region, Pan, Zoom Out, or in-thread variations.

## Variants of This Template

- For typography compositing texture layers, use a much quieter parameter stack (`--s 75 --exp 5 --no text, watermark, logo, focal point`). See [Recipe C](../workflows/recipe-c-typography-compositing.md).
- For tileable patterns, add `--tile` to the parameter stack and remove human/character language. See [prompt 15](../prompts/04-data-intelligence-hero/15-tileable-brand-texture.md).
- For multi-frame narrative work, the template is reused per shot with the same locks. See [Recipe D](../workflows/recipe-d-long-form-narrative.md).

## Related

- [`templates/prompt-template-nano-banana.md`](./prompt-template-nano-banana.md) — Nano Banana equivalent.
- [`templates/prompt-template-flux.md`](./prompt-template-flux.md) — Flux.2 equivalent.
- [`templates/deliverable-spec-template.md`](./deliverable-spec-template.md) — project-level brief template.
- [`frameworks/midjourney/parameter-stacks.md`](../frameworks/midjourney/parameter-stacks.md)
- [`reference/`](../reference/) — toolkit references.
- [`prompts/`](../prompts/) — 24 fully-realized examples.
