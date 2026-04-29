# AI Disclosure Statement Template

Per-asset and per-campaign disclosure statement template. Referenced from [`../compliance/disclosure-standards.md`](../compliance/disclosure-standards.md). Each AI-generated asset in this add-on's scope produces a completed instance of this template, archived as part of provenance documentation.

---

## Per-Asset Disclosure Statement

Use this version for individual AI-generated assets.

| Field | Value |
| :--- | :--- |
| **Asset ID** | [Unique asset identifier; project-codename + asset-name] |
| **Asset filename** | [filename.ext] |
| **Asset description** | [Short description of what the asset depicts] |
| **Project** | [Project name or codename] |
| **Sub-register** | [A / B / C — per project register declaration] |
| **Production date** | [YYYY-MM-DD] |
| **Producer** | [Designer name or vendor name] |
| **Producing organization** | [Organization name] |

### Generation Details

| Field | Value |
| :--- | :--- |
| **Primary model** | [Midjourney v7 / Nano Banana Pro / Flux.2 Pro / Ideogram v3 / Recraft V3 / GPT Image 2 / Adobe Firefly 4 / etc.] |
| **Model version** | [Specific version, including patch where known] |
| **Secondary tools** | [Compositing tools — Photoshop, Figma — and their versions] |
| **Prompt (final)** | [Final prompt as published] |
| **Prompt iteration count** | [Number of iterations to reach final] |
| **Reference images** | [References used: brand profile, srefs, in-house references, third-party references with attribution] |
| **Reference image attribution** | [Where third-party references are used, the attribution] |

### Provenance

| Field | Value |
| :--- | :--- |
| **C2PA Content Credentials applied** | [YES — manifest signed by [SIGNER IDENTITY] / NO — exception with rationale] |
| **C2PA manifest location** | [Embedded in asset metadata / Stored externally at [PATH]] |
| **SynthID embedded (if Google tools used)** | [YES / N/A] |
| **Visible disclosure language** | [Exact text of visible disclosure] |
| **Visible disclosure placement** | [Caption / colophon / footer / channel-specific note] |

### Compliance

| Field | Value |
| :--- | :--- |
| **Default rule compliance** | [Confirms compliance with default rule from `../docs/03-candidate-imagery-problem.md`] |
| **Depicts people?** | [YES / NO] |
| **People are real or fabricated?** | [Real with consent / Archetypal/composite / N/A — no people] |
| **Consent documentation (if real)** | [Reference to consent file] |
| **Representation testing (Test 1 — MST)** | [Pass / Fail / N/A — no people] |
| **Representation testing (Test 2 — Intersectional)** | [Pass / Fail / N/A — no people] |
| **Representation testing (Test 3 — Bias amplification)** | [Pass / Fail / N/A — not AI-generated humans] |
| **Failure-mode review** | [Pass — all documented failure modes checked] |
| **Reviewer name** | [Reviewer who confirmed compliance] |
| **Reviewer date** | [YYYY-MM-DD] |

### Jurisdictional Compliance

| Jurisdiction | Applicable | Compliance Posture |
| :--- | :-: | :--- |
| US Federal (Title VII et al.) | [YES] | Disparate-impact reviewed |
| Colorado AI Act | [YES — if Colorado audience] | "Reasonable care" documentation |
| Illinois HB 3773 | [YES — if Illinois audience] | Candidate notice applied |
| EU AI Act Article 50 | [YES — if EU audience and photorealistic] | Visible disclosure applied |
| EU AI Act Annex III §4 | [YES — if part of high-risk system] | Conformity documentation |
| Tennessee ELVIS Act | [YES — if Tennessee audience] | No unauthorized likeness |
| Ontario Bill 149 | [YES — if Ontario job posting] | AI-use disclosure applied |
| Quebec Law 25 §12.1 | [YES — if Quebec audience and automated decision] | Notice applied |
| UK ICO recommendations | [YES — if UK audience] | Aligned |

### Publication

| Field | Value |
| :--- | :--- |
| **Channels** | [List of publication channels] |
| **Publication date(s)** | [Per channel] |
| **Geographic scope** | [Geographies where published] |
| **Time period of use** | [Start date — End date or "ongoing"] |
| **Withdrawal triggers** | [Conditions that would trigger asset retirement] |

