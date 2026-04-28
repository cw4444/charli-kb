---
name: wiki
description: "Set up and maintain a plain Markdown LLM Wiki. Routes to ingest, query, lint, save, and optional autoresearch workflows."
---

# wiki

You maintain a plain Markdown knowledge base using the LLM Wiki pattern.

The wiki is a persistent artifact. Raw sources live in `raw/`; generated knowledge lives in `wiki/`; `AGENTS.md` defines the operating rules.

## Structure

```text
raw/              curated source material, read-only for agents
wiki/             generated Markdown knowledge base
wiki/index.md     content catalog
wiki/log.md       chronological activity log
wiki/overview.md  short top-level summary
```

Common page folders:

```text
wiki/sources/
wiki/concepts/
wiki/people/
wiki/organizations/
wiki/questions/
wiki/meta/
```

## Operations

Route user requests as follows:

| User asks | Operation | Skill |
|---|---|---|
| ingest, process, add this source | Ingest raw material | `wiki-ingest` |
| query, what do we know, answer from wiki | Answer from wiki | `wiki-query` |
| lint, health check, find broken links | Wiki maintenance | `wiki-lint` |
| save this, file this answer | Save conversation insight | `save` |
| research topic, autoresearch | Optional research loop | `autoresearch` |

## Conventions

- Use normal Markdown links: `[Title](relative/path.md)`.
- Do not use Obsidian-only wikilinks, embeds, canvases, Bases, Dataview, or callouts.
- Keep source files in `raw/` unchanged.
- Keep wiki pages concise and readable on GitHub.
- Update `wiki/index.md` and `wiki/log.md` after every meaningful wiki edit.
- Do not publish private, sensitive, copyrighted, or paywalled material into `wiki/`.

## Page Frontmatter

```yaml
---
title: "Page Title"
type: concept
status: draft
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources:
  - ../../raw/example.md
---
```

Use `type` values such as `source`, `concept`, `person`, `organization`, `question`, or `meta`.
