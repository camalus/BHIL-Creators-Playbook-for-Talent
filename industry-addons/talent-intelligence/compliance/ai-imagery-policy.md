# AI Imagery Policy Template

A defensible-by-default policy template for AI-generated imagery in talent intelligence and recruiting contexts. Adapt to your organization's posture; have counsel review before ratification.

This template assumes a global organization with US, EU, UK, and Canadian footprint. Single-jurisdiction organizations should still adopt the most stringent applicable provisions to retain optionality if they expand.

---

## [ORGANIZATION NAME] — AI Imagery in Talent and Recruiting Communications

### Effective: [DATE] · Version: [N.N] · Owner: [ROLE]

---

### 1. Purpose

This policy governs the use of AI-generated and AI-modified imagery in [Organization Name]'s recruiting, employer brand, talent intelligence, and external talent communications. It establishes the default rule, the permitted uses, the prohibited uses, the disclosure requirements, the consent requirements, and the recordkeeping requirements.

This policy applies to:

- Career site imagery, including hero plates, secondary imagery, role-specific imagery, and benefits / culture imagery.
- Recruiting marketing assets across LinkedIn, Indeed, Glassdoor, Twitter/X, TikTok, Instagram, Facebook, and other paid and organic channels.
- Workforce reports, salary guides, EVP communications, and DEI reports.
- Internal and external talent intelligence visualizations, dashboards, and decks.
- Conference materials, including keynote backdrops, booth graphics, and sponsorship assets.
- Executive search dossiers, leadership briefs, and board search materials.
- Any asset where a candidate, employee, or member of the public could reasonably encounter the imagery in a talent or recruiting context.

This policy does not govern:

- Internal HR-systems UI imagery (employee handbook diagrams, HRIS interfaces).
- Imagery in non-recruiting contexts (product marketing, customer-facing communications outside talent).
- Imagery in agreements, legal documents, or compliance disclosures themselves.

### 2. The Default Rule

> **AI for abstract concept and environmental/background. Real photography (with consent and C2PA-tagged provenance) for humans wherever a viewer might mistake the subject for a real employee or candidate. Anonymous-silhouette / illustrated / environmental alternatives are the legitimate exits.**

Every asset produced under this policy declares its compliance with the default rule. Where the rule is not followed, the deviation is documented and authorized in writing by [APPROVING ROLE].

### 3. Permitted Uses of AI-Generated Imagery

AI-generated imagery is permitted for:

**3.1 Abstract concept illustration.** Skills graphs, talent-flow diagrams, capability maps, dashboard hero plates, organizational schematics, and similar visualizations that do not depict real or fabricated people as the primary subject.

**3.2 Environmental and background scenes.** Workplace details (workspace, window, hallway, tooling) without identifiable faces, atmospheric backgrounds, architectural metaphor photography (mountains, buildings, sky, abstract structures).

**3.3 Clearly stylized illustrations.** Illustrated alternatives in the GitLab, GitHub Octocat, Notion, Mailchimp, or Salesforce Trailblazer register — imagery that is obviously not photo-real and would not be mistaken for a photograph of a real person.

**3.4 Document props and editorial textures.** Paper grain, topographic engravings, abstract data art, and similar background texture work.

**3.5 Composite archetypal persons in templates and explainers.** Imagery depicting a clearly archetypal/composite person — used solely for templates, explainers, training materials, and example assets — provided that:
   - The image is not used as a final candidate-facing asset.
   - The image carries visible AI disclosure (per Section 5).
   - The image passes representation testing (per Section 8).
   - The image cannot be reasonably mistaken for a real, identifiable individual.

**3.6 AI-modified real photography** (e.g., background removal, lighting correction, color grading) provided the modifications do not create misleading representation of the person depicted, and provided the underlying photograph carries documented consent.

### 4. Prohibited Uses of AI-Generated Imagery

AI-generated imagery is prohibited for:

