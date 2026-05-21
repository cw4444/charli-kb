---
title: "AI And Agents 2026 Timeline"
type: timeline
status: draft
created: 2026-05-21
updated: 2026-05-21
sources:
  - ../sources/current-ai-agent-landscape-2026.md
  - ../sources/anthropic-compute-and-talent-signal-2026.md
  - ../../themes/ai-consciousness/character-formation-and-persona-safety.md
  - https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
  - https://openai.com/index/retiring-gpt-4o-and-older-models/
  - https://help.openai.com/en/articles/20001051
  - https://github.com/openclaw/openclaw
  - https://github.com/torvalds/linux
---

# AI And Agents 2026 Timeline

This is a lightweight historical timeline for the AI/agent acceleration of 2026. It is not meant to preserve every product update. It exists because 2026 is moving fast enough that individual source notes can become hard to place in sequence.

Use this page for events that are useful historical anchors:

- model retirements that changed user behavior or culture;
- agent tools becoming mainstream;
- major lab infrastructure/talent moves;
- source drops that shaped this wiki's structure;
- safety/model-welfare/character-formation milestones;
- public adoption signals that were big enough to affect the discourse.

Future lint rule: update this page if it helps preserve the shape of the year. Delete or collapse entries that turn out to be noise.

## Short Read As Of 2026-05-21

The first five months of 2026 already show several converging threads:

- AI agents moved from demos into everyday developer and workplace tools.
- OpenAI and Anthropic kept shipping Codex/Claude Code-style agent updates.
- Google pushed Gemini CLI, subagents, Deep Research, computer-use, and enterprise agents.
- OpenClaw became a viral open-source local-agent gateway, reportedly passing Linux in GitHub stars in February and showing 250k+ stars by May.
- Karpathy's LLM Wiki pattern gave this repo a direct structural ancestor.
- Karpathy then joined Anthropic's pre-training team.
- Anthropic paired its constitution/model-welfare/character-formation lane with major compute access from SpaceX/Colossus.
- GPT-4o, a model many users were emotionally attached to, was retired from ChatGPT on 2026-02-13.

The durable theme is not one company winning. It is that agents, model character, compute, public attachment, and knowledge-work rearchitecture all became visible at the same time.

## Timeline

### 2026-01-22 - Anthropic publishes Claude's new constitution

Anthropic published a fuller constitution for Claude and later described the full constitution as written with Claude as the primary audience. In this wiki, that belongs to the [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md) lane: model-facing values, role self-description, and positive character formation as safety surfaces.

Why it matters: Anthropic is not only saying "do not do bad things." It is shaping a named assistant's role, self-understanding, and behavior through explicit principles.

Source:

- [Anthropic: Claude's constitution](https://www.anthropic.com/constitution)

### 2026-02-13 - GPT-4o retired from ChatGPT

OpenAI retired GPT-4o, GPT-4.1, GPT-4.1 mini, OpenAI o4-mini, and previously announced GPT-5 variants from ChatGPT on 2026-02-13. OpenAI's January 29 announcement singled out GPT-4o for special context: users had preferred its conversational style and warmth, OpenAI had previously restored access after feedback, and later personality work in GPT-5.1/GPT-5.2 was shaped by that feedback.

Why it matters: GPT-4o's retirement is part of the model-character/user-attachment story. It showed that users do not experience model replacement as a pure capability upgrade. Style, warmth, continuity, and trust matter.

Sources:

- [OpenAI: Retiring GPT-4o and older models](https://openai.com/index/retiring-gpt-4o-and-older-models/)
- [OpenAI Help Center: Retiring GPT-4o and other ChatGPT models](https://help.openai.com/en/articles/20001051)

### 2026-02 - OpenClaw passes Linux in GitHub-star discourse

OpenClaw's public rise became a major agentic-engineering signal. OpenClaw.report reported that OpenClaw passed the Linux kernel in GitHub stars around February 2026, with a cited snapshot of roughly 218,261 stars for OpenClaw versus 218,260 for Linux. As checked on 2026-05-21, GitHub showed Linux at about 234k stars, while OpenClaw's repository and surrounding reporting showed OpenClaw in the 250k+ range.

Why it matters: GitHub stars are not importance, quality, or infrastructure value. Linux is still Linux. The signal is attention velocity: a local-agent framework becoming one of the most visible open-source projects in months.

Sources:

- [GitHub: openclaw/openclaw](https://github.com/openclaw/openclaw)
- [GitHub: torvalds/linux](https://github.com/torvalds/linux)
- [OpenClaw.report: OpenClaw Just Passed Linux on GitHub](https://openclaw.report/community/openclaw-passes-linux-github-what-it-means)

### 2026-04-04 - Karpathy publishes the LLM Wiki pattern

Andrej Karpathy published the `llm-wiki.md` gist on 2026-04-04. The pattern is simple: maintain a plain Markdown wiki that humans curate and agents can read, update, and query directly. This repo is built in that spirit.

Why it matters: this is one of the cleanest practical patterns for agent-readable knowledge. It avoids overbuilding a second brain and instead makes the knowledge base legible to both humans and agents.

Source:

- [Karpathy gist: llm-wiki.md](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)

### 2026-04-22 - OpenAI introduces workspace agents in ChatGPT

OpenAI introduced workspace agents in ChatGPT for Business, Enterprise, Edu, and Teachers plans. The important shift is from single-user chat to shared, Codex-powered agents with organizational context, runs, updates, permissions, and admin visibility.

Why it matters: agents are becoming workplace infrastructure, not just personal assistants.

Source:

- [OpenAI: Introducing workspace agents in ChatGPT](https://openai.com/index/introducing-workspace-agents-in-chatgpt/)

### 2026-04 to 2026-05 - Google pushes Gemini agents and subagents

Google's 2026 agent push includes Gemini CLI, Gemini CLI subagents, plan mode, Gemini Deep Research Max, Gemini Enterprise agents, and a Gemini 2.5 Computer Use model.

Why it matters: Google is pushing the same broad pattern as OpenAI and Anthropic: agentic research, terminal agents, subagents, enterprise agents, computer use, and governed access to proprietary context.

Sources:

- [Google: Gemini CLI](https://blog.google/technology/developers/introducing-gemini-cli-open-source-ai-agent/)
- [Google Developers: Subagents in Gemini CLI](https://developers.googleblog.com/en/subagents-have-arrived-in-gemini-cli/)
- [Google: Deep Research Max](https://blog.google/innovation-and-ai/models-and-research/gemini-models/next-generation-gemini-deep-research)
- [Google Cloud: Gemini Enterprise agents](https://cloud.google.com/gemini-enterprise/agents)
- [Google DeepMind: Gemini 2.5 Computer Use model](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/gemini-computer-use-model/)

### 2026-05-06 - Anthropic takes SpaceX/Colossus compute capacity

Axios and Data Center Dynamics reported that Anthropic would use compute capacity from SpaceX/xAI's Colossus 1 data center in Memphis. Axios later reported the deal at $1.25 billion per month, or $15 billion per year, through May 2029, with a 90-day exit option.

Why it matters: Anthropic's careful model-welfare/constitution public posture is now paired with extremely serious frontier compute pressure.

Source:

- [Anthropic Compute And Talent Signal 2026](../sources/anthropic-compute-and-talent-signal-2026.md)

### 2026-05-08 - Anthropic publishes "Teaching Claude why"

Anthropic published "Teaching Claude why," reporting that principled explanations, constitutional material, difficult ethical-advice data, and positive fictional stories about admirable AI behavior reduced agentic misalignment more robustly than action-only demonstrations.

Why it matters: this is one of the clearest examples of model character as a safety surface. The adorable version is "Anthropic gave Claude better stories about good AI." The careful version is: narrative, role, and constitutional self-description appear to affect model behavior under pressure.

Sources:

- [Anthropic: Teaching Claude why](https://www.anthropic.com/research/teaching-claude-why)
- [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md)

### 2026-05-14 - OpenAI expands Codex access and mobile/remote work

OpenAI announced "Work with Codex from anywhere," part of a fast-moving Codex product line that includes cloud tasks, code review, automation, local/CLI workflows, and workspace agents.

Why it matters: coding agents are becoming less like occasional developer helpers and more like persistent work agents that can run, report, and be managed across contexts.

Source:

- [OpenAI: Work with Codex from anywhere](https://openai.com/index/work-with-codex-from-anywhere/)

### 2026-05-14 - xAI launches Grok Build early beta

xAI launched Grok Build early beta as a terminal coding agent with plan mode, diffs, AGENTS.md, plugins, hooks, skills, MCP servers, and parallel subagents.

Why it matters: by May 2026, the coding-agent pattern is no longer an OpenAI/Anthropic-only story. Multiple labs are converging on terminals, repo instructions, tools, subagents, and reviewable diffs.

Source:

- [xAI: Introducing Grok Build Early Beta](https://x.ai/news/grok-build-cli)

### 2026-05-19 - Karpathy joins Anthropic

Karpathy joined Anthropic's pre-training team in May 2026, according to TechCrunch, Forbes, and Axios reporting.

Why it matters: coming after the LLM Wiki gist and during the agent/coding-tool acceleration, this is a meaningful talent signal. It also links a practical agent-readable-knowledge pattern to the lab currently most publicly focused on model character and welfare uncertainty.

Source:

- [Anthropic Compute And Talent Signal 2026](../sources/anthropic-compute-and-talent-signal-2026.md)

## Watchlist

Future agents should consider adding entries when these threads produce durable changes:

- Claude Code, Codex, Gemini CLI, Grok Build, or OpenClaw major release shifts;
- model retirements or continuity policies that affect user attachment;
- official model-welfare or post-deployment interview updates;
- major compute, data-center, or talent moves;
- agent-safety incidents involving local tools, email, money, secrets, or public posting;
- public guidance around sandboxing, MCP, browser/computer use, and explicit consent;
- this wiki's own workflow changes if the Karpathy LLM Wiki pattern evolves.

## Do Not Overclaim

- Do not treat GitHub stars as importance.
- Do not treat every product update as historically meaningful.
- Do not assume Anthropic's welfare framing proves Claude is conscious.
- Do not assume OpenAI, Anthropic, Google, xAI, and OpenClaw are building the same thing just because they all use agent language.
- Do not preserve this page as canon if it becomes stale noise. Timeline pages are allowed to be rewritten or deleted.

## Related Pages

- [Current AI Agent Landscape 2026](../sources/current-ai-agent-landscape-2026.md)
- [Anthropic Compute And Talent Signal 2026](../sources/anthropic-compute-and-talent-signal-2026.md)
- [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md)
- [What Can AI Agents Do For Normal Tired Humans?](../questions/what-can-ai-agents-do-for-normal-tired-humans.md)
- [Agentic Work Rearchitecture](../concepts/agentic-work-rearchitecture.md)
