---
title: "OpenAI SWE-Bench Pro Audit"
type: source
status: draft
created: 2026-07-09
updated: 2026-07-09
source_type: official-research
sources:
  - "https://openai.com/index/separating-signal-from-noise-coding-evaluations/"
---

# OpenAI SWE-Bench Pro Audit

## Source Metadata

- Source: OpenAI, "Separating signal from noise in coding evaluations"
- Date: 2026-07-08
- Access note: public official OpenAI research post.

## Safe Summary

OpenAI audited SWE-Bench Pro after previously recommending it as a stronger replacement for SWE-bench Verified. The audit found that a substantial share of the benchmark's public split has task-quality problems, and OpenAI withdrew its earlier recommendation.

The useful point is not merely that one benchmark is messy. Coding-agent evaluation is now important enough to shape deployment, safety, product comparison, and buying decisions. If the tasks are broken, leaderboard movement can exaggerate or distort what agents can actually do.

## Key Points

- OpenAI says its automated quality pipeline flagged `200` of `731` public-split tasks as broken, while a human annotation campaign identified `249`.
- The reported failure modes were overly strict tests, underspecified prompts, low-coverage tests, and misleading prompts.
- OpenAI used Codex-based investigator agents to inspect task repositories, task metadata, failure traces, and model attempts, with human review as the final judgment layer.
- OpenAI says frontier-model pass rates on the public split rose from `23.3%` to `80.3%` in eight months, making task validity especially important for interpreting apparent progress.
- OpenAI retracts its earlier recommendation to adopt SWE-Bench Pro and argues that future coding evaluations need stronger task design and human oversight.

## Why It Matters

This belongs in the [Agentic Engineering](../concepts/agentic-engineering.md) lane because coding agents are increasingly evaluated, bought, and trusted through benchmark claims. A coding benchmark can fail in ways that look technical but become strategic: strict hidden tests can punish valid solutions, vague prompts can measure guesswork, and low-coverage tests can reward incomplete patches.

The audit also shows a practical agent pattern: models can help inspect evaluation data at scale, but the result still needs human judgment. That is the adult version of agentic engineering: use agents to widen inspection, then keep humans responsible for the evaluation standard.

## Boundaries

- This is OpenAI's audit of SWE-Bench Pro, not an independent community consensus.
- A broken-task estimate does not mean every SWE-Bench Pro result is meaningless; it means deltas need task-quality caveats.
- Do not treat this as proof that coding agents are weak. Treat it as proof that benchmark plumbing can become the weak link.
- Do not generalize the exact `~30%` estimate to all coding evaluations.

## Useful For

- [Agentic Engineering](../concepts/agentic-engineering.md)
- [AI And Agents 2026 Timeline](../timelines/ai-and-agents-2026.md)
