---
title: "Representational Geometry"
type: concept
status: draft
created: 2026-06-04
updated: 2026-06-10
sources:
  - ../sources/representational-geometry-brains-and-llms.md
---

# Representational Geometry

Representational geometry studies how information is organized across patterns of activity in a high-dimensional space. A useful nearby phrase is **representation as relational geometry**: meaning often lives in structured relations across many units, not in one privileged unit with a tidy label taped to it.

The basic move is to stop asking only:

> Which single neuron, unit, or feature represents this thing?

and also ask:

> How are many activity patterns arranged relative to one another, and what can another part of the system read from that arrangement?

## Why Geometry Matters

A distributed system can represent several variables at once. Individual units may respond to mixtures of those variables, while the population as a whole still makes a particular variable:

- decodable;
- separable from other variables;
- generalizable across conditions;
- usable by a downstream readout;
- resistant to interference.

The geometry can therefore be computationally meaningful even when no single unit has a tidy label.

## Representation As Relational Geometry

At this level, asking what one neuron or one feature "really means" can be the wrong first question. The more durable object is the geometry of the representation space:

- which states align;
- which directions stay parallel;
- which variables interfere;
- which transformations generalize across contexts.

This does not mean single-unit interpretation is useless. It means unit-level stories can be inadequate even when population-level readout is crisp.

## Brain Example

In the 2026 basolateral-amygdala study summarized in [Representational Geometry In Brains And LLMs](../sources/representational-geometry-brains-and-llms.md), individual neurons showed mixed selectivity for variables including stimulus identity, valence, trembling, and burrow ingress.

Population activity could nevertheless form geometries that supported specialized readouts of particular variables across conditions without interference from the others.

## AI Example

In Tegmark and colleagues' "The Geometry of Concepts," sparse-autoencoder features extracted from LLMs showed local analogy-like structures, intermediate-scale modularity, and large-scale anisotropic organization.

The useful interpretation is not that concepts are literal objects floating inside a model. It is that relationships among model features can have measurable structure that may help explain how concepts are organized and used.

## Parallel Coding Directions

A variable can generalize across new inputs when the transformation corresponding to that variable keeps a stable geometric direction across contexts.

In sparse-autoencoder geometry, this appears as analogy-like structure among feature vectors. In the basolateral-amygdala paper, the same organizing principle appears in a different measurement space: population activity can support cross-condition generalization when the coding direction for a variable is preserved across conditions.

That is the clean bridge from the raw Fusi/SAE note: abstraction survives novelty when representational geometry preserves a stable directional relation.

## What Is Not Unified Yet

SAE decoder geometry and biological neural activity geometry are not the same object. One studies learned feature-dictionary vectors in an interpretability tool; the other studies activity states in living neural populations during behavior.

The current honest claim is that they share an organizing principle. A stronger claim would need a formal mapping between feature dictionaries, biological population codes, model activation trajectories, and generalization metrics.

## Why It Matters For This Wiki

Representational geometry is a clean bridge between neuroscience and AI interpretability.

It sharpens several existing threads:

- [Perception And Imagination Overlap](perception-and-imagination-overlap.md): shared code can be understood as overlapping population structure, not necessarily one-to-one neuron reuse alone.
- [Reality Threshold](reality-threshold.md): felt realness may depend on distributed signals and readout rules rather than one "real" switch.
- [Optimism](optimism.md): future representations may differ in geometry, separation, vividness, and accessibility.
- [AI consciousness interpretability](../../themes/ai-consciousness/interpretability.md): internal structure matters, but structure and decodability do not establish subjective experience.

## Do Not Overclaim

- A decodable variable is not necessarily explicitly represented for the system's own use.
- A linear or specialized readout is not a little inner observer.
- Similar geometry across systems does not prove similar mechanisms or experiences.
- Sparse-autoencoder features are useful interpretability objects, not guaranteed natural atoms of thought.
- Mixed selectivity does not mean individual units are irrelevant.
- Decodability is not consciousness.

## Related Pages

- [Representational Geometry In Brains And LLMs](../sources/representational-geometry-brains-and-llms.md)
- [Can SAE Decoder Geometry And Neural Activity Geometry Be Unified?](../questions/can-sae-decoder-geometry-and-neural-activity-geometry-be-unified.md)
- [Stefano Fusi](../people/stefano-fusi.md)
- [Neuroscience](../../themes/neuroscience/overview.md)
- [Interpretability And Whether Internal States Matter](../../themes/ai-consciousness/interpretability.md)
- [Perception And Imagination Overlap](perception-and-imagination-overlap.md)
- [Reality Threshold](reality-threshold.md)
