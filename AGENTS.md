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

## Source Hierarchy

When processing science, technology, philosophy, or research topics:

1. Prefer primary sources where available: papers, preprints, datasets, code repositories, and official lab, university, publisher, or company pages.
2. Use journalism, newsletters, podcasts, social posts, and commentary as discovery trails, explanation, framing, context, or quoted commentary where useful.
3. Clearly separate what the primary source claims, what journalists or commentators say, and what Charli infers, connects, or speculates.
4. Preserve source metadata where known: title, author, publication or platform, date, URL, and access notes such as paywalled, public, arXiv, screenshot, or transcript.
5. For paywalled or copyrighted material: do not reproduce the full text, do not create a substitute for the original article, summarize the concept in original words, use short quotes only when necessary, and link back to the original publication.
6. For X/Twitter posts: treat them as unstable references unless archived or captured in `raw/`; preserve the URL, author handle, date, and screenshot or source note; do not assume all agents can fetch or read X URLs reliably.

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
