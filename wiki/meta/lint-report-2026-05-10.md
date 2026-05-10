---
title: "Lint Report 2026-05-10"
type: meta
status: draft
created: 2026-05-10
updated: 2026-05-10
---

# Lint Report: 2026-05-10

## Summary

- Pages scanned: 66 Markdown files.
- Issues found: 1 template-only missing link, 1 duplicate/overlap cleanup, 1 public/private boundary cleanup.
- Needs review: legacy `raw/private/` path mentions remain in old historical log entries; these are paths only, not source text.

## Broken Links

- No broken content links found.
- The only missing link detected was `relative/path.md` inside `skills/wiki/SKILL.md`, which is a template placeholder.

## Orphan Pages

- No orphan pages found among root and `wiki/` Markdown content after the new package was linked from `wiki/index.md`.

## Duplicate Or Overlapping Pages

- `wiki/concepts/observer-dependent-facts.md` overlapped with the new root-level research package.
- Action taken: consolidated it into a short bridge page pointing to:
  - [Observer-Independent Facts](../../themes/observer-independent-facts.md)
  - [Local Friendliness](../../themes/local-friendliness.md)
  - [Wigner's Friend](../../themes/wigners-friend.md)
  - [Bell Inequalities](../../themes/bell-inequalities.md)

## Missing Frontmatter

- Expected exceptions: `README.md`, `wiki/index.md`, `wiki/log.md`, `wiki/overview.md`, and skill/template files do not consistently use wiki-page frontmatter.
- Generated package pages include frontmatter where appropriate.

## Citation Gaps

- The new research package includes source links and source metadata in `sources/source-index.md`, `sources/sources.csv`, and `sources/sources.json`.
- No immediate citation gaps found in the new theme pages.

## Stale Or Contradictory Claims

- No contradictions found in the new package.
- Proietti et al. is stated conservatively: the experimental violation is separated from the stronger observer-dependent interpretation.

## Public/Private Boundary Risks

- Removed a private Notion URL from `wiki/sources/observer-dependent-facts-wigners-friend.md`.
- Existing historical log entries mention `raw/private/` paths but do not include copied private source text.
