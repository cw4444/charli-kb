---
name: wiki-query
description: "Answer questions from Charli KB by reading the index, current handoff, and relevant Markdown pages, with clear source boundaries."
---

# wiki-query

Answer from the wiki first. Do not re-derive from raw sources unless the wiki is missing needed evidence or the user asks for fresh research.

## Workflow

1. Read `wiki/index.md`.
2. Read `wiki/meta/current-state.md` when current routing or context matters.
3. Identify the most relevant wiki pages.
4. Read only those pages unless the user asks for a deep synthesis.
5. Answer with Markdown links to supporting pages.
6. Separate wiki-backed facts from inference or speculation.
7. If the wiki lacks enough evidence, say exactly what is missing.
8. If the answer is valuable and public-safe, offer to save it as a page in `wiki/questions/`.

## Query Depth

- Quick: use `wiki/index.md` and maybe one page.
- Standard: read `wiki/index.md`, `wiki/meta/current-state.md`, and 3-5 relevant pages.
- Deep: read all relevant pages and optionally inspect raw sources if needed.

## Filing Answers Back

When saving a durable answer:

```yaml
---
title: "Short Answer Title"
type: question
status: draft
created: YYYY-MM-DD
updated: YYYY-MM-DD
question: "The user's question"
sources:
  - ../concepts/relevant-page.md
---
```

Then update `wiki/index.md` and append to `wiki/log.md`.
