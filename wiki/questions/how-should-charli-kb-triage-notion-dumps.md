---
title: "How Should charli-kb Triage Notion Dumps?"
type: question
status: draft
created: 2026-04-28
updated: 2026-05-03
question: "How should charli-kb decide what to ingest from a large Notion dump?"
sources:
  - ../sources/dan-koe-focus-creativity-life-reset-batch.md
---

# How Should charli-kb Triage Notion Dumps?

Notion should remain the capture dump. `charli-kb` should only keep material that earns a place in a durable knowledge base.

For the Notion `Ready to Export` database, the only statuses should be `Ready`, `Draft`, `Ignored`, and `Exported`.

- `Ready`: active intake.
- `Draft`: checked, but needs Charli to review, add a missing source, or decide whether it deserves long-term preservation.
- `Ignored`: checked and rejected for GitHub.
- `Exported`: added to GitHub as a new page or an update to existing content.

Only items marked `Ready` are active ingest candidates. Items marked `Exported`, `Ignored`, or `Draft` should be skipped unless Charli explicitly asks to reopen them.

A Notion item is worth moving into `raw/` when at least one of these is true:

- It supports a current project.
- It answers a question that is still live.
- It contains original notes or synthesis worth preserving.
- It connects multiple ideas that are already recurring.
- It is a primary source or high-quality reference for a topic the wiki is actively building.
- It belongs to one of the wiki's durable lanes: AI, reality, or the overlap between them.
- It would be useful to an external human reader or future agent, not only meaningful as a private memory.

A Notion item should stay in Notion when:

- It was merely interesting in the moment.
- It is motivational but not operational.
- It duplicates ideas already captured.
- It is a full copyrighted article that would be risky to publish.
- No future page or question can be named for it.
- It is merely the same idea in a different wrapper.
- It is a private thought that should stay out of public GitHub.

For large exports, process in small batches. Each batch should produce either concept pages, source summaries, a question answer, or a clear discard note. Do not bulk-import Notion into the wiki.
