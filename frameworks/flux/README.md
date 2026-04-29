# Flux.2 (Black Forest Labs)

> Released November 2025. A 24B-parameter Mistral-3 vision-language model paired with a rectified-flow transformer. Leading photorealism and prompt adherence among 2026 flagships, and the only flagship that BHIL can run air-gapped via open weights.

## When to Choose Flux

| Use Case | Why Flux Wins |
| :--- | :--- |
| Client-confidential work that cannot leave the network | Flux.2 [dev] open weights and Flux.2 [klein] Apache 2.0 mean fully on-prem deployment |
| Editorial photorealism where Midjourney's "MJ-look" is unwanted | Flux.2 Pro produces photographic register without MJ's stylistic signature |
| Mask-free editing on existing images | Flux.1 Kontext is the best-in-class mask-free editor |
| Persona portraiture for intelligence personas | Documentary-photographic register on prompt; less stylized than MJ default |
| Architectural and location-intelligence renders | Strong prompt adherence on materiality, lighting, and architectural detail |

## When Not to Use Flux

- **Default beauty / cinematic register** — Midjourney's stylize parameter is a more reliable path.
- **Long-passage typography** — Nano Banana Pro and Ideogram v3 are stronger.
- **Conversational multi-turn editing** — Nano Banana's chat pattern is purpose-built for this; Flux Kontext is editing-strong but not chat-native.
- **Real-time grounded output** — only Gemini supports Search grounding.

## The Model Family

| Variant | Positioning |
| :--- | :--- |
| **Flux.2 Pro** | Hosted, highest quality, best prompt adherence. Default for client-grade BHIL output. |
| **Flux.2 [dev]** | Open weights with non-commercial license. For research, experimentation, BHIL's internal evaluation pipeline. |
| **Flux.2 [klein]** | Apache 2.0 — fully commercial-permitted open weights. The deployment target for air-gapped client work. |
| **Flux.1 Kontext** | The mask-free image-editing model. Pair with Flux.2 generation for the full pipeline. |

## Prompting Discipline

Flux.2 rewards the same patterns that work on Nano Banana — **descriptive prose, cinematographer vocabulary, no negatives.** The Flux team explicitly dropped support for negative prompts in 2.0; describe what you want.

A tested baseline pattern:

```text
[Subject in narrative form] + [Action / posture] + [Environment] +
[Camera and lens specifics] + [Lighting register] + [Color grade] +
[Aspect ratio and resolution]
```

Length sweet spot: 60–120 words. Past 150 words, late content gets attenuated similarly to other transformer-based models.

## Worked Example — Persona Portrait

```text
Editorial photograph of a mid-40s woman intelligence analyst seated
at a sparse modern workstation, half-lit from a single cool-temperature
window to camera-left, three monitors glowing in shallow focus behind
her, wearing a charcoal merino crewneck and minimal wire-frame glasses.
Expression: focused, neutral, mid-analysis. Restrained color palette:
charcoal, steel blue, a single warm skin highlight. Shot on a Leica Q3,
28mm, f/2.8, natural skin texture, no retouching, documentary tone.
3:2 aspect.
```

This same prompt structure works across Flux.2 Pro and the open-weights variants with consistent results.

## Flux.1 Kontext for Editing

Kontext is a separate model purpose-built for mask-free editing. The pattern:

1. Generate or supply a base image (from Flux.2, MJ, or photography).
2. Prompt Kontext with: *"In the supplied image, [change description]. Preserve everything else."*
3. Iterate against the same base or against Kontext's output.

Kontext's strength relative to Nano Banana Framework C: surgical precision on small regions. *"Replace the desk lamp with a brass banker's lamp"* lands more cleanly on Kontext than on Gemini, which sometimes adjusts surrounding elements.

Kontext's weakness: it's a single-model edit, not a multi-turn conversation. State doesn't persist; each edit is independent.

## On-Prem Deployment for Client-Confidential Work

The 2026 strategic differentiator. Flux.2 [klein] under Apache 2.0 means BHIL can:

- Deploy Flux.2 on a customer-controlled GPU server inside the client's network.
- Generate imagery for sensitive deliverables (defense, regulated finance, government) without any data leaving the client's perimeter.
- Pair with a BHIL-trained LoRA (see [Stable Diffusion 3.5](../stable-diffusion/README.md) — same LoRA pattern applies to Flux open weights with the appropriate training scripts) for brand-locked output without external model dependencies.

The hardware budget: a single H100 or two A100s handle Flux.2 [klein] inference comfortably. Training a brand LoRA is a one-time cost; ongoing inference is BAU.

## SynthID and Provenance

Flux does not embed Google's SynthID, and Black Forest Labs does not currently publish a watermarking specification of equivalent strength. For clients who specifically require detectable AI provenance, **route to Gemini for the deliverable.** For clients where provenance disclosure happens at the methodology-note level (most BHIL work), Flux is fine.

## Failure Modes

- **Trying to use negatives** — Flux.2 dropped them. Frame everything positively.
- **Over-detailed long prompts** — past 150 words, late content gets dropped. Split into generation + Kontext edit.
- **Expecting MJ-look on default settings** — Flux's default is documentary photorealism, not stylized cinema. To get MJ-style output from Flux you have to explicitly prompt for it ("painterly editorial illustration, cinematic color grade") and even then it lands differently.
- **Treating Kontext as multi-turn** — each Kontext edit is a single operation. For chained edits, use Nano Banana.

## Related

- [`docs/07-other-models.md`](../../docs/07-other-models.md) — chapter context across all alternative models.
- [`prompts/01-intelligence-report-covers/03-due-diligence-briefing.md`](../../prompts/01-intelligence-report-covers/03-due-diligence-briefing.md) — production prompt using Flux.2 Pro.
- [`prompts/05-character-personas/17-vigil-analyst.md`](../../prompts/05-character-personas/17-vigil-analyst.md) — persona portrait using Flux.2 Pro.
- [`prompts/06-geospatial/22-architectural-brief-locus.md`](../../prompts/06-geospatial/22-architectural-brief-locus.md) — architectural render using Flux.2 Pro.
