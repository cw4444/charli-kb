---
title: "Current State"
type: meta
status: active
created: 2026-04-28
updated: 2026-05-03
---

# Current State

This repo is a plain Markdown personal knowledge base based on Karpathy's LLM Wiki idea. It is meant to be readable by humans and AI agents directly on GitHub.

## Current Workflow

- Notion is Charli's messy capture dump.
- The Notion `Ready to Export` database is the review queue.
- Agents only need to check items marked `Ready`.
- The only queue statuses should be `Ready`, `Draft`, `Ignored`, and `Exported`.
- Items marked `Exported`, `Ignored`, or `Draft` should be skipped unless Charli explicitly asks to revisit them.
- Agents read `Ready` items and decide whether to ingest as `Exported`, leave for human review as `Draft`, or reject as `Ignored`.
- Useful synthesis goes into `wiki/`.
- Raw/private material stays out of git.
- Notion comments and `AI Summary` fields are useful audit trails.
- Local `skills/` are useful but may include cloned-template leftovers; use only the parts relevant to Charli's actual workflow.
- Codex is the gatekeeper for GitHub KB updates. Charli should capture and mark candidates, but agents should create, update, index, log, and push wiki changes.
- Agreed wiki, rule, or handoff updates should be committed and pushed to GitHub after verification unless publication risk is unclear.

## Current Priorities

- Keep the wiki small, useful, and source-aware.
- Prefer synthesis over archiving.
- Do not ingest every interesting thing.
- Warn Charli when a queued item is the same idea already captured elsewhere in the wiki.
- Use discernment: the main lanes are AI and reality, especially where they overlap.
- Separate primary-source claims, commentary, and Charli's own inferences.
- Preserve source metadata and copyright boundaries.
- Keep the repo agent-readable without adopting an Obsidian workflow.
- Keep skills aligned with the Notion-to-wiki loop; ignore editor-specific or inherited workflow debris unless Charli asks for it.
- Keep GitHub as the clean distilled knowledge base, not a second Notion or bulk Markdown export target.
- The durable subject lanes are AI, reality, and their overlap: perception, belief, expectation, action, agents, knowledge systems, reality monitoring, and related source-backed concepts.

## Recent Additions

- Added [How Can Normal Humans Use Codex?](../questions/how-can-normal-humans-use-codex.md), a plain-English guide to Codex for non-developers.
- Added [OpenAI Codex For Everyday Work](../sources/openai-codex-for-everyday-work.md), based on official OpenAI Codex documentation, Help Center pages, and prompt guidance.
- Added examples of small first Codex prompts for non-developers: local trackers, simple galleries, folder inspection, and approval-gated cleanup.
- Created two Codex automation proposals in the app: one daily Notion `Ready to Export` review for `charli-kb`, and one daily official OpenAI Codex docs refresh check for the non-developer guide.

## Things To Know

- Charli values blunt discernment over enthusiastic hoarding.
- It is okay to mark items `Ignored` when they are only personally resonant or already covered by existing wiki pages.
- It is okay to mark items `Draft` when they need missing sources, source clarification, or human judgment.
- Mark items `Exported` only when GitHub received a new page or an update to an existing page.
- Do not add extra statuses; four states are enough.
- When ingesting from Notion, leave a comment explaining what happened and update the row status when possible.
- For `Exported` Notion rows, say whether GitHub received a new page or an update to an existing page.
- Use the external-reader test: would this help an external human reader or future agent, or is it only a private memory?
- Future agents should read `AGENTS.md`, `wiki/index.md`, `wiki/log.md`, and this page before major wiki maintenance.

## Next Useful Steps

- Continue testing the Notion review queue with a mix of articles, videos, screenshots, and personal notes.
- Confirm the scheduled automations behave correctly on their first real runs, especially Notion schema updates and GitHub push behavior.
- Periodically lint the wiki for dead links, duplicate concepts, stale source notes, and public/private boundary issues.
- Consider consolidating overlapping concepts only after several more ingest batches reveal real repetition.
