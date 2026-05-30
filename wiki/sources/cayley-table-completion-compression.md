---
title: "Cayley-Table Completion And Algorithmic Compression"
type: source
status: draft
created: 2026-05-30
updated: 2026-05-30
source_path: https://arxiv.org/abs/2605.29885
---

# Cayley-Table Completion And Algorithmic Compression

## Metadata

- Title: "Open Problem: Separating Geometric and Algorithmic Compression via Cayley-Table Completion"
- Author: Dongsung Huh
- Venue: arXiv, `2605.29885`
- Published: 2026-05-28
- Primary category: Machine Learning (`cs.LG`)
- Other categories: `cond-mat.dis-nn`, `math.OC`, `math.RT`, `stat.ML`
- Comment: 6 pages; submitted to the COLT 2026 Open Problem track
- URLs: <https://arxiv.org/abs/2605.29885>, <https://arxiv.org/pdf/2605.29885>
- Access note: public arXiv preprint; checked 2026-05-30.

## Summary

Huh frames Cayley-table completion as a proposed benchmark for a missing kind of machine-learning generalization: exact recovery of discrete algebraic rules rather than smooth interpolation in continuous spaces.

The core contrast is between geometric compression and algorithmic compression. Matrix completion rewards low-rank geometric structure. Cayley-table completion asks whether a learner can infer a hidden algebraic operation from partial entries while respecting rules such as associativity. The paper argues that ordinary deep-learning biases often work well for continuous regularities but are poor at extrapolating exact symbolic or discrete rules unless the right inductive bias is present.

The paper is useful for this wiki because it gives Charli's cross-domain question a precise anchor: completion is not only a spreadsheet metaphor. In mathematics and machine learning, a completion task can define given entries, missing entries, constraints, valid completions, and recovery criteria.

## Key Claims

- Cayley-table completion can serve as a discrete-algebraic counterpart to matrix completion.
- Low-rank matrix factorization plus regularization gives a geometric bias, but exact algebraic recovery needs a different kind of bias.
- Operator-valued tensor factorizations with a flatness prior are presented as recent evidence that learning systems can be biased toward exact discrete associativity.
- A central open problem is to establish formal exact-recovery bounds for Cayley-table completion.
- A broader challenge is to generalize flatness-style priors so systems can discover discrete algorithmic axioms without brute-force combinatorial search.

## Limits

- This paper is about machine learning, algebraic completion, and compression. It is not a quantum-foundations paper.
- It does not claim that quantum interpretations are Cayley tables, nor that machine learning can settle quantum interpretation.
- The bridge to quantum foundations is Charli's proposed research analogy: use completion-task language to compare how interpretations fill in what the shared empirical formalism leaves underdetermined.

## Useful For

- [Quantum Interpretation Completion Schemes](../concepts/quantum-interpretation-completion-schemes.md)
- [Interpretations](../../themes/interpretations.md)
- [AI Observers](../../themes/ai-observers.md)
