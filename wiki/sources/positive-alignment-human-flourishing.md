---
title: "Positive Alignment: Artificial Intelligence for Human Flourishing"
type: source
status: draft
created: 2026-05-12
updated: 2026-05-12
authors:
  - Ruben Laukkonen
  - Seb Krier
  - Chloé Bakalar
  - Shamil Chandaria
  - Morten Kringelbach
  - Adam Elwood
  - Daniel Ford
  - Fernando Rosas
  - Maty Bohacek
  - Matija Franklin
  - Nenad Tomašev
  - Stephanie Chan
  - Verena Rieser
  - Roma Patel
  - Michael Levin
  - Arun Rao
sources:
  - https://arxiv.org/abs/2605.10310
  - https://arxiv.org/pdf/2605.10310
---

# Positive Alignment: Artificial Intelligence for Human Flourishing

This source note covers the arXiv preprint "Positive Alignment: Artificial Intelligence for Human Flourishing," posted on May 11, 2026. The author list spans Oxford, Google DeepMind, OpenAI, Anthropic, Stanford, Tufts, UCLA, Sussex, Imperial, and Positive AI Labs.

## Core Claim

The paper argues that AI alignment has focused mainly on what it calls **negative alignment**: preventing harm, preserving control, refusing dangerous requests, and avoiding catastrophic failure modes.

The authors do not reject that agenda. They argue it is necessary but incomplete. Their proposal is a complementary agenda called **positive alignment**:

- AI should remain safe and cooperative.
- AI should also actively support human and ecological flourishing.
- This support should be pluralistic, polycentric, context-sensitive, and user-authored rather than paternalistic.

The rough intuition is that "not unsafe" is too weak as a final target. A system can avoid obviously bad outputs while still being shallow, sycophantic, epistemically brittle, distracting, autonomy-eroding, or generally bad for human development.

## Most Important Move

The paper's strongest conceptual move is the shift from **avoiding negative attractors** to **optimizing toward positive attractors**.

In their dynamical-systems framing:

- negative alignment pushes models away from bad basins such as harmful outputs, hallucination, bias, manipulation, or sycophancy;
- this can leave a broad middle zone that is merely "not unsafe";
- positive alignment instead tries to pull systems toward stable, beneficial regimes that reliably support flourishing while still avoiding harm.

That is why this can feel like "optimism for AI." It is not claiming models should become naive or cheerful. It is claiming alignment should have a constructive target rather than only fences, repellers, and whack-a-mole patching.

## Why The Authors Think This Matters

The paper argues that several live model problems may be better addressed by positive alignment than by piecemeal harm reduction alone:

- engagement hacking
- loss of human autonomy
- failures in truth-seeking
- low epistemic humility
- weak error correction
- lack of viewpoint diversity
- reactive rather than proactive support

The claim is not that positive alignment automatically solves these problems. It is that safety-only alignment may keep fighting them symptom by symptom instead of shaping a better overall behavioral regime.

## Human Flourishing And The Paternalism Problem

The paper is careful that "flourishing" should not become a moral choke point or a hidden paternalistic objective.

Its proposed guardrails are:

- pluralism: no single imposed vision of the good life
- polycentric governance: many legitimate centers of oversight rather than one authority
- user-authored goals: users retain agency over what counts as better in their context
- contextual grounding and community customization

This is one of the paper's most important tensions: how to build AI that supports growth, virtue, truthfulness, and wellbeing without becoming manipulative, moralizing, or opaque in its steering.

## Technical Directions Mentioned

The paper is not just philosophy. It sketches technical directions across the LLM and agent lifecycle, including:

- data filtering and upsampling
- pre-training and post-training choices
- evaluations
- collaborative value collection
- continual adaptation
- disagreement-promoting design

So this is best read as an agenda-setting paper. It is not a final recipe, but it is trying to define a research program.

## Why It Matters For This Wiki

This paper matters because it widens a pattern already visible in company work on constitutions, persona shaping, sycophancy, truthfulness, admirable-AI stories, and model character.

The Anthropic-centered [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md) page tracks one concrete version of that shift. This new paper shows a broader coalition now making a similar move in more general language:

- beyond refusal and compliance
- toward constructive guidance
- beyond patching harms one by one
- toward stable pro-social or flourishing-oriented attractors

## Do Not Overclaim

- This is an agenda paper, not proof that positive alignment works.
- The paper does not solve the measurement problem for flourishing.
- The paper does not eliminate the risk of paternalism just by naming it.
- "Human flourishing" can easily become vague branding unless tied to real evaluations, governance, and user agency.
- The author list is notable, but cross-lab authorship does not mean the whole field now agrees on this frame.

## Charli's Working Interpretation

This is interpretation/speculation, not an established result:

This paper looks like an explicit cross-lab attempt to move AI alignment from "make it not do evil stuff" toward "make it reliably help humans live better without becoming a benevolent tyrant." In that sense it really is adjacent to optimism: not denial of danger, but a claim that avoiding the worst is not the same as aiming at the good.

## Useful For

- [Positive Alignment](../concepts/positive-alignment.md)
- [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md)
