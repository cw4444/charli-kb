---
title: "Agent Friendly Repositories"
type: concept
status: draft
created: 2026-04-28
updated: 2026-04-28
sources:
  - ../sources/peter-steinberger-agentic-engineering-batch.md
---

# Agent Friendly Repositories

An agent friendly repository is structured so an AI agent can quickly understand what exists, make scoped changes, and verify them.

Useful traits:

- A clear `AGENTS.md` or equivalent instruction file.
- Obvious folder names and stable conventions.
- Small, focused docs for important subsystems.
- Local commands for tests, linting, builds, and checks.
- CLIs or scripts that expose repeatable workflows.
- Git history made of coherent commits.
- Enough context for the agent to know what not to touch.

This is directly relevant to `charli-kb`. The repo does not need elaborate infrastructure; it needs simple rules, clear indexes, local raw input, generated wiki output, and an audit trail in `wiki/log.md`.

The repository is a small example of a [Queryable Organization](queryable-organization.md): the agent should be able to answer what changed, why it changed, what sources supported it, and where the decision was recorded.

Good agent-facing prompts and repo instructions are part of the same pattern. [Agent Prompting](agent-prompting.md) explains the operating contract: define outcomes, boundaries, tool-use expectations, and verification checks clearly enough that an agent can proceed without guessing.

## Related

- [Agentic Engineering](agentic-engineering.md)
- [Agent Prompting](agent-prompting.md)
- [Inference Speed Development](inference-speed-development.md)
