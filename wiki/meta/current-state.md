---
title: "Current State"
type: meta
status: active
created: 2026-04-28
updated: 2026-05-12
---

# Current State

This repo is a plain Markdown personal knowledge base based on Karpathy's LLM Wiki idea. It is meant to be readable by humans and AI agents directly on GitHub.

## Current Workflow

- Default to repo-first research when Charli asks a research question: search public/primary sources directly, synthesize into Markdown, update index/log/handoff, then commit and push.
- Notion is optional intake, not the main workflow. Use it only when it contains something uniquely useful: Charli's own hunch, private context, screenshot, source trail, or a saved item she explicitly wants processed.
- Most copied articles in Notion are discussion material, not durable source material. Do not treat Notion clips as adding value when public sources can be researched directly.
- The Notion `Ready to Export` database remains a review queue only for items Charli deliberately wants checked.
- Agents only need to check items marked `Ready`.
- The only queue statuses should be `Ready`, `Draft`, `Ignored`, and `Exported`.
- Items marked `Exported`, `Ignored`, or `Draft` should be skipped unless Charli explicitly asks to revisit them.
- Agents read `Ready` items and decide whether to ingest as `Exported`, leave for human review as `Draft`, or reject as `Ignored`.
- Useful synthesis goes into Markdown in the repo. For larger research packages, root-level folders such as `sources/`, `themes/`, `maps/`, and `reading-paths/` are acceptable when they make the result clearer than forcing everything into `wiki/`.
- Raw/private material stays out of git.
- Notion comments and `AI Summary` fields are useful audit trails only for Notion-originated items.
- Local `skills/` are useful but may include cloned-template leftovers; use only the parts relevant to Charli's actual workflow.
- Codex is the gatekeeper for GitHub KB updates. Charli should capture and mark candidates, but agents should create, update, index, log, and push wiki changes.
- Agreed wiki, rule, or handoff updates should be committed and pushed to GitHub after verification unless publication risk is unclear.

## Current Priorities

- Keep the wiki small, useful, and source-aware.
- Prefer synthesis over archiving.
- Do not ingest every interesting thing.
- Warn Charli when a queued item is the same idea already captured elsewhere in the wiki.
- Use discernment: the main lanes are AI and reality, especially where they overlap.
- Separate primary-source claims, commentary, and Charli's own inferences.
- Preserve source metadata and copyright boundaries.
- Keep the repo agent-readable without adopting an Obsidian workflow.
- Keep skills aligned with repo-first, source-aware research. The local `autoresearch` skill is a thin local adaptation inspired by Karpathy's autoresearch pattern; keep it lightweight and focused on public-safe Markdown synthesis.
- Keep GitHub as the clean distilled knowledge base, not a second Notion or bulk Markdown export target.
- The durable subject lanes are AI, reality, and their overlap: perception, belief, expectation, action, agents, knowledge systems, reality monitoring, and related source-backed concepts.

## Recent Additions

