---
name: autoresearch
description: "Optional web research loop that finds sources, summarizes them, and files original synthesis into a plain Markdown LLM Wiki."
---

# autoresearch

Use this only when the user asks for agent-led research.

The output is wiki pages, not a long chat transcript.

## Source Rules

- Prefer primary sources, official docs, reputable publications, and permissively accessible material.
- Avoid paywalled or copyrighted text dumps.
- Store only source metadata, citations, and original summaries in `wiki/`.
- If using web sources, include URLs and access dates.

## Workflow

1. Clarify the research topic if needed.
2. Search for a small, high-quality source set.
3. Read and summarize sources in original words.
4. Create source summaries in `wiki/sources/`.
5. Create or update relevant concept, person, organization, and question pages.
6. Create a synthesis page in `wiki/questions/Research - Topic.md`.
7. Update `wiki/index.md`.
8. Append to `wiki/log.md`.

## Synthesis Page Shape

```md
---
title: "Research - Topic"
type: question
status: draft
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources:
  - ../sources/source-page.md
---

# Research - Topic

## Overview

## Key Findings

## Sources

## Open Questions
```

Keep research bounded unless the user asks for a deep dive.
