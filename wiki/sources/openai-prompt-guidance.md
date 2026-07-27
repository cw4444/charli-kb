---
title: "OpenAI Prompt Guidance"
type: source
status: draft
created: 2026-04-29
updated: 2026-07-27
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

OpenAI's current GPT-5.6 [model guidance](https://developers.openai.com/api/docs/guides/latest-model) makes the same capability-era shift later articulated by Anthropic: GPT-5.6 can better infer a user's underlying goal and intended level of work from the surrounding context, so an agent often does not need every step prescribed. The retained prompt work is the irreducible stuff: domain context, hard constraints, approval boundaries, success criteria, and a clear rule for ambiguities that should trigger a question.

## Durable Claims

- Newer models often work better with outcome-first prompts than with old process-heavy prompt stacks.
- Short personality and collaboration-style instructions can shape how an assistant feels and works, but they should not replace task goals, success criteria, tool rules, or stopping conditions.
- Preambles are useful in tool-heavy workflows because they show the user that the agent has started and what it is doing first.
- Structured output contracts help control verbosity and format.
- Follow-through policies are useful: proceed when the task is clear and low-risk; ask when the action is irreversible, externally consequential, sensitive, or materially ambiguous.
- Tool-use instructions matter most when correctness depends on context gathering, dependency checks, and verification.
- Prompt guidance is empirical. It should be tested against the actual task, tool surface, and failure modes.
- GPT-5.6 guidance recommends simplifying repeated instructions, examples, and tool descriptions while preserving product requirements and any instruction that closes a measured performance gap.
- OpenAI says to state each instruction once, expose only task-relevant tools, keep their descriptions concise and precise, and watch repeated context/tool content as sessions grow.
- Leaner prompts are not a licence for reckless autonomy: GPT-5.6 guidance keeps a compact, explicit policy for safe in-scope local work versus external, destructive, costly, or scope-expanding actions that require confirmation.

## GPT-5.6 Prompt-Engineering Update

OpenAI reports that, in a sample of internal coding-agent evaluations, leaner system prompts improved scores by roughly 10-15% while reducing total tokens by 41-66% and cost by 33-67%. Those are directional internal ranges, not a promise for every task. The recommended method is properly boring: start with a working prompt/tool set, remove one group of instructions, examples, or tools at a time, and rerun the same representative evaluations.

The OpenAI and Anthropic positions now converge on the core rule: write instructions for what the model cannot safely infer, and use the environment to make the rest inspectable. That includes a genuine difference from vague "just trust the model" enthusiasm: approval and autonomy boundaries still have to be named. GPT-5.6's own example distinguishes read-only/review work, requested local implementation and validation, and external/destructive/costly/scope-expanding actions.

For this wiki, the practical pattern remains: `AGENTS.md` holds durable public/private and publication boundaries; task-level requests supply the goal; a relevant skill or local page supplies specialised procedure only when needed; and the agent reads the repo before acting. The complexity belongs in the work, not in a duplicated stack of instruction wallpaper.

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
- [Anthropic Context Engineering For Claude 5 Generation Models](anthropic-context-engineering-claude-5.md)
- [How Should charli-kb Work With Agents?](../questions/how-should-charli-kb-work-with-agents.md)
