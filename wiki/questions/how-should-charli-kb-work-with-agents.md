---
title: "How Should charli-kb Work With Agents?"
type: question
status: draft
created: 2026-04-28
updated: 2026-04-28
question: "How should charli-kb be organized so agents can usefully maintain it?"
sources:
  - ../sources/peter-steinberger-agentic-engineering-batch.md
---

# How Should charli-kb Work With Agents?

`charli-kb` should be treated as an agent friendly repository, not just a notes folder.

The current useful loop is:

1. Human captures messy material in Notion or local `raw/`.
2. Agent reviews candidates and decides whether they deserve synthesis.
3. Agent writes original summaries and concept pages into `wiki/`.
4. Agent updates `wiki/index.md`, `wiki/log.md`, and relevant cross-links.
5. Agent commits the change and leaves an audit note in the source system when possible.

The repo should stay boring. Boring is useful for agents. Clear folders, normal Markdown links, simple frontmatter, and a readable index are worth more than elaborate tooling until there is a repeated pain.

## Current Principle

Do not automate the capture system before the synthesis system proves what it needs. The bottleneck is discernment, not export mechanics.
