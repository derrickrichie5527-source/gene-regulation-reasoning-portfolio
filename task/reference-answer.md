# Reference answers: questions 1-3

## Q1 - A stable ratio can hide two changing quantities

Control delta-Cq = 25 - 20 = 5. Treated delta-Cq = 24 - 19 = 5. Delta-delta-Cq = 0, so the reported target/H fold change is 2^0 = 1.

But H per cell doubles. Target per cell therefore changes by 1 x 2 = 2-fold. The one-cycle reduction in target Cq is consistent with that result under the equal-input and amplification assumptions. H is an unsuitable invariant reference here. The ratio was unchanged; target abundance was not. Recovery matching and valid independent H calibration are essential. [S1; original calculation]

## Q2 - Equal captured signal is not equal production

Control corrected signal = 100 / 0.80 = 125. Treatment = 100 / 0.40 = 250. Treated/control = 2.

Under the matched-incorporation and short-pulse assumptions, this supports approximately twice as much RNA production per cell during that window. It does not prove direct promoter activation, identify a transcription factor, establish all earlier time points, or independently quantify RNA degradation. The post-extraction spike only monitors downstream recovery; uptake and incorporation require separate controls. [S2; original calculation]

## Q3 - A chase must actually stop the input

The treated chase retains 30% of its original R synthesis. R abundance therefore follows production minus loss, not decay alone. Remaining production makes disappearance slower than it would be with full blockade; fitting a simple exponential can produce a misleading apparent half-life. The 2-versus-6-hour values are not reliable estimates of native degradation.

Even complete synthesis inhibition would not establish an unperturbed degradation system: a global inhibitor can deplete short-lived components of degradation machinery. S4 demonstrates this problem in a yeast pathway; it is a caution here, not proof of the same human mechanism.

Panel D avoids cycloheximide and follows an existing labeled cohort with defined controls. It is more appropriate for inference, but still requires growth correction and its own labeling assumptions. [S4, S5]

# Reference answers: questions 4-5

## Q4 - Protein loss per cell includes growth dilution

Panel D control reaches 0.5 at 4 hours, so its loss half-life is 4 hours. Treatment reaches 0.25 at 12 hours: two half-lives, giving a 6-hour loss half-life.

| Quantity | Control | Compound X |
| --- | ---: | ---: |
| Observed per-cell loss half-life, hours | 4 | 6 |
| k_loss, per hour | 0.173287 | 0.115525 |
| k_growth, per hour | 0.057762 | 0.028881 |
| k_degradation = k_loss - k_growth, per hour | 0.115525 | 0.086643 |
| Degradation-only half-life, hours | 6 | 8 |

Actual degradation becomes slower by a rate ratio of 0.086643 / 0.115525 = 0.75, or a half-life ratio of 8 / 6 = 1.333. Total per-cell clearance falls to two-thirds of control because degradation and growth dilution both fall. A cell population growing more slowly dilutes the labeled protein among new cells more slowly. [S5, S6; original calculation]

## Q5 - Both synthesis and clearance contribute

At steady state, S = P x k_loss. The synthesis-rate ratio is 3 x (0.115525 / 0.173287) = 2.

Mature mRNA per cell is twofold higher. Effective synthesis per mRNA therefore changes by S_ratio / M_ratio = 2 / 2 = 1.

The abundance ratio can be reconstructed as:

P_ratio = S_ratio x (k_loss_control / k_loss_treated) = 2 x 1.5 = 3.

The model requires twice the synthesis flux and lower clearance, rather than degradation alone. Unchanged effective synthesis per mRNA is a net inferred result, not a direct measurement proving that every translation-regulatory step is unchanged. Compensating processes or unmodeled effects remain possible. No percentage allocation of the overall abundance change is uniquely implied by this multiplicative calculation. [S5, S6; original calculation]

# Reference answers: questions 6-8

## Q6 - Which claims survive?

**A: Reject as a sole explanation.** If synthesis stayed fixed, the measured clearance change would predict 1.5-fold abundance, not threefold. Also, slower cell growth contributes to clearance.

**B: Reject.** The inferred effective synthesis-per-mRNA ratio is 1, not 3, under the supplied model. This does not establish that every translation-control process is unchanged.

**C: Support conditionally.** Twice the synthesis combined with a clearance factor of 1.5 reconstructs threefold abundance. The result depends on steady state, calibration and the turnover model.

**D: Unsupported.** There is no direct binding, enzyme activity, ubiquitination, localization or pathway-specific evidence. Reduced degradation does not identify its mechanism. [S1-S6; case-specific synthesis]

## Q7 - Experiments that separate explanations

**Synthesis per mRNA:** use an independent, R-specific short metabolic protein-labeling time course without cycloheximide, quantify newly made R, and measure calibrated R mRNA per viable cell in parallel. Control labeling precursor enrichment, recovery, cell input, viability and assay specificity; include multiple early times and account for degradation of labeled product. A twofold synthesis increase alongside twofold mRNA supports the inferred ratio of 1; a reproducible discrepancy challenges the model. A single pulse intensity is confounded by labeling kinetics and degradation. [S5]

**Endogenous regulatory-element dependence:** perturb a candidate cis-regulatory element at the R locus, using precise sequence editing or carefully controlled CRISPR interference, and quantify calibrated newly made R RNA in vehicle and X conditions. Include non-targeting and nearby control perturbations, multiple independently validated edits or guides, viable-cell input, a check that basal expression remains measurable, and restoration of the element where feasible. A selective reduction in the X response supports element dependence. A general loss of basal expression alone does not isolate the X response. Off-target changes, chromatin spreading or redundant elements can complicate interpretation. Dependence does not establish direct binding by X: upstream regulation can still require the same element. A matched reporter is acceptable as supporting evidence, with copy/delivery and reporter-turnover controls, but cannot substitute entirely for the endogenous context. [S1, S2, S7; proposed design]

**Degradation pathway:** require a specific pathway perturbation with verified target engagement and an independent turnover readout, plus rescue or an orthogonal perturbation where feasible. Inhibitor-induced accumulation alone is insufficient to identify the route. [S4, S5; proposed design]

## Q8 - Corrected conclusion

After correcting the assay normalization and recovery, compound X is associated with twofold mature and newly made RNA signals and threefold protein R abundance per viable cell. Under the steady-state model, the evidence implies twice the protein synthesis flux and reduced clearance from both slower degradation and slower growth, with unchanged net synthesis per mRNA. Direct molecular targets, promoter mechanisms and statistical reliability remain unresolved because the case supplies simulated point values without biological replicates or uncertainty estimates.
