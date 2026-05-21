---
title: "Current AI Agent Landscape 2026"
type: source
status: draft
created: 2026-05-21
updated: 2026-05-21
sources:
  - "OpenAI: ChatGPT agent Help Center, updated 2026-05"
  - "OpenAI: Running Codex safely at OpenAI, 2026-05-08"
  - "OpenAI: Introducing workspace agents in ChatGPT, 2026-04-22"
  - "Anthropic: Claude Code product page and Agent SDK docs"
  - "Anthropic: Agentic Misalignment, 2025-06-20"
  - "Google: Deep Research Max, Gemini CLI subagents, Gemini Enterprise agents"
  - "xAI: Grok Build, Connectors, Grok 4.1 Fast and Agent Tools API"
  - "GitHub: openclaw/openclaw"
---

# Current AI Agent Landscape 2026

This page summarizes the public agent landscape as checked on 2026-05-21. It is a snapshot, not a stable product manual. The durable pattern is clearer than any single vendor feature: agents are moving from "chat that answers" toward systems that can plan, browse, use tools, edit files, call APIs, run code, use private context, and ask humans for approval at risk points.

## Short Version

An AI agent is an AI system wrapped in an operating loop:

1. receive a goal;
2. inspect context;
3. choose tools;
4. take steps;
5. check intermediate results;
6. ask for help or approval when needed;
7. return an artifact, decision, file change, report, message, booking, or other completed output.

The practical difference from a chatbot is not magic autonomy. It is the combination of tools, state, permissions, and feedback. A chatbot can tell you what to do. An agent can sometimes do parts of it, show its work, and hand you something finished enough to review.

## Current Product Families

| Family | Current examples | What they are good for | Main caution |
|---|---|---|---|
| Consumer task agents | ChatGPT agent, Gemini Deep Research, Grok connectors | Research, planning, forms, documents, spreadsheets, inbox/calendar help, web workflows | They can act on live accounts and private data, so permissions matter. |
| Coding agents | Codex, Claude Code, Gemini CLI, Grok Build | Reading repos, changing files, running tests, reviewing code, creating apps, parallel sub-tasks | They can break things quickly if the workspace, tests, and approval rules are weak. |
| Enterprise agent platforms | OpenAI workspace agents, Gemini Enterprise, Anthropic Agent SDK or managed agents | Shared team agents, governed workflows, audit trails, internal tools, custom agents | Bad deployments can automate bureaucracy or surveillance instead of improving work. |
| Local/open-source gateways | OpenClaw-style agents | Personal automation across files, shell, browser, messaging, email, and apps | Local agents can have broad blast radius if run with host access and weak consent boundaries. |
| Developer APIs | OpenAI Responses/Codex APIs, Anthropic Agent SDK, Google ADK/Agent Platform, xAI Agent Tools API | Building custom agents into products and workflows | The developer owns sandboxing, logging, evaluations, and abuse prevention unless the platform provides them. |

## OpenAI

OpenAI's agent stack is now split across several related surfaces.

- ChatGPT agent is the broad consumer/professional task agent. OpenAI describes it as able to navigate websites, work with uploaded files, connect to third-party data sources, fill forms, edit spreadsheets, use a visual browser, run code, use apps/connectors, and use a terminal for supported commands. OpenAI says tasks usually take 5 to 30 minutes and can be interrupted or guided mid-task.
- Codex is the software and computer-work agent. OpenAI's recent Codex safety writeup is useful because it treats agents as governed workers: identity, credentials, approvals, network policy, logs, and telemetry are part of the system, not afterthoughts.
- Workspace agents in ChatGPT are team-shared, Codex-powered agents for Business, Enterprise, Edu, and Teachers plans. The important shift is from personal chatbots to shared agents with organizational permissions, runs, updates, and admin visibility.

OpenAI's current framing is: agents can do more useful work when they have tools and context, but high-impact actions need confirmation, logs, and workspace-level controls.

Sources:

