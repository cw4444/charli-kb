---
title: "Computer Work Agent"
type: concept
status: draft
created: 2026-05-21
updated: 2026-06-17
sources:
  - ../sources/openai-codex-for-everyday-work.md
  - ../sources/current-ai-agent-landscape-2026.md
  - ../sources/chatgpt-memory-dreaming-2026.md
---

# Computer Work Agent

A computer work agent is an AI agent that does not stop at writing code. It uses code, files, browser surfaces, desktop apps, APIs, connectors, MCP servers, schedules, memories, and review panes to carry a piece of computer-mediated work from instruction to artifact.

The phrase is useful because much "non-code" work on a computer is already mediated by code-shaped surfaces:

- shell commands;
- web pages;
- APIs;
- spreadsheets;
- documents;
- slide decks;
- messages;
- calendars;
- local files;
- automation triggers;
- GUI apps.

Codex is still centered on code, but OpenAI's 2026 Codex direction shows the boundary moving outward: from code diffs and tests toward end-to-end computer work.

## Core Pattern

A computer work agent combines:

- **durable context:** threads, memories, checked-in docs, and long-running workspaces;
- **tools:** shell, browser, computer use, MCP, connectors, plugins, skills, and APIs;
- **control:** steering, queuing, approvals, goals, and verifiers;
- **review surfaces:** side panels, diffs, browser previews, spreadsheets, PDFs, decks, and artifacts;
- **recurrence:** automations and thread automations that wake up on a schedule.

The work loop becomes:

1. state the outcome;
2. provide or let the agent gather context;
3. let it act across the relevant computer surfaces;
4. inspect the artifact beside the conversation;
5. steer or queue the next step;
6. preserve durable context for the next run.

OpenAI's June 2026 [ChatGPT Memory Dreaming](../sources/chatgpt-memory-dreaming-2026.md) update makes the durable-context part more concrete. A long-running assistant needs more than a large context window inside one conversation. It needs a maintained memory layer that can carry forward relevant facts, follow preferences and constraints, revise stale assumptions, and remain inspectable enough for the user to correct it.

That makes memory a working-systems feature, not just a personalization flourish. It also makes memory quality, privacy, correction, and scope part of the agent's operational boundary.

## Why This Matters

The old framing was:

> Codex helps developers write code.

The broader 2026 framing is:

> Codex helps people get computer work done, with code as one important substrate.

That shift matters for normal users because the useful output may be a report, cleaned spreadsheet, deck, browser app, wiki update, drafted reply, pull request, or scheduled monitoring loop. The user does not need to care whether the agent used HTML, Python, shell commands, a browser, MCP, or a connector, as long as the permissions and result are reviewable.

Charli's 2026-06-15 UK Windows app access to Codex computer use and the Codex Chrome extension is a practical marker for this concept. It also shows why environment matters: a GUI-enabled desktop app agent can operate browser and app surfaces, while WSL/terminal Codex remains strongest as a repo, shell, file, and Git curator. Computer-work agency is not one magic capability; it is the agent plus the surfaces it can actually reach.

## Relation To This Wiki

This wiki is already a computer-work-agent pattern:

- `AGENTS.md` defines rules and public/private boundaries;
- wiki pages hold durable context;
- source notes preserve evidence;
- the timeline tracks fast-moving AI events;
- a daily refresh brief can become a scheduled Codex automation;
- Git commits and pushes make the work auditable.

The human provides taste, judgment, source boundaries, and "what matters." Codex does much of the file work, research, cross-linking, verification, and publication.

## Do Not Overclaim

- Do not say computer work agents can safely operate a whole life unattended.
- Do not confuse reach with judgment.
- Do not treat memory as a replacement for explicit written rules.
- Do not treat synthesized memory as a perfect record of the user or the work.
- Do not automate high-impact actions without approval gates.
- Do not assume a GUI action is safe just because it is not code.

The safe version is bounded, reviewable computer work with explicit permissions and durable context.

## Related Pages

- [OpenAI Codex For Everyday Work](../sources/openai-codex-for-everyday-work.md)
- [ChatGPT Memory Dreaming 2026](../sources/chatgpt-memory-dreaming-2026.md)
- [Codex Goals](codex-goals.md)
- [How Can Normal Humans Use Codex?](../questions/how-can-normal-humans-use-codex.md)
- [Agentic Work Rearchitecture](agentic-work-rearchitecture.md)
- [Agentic Engineering](agentic-engineering.md)
- [Agent Friendly Repositories](agent-friendly-repositories.md)
- [What Can AI Agents Do For Normal Tired Humans?](../questions/what-can-ai-agents-do-for-normal-tired-humans.md)
