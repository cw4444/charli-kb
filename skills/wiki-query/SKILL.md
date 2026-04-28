---
name: wiki-query
description: "Answer questions from a plain Markdown LLM Wiki. Reads wiki/index.md first, then relevant pages, and cites supporting wiki pages with Markdown links."
---

# wiki-query

Answer from the wiki first. Do not re-derive from raw sources unless the wiki is missing needed evidence.

## Workflow

1. Read `wiki/index.md`.
2. Identify the most relevant wiki pages.
3. Read only those pages unless the user asks for a deep synthesis.
4. Answer with Markdown links to supporting pages.
5. If the wiki lacks enough evidence, say exactly what is missing.
6. If the answer is valuable, offer to save it as a page in `wiki/questions/`.

## Query Depth

- Quick: use `wiki/index.md` and maybe one page.
- Standard: read `wiki/index.md` plus 3-5 relevant pages.
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
