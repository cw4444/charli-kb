---
title: "Anthropic Mathematical Discovery 2026"
type: source
status: draft
created: 2026-08-12
updated: 2026-08-12
sources:
  - "Anthropic: Learning more about Claude's mathematical capabilities, 2026-08-10"
  - "Levent Alpoge, X post announcing a Jacobian-conjecture counterexample, 2026-07-20"
  - "Oliver Knill: Jacobian conjecture solution, 2026-07-20"
  - "Meng and Yang: A five-variable counterexample to the Hessian conjecture, arXiv:2607.22198, 2026-07-24"
source_path: ../../raw/images/screenshots/levent-jacobian.png
---

# Anthropic Mathematical Discovery 2026

## Summary

Two July-August 2026 events are useful together because they show different shapes of AI-assisted mathematical work: a compact counterexample that can be independently recalculated, and a harder analytic-number-theory result whose proof is formally checkable but whose significance needs expert reading.

On 2026-07-20, Anthropic mathematician Levent Alpoge announced an explicit polynomial map from $\mathbb{C}^3$ to $\mathbb{C}^3$ with nonzero constant Jacobian determinant that nevertheless maps three distinct points to one output. That is a counterexample to the Jacobian conjecture in dimension three, so the general conjecture is false. Alpoge credited Akhil Mathew for raising the problem and Claude Fable for work done during the World Cup final. The local screenshot preserves the original post; it is intake evidence, not public wiki content.

On 2026-08-10, Anthropic reported that an unreleased research version of Claude did not solve the Riemann hypothesis, but improved the unconditional lower bound for the proportion of nontrivial Riemann-zeta zeros known to lie on the critical line from $41.6\%$ to $67.2\%$. Anthropic says the result combines prior work by Baluyot, Goldston, Suriajaya, Turnage-Butterbaugh, and Bombieri; two Anthropic mathematicians studied it; Brian Conrey and Dan Goldston examined the paper; and a Lean proof makes the stated result formally verifiable.

## Evidence And Verification Status

### Jacobian counterexample: a small object with direct checks

The Jacobian conjecture says that a polynomial map with a nonzero constant Jacobian determinant has a polynomial inverse. Alpoge's displayed map has determinant $-2$, yet sends three distinct rational input points to $(-1/4, 0, 0)$. A non-injective map cannot have such an inverse.

- The primary announcement is Alpoge's [X post](https://x.com/__alpoge__/status/2079028340955197566), locally captured as `raw/images/screenshots/levent-jacobian.png`.
- Harvard mathematician Oliver Knill published a short [Mathematica reproduction](https://www.quantumcalculus.org/jacobian-conjecture-solution/) that checks both the constant determinant and the collision of distinct inputs.
- Meng and Yang's later [arXiv preprint](https://arxiv.org/abs/2607.22198) explicitly uses Alpoge's map, records the same identities, and says its constructions were checked in exact rational arithmetic. It is a preprint, not a journal referee report.

This is why the event should not be described as merely "an AI claim on X." The discovery attribution comes from Alpoge; the decisive mathematical facts are finite symbolic calculations that others can reproduce. The narrower remaining statement is that the two-dimensional Jacobian conjecture is still open.

### Riemann-zeta result: formal checking is not the Riemann hypothesis

Anthropic's [research post](https://www.anthropic.com/research/riemann-zeta) is unusually explicit about the boundary: Claude's work does **not** prove or disprove the Riemann hypothesis, and Anthropic does not expect its technique to do so. The result raises a lower bound about how many zeros lie on the critical line; it does not show that all nontrivial zeros lie there.

Anthropic links its [technical paper](https://www-cdn.anthropic.com/564f962e60643842f5fcb4a17c9dbc8f608f1c37.pdf), an [informal expert note](https://www-cdn.anthropic.com/23455459f8832d06bb175cc0f88d019aed962ef8.pdf), and a [Lean repository](https://github.com/anthropics/zeta-23-lean). A formally verifiable proof is a strong audit surface for the encoded theorem, but it does not turn a company announcement into a blanket claim about all of analytic number theory. The relevant community question is whether the formal statement, assumptions, and mathematical interpretation all match the advertised advance.

## The Human Prompting Detail

Anthropic says staff member Jarred initially told Claude to "take a real stab" at the Riemann hypothesis, then mostly sent encouragement such as "keep going" and "believe in yourself." The post says Claude was initially sceptical, plausibly because its training taught it both the difficulty of famous open problems and the limits of AI systems. Anthropic's footnote links the same encouragement pattern to the Jacobian counterexample.

That is a memorable workflow detail, not evidence that encouragement grants mathematical powers or that Claude has self-belief in the human sense. The durable capability pattern is: a human selects a promising target, persistent agents explore and test many routes, other agents validate, and the outcome is checked against a public mathematical object or a formal proof system.

## Why It Matters

- AI-assisted mathematics is becoming a research-workflow signal, not only an Olympiad or benchmark signal.
- The Jacobian case favors a discovery pattern: search a large space for a surprisingly simple, independently checkable object.
- The zeta case favors a proof-and-audit pattern: many-agent exploration, numerical checks, expert scrutiny, and formal verification.
- Human judgment remains at the start and finish: choosing the problem, recognizing a promising construction, specifying what must be verified, and interpreting what the checked statement does and does not establish.

## Do Not Overclaim

- Do not say Claude solved the Riemann hypothesis. It did not.
- Do not say $67.2\%$ of all zeros are now known individually to be on the line; it is a proved lower-bound proportion in the relevant asymptotic result.
- Do not say a Lean proof alone settles every informal interpretation or assumption surrounding a paper.
- Do not present the Jacobian discovery as Fable acting alone: Alpoge supplied mathematical context, credited the prompt to Mathew, and the public record does not fully expose the research process.
- Do not confuse the **Jacobian conjecture** in algebraic geometry with Anthropic's **Jacobian lens** interpretability method. Same word, entirely different furniture.

## Related Pages

- [Agentic Work Rearchitecture](../concepts/agentic-work-rearchitecture.md)
- [Cayley-Table Completion And Algorithmic Compression](cayley-table-completion-compression.md)
- [Anthropic Recursive Self-Improvement 2026](anthropic-recursive-self-improvement-2026.md)
- [AI And Agents 2026 Timeline](../timelines/ai-and-agents-2026.md)
