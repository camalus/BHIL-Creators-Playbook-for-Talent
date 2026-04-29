# 08 · Glossary

Terms used throughout this playbook, in alphabetical order. Where a term has a deeper treatment elsewhere in the repository, the link follows the definition.

---

**Aesthetic Lock** — The first of the four pillars of a repeatable BHIL pipeline. The Sref and moodboard library treated as an approved, versioned design system. See [`../workflows/pipeline-pillars.md`](../workflows/pipeline-pillars.md).

**Aleph** — Runway's video-to-video editing capability. Used in Step 7 of the Nano Banana → Veo loop and in Recipe D for color matching between Kling and Veo clips.

**Anamorphic** — Widescreen photographic technique that produces a 2.39:1 aspect ratio with characteristic oval bokeh. Useful for executive banners and "film-still" hero imagery. See [`../reference/camera-and-lens.md`](../reference/camera-and-lens.md).

**ar (`--ar`)** — Midjourney aspect-ratio parameter. Changes composition, not just crop. See [`../frameworks/midjourney/parameters.md`](../frameworks/midjourney/parameters.md).

**Asset Management** — Third pillar of a repeatable pipeline. The unglamorous discipline of tagging, naming, and versioning every prompt, render, seed, and reference. See [`../workflows/pipeline-pillars.md`](../workflows/pipeline-pillars.md).

**Bleach bypass** — Color treatment that produces desaturated tones, crushed blacks, harsh highlights. Cold, industrial, military-brief register. See [`../reference/color-and-film-stock.md`](../reference/color-and-film-stock.md).

**C2PA Content Credentials** — Coalition for Content Provenance and Authenticity standard for cryptographic content signing. Embedded in Nano Banana Pro, NB2, and Adobe Firefly outputs. See [`../frameworks/nano-banana/synthid-c2pa.md`](../frameworks/nano-banana/synthid-c2pa.md).

**Character Library** — Second pillar of a repeatable pipeline. The 4–8 archetypal figures BHIL uses across deliverables, each with NB character sheet, MJ `--oref` URL, Runway saved reference, voice/persona notes. See [`../workflows/pipeline-pillars.md`](../workflows/pipeline-pillars.md).

**Chiaroscuro** — High-contrast lighting from a single hard source, with deep shadows. The default register for analyst-at-workstation imagery and intelligence-aesthetic covers. See [`../reference/lighting.md`](../reference/lighting.md).

**Conversational Mode (Midjourney)** — Pairing of Draft Mode with iterative chat. Used for rapid ideation; "Enhance" reruns a draft at full quality.

**Cref (`--cref`)** — Midjourney V6.1 Character Reference parameter. Superseded by `--oref` in V7. Useful only when rendering against legacy V4-era style codes. See [`../frameworks/midjourney/omni-reference.md`](../frameworks/midjourney/omni-reference.md).

**Cw (`--cw`)** — Midjourney Character Weight (0–100, default 100). At 100, copies face, hair, AND clothing; at 0, copies face only — the right setting when you want the same person in new outfits or eras.

**Draft Mode (`--draft`)** — Midjourney V7-exclusive mode. 10× faster, 50% GPU cost. Pairs with Conversational Mode. Not compatible with `--oref`.

**Exp (`--exp`)** — Midjourney V7 experimental aesthetic parameter (0–100). Released April 2025. BHIL sweet spot: 5–25.

**First and Last Frame** — Veo 3.1 conditioning capability. Generate the START frame in Nano Banana, generate the END frame in Nano Banana with the START as in-chat reference, feed both to Veo. See [`../workflows/nano-banana-veo-loop.md`](../workflows/nano-banana-veo-loop.md).

**Flow** — Google's web interface for Veo, alongside Vertex AI and the Gemini API. One of three entry points for Veo 3.1's first/last-frame conditioning.

**Grounded prompts** — Nano Banana Pro / NB2 feature that uses Google Search (and on NB2, Google Image Search) to ground image generation in real-world facts. See [`../frameworks/nano-banana/framework-d-grounded-prompts.md`](../frameworks/nano-banana/framework-d-grounded-prompts.md).

**imageConfig** — The Gemini API field that controls image output. Uses `aspectRatio` and `imageSize` (uppercase: `"1K"`, `"2K"`, `"4K"`). Gemini does not accept Midjourney-style parameter syntax.

**Ingredients to Video** — Veo feature that accepts up to 3 Nano Banana character references to maintain identity across video generation.

**Iw (`--iw`)** — Midjourney image weight for an attached image prompt (0–2). Below 1: text wins. Above 1: image wins. For brand refs: 0.5–1.0.

**Kontext (Flux.1 Kontext)** — Black Forest Labs' mask-free editing engine. Best-in-class for editing existing imagery without explicit mask annotation. See [`../frameworks/flux/README.md`](../frameworks/flux/README.md).

**LoRA** — Low-Rank Adaptation, a parameter-efficient fine-tuning method. The mechanism by which a BHIL brand-specific Stable Diffusion model would be trained on prior deliverables. See [`../frameworks/stable-diffusion/README.md`](../frameworks/stable-diffusion/README.md).

**Moodboard** — Midjourney's persistent house-style mechanism. Upload 20–100+ brand reference images, get a moodboard ID that surfaces as `--p [code]`. Superior to raw `--sref` for persistent brand register. See [`../frameworks/midjourney/moodboards.md`](../frameworks/midjourney/moodboards.md).

