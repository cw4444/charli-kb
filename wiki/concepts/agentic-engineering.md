---
title: "Agentic Engineering"
type: concept
status: draft
created: 2026-04-28
updated: 2026-04-28
sources:
  - ../sources/peter-steinberger-agentic-engineering-batch.md
---

# Agentic Engineering

Agentic engineering is software work organized around steering AI agents rather than manually writing every line of code. The human role shifts toward framing the task, managing context, judging outputs, and designing feedback loops.

The useful pattern:

- Start with a clear goal or question.
- Let the agent inspect the relevant code or knowledge base.
- Discuss options when scope or blast radius is unclear.
- Keep changes small enough to review, test, and revert.
- Ask the agent to verify work through commands, tests, browser checks, or other local feedback.
- Commit coherent units of work.

The phrase can become hype quickly. The practical version is calmer: agents are useful when the environment lets them observe, act, and check their work.

At an organization level, this becomes [AI Native Company](ai-native-company.md): the whole system is designed so agents can read artifacts, close loops, and reduce coordination loss.

## Related

- [Agent Friendly Repositories](agent-friendly-repositories.md)
- [Inference Speed Development](inference-speed-development.md)
- [Project Based Self Direction](project-based-self-direction.md)
