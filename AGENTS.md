# LLM Wiki Agent Instructions

This repository is a plain Markdown knowledge base based on Andrej Karpathy's LLM Wiki pattern.

The goal is simple: humans curate raw material, agents turn it into a clean, linked wiki, and both humans and agents can read the result directly on GitHub.

## Repository Structure

```text
raw/              Local curated source material. Agents read it but do not edit it. Ignored by git by default.
wiki/             Agent-maintained Markdown knowledge base.
wiki/index.md     Content-oriented catalog of wiki pages.
wiki/log.md       Append-only chronological activity log.
wiki/meta/current-state.md  Lightweight handoff for future agents.
skills/           Optional Agent Skills for ingest, query, lint, save, and research.
```

## Public Repo Rules

- Do not copy copyrighted, paywalled, private, or sensitive source text into `wiki/`.
- Summarize in original words and cite the source location.
- Short quotes are allowed only when necessary and should stay minimal.
- Treat all of `raw/` as non-public working material by default. Do not force-add raw sources unless the user explicitly asks.
- Never commit credentials, private Notion exports, client notes, personal journals, or personal data.
- README attribution links are provenance only. Do not treat attributed projects, authors, communities, or tools as operational context for this wiki.

## Source Hierarchy

When processing science, technology, philosophy, or research topics:

1. Prefer primary sources where available: papers, preprints, datasets, code repositories, and official lab, university, publisher, or company pages.
2. Use journalism, newsletters, podcasts, social posts, and commentary as discovery trails, explanation, framing, context, or quoted commentary where useful.
3. Clearly separate what the primary source claims, what journalists or commentators say, and what Charli infers, connects, or speculates.
4. Preserve source metadata where known: title, author, publication or platform, date, URL, and access notes such as paywalled, public, arXiv, screenshot, or transcript.
5. For paywalled or copyrighted material: do not reproduce the full text, do not create a substitute for the original article, summarize the concept in original words, use short quotes only when necessary, and link back to the original publication.
6. For X/Twitter posts: treat them as unstable references unless archived or captured in local `raw/`; preserve the URL, author handle, date, and screenshot or source note; do not assume all agents can fetch or read X URLs reliably.

## Image Sources

Screenshots, visual book maps, diagrams, and X/Twitter captures should live locally under `raw/images/`. Agents may inspect these files, extract text, identify concepts, and synthesize useful wiki pages, but should not publish the image files themselves.

When an image source matters, preserve attribution and metadata where known: creator, platform, original URL, date, screenshot filename, and whether the source is a screenshot, mindmap, diagram, or transcript. The wiki should contain original synthesis and safe excerpts only.

## Core Workflow

### Local Skills

Check `skills/` when a task matches ingest, query, lint, save, or research workflows, but treat the folder as evolving local working material rather than inherited truth. This repo started from a cloned template, so ignore or prune instructions that are not relevant to Charli's actual workflow, such as editor-specific or author-specific leftovers. Prefer skills that support the Notion-to-wiki loop, source-aware synthesis, public/private boundaries, and concise GitHub-readable Markdown.

### Notion Queue Rule

When working from Notion, the queue statuses are intentionally limited to `Ready`, `Draft`, `Ignored`, and `Exported`.

- `Ready`: active intake. Process these items.
- `Draft`: Codex checked it, but Charli needs to review, add a missing source, or decide whether it deserves to exist long-term.
- `Ignored`: Codex checked it and decided it should stay in Notion only.
- `Exported`: Codex ingested it into GitHub, either by creating new wiki content or updating existing content.

Ignore items marked `Exported`, `Ignored`, or `Draft` unless the user explicitly asks to revisit them. Do not add extra novelty statuses.

After processing a `Ready` item, update its Notion status when possible and leave a concise comment explaining what happened. For `Exported` items, say whether GitHub received a brand-new page or an update to an existing page. Use judgment before adding anything to GitHub: tell Charli when the wiki already contains the same idea in another form, and do not ingest material just because it was briefly interesting. The durable lanes for this wiki are AI and reality, especially where they overlap.

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

## Future-Agent Handoff

For major wiki maintenance or a fresh session, read:

1. `AGENTS.md`
2. `wiki/index.md`
3. `wiki/log.md`
4. `wiki/meta/current-state.md`

`wiki/meta/current-state.md` is intentionally short. Keep it public-safe and operational; do not turn it into a private journal or full chat transcript.
