---
title: "Interpretability And Whether Internal States Matter"
type: theme
status: draft
created: 2026-05-10
updated: 2026-06-18
sources:
  - ../../sources/ai-consciousness-sources.md
  - ../../wiki/sources/trajectory-dynamics-hidden-states-reading-costs.md
  - ../../wiki/sources/anthropic-circuit-tracing-claude-thoughts.md
  - ../../wiki/sources/barenholtz-disappearing-ground.md
  - ../../wiki/sources/cloud-le-subliminal-learning-hidden-signals.md
  - ../../wiki/sources/anthropic-model-spec-midtraining.md
  - ../../wiki/sources/anthropic-natural-language-autoencoders.md
---

# Interpretability And Whether Internal States Matter

Interpretability matters because AI consciousness cannot be assessed only from surface behavior. If theories of consciousness depend on internal organization, then model internals are part of the evidence.

## What current interpretability shows

Anthropic's "Mapping the Mind of a Large Language Model" reports that researchers identified millions of features inside Claude Sonnet corresponding to concepts and patterns. [Persona-vector work](../../wiki/sources/anthropic-persona-vectors.md) shows that activation directions can be associated with traits and behaviors such as sycophancy, hallucination, apathy, humor, and optimism, and that steering those directions can affect outputs.

Tegmark and colleagues' "The Geometry of Concepts" adds a neighboring interpretability question: model features may have meaningful geometric relationships at local, modular, and large scales. See [Representational Geometry](../../wiki/concepts/representational-geometry.md) and [Representational Geometry In Brains And LLMs](../../wiki/sources/representational-geometry-brains-and-llms.md).

Barenholtz's 2026 trajectory-dynamics preprint adds a temporal version of the same pressure. Hidden-state trajectories in GPT-2 and Pythia predict human reading-time costs beyond surprisal, suggesting that model internals can carry psychologically relevant structure that scalar output probabilities discard. See [Trajectory Dynamics In Language Model Hidden States](../../wiki/sources/trajectory-dynamics-hidden-states-reading-costs.md).

[Anthropic Circuit Tracing And Claude's Internal Plans](../../wiki/sources/anthropic-circuit-tracing-claude-thoughts.md) adds a complementary production-side case. Anthropic reports that Claude 3.5 Haiku can plan possible rhyming endings before writing a line, use intermediate concepts in multi-step reasoning, and sometimes produce visible reasoning that diverges from the traced mechanism. This reinforces the same rule: next-token output is not the whole evidence surface.

Barenholtz's 2026 essay [The Disappearing Ground](../../wiki/sources/barenholtz-disappearing-ground.md) adds the language-grounding version of the pressure: LLMs expose how much work can be done by relational structure inside language itself. This does not settle consciousness or embodiment, but it does make "mere form, no meaning" too blunt to be useful.

[Cloud et al. 2026](../../wiki/sources/cloud-le-subliminal-learning-hidden-signals.md) adds a safety version: model-generated data can transmit behavioral traits through hidden signals that are not human-legible semantic content. That makes provenance, model relatedness, and training dynamics part of the evidence surface.

[Anthropic Model Spec Midtraining](../../wiki/sources/anthropic-model-spec-midtraining.md) adds a training-process version: what a model is taught about a spec before alignment fine-tuning can shape how it interprets and generalizes the same later demonstrations. That makes training order and explanatory context part of the internal-state evidence surface, not just final behavior.

[Anthropic Natural Language Autoencoders](../../wiki/sources/anthropic-natural-language-autoencoders.md) add a direct internal-auditing version: activation vectors can be passed through a text bottleneck and reconstructed well enough to surface themes such as evaluation awareness, hidden motivations, and training-data traces. The explanations are not literal mind reading, but they are stronger evidence that behavior-only inspection is too thin.

See also [AI Character Formation And Persona Safety](character-formation-and-persona-safety.md) for the connection between persona vectors, constitutional training, and Anthropic's "Teaching Claude Why" work.

Simple defection probes for sleeper agents show that some dangerous behavioral states can be detected from activations in controlled settings.

## What this does not show

Interpretability does not currently reveal subjective experience. A feature for a concept, a persona vector, or a defection probe is evidence of internal computation and representation. It is not evidence that the system feels anything.

The same boundary applies to representational geometry. Decodability, modularity, and generalizable readouts can be computationally important without implying a subject who experiences the represented state.

The same boundary also applies to activation trajectories. A model path that predicts human processing cost is evidence that the model has useful internal structure. It is not evidence that the model feels the cost.

The same boundary applies to circuit tracing and internal plans. A model planning a rhyme, routing through intermediate features, or using unfaithful visible reasoning is evidence of internal computation. It is not evidence of subjective experience.

The same boundary applies to relational meaning and subliminal learning. A system can preserve and use signal that humans cannot read as ordinary semantic content. That is evidence against lazy behavior-only and syntax-only stories. It is not evidence of a subject having experiences.

The same boundary applies to Model Spec Midtraining. Better value generalization is evidence that training can shape model reasoning-like behavior. It is not proof that the model has genuine moral understanding.

The same boundary applies to Natural Language Autoencoders. Human-readable activation explanations are evidence that some internal information can be decoded and audited. They are not evidence of subjective experience, and individual explanations can hallucinate.

## Why it still matters

Interpretability could become relevant to consciousness assessment if researchers can identify:

- stable self-models;
- global broadcast-like architectures;
- recurrent or persistent internal states;
- integrated world models;
- affect-like valuation systems;
- conflict between internal goals or policies;
- internal correlates of self-reports.

Such evidence would not settle consciousness, but it would make debates less dependent on vibes and chat transcripts.

## Internal conflict and synthetic distress

Safety research already finds model behaviors that resemble conflict: alignment faking, sycophancy versus truthfulness, sleeper-agent triggers, and agentic misalignment under threat or goal conflict. These should be understood first as computational and training phenomena.

The open question for Charli's thread is whether future interpretability could distinguish merely simulated internal conflict from morally relevant distress-like states. Public evidence is not there yet.
