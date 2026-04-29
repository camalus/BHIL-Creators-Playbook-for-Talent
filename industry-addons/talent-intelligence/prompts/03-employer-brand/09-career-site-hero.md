# 09 · Career Site Hero

The dominant hero image on an employer's careers landing page. The single highest-stakes employer-brand asset because it sets candidate expectation for everything downstream.

| Field | Value |
| :--- | :--- |
| **Use case** | Hero plate on a careers landing page or top-of-funnel employer-brand campaign |
| **Sub-register** | C — Recruiting-agency editorial-illustration hybrid |
| **Recommended model** | **Real photography preferred.** Where AI is used: Recraft V3 (illustrated alternative) or Nano Banana Pro / MJ v7 (environmental, no faces) |
| **Aspect ratio** | 1920×1080 desktop hero, 750×1334 mobile hero |
| **Production tier** | 2 — Mid-tier |
| **Compliance posture** | **Highest stakes.** Real-employee photography with consent is the gold standard. AI-generated fabricated employees are prohibited. Illustrated and environmental alternatives are the permitted AI paths. |

## Default Rule Application

This prompt is the most direct application of the default rule from [`../../docs/03-candidate-imagery-problem.md`](../../docs/03-candidate-imagery-problem.md):

> **AI for abstract concept and environmental/background. Real photography (with consent and C2PA-tagged provenance) for humans wherever a viewer might mistake the subject for a real employee or candidate. Anonymous-silhouette / illustrated / environmental alternatives are the legitimate exits.**

Three permitted paths for the career site hero, in order of preference:

1. **Real employee photography.** Documentary daylight portrait of a named, consented employee in a real workplace context. This is the gold standard. AI is not used to generate the human subject.
2. **Illustrated alternative.** Recraft V3 generates an illustrated scene in the GitLab/Notion/Mailchimp register — clearly stylized, not photo-real, no chance of being mistaken for a real employee. Visible AI disclosure applied.
3. **Environmental detail.** Nano Banana Pro or MJ v7 generates a workplace environmental scene with no faces — a workspace, a window onto a city, a tooling close-up. Visible AI disclosure applied.

The fourth (prohibited) path — AI-generated photo-real "employee" — is the documented failure mode. Levi's × Lalaland, Mango Teen, and Coca-Cola Christmas all sit here.

## Prompt — Recraft V3 (Illustrated Alternative, Path 2)

For the illustrated alternative when real photography is not feasible (budget, timeline, employee unavailability):

```text
Editorial illustrated workplace scene in flat-vector register reminiscent of GitLab and
Notion brand illustration. A team of 3-4 figures collaborating around a laptop in a sunlit
modern office, faces stylized and unmistakably illustrated rather than photo-real,
gestural rather than detailed, hand-drawn quality. [BRAND ACCENT] as primary fill color
with soft cream secondary; deep navy line work. Natural daylight from a window at left,
warm cast in highlights. Generous negative space at right for headline overlay.
Stylized rather than photographic — this should not read as photography. Style: Recraft V3
illustration register, Mailchimp Collins-influenced outsider art register.
```

### Recraft V3 Configuration

| Parameter | Value | Rationale |
| :--- | :--- | :--- |
| Style | "Illustration — flat vector" or "Illustration — hand-drawn" | Avoids photo-real register |
| Palette | Brand palette + cream/ivory neutral | Single-accent register from sub-register C |
| Aspect ratio | 16:9 (desktop) or 9:16 (mobile) | Crop variants needed |

## Prompt — Nano Banana Pro (Environmental Detail, Path 3)

For the environmental workplace detail when no human subject is needed:

```text
Documentary workplace photograph, eye-level perspective, a working desk in a sunlit modern
office. Mid-day natural daylight from a window at left, warm cast in highlights, slight
desaturation. Visible: an open laptop with a code editor or design tool, a notebook with
handwritten notes, a ceramic mug, a small plant. No people in frame, no faces, no figures
implied. Slight depth-of-field, focus on the desk surface, background gently blurred.
Tailored, lived-in, real — not staged stock photography. [BRAND PROFILE] register applied
through subtle ambient color cast. Slight grain, slight desaturation, documentary
photography register.
```

### Nano Banana Pro Configuration

