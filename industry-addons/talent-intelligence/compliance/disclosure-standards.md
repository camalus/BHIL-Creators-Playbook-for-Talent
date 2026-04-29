# Disclosure Standards

The technical and design implementation of disclosure for AI-generated imagery in talent and recruiting communications. Two layers: cryptographic provenance (C2PA Content Credentials) and human-readable visible disclosure.

## Two Layers, One Standard

| Layer | What It Is | Who Sees It |
| :--- | :--- | :--- |
| **Cryptographic provenance** | C2PA Content Credentials embedded in asset metadata, signed at generation | Platforms, regulators, sophisticated users; surfaced by LinkedIn, TikTok, Meta as "CR" / "AI Info" badges |
| **Visible disclosure** | Human-readable text or icon in or alongside the asset | All viewers |

Both layers apply by default to AI-generated imagery in this add-on's scope. Some assets carry only cryptographic provenance (where visible disclosure would compromise the asset, or where the AI generation is incidental — abstract texture overlay on real photography); the rationale is documented per asset.

## Layer 1 — C2PA Content Credentials

**Status:** The de facto industry standard as of 2026. Adoption (2024-2026) covers Adobe (Photoshop, Lightroom, Firefly), Microsoft (M365 February 2026), Google Pixel and DeepMind tools, Leica/Nikon/Canon/Fujifilm/Sony/Samsung cameras, OpenAI DALL-E 3 (auto-attached), Meta, and Amazon Titan. LinkedIn surfaces credentials with a "CR" icon. TikTok auto-labels with C2PA detection. YouTube has required disclosure of realistic synthetic content since March 2024. CAI membership grew from ~3,300 (September 2024) to 6,000+ (January 2026). DOD became the first US federal agency to implement C2PA (DVIDS, 2024).

### What C2PA Captures

A signed C2PA manifest captures:

- **Provenance** — what tool created the asset (Adobe Firefly, Photoshop, Microsoft Copilot, etc.), version, date.
- **Edits** — every modification applied to the asset, including AI-driven generation, edits, transformations.
- **Source ingredients** — for composite assets, every contributing source (each with its own manifest).
- **Identity** — optional cryptographic identity of the producer (who signed the manifest).
- **Custom metadata** — additional fields per producer's standard.

### Production Defaults

For every AI-generated asset in [Organization Name]'s talent and recruiting work:

1. **Generate with C2PA-supporting tools.** Default to Adobe Firefly, Adobe Photoshop with Content Credentials enabled, Microsoft M365 Copilot, Google DeepMind tools (with SynthID), OpenAI DALL-E 3 (auto-attached), and equivalent C2PA-compatible tools. Tools that do not support C2PA require justification and additional documentation per [`ai-imagery-policy.md`](./ai-imagery-policy.md) Section 5.

2. **Preserve C2PA through compositing.** When compositing in Figma, Photoshop, or other tools, the composite asset carries C2PA manifests from every source layer. Tools that strip C2PA during compositing require additional documentation and a manual provenance log entry.

3. **Sign at publication.** The final published asset is signed at publication time with the producer's cryptographic identity ([Organization Name]'s C2PA identity, registered with [REGISTRAR]).

4. **Verify on receipt** for assets received from external vendors. Vendors providing imagery without C2PA must provide alternative provenance documentation per the vendor governance section of [`ai-imagery-policy.md`](./ai-imagery-policy.md) Section 10.3.

### Production Failure Modes

- **C2PA stripped during platform upload.** Some platforms re-encode images during upload, stripping C2PA. Mitigation: monitor publication channels for C2PA preservation; for channels that strip C2PA, rely on visible disclosure plus organizational records.
- **C2PA stripped during compositing.** Naive image-tool re-encoding strips manifests. Mitigation: composite in tools that preserve metadata (Figma, Photoshop with appropriate settings).
- **Vendor non-compliance.** External vendors providing imagery without C2PA. Mitigation: contractual requirement plus vendor attestation per project.

## Layer 2 — Visible Disclosure

Visible disclosure is human-readable text or an icon in or alongside the asset. The standard varies by channel and asset type.

### When Visible Disclosure Is Required

Visible disclosure is **required** when:

1. The asset depicts (or appears to depict) a person, scene, or content that a viewer might reasonably mistake for non-AI-generated photography.
2. The asset is in a channel covered by platform AI-disclosure rules (YouTube, TikTok, Meta "Made with AI" / "AI Info").
3. The asset is in a jurisdiction with legal disclosure requirements (EU AI Act Article 50 for deepfakes, jurisdiction-specific requirements per [`jurisdiction-matrix.md`](./jurisdiction-matrix.md)).
4. The asset is in a context where disclosure functions as a competitive trust signal (career site hero, DEI report, employer-brand campaign).

Visible disclosure is **not required** (but C2PA is still applied) when:

