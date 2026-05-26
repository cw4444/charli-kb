---
name: wiki-ingest
description: "Turn a source, saved item, screenshot, or public-source thread into public-safe Markdown pages for Charli KB, with index, log, handoff, verification, commit, and push."
---

# wiki-ingest

Read the source. Write the wiki. Keep the public repo safe. Do the boring finishing steps.

## First Pass

1. Read `AGENTS.md`, `wiki/index.md`, recent `wiki/log.md`, and `wiki/meta/current-state.md`.
2. Check `git status --short`.
3. Search existing wiki pages for overlap before creating anything.
4. Decide whether the source deserves:
   - a new `wiki/sources/` note,
   - an update to an existing source/concept/theme page,
   - a new concept/question/timeline entry,
   - or no GitHub entry because it is duplicate, private, flimsy, or too low-value.

## Public Safety

- Do not copy long source passages into `wiki/`.
- Summarize in original words.
- Use short quotes only when necessary.
- Do not publish private notes, credentials, client material, personal data, or paywalled/copyrighted material.
- If a source is not safe for public synthesis, say so and stop or ask for direction.

## Source Hierarchy

For science, technology, philosophy, or research topics:

- Prefer primary sources when available: papers, preprints, datasets, code repositories, official docs, and official lab, university, publisher, or company pages.
- Treat journalism, newsletters, podcasts, social posts, and commentary as discovery, explanation, framing, or context.
- Separate primary-source claims from commentary and from Charli's own inferences or speculation.
- Preserve metadata where known: title, author, publication or platform, date, URL, and access notes.
- For paywalled or copyrighted sources, do not reproduce the full text or create a substitute for the original. Write original summaries and link back.
- For X/Twitter posts, preserve URL, author handle, date, and a screenshot or transcription note when the item matters. Do not assume future agents can fetch X reliably.

## Local Raw And Image Sources

Sources may live under `raw/`, including notes, article captures, screenshots, diagrams, mindmaps, or X/Twitter captures.

- Treat `raw/` as non-public working material by default.
- Do not edit `raw/`.
- Do not force-add `raw/` files unless Charli explicitly asks.
- Extract visible text and structure only as needed for synthesis.
- Preserve creator, platform, original URL, date, screenshot filename, and access notes when known.
- Do not rehost images in the public wiki by default.

## Write Pattern

1. Identify key claims, entities, concepts, decisions, open questions, and contradictions.
2. Create or update a source summary in `wiki/sources/`.
3. Create or update relevant pages in `wiki/concepts/`, `wiki/people/`, `wiki/organizations/`, `wiki/questions/`, `wiki/timelines/`, or `themes/`.
4. Use normal Markdown links between pages.
5. Update `wiki/index.md`.
6. Append a new entry at the top of `wiki/log.md`.
7. Update `wiki/meta/current-state.md` when the edit changes routing, priorities, or useful future context.
8. Validate touched links.
9. Commit and push if the update is public-safe and agreed.

## Source Summary Template

```md
---
title: "Source Title"
type: source
status: draft
created: YYYY-MM-DD
updated: YYYY-MM-DD
source_path: ../../raw/articles/example.md
---

# Source Title

## Summary

Brief original summary.

## Key Points

- Point with link to relevant wiki page.

## Useful For

- Topic or question this source supports.
```

## Log Entry Template

```md
## [YYYY-MM-DD] ingest | Source Title
- Source: `raw/articles/example.md`
- Pages created:
- Pages updated:
- Key insight:
```

## What Not To Do

- Do not edit files under `raw/`.
- Do not create duplicate pages without checking `wiki/index.md`.
- Do not use Obsidian-only syntax.
- Do not silently overwrite contradictions. Note them clearly on the relevant pages.
- Do not create a page because a source is momentarily interesting. It has to help the durable AI/reality/wiki-management lanes.