**Nano Banana** — Google's umbrella brand for native Gemini image generation. Three live models in April 2026: NB (`gemini-2.5-flash-image`), NB Pro (`gemini-3-pro-image-preview`), NB2 (`gemini-3.1-flash-image-preview`). See [`../frameworks/nano-banana/README.md`](../frameworks/nano-banana/README.md).

**Negative prompt** — Specification of what should not appear. Deprecated or removed in most 2026 flagships; see [Rule 2](01-foundational-rules.md#rule-2--describe-what-you-want-not-what-you-dont).

**Omni-Reference (`--oref`)** — Midjourney V7-exclusive replacement for `--cref`. Released May 2025. Handles characters, objects, garments, vehicles, logos. Costs 2× GPU time per render. See [`../frameworks/midjourney/omni-reference.md`](../frameworks/midjourney/omni-reference.md).

**Orchestration** — Fourth pillar of a repeatable pipeline. The node-based pipeline (Runway Workflow or equivalent) built once and reused per deliverable. See [`../workflows/pipeline-pillars.md`](../workflows/pipeline-pillars.md).

**Ow (`--ow`)** — Midjourney Omni-Weight (1–1000, default 100). Practical range 50–250. Higher `--ow` needed with high `--stylize` / `--exp` to preserve identity.

**P (`--p` / `--profile`)** — Midjourney personalization. Profile or moodboard code. Unlocked via rating ~200 image pairs at midjourney.com/rank-v7. Stack freely: `--p bhil7 bhil-cover`.

**Personalization** — Midjourney's ranked profile that learns taste via pairwise image rating. Each MJ version has its own profile (V7 `--p` does not transfer to V6). See [`../frameworks/midjourney/personalization.md`](../frameworks/midjourney/personalization.md).

**Q (`--q`)** — Midjourney quality / render-time budget (0.25–4). BHIL default: 1 for production, 2 for final hero renders.

**Rectified-flow transformer** — The architecture underlying Flux.2. Different from the diffusion architecture used by SD and the autoregressive components in some other models. Relevant to understanding why Flux's prompt adherence is qualitatively different.

**Rembrandt lighting** — Textbook portrait lighting: key at 45°, small triangle of light on the shadow-side cheek. The default for executive portraiture. See [`../reference/lighting.md`](../reference/lighting.md).

**Repeat (`--r` / `--repeat`)** — Midjourney parameter to run the same prompt N times. Combine with `--sref random --r 10` for bulk Sref code discovery.

**S / Stylize (`--s` / `--stylize`)** — Midjourney aesthetic-strength parameter (0–1000). 0–50: literal/product. 50–150: balanced. 150–300: editorial. 300–500: illustrative. BHIL defaults: 50–150 covers, 200–400 frameworks.

**Seed (`--seed`)** — Midjourney noise-field fix. ~99% reliable within a session in V7. Used to hold composition while iterating small prompt changes.

**Sref (`--sref`)** — Midjourney style reference (URL, code, or random). Does not copy subjects, only aesthetic signature. Stack multiple. The operational spine of brand-consistent MJ practice. See [`../frameworks/midjourney/sref-library.md`](../frameworks/midjourney/sref-library.md).

**Sref random** — Midjourney's random Sref-discovery mode. `--sref random --r 10` harvests 10 codes per prompt run.

**Style raw (`--style raw`)** — Midjourney parameter that disables MJ's auto-beautification. The single most important parameter for intelligence imagery. Pair with low `--s` for documentary realism.

**SynthID** — Google DeepMind's invisible watermarking system. Carried on every Gemini image-model output. Cannot be stripped without destructive re-encoding. See [`../frameworks/nano-banana/synthid-c2pa.md`](../frameworks/nano-banana/synthid-c2pa.md).

**Sv (`--sv`)** — Midjourney Sref interpreter version (V7: 1/2/3/4/6). V7 defaults to `--sv 6`, but legacy V6-era codes were authored against `--sv 4`. Add `--sv 4` if a legacy code stops working.

**Sw (`--sw`)** — Midjourney style weight (0–1000, default 100). Practical range 65–175. Test new codes at `--sw 1000 --s 0` first.

**thought_signature** — Field on the Gemini API that preserves reasoning state across turns. Required for multi-turn conversational editing on raw REST. The official Google GenAI SDK handles this automatically via `chats.create()`.

**Tile (`--tile`)** — Midjourney parameter that produces seamlessly tileable textures. Useful for brand background fills.

**Tilt-shift** — Camera technique that produces architectural / miniature / isometric effects. Geospatial renders, city-scape covers, framework dioramas. See [`../reference/camera-and-lens.md`](../reference/camera-and-lens.md).

**V (`--v`)** — Midjourney version parameter. Pin `--v 7` explicitly in shared prompts.

**Veo 3.1** — Google's flagship video generation model (April 2026). Veo 3.1 Lite released April 3, 2026. The BHIL motion default. See [`../workflows/nano-banana-veo-loop.md`](../workflows/nano-banana-veo-loop.md).

**Vertex AI** — Google Cloud's enterprise AI platform. One of three Veo 3.1 entry points (alongside Flow and the Gemini API).

**VLM** — Vision-Language Model. The architecture pattern underlying Flux.2's prompt-adherence advantage and Gemini 3's reasoning advantage.

**Weird (`--weird` / `--w`)** — Midjourney aesthetic-unconventionality parameter (0–3000). 300–800 useful for OSINT "glitchy surveillance" covers. 2000+ is exploration-only.
