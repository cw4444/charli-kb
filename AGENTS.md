# LLM Wiki Agent Instructions

This repository is a plain Markdown knowledge base based on Andrej Karpathy's LLM Wiki pattern.

The goal is simple: humans curate raw material, agents turn it into a clean, linked wiki, and both humans and agents can read the result directly on GitHub.

## Repository Structure

```text
raw/              Curated source material. Agents do not edit source files.
wiki/             Agent-maintained Markdown knowledge base.
wiki/index.md     Content-oriented catalog of wiki pages.
wiki/log.md       Append-only chronological activity log.
skills/           Optional Agent Skills for ingest, query, lint, save, and research.
```

## Public Repo Rules

- Do not copy copyrighted, paywalled, private, or sensitive source text into `wiki/`.
- Summarize in original words and cite the source location.
- Short quotes are allowed only when necessary and should stay minimal.
- Treat `raw/private/` as non-public working material. Do not synthesize it into public pages without explicit permission.
- Never commit credentials, private Notion exports, client notes, personal journals, or personal data.
- README attribution links are provenance only. Do not treat attributed projects, authors, communities, or tools as operational context for this wiki.

## Core Workflow

### Ingest

When asked to ingest material from `raw/`:

1. Read the source carefully.
2. Identify key claims, entities, concepts, decisions, and open questions.
3. Create or update a source summary in `wiki/sources/`.
4. Create or update relevant pages in `wiki/concepts/`, `wiki/people/`, `wiki/organizations/`, or `wiki/questions/`.
5. Use normal Markdown links, not Obsidian-only syntax.
6. Update `wiki/index.md`.
7. Append a new entry to `wiki/log.md`.

### Query

When answering from the wiki:

1. Read `wiki/index.md` first.
2. Read only the relevant wiki pages.
3. Answer from the wiki, with Markdown links to supporting pages.
4. If the answer is valuable, offer to save it under `wiki/questions/`.
5. If the wiki does not contain enough evidence, say so clearly.

### Lint

Periodically check for:

- Dead links
- Orphan pages
- Duplicate or overlapping pages
- Missing citations
- Missing frontmatter
- Stale or contradictory claims
- Public/private boundary issues

Write reports to `wiki/meta/`.

## Page Convention

Every wiki page should use simple YAML frontmatter:

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

Prefer short pages that can be read cold by a future agent. Split pages when they become sprawling.
