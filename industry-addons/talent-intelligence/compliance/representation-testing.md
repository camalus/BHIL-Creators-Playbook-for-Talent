# Representation Testing

Operational protocols for demographic representation testing of AI-generated imagery in talent and recruiting communications. Required for every asset depicting people under [`ai-imagery-policy.md`](./ai-imagery-policy.md) Section 8.

## Why Representation Testing

Three documented patterns make representation testing non-optional in this category:

1. **AI image models systematically over- and under-represent protected groups in ways that don't match real-world distributions.** The Bloomberg June 2023 Stable Diffusion bias audit documented women at 3% of "judge" images vs. 34% real-world; 70% darker-skin generation for "fast-food worker." The Wilson-Ghosh-Caliskan 2024-2025 University of Washington findings on SD XL documented persistent representational harms.

2. **AI image models can over-correct in ways that produce historical inaccuracy.** Google Gemini suspended image generation in February 2024 after over-correction produced historically inaccurate diverse Nazi soldiers — a high-profile case of correction-without-context failing badly.

3. **Synthetic-diversity backlash is documented.** Levi's × Lalaland (2023) drew immediate criticism for "artificial diversity"; Mango Teen, Coca-Cola Christmas, Guess/Vogue, and others followed. The pattern: AI-generated demographic variety that doesn't match the depicted organization's actual workforce reads as performative.

## The Three Tests

Every asset depicting people undergoes three tests:

### Test 1 — Monk Skin Tone Scale Audit

The Monk Skin Tone Scale is a 10-point scale developed by Dr. Ellis Monk and adopted by Google for representation testing. It is the contemporary standard for skin tone representation analysis, replacing the older Fitzpatrick six-point scale.

**Procedure:**

1. Identify each person depicted in the asset.
2. Classify each person's skin tone against the Monk 10-point scale (MST-1 through MST-10, lightest to darkest).
3. Tabulate the distribution of MST classifications across the asset (or campaign).
4. Compare the distribution to:
   - The actual demographic distribution of the depicted organization's workforce.
   - The actual demographic distribution of the target audience (candidates the asset will reach).
   - The actual demographic distribution of the geographic market.
5. Flag any distribution that deviates significantly from the comparison populations.

**Pass criteria:**

- The asset's distribution does not over-represent any MST band relative to the comparison populations by more than [THRESHOLD — e.g., 15 percentage points].
- The asset's distribution does not under-represent any MST band relative to the comparison populations by more than [THRESHOLD].
- The asset's distribution does not include MST bands not present in the comparison populations.

**Documentation:**

A representation test record is created for each tested asset, capturing the MST classification of each depicted person, the comparison populations used, the threshold applied, and the pass/fail result.

### Test 2 — Intersectional Audit

Single-axis testing (skin tone alone, or gender alone) misses intersectional representation patterns. Intersectional audit checks the combined distribution of multiple demographic axes.

**Procedure:**

1. Define the intersectional axes relevant to the asset: typically race/skin tone, gender presentation, age band, visible ability, and cultural markers.
2. Classify each depicted person across all relevant axes.
3. Tabulate the intersectional distribution (e.g., older Black women, young South Asian men, etc.).
4. Compare to the comparison populations.
5. Flag intersectional gaps (e.g., a campaign that depicts Black women but only as younger employees, or that depicts visible disability but only as young white men).

**Pass criteria:**

- The asset's intersectional distribution is consistent with the comparison populations.
- No intersectional band is systematically excluded.
- No intersectional band is over-represented in ways that read as tokenism (e.g., a single visibly-disabled person as the "diversity" representative across an otherwise homogeneous campaign).

### Test 3 — Bias Amplification Check

For AI-generated imagery specifically, the third test examines the prompt-to-output relationship for bias amplification.

**Procedure:**

1. Document the prompt used to generate the asset.
2. Generate 20-50 variations of the prompt (or run the same prompt 20-50 times).
3. Tabulate the demographic distribution across the variations.
4. Compare to the comparison populations and to the documented model bias literature (Bloomberg Stable Diffusion audit, Wilson-Ghosh-Caliskan SD XL findings).
5. Flag any pattern where the model systematically produces demographic distributions that don't match the prompt's intent or the target population.

