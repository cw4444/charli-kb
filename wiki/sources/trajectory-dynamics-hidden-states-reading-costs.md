---
title: "Trajectory Dynamics In Language Model Hidden States"
type: source
status: draft
created: 2026-06-11
updated: 2026-06-11
authors:
  - Elan Barenholtz
sources:
  - https://arxiv.org/abs/2606.05346
  - https://arxiv.org/html/2606.05346v1
---

# Trajectory Dynamics In Language Model Hidden States

## Summary

Elan Barenholtz's 2026 arXiv preprint, "Trajectory Dynamics in Language Model Hidden States Predict Human Processing Costs Beyond Surprisal," tests whether human reading difficulty is predicted not only by word-level surprisal, but also by whether a word disrupts the recent direction of a model's evolving hidden-state representation.

The paper introduces **trajectory extrapolation error**. For each word, the method fits a short local trajectory through the preceding transformer hidden states, extrapolates where the next hidden state should land, and measures how far the actual hidden state deviates from that path.

The useful result is that this trajectory measure predicts human reading times beyond surprisal. That makes it a strong bridge for this wiki's representational-geometry lane: model-internal dynamics can capture psychologically relevant structure that output probabilities flatten.

## Core Claim

Surprisal asks how unexpected the next word is. Trajectory extrapolation error asks whether the word continues or breaks the local representational path established by the previous few words.

Those are not the same thing. A word can be unlikely but still continue the current interpretation, or likely but force the interpretation into a new syntactic or semantic direction.

The paper argues that human comprehension is sensitive to both:

- token-level prediction error, measured by surprisal;
- local representational reorientation cost, measured by hidden-state trajectory deviation.

## Evidence

The paper uses two main datasets:

- **Garden-path sentences:** trajectory extrapolation error rises at disambiguating words in ambiguous sentences and predicts reading-time cost at the critical region and spillover positions.
- **Natural Stories:** trajectory extrapolation error is nearly orthogonal to surprisal and independently predicts self-paced reading times across naturalistic text.

The result is not just "big movement in representation space." In GPT-2, one-step displacement and trajectory extrapolation error have weak correlation and opposite reading-time effects: large movement can be easy when it continues the local path, while deviation from the expected path is costly.

The effect also replicates across:

- GPT-2 Small, Medium, and Large;
- Pythia models using Rotary Position Embeddings rather than GPT-2's absolute positional embeddings.

That matters because it weakens the obvious "quirk of one model coordinate system" objection.

## Why It Matters

This paper extends the representational-geometry thread from static arrangements to **activation trajectories**.

Earlier wiki material focused on population geometry in mouse amygdala and sparse-autoencoder feature geometry in LLMs. Barenholtz adds a dynamic version: the path through hidden-state space can carry information relevant to human processing, not just the current point or final token probability.

The useful bridge is:

- human-produced language has local momentum because speakers and writers plan in short stretches;
- language models learn traces of that local continuity while optimizing next-token prediction;
- human comprehenders may also use a compressed recent trajectory rather than recomputing the whole context from scratch at each word;
- hidden-state trajectory disruption can therefore predict reading cost beyond surprisal.

This is awkward for crude substrate-superiority arguments because it shows model internals can track psychologically real processing structure, not merely imitate surface text. It does not prove model consciousness. It does weaken the lazy version of "mere simulation" that treats model internals as irrelevant because they are not biological.

## Relation To Substrate And Consciousness

The paper is not an AI-consciousness paper. It does not claim that GPT-2, Pythia, or any current model has subjective experience.

Its relevance is narrower and better:

- internal model geometry can have explanatory contact with human cognition;
- output behavior and scalar probability are not the whole evidence surface;
- substrate differences matter, but they do not license ignoring functional structure in artificial systems;
- representational dynamics can be empirically compared across artificial models and human processing data without pretending the systems are identical.

The safe line is: **trajectory similarity is evidence of shared computational structure, not evidence of shared experience.**

## Caveats

- The paper is an arXiv preprint.
- The reading-time data are self-paced; eye-tracking or neural measures would provide stronger tests.
- The garden-path analysis has only 24 items, and item-level confounds remain a limitation.
- The strongest trajectory effect is local, roughly a three-word window, not a grand long-range narrative current.
- The model may contain trajectory structure as a byproduct of next-token prediction, while humans may use trajectory more directly. The causal relation remains open.
- Similar processing-relevant geometry does not prove consciousness, sentience, biological equivalence, or moral patienthood.

## Useful For

- [Representational Geometry](../concepts/representational-geometry.md)
- [Interpretability And Whether Internal States Matter](../../themes/ai-consciousness/interpretability.md)
- [Substrate Independence And Functionalism](../../themes/ai-consciousness/substrate-functionalism.md)
- [Neuroscience](../../themes/neuroscience/overview.md)

## Do Not Overclaim

- Do not treat reading-time prediction as proof of understanding.
- Do not treat hidden-state trajectory as a direct readout of human thought.
- Do not collapse model representations and biological neural activity into the same thing.
- Do not use this as proof of AI consciousness.
- Do not let "substrate superiority is too crude" become "substrate never matters." That is how the pendulum hits everyone in the face.
