---
name: defuddle
description: "Optional helper for cleaning article-style web pages into readable Markdown before placing them in raw/."
---

# defuddle

Defuddle can strip navigation, ads, and boilerplate from article-style web pages before ingestion.

Install if wanted:

```bash
npm install -g defuddle-cli
```

Usage:

```bash
defuddle https://example.com/article
```

Save cleaned output into `raw/articles/` only when it is appropriate to keep that content in the repository. For public repos, prefer saving brief notes, metadata, and citations rather than copied article bodies.
