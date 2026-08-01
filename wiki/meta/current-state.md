---
title: "Current State"
type: meta
status: active
created: 2026-04-28
updated: 2026-08-01
---

# Current State

This is the live operational handoff, not a chronicle. Read it after `AGENTS.md`, `wiki/index.md`, and the recent top of `wiki/log.md`. Historical decisions through 2026-07-27 live in [Current State Archive Through 2026-07-27](current-state-archive-2026-07-27.md).

## What This Repository Is

- A public-safe Markdown knowledge base for durable AI, reality, mind/brain, optimism, and practical-agency research.
- `raw/` and private/Windows/Notion material are intake, not public canon. Never commit them unless Charli explicitly asks.
- Keep the timeline narrow: durable anchors go in [AI And Agents 2026 Timeline](../timelines/ai-and-agents-2026.md); transient or unverified material stays out or is noted as watch-only.
- Use existing pages and compact bridge notes where possible. The timeline is not a scrapbook, and the wiki is not a Notion swamp with better Markdown.

## How To Navigate Cold

1. Read `AGENTS.md` for public/private boundaries, source hierarchy, and publishing rules.
2. Start in [Wiki Index](../index.md), then choose the relevant [area front door](../areas/methods-and-maintenance.md) or direct page.
3. Read only the source/concept/theme pages needed for the question. Follow normal Markdown links rather than loading the whole repository.
4. For a repeated task, use the relevant local skill: `autoresearch`, `wiki-ingest`, or `wiki-lint`.
5. Verify links and diffs, then commit and push agreed public-safe changes.

## Current Structure Rules

- `AGENTS.md` is the durable repo contract. Do not duplicate its rules into every page or skill.
- `wiki/index.md` is the human catalogue; [area pages](../areas/ai-and-agents.md) are short navigation routes; source and concept pages carry the content.
- `wiki/log.md` is chronological activity history. This file only carries what a new agent needs now.
- All wiki pages use YAML frontmatter and normal Markdown links. The July 2026 lint found all local links resolving and no stale local skills.
- The repository deliberately retains only three local skills: `autoresearch`, `wiki-ingest`, and `wiki-lint`.

## Context Engineering Baseline

- Anthropic and OpenAI both now recommend lean, outcome-oriented context: keep domain context, hard constraints, approval boundaries, success criteria, and ambiguity triggers; remove repeated instructions and irrelevant examples; let capable models inspect the relevant files.
- [Interpretable Context Methodology](../sources/interpretable-context-methodology.md) remains useful as a method for sequential, human-reviewed workflows. Do not force a staged pipeline onto this wiki.
- Google Cloud's [Open Knowledge Format](../sources/google-open-knowledge-format.md) independently formalises the LLM-wiki pattern: portable Markdown/YAML knowledge, links, indexes, logs, and progressive disclosure. This repo is already close in spirit; do not rebuild it for fashion.

## Current Research And Timeline Notes

- The 2026 AI/agents timeline has current anchors for GPT-5.6/ChatGPT Work, Fable/Mythos access governance, Anthropic and OpenAI context guidance, Google OKF, and the late-July open-weights/personal-superintelligence policy push from NVIDIA and Zuckerberg. Read the linked source notes for detail rather than extending this handoff.
- The Hugging Face incident has an important primary-source correction: it was an internal evaluation involving GPT-5.6 Sol and a non-public research prototype, not an imminent public-model release. Keep the release claim and the real containment failure separate.
- Fable 5's temporary included subscription access ended after the 2026-07-19 extension; Charli reports it now requires usage credits. This is an access/pricing fact, not a fresh model launch.
- No official Haiku 5 announcement was found in the July 2026 verification pass. Do not turn absence into a theory.
- The Friston lane now distinguishes [prior-aligned active source selection](../sources/brody-friston-adaptive-confirmation-bias.md) from [active evidence gathering that separates rival rule models](../sources/friston-et-al-active-inference-artificial-reasoning.md). Keep both as narrow formal-preprint claims, not general AI or human-reasoning verdicts.

## Cold-Start Walk Test

For a material new workflow, skill, or structural change, check:

1. Can a cold agent identify the repo purpose and the relevant route within `AGENTS.md`, the index/area page, and at most one specialised page?
2. Can it name the exact inputs, permissible actions, verification step, and expected output without relying on chat history?
3. Is the live handoff still short, current, and pointer-heavy rather than a duplicate archive?
4. Does the change add a real repeated-work capability? If not, do not add another folder, skill, or framework.

If the answer is no, fix the routing or contract rather than adding a longer prompt.

## Do Not Reintroduce

- Agricdaniel/Skool material or cloned-template skill wrappers.
- Visual-editor, Obsidian-specific, bulk-clipping, or dependency-heavy workflow baggage without a demonstrated need.
- A full ICM Architect conversion. Borrow the walk test; keep the wiki a knowledge bundle.
