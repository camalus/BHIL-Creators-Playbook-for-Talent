# Jurisdiction Matrix

Per-jurisdiction obligations for AI imagery in talent and recruiting communications. Current as of April 2026.

This matrix documents the regulatory landscape; it does not constitute legal advice. Counsel review is required for any production decision based on this matrix.

## Multi-Jurisdiction Default

**For multi-jurisdiction projects (US + EU + UK + Canada), apply the most stringent applicable obligations across all dimensions.** This produces a defensible posture across all jurisdictions and avoids the operational complexity of per-jurisdiction asset variants. The cost is occasionally over-compliant for single-jurisdiction work; the benefit is one production posture instead of N.

## United States — Federal

### Title VII / ADEA / ADA / GINA / EPA

**Status:** Active. Statutes in force.

**Application to AI imagery:** Anti-discrimination law treats imagery as part of recruiting practices under EEOC Compliance Manual Section 15. Disparate-impact analysis applies to AI-generated imagery: an asset that systematically excludes or stereotypes protected groups can produce liability regardless of intent. *Mobley v. Workday* (N.D. Cal., No. 3:23-cv-00770) was conditionally certified as an ADEA collective on May 16, 2025 with potential reach in the hundreds of millions of applicants. *EEOC v. iTutorGroup* (E.D.N.Y., 2023) settled for $365,000 + 5-year injunctive relief.

**Operational obligations:** Representation testing per [`representation-testing.md`](./representation-testing.md). Documented review process. Five-year recordkeeping (aligning with OFCCP).

### EEOC AI Guidance — Withdrawn

**Status:** The May 2023 EEOC guidance "Assessing Adverse Impact in Software, Algorithms, and Artificial Intelligence Used in Employment Selection Procedures" was removed from the EEOC website on January 27, 2025 following the Trump AI Executive Order revoking EO 14110.

**Application:** The underlying statutes (Title VII, ADEA, etc.) remain in force. The withdrawn guidance had described the EEOC's interpretation; absent the guidance, employers should rely on the underlying statutory text and litigation precedent.

### OFCCP AI Guidance — Retained

**Status:** April 29, 2024 *Artificial Intelligence and Equal Employment Opportunity for Federal Contractors* remains on the OFCCP website and is the most current federal touchstone.

**Application to AI imagery:** Federal contractors must monitor AI-driven recruiting and selection tools (including imagery used in recruiting) for disparate impact. Recordkeeping requirements (10-year retention for some categories) align with the five-year minimum in this add-on's policy and may require longer retention for specific assets.

## United States — State

### Colorado — AI Act SB 24-205

**Effective:** June 30, 2026 (delayed from February 1, 2026 by August 2025 special session).

**Scope:** "Consequential decisions" including employment decisions. AI imagery in recruiting may fall within scope where the imagery is part of a system that contributes to selection decisions.

**Operational obligations:**
- Risk management policy.
- Annual impact assessment.
- Notice to consumers (candidates) when AI is used in consequential decisions.
- "Reasonable care" duty to avoid algorithmic discrimination.

**Production posture:** Default to NIST AI RMF GOVERN/MAP/MEASURE/MANAGE as the umbrella governance framework supporting "reasonable care" defensibility.

### Illinois — HB 3773 (Amending Illinois Human Rights Act)

**Effective:** January 1, 2026.

**Scope:** Employer use of AI in recruiting, hiring, promotion, demotion, discharge, discipline, tenure, or terms of employment.

**Operational obligations:** Notice to candidates and employees when AI is used.

### Illinois — AI Video Interview Act (820 ILCS 42)

**Effective:** January 1, 2020. Amended subsequently.

**Scope:** AI analysis of video interviews specifically. Adjacent to imagery: covers facial-analysis AI in interviews.

**Operational obligations:** Candidate notice; consent; demographic data collection; race-and-ethnicity reporting.

### NYC — Local Law 144

**Effective:** July 5, 2023.

**Scope:** Automated Employment Decision Tools (AEDTs) producing scores, classifications, or recommendations used in hiring or promotion decisions in NYC.

**Application to AI imagery:** Limited direct application — imagery itself is not typically an AEDT. However, programmatic ad-targeting that selects which images to show which candidates can be in scope.

**Operational obligations:** Annual independent bias audit of in-scope tools; candidate notice; result publication.

### Maryland — HB 1202

**Effective:** October 2020.

**Scope:** Facial recognition / facial template use in employment interviews specifically.

**Operational obligations:** Applicant consent.

### Tennessee — ELVIS Act

**Effective:** July 1, 2024.

**Scope:** Civil and Class A misdemeanor liability for unauthorized AI replicas of voice or likeness.

**Application to AI imagery:** Direct application. AI-generated imagery resembling a real, identifiable individual without consent is exposed.

**Operational obligations:** No AI-generated likeness of real persons without documented consent.

### California

**Status (as of April 2026):** AB 2930, SB 7 ("No Robo Bosses"), and AB 1018 all failed in the 2025 sessions. Reintroductions are expected. Existing California Consumer Privacy Act / California Privacy Rights Act obligations apply to candidate personal data including imagery.

