---
name: wiki-lint
description: "Health check Charli KB. Finds broken links, stale navigation, duplicate pages, missing frontmatter, citation gaps, and public/private boundary risks."
---

# wiki-lint

Run periodically to keep the wiki useful.

Write reports to `wiki/meta/lint-report-YYYY-MM-DD.md`.

## Checks

1. Broken Markdown links in public pages.
2. `wiki/index.md` entries that point to missing files.
3. Orphan wiki pages that nothing links to.
4. Duplicate or overlapping pages.
5. Missing required frontmatter: `title`, `type`, `status`, `created`, `updated`.
6. Source-backed claims with no citation or source link.
7. Stale or contradictory claims, especially timelines and fast AI/product/company claims.
8. Public/private boundary risks, especially accidental publication of raw, private, client, personal, credential, or paywalled material.
9. Obsidian-only syntax or cloned-template cruft.
10. Cold-start walk test for material workflow/structure changes: can a new agent find the route, exact inputs, permitted actions, verification step, and expected output within the root instructions, index/area page, and at most one specialised page?

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

## Template Or Workflow Cruft

## Cold-Start Walk Test
```

Fix small obvious issues when the user asked for cleanup. Do not merge or delete substantive wiki pages without clear approval.
