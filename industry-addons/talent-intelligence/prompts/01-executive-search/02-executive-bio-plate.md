# 02 · Executive Bio Plate

A single-spread profile of a candidate or appointed executive — used in dossiers, board materials, and announcement decks. **This prompt has the strongest compliance guardrail in the add-on.**

| Field | Value |
| :--- | :--- |
| **Use case** | Single-spread executive profile for use in candidate dossiers, board materials, announcement decks. |
| **Sub-register** | A — Retained-search editorial |
| **Recommended model** | **For real candidates: real photography only — NO AI generation.** For templates and explainers: Midjourney v7 (archetypal-only) + Ideogram v3 (typographic). |
| **Aspect ratio** | 8.5×11" single page or two-page spread (17×11"). Portrait. |
| **Production tier** | 3 — Archival |
| **Compliance posture** | **Critical — strongest guardrail.** Real-candidate plates use real photography with consent, full stop. Archetypal-only AI generation for templates and explainers, never as final candidate-facing assets. Visible AI disclosure. |

## ⚠️ Critical Compliance Notice

**This deliverable depicts an executive's identity. The default rule applies:**

- **If the plate represents a real, named candidate or appointed executive: real photography only.** The candidate's actual photograph is the appropriate representation. Documented consent per [`../../compliance/consent-and-likeness.md`](../../compliance/consent-and-likeness.md) is required. AI-generated portraits of real individuals are **prohibited** under [`../../compliance/ai-imagery-policy.md`](../../compliance/ai-imagery-policy.md) Section 4.5 and exposed to Tennessee ELVIS Act, state right-of-publicity, and EU AI Act Article 50 deepfake liability.
- **If the plate is a template or explainer:** AI generation may produce a clearly archetypal/composite person, with the guardrails below. The result is never used as a final candidate-facing asset.

The prompts below produce *archetypal-only template imagery*. They are not intended for real-candidate plates.

## Prompt — Midjourney v7 (archetypal-only template imagery)

```text
Editorial executive portrait for a candidate dossier template. An archetypal senior
executive in a tailored charcoal suit, mid-50s, neutral business demeanor, photographed
seated at a polished walnut conference table, soft natural window light from upper-left,
tight chest-up framing, eyeline at upper third of frame, thoughtful gaze just off-camera.
Background blurred boardroom interior, navy and walnut tones, 1.5 stops darker than face.
No facial features that resemble any specific real person — composite, generic, archetypal
features only. No identifying details (no name badge, no jewelry, no distinctive marks).
Documentary editorial photography register, slight grain, slightly desaturated palette,
warm cast in highlights. Foreign Affairs × Palantir field brief register. [BHIL profile]
--ar 4:5 --style raw --stylize 150 --v 7
```

### Parameters

| Parameter | Value | Rationale |
| :--- | :--- | :--- |
| `--ar` | 4:5 | Vertical portrait orientation appropriate for executive plate |
| `--style raw` | raw | Documentary register |
| `--stylize` | 150 | Lower stylize for portrait realism |
| `--v` | 7 | Latest Midjourney for portrait fidelity |

## Prompt — Ideogram v3 (typographic overlay)

After generating the portrait base, composite the typographic overlay:

```text
Executive bio plate layout. Top-bleed editorial portrait covering upper 60% of page (image
generated separately). Below portrait, three-column layout. Left column: executive name in
heavy serif display (Canela Deck or GT Sectra Bold), 36-42pt; below name in tracked small
caps "[CURRENT TITLE] · [CURRENT COMPANY]" 9pt. Center column: three-paragraph bio
organized as "Career Arc / Signature Wins / Distinctions" with each section preceded by
small-caps tracked subhead, 8pt. Right column: signature wins as discreet sidebar with
metric bullets — each bullet a short statement followed by a measurement (revenue, scale,
years), 11pt body type with 9pt metric in signal-red. Page footer: "[CLIENT FIRM] ·
[PROJECT CODENAME] · [PAGE NUMBER]" in 8pt regular. Subtle paper-grain texture overlay at
8% opacity. Layout follows Korn Ferry KF Serif portrait template applied to BHIL register.
```

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[EXECUTIVE NAME]` | Real name (real-candidate plate) or "Archetypal Candidate" (template) | For real candidates: real name. For templates: clearly archetypal label. |
| `[CURRENT TITLE]` | "Chief Operating Officer" | Tracked small caps |
| `[CURRENT COMPANY]` | Real company name (real candidate) or "Confidential" (template) | |
| `[CLIENT FIRM]` | Search firm name | Footer |
| `[PROJECT CODENAME]` | "Project Aurora" | Footer |
| `[PAGE NUMBER]` | Sequential | |
| `[CAREER ARC]` | 80-120 word narrative | Three-paragraph structure |
| `[SIGNATURE WINS]` | 3-5 bullets with metrics | Sidebar |
| `[DISTINCTIONS]` | Awards, board service, publications | Optional |

## Variants

### Variant A — Real candidate (real photography brief)

This is the default for production work. The variant is not an AI prompt; it is a photography brief for a commissioned shoot or an existing licensed photograph.

```text
PHOTOGRAPHY BRIEF (not AI generation):
- Format: editorial portrait, 8x10 sensor or 35mm full-frame.
- Lighting: soft single-source key at 45°, fill at 30%. Natural window or large softbox.
  Background 1.5 stops darker than face.
