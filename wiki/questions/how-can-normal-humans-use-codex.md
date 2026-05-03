---
title: "How Can Normal Humans Use Codex?"
type: question
status: draft
created: 2026-05-03
updated: 2026-05-03
question: "How can non-developers use Codex for everyday work?"
sources:
  - ../sources/openai-codex-for-everyday-work.md
---

# How Can Normal Humans Use Codex?

Codex is officially described as an AI agent for code, but the useful non-developer translation is simpler: Codex is a work agent that can read a workspace, follow instructions, use tools, change files, verify outputs, and come back on a schedule.

That makes it useful for people who do not want to "code" but do want help maintaining a knowledge base, cleaning spreadsheets, generating reports, preparing documents, checking an intake queue, or connecting apps.

## What Codex Is For

Use Codex when the task has a place to happen and a definition of done.

Good examples:

- "Check my Notion intake queue once a day and update my Markdown wiki if anything earns it."
- "Clean this spreadsheet and produce a short report."
- "Turn these rough notes into a structured document."
- "Read this folder of source material and make a summary with citations."
- "Build a simple website or dashboard from this brief."
- "Check what changed in this project this week and summarize it."

Poor examples:

- "Be generally smarter for me."
- "Organize my whole life."
- "Remember everything forever."
- "Do something useful with all my notes."

Codex works best when the task names the input, the rules, the output, and how to tell whether it succeeded.

## The Basic Pieces

### `AGENTS.md`

`AGENTS.md` is the instruction sheet for a project. Codex reads it before working.

Use it for rules that should always apply:

- what the project is for
- what files are public or private
- what counts as done
- what must never be copied, deleted, or published
- how logs, indexes, or handoff notes should be updated

For `charli-kb`, `AGENTS.md` tells Codex that Notion is the messy capture dump, GitHub is the clean wiki, and only `Ready` items should be processed.

### Skills

Skills are reusable workflows. A skill is like a small instruction pack Codex can load when a task matches it.

Use a skill when you repeat a job:

- ingesting sources into a wiki
- making slide decks
- analyzing spreadsheets
- checking a frontend in a browser
- following a house style for documents

You do not need to write one first. A normal prompt can be: "Codex, make me a skill for how we process Notion items into this wiki."

### Plugins

Plugins are installable bundles that can add skills, app connections, and MCP servers.

Use plugins when Codex needs a real service:

- Gmail for inbox triage
- Slack for channel summaries
- Google Drive for Docs, Sheets, and Slides
- Notion for databases and pages
- GitHub for repositories, issues, and pull requests

For normal humans, the main rule is: install a plugin when Codex needs access to an app you already use.

### MCP

MCP means Model Context Protocol. In human terms, it is a way to give Codex extra tools and context.

Use MCP when Codex needs to talk to a specific system or tool that is not already built in. Examples include developer documentation, Figma designs, browser automation, Sentry logs, GitHub, or a custom internal tool.

You do not need to understand the protocol to benefit from it. The practical prompt is:

> "Codex, can you build or configure an MCP server for this tool, then explain how I use it?"

### Automations

Automations are scheduled Codex runs. They are useful for recurring chores.

Use automations for:

- daily Notion intake checks
- weekly repo summaries
- recurring report generation
- bug triage
- "tell me if anything needs my attention"

For project-scoped automations, the Codex app needs access to the project on disk. In a Git repo, automations can run in the local project or in a separate worktree. Worktrees are safer when the automation may change files because they keep background changes away from unfinished work.

### Memories

Memories are optional local context Codex can carry across threads. They are useful for stable preferences and recurring workflows.

Do not use memories as the only place for important rules. Put rules that must always apply in `AGENTS.md` or checked-in documentation.

## The Useful Mental Model

ChatGPT is good for conversation, exploration, brainstorming, and working through ideas.

Codex is good when the idea needs to touch files, tools, apps, or a schedule.

The handoff looks like this:

1. Talk through the idea in ChatGPT or Codex.
2. Decide what repeatable work should happen.
3. Put durable rules in `AGENTS.md`.
4. Connect needed apps with plugins or MCP.
5. Use skills for repeatable workflows.
6. Use automations for scheduled work.
7. Let Codex report what it changed.

## Example: A Phone-To-Wiki Bridge

Charli's workflow:

- Capture interesting pages, URLs, and notes in Notion from a phone.
- Mark only serious candidates as `Ready`.
- Codex checks the `Ready to Export` database on a schedule.
- Codex ignores `Draft`, `Ignored`, and `Exported`.
- Codex decides whether the item is useful to an external human reader or future agent.
- If it earns GitHub, Codex creates or updates concise Markdown wiki pages.
- Codex updates the wiki index and log.
- Codex comments in Notion and marks the row `Exported`, `Ignored`, or `Draft`.

This is a better use of Codex than bulk-exporting Notion into GitHub. The value is judgment, synthesis, and audit trail, not hoarding.

## What To Ask Codex

Good starter prompts:

- "Read this folder and tell me what should become a durable wiki page."
- "Make an `AGENTS.md` for this project so future Codex runs know the rules."
- "Create a repeatable skill for this workflow."
- "Set up a daily automation that checks this database and reports anything needing action."
- "Tell me whether this needs a plugin, MCP server, automation, or just a one-off prompt."
- "Build the smallest working version, then explain how I use it."

## What Not To Do

Do not ask Codex to become a vague second brain. Give it a doorway, a rule, and an output.

Do not publish private notes just because Codex can read them.

Do not automate deletion until a review workflow has proved itself.

Do not add integrations for sport. Add them when a real recurring task needs them.

## Sources

- [OpenAI Help Center: Using Codex with your ChatGPT plan](https://help.openai.com/en/articles/11369540-codex-in-chatgpt)
- [OpenAI Codex use cases](https://developers.openai.com/codex/use-cases)
- [OpenAI Codex app features](https://developers.openai.com/codex/app/features)
- [OpenAI Codex automations](https://developers.openai.com/codex/app/automations)
- [OpenAI AGENTS.md guidance](https://developers.openai.com/codex/guides/agents-md)
- [OpenAI Codex skills](https://developers.openai.com/codex/skills)
- [OpenAI Codex plugins](https://developers.openai.com/codex/plugins)
- [OpenAI Codex MCP](https://developers.openai.com/codex/mcp)
- [OpenAI Codex memories](https://developers.openai.com/codex/memories)
- [OpenAI Codex workflows](https://developers.openai.com/codex/workflows)
