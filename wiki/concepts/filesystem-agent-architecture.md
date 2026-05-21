---
title: "Filesystem Agent Architecture"
type: concept
status: draft
created: 2026-05-21
updated: 2026-05-21
sources:
  - ../sources/interpretable-context-methodology.md
  - ../sources/openai-codex-for-everyday-work.md
---

# Filesystem Agent Architecture

Filesystem agent architecture is the pattern of using folders and plain files as the control surface for agent work.

The core idea is simple: if an agent can read the right instructions, source files, prior outputs, and verification notes from a predictable folder structure, then the folder structure itself can do part of the orchestration work that might otherwise be hidden inside a framework.

## Why It Matters

This is the sober version of "folders and Markdown are the secret sauce."

Folders are not magic. They help when they make the work:

- visible
- editable
- reviewable
- diffable
- resumable
- portable
- understandable by humans and agents

That matters because many useful agent workflows are sequential rather than fully autonomous. A human asks for research, checks the source note, lets the agent update a concept page, reviews the diff, and then publishes. The workflow succeeds because the intermediate artifacts are readable and correctable.

## Pattern

A filesystem-oriented agent workflow usually has:

- a top-level instruction file such as `AGENTS.md`, `CLAUDE.md`, or `CONTEXT.md`
- stable reference material for conventions, tone, boundaries, and domain context
- working folders for input, output, drafts, reports, or stage artifacts
- scripts for mechanical work that does not need a model
- logs or handoff files that make the latest state explicit
- Git history for review and rollback

In Van Clief and McDermott's Interpretable Context Methodology, numbered folders encode workflow stages and stage-level `CONTEXT.md` files define each stage's inputs, process, and outputs. The broader lesson is not that every repo needs that exact layout. The lesson is that context structure is architecture.

## Fit

This pattern fits workflows that are:

- sequential: one step follows another
- reviewable: a human should inspect intermediate output
- repeatable: the same workflow runs again with different input
- source-sensitive: citations, provenance, or audit trails matter
- small enough that local files and Git are adequate infrastructure

It is especially useful for knowledge-base work, research synthesis, document production, content pipelines, and agent-readable repositories.

## Limits

Filesystem architecture is a bad fit when the system needs:

- real-time multi-agent message passing
- high-concurrency user traffic
- complex automated branching
- robust queueing, retries, and deployment infrastructure
- hidden or access-controlled state that cannot safely sit in plain files

Once the workflow needs those things, a framework, queue, database, or service layer may be the right tool. The point is to avoid adding that machinery before the problem requires it.

## For charli-kb

This repo is already a filesystem agent architecture in miniature:

- `AGENTS.md` defines the public/private boundary and operating rules.
- `wiki/index.md` is the map.
- `wiki/sources/` holds source summaries.
- `wiki/concepts/` and `wiki/questions/` hold reusable synthesis.
- `wiki/log.md` records what changed and why.
- `wiki/meta/current-state.md` gives the next agent a small live handoff.
- `skills/` turns repeated tasks into local workflows.

The useful improvement from ICM is to be more explicit about contracts. When a repeated workflow emerges, define the expected inputs, process, outputs, and verification surface in a skill or meta page instead of relying on memory or chat history.

## Related

- [Interpretable Context Methodology](../sources/interpretable-context-methodology.md)
- [Agentic Engineering](agentic-engineering.md)
- [Agent Friendly Repositories](agent-friendly-repositories.md)
- [Agent Prompting](agent-prompting.md)
- [Queryable Organization](queryable-organization.md)
