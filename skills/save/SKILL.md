---
name: save
description: "Save a durable insight, answer, decision, or session summary into Charli KB as public-safe Markdown."
---

# save

Use this when a conversation produces knowledge worth keeping.

## Workflow

1. Check whether the material is public-safe.
2. Identify the durable insight, answer, decision, or summary.
2. Choose the right destination:
   - `wiki/questions/` for answered questions and syntheses
   - `wiki/concepts/` for reusable ideas
   - `wiki/meta/` for decisions or session notes
   - `wiki/timelines/` for dated event sequences
3. Write the page in declarative present tense, in original words.
4. Use normal Markdown links to related wiki pages.
5. Update `wiki/index.md`.
6. Append to `wiki/log.md`.
7. Update `wiki/meta/current-state.md` when the saved item changes future routing or context.
8. Commit and push if public-safe and agreed.

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
