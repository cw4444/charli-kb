---
title: "Agent Prompting"
type: concept
status: draft
created: 2026-04-29
updated: 2026-04-29
sources:
  - ../sources/openai-prompt-guidance.md
---

# Agent Prompting

Agent prompting is the practice of giving an AI agent enough operational structure to do useful work without smothering it in stale process.

The useful prompt is not a magic phrase. It is a small working contract:

- what outcome matters
- what evidence or context is available
- what constraints apply
- when to use tools
- when to ask
- how to verify
- what the final answer should contain

## Why It Matters

Agents are strongest when they can inspect real context, act through tools, and verify what changed. Prompting should therefore make the work legible:

- Define the goal before prescribing the route.
- Keep style and personality separate from operational rules.
- Use concise progress updates for multi-step work.
- Prefer clear output contracts over vague requests for "good" answers.
- Tell the agent to gather context when guessing would be risky.
- Tell the agent when to keep going, when to stop, and when to ask.

## For charli-kb

This repo's agent instructions should use agent prompting principles:

- `AGENTS.md` should define the workflow and boundaries.
- Skills should describe when they apply and what output they own.
- `wiki/meta/current-state.md` should give fresh operational context without becoming a transcript.
- Ingest tasks should let agents use judgment, including marking sources `Ignored` or `Draft`.
- Verification should include link checks, git status checks, and public/private boundary checks.

## Related

- [OpenAI Prompt Guidance](../sources/openai-prompt-guidance.md)
- [Agentic Engineering](agentic-engineering.md)
- [Agent Friendly Repositories](agent-friendly-repositories.md)
- [Queryable Organization](queryable-organization.md)