## European Union

### EU AI Act — Regulation (EU) 2024/1689

**High-risk obligations effective:** August 2, 2026.

**Scope (Annex III §4):** AI systems used "to recruit or select natural persons, in particular to place targeted job advertisements, to analyse and filter job applications, and to evaluate candidates."

**Application to AI imagery:** Recruitment AI imagery falls within the scope where the imagery is part of an in-scope system. Standalone imagery may not always be in scope, but imagery in recruiting communication systems, programmatic ad-targeting, and candidate-facing interfaces commonly are.

**Operational obligations:**
- Risk management system.
- Data and data governance.
- Technical documentation.
- Record-keeping (logs).
- Transparency and provision of information to deployers.
- Human oversight.
- Accuracy, robustness, cybersecurity.
- Conformity assessment, CE marking, registration in the EU AI database.

### EU AI Act — Article 50 (Transparency for Deepfakes)

**Effective:** August 2, 2026.

**Scope:** "AI system that generates or manipulates image, audio or video content constituting a deep fake" must be disclosed.

**Application to AI imagery:** Photorealistic AI-generated employer-brand imagery resembling real-looking people is in scope. Clearly stylized illustration is generally out of scope but should still carry disclosure.

**Operational obligations:** Clear and visible disclosure of synthetic content. The Code of Practice on AI Labelling and Transparency final version is expected June 2026.

### GDPR — Article 35 DPIAs

**Status:** In force.

**Application to AI imagery:** DPIAs apply to AI training on candidate or employee imagery. Per-asset consent and lawful-basis documentation required.

## United Kingdom

### UK ICO Recommendations — November 6, 2024

**Status:** Recommendations from the *AI in Recruitment Outcomes Report*, ~300 recommendations across seven themes (fairness, transparency, accountability, etc.).

**Application:** Not law, but ICO-authority recommendations carry weight in regulatory action and litigation. Production posture should align with ICO recommendations.

### UK GDPR

**Status:** In force (post-Brexit equivalent of EU GDPR).

**Application:** Same DPIA obligations as EU GDPR for candidate imagery.

## Canada

### Federal — AIDA (Artificial Intelligence and Data Act)

**Status:** Bill C-27 stalled as of April 2026. Federal AI law not yet in force.

### Quebec — Law 25 §12.1

**Status:** In force.

**Application:** Notice required for exclusively-automated decisions; Commission d'accès à l'information disclosure required ≥60 days before biometric database creation.

### Ontario — Working for Workers Four Act (Bill 149)

**Effective:** January 1, 2026.

**Scope:** AI use disclosure in publicly advertised job postings for employers with ≥25 employees in Ontario.

**Operational obligations:** Disclosure when AI is used in screening, assessment, or selection.

## Cross-Cutting — C2PA Content Credentials

**Status:** Industry standard. Not a regulatory requirement in any jurisdiction as of April 2026, but operationally treated as a default by major platforms (LinkedIn, TikTok, Meta, YouTube auto-labeling) and supports compliance with disclosure obligations across multiple jurisdictions.

**Operational posture:** Default to C2PA per [`disclosure-standards.md`](./disclosure-standards.md).

## Cross-Jurisdiction Compliance Checklist

For multi-jurisdiction projects:

- [ ] **EU AI Act Article 50** — visible disclosure on deepfake-equivalent imagery.
- [ ] **EU AI Act high-risk obligations** — applicable August 2, 2026; risk management and conformity assessment for in-scope systems.
- [ ] **GDPR / UK GDPR / Quebec Law 25** — DPIA, lawful basis, data subject rights for candidate imagery.
- [ ] **Colorado AI Act** — risk management policy and annual impact assessment for "consequential decision" systems.
- [ ] **Illinois HB 3773** — candidate notice when AI used in recruiting.
- [ ] **Illinois AIVIA** — covered if video interviews are in scope.
- [ ] **NYC Local Law 144** — applicable if AEDTs are in NYC scope.
- [ ] **Maryland HB 1202** — applicable if facial recognition in interviews.
- [ ] **Tennessee ELVIS Act** — no AI likeness of real persons without consent.
- [ ] **Ontario Bill 149** — disclosure in publicly advertised job postings (≥25 employees).
- [ ] **UK ICO recommendations** — alignment with the ~300 recommendations.
- [ ] **Title VII / ADEA / ADA / GINA / EPA** — disparate impact testing on AI imagery.
- [ ] **OFCCP guidance** — federal contractor obligations.
- [ ] **C2PA Content Credentials** — applied as default.
- [ ] **Five-year recordkeeping** — provenance archive maintained.

## Update Cadence

This matrix is updated on a quarterly cadence and on material regulatory changes. Production teams should consult the most current version before each project.

## Related

- [Compliance README](./README.md)
- [AI imagery policy](./ai-imagery-policy.md)
- [Disclosure standards](./disclosure-standards.md)
- [Representation testing](./representation-testing.md)
- [Consent and likeness](./consent-and-likeness.md)
