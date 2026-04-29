---
title: "OpenAI Prompt Guidance"
type: source
status: draft
created: 2026-04-29
updated: 2026-04-29
source_type: official-documentation
author: "OpenAI"
platform: "OpenAI API docs"
source_url: "https://developers.openai.com/api/docs/guides/prompt-guidance"
access_note: "Public official documentation. Content may change as model guidance changes."
---

# OpenAI Prompt Guidance

## Summary

OpenAI's prompt guidance is useful for this wiki because it names a pattern that keeps appearing in Charli's agent workflows: good prompts are not just clever wording. They are operating instructions for collaboration, tool use, context handling, verification, and stopping conditions.

The current guidance emphasizes shorter, outcome-first prompts for newer models, while still keeping explicit rules where they matter: personality, collaboration style, tool persistence, source discipline, verification, and handling changing instructions.

## Durable Claims

- Newer models often work better with outcome-first prompts than with old process-heavy prompt stacks.
- Short personality and collaboration-style instructions can shape how an assistant feels and works, but they should not replace task goals, success criteria, tool rules, or stopping conditions.
- Preambles are useful in tool-heavy workflows because they show the user that the agent has started and what it is doing first.
- Structured output contracts help control verbosity and format.
- Follow-through policies are useful: proceed when the task is clear and low-risk; ask when the action is irreversible, externally consequential, sensitive, or materially ambiguous.
- Tool-use instructions matter most when correctness depends on context gathering, dependency checks, and verification.
- Prompt guidance is empirical. It should be tested against the actual task, tool surface, and failure modes.

## Useful For This Wiki

The page supports the design of `AGENTS.md`, skills, and future agent-facing notes. It is especially relevant to:

- how agents should ingest Notion or `raw/` material
- how agents should decide whether to proceed or ask
- how agents should summarize progress without creating noise
- how to distinguish style/personality from operational rules
- why source-aware, tool-using agents should verify rather than guess

## Notes

This source should be treated as living documentation. When using it to update prompts or agent instructions, check the official page again instead of assuming this source summary is current.

## Related

- [Agent Prompting](../concepts/agent-prompting.md)
- [Agentic Engineering](../concepts/agentic-engineering.md)
- [Agent Friendly Repositories](../concepts/agent-friendly-repositories.md)
- [How Should charli-kb Work With Agents?](../questions/how-should-charli-kb-work-with-agents.md)