- Added [Many-Worlds, Wheeler, and Observer-Dependent Reality](../../themes/many-worlds-and-observer-dependent-reality.md), which finally ties Everett properly into the Bell/Wigner package instead of leaving it as a short paragraph in `Interpretations`. The page compares Everett with Wheeler, QBism, relational quantum mechanics, consistent histories, Frauchiger-Renner, local friendliness, information-theoretic approaches, and Markus Muller's observer-first edge cases.
- Added [Agentic Work Rearchitecture](../concepts/agentic-work-rearchitecture.md) and [Enterprise Agent Deployment 2026](../sources/enterprise-agent-deployment-2026.md), capturing the 2026 shift from AI as productivity add-on to governed enterprise agents and work redesign.
- Updated the root [README](../../README.md) so a human or agent can see the repo's two main lanes: AI and reality. The Bell/Wigner package is now a section rather than the whole framing.
- Added [Cognitive Latency Shock](../concepts/cognitive-latency-shock.md), using the [Bryan Johnson Claude KB Tweet](../sources/bryan-johnson-claude-kb.md) as a source for the felt-speed shift that happens when AI turns raw material into queryable memory and fast artifacts.
- Added [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md), connecting Anthropic's "Teaching Claude Why," persona vectors, agentic misalignment, Claude's constitution, and the idea that model character/persona is becoming a safety surface.
- Added [Mind Children - Hans Moravec](../sources/mind-children-hans-moravec.md), plus [Hans Moravec](../people/hans-moravec.md), as historical lineage for AI consciousness, mind uploading, substrate independence, posthumanism, continuity of self, and machine intelligences as possible descendants rather than tools.
- Added [QBism, Global Constraints, and Observer-Dependent Reality](../../themes/qbism-adlam-observer-dependent-reality.md), a careful comparison of QBism and Emily Adlam's all-at-once/global-constraint ideas. The page keeps agent-relative quantum states separate from global law/time structure and explicitly warns against idealism, simulation-theory, and consciousness-causes-collapse overclaims.
- Added a root-level research package, [AI Consciousness And Model Welfare](../../themes/ai-consciousness/overview.md), with public-source synthesis on AI consciousness, model welfare, self-reports, interpretability, agency, functionalism, biological objections, moral patienthood, company positions, a source CSV, a Mermaid map, and a reading path.
- Workflow update: repo-first direct research is now preferred for public research topics; Notion is reserved for genuinely useful intake rather than copied article storage.
- Added a root-level research package, [Bell, Wigner's Friend, and Observer-Dependent Reality](../../README.md), with source metadata, theme pages, concept maps, reading path, glossary, open questions, and optional static HTML.
- Added [How Can Normal Humans Use Codex?](../questions/how-can-normal-humans-use-codex.md), a plain-English guide to Codex for non-developers.
- Added [OpenAI Codex For Everyday Work](../sources/openai-codex-for-everyday-work.md), based on official OpenAI Codex documentation, Help Center pages, and prompt guidance.
- Added examples of small first Codex prompts for non-developers: local trackers, simple galleries, folder inspection, and approval-gated cleanup.
- Created two Codex automation proposals in the app: one daily Notion `Ready to Export` review for `charli-kb`, and one daily official OpenAI Codex docs refresh check for the non-developer guide.

## Things To Know

- Charli values blunt discernment over enthusiastic hoarding.
- The AI consciousness/model welfare package is intentionally balanced: it does not conclude current AI is conscious, does not dismiss AI consciousness as impossible, separates consciousness from agency and moral patienthood, and treats company welfare/safety materials as important but not neutral.
- The Bell/Wigner/observer-dependent-reality package is the current template for substantial research threads: overview, source index, structured source data, theme pages, concept map, reading path, glossary, open questions, conservative caveats, and optional static HTML.
- When researching, prefer primary sources, public papers, official pages, reputable reviews, and explicit caveats over copied article text from Notion.
- It is okay to mark items `Ignored` when they are only personally resonant or already covered by existing wiki pages.
- It is okay to mark items `Draft` when they need missing sources, source clarification, or human judgment.
- Mark items `Exported` only when GitHub received a new page or an update to an existing page.
- Do not add extra statuses; four states are enough.
- When ingesting from Notion, leave a comment explaining what happened and update the row status when possible.
- For `Exported` Notion rows, say whether GitHub received a new page or an update to an existing page.
- Use the external-reader test: would this help an external human reader or future agent, or is it only a private memory?
- Future agents should read `AGENTS.md`, `wiki/index.md`, `wiki/log.md`, and this page before major wiki maintenance.

## Next Useful Steps

- Update `AGENTS.md` later to reflect the repo-first research default and demote the Notion queue to optional intake.
- Consider trimming or rewriting old Notion-centric guide pages so they do not imply Notion is required for research.
- Periodically lint the wiki for dead links, duplicate concepts, stale source notes, and public/private boundary issues.
- Consider consolidating overlapping concepts only after several more ingest batches reveal real repetition.
