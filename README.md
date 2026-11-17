# Alpha-TCM: Auditable Knowledge Integration for Multimodal TCM Inference

**Yucheng Liu and Everett X. Wang · Preprint, 2026**

**[Read the current paper (PDF, including supplementary methods)](paper/alpha-tcm.pdf)** · [arXiv:2610.38754](https://arxiv.org/abs/2610.38754)

Knowledge-guided multimodal systems need a way to measure how supplied knowledge changes predictions, including when that knowledge is wrong. Alpha-TCM addresses this problem for traditional Chinese medicine (TCM) through an implemented workflow that separates measurements, supplied knowledge, predictions, and reviewer decisions.

## Contribution

Observations and contextual knowledge enter separately. A replaceable probabilistic prior supports controlled knowledge interventions while holding the modality encoders fixed. Bayesian committee accounting removes the reference prior already contained in each encoder before inserting contextual knowledge. This makes knowledge dependence inspectable and allows comparisons against learned context with the same information.

## Main findings

A fully simulated confirmation study uses ten paired seeds and four training sizes.

- Knowledge context reduces prediction error relative to knowledge-free fusion at 600 and 1,200 training cases.
- Equal-information learned context is competitive at 600 training cases and has lower error at larger sizes. The results distinguish gains from additional context from gains attributable to a particular prior representation.
- Overconfident and displaced priors are the most damaging tested knowledge corruptions.
- Case-level conflict detection remains weak, and training-time prior regularisation shows no consistent benefit.
- Functional tests verify the connected workflow separately from predictive performance.

The study demonstrates an approach to auditing knowledge dependence before clinical evaluation. All predictive experiments are simulated; they do not establish clinical diagnostic or treatment validity.

## Repository contents

- `paper/alpha-tcm.pdf`: the current 11-page named-author preprint, including supplementary methods.
- `README.md`: paper overview, main findings, and citation information.

This is a paper repository. Research code, datasets, and experiment outputs are not included in this release. The PDF is unchanged from the current full manuscript, including its LLM disclosure statement.

## Citation

The existing, versionless arXiv URL is retained and will resolve to the latest announced replacement. The PDF above provides the current manuscript directly.

```bibtex
@misc{liu2026alphatcm,
  title         = {Alpha-TCM: Auditable Knowledge Integration for Multimodal TCM Inference},
  author        = {Liu, Yucheng and Wang, Everett X.},
  year          = {2026},
  eprint        = {2610.38754},
  archivePrefix = {arXiv},
  primaryClass  = {cs.LG},
  url           = {https://arxiv.org/abs/2610.38754}
}
```

## Rights

This repository does not grant a new reuse license. The manuscript's existing rights and arXiv license remain applicable.