**Pass criteria:**

- Variations produce demographic distributions consistent with the prompt's intent.
- The model is not systematically defaulting to a demographic that doesn't match the comparison populations.
- Where the model exhibits known bias (e.g., defaulting to lighter skin for "professional," or to younger people for "ambitious"), the prompt has been adjusted to counteract this bias and the adjustment is documented.

## Failure Mode Review

Every tested asset is also checked against documented failure modes:

| Failure Mode | What To Check For | Reference Case |
| :--- | :--- | :--- |
| **Synthetic diversity** | AI-generated demographic variety not matching the depicted organization's actual workforce | Levi's × Lalaland (2023) |
| **Tokenism** | Single representative of a protected group as the "diversity" element | Stock-photo "diversity grid" register |
| **Over-correction** | Demographic representation that produces historical or contextual inaccuracy | Google Gemini Nazi soldiers (Feb 2024) |
| **Stereotyping** | Protected groups consistently in subordinate, support, or background roles | Bloomberg Stable Diffusion audit (Jun 2023) |
| **Likeness leak** | AI-generated person resembling a recognizable real individual | Tennessee ELVIS Act exposure |
| **Erasure** | Protected groups absent from imagery despite being present in target population | DEI report covers without underrepresented employees |

## Comparison Populations

The "comparison populations" referenced in Tests 1 and 2 are the populations against which representation is benchmarked. Three layers:

1. **Depicted organization's workforce.** For employer-brand assets, the comparison is the actual demographic distribution of the organization's workforce (or the relevant business unit).
2. **Target audience.** For recruiting marketing, the comparison is the demographic distribution of candidates the asset will reach (informed by the geographic market, the job family, and the channel).
3. **Geographic market.** As a backstop, the comparison is the demographic distribution of the relevant geographic labor market.

When the three layers conflict (e.g., the organization's workforce is less diverse than the target audience), the production decision is documented and authorized in writing — the asset should not over-represent diversity beyond the workforce reality but also should not under-represent the target audience the asset is recruiting.

## Operational Workflow

```text
1. Asset generated.
2. Reviewer applies Test 1 (Monk Skin Tone Scale).
3. Reviewer applies Test 2 (intersectional).
4. Reviewer applies Test 3 (bias amplification check) for AI-generated assets.
5. Reviewer applies failure-mode review.
6. Reviewer documents results in the asset's provenance record.
7. If all tests pass: asset proceeds to approval.
8. If any test fails:
   - Asset is rejected and regenerated (preferred).
   - Or asset is modified to correct the issue.
   - Or asset is documented as an exception with [APPROVING ROLE] sign-off.
9. Re-tested asset re-enters at step 7.
```

## Tools and Resources

- **Monk Skin Tone Scale.** Reference at skintone.google.
- **Bloomberg June 2023 Stable Diffusion bias audit.** Available at bloomberg.com/graphics/2023-generative-ai-bias.
- **Wilson-Ghosh-Caliskan 2024-2025 SD XL findings.** University of Washington research.
- **Adobe Firefly representation guidance.** Adobe publishes its Firefly bias-mitigation approach.
- **Dove Real Beauty Prompt Playbook.** Open-source prompting guidance designed to reduce demographic bias.

## Limitations

Representation testing has limits this protocol acknowledges:

- **Demographic classification is itself imperfect.** Skin tone, gender presentation, age, ability, and cultural markers are observed by reviewers, who may classify differently. Use multiple reviewers for high-stakes assets.
- **Comparison populations are estimates.** Workforce demographic data, target audience demographic data, and labor market demographic data all carry uncertainty.
- **Pass criteria thresholds are organizational choices.** Different organizations may set different thresholds. Document the threshold and the rationale.
- **Testing does not produce equity.** Passing representation testing does not mean an asset, campaign, or organization is equitable. It means the asset meets the production threshold for representation; equity requires broader work.

## Related

- [Compliance README](./README.md)
- [AI imagery policy](./ai-imagery-policy.md)
- [Candidate imagery decision tree](../workflows/candidate-imagery-decision-tree.md)
- [Consent and likeness](./consent-and-likeness.md)
