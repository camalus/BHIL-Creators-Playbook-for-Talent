# 06 · Skills Graph Network

A glowing force-directed network of dots and lines representing a skills ontology, capability map, or organizational skills inventory. The signature visual for "skills intelligence" platforms.

| Field | Value |
| :--- | :--- |
| **Use case** | Standalone skills graph visualization for marketing pages, product features, conference materials, vendor decks. |
| **Sub-register** | B — Talent-intelligence platform dashboard |
| **Recommended model** | Flux.2 Pro (best for glow-on-dark photographic register) or Recraft V3 (best for vector-style precision). |
| **Aspect ratio** | 16:9 landscape (1920×1080), 1:1 square (1080×1080), or 4:5 portrait (1080×1350) for social. |
| **Production tier** | 2 — Mid-tier |
| **Compliance posture** | Skill labels must not unintentionally surface protected characteristics. Synthetic data only; no real employee skill mapping without consent. |

## Prompt — Flux.2 Pro

```text
force-directed skills graph network. dark gradient mesh ground: deep navy #0A0F1E to
near-black #050810, with subtle [PLATFORM ACCENT 1] glow at lower-left and [PLATFORM
ACCENT 2] glow at upper-right. dozens of glowing nodes scattered across the frame -
nodes as soft dots with 30-50% opacity bloom in [PLATFORM ACCENT 1]. thin glowing edges
connecting nodes - thinner edges (0.5pt visual) for weak relationships, thicker (2pt) for
strong. one focal node center-frame brighter and slightly larger, in [PLATFORM ACCENT 2],
with its first-degree connections highlighted at higher intensity. select labeled nodes
in white sans-serif type at 9-11pt: "Python", "machine learning", "data engineering",
"product strategy", "regulatory compliance" - synthetic sample skills only. unlabeled
nodes float in supporting role. legend bottom-right in 9pt white: "● node = skill ·
edge = relationship strength". cinematic depth, soft glow auras, subtle motion-blur
on a few outer nodes. eightfold capability dashboard register applied.
```

### Flux.2 Pro Configuration

| Field | Value |
| :--- | :--- |
| Model | `flux-2-pro` |
| Width × Height | `1920 × 1080` |
| Steps | 50 |
| Guidance | 4.0 |

## Prompt — Recraft V3 (vector alternative)

For a sharper, more diagrammatic register suitable for product UI mockups and printed materials.

```text
Force-directed skills graph network in vector illustration register. Dark gradient mesh
backdrop (deep navy to near-black). Glowing nodes as soft circles in [PLATFORM ACCENT 1]
with vector-clean edges. Thin connecting lines varying in weight by relationship
strength. One focal node center, brighter, larger, in [PLATFORM ACCENT 2]. Labeled
sample skills at select nodes in clean sans-serif. Legend bottom-right. Vector precision,
soft glow effects rendered as gradient overlays. Suitable for product UI compositing.
```

### Recraft V3 Configuration

| Field | Value |
| :--- | :--- |
| Model | `recraftv3` |
| Style | `vector_illustration` (or `digital_illustration` for softer feel) |
| Width × Height | `1920 × 1080` |

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[PLATFORM ACCENT 1]` | "aqua #00D4FF" | Primary node color |
| `[PLATFORM ACCENT 2]` | "orange #FF6B35" | Focal node + highlight color |
| Sample skills | 5-10 skills relevant to the platform's audience | Synthetic only |
| Node count | 30-80 visible nodes typical | Specify in prompt |
| Density | "sparse," "moderate," or "dense" | Adjusts edge count |

## Variants

### Variant A — Force-directed cloud (canonical)

The default. The graph reads as an organic cloud of skills with relationships emerging through edge density.

### Variant B — Hierarchical tree

For platforms emphasizing capability taxonomies and hierarchical skills relationships.

```text
Hierarchical skills tree on dark gradient mesh ground. A central root node at top
(brightest, largest), branching downward through three tiers of nodes. First tier:
broad capability domains. Second tier: skill clusters within each domain. Third tier:
specific skills. Edges fan out from each parent to its children. Labels on first-tier
nodes always shown; second-tier shown for selected branches; third-tier shown only when
hovered. [PLATFORM ACCENT 1] for unselected nodes; [PLATFORM ACCENT 2] for highlighted
path. Lightcast Open Skills taxonomy register applied.
```

### Variant C — Honeycomb capability matrix

For platforms emphasizing skills inventory and capability density (Workday Skills Cloud register).

```text
A honeycomb matrix of hexagonal cells on dark gradient mesh ground. Each cell represents
a skill, sized by demand and colored by category. Adjacent cells with high relationship
strength share a faint glowing edge between them. Selected cells brighter; unselected
cells at lower opacity. Legend bottom-right. Workday Skills Cloud register applied to
[PLATFORM NAME].
```

### Variant D — Constellation map

For platforms emphasizing the "discovery" or "exploration" register (Gloat Loomra orbital).

```text
Skills constellation map. Dark cosmic gradient ground (deep navy to near-black with
subtle nebula textures). Skills as glowing star nodes at varying brightness, with thin
glowing connection lines forming constellations. A central focal node "orbits" with
small satellite nodes in elliptical motion (rendered as motion-blur traces). Unlabeled
mostly; a few key skill labels visible. Gloat Loomra Knowledge Graph register applied.
```

## Failure Modes

| Failure | Symptom | Mitigation |
| :--- | :--- | :--- |
| **Generic network-graph stock register** | Output looks like generic "data network" stock | Specify "soft glow auras" + specific platform palette + "eightfold capability dashboard register" anchor |
| **Edge clutter** | Too many edges; the graph reads as visual noise | Specify density ("sparse" or "moderate"); for high-density needs, vary edge opacity by strength |
| **Off-register hard edges** | Vector-clean edges where soft-glow would be appropriate (Flux register) | Use Flux.2 Pro for soft-glow; Recraft V3 only when vector precision is the goal |
| **Skill label content surfaces protected characteristics** | Sample skills include unintended demographic associations | Use sample skills that are technical, role-functional, or industry-specific without demographic load |
| **Color palette generic SaaS** | Output uses generic blue-purple not matching platform brand | Lock [PLATFORM ACCENT 1] and [PLATFORM ACCENT 2] with specific hex codes |

## Compliance Notes

- **Synthetic data only.** No real employee skill mapping without consent. Sample skill labels are illustrative.
- **Skill labels reviewed for inadvertent demographic content.** A skills graph that consistently shows certain skill clusters surrounded by certain demographic markers can produce disparate-impact concerns even with synthetic data.
- **C2PA Content Credentials** applied at generation.
- **Visible AI disclosure** in marketing collateral best practice.
- **Five-year recordkeeping** per [`../../compliance/ai-imagery-policy.md`](../../compliance/ai-imagery-policy.md) Section 9.

## Related

- [02-talent-intelligence-platform README](./README.md)
- [Sub-register B specification](../../reference/sub-register-b-platform.md)
- [Gloat Loomra exemplar](../../reference/exemplar-library.md)
- [Flux.2 framework (Parent)](../../../../frameworks/flux-2.md)
- [Recraft V3 framework (Parent)](../../../../frameworks/recraft-v3.md)