**4.1 Career site hero imagery featuring fabricated employees.** Career site heroes that depict AI-generated "employees" are the principal failure mode in this category. Real photography with consent is required for career site hero personification, or anonymous-silhouette / illustrated alternatives.

**4.2 DEI report imagery featuring synthetic diversity.** AI-generated demographically-varied employees who don't actually exist. Architectural restraint, named-employee storytelling, or data-led abstract are the alternatives. The Levi's × Lalaland (2023), Mango Teen (2024), Coca-Cola (2024-2025), and Google Gemini (2024) reference cases inform this prohibition.

**4.3 Executive bio plates or leadership briefs featuring AI-generated portraits of real or fabricated executives.** Real photography only for representation of named individuals; clearly archetypal-only AI imagery for templates and explainers.

**4.4 Recruiter campaign tiles featuring AI-generated quoted "employees."** Quote attribution requires consent for the named employee; AI-generated photo of the quoted employee is impermissible.

**4.5 Any AI-generated imagery resembling a real, identifiable individual** without that individual's documented consent, regardless of context. This is a Tennessee ELVIS Act, state right-of-publicity, and EU AI Act Article 50 deepfake exposure.

**4.6 Imagery depicting protected characteristics in ways that would constitute disparate-impact violations** under Title VII, ADEA, ADA, GINA, EPA, or equivalent state and international anti-discrimination law. Representation testing (Section 8) is the operational test.

**4.7 Imagery in jurisdictions where AI-generated imagery in recruiting is restricted by law,** including but not limited to: jurisdictions where the EU AI Act Article 50 transparency obligations apply without conformant disclosure, Tennessee for any unauthorized likeness, and other jurisdictions per the jurisdiction matrix.

### 5. Disclosure Requirements

All AI-generated imagery used in recruiting and talent communications carries:

**5.1 C2PA Content Credentials** embedded in the asset's metadata, signed at generation time. Production tools default to Adobe Firefly, Photoshop with Content Credentials, Microsoft M365, Google DeepMind tools (with SynthID), OpenAI DALL-E 3 (auto-attached), and equivalent C2PA-compatible tools. Composite assets carry C2PA signatures from each contributing source layer.

**5.2 Visible disclosure** for assets in which a viewer might reasonably mistake the depicted person, scene, or content for non-AI-generated. The visible disclosure language is documented in [`disclosure-standards.md`](./disclosure-standards.md) and adapted per channel.

**5.3 Provenance documentation** in the asset metadata: the prompt, the model and version, the reference images used, the generation date, the reviewer's identity, and the representation test results. This documentation is retained per Section 9.

### 6. Consent Requirements

Where imagery depicts real people, [Organization Name] obtains and documents:

**6.1 Written model release** separate from the employment agreement. The release defines:
   - Channels of use (career site, social media, paid advertising, internal materials, etc.).
   - Geographies of use.
   - Time period of use (typically 1-3 years; longer periods require renewal).
   - Whether the imagery may be used to train AI systems (default: no).
   - Withdrawal rights (the depicted person can revoke consent at any time, with operational implications for asset removal).

**6.2 Re-confirmation upon employment status change.** When a depicted employee's employment status changes (departure, role change, location change), the imagery is either retired or re-confirmed.

**6.3 GDPR / CCPA / equivalent privacy compliance.** Personal data (the photograph) is processed under documented lawful basis; data subject rights (access, deletion, portability) are honored.

### 7. Production Process

**7.1 Pre-production.** Each project begins with a deliverable spec (per [`../templates/employer-brand-spec-template.md`](../templates/employer-brand-spec-template.md) or [`../templates/candidate-dossier-template.md`](../templates/candidate-dossier-template.md)) that declares the sub-register, the assets to be produced, the imagery sources, the consent requirements, and the compliance review requirements.

**7.2 Generation.** AI generation tools are used per the production-tier guidance in [`../workflows/three-production-tiers.md`](../workflows/three-production-tiers.md). Tools must support C2PA Content Credentials by default.

