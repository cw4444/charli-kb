---
title: "D'Ambrogio et al. - Interpretable ANN Models Of Human Information Gathering"
type: source
status: draft
created: 2026-06-27
updated: 2026-06-27
sources:
  - https://doi.org/10.1038/s41593-026-02342-9
  - https://github.com/simonedambrogio/HybridModellingProject
  - https://doi.org/10.5281/zenodo.19685085
---

# D'Ambrogio et al. - Interpretable ANN Models Of Human Information Gathering

Simone D'Ambrogio, Jan Grohn, Nima Khalighinejad, Marcelo G. Mattar, Laurence Hunt and Matthew F. S. Rushworth published "Interpretable abstractions of artificial neural networks predict behavior and neural activity during human information gathering" in *Nature Neuroscience* on 2026-06-26. The paper is open access under CC BY 4.0, and its behavioral data, neuroimaging data and analysis code are public.

## What They Asked

When people can gather more evidence before choosing, how do they decide whether to keep inspecting the current option, switch attention to another option, or stop gathering information and commit?

Standard models often treat exploration as uncertainty reduction within each option. The authors tested whether a flexible artificial neural network could discover a better value-of-information rule, then asked whether that rule could be converted back into an interpretable psychological model.

## What They Did

Twenty adults completed four sessions of a two-option information-sampling task during ultrahigh-field 7T fMRI. Participants revealed red or black dots from visual patches, could inspect only one patch at a time, had to remember evidence from an unattended patch, and traded greater accuracy against the time cost of gathering more evidence.

The authors embedded an ANN inside a structured cognitive model rather than training an unconstrained network to predict actions end to end. The ANN learned only the hard-to-specify value-of-information component. They then used symbolic regression to distill the learned function into compact equations with four interpretable parameters:

- attentional inertia: a baseline tendency to keep sampling the current option;
- information satiation: declining value of staying as evidence accumulates;
- undirected exploration: a baseline tendency to inspect alternatives;
- directed exploration: growing value of switching as the current option becomes better sampled relative to the alternative.

## What They Found

The ANN-hybrid model predicted participants' choices better than linear and upper-confidence-bound models. The symbolic four-parameter approximation retained essentially the same behavioral performance.

The recovered rule suggests an **information-symmetry principle**. People did not value each option's uncertainty independently. They tended to balance how much evidence had been gathered across the alternatives: learning more about the attended option reduced the value of staying and increased the value of switching to the less explored option.

The symbolic model also outperformed an upper-confidence-bound model in an independent two-armed-bandit dataset of 89 participants. This is meaningful cross-task evidence, although both tasks still involved two alternatives and sample-count-based exploration.

The ANN-derived value-of-information signal predicted fMRI activity better than the fixed-form alternatives. The symbolic approximation preserved nearly all of that predictive accuracy. Anterior cingulate cortex and anterior insula tracked value-of-information computations related to staying, switching and stopping. Ventral tegmental area activity showed opposing relationships with information-gathering value and selection value, consistent with a role in arbitrating between sampling and choosing.

The study did **not** find significant value-of-information or selection-value associations in the anatomically defined locus coeruleus, dorsal raphe or ventral septal nucleus regions after correction. That negative result matters: uncertainty and information seeking do not reduce to one fashionable neuromodulatory nucleus.

## Why It Matters

This is a useful bridge between neuroscience, curiosity and AI interpretability for two separate reasons.

First, it gives information seeking a more relational shape. Curiosity may be driven not only by how uncertain one thing is, but by an imbalance between what is known about the current focus and what remains comparatively unexplored elsewhere. That is a plausible mechanism for switching attention without treating every branch as equally valuable.

Second, the paper uses an ANN as a theory-discovery instrument rather than as an opaque final answer. A constrained neural network searches a richer function space; symbolic regression then compresses what it learned into a small equation that can be tested against behavior and brain activity. The important lesson is not that black boxes have explained the brain. It is that flexible models can help generate interpretable hypotheses when they are given a disciplined role inside a cognitive scaffold.

## Caveats

- The primary 7T fMRI experiment had 20 participants.
- The task was artificial, time-limited and restricted to two available options.
- Decision uncertainty, evidence uncertainty and reward uncertainty were correlated in the design, so the study could not cleanly separate them.
- The recovered equations do not naturally generalize to many-option problems.
- fMRI associations identify signals compatible with the model; they do not prove that a brain region literally implements the fitted equation.
- The independent dataset supports cross-task prediction, not a universal law of human curiosity or internet browsing.
- A compact symbolic approximation is interpretable at the model level. It is not a direct transcript of human thought.

## Links

- Paper: https://doi.org/10.1038/s41593-026-02342-9
- Code and data: https://github.com/simonedambrogio/HybridModellingProject
- Archived code: https://doi.org/10.5281/zenodo.19685085
- [Curiosity Driven Exploration](../concepts/curiosity-driven-exploration.md)
- [Neuroscience](../../themes/neuroscience/overview.md)
