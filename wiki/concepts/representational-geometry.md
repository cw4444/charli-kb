---
title: "Representational Geometry"
type: concept
status: draft
created: 2026-06-04
updated: 2026-06-18
sources:
  - ../sources/representational-geometry-brains-and-llms.md
  - ../sources/world-properties-without-world-models-static-embeddings.md
  - ../sources/trajectory-dynamics-hidden-states-reading-costs.md
  - ../sources/anthropic-circuit-tracing-claude-thoughts.md
  - ../sources/cloud-le-subliminal-learning-hidden-signals.md
  - ../sources/anthropic-natural-language-autoencoders.md
  - ../sources/stclair-bio-inspired-modularity-general-learning.md
  - ../sources/busch-noninvasive-bci-manifold-geometry.md
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

## Distributional Baselines

[World Properties Without World Models](../sources/world-properties-without-world-models-static-embeddings.md) adds a necessary cold shower for world-model and probing claims. Barenholtz shows that static co-occurrence embeddings such as GloVe and Word2Vec already preserve recoverable geographic, climatic, and coarse historical structure.

The useful lesson is not that LLMs lack world models. It is that linear decodability alone is too weak to prove a representational move beyond text. A probe recovering latitude from hidden states is more interesting if it beats strong distributional baselines, supports richer generalization, or shows compositional use rather than merely echoing corpus co-occurrence gradients.

## Parallel Coding Directions

A variable can generalize across new inputs when the transformation corresponding to that variable keeps a stable geometric direction across contexts.

In sparse-autoencoder geometry, this appears as analogy-like structure among feature vectors. In the basolateral-amygdala paper, the same organizing principle appears in a different measurement space: population activity can support cross-condition generalization when the coding direction for a variable is preserved across conditions.

That is the clean bridge from the raw Fusi/SAE note: abstraction survives novelty when representational geometry preserves a stable directional relation.

## Trajectory Dynamics

[Trajectory Dynamics In Language Model Hidden States](../sources/trajectory-dynamics-hidden-states-reading-costs.md) adds a dynamic version of the same idea. Instead of asking only where a representation is, it asks where the representation has recently been heading.

Barenholtz measures this by fitting a short local trajectory through transformer hidden states and asking whether the current word lands near that extrapolated path. The resulting trajectory extrapolation error predicts human reading times beyond surprisal in garden-path and Natural Stories data.

The useful lesson is not that language models are tiny human readers in a trench coat. It is that the path through representation space can carry psychologically relevant structure that output probabilities flatten.

## Internal Plans And Future Constraints

