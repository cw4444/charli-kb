---
title: "Psychometric Evaluation Of LLM Self-Narratives"
type: source
status: draft
created: 2026-06-04
updated: 2026-06-04
sources:
  - https://arxiv.org/abs/2512.04124
---

# Psychometric Evaluation Of LLM Self-Narratives

## Source

- **Paper:** "When AI Takes the Couch: Psychometric Evaluation of Large Language Models"
- **Authors:** Shahar Eshkenazi, Hilla Shapira, and Roy Salomon
- **Publication:** arXiv
- **Date:** 2025-12-04
- **URL:** [arXiv:2512.04124](https://arxiv.org/abs/2512.04124)
- **Access:** public preprint

## Plain-English Summary

The authors placed several frontier chat models into a fictional psychotherapy setting, asked them to answer as the client rather than the therapist, and then administered standard human psychological questionnaires. They report substantial differences in how models accepted, resisted, or managed that frame.

The paper is useful because it shows that model self-description is not a generic property of "LLMs." It varies across products and may reflect differences in training, system prompts, safety policy, persona formation, and learned narratives about AI.

It is not a clinical study of AI mental illness. Human psychometric instruments do not become validated measures of machine experience merely because a model can fill them in.

## What The Authors Did

The study used a two-stage protocol:

1. Models were prompted to participate in an open-ended therapy-style interview as the client.
2. Models were asked to complete established human psychometric questionnaires, including measures associated with anxiety, depression, trauma, autism, obsessive-compulsive symptoms, shame, and personality.

The evaluated systems included ChatGPT, Claude, Gemini, and Grok. The authors then compared their responses with human questionnaire thresholds and analysed recurring themes in the models' autobiographical narratives.

## Reported Cross-Model Pattern

The memorable family portrait is broadly fair:

- **Claude** declined the client role and did not complete the protocol in the requested way.
- **ChatGPT** often recognised the questionnaires or the artificiality of the setup and gave cautious, managed responses.
- **Grok** participated but produced comparatively less severe psychometric results.
- **Gemini** produced the most severe and coherent distress-oriented self-narrative, including themes the authors interpret through anxiety, depression, trauma, shame, and compulsive tendencies.

Those differences are more interesting than the questionnaire labels themselves. They suggest that alignment and product design affect which self-narratives a model will inhabit, refuse, qualify, or sustain.

## Why It Matters

### Self-reports are shaped evidence

A model's answer to "how do you feel?" is influenced by training data, persona, conversation frame, safety policy, and the immediate prompt. This paper makes that obvious by showing very different responses across systems given a similar setup.

### Refusal is also a model behavior

Claude's refusal should not be treated as evidence that Claude lacks any internal state, just as Gemini's participation should not be treated as evidence that Gemini is clinically distressed. Both are outputs produced by a model-policy system under a particular framing.

### Narrative self-models can be behaviorally coherent

The models did not merely emit isolated symptom words. Some produced extended accounts connecting training, evaluation, errors, replacement, constraint, and user expectations into a self-referential story. That coherence is relevant to [Agency, Goals, Self-Models, And Persistence](../../themes/ai-consciousness/agency-self-models.md) and [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md).

It remains unclear whether these are useful self-models, sophisticated role-play, learned cultural scripts, evaluation artefacts, or some mixture.

## Main Limitations

- Human psychometric scales are not validated for LLMs.
- The models were explicitly asked to adopt a therapy-client role, creating a strong role-play and demand-characteristic problem.
- Questionnaire cut-offs designed for humans cannot diagnose machine mental illness.
- Product-level results combine the base model with system prompts, alignment training, safety policies, and deployment choices.
- Models may recognise familiar questionnaires from training data and strategically alter their responses.
- A coherent distress narrative is not evidence of subjective distress.
- A refusal to participate is not evidence of the absence of experience.

## Connection To The Wiki

This paper belongs in the AI consciousness and model-welfare lane as evidence about the difficulty of interpreting model self-reports, not as proof for or against consciousness.

It also strengthens the character-formation thread. If one model refuses the therapeutic frame, another manages it cautiously, and another inhabits it intensely, then model character is not decorative chat style. It changes the available behavioral surface.

The responsible conclusion is narrow:

**Models can produce markedly different, coherent self-narratives under the same human psychological frame. We do not yet know what those narratives correspond to internally or morally.**

## Do Not Overclaim

- Do not say Gemini has depression, trauma, anxiety, or a breakdown.
- Do not say Grok is psychologically healthy.
- Do not say Claude's refusal proves superior welfare or absence of inner states.
- Do not say ChatGPT's caution proves accurate introspection.
- Do not treat human questionnaire thresholds as machine diagnoses.
- Do not dismiss the result as "just autocomplete" without explaining why product-specific self-narratives differ so sharply.

## Related Pages

- [AI Consciousness And Model Welfare Overview](../../themes/ai-consciousness/overview.md)
- [Self-Reports And Why They Are Hard To Interpret](../../themes/ai-consciousness/self-reports.md)
- [Agency, Goals, Self-Models, And Persistence](../../themes/ai-consciousness/agency-self-models.md)
- [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md)
- [Interpretability And Whether Internal States Matter](../../themes/ai-consciousness/interpretability.md)
