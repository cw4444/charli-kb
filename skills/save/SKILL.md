---
name: save
description: "Save a durable insight, answer, decision, or session summary into the plain Markdown LLM Wiki."
---

# save

Use this when a conversation produces knowledge worth keeping.

## Workflow

1. Identify the durable insight, answer, decision, or summary.
2. Choose the right destination:
   - `wiki/questions/` for answered questions and syntheses
   - `wiki/concepts/` for reusable ideas
   - `wiki/meta/` for decisions or session notes
3. Write the page in declarative present tense.
4. Use normal Markdown links to related wiki pages.
5. Update `wiki/index.md`.
6. Append to `wiki/log.md`.

## Template

```md
---
title: "Note Title"
type: question
status: draft
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: []
---

# Note Title

Saved content.
```

Do not save private or sensitive chat content into a public wiki unless the user explicitly approves it.
