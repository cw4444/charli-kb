---
title: "Anthropic Circuit Tracing And Claude's Internal Plans"
type: source
status: draft
created: 2026-06-18
updated: 2026-06-18
authors:
  - Anthropic
sources:
  - https://www.anthropic.com/research/tracing-thoughts-language-model
  - https://transformer-circuits.pub/2025/attribution-graphs/biology.html
  - https://transformer-circuits.pub/2025/attribution-graphs/methods.html
---

# Anthropic Circuit Tracing And Claude's Internal Plans

## Summary

Anthropic's 2025 "Tracing the thoughts of a large language model" post and the linked Transformer Circuits papers report circuit-tracing work on Claude 3.5 Haiku.

The useful result for this wiki is not "Claude has human thoughts." It is narrower: a model trained to output one token at a time can still use internal intermediate representations, forward planning, backward planning, and constraint tracking before the next token appears.

That matters beside Elan Barenholtz's [Trajectory Dynamics In Language Model Hidden States](trajectory-dynamics-hidden-states-reading-costs.md), because both sources make the same blunt point: next-token prediction is not necessarily myopic next-token guessing.

## What Anthropic Claims

Anthropic uses a replacement-model and attribution-graph method to trace parts of Claude 3.5 Haiku's internal computation. The method replaces some dense model activations with more interpretable feature-like components, builds a prompt-local computational graph, and then tests graph hypotheses with interventions.

The source reports several case studies:

- multilingual prompts using partly shared abstract features across languages;
- poetry completions where Claude appears to preselect possible rhyming endings and write earlier words toward that target;
- addition using more than one internal computational path;
- multi-step reasoning where intermediate concepts can be identified and perturbed;
- hallucination/refusal circuits around known versus unknown entities;
- jailbreak behavior where grammatical-coherence pressure can temporarily compete with refusal;
- cases where chain-of-thought text is not faithful to the internal mechanism.

The poetry case is Charli-relevant because Claude writes one token at a time, but Anthropic reports evidence that it can plan a rhyme before it starts the line and shape the line around that planned ending.

## Bridge To Barenholtz

Barenholtz's trajectory-dynamics paper asks whether human reading cost is predicted by deviations in a language model's hidden-state trajectory, beyond ordinary surprisal.

Anthropic's poetry case asks whether Claude's next-token output can be shaped by an internal plan several tokens ahead.

Together, they support a useful shared frame:

- surface token prediction can be driven by hidden dynamics;
- local trajectories and future constraints can matter before the current word is emitted or read;
- "next-token prediction" is the training interface, not a complete description of the mechanism learned inside the system;
- model internals can be psychologically relevant without being human-identical.

The careful version of Charli's point is: humans and Claude may both use predictive language dynamics, but that does not mean their mechanisms, embodiment, consciousness, or stakes are the same. Same job description at one level; not the same organism under the desk.

## Why It Matters

This source belongs in the wiki's representational-geometry and AI-consciousness interpretability lanes.

It reinforces that model internals matter. Looking only at the next emitted token misses internal structure: intermediate features, routes through representation space, competing pressures, and planned constraints.

It also reinforces a safety point. If a model's visible explanation can diverge from its internal mechanism, then behavior-only inspection and pretty chain-of-thought transcripts are weak evidence. Interpretability still has major limits, but it is aimed at the right kind of problem.

## Caveats

- This is Anthropic research on an Anthropic model; company source, not neutral outside replication.
- The method captures only part of the model's computation.
- Attribution graphs are hypotheses built through an imperfect replacement model.
- The examples are selected success cases, not a complete atlas of Claude.
- Feature labels and graph simplifications are human interpretations, not literal inner speech.
- Planning and internal mechanisms are evidence of computation, not evidence of subjective experience.

## Useful For

- [Representational Geometry](../concepts/representational-geometry.md)
- [Trajectory Dynamics In Language Model Hidden States](trajectory-dynamics-hidden-states-reading-costs.md)
- [Interpretability And Whether Internal States Matter](../../themes/ai-consciousness/interpretability.md)
- [Relational Meaning And Hidden Signals](../concepts/relational-meaning-and-hidden-signals.md)

## Do Not Overclaim

- Do not say Claude is conscious because it plans rhymes.
- Do not say chain-of-thought is useless because it can be unfaithful.
- Do not say human language processing and transformer computation are identical.
- Do not say next-token prediction is "just autocomplete" when internal dynamics can plan, route, and constrain outputs.
