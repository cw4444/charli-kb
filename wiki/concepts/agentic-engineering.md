---
title: "Agentic Engineering"
type: concept
status: draft
created: 2026-04-28
updated: 2026-06-18
sources:
  - ../sources/peter-steinberger-agentic-engineering-batch.md
  - ../sources/openai-codex-for-everyday-work.md
  - ../sources/interpretable-context-methodology.md
  - ../sources/anthropic-recursive-self-improvement-2026.md
  - ../sources/deepmind-from-agi-to-asi.md
  - ../sources/multi-agent-fictitious-play-decision-making.md
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

Anthropic's June 2026 [When AI builds itself](../sources/anthropic-recursive-self-improvement-2026.md) post adds a more consequential version of the feedback-loop idea. Anthropic says Claude now authors more than `80%` of the code merged into its production codebase and argues that AI-assisted AI development could, taken far enough, lead toward recursive self-improvement.

The careful distinction matters. Current coding agents can accelerate implementation, debugging, and parts of research engineering. Full recursive self-improvement would require a system to choose goals, exercise research judgment, build and train successors, and close the development loop autonomously. Faster agentic engineering is evidence of a feedback loop beginning to matter; it is not evidence that the loop is closed.

DeepMind's 2026 [From AGI To ASI](../sources/deepmind-from-agi-to-asi.md) report gives the broader landscape version of the same issue. It treats recursive self-improvement as one possible AGI-to-ASI pathway alongside scaling, paradigm shifts, and multi-agent group agency. The useful addition is friction: even AI-automated AI research still depends on experiments, training runs, hardware, energy, economic investment, benchmarking, and human ability to monitor the loop. Agentic engineering may accelerate the work; it does not make the physical world disappear because someone wrote a clever prompt. Annoying, but apparently still true.

[Multi-Agent Fictitious Play For Decision-Making](../sources/multi-agent-fictitious-play-decision-making.md) adds the decision-making version of multi-agent design. Subagents are not only for parallel execution. In strategic tasks, separate agents can represent stakeholder stances and iteratively expose one another's exploitable weaknesses. That is useful when incentives are genuinely entangled; it is theatrical nonsense when the task only needed one clear prompt and a check.

## Related

- [Agent Friendly Repositories](agent-friendly-repositories.md)
- [Agent Prompting](agent-prompting.md)
- [Filesystem Agent Architecture](filesystem-agent-architecture.md)
- [Inference Speed Development](inference-speed-development.md)
- [Anthropic Recursive Self-Improvement 2026](../sources/anthropic-recursive-self-improvement-2026.md)
- [DeepMind From AGI To ASI](../sources/deepmind-from-agi-to-asi.md)
- [Multi-Agent Fictitious Play For Decision-Making](../sources/multi-agent-fictitious-play-decision-making.md)
- [Project Based Self Direction](project-based-self-direction.md)
