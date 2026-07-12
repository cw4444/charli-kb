---
title: "Brody et al. - The Adaptive Nature Of Confirmation Bias"
type: source
status: draft
created: 2026-07-12
updated: 2026-07-12
sources:
  - "Dorje C. Brody, Karl J. Friston, Bernhard K. Meister, and Emmanuel M. Pothos, The adaptive nature of confirmation bias, arXiv:2606.23325v1, 2026-06-22"
---

# Brody et al. - The Adaptive Nature Of Confirmation Bias

## Source Metadata

- Source: Dorje C. Brody, Karl J. Friston, Bernhard K. Meister, and Emmanuel M. Pothos, [The adaptive nature of confirmation bias](https://arxiv.org/abs/2606.23325), arXiv:2606.23325v1, 2026-06-22.
- Access note: public arXiv preprint, CC BY 4.0.
- Status: theoretical/modeling paper, not a new behavioural experiment or a general empirical vindication of confirmation bias.

## Summary

Brody, Friston, Meister, and Pothos ask whether an *active* form of confirmation bias can sometimes be rational: when an agent can choose among evidence sources, does choosing one closer to an existing prior ever reduce error rather than merely protect a preferred belief?

In their binary hypothesis-testing model, the answer is yes under specific assumptions. Evidence sources are represented as potentially incompatible matrix-valued observations in a Hilbert-space / quantum-probability formalism. When the agent selects evidence to minimise expected hypothesis-selection error, the optimal source becomes more aligned with the stronger prior. The authors obtain the same evidence-selection rule through a maximum-information active-inference formulation.

In their sequential model, the selected current observation can carry the relevant accumulated state, reducing the memory needed for inference and yielding exponential error reduction with sample size. This is a formal result about an adaptive sampling rule, not a finding that ordinary human confirmation bias is broadly truth-tracking.

## Why It Matters

The paper sharpens an important distinction across the wiki's judgment-bias lane:

- **Focusing illusion**: what is currently attended can feel disproportionately important.
- **Availability and frequency illusion**: salient or repeated examples become easier to retrieve and can feel more common or significant.
- **Active confirmation bias**: an agent may also choose the next source of information in a prior-sensitive way.

Together, these make a self-reinforcing loop possible: attention narrows the question; available examples make one hypothesis feel familiar; chosen sources supply further congenial evidence; repeated noticing then feels like a property of the world. The loop may conserve effort or simplify sequential inference in a well-structured environment. In an adversarial media environment, it can manufacture confidence while hiding the evidence needed to correct a bad prior.

## The Friston Connection

The paper connects its result to active inference by treating evidence choice as expected-free-energy minimisation, with information gain and outcome-cost terms. In its unconstrained toy setup, the information-maximising and error-minimising choices agree.

The authors explicitly note an important limit: when only finitely many real evidence sources are available, the error-minimising choice and the information-maximising choice can differ. That is precisely where real life becomes unpleasantly less elegant than the model.

## Do Not Overclaim

- This is a preprint and a formal derivation, not a demonstration that everyday confirmation bias is adaptive.
- The result depends on binary hypotheses, selectable evidence, modelled source incompatibility, and the paper's objective function.
- It does not show that biased newspapers, algorithmic feeds, conspiracy content, or selectively chosen social-media sources are epistemically good.
- Memory efficiency is not equivalent to truth, welfare, fairness, or robust learning under distribution shift.
- "Quantum" here refers to a mathematical probability formalism; the authors do not claim that brains require physical quantum-computing resources.

## Related Pages

- [Frequency Illusion](../concepts/frequency-illusion.md)
- [Focusing Illusion](../concepts/focusing-illusion.md)
- [Kahneman And Tversky - Judgment Under Uncertainty](kahneman-tversky-judgment-under-uncertainty.md)
- [Salience Weighted Judgment](../concepts/salience-weighted-judgment.md)