- Framing: chest-up. Eyeline at upper third. Direct-to-camera or thoughtful off-camera.
- Wardrobe: tailored business attire. No pattern louder than fine pinstripe.
- Background: blurred boardroom or neutral wall. No identifying details.
- Treatment: documentary editorial register. Slight grain. Slightly desaturated palette.
- Consent: written model release per consent-and-likeness.md before shoot.
- Provenance: photographer's identity documented; C2PA Content Credentials applied at
  capture or post-production.
```

### Variant B — Archetypal-only AI template (canonical AI variant)

The Midjourney prompt above. Used for template assets, training materials, and explainers. Never as final real-candidate plates.

### Variant C — Anonymous-silhouette alternative

For dossier longlists where individual identification is reserved for later stages.

```text
Editorial executive plate with anonymous silhouette. A featureless gray silhouette in
chest-up framing, on a slightly textured warm-ivory ground. To the right of the silhouette,
small-caps role-and-industry descriptor in deep navy ("CFO · TOP-5 GLOBAL BANK"), 9pt.
Below, three-paragraph bio with name redacted as "███████" and company as "███████".
Footer carries codename only. Foreign Affairs editorial register. [BHIL profile] --ar 4:5
--style raw --stylize 100 --v 7
```

### Variant D — Editorial environment over portrait

For executive plates where the workplace context is more telling than the portrait itself.

```text
Editorial environmental detail in place of portrait: an executive's office artifacts —
a desk corner with annotated reports, a fountain pen on a leather blotter, a half-filled
coffee cup, light through a window onto walnut surfaces. No face, no full figure. Tight
selective focus on a single artifact. Documentary photography register. [BHIL profile]
--ar 4:5 --style raw --stylize 150 --v 7
```

## Failure Modes

| Failure | Symptom | Mitigation |
| :--- | :--- | :--- |
| **Real-person resemblance leak** | Generated portrait closely resembles a recognizable real individual | Reverse-image-search check before use; if any resemblance > 70%, regenerate with adjusted prompt |
| **Over-stylized "AI face" register** | Generated portrait reads as an AI portrait — uncanny-valley features, smooth skin, generic boardroom-stock energy | Use `--style raw`, lower `--stylize`, add specific compositional anchors (window light, walnut conference table) |
| **Used as final asset** | Archetypal-only template image deployed as a real-candidate plate | **Critical violation.** Process control: every plate must declare whether it represents a real candidate (real photo only) or a template (AI archetypal allowed) per the spec template. |
| **Compliance documentation gap** | No record of prompt, generation date, reviewer | Use the asset-level disclosure template per [`../../templates/ai-disclosure-statement-template.md`](../../templates/ai-disclosure-statement-template.md) |
| **Over-confident demographic specification** | Prompt produces only one demographic across many runs | Run 20-50 variations; tabulate per [`../../compliance/representation-testing.md`](../../compliance/representation-testing.md); adjust prompt language to broaden distribution |

## Compliance Notes

- **Real-candidate plates: real photography only.** Per [`../../compliance/ai-imagery-policy.md`](../../compliance/ai-imagery-policy.md) Section 4.3 and [`../../compliance/consent-and-likeness.md`](../../compliance/consent-and-likeness.md). No exceptions. AI-generated portraits of real candidates are prohibited.
- **Archetypal-only template imagery: tightly constrained.** Use only for templates, explainers, training materials. Never deployed as final candidate-facing assets.
- **Visible AI disclosure** required on archetypal-only template imagery. Asset-level disclosure per [`../../templates/ai-disclosure-statement-template.md`](../../templates/ai-disclosure-statement-template.md).
- **Representation testing** applied to every plate. Bias amplification check (Test 3 in [`../../compliance/representation-testing.md`](../../compliance/representation-testing.md)) is critical here — single archetypal portraits must be reviewed against a 20-50 variation distribution to confirm the model is not systematically defaulting to a single demographic.
- **Reverse-image-search resemblance check** for every AI-generated portrait. Document the check result in the asset's provenance archive.
- **Five-year recordkeeping** per [`../../compliance/ai-imagery-policy.md`](../../compliance/ai-imagery-policy.md) Section 9.
- **Tennessee ELVIS Act exposure** if any real-person resemblance leaks; reverse-image-search check is a critical mitigation.

## Related

- [01-executive-search README](./README.md)
- [Sub-register A specification](../../reference/sub-register-a-retained-search.md)
- [AI imagery policy](../../compliance/ai-imagery-policy.md)
- [Consent and likeness](../../compliance/consent-and-likeness.md)
- [Representation testing](../../compliance/representation-testing.md)
- [Candidate Dossier Spec Template](../../templates/candidate-dossier-template.md)
- [Candidate Imagery Decision Tree](../../workflows/candidate-imagery-decision-tree.md)