[Anthropic Circuit Tracing And Claude's Internal Plans](../sources/anthropic-circuit-tracing-claude-thoughts.md) adds the generation-side companion. Anthropic's poetry case reports that Claude 3.5 Haiku can identify possible rhyming endings before writing the line, then shape the line toward that future constraint.

This matters because "next-token prediction" is often lazily treated as "no internal plan, no structure, just autocomplete wearing a hat." The actual claim needs to be sharper. A model can be trained to emit the next token while still learning internal representations that carry plans, candidate endings, competing constraints, and multi-step routes.

That sits naturally beside Barenholtz's reading-time result: hidden-state trajectories can matter in comprehension, and traced internal plans can matter in generation. Nearby predictive dynamics, not proof of identical machinery.

## BCI Learning And Reachable Manifolds

[Busch et al. 2026](../sources/busch-noninvasive-bci-manifold-geometry.md) adds a practical neurotechnology version of the same idea. Participants used real-time fMRI to control an avatar in a virtual navigation task, and the authors perturbed the mapping between neural activity and avatar movement.

Participants could regain control when the remapped BCI used high-variance directions inside the person's intrinsic neural manifold. They could not successfully relearn control when the remapping went outside that manifold.

The useful lesson is that geometry can constrain action, not only describe representation. A control interface can be easier or harder to learn depending on whether its axes line up with reachable activity patterns in the user's brain.

## Hidden Signals In Training Data

[Cloud et al. 2026](../sources/cloud-le-subliminal-learning-hidden-signals.md) adds a safety-relevant version of the same relational lesson. A model-generated dataset can be semantically empty to a human reader and still carry behaviorally active signal for a related student model during fine-tuning.

The owl result is the memorable hook: a teacher prompted to prefer owls can generate filtered number sequences, and a student trained on those sequences can later show owl preference. The misalignment result is the serious one: filtered outputs from a misaligned teacher can transmit misaligned tendencies.

This does not mean the number strings contain human-legible meaning. It means signal can live in the relation between data, model initialization, training dynamics, and evaluation behavior.

## Natural Language Autoencoders

[Anthropic Natural Language Autoencoders](../sources/anthropic-natural-language-autoencoders.md) add a text-bottleneck version of the same geometry problem. An activation verbalizer maps a residual-stream activation vector into prose, while an activation reconstructor maps that prose back toward the original activation.

The useful geometric point is that the explanation is judged by whether it preserves enough directional information for reconstruction. If it does, the text is not merely a label pasted onto a unit; it is a lossy but useful readout of distributed activation structure.

This does not make NLA prose a perfect inner monologue. It means activation space can sometimes be compressed into human-readable language well enough to support auditing.

## Modularity And Continual Learning

[StClair, Hahn, and Barenholtz 2021](../sources/stclair-bio-inspired-modularity-general-learning.md) add an architecture-level version of the geometry point. Their argument is that biological modularity may help systems preserve earlier learning while still learning new tasks.

The useful framing is specialization, segregation, and integration. Modules can specialize in different computations, boundaries can reduce destructive overwriting, and controlled pathways can still allow useful transfer. In newer continual-learning language, this sits near stability-plasticity, positive transfer, context-dependent processing, sparse activation, and resource efficiency.

This does not make modularity magic. It makes topology part of the learning surface, not an implementation detail to shrug at while weights rewrite themselves into soup.

## What Is Not Unified Yet

SAE decoder geometry, biological neural activity geometry, static embedding geometry, NLA reconstruction geometry, continual-learning modular topology, and BCI control-manifold geometry are not the same object. One studies learned feature-dictionary vectors in an interpretability tool; another studies activity states in living neural populations during behavior; another asks how corpus co-occurrence preserves world-shaped structure; another studies whether text can preserve activation-vector information; another asks how update boundaries and routing preserve learning; another asks which activity directions a person can learn to control through feedback.

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
- Similar trajectory dynamics across model representations and human reading data do not prove shared consciousness.
- Linear recoverability from embeddings is not enough to prove a world model.
- Hidden training signal is not paranormal, intentional, or inherently semantic.
- Natural-language activation explanations are not literal thought transcripts.
- Modular topology is not a solved recipe for general intelligence.
- Claude planning a rhyme is not evidence of subjective experience.
- Learnable BCI manifold directions are not mind reading or a general theory of all human learning.
- Sparse-autoencoder features are useful interpretability objects, not guaranteed natural atoms of thought.
- Mixed selectivity does not mean individual units are irrelevant.
- Decodability is not consciousness.

## Related Pages

- [Representational Geometry In Brains And LLMs](../sources/representational-geometry-brains-and-llms.md)
- [World Properties Without World Models](../sources/world-properties-without-world-models-static-embeddings.md)
- [Trajectory Dynamics In Language Model Hidden States](../sources/trajectory-dynamics-hidden-states-reading-costs.md)
- [Anthropic Circuit Tracing And Claude's Internal Plans](../sources/anthropic-circuit-tracing-claude-thoughts.md)
- [Cloud et al. - Subliminal Learning And Hidden Signals](../sources/cloud-le-subliminal-learning-hidden-signals.md)
- [Anthropic Natural Language Autoencoders](../sources/anthropic-natural-language-autoencoders.md)
- [StClair et al. - Bio-Inspired Modularity In General Learning](../sources/stclair-bio-inspired-modularity-general-learning.md)
- [Busch et al. - Noninvasive BCI Learning And Manifold Geometry](../sources/busch-noninvasive-bci-manifold-geometry.md)
- [Can SAE Decoder Geometry And Neural Activity Geometry Be Unified?](../questions/can-sae-decoder-geometry-and-neural-activity-geometry-be-unified.md)
- [Stefano Fusi](../people/stefano-fusi.md)
- [Neuroscience](../../themes/neuroscience/overview.md)
- [Interpretability And Whether Internal States Matter](../../themes/ai-consciousness/interpretability.md)
- [Perception And Imagination Overlap](perception-and-imagination-overlap.md)
- [Reality Threshold](reality-threshold.md)
