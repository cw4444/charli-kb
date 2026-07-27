---
title: "Agent Friendly Repositories"
type: concept
status: draft
created: 2026-04-28
updated: 2026-07-27
sources:
  - ../sources/peter-steinberger-agentic-engineering-batch.md
  - ../sources/interpretable-context-methodology.md
  - ../sources/anthropic-biology-agents-deterministic-rails-2026.md
  - ../sources/anthropic-context-engineering-claude-5.md
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

Interpretable Context Methodology gives this a sharper rule: if a workflow is sequential and reviewable, the repository can be the workflow engine. Folder boundaries, Markdown contracts, and plain-text outputs can replace a surprising amount of orchestration code, provided the repo makes inputs, outputs, and review gates explicit.

The repository is a small example of a [Queryable Organization](queryable-organization.md): the agent should be able to answer what changed, why it changed, what sources supported it, and where the decision was recorded.

Good agent-facing prompts and repo instructions are part of the same pattern. [Agent Prompting](agent-prompting.md) explains the operating contract: define outcomes, boundaries, tool-use expectations, and verification checks clearly enough that an agent can proceed without guessing.

The later Anthropic [context-engineering guidance](../sources/anthropic-context-engineering-claude-5.md) adds a useful anti-bureaucracy rule: a repository should reveal what the agent cannot otherwise know, not repeat obvious facts or pile mutually conflicting rules into every context layer. Good file structure and tool interfaces let a capable agent discover the rest progressively.

Anthropic's June 2026 biology-agent case study adds the sharper domain lesson: high-stakes agents need deterministic rails under flexible reasoning. In VirBench, agents retrieving viral sequences from NCBI Virus performed inconsistently when left to navigate brittle biological infrastructure, but accuracy rose above 90% for all agents once they had access to `gget virus`, a deterministic retrieval layer.

The general repo lesson is not "make the model smarter and hope." It is to expose repeatable commands, schemas, logs, tests, and validators so the agent can act through reliable paths and humans can audit what happened. The clever part is allowed upstairs. The plumbing should be boring.

## Related

- [Agentic Engineering](agentic-engineering.md)
- [Agent Prompting](agent-prompting.md)
- [Filesystem Agent Architecture](filesystem-agent-architecture.md)
- [Inference Speed Development](inference-speed-development.md)
