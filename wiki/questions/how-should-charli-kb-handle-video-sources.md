---
title: "How Should charli-kb Handle Video Sources?"
type: question
status: draft
created: 2026-04-28
updated: 2026-04-28
question: "When is a full video transcript needed for charli-kb ingestion?"
sources:
  - ../sources/ai-native-company-and-sidequest-prototyping-batch.md
---

# How Should charli-kb Handle Video Sources?

Full video transcripts are useful when the wiki needs detailed claims, process steps, or source fidelity. They are not always necessary.

Use the smallest source that supports the intended synthesis:

- A title, tweet, or summary is enough for triage.
- A partial transcript is enough for high-level concepts when claims are clearly marked as commentary.
- A full transcript is needed when the wiki will preserve detailed claims, attribute specific quotes, compare arguments, or treat the video as a primary source.

For long videos, avoid dumping the whole transcript into Notion by default. Prefer a source note with:

- video title
- creator or speaker
- URL
- date if known
- topic
- short reason it may matter
- transcript status: none, partial, full, or externally linked

The agent can then decide whether more source detail is worth the cost.