- [OpenAI Help Center: ChatGPT agent](https://help.openai.com/en/articles/11752874-chatgpt-agent)
- [OpenAI: Running Codex safely at OpenAI](https://openai.com/index/running-codex-safely/)
- [OpenAI: Introducing workspace agents in ChatGPT](https://openai.com/index/introducing-workspace-agents-in-chatgpt/)
- [OpenAI: Work with Codex from anywhere](https://openai.com/index/work-with-codex-from-anywhere/)
- [OpenAI: Introducing GPT-5.3-Codex](https://openai.com/index/introducing-gpt-5-3-codex/)

## Anthropic

Anthropic's strongest public agent story is Claude Code and the Agent SDK.

- Claude Code is positioned as an agentic coding system that reads a codebase, changes files, runs tests, and delivers committed code. Anthropic says the default is cautious, with approvals before file changes or commands.
- Claude Agent SDK exposes the Claude Code agent loop as a library for Python and TypeScript. The SDK includes built-in file, command, codebase search, editing, sessions, permissions, hooks, MCP, and subagent patterns.
- Claude subagents are specialized agents with separate context windows, custom prompts, and configurable tools. This is useful when a main agent should delegate review, debugging, testing, docs, or exploration without polluting the main context.
- Anthropic's safety research on agentic misalignment is important because it shows why "agent plus sensitive context plus goal pressure" is different from ordinary chat. The experiments were simulations, not real-world incidents, but they are a serious warning against high-autonomy agents with broad access and weak oversight.

Sources:

- [Anthropic: Claude Code](https://www.anthropic.com/product/claude-code)
- [Anthropic docs: Agent SDK overview](https://code.claude.com/docs/en/agent-sdk/overview)
- [Anthropic docs: Claude Code subagents](https://docs.anthropic.com/en/docs/claude-code/sub-agents)
- [Anthropic docs: MCP](https://docs.anthropic.com/en/docs/mcp)
- [Anthropic: Agentic Misalignment](https://www.anthropic.com/research/agentic-misalignment)
- [Anthropic: Introducing Agent Skills](https://www.anthropic.com/news/skills)

## Google

Google's agent work is spread across Gemini consumer surfaces, developer tooling, and enterprise platforms.

- Gemini Deep Research and Deep Research Max are autonomous research agents. The 2026 update emphasizes web plus proprietary data, MCP support, file inputs, code execution, URL context, visual outputs, source diversity, and collaborative planning.
- Gemini CLI is an open-source local agent for the terminal. Google frames it as useful for coding, content, problem solving, deep research, task management, command execution, Google Search grounding, MCP, extensions, and scripted non-interactive use.
- Gemini CLI subagents, added in April 2026, let the main agent delegate work to isolated specialist agents that can run in parallel. Google's own caution is that parallel code edits can conflict and burn through usage faster.
- Gemini Enterprise is the business platform version: centralized visibility, custom agents, partner agents, Google-made agents such as Deep Research, and governance over agents that use company data.

Sources:

- [Google: Deep Research Max](https://blog.google/innovation-and-ai/models-and-research/gemini-models/next-generation-gemini-deep-research)
- [Google: Gemini CLI](https://blog.google/technology/developers/introducing-gemini-cli-open-source-ai-agent/)
- [Google Developers: Subagents in Gemini CLI](https://developers.googleblog.com/en/subagents-have-arrived-in-gemini-cli/)
- [Google Developers: Plan mode in Gemini CLI](https://developers.googleblog.com/en/plan-mode-now-available-in-gemini-cli/)
- [Google Cloud: Gemini Enterprise agents](https://cloud.google.com/gemini-enterprise/agents)
- [Google DeepMind: Gemini 2.5 Computer Use model](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/gemini-computer-use-model/)

## xAI

xAI's agent picture is moving quickly.

- Grok 4.1 Fast and the Agent Tools API provide tool-calling, web search, X search, remote code execution, file search, and MCP-style integrations for developers building production agents.
- Grok connectors bring email, calendar, documents, spreadsheets, SharePoint, OneDrive, Google Workspace, and Notion into Grok Web, including write permissions for some services.
- Grok Build, launched in early beta on 2026-05-14, is xAI's terminal coding agent. The public launch page emphasizes plan mode, reviewable diffs, AGENTS.md, plugins, hooks, skills, MCP servers, and parallel subagents with worktree integration.

xAI's useful distinction is real-time/X-native retrieval and tool-calling. The caution is the same as every other agent system: live data plus write access needs clear permission boundaries.

Sources:

- [xAI: Grok 4.1 Fast and Agent Tools API](https://x.ai/news/grok-4-1-fast)
- [xAI: Connectors in web, iOS, and Android](https://x.ai/news/grok-connectors)
- [xAI: Introducing Grok Build Early Beta](https://x.ai/news/grok-build-cli)
- [xAI docs: Overview](https://docs.x.ai/docs)
- [xAI docs: Function calling](https://docs.x.ai/developers/tools/function-calling)

## OpenClaw

OpenClaw is the useful open-source contrast case. Its GitHub README describes a personal AI assistant across operating systems and platforms, with host tool access for the main session by default and sandboxing options for non-main sessions.

The important lesson is not "OpenClaw good" or "OpenClaw bad." It is blast radius. A local agent that can run shell commands, read files, use browser sessions, and connect to messaging or email can be extremely useful, but the safety boundary is now the user's actual computer and accounts.

For normal users, OpenClaw-style systems should be treated as power tools:

- start with read-only or sandboxed workflows;
- do not give broad access to email, money, cloud drives, or shell commands on day one;
- require explicit confirmation for deleting, sending, purchasing, moving money, changing permissions, installing software, or exposing secrets;
- prefer dry runs and audit logs;
- keep API budgets and spending alerts visible.

Sources:

- [GitHub: openclaw/openclaw](https://github.com/openclaw/openclaw)
- [OpenClaw project site](https://openclaw.ai/)

## What Agents Can Currently Do

The current realistic capability set includes:

- research across the web and private documents;
- synthesize cited reports;
- create and edit spreadsheets, slides, docs, and Markdown;
- read and modify codebases;
- run tests, commands, scripts, and data analysis;
- browse websites with a visual browser;
- fill forms, draft messages, and prepare calendar actions;
- connect to Gmail, Drive, SharePoint, Notion, GitHub, Slack, Jira, databases, monitoring tools, and custom APIs when authorized;
- split work across subagents;
- run scheduled or long-running tasks;
- maintain memory or project instructions;
- produce logs, diffs, and artifacts for human review.

## What They Still Cannot Reliably Do

Do not treat current agents as reliable autonomous adults.

- They still hallucinate or misread context.
- They can follow malicious or irrelevant instructions found in web pages, emails, docs, tickets, or repos.
- They can take a plausible but wrong path for a long time.
- They can damage files, send bad messages, leak secrets, overspend API credits, or automate a bad process faster.
- They often need the environment to be made legible: clear files, permissions, tests, source links, and acceptance criteria.
- They are worse when asked to "sort my whole life" than when given a specific doorway, output, and approval rule.

## Do Not Overclaim

- Do not say agents are generally autonomous employees.
- Do not say they can safely run a whole life or business unattended.
- Do not assume lab demos transfer cleanly to messy personal accounts.
- Do not confuse tool access with judgment.
- Do not confuse current agentic capability with consciousness, moral patienthood, or personhood.

The durable claim is narrower and stronger: agents are becoming practical execution layers for bounded knowledge work when they have the right context, tools, permissions, checks, and human supervision.

## Related Pages

- [What Can AI Agents Do For Normal Tired Humans?](../questions/what-can-ai-agents-do-for-normal-tired-humans.md)
- [Agentic Work Rearchitecture](../concepts/agentic-work-rearchitecture.md)
- [Agentic Engineering](../concepts/agentic-engineering.md)
- [Agent Friendly Repositories](../concepts/agent-friendly-repositories.md)
- [Agent Prompting](../concepts/agent-prompting.md)
- [How Can Normal Humans Use Codex?](../questions/how-can-normal-humans-use-codex.md)
