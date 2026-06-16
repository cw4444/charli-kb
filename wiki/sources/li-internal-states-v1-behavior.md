---
title: "Li et al. - Internal States And V1 Behavior Covariation"
type: source
status: draft
created: 2026-06-16
updated: 2026-06-16
sources:
  - https://doi.org/10.1038/s41593-026-02296-y
  - ./v1-feedback-task-context-source-batch.md
---

# Li et al. - Internal States And V1 Behavior Covariation

Baowang Li, Jason M. Samonds, Yuzhi Chen, Thibaud Taillefumier, Nicholas J. Priebe and Eyal Seidemann published "Fluctuating internal states mediate neural-behavioral covariations in V1" in *Nature Neuroscience* on 2026-05-13.

The article page is subscription preview rather than open access, so this note uses the public abstract, figure captions, references, data/code availability statements and metadata. The experimental data and figure code are publicly listed on figshare.

## What They Did

The authors measured membrane potential (V_m) from single neurons in macaque primary visual cortex (V1) while monkeys performed a reaction-time visual detection task.

The key question is how internal state and external visual input interact at the level of early visual cortex. V1 is often treated as early sensory machinery, but the paper asks whether trial-to-trial fluctuations in internal state are already shaping the relationship between single-neuron voltage and behavior.

## What They Found

From the public abstract:

- most V1 neurons gradually depolarized before target onset;
- variation in that pre-target buildup correlated with the monkeys' reaction times;
- after target onset, membrane-potential fluctuations correlated with choice;
- those neural-behavioral covariations depended strongly on target location and contrast;
- a simple computational model with fluctuating multiplicative gain could account for the results.

The authors' interpretation is that covariations between single-neuron V1 membrane potential and behavior are implemented by internal-state-related nonlinear modulations operating at, or before, V1.

## Why It Matters

This is a direct early-visual-cortex version of the wiki's active-perception lane. The result suggests that even V1 is not merely passing visual input upstream like a camera cable. Internal state can modulate sensory processing before or at V1, and those modulations can track reaction time and choice.

The open-access [V1 Feedback And Task Context Source Batch](v1-feedback-task-context-source-batch.md) supplies adjacent evidence from *Nature Communications*: V4-to-V1 feedback in macaque figure-ground parsing, task-targeted V1 comodulation in macaque sensory decisions, and multiplexed task-context representation in mouse V1. Together they make the same point less dependent on one closed article.

The useful bridge to [Reality Threshold](../concepts/reality-threshold.md) is cautious: perception is not just an external signal crossing a passive detector. The detector's gain and state can already be changing before the target arrives.

The useful bridge to [Locus Coeruleus](../concepts/locus-coeruleus.md) is also cautious. The paper's model is about fluctuating multiplicative gain, and the article references adaptive gain and state-dependent detection work. That does not prove LC causality in this experiment. It does reinforce the broader point that internal state can alter how sensory evidence lands.

## Caveats

- The article itself is not open access in this pass; do not summarize beyond public abstract/metadata unless a legitimate full text is available.
- This is macaque V1 during a reaction-time visual detection task, not a general theory of all perception.
- Single-neuron membrane potential covariation with behavior is not the same as the neuron "deciding" perception.
- Multiplicative gain is a model account, not proof of one named neuromodulatory mechanism.
- The result supports state-dependent perception, not manifestation, wishful seeing or "reality is whatever you feel."

## Access

- DOI: https://doi.org/10.1038/s41593-026-02296-y
- Nature article page: https://www.nature.com/articles/s41593-026-02296-y
- Data and code project: https://figshare.com/projects/Fluctuating_internal_states_mediate_neural-behavioral_covariations_in_V1/216568
