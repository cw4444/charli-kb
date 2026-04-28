---
name: wiki-ingest
description: "Ingest curated sources from raw/ into a plain Markdown LLM Wiki. Creates or updates wiki pages, cross-references them with Markdown links, updates wiki/index.md, and appends to wiki/log.md."
---

# wiki-ingest

Read the source. Write the wiki. Keep the public repo safe.

## Inputs

Sources normally live under `raw/`.

Examples:

- `raw/articles/example.md`
- `raw/notes/exported-note.md`
- `raw/private/example.md` only with explicit permission to use in public wiki pages

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

## Single Source Ingest

1. Read `wiki/index.md` to understand existing pages.
2. Read the source completely.
3. Identify key claims, entities, concepts, decisions, open questions, and contradictions.
4. Create or update a source summary in `wiki/sources/`.
5. Create or update relevant pages in:
   - `wiki/concepts/`
   - `wiki/people/`
   - `wiki/organizations/`
   - `wiki/questions/`
6. Use normal Markdown links between wiki pages.
7. Update `wiki/index.md`.
8. Append a new entry at the top of `wiki/log.md`.

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

## Batch Ingest

For multiple sources:

1. List the files to be processed.
2. Ingest each source.
3. Do one final cross-reference pass.
4. Update `wiki/index.md` and `wiki/log.md` once at the end when practical.

## What Not To Do

- Do not edit files under `raw/`.
- Do not create duplicate pages without checking `wiki/index.md`.
- Do not use Obsidian-only syntax.
- Do not silently overwrite contradictions. Note them clearly on the relevant pages.
