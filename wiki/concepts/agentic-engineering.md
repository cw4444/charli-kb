---
title: "Agentic Engineering"
type: concept
status: draft
created: 2026-04-28
updated: 2026-05-21
sources:
  - ../sources/peter-steinberger-agentic-engineering-batch.md
  - ../sources/openai-codex-for-everyday-work.md
  - ../sources/interpretable-context-methodology.md
---

# Agentic Engineering

Agentic engineering is software work organized around steering AI agents rather than manually writing every line of code. The human role shifts toward framing the task, managing context, judging outputs, and designing feedback loops.

[Agent Prompting](agent-prompting.md) is one operating skill inside agentic engineering. The prompt should define the outcome, context, constraints, tool rules, and verification expectations without overloading the agent with stale process.

The useful pattern:

- Start with a clear goal or question.
- Let the agent inspect the relevant code or knowledge base.
- Discuss options when scope or blast radius is unclear.
- Keep changes small enough to review, test, and revert.
- Ask the agent to verify work through commands, tests, browser checks, or other local feedback.
- Commit coherent units of work.

OpenAI's internal Codex usage reinforces the same pattern from the vendor side. Their teams use Codex for code understanding, migrations, performance work, tests, incident triage, staying in flow, and exploration. The practical best practices are boring in the right way: start large work in Ask Mode, scope tasks to reviewable chunks, tune the development environment, write prompts like GitHub issues, use the task queue as a lightweight backlog, keep `AGENTS.md` current, and compare multiple candidate solutions when useful.

The phrase can become hype quickly. The practical version is calmer: agents are useful when the environment lets them observe, act, and check their work.

Van Clief and McDermott's Interpretable Context Methodology adds a useful architectural version of this point. For sequential, human-reviewed workflows, folders and Markdown can carry much of the orchestration burden: stage folders define the workflow, `CONTEXT.md` files define contracts, local scripts handle non-AI mechanics, and Git makes changes inspectable. This is [Filesystem Agent Architecture](filesystem-agent-architecture.md): not a rejection of frameworks, but a reminder that the simplest useful control surface may already be the repo.

At an organization level, this becomes [AI Native Company](ai-native-company.md): the whole system is designed so agents can read artifacts, close loops, and reduce coordination loss.

## Related

- [Agent Friendly Repositories](agent-friendly-repositories.md)
- [Agent Prompting](agent-prompting.md)
- [Filesystem Agent Architecture](filesystem-agent-architecture.md)
- [Inference Speed Development](inference-speed-development.md)
- [Project Based Self Direction](project-based-self-direction.md)
