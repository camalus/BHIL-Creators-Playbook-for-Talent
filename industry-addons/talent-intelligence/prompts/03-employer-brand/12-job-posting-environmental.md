# 12 · Job Posting Environmental

The hero image at the top of a job posting (LinkedIn req page, careers-site detail page, or job-board listing). The "workplace environmental detail with no faces" register is now standard, sidestepping the candidate-imagery problem entirely.

| Field | Value |
| :--- | :--- |
| **Use case** | Job posting hero image, LinkedIn req page, careers-site role detail page, job-board listing |
| **Sub-register** | C — Recruiting-agency editorial-illustration hybrid |
| **Recommended model** | Nano Banana Pro / Midjourney v7 (environmental, no faces) |
| **Aspect ratio** | 1600×400 LinkedIn req banner, 1200×630 OG/social, 1920×400 careers-site detail |
| **Production tier** | 1 — Fast iteration |
| **Compliance posture** | Lower-stakes than career site hero. Environmental imagery without people sidesteps consent and likeness concerns. AI disclosure applied per channel standards. |

## Format Anatomy

The "workplace environmental detail" convention (Atlassian job detail pages, Stripe job postings, Notion careers detail) is now the dominant pattern for high-quality job postings:

- **No faces, no figures.** A workspace, a window onto a city, a tooling close-up, a team artifact (whiteboard, sticky notes, code on screen).
- **Documentary daylight register.** Natural light, slight grain, slight desaturation.
- **Subtle brand color overlay or accent.** A monitor showing brand-colored UI, a brand-colored object on the desk, or a subtle color cast.
- **Department/team context.** The environmental scene cues the role (engineering desk for engineering roles, design table for design roles, manufacturing floor for operations roles, etc.).

## Prompt — Nano Banana Pro (Generic Engineering Workplace)

The default — engineering workplace environmental:

```text
Documentary workplace photograph, eye-level, [JOB FAMILY] workspace in a modern office.
Mid-day natural daylight from a window at left, warm cast in highlights, slight
desaturation. Visible: an open laptop with a code editor, a notebook with handwritten
notes, a ceramic mug, headphones, a small plant. No people in frame, no faces, no
figures implied, no hands. Slight depth-of-field, focus on the desk surface, background
gently blurred showing a sense of an open-office context. Tailored, lived-in, real — not
staged stock photography. Slight grain, slight desaturation, documentary photography
register reminiscent of Stripe and Notion careers imagery. Subtle [BRAND ACCENT] in the
code editor on the laptop screen.
```

## Prompt — Midjourney v7 (Architectural Workplace)

For higher-stakes role postings (senior, executive) needing more architectural register:

```text
Documentary architectural photograph of a [ROLE CONTEXT] workspace in a modernist office
building, low-angle, generous natural daylight from floor-to-ceiling windows, slight
warm cast in highlights, restrained editorial palette. No people visible. Editorial
photography register. Foreign Affairs × Palantir field brief register. [BHIL profile]
--ar 8:2 --style raw --stylize 200 --v 7
```

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[CLIENT FIRM]` | "Atlassian" | Brand context |
| `[BRAND ACCENT]` | "#0052CC" or other client accent | Subtle color cast |
| `[BRAND PROFILE]` | Client's brand profile | Photographic register |
| `[JOB FAMILY]` | "Engineering" / "Design" / "Sales" / "Operations" | Drives the environmental detail |
| `[ROLE CONTEXT]` | "engineering" / "design" / "trading floor" / "lab" / "manufacturing" | Specific workplace archetype |

## Variants

### Variant A — Engineering desk (canonical)

The default. Engineering / technical role contexts.

### Variant B — Design studio

For design / creative role contexts. Substitute: design canvas, Pantone swatches, a tablet, a rolled-up technical drawing, a white-board with sketches.

### Variant C — Lab / scientific workspace

For research, science, healthcare role contexts. Substitute: scientific instruments, a microscope, lab notebooks, a window onto a lab corridor.

### Variant D — Manufacturing / operations floor

For operations, manufacturing, supply-chain role contexts. Substitute: a factory floor view, machinery in soft focus, a clipboard or tablet, safety equipment in foreground.

### Variant E — Field / outdoor workplace

For field service, energy, agriculture, outdoor role contexts. Substitute: tools laid out on a tailgate, a vehicle in the background, a job-site with no people in frame.

### Variant F — Boardroom / executive workspace

For senior leadership role contexts. Substitute: a boardroom with high-backed chairs, a window onto a city skyline, a polished surface table, no people.

## Compliance Notes

1. **No faces, no figures, no implied people.** This is the operational test. Hands, partial bodies, or implied human presence (a chair pulled out as if just-vacated) are still acceptable; full faces or figures are not. The register works because it sidesteps the candidate-imagery problem.

2. **Visible AI disclosure** per [`../../compliance/disclosure-standards.md`](../../compliance/disclosure-standards.md):

   > *"Header image generated with AI."*

   Placement: caption immediately below the hero or in the footer of the job posting page. Lower-stakes than career site hero but still required.

3. **C2PA Content Credentials** applied to the asset.

4. **Real-photography substitution.** Because no faces are required, real photography of the actual workplace is straightforward and is preferred where available. Tier 1 production speed makes AI generation attractive, but a real photograph of the actual workspace produces stronger candidate signal where time and access allow.

5. **No representation testing required for no-people assets.** Per [`../../compliance/representation-testing.md`](../../compliance/representation-testing.md), representation testing applies to assets depicting people. Variants A-F all qualify for the no-people exemption.

## Failure Modes

| Failure Mode | What Happens | Mitigation |
| :--- | :--- | :--- |
| **Faces leak in** | Output has a partial face in deep background blur | Re-generate; prompt explicitly excludes faces |
| **Stock-photo register** | Output reads as iStock/Getty rather than brand-specific | Strengthen brand profile cues; reference exemplars |
| **Wrong workplace archetype** | Engineering job posting shows lab, or vice versa | Match variant to job family |
| **Brand color too prominent** | Color overwhelms the documentary register | Reduce to subtle color cast or single brand-colored object |
| **Disclosure missing** | AI imagery without visible disclosure | Add disclosure per channel standards |

## Related

- [Prompts category README](./README.md)
- [Career site hero (related, higher stakes)](./09-career-site-hero.md)
- [Sub-register C specification](../../reference/sub-register-c-agency.md)
- [Disclosure standards](../../compliance/disclosure-standards.md)
- [Three production tiers](../../workflows/three-production-tiers.md)
- [Parent: NB Pro prompt patterns](../../../../prompts/README.md)
