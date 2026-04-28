---
name: wiki-lint
description: "Health check a plain Markdown LLM Wiki. Finds broken links, orphan pages, duplicate topics, missing citations, missing frontmatter, stale claims, and public/private boundary risks."
---

# wiki-lint

Run periodically to keep the wiki useful.

Write reports to `wiki/meta/lint-report-YYYY-MM-DD.md`.

## Checks

1. Broken Markdown links.
2. Orphan wiki pages that nothing links to.
3. Duplicate or overlapping pages.
4. Missing required frontmatter: `title`, `type`, `status`, `created`, `updated`.
5. Source-backed claims with no citation or source link.
6. Stale or contradictory claims.
7. `wiki/index.md` entries that point to missing files.
8. Public/private boundary risks, especially references to `raw/private/`.

## Report Template

```md
---
title: "Lint Report YYYY-MM-DD"
type: meta
status: draft
created: YYYY-MM-DD
updated: YYYY-MM-DD
---

# Lint Report: YYYY-MM-DD

## Summary

- Pages scanned:
- Issues found:
- Needs review:

## Broken Links

## Orphan Pages

## Duplicate Or Overlapping Pages

## Missing Frontmatter

## Citation Gaps

## Stale Or Contradictory Claims

## Public/Private Boundary Risks
```

Do not auto-delete or merge pages without user approval.
