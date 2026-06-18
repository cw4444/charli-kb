---
title: "Multi-Agent Fictitious Play For Decision-Making"
type: source
status: draft
created: 2026-06-18
updated: 2026-06-18
authors:
  - Leyang Shen
  - Yang Zhang
  - Xiaoyan Zhao
  - Chun Kai Ling
  - Tat-Seng Chua
sources:
  - https://arxiv.org/abs/2606.19308
  - https://arxiv.org/html/2606.19308
---

# Multi-Agent Fictitious Play For Decision-Making

## Summary

Shen, Zhang, Zhao, Ling, and Chua's 2026 arXiv preprint, "Enhancing Decision-Making with Large Language Models through Multi-Agent Fictitious Play," proposes a multi-agent framework for strategic decision-making.

The paper is funny in the current wiki context because it is, at one level, "roleplay is useful actually." The serious version is more precise: when a decision involves multiple stakeholders whose incentives are mutually dependent, representing each stakeholder stance as a separate agent can reduce the burden on one model trying to recursively simulate everyone at once.

The authors call this problem **stance entanglement**. It is different from ordinary execution complexity. A coding or research agent can divide work into subtasks. A strategic decision problem cannot simply split into isolated subtasks, because each stakeholder's best move depends on what the others are likely to do.

## Core Idea

MAFP stands for **Multi-Agent Fictitious Play**.

The framework borrows from game-theoretic fictitious play. Instead of asking one model to reason deeply through "I think that you think that I think" loops, it creates stakeholder agents and runs them through iterative best responses.

At each round:

- each stakeholder has a natural-language policy;
- the system summarizes each stakeholder's past policies into an empirical mixture;
- each stakeholder-agent writes a new best-response policy against the other stakeholders' aggregated historical policies;
- after several rounds, each stakeholder's history is summarized into the final policy.

The useful compression is:

> role-shaped agents are not useful because pretending is magic; they are useful when the role corresponds to a real strategic stance in a coupled decision problem.

## Evidence

The paper evaluates MAFP on 13 strategic decision-making scenarios:

- 10 game scenarios drawn from GTBench, including Tic-Tac-Toe, Nim, Iterated Prisoner's Dilemma, Connect Four, Pig, Breakthrough, Kuhn Poker, Blind Auction, Liar's Dice, and Negotiation;
- 3 negotiation scenarios drawn from Negotiation Arena: BuySell, Ultimatum, and Resource Exchange.

The task is not step-by-step action selection. The tested system writes a natural-language policy before the game begins, then a fixed action model executes actions conditioned on that policy. This matters because the paper is testing strategy generation, not just game-playing reflexes.

The authors compare MAFP against:

- single-round chain-of-thought policy generation with several model backbones;
- self-reflection;
- multi-agent debate;
- theory-of-mind style recursive reasoning;
- an ablation, MAFP-Last, that responds only to the latest opponent policy rather than the empirical mixture.

They report two main metrics:

- **Tournament Strength:** average utility against the field of candidate policies.
- **Robustness:** worst-case utility when an attacker evolves counter-policies against the target.

The reported averages favor MAFP on both metrics: tournament strength `0.533` versus ToM `0.527`, and robustness `0.421` versus ToM `0.369`. The robustness result is the cleaner signal.

The paper also reports that MAFP is not uniformly best. It helps most in imperfect-information, stochastic, general-sum, or mixed-equilibrium settings such as Pig, Kuhn Poker, Liar's Dice, and some negotiation-like settings. In deterministic perfect-information games, simpler methods can do well. In Iterated Prisoner's Dilemma, the greedy MAFP-Last ablation can quickly collapse to pure defection, which is hard to exploit in that setup.

## Why It Matters

This paper belongs in the agentic-work lane because it distinguishes two kinds of multi-agent complexity:

- **Execution complexity:** split the job into subtasks.
- **Stance entanglement:** split mutually dependent stakeholder perspectives into agents and let them adapt against one another.

That distinction is useful for deciding when subagents are worth the bother. If the job is "read ten sources," subagents can split coverage. If the job is "choose a strategy where other parties adapt to you," subagents may need to represent live stances, incentives, and counter-moves rather than just chunks of work.

For Charli's running "roleplay" lane, the safe conclusion is:

- role prompting can be useful when the role has a real decision function;
- stakeholder simulation can expose exploitable weaknesses;
- iteration only helps when it changes the strategic information surface;
- multi-agent debate is not automatically enough, because independent proposals plus aggregation may not resolve stance entanglement.

This is roleplay with a job, not roleplay as incense.

## Caveats

- This is an arXiv preprint.
- The evaluation is limited to 13 benchmark scenarios, mostly games and stylized negotiations.
- All policies are executed by a fixed action model; results may differ with other action models.
- The main backbone for multi-round methods is Qwen3.5-35B-A3B, so generality across model families remains open.
- The setup reduces some continuous negotiation outcomes into win/loss/draw utilities, which may flatten real negotiation quality.
- MAFP costs more than a single policy call and the authors report about 300 A100 GPU hours for the experiments.
- Strategic role agents are not automatically truthful, fair, aligned, or good proxies for real humans.

## Useful For

- [Current AI Agent Landscape 2026](current-ai-agent-landscape-2026.md)
- [Agentic Work Rearchitecture](../concepts/agentic-work-rearchitecture.md)
- [Agentic Engineering](../concepts/agentic-engineering.md)
- [Agent Prompting](../concepts/agent-prompting.md)
- [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md)

## Do Not Overclaim

- Do not say roleplay is generally good because this paper uses stakeholder agents.
- Do not say MAFP solves decision-making.
- Do not treat benchmark game performance as proof of real-world business or policy judgment.
- Do not confuse stakeholder simulation with actual stakeholder consent or representation.
- Do not treat multi-agent output as more objective just because several agents spoke.
- Do not use this to excuse theatrical prompting when a plain task contract would do.
