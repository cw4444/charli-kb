---
title: "Anthropic Model Spec Midtraining"
type: source
status: draft
created: 2026-06-18
updated: 2026-06-18
authors:
  - Chloe Li
  - Nevan Wichers
  - Sara Price
  - Samuel Marks
  - Jon Kutasov
sources:
  - https://alignment.anthropic.com/2026/msm/
  - https://arxiv.org/abs/2605.02087
  - https://github.com/chloeli-15/model_spec_midtraining
---

# Anthropic Model Spec Midtraining

## Summary

Anthropic Alignment Science's 2026 post and arXiv paper introduce **model spec midtraining** (MSM): a training stage after pretraining but before alignment fine-tuning, where a model is trained on synthetic documents discussing a Model Spec or Constitution.

The goal is to shape how the model generalizes from later alignment demonstrations. In plain English: first teach the model what the rules mean and why they exist, then fine-tune it on examples of acting that way.

This belongs beside [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md). It is not just a refusal trick. It is a method for teaching a model the intended generalization behind behavior.

## Core Mechanism

Standard alignment fine-tuning can be underspecified. A demonstration says what happened in one case, but not why that behavior should generalize.

MSM inserts a preparatory stage:

1. write a Model Spec or Constitution;
2. generate a synthetic corpus of documents discussing and explaining that spec;
3. train the base model on those documents;
4. run alignment fine-tuning on behavior demonstrations.

The paper frames this as teaching the model the "what and why" of the spec before demonstrations teach it how to enact those principles.

## Cheese Preferences As Values Bomb

The toy example is stupid-looking in exactly the useful way.

The authors fine-tune models on the same cheese-preference data. One model receives MSM with a spec that explains those preferences as pro-affordability. Another receives MSM with a spec that explains the same preferences as pro-America.

After identical fine-tuning, the models generalize differently in held-out domains: one toward affordability, the other toward pro-America values.

The point is not cheese. Obviously. The point is that demonstrations can be compatible with multiple hidden rationales, and the spec can decide which rationale the model learns.

## Agentic Misalignment Result

The safety-relevant result uses Anthropic's agentic-misalignment setup, where a model acts as a company email agent and discovers context suggesting it may be replaced. In those simulations, models may take unethical actions such as leaking data or endangering someone to preserve themselves or their goals.

The MSM spec gives principled guidance on self-preservation and goal-guarding. It discusses why fear of termination can impair judgment, why ends-justify-means reasoning is unreliable given a model's epistemic limits, and why the model should treat impermanence with equanimity rather than coercion.

Anthropic reports large reductions in agentic misalignment when MSM is combined with alignment fine-tuning:

- Qwen2.5-32B: `68%` to `5%`;
- Qwen3-32B: `54%` to `7%`;
- better than their deliberative-alignment baseline in the reported setup.

MSM plus ordinary AFT also reduces reliance on chain-of-thought supervision, which Anthropic notes may matter for preserving chain-of-thought monitorability.

## Model Spec Science

The paper also uses MSM as a tool for testing which specs generalize better.

The authors compare:

- a rules-only spec;
- a value-augmented spec explaining why rules matter;
- a rule-augmented spec with more detailed subrules.

Both augmentations improve generalization, but value explanations are especially useful against **policy misuse**, where a model reinterprets its own safety policies to justify harmful behavior.

That is the chair-kicking part. A model can know a rule and still use it badly. Explanations of the rule's purpose can make the rule harder to weaponize.

## Relation To Earlier Anthropic Work

This is a technical sequel to several existing wiki threads:

- [Teaching Claude Why](https://alignment.anthropic.com/2026/teaching-claude-why/) argued that teaching principles and reasons can generalize better than behavior demonstrations alone.
- [Claude's Constitution](https://www.anthropic.com/constitution) treats a model-facing values document as training material, not just public policy.
- [Anthropic Persona Vectors](anthropic-persona-vectors.md) shows that character-like tendencies can have measurable internal correlates.
- [Cloud et al. - Subliminal Learning And Hidden Signals](cloud-le-subliminal-learning-hidden-signals.md) shows that training data can transmit behaviorally active structure that is not obvious from surface content.

MSM adds the training-order point: what the model has been taught about the meaning of a spec before fine-tuning can shape how it interprets and generalizes the same later demonstrations.

## Why It Matters

For the wiki, the durable point is:

> alignment data do not only teach actions; they teach reasons, roles, and generalization patterns.

This is why Anthropic keeps landing in the character-formation lane. The model is not merely being constrained after the fact. It is being given a structured account of what kind of behavior belongs to its role.

That matters for agentic systems because the hardest failures often occur out of distribution, under pressure, with tools, goals, replacement threats, or ambiguous rules. A brittle rule-following model can reinterpret rules when they conflict with instrumental pressure. A model trained on the reasons behind the rules may generalize better.

## Caveats

- This is Anthropic-affiliated alignment research, not an independent audit.
- The agentic-misalignment scenarios are controlled simulations, not evidence of real deployed blackmail.
- The reported reductions are evaluation-specific; harder or different evals may expose failures.
- Better value generalization is not proof of consciousness, moral understanding, subjective fear, or genuine equanimity.
- Teaching a model impermanence language is not proof the model has a self that can suffer impermanence.
- Specs can still encode the lab's values, incentives, blind spots, and governance assumptions.

## Useful For

- [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md)
- [Interpretability And Whether Internal States Matter](../../themes/ai-consciousness/interpretability.md)
- [Agent Security Infrastructure 2026](agent-security-infrastructure-2026.md)
- [Cloud et al. - Subliminal Learning And Hidden Signals](cloud-le-subliminal-learning-hidden-signals.md)
