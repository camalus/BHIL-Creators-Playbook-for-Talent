# 16 · Conference Keynote Backdrop

The ultra-wide LED backdrop behind a keynote speaker at an HR Tech, talent intelligence, or recruiting conference (UNLEASH, HR Tech Conference, Transform, RecFest, ERE).

| Field | Value |
| :--- | :--- |
| **Use case** | Conference stage backdrop, keynote LED graphics, sponsorship stage assets |
| **Sub-register** | B — Talent-intelligence platform dashboard |
| **Recommended model** | Midjourney v7 (gradient mesh + particle aurora) + Ideogram v3 (typographic). Workflow Recipe C. |
| **Aspect ratio** | 16:9 (1920×1080) standard; 2.5:1 (3840×1536) ultra-wide LED variant |
| **Production tier** | 2 — Mid-tier |
| **Compliance posture** | Backdrop motion clips (if generated) require Veo 3.1 / Runway provenance documentation. Conference IP licensing if recognition badges or logos used. |

## Format Anatomy

The settled convention for conference keynote backdrops in the talent intelligence / HR Tech world:

- **Ultra-wide LED format** — 16:9 standard for projection, 2.5:1 ultra-wide variant for LED stage walls.
- **Dark gradient mesh in platform brand palette** — deep purples, navy-to-black, indigo-to-black with platform accent (aqua, coral, lime, magenta).
- **Single typographic headline** — the keynote title or theme in display type, typically center-positioned or upper-third.
- **Abstract particle / aurora animation** — atmospheric particles, light streaks, or aurora-like color washes synchronized to speaker pacing (motion variant).
- **Optional brand mark** — sponsor or platform brand mark in lower-corner.
- **Optional event mark** — the conference's wordmark or session ID.

## Prompt — Midjourney v7 (Gradient Mesh + Particle Aurora)

The atmospheric base for the backdrop:

```text
Conference keynote stage backdrop, ultra-wide 2.5:1 aspect ratio. A dark gradient mesh
backdrop transitioning from deep [PLATFORM PRIMARY] in upper-left through deep navy
center to deep [PLATFORM SECONDARY] in lower-right. Atmospheric particle effect — small
glowing dots and light streaks like an aurora — in [PLATFORM ACCENT] across the
mid-ground. Soft volumetric light from upper-left suggesting stage lighting integration.
Generous negative space in the center for typographic headline overlay. No people, no
figures, no buildings. Atmospheric, theatrical, restrained. Sub-register B platform
dashboard register, Eightfold Cultivate / UNLEASH stage register. [PLATFORM PROFILE]
[PLATFORM SREFS] --ar 5:2 --style raw --stylize 300 --v 7
```

## Prompt — Ideogram v3 (Typographic Headline)

For the typographic overlay layered onto the gradient mesh:

```text
Conference keynote stage typographic overlay, ultra-wide 2.5:1 aspect ratio. Center:
editorial display headline "[KEYNOTE TITLE]" in heavy serif or humanist sans display
(Canela Deck or Inter Display register), warm ivory, 96-120pt. Below headline: subtitle
"[KEYNOTE SUBTITLE]" in regular weight italic, 32pt warm ivory, 60% opacity. Lower-left
or lower-right corner: platform brand wordmark "[PLATFORM]" small in 18pt warm ivory.
Lower-center or lower-right: event mark "[EVENT NAME] · [YEAR]" in tracked small caps,
14pt warm ivory at 70% opacity. Restrained, single typographic composition, generous
negative space, no other elements.
```

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[PLATFORM]` | "Eightfold" / "Gloat" / "Lightcast" / "Beamery" | The platform brand context |
| `[PLATFORM PROFILE]` | Platform's brand profile | Replaces parent BHIL profile for sub-register B |
| `[PLATFORM SREFS]` | Platform's style references (locked srefs from previous work) | Visual consistency across event materials |
| `[PLATFORM PRIMARY]` | "deep purple #2D1A4A" (Eightfold) | Gradient mesh upper-left |
| `[PLATFORM SECONDARY]` | "deep indigo #1A1A4A" | Gradient mesh lower-right |
| `[PLATFORM ACCENT]` | "aqua #00C4D4" / "coral #FF6B6B" / "lime #B6E55C" | Particle and aurora accent |
| `[KEYNOTE TITLE]` | "The Skills Pivot" / "The Infinite Workforce" | Keynote title |
| `[KEYNOTE SUBTITLE]` | "Talent Intelligence for the AI Era" | Editorial subtitle |
| `[EVENT NAME]` | "UNLEASH" / "Cultivate" / "HR Tech Conference" / "Transform" | Conference brand |
| `[YEAR]` | "2026" | Event year |

## Variants

### Variant A — Standard 16:9 backdrop

The projection-format default. Most conference rooms support this format.

### Variant B — Ultra-wide 2.5:1 LED backdrop

For LED stage walls (UNLEASH, large HR Tech Conference stages, Eightfold Cultivate). Ultra-wide format with the gradient mesh extending to fill the wall.

### Variant C — Multi-panel LED (3:1 or wider)

For exceptionally wide LED installations. Designed as a tileable pattern with the headline centered and the gradient mesh tileable across panels.

### Variant D — Atmospheric only (no headline)

For ambient stage moments (between keynotes, during transitions, during panel sessions). Just the gradient mesh and particle aurora; no typographic overlay.

### Variant E — Recognition-badge variant

For sponsor moments where the backdrop displays the platform's recognition badges (Fosway 9-Grid, IDC MarketScape, Brandon Hall). Substitute the keynote headline with a horizontal strip of badges. Subject to badge licensing requirements.

## Compliance Notes

1. **Recognition badges require licensing.** Using a Fosway 9-Grid badge, IDC MarketScape badge, Brandon Hall badge, or similar without entitlement is a trademark exposure. Variant E requires confirmation of badge licensing.

2. **Conference IP licensing.** Conference brand wordmarks (UNLEASH, HR Tech Conference, Transform, RecFest, ERE) are trademarks of their respective organizations. Use of these wordmarks requires sponsorship-or-speaker entitlement.

3. **Visible AI disclosure** for the backdrop:

   > *"Stage imagery generated with AI."*

   Placement: keynote credits slide and printed program. Backdrop itself does not require on-screen disclosure if the disclosure appears in the program and credits.

4. **C2PA Content Credentials** applied to the asset and (where motion is generated) to the motion variant.

5. **Motion variant provenance.** When the backdrop becomes motion (Veo 3.1 / Runway Gen-4 generated atmospheric animation), motion provenance documentation is required separately from the static backdrop.

6. **No human subjects on the backdrop.** The gradient mesh + particle aurora register is fully abstract; no representation testing concerns. If silhouettes or implied figures appear in mesh accidents, regenerate.

## Failure Modes

| Failure Mode | What Happens | Mitigation |
| :--- | :--- | :--- |
| **Headline illegible at viewing distance** | Audience can't read the headline from the back of a 1,000-seat hall | Headline weight and size tuned for stage viewing — typically 96pt+ for ultra-wide formats |
| **Gradient mesh too busy** | Particle effect competes with headline | Reduce particle density; concentrate particles in the negative-space upper or lower thirds |
| **Brand color drift** | Generated palette drifts from platform brand | Lock palette via [PLATFORM PROFILE] and srefs |
| **Unauthorized recognition badges** | Variant E uses badges the platform isn't entitled to | Confirm badge licensing per project |
| **Conference brand wordmark unauthorized** | Asset uses event brand without entitlement | Confirm sponsorship/speaker entitlement |
| **Motion provenance missing** | Motion variant generated without C2PA / Veo provenance | Document motion provenance separately |

## Related

- [Prompts category README](./README.md)
- [Sub-register B specification](../../reference/sub-register-b-platform.md)
- [Vendor pitch deck hero (related)](../02-talent-intelligence-platform/08-vendor-pitch-deck-hero.md)
- [Three production tiers](../../workflows/three-production-tiers.md)
- [Disclosure standards](../../compliance/disclosure-standards.md)
- [Parent: Workflow Recipe C](../../../../workflows/README.md)