1. The asset is clearly stylized illustration that no viewer could mistake for photography (GitLab register, Mailchimp register, Octocat register).
2. The AI generation is incidental to the asset's purpose (abstract texture overlay on real photography, where the texture is not the primary subject).
3. The asset is in a confidential / internal context (executive search dossier where the audience is the search committee only) — though visible disclosure may still be applied as a defensive practice.

### Visible Disclosure Language

Default disclosure phrases, per channel and context:

#### Career Site Hero

> *"Image generated with AI. Real employees featured throughout this site — see [link]."*

Placement: discreet caption immediately below the hero image, with link to a "Real Employees" page that documents which assets are AI-generated and which feature real employees.

#### LinkedIn / Social Media (Single Image)

> *"AI-generated image."*

Placement: in the post copy, ideally as the first line. Platform "Made with AI" / "AI Info" labels (where supported by C2PA detection) supplement.

#### Workforce Reports / DEI Reports

> *"Cover imagery generated with AI. Employee imagery throughout this report features real [Organization Name] employees with their consent."*

Placement: colophon page or copyright page.

#### Conference Keynote Backdrop

> *"Stage imagery generated with AI."*

Placement: keynote credits slide and printed program.

#### Executive Search Materials

> *"Cover imagery is illustrative and AI-generated. Candidate biographies and photographs depict real individuals with their consent."*

Placement: confidentiality notice page or first internal spread.

### Visible Disclosure Design

The visible disclosure language is rendered:

- **In a typeface and weight that is legible**, not microscopic disclaimer text designed to be missed.
- **At a contrast ratio of 4.5:1 minimum** against its background (WCAG AA).
- **Adjacent to the imagery, not separated by intervening content**, except where channel constraints require (e.g., social media post copy).
- **In the language of the audience.** For multi-language deployments, disclosure is localized.

### Channel-Specific Requirements

| Channel | Auto-Detection | Manual Label Available | Best Practice |
| :--- | :-: | :-: | :--- |
| **LinkedIn** | C2PA → "CR" icon | Yes (post copy) | C2PA + post copy first line |
| **TikTok** | C2PA detection auto-labels | Yes ("AI-generated content" toggle) | C2PA + manual toggle on |
| **Meta (FB / Instagram)** | "Made with AI" / "AI Info" | Yes ("AI Info" toggle) | C2PA + manual toggle on |
| **YouTube** | No auto-detect | Yes ("Altered or synthetic content") | Manual toggle on for any synthetic content |
| **Twitter/X** | Limited | No standardized | Caption disclosure in tweet copy |
| **Career site (own)** | N/A | N/A | Visible caption + footer note |
| **Email campaigns** | N/A | N/A | Visible caption in email body |
| **Print collateral** | N/A | N/A | Caption or colophon |

## SynthID — Complementary, Not Substitute

Google DeepMind's SynthID is an invisible watermarking technology embedded in 20B+ images by Google AI tools. It is complementary to C2PA, not a substitute:

- **SynthID is invisible.** It does not appear in the image to the viewer.
- **SynthID is robust to common transformations** (compression, cropping, modest editing).
- **SynthID detection requires Google's tooling.**
- **C2PA is the regulator-facing standard.** It carries human-readable provenance; SynthID detection is a binary "AI or not."

Where both are available (Google DeepMind tools), use both. Where only C2PA is available, use C2PA. SynthID alone is insufficient for the disclosure obligations in this add-on's scope.

## Disclosure Failure Modes

Documented failure modes from the industry record:

- **The "buried disclaimer" failure.** A 6-point disclaimer at the bottom of a colophon page does not constitute disclosure for an asset that depicted AI-generated employees prominently. The Levi's × Lalaland (2023) backlash centered on insufficient and slow disclosure.
- **The "removed during upload" failure.** C2PA stripped during platform upload, leaving no detectable provenance. Mitigation: visible disclosure as backup.
- **The "different-channel divergence" failure.** Asset has full disclosure on the website, none on the LinkedIn social variant. Multi-channel campaigns require disclosure in every channel.
- **The "invisible watermark only" failure.** SynthID alone, no C2PA, no visible disclosure. Insufficient for regulatory and trust purposes.
- **The "stylized illustration but actually photo-real" failure.** Asset described internally as "stylized illustration" but actually photo-real enough to confuse viewers. The trigger for visible disclosure is *whether viewers might reasonably mistake the asset*, not the producer's classification.

## Asset-Level Disclosure Statement

For each AI-generated asset, [Organization Name] produces a per-asset disclosure statement using [`../templates/ai-disclosure-statement-template.md`](../templates/ai-disclosure-statement-template.md). This statement is part of the provenance archive (per [`ai-imagery-policy.md`](./ai-imagery-policy.md) Section 9).

## Related

- [Compliance README](./README.md)
- [AI imagery policy](./ai-imagery-policy.md)
- [Jurisdiction matrix](./jurisdiction-matrix.md)
- [Consent and likeness](./consent-and-likeness.md)
- [AI disclosure statement template](../templates/ai-disclosure-statement-template.md)
- [Candidate imagery decision tree](../workflows/candidate-imagery-decision-tree.md)