| Parameter | Value |
| :--- | :--- |
| Aspect ratio | 16:9 (desktop) or 9:16 (mobile) |
| Style | Documentary photography |
| Tone | Warm, natural daylight |

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[CLIENT FIRM]` | "Atlassian" | Brand context |
| `[BRAND ACCENT]` | "#0052CC" (Atlassian blue) | Sub-register C single accent |
| `[BRAND PROFILE]` | Client's brand profile | Photography palette and treatment |
| `[JOB FAMILY]` | "Engineering" / "Design" / "Sales" | Influences the workplace context shown |
| `[LOCATION ARCHETYPE]` | "open office" / "home office" / "lab" / "field" | Contextual setting |

## Variants

### Variant A — Illustrated team scene (Path 2)

The flagship recruiting-illustration register. Use for organizations leaning into illustration as authenticity hedge (GitLab, Notion, Mailchimp register).

```text
Editorial illustrated workplace scene in flat-vector register. A team of 3-4 figures
collaborating around a laptop in a sunlit modern office, faces stylized and unmistakably
illustrated.
```

### Variant B — Illustrated single subject (Path 2)

For role-specific career pages (engineering, design, etc.):

```text
Editorial illustrated portrait of a single figure at a workspace, flat-vector register,
illustrated and clearly not photo-real. The figure is in profile or three-quarter view at
a laptop, with [JOB FAMILY] context visible (a code editor, design canvas, etc.).
```

### Variant C — Environmental no-faces (Path 3)

The environmental detail when human subjects aren't needed:

```text
Documentary workplace photograph, eye-level, a working desk in a sunlit modern office.
No people in frame.
```

### Variant D — Architectural workplace (Path 3)

For organizations with distinctive architectural workplaces:

```text
Documentary architectural photograph of a modern office interior, a large open atrium with
warm natural daylight, no people visible, restrained editorial register.
```

## Compliance Notes

This prompt's compliance posture is the most stringent in the add-on:

1. **No AI-generated photo-real "employees."** Variants A, B, C, and D all comply with the default rule. A prompt asking for AI-generated photo-real employees would be a policy violation per [`../../compliance/ai-imagery-policy.md`](../../compliance/ai-imagery-policy.md) Section 4.1.

2. **Visible AI disclosure** required on any AI-generated career site hero per [`../../compliance/disclosure-standards.md`](../../compliance/disclosure-standards.md):

   > *"Image generated with AI. Real employees featured throughout this site — see [link]."*

   Placement: discreet caption immediately below the hero image, with link to a "Real Employees" page documenting which assets are AI-generated and which feature real employees.

3. **C2PA Content Credentials** applied to every generated asset.

4. **Representation testing** per [`../../compliance/representation-testing.md`](../../compliance/representation-testing.md) — even illustrated alternatives undergo the three tests; particular attention to bias amplification (Test 3) given the high candidate-facing visibility.

5. **If real photography is used** (the preferred path), full consent process per [`../../compliance/consent-and-likeness.md`](../../compliance/consent-and-likeness.md): written model release separate from employment agreement, defined scope, withdrawal rights, GDPR/CCPA-aligned processing.

## Failure Modes

| Failure Mode | What Happens | Mitigation |
| :--- | :--- | :--- |
| **Photo-real "employee" generated** | Asset reads as fabricated employee. Levi's/Mango/Coca-Cola backlash pattern. | Prompts explicitly avoid photo-real human subjects. Reviewer rejects any output reading as photo-real person. |
| **Illustration-but-actually-photoreal drift** | Recraft V3 output drifts toward photo-real. | Re-prompt with stronger illustration register cues; reject outputs that could be mistaken for photography. |
| **Diversity grid composition** | Illustrated team scene reads as performative diversity. | Match depicted diversity to comparison populations per representation testing. |
| **Stock-photo register leak** | Output reads as iStock/Getty rather than brand-specific. | Strengthen brand profile cues; reference exemplars. |
| **Disclosure missing or buried** | Visible disclosure not present or rendered too small. | WCAG AA contrast, legible weight, adjacent placement. |

## Related

- [Prompts category README](./README.md)
- [Candidate imagery decision tree](../../workflows/candidate-imagery-decision-tree.md)
- [Sub-register C specification](../../reference/sub-register-c-agency.md)
- [AI imagery policy](../../compliance/ai-imagery-policy.md)
- [Disclosure standards](../../compliance/disclosure-standards.md)
- [Representation testing](../../compliance/representation-testing.md)
- [Consent and likeness](../../compliance/consent-and-likeness.md)
- [Parent: NB Pro prompt patterns](../../../../prompts/README.md)
