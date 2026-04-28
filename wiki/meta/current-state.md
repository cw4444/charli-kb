---
title: "Current State"
type: meta
status: active
created: 2026-04-28
updated: 2026-04-28
---

# Current State

This repo is a plain Markdown personal knowledge base based on Karpathy's LLM Wiki idea. It is meant to be readable by humans and AI agents directly on GitHub.

## Current Workflow

- Notion is Charli's messy capture dump.
- The Notion `Ready to Export` database is the review queue.
- Agents read queued items and decide whether to ingest, ignore, or mark draft.
- Useful synthesis goes into `wiki/`.
- Raw/private material stays out of git.
- Notion comments and `AI Summary` fields are useful audit trails.

## Current Priorities

- Keep the wiki small, useful, and source-aware.
- Prefer synthesis over archiving.
- Do not ingest every interesting thing.
- Separate primary-source claims, commentary, and Charli's own inferences.
- Preserve source metadata and copyright boundaries.
- Keep the repo agent-readable without adopting an Obsidian workflow.

## Things To Know

- Charli values blunt discernment over enthusiastic hoarding.
- It is okay to mark items `Ignored` when they are only personally resonant or already covered by existing wiki pages.
- It is okay to mark items `Draft` when they need missing sources, source clarification, or human judgment.
- When ingesting from Notion, leave a comment explaining what happened and update the row status when possible.
- Future agents should read `AGENTS.md`, `wiki/index.md`, `wiki/log.md`, and this page before major wiki maintenance.

## Next Useful Steps

- Continue testing the Notion review queue with a mix of articles, videos, screenshots, and personal notes.
- Periodically lint the wiki for dead links, duplicate concepts, stale source notes, and public/private boundary issues.
- Consider consolidating overlapping concepts only after several more ingest batches reveal real repetition.