**7.3 Review.** Every asset undergoes review by a designated reviewer ([REVIEWER ROLE]) who confirms compliance with this policy, applies representation testing (Section 8), and signs off in the asset's provenance documentation.

**7.4 Approval and publication.** Final approval rests with [APPROVING ROLE]. Published assets carry their disclosure per Section 5.

**7.5 Archival.** Approved assets and their provenance documentation are archived per Section 9.

### 8. Representation Testing

Every asset depicting people undergoes representation testing per the protocols in [`representation-testing.md`](./representation-testing.md). At minimum:

**8.1 Monk Skin Tone Scale audit** — for assets depicting people, the asset's skin-tone distribution is compared to the Monk Skin Tone Scale 10-point scale and benchmarked against the target audience's actual demographic distribution.

**8.2 Intersectional audit** — for assets or campaigns depicting multiple people, the intersectional representation (race × gender × age × ability × etc.) is compared to the target audience's actual intersectional distribution.

**8.3 Bias amplification check** — for AI-generated imagery, the prompt and output are checked against documented model biases (Bloomberg June 2023 Stable Diffusion audit, Wilson-Ghosh-Caliskan 2024-2025 University of Washington findings).

**8.4 Failure-mode review** — every asset is checked against the documented failure cases (Levi's × Lalaland, Mango Teen, Coca-Cola, Google Gemini) and similar patterns.

Assets failing representation testing are rejected, regenerated, or modified before publication.

### 9. Recordkeeping

[Organization Name] retains the following for every asset for **five years minimum** from the asset's last published date:

- The deliverable spec.
- The prompts (including all iteration history).
- The model and version used.
- The reference images.
- The generation date.
- The reviewer's identity and review notes.
- The representation test results.
- The consent documentation (where applicable).
- The disclosure language and placement.
- The publication channels and dates.
- Any modifications or retirements.

Five-year retention aligns with OFCCP requirements (US federal contractors) and provides headroom for the EU AI Act high-risk recruitment obligations and Colorado AI Act "reasonable care" defensibility.

### 10. Governance

**10.1 Policy ownership.** This policy is owned by [POLICY OWNER ROLE] and reviewed at least annually. Material changes require [APPROVING ROLE] sign-off.

**10.2 Training.** All [Organization Name] talent acquisition, employer brand, talent intelligence, and external communications staff receive training on this policy at hire and annually.

**10.3 Vendor governance.** Vendors producing imagery on behalf of [Organization Name] (agencies, freelancers, design partners) are contractually bound to this policy and provide attestation per project.

**10.4 Incidents.** Material policy violations are reported to [INCIDENT ROLE] and remediated. The remediation, including any external disclosure, is documented in the policy violation log.

**10.5 Updates.** Regulatory changes are monitored by [LEGAL/COMPLIANCE ROLE] and incorporated into this policy as required.

---

## Implementation Notes

When adapting this template for your organization:

- Replace all bracketed roles and dates with your organization's specifics.
- Have counsel review the entire document, with particular attention to the prohibited-uses list (Section 4) and the consent requirements (Section 6).
- Coordinate with your privacy team on Section 6.3 to align with your existing GDPR / CCPA practices.
- Coordinate with your records management team on Section 9 to align with your existing retention practices.
- For organizations operating in jurisdictions outside US/EU/UK/Canada, expand the jurisdiction matrix and adapt obligations accordingly.

## Related

- [Compliance README](./README.md)
- [Disclosure standards](./disclosure-standards.md)
- [Jurisdiction matrix](./jurisdiction-matrix.md)
- [Representation testing](./representation-testing.md)
- [Consent and likeness](./consent-and-likeness.md)
- [AI disclosure statement template](../templates/ai-disclosure-statement-template.md)
- [Candidate imagery decision tree](../workflows/candidate-imagery-decision-tree.md)
