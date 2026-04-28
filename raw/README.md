# Raw Sources

Put curated source material here before asking an agent to ingest it.

Guidelines:

- Agents should not edit source files.
- Prefer Markdown, plain text, PDFs, or exported notes.
- `raw/` is ignored by git by default. It is local working input, not the publishable knowledge base.
- Do not force-add copied paywalled, copyrighted, private, sensitive, or personal material.
- The publishable layer is `wiki/`, which should contain original summaries, synthesis, citations, and links.

Suggested local folders:

```text
articles/              Article exports or copied text.
notes/                 Personal exports or working notes.
images/screenshots/    General screenshots for agents to inspect.
images/mindmaps/       Book maps, diagrams, and visual summaries.
images/x-posts/        Screenshots or captures of X/Twitter posts.
```

For images, keep the image file local in `raw/images/`. The wiki should contain attribution, metadata, OCR/transcription only when safe, and original synthesis. Do not rehost screenshots in git unless explicitly approved.