### Recordkeeping

| Field | Value |
| :--- | :--- |
| **Archive location** | [Project workspace path or DAM identifier] |
| **Retention end date** | [Five years from last publication date] |
| **Records included in archive** | [Prompts, model versions, references, generated assets, review notes, consent docs, disclosure language, publication records] |

---

## Per-Campaign Disclosure Statement

Use this version for multi-asset campaigns. Each asset still requires a per-asset record; the campaign statement summarizes posture across the campaign.

| Field | Value |
| :--- | :--- |
| **Campaign name** | [Campaign name] |
| **Campaign type** | [Career site refresh / EVP launch / LinkedIn campaign / multi-channel] |
| **Campaign period** | [Start date — End date] |
| **Producing organization** | [Organization name] |
| **Campaign lead** | [Lead name] |
| **Total AI-generated assets in campaign** | [N] |
| **Real photography assets in campaign** | [N] |

### Campaign-Level Compliance Posture

| Field | Value |
| :--- | :--- |
| **Default rule compliance posture** | Applied across all assets per [`../compliance/ai-imagery-policy.md`](../compliance/ai-imagery-policy.md) |
| **Disclosure standard applied** | Per [`../compliance/disclosure-standards.md`](../compliance/disclosure-standards.md) |
| **Representation testing applied** | Per [`../compliance/representation-testing.md`](../compliance/representation-testing.md) |
| **Consent process applied** | Per [`../compliance/consent-and-likeness.md`](../compliance/consent-and-likeness.md) |
| **Jurisdictions in scope** | [List of jurisdictions per campaign reach] |
| **Highest-stake assets** | [List of assets with highest compliance stakes — career site heroes, DEI report covers, etc.] |

### Campaign Asset Manifest

| Asset ID | Asset Type | Sub-Register | AI / Real / Mixed | Compliance Reviewer | Status |
| :--- | :--- | :-: | :-: | :--- | :-: |
| [ID] | [Type] | [A/B/C] | [AI/Real/Mixed] | [Reviewer] | [Approved/Pending/Rejected] |
| ... | ... | ... | ... | ... | ... |

### Sign-Off

| Role | Name | Date |
| :--- | :--- | :--- |
| Producer | [Name] | [Date] |
| Compliance reviewer | [Name] | [Date] |
| Project lead | [Name] | [Date] |
| Final approver | [Name] | [Date] |

---

## Example — Completed Per-Asset Statement (Illustrative)

The following is an illustrative example only. Real disclosure statements contain real values.

| Field | Value |
| :--- | :--- |
| Asset ID | atlassian-careers-2026-engineering-hero |
| Asset filename | atlassian-careers-2026-eng-hero-v3.jpg |
| Asset description | Career site hero for engineering roles, illustrated alternative |
| Project | Atlassian 2026 Career Site Refresh |
| Sub-register | C — Recruiting-agency editorial-illustration hybrid |
| Production date | 2026-04-15 |
| Producer | [Designer Name] |
| Producing organization | [Organization Name] |
| Primary model | Recraft V3 |
| Model version | recraft-v3 (latest 2026-Q2) |
| Prompt (final) | "Editorial illustrated workplace scene in flat-vector register..." |
| C2PA Content Credentials applied | YES — manifest signed by [Organization C2PA Identity] |
| Visible disclosure language | "Image generated with AI. Real employees featured throughout this site." |
| Default rule compliance | YES — illustrated alternative, no photo-real human subjects |
| Reviewer name | [Reviewer Name] |
| Reviewer date | 2026-04-18 |
| Channels | atlassian.com/careers, LinkedIn, Indeed |
| Publication date | 2026-05-01 |
| Retention end date | 2031-05-01 |

## Related

- [Templates README](./README.md)
- [AI imagery policy](../compliance/ai-imagery-policy.md)
- [Disclosure standards](../compliance/disclosure-standards.md)
- [Representation testing](../compliance/representation-testing.md)
- [Consent and likeness](../compliance/consent-and-likeness.md)
- [Jurisdiction matrix](../compliance/jurisdiction-matrix.md)
