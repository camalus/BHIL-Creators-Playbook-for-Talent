# 11 · EVP Pillar Treatment

The visual system for an Employer Value Proposition — typically three to five pillars, each with a custom icon, headline, and supporting visual. The Marriott "Be" framework (begin / belong / become) and CAE "Our Promise. For All." are the canonical references.

| Field | Value |
| :--- | :--- |
| **Use case** | EVP launch deck, EVP visual system, careers-page pillar block, EVP toolkit pages |
| **Sub-register** | C — Recruiting-agency editorial-illustration hybrid |
| **Recommended model** | Recraft V3 (icon system) + Ideogram v3 (typographic layout). Workflow Recipe C. |
| **Aspect ratio** | 1-page summary (1920×1080) and 50+pp toolkit (8.5×11" or A4) |
| **Production tier** | 2 — Mid-tier |
| **Compliance posture** | Icon system is fully AI-permitted (abstract). Supporting imagery follows the default rule — illustrated alternative or real photography. C2PA Content Credentials applied. |

## Format Anatomy

The Marriott "Be" reference structure, generalized:

- **Three to five pillars** (three is most common; five is the maximum that reads cleanly).
- **Each pillar has:**
  - A short word or phrase as headline (Marriott: "begin," "belong," "become" — single sentence-case verbs).
  - A custom icon in the brand register.
  - 2-3 lines of supporting copy explaining the pillar.
  - Optional supporting visual (illustrated or real-photographic).
- **Visual rhythm:** the pillars are visually parallel — same icon size, same headline weight, same copy length, same vertical spacing.

## Prompt — Recraft V3 (Icon System)

Generates the custom icon set for each pillar. The icons are clearly geometric/illustrated, not photo-real:

```text
A set of three custom icons for an EVP pillar system, in a unified flat-vector
illustration register. Each icon is geometric, simple, hand-drawn quality, with consistent
line weight (3px) and consistent style across all three. Each icon is rendered in [BRAND
ACCENT] line work on a soft cream/ivory ground. Style: flat-vector illustration in the
register of GitLab brand iconography or Notion brand iconography — geometric, restrained,
clearly illustrated rather than photo-real. Each icon should fit a 200×200 square with
generous padding. Icons are abstract metaphors for: [PILLAR 1], [PILLAR 2], [PILLAR 3].
No text, no labels, no people in the icons.
```

### Recraft V3 Configuration

| Parameter | Value |
| :--- | :--- |
| Style | "Illustration — flat vector" or "Icon — geometric" |
| Palette | Brand single accent + cream/ivory ground |
| Set generation | Generate the three icons in a single set for visual coherence |

## Prompt — Ideogram v3 (Typographic Layout)

Generates the layout that hosts the icons:

```text
EVP pillar layout, three columns side-by-side, full-bleed cream/ivory background. Each
column has: small custom icon centered at top (200×200), a short sentence-case word or
phrase headline immediately below in serif display 36pt warm navy, 2-3 lines of supporting
copy in regular sans 14pt below headline, and a faint horizontal hairline rule at column
bottom. Columns separated by generous negative space. Below the three columns: a single
banner row with the EVP framework name in serif display 28pt centered.

Pillar 1: [PILLAR 1] — "[PILLAR 1 SUPPORTING COPY]"
Pillar 2: [PILLAR 2] — "[PILLAR 2 SUPPORTING COPY]"
Pillar 3: [PILLAR 3] — "[PILLAR 3 SUPPORTING COPY]"

Framework name banner: "[EVP FRAMEWORK NAME]"

Lower-right: [CLIENT FIRM] wordmark in 14pt warm navy. Restrained, sub-register C
editorial register, lower-case sentence-case throughout, generous negative space.
```

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[CLIENT FIRM]` | "Marriott" | Brand context |
| `[BRAND ACCENT]` | "#003B7A" (Marriott navy) or client brand accent | Single accent |
| `[EVP FRAMEWORK NAME]` | "Be" or "Our Promise. For All." | The framework's name |
| `[PILLAR 1 / 2 / 3]` | "begin" / "belong" / "become" (Marriott) | Single verbs preferred; sentence-case |
| `[PILLAR N SUPPORTING COPY]` | "Begin your career with curiosity..." | 2-3 sentence supporting copy per pillar |

## Variants

### Variant A — Three-pillar grid (Marriott "Be" canonical)

Three columns, single verbs, 2-3 lines of supporting copy. The Marriott reference.

### Variant B — Five-pillar grid (CAE "Our Promise. For All." register)

Five columns side-by-side, longer pillar names, 2-3 lines of supporting copy. Requires wider format (24:9 or two-up rows of three then two).

### Variant C — Single-pillar deep dive

For toolkit pages that detail one pillar at a time. Single pillar headline + extended copy + larger icon + supporting illustrated scene from the [`09-career-site-hero.md`](./09-career-site-hero.md) prompt's illustrated alternative.

### Variant D — Manifesto layout

Pillar names treated as section headlines in a long-form manifesto document, with each section running 1-2 pages. Used for EVP launch decks and printed toolkits.

## Compliance Notes

1. **Icon system is fully AI-permitted.** Custom icons depicting abstract metaphors for pillar concepts are clearly stylized and would not be mistaken for photography. Sub-register A's full visual permissions apply — no representation testing required for abstract icons specifically.

2. **Supporting imagery follows the default rule.** Where pillar pages include supporting imagery depicting people, the default rule applies: real employee photography with consent (preferred) or illustrated alternative. Photo-real AI-generated employees are prohibited.

3. **EVP framework name as IP.** The EVP framework name (e.g., Marriott "Be") is typically trademarked or has trademark-like brand significance. Do not reuse another organization's framework names.

4. **Localization compliance.** EVP rolled out across markets must adapt to legal frameworks of each market — pillar names, supporting copy, and visual register may all require localization. The icon system typically translates more cleanly than the copy does.

5. **Visible AI disclosure** for the icon system and layout per [`../../compliance/disclosure-standards.md`](../../compliance/disclosure-standards.md). Disclosure is typically applied at the toolkit colophon level rather than per-icon.

## Failure Modes

| Failure Mode | What Happens | Mitigation |
| :--- | :--- | :--- |
| **Icon style inconsistency** | Three icons read as different illustrators' work | Generate as a set in single Recraft V3 session; reject set if any icon drifts in register |
| **Pillar names too long** | Layout breaks; reads as a wordy slogan rather than a verb-driven framework | Pillar names should be 1-3 words; verbs preferred |
| **Supporting copy too long** | Layout overflows; reads as descriptive paragraph rather than supporting copy | Supporting copy 2-3 lines / 30-50 words maximum |
| **Photo-real "employee" in supporting imagery** | Default rule violation | Use illustrated alternative or real photography |
| **Framework name conflict** | Framework name accidentally echoes another organization's trademarked framework | Trademark search before EVP launch |

## Related

- [Prompts category README](./README.md)
- [Sub-register C specification](../../reference/sub-register-c-agency.md)
- [Career site hero (related prompt)](./09-career-site-hero.md)
- [Three production tiers](../../workflows/three-production-tiers.md)
- [Parent: Recraft V3 prompt patterns](../../../../prompts/README.md)
