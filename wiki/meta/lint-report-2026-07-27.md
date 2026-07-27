---
title: "Lint Report 2026-07-27"
type: meta
status: draft
created: 2026-07-27
updated: 2026-07-27
---

# Lint Report: 2026-07-27

## Summary

- Pages scanned: 188 Markdown files under `wiki/`.
- Skills scanned: 3 active local skills.
- Issues fixed: 3 missing frontmatter blocks on legacy root pages.
- Needs review: none from this bounded maintenance pass.

## Broken Links

All local Markdown links resolve.

## Orphan Pages

No new obvious orphan was introduced by the recent source/timeline work. This pass did not attempt a semantic merge of established standalone research pages.

## Duplicate Or Overlapping Pages

No duplicate was created by the recent context-engineering / Open Knowledge Format cluster: ICM remains the workflow method, OpenAI/Anthropic notes cover model-guidance changes, and OKF is the portable knowledge-format proposal.

## Missing Frontmatter

Fixed required frontmatter on:

- [Wiki Index](../index.md)
- [Wiki Log](../log.md)
- [Overview](../overview.md)

All wiki Markdown pages now have `title`, `type`, `status`, `created`, and `updated` frontmatter fields.

## Citation Gaps

No new citation gap found in the pages touched by the recent AI/context-format updates.

## Stale Or Contradictory Claims

No Agricdaniel or Skool reference appears in public repo content, active skills, `AGENTS.md`, or `README.md`.

The dated [Daily AI Timeline Refresh](daily-ai-timeline-refresh.md) brief is still aligned with the current timeline's inclusion rules and agent-readable-knowledge theme. It was not changed merely for having an older creation date.

## Public/Private Boundary Risks

No obvious public reference to `raw/` private material, credentials, client data, or personal journals was found in this bounded pass.

## Template Or Workflow Cruft

Only the intended local skills remain:

- `autoresearch`
- `wiki-ingest`
- `wiki-lint`

No stale template skill, Agricdaniel/Skool material, or editor-specific wrapper was found. No skills were removed because there were none left to remove. Good. The bin is empty; do not buy more bins.
