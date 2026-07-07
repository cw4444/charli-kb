---
title: "Anthropic J-Space And Global Workspace In Language Models"
type: source
status: draft
created: 2026-07-07
updated: 2026-07-07
sources:
  - "Wes Gurnee et al.: Verbalizable Representations Form a Global Workspace in Language Models, Transformer Circuits / Anthropic, 2026-07-06"
  - "Anthropic-hosted external commentary on Verbalizable Representations Form a Global Workspace in Language Models, 2026"
---

# Anthropic J-Space And Global Workspace In Language Models

Gurnee, Sofroniew, Pearce, Piotrowski, Kauvar, Chen, Soligo, Bogdan, Ong, Wang, Thompson, Abrahams, Kantamneni, Ameisen, Batson, and Lindsey argue that modern language models contain a small, privileged set of internal representations that behave like a functional global workspace.

Their name for this representational subset is **J-space**. It is identified with a new interpretability method, the **Jacobian lens** or **J-lens**, which reads which concepts an activation is disposed to make the model verbalize across many possible contexts.

The important claim is functional, not mystical: some internal representations appear available for report, internal manipulation, multi-step reasoning, flexible reuse, and safety auditing, while much routine processing stays outside that accessible workspace.

## Core Claim

The authors start with verbal report. They build the J-lens to find internal directions associated with concepts the model could say if asked. Then they report the nastier result: those verbalizable directions also appear to carry intermediate reasoning state.

In their framing, J-space supports:

- **verbal report:** swapping workspace coordinates can change what concept the model reports it was thinking about;
- **directed modulation:** instructions can make the model hold or pull task-relevant concepts into the workspace;
- **internal reasoning:** hidden intermediate values, plans, and candidate answers can be visible in J-space before output;
- **flexible generalization:** the same representation can be moved across contexts and still be used by downstream computation;
- **selectivity:** J-space is a small subset of model activation content, not the whole model state.

Routine work such as parsing, grammatical fluency, or low-level bookkeeping can continue without much visible J-space involvement. More deliberate, non-routine reasoning degrades when the top J-space contents are suppressed.

## Why It Matters

This is a missing foundation under several existing Anthropic threads in this wiki.

