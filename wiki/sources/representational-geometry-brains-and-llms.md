---
title: "Representational Geometry In Brains And LLMs"
type: source
status: draft
created: 2026-06-04
updated: 2026-06-04
sources:
  - https://www.nature.com/articles/s41593-026-02315-y
  - https://arxiv.org/abs/2410.19750
---

# Representational Geometry In Brains And LLMs

This source note compares two distinct research programs that use geometry to study distributed representations:

- Pia-Kelsey O'Neill, Lorenzo Posani, and colleagues' 2026 *Nature Neuroscience* paper, "The representational geometry of emotional states in basolateral amygdala";
- Yuxiao Li, Eric J. Michaud, David D. Baek, Joshua Engels, Xiaoqing Sun, and Max Tegmark's 2024 arXiv paper, "The Geometry of Concepts: Sparse Autoencoder Feature Structure."

The bridge is computational. It is not a claim that mouse amygdalae are language models, that LLMs have emotions, or that similar analysis methods imply similar subjective experience.

## Nature Neuroscience: Emotional-State Geometry In Mouse Amygdala

O'Neill, Posani, and colleagues studied how basolateral amygdala (BLA) activity represents variables related to emotional states in mice.

The mice were presented with conditioned stimuli that elicited trembling and ingress into a burrow, interpreted in the study as fear-related and flight-to-safety behaviors. The researchers report that:

- BLA inactivation disrupted several differential responses to aversive versus neutral stimuli without eliminating trembling or burrow ingress themselves, supporting a role in valence representation rather than direct motor commands;
- individual BLA neurons rarely represented only one variable;
- single neurons instead showed mixed selectivity for stimulus identity, stimulus valence, trembling, and/or ingress;
- population activity sometimes formed a geometry that allowed specialized readouts of one variable;
- those readouts could generalize across conditions and avoid interference from other represented variables.

The important result is not a neat "fear neuron." Useful emotional-state variables can become cleanly readable at the population level even when individual neurons are messy and multifunctional.

Source:

- [Nature Neuroscience: The representational geometry of emotional states in basolateral amygdala](https://www.nature.com/articles/s41593-026-02315-y)

## Tegmark And MIT: Concept Geometry In LLM Features

Li et al. studied feature dictionaries produced by sparse autoencoders applied to large language models.

They describe structure at three scales:

- **atomic scale:** local "crystal" structures with parallelogram or trapezoid relationships, extending familiar analogy-vector examples;
- **intermediate or "brain" scale:** spatial modularity, including clusters or "lobes" such as math and code features;
- **large or "galaxy" scale:** an anisotropic feature cloud with a power-law eigenvalue spectrum.

The paper's useful claim is that concept-like features are not merely an unstructured bag of directions. Their relationships have measurable geometric organization.

Source:

- [arXiv: The Geometry of Concepts: Sparse Autoencoder Feature Structure](https://arxiv.org/abs/2410.19750)

## The Useful Bridge

Both papers push against the same naive picture:

> One meaningful thing should correspond to one cleanly specialized unit.

Instead, meaningful variables may be distributed across a population, and the relationships among activity patterns can matter more than any one unit in isolation.

In both cases, geometry can support useful readout:

- a downstream biological circuit may read valence or safety from mixed-selectivity neural activity;
- an interpretability method may identify concept relationships and modules in model feature space.

This suggests a durable research question for the wiki:

> When does the geometry of a distributed representation make a variable abstract, generalizable, separable, or usable by another part of the system?

## Important Differences

The resemblance should stay bounded.

- The amygdala paper studies neural population activity in living mice during conditioned behavior.
- The Tegmark paper studies sparse-autoencoder feature vectors extracted from LLM activations.
- BLA geometry is dynamic and tied to biological circuits, behavior, bodily state, learning, and evolution.
- LLM feature geometry is shaped by model architecture, training data, optimization, and the sparse-autoencoder analysis method.
- Similar geometric vocabulary does not establish shared mechanisms, shared concepts, shared emotions, or shared consciousness.

## Do Not Overclaim

- Do not say the amygdala paper decoded subjective fear itself. It studied neural activity and behavior-related variables in mice.
- Do not say single neurons are unimportant. The result is that single-neuron selectivity is insufficient for the population computation being studied.
- Do not say LLMs think in literal crystals, lobes, or galaxies. Those are geometric descriptions and metaphors for feature-space structure.
- Do not treat sparse-autoencoder features as guaranteed natural concepts rather than analysis-dependent model features.
- Do not say similar representational geometry proves biological and artificial systems understand or feel in the same way.
- Decodability is not consciousness.

## Related Pages

- [Representational Geometry](../concepts/representational-geometry.md)
- [Neuroscience](../../themes/neuroscience/overview.md)
- [Interpretability And Whether Internal States Matter](../../themes/ai-consciousness/interpretability.md)
- [Wadia Shared Code For Perception And Imagination](wadia-shared-code-perception-imagination.md)

