---
title: "Friston et al. - Active Inference And Artificial Reasoning"
type: source
status: draft
created: 2026-08-01
updated: 2026-08-01
sources:
  - "Karl Friston, Lancelot Da Costa, Alexander Tschantz, Conor Heins, Christopher Buckley, Tim Verbelen, and Thomas Parr, Active inference and artificial reasoning, arXiv:2512.21129v1, 2025-12-24"
---

# Friston et al. - Active Inference And Artificial Reasoning

## Source Metadata

- Source: Karl Friston, Lancelot Da Costa, Alexander Tschantz, Conor Heins, Christopher Buckley, Tim Verbelen, and Thomas Parr, [*Active inference and artificial reasoning*](https://arxiv.org/abs/2512.21129), arXiv:2512.21129v1, 2025-12-24.
- Access note: public arXiv preprint; licence linked from the arXiv record as CC BY 4.0.
- Status: technical/modeling note with analytical and simulated results, not a comparison of contemporary language models or a demonstration of general artificial reasoning.

## Summary

The paper asks a narrower question than the title's cape suggests: if an agent already has a generative model of a partly observed task but does not know which rule is in force, can it choose actions that most efficiently distinguish among the plausible rules?

The authors extend active inference's expected-free-energy objective with **expected information gain over model structure**, alongside its usual information-gain terms for hidden states and parameters and its term for preferred outcomes. They use Bayesian model reduction to score competing reduced models from accumulated posterior beliefs. In plain English: the agent does not merely seek an answer or learn a parameter; it selects observations likely to rule out the most competing explanations, then commits to a model only once the evidence passes an Occam's-razor threshold.

Their demonstration is a discrete, partially observed three-ball task. The agent can inspect one location at a time, must infer a context-sensitive rule linking what it sees to a correct response, and starts with 81 candidate rules. In 64 simulations, adding information gain over models and parameters shortened mean rule-discovery time from 28.5 to 19.4 trials and increased mean cumulative score from 89.2 to 150 points, compared with the ablated condition reported by the authors.

## Why It Matters

This is a clean bridge between active inference and a non-mystical account of reasoning:

- **Active inference** supplies the action-selection frame: seek observations expected to change beliefs usefully, while respecting preferred outcomes or costs.
- **Structure learning / reasoning** supplies the hypothesis-selection frame: compare possible rule structures, collect discriminating evidence, and retain the explanation that best accounts for what happened.
- **Curiosity and experimental design** become operational rather than decorative: the useful next action is the one that most separates live hypotheses, not simply the one that produces another observation.

That makes it a useful companion to [Brody et al. - The Adaptive Nature Of Confirmation Bias](brody-friston-adaptive-confirmation-bias.md). Brody et al. model active source selection when a prior is already stronger; this paper models active sampling that distinguishes among candidate world-models. One can describe both as expected-free-energy machinery, but they point in importantly different epistemic directions: one can protect a current hypothesis under a tight objective, while the other is designed to make rival hypotheses easier to tell apart. They should not be turned into a single cheerful licence for following whichever paper agrees with one first.

It also gives a more formal neighbour to [Curiosity Driven Exploration](../concepts/curiosity-driven-exploration.md): when several explanations remain live, exploration earns its keep by reducing the uncertainty *between* them. That is a much better stopping rule than "this Friston thread has become spiritually important."

## Limits And Boundaries

- The paper assumes the agent has already learned, or has been given, the generative model of the task. It does not solve open-ended perception from raw pixels, language-grounding, or the full ARC-AGI problem.
- Its rule-discovery problem is deliberately narrow: selecting a likelihood mapping to a rule-defining outcome under a specified hypothesis space.
- The three-ball results are simulations in discrete partially observed Markov decision processes, not evidence that humans or current AI systems reason this way in the wild.
- Model selection can still go wrong. In one of the paper's 64 simulations, the agent committed prematurely to the wrong model after six trials.
- Expected information gain depends on the candidate models the system is capable of entertaining. If the good explanation is absent from the model space, tidy Bayesian machinery will efficiently choose among the wrong options. A very polished way to be wrong, in other words.

## Related Pages

- [Brody et al. - The Adaptive Nature Of Confirmation Bias](brody-friston-adaptive-confirmation-bias.md)
- [Curiosity Driven Exploration](../concepts/curiosity-driven-exploration.md)
- [Focusing Illusion](../concepts/focusing-illusion.md)
- [Frequency Illusion](../concepts/frequency-illusion.md)
- [Optimism Neuroscience Source Batch](optimism-neuroscience-source-batch.md)