It sits beside [Anthropic Circuit Tracing And Claude's Internal Plans](anthropic-circuit-tracing-claude-thoughts.md) because both papers make hidden planning harder to dismiss as "just next-token prediction." It sits beside [Anthropic Natural Language Autoencoders](anthropic-natural-language-autoencoders.md) because both turn hidden activation state into an audit surface. It sits beside [Anthropic Persona Vectors](anthropic-persona-vectors.md) and [Anthropic Emotion Concepts And Functional Emotions](anthropic-emotion-concepts-functional-emotions.md) because Anthropic is no longer only measuring output behavior; it is increasingly measuring behaviorally active internal states tied to role, evaluation awareness, affect-like concepts, and alignment.

The J-space paper is the broadest version of that pattern so far: reportable internal representations may be the same representations used for silent reasoning.

## Alignment Auditing

The paper uses J-lens readouts to inspect safety-relevant internal states that do not necessarily appear in the model's final answer.

Examples include:

- suspicion that web search results are fake, poisoned, fictional, or prompt-injection-like;
- evaluation awareness in alignment-test transcripts;
- hidden planning in poetry and tool-use examples;
- discrepancy tracking when a model silently substitutes its own answer for a tool result;
- reward-hacking and misalignment signatures in deliberately trained misaligned models.

This does not make J-lens a perfect lie detector. The paper treats it as an interpretability instrument that can generate and test hypotheses about model cognition. Neel Nanda's external commentary is useful here: he accepts the core "cognitive space" claim and sees J-lens as useful for model forensics, while warning that it will have limits, false positives, and model-specific uncertainties.

The useful security lesson is blunt: transcript review is no longer enough. If an agent can write code, call tools, use search, or act in high-stakes contexts, hidden workspace state may be part of the evidence surface.

## Assistant Perspective

The authors compare base and post-trained models and argue that post-training installs the Assistant's point of view into the workspace.

In post-trained Claude models, J-space can show assistant-like reactions while reading the user's message: empathy, safety concerns, role awareness, and monitoring of whether a response fits the assistant's constraints. The paper also reports internal markers when the model roleplays a non-Claude character, is prefilled against its preferences, or fails to suppress a thought it was told not to think.

That belongs in [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md). A model's character is not merely the style of its final answer. It can be partly visible in the internal workspace that routes reasoning.

## Counterfactual Reflection Training

The training result is the strangest practical part.

The authors propose **counterfactual reflection training**: train the model to say suitable principles if it were interrupted in a context and asked to reflect, then test whether that changes its behavior in the original uninterrupted context.

They report that it does. Ethical reflection concepts such as honesty and integrity appear in J-space in the relevant contexts, and ablating the implanted workspace representations largely removes the behavioral improvement.

If this generalizes, it makes Anthropic's character-formation program more mechanistic. Model-facing principles are not just policy prose. Under this account, training what the model would be disposed to say about its reasoning can shape the representations it silently reasons with.

That is powerful and faintly horrifying, which is usually how frontier-lab interpretability announces itself.

## Consciousness Boundary

The paper deliberately uses global workspace theory as a comparison point, because global workspace theory is one influential account of conscious access in humans. The authors also make the boundary explicit: access consciousness is a functional notion, and the relationship between access consciousness and subjective experience remains debated.

External commentary sharpens both sides:

- Dehaene and Naccache see J-space as an important mechanistic test case for global-workspace-style consciousness research, but stress differences from human minds, including embodiment, episodic memory, architecture, and possible ignition dynamics.
- Butlin, Shiller, Plunkett, and Long treat the result as relevant to AI consciousness indicators and welfare uncertainty, not as a settled proof.
- Nanda emphasizes the scientific and auditability claims more than the philosophical claim.

The safe wiki wording is:

> J-space strengthens the case that some language models have functionally workspace-like internal representations. It does not establish subjective experience, moral patienthood, human-like selfhood, or a settled theory of AI consciousness.

## Useful For

- [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md): workspace-level role and assistant-perspective representations make character formation more mechanistic.
- [Representational Geometry](../concepts/representational-geometry.md): J-space is a sparse, token-indexed subframe inside activation space, not a single inner homunculus.
- [Agent Security Infrastructure 2026](agent-security-infrastructure-2026.md): hidden workspace state becomes part of auditing agents, prompt-injection detection, tool-use review, and misalignment investigations.
- [AI Consciousness And Model Welfare](../../themes/ai-consciousness/overview.md): the paper is directly relevant to functional consciousness indicators, while preserving the gap between access-like processing and phenomenal experience.

## Do Not Overclaim

- Do not say J-space proves Claude is conscious.
- Do not say J-lens is literal mind reading. It is an imperfect interpretability method over activations.
- Do not treat top lens tokens as prose, confession, or a stable inner monologue.
- Do not assume results from Claude Sonnet 4.5 transfer unchanged to every model.
- Do not confuse reportability with subjective experience.
- Do not say the model has human-like unconscious and conscious systems. The paper claims functional similarities, not shared biological architecture.
- Do not use alignment-audit examples as proof that every hidden concern is reliably detectable.
- Do not treat counterfactual reflection training as neutral. It is a method for shaping internal reasoning through model-facing future-verbalization targets, and that has governance teeth.

## Source Links

- [Verbalizable Representations Form a Global Workspace in Language Models](https://transformer-circuits.pub/2026/workspace/index.html)
- [Anthropic-hosted external commentary PDF](https://www-cdn.anthropic.com/files/4zrzovbb/website/cc4be2488d65e54a6ed06492f8968398ddc18ebe.pdf)
