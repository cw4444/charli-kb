# charli-kb

A plain Markdown knowledge base built around Andrej Karpathy's LLM Wiki pattern.

This is a personal knowledge base, not a finished reference encyclopedia. The structure is open for anyone to copy, adapt, or interrogate with an AI agent; the actual wiki content reflects my own reading, notes, and current lines of thought.

This repo is intentionally small. It is not an Obsidian vault and it is not tied to a specific AI agent. The pattern is:

1. Put curated source material in `raw/`.
2. Ask an AI coding agent to process it.
3. The agent writes clean, linked Markdown pages in `wiki/`.
4. The agent keeps `wiki/index.md` and `wiki/log.md` current.

## Folders

```text
raw/              Source material you curate.
raw/private/      Local/private material. Do not publish by default.
wiki/             Generated knowledge base.
skills/           Optional Agent Skills for supported agents.
AGENTS.md         Instructions for agents working in this repo.
```

## Basic Use

Drop or export useful material into `raw/`, then ask your agent:

```text
Ingest raw/articles/example.md into the wiki.
```

For questions:

```text
Answer from the wiki: what do we know about X?
```

For maintenance:

```text
Lint the wiki.
```

## Public Repo Safety

This repository is meant to be readable on GitHub, but `raw/` is ignored by default. Do not publish private notes, personal data, client material, credentials, or copied paywalled/copyrighted text. The wiki should contain original summaries and citations, not wholesale source dumps.

## Why This Exists

Notion remains the messy capture dump. `charli-kb` is the distilled layer: an agent-readable personal knowledge base that can be queried, reviewed, linted, and updated over time.

The goal is not to save everything. The goal is to keep what becomes useful when an agent can connect it to other notes, current projects, and future questions.

## Skills

The reusable skills are:

- `wiki-ingest`: turn raw material into wiki pages.
- `wiki-query`: answer from the wiki and optionally save useful answers.
- `wiki-lint`: check the wiki's health.
- `save`: file durable insights from a conversation.
- `defuddle`: optional URL cleanup helper.
- `autoresearch`: optional web research loop for users who want agent-led research.

The repo keeps these as plain Agent Skills in `skills/<name>/SKILL.md`.

## Attribution

Original concept by [Andrej Karpathy](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f). Repository structure adapted from [AgriciDaniel/claude-obsidian](https://github.com/AgriciDaniel/claude-obsidian). This repo is built and maintained with [Codex from OpenAI](https://chatgpt.com/codex/cloud).
