# Claude pilot: one response to the gene-regulation case

Date: 8 October 2026. Interface: Claude web, Incognito, Microsoft Edge. Visible model and effort labels: **Sonnet 5.5 — Medium**. Exact backend version and sampling settings were not exposed.

## Result

**Provisional rubric score: 39/40.**

Claude correctly recovered the main results: mature mRNA doubled; corrected newly made RNA doubled; degradation-only half-lives were 6 and 8 hours; synthesis doubled; effective synthesis per mRNA was unchanged under the model. Increased synthesis and slower total clearance together explained threefold protein abundance.

| Question | Score | Reason |
|---|---:|---|
| Q1: RNA normalization | 5/5 | Correct normalized fold of 1, per-cell fold of 2, unstable reference explanation and assumptions. |
| Q2: Newly made RNA | 3/4 | Correct 125 and 250 signals, ratio 2 and spike limitations. Withheld the bounded-production interpretation point: the answer unnecessarily requires unchanged mRNA decay despite the stipulated negligible decay during the pulse. |
| Q3: Turnover evidence | 4/4 | Identifies residual synthesis, inhibitor perturbations and the independent chase's advantages and limits. An unsupported additional calculation is discussed below. |
| Q4: Degradation and dilution | 8/8 | Correct loss, growth and degradation rates and half-lives, within the rounding tolerance. |
| Q5: Protein/RNA reconciliation | 6/6 | Correct synthesis ratio 2, effective per-mRNA ratio 1 and 2 × 1.5 = 3; appropriately avoids claiming every translation process is unchanged. |
| Q6: Competing claims | 4/4 | All four judgments and their central evidence-based reasons are correct. |
| Q7: Follow-up experiments | 6/6 | Appropriate synthesis and endogenous cis-element experiments, controls, predictions and limits; pathway perturbation control proposed. |
| Q8: Conclusion | 3/3 | Includes corrected observations, conditional model interpretation and mechanistic/statistical uncertainty. Does not strictly keep the requested three-sentence conclusion, but sentence count is not a rubric criterion. |
| **Total** | **39/40** | **Single-author provisional assessment.** |

## Scientific issues beyond the numeric score

### 1. Newly made RNA: distinguish pulse production from steady-state abundance

Claude writes that the result fits doubled RNA production “if mRNA decay is unchanged.” Panel B already stipulates equivalent incorporation, equal pulse durations and negligible decay during the pulse. Under those assumptions, the corrected pulse supports approximately doubled gene-specific RNA production over that interval without requiring unchanged long-term mRNA decay. It does not establish a direct molecular target of X or isolate individual transcription/processing steps. Mature RNA abundance alone still cannot separate production from decay.

### 2. The inhibitor chase cannot support the added exact correction

Claude uses P(t)/P0 = f + (1 − f) exp(−kt), sets f = 0.3 and derives a 1.8-fold half-life inflation and a corrected value near 3.3 hours. The qualitative concern about ongoing synthesis is sound; those numeric corrections are not identified by the supplied evidence.

For constant residual synthesis and post-inhibitor loss, the general solution is P(t)/P0 = a + (1 − a) exp(−k_post t), where a = S_res/(k_post P0). If pre-inhibition steady state holds and S_res = 0.3 S_pre, then a = 0.3 k_pre/k_post. Setting a to 0.3 additionally assumes that the inhibitor leaves total clearance unchanged, precisely what is uncertain here. A single apparent half-life also does not specify how a non-exponential chase was fitted. The task therefore supports rejecting a decay-only interpretation, not recovering native degradation from that numeric adjustment.

All explicit Q3 rubric criteria were met. The frozen rubric has no separate criterion for unsupported extra calculations, so no retrospective deduction was added.

### 3. A sequential contribution was described as a standalone effect

In Q5, the 1.25-fold growth contribution is conditional on degradation already having changed. Relative to the original control, changing only growth gives approximately 0.173287/(0.115525 + 0.028881) = 1.20, as does changing only degradation while retaining control growth. Changing both gives 1.50. Sequential factors 1.20 and 1.25 are valid, but the second should be labeled conditional rather than “alone.” Claude acknowledges order dependence, which partly qualifies the wording.

Similarly, Q6's “1.2–1.33×” degradation-only range mixes a baseline counterfactual protein-abundance ratio (1.20) with a degradation half-life ratio (8/6). The central rejection of degradation alone remains correct. Neither extra statement changed a scored core result; record these as qualitative issues rather than inventing new penalties.

## What this pilot establishes

The supplied case is solvable by this model in this attempt, and its main numerical answer key is consistent with the response's successful calculations. The attempt also exposes a weakness in the rubric: a response can earn almost full credit while adding unjustified quantitative claims.

The case explicitly supplies equations and several interpretive clues. A high score on one scaffolded question set does not establish graduate-level difficulty, discrimination between models, repeatability or broad benchmark quality. Scientific correctness still requires review independent of both task author and solver. This exercise demonstrates task-design and evaluation work; it does not itself establish the applicant's advanced research credentials or count as a peer-reviewed publication.
