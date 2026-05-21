---
title: "Current State"
type: meta
status: active
created: 2026-04-28
updated: 2026-05-21
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

- Updated [Sidequest Prototyping](../concepts/sidequest-prototyping.md) with the stronger Anthropic/Cat Wu "sidequest maxxing" operational pattern: afternoon prototypes, demos over standups, dogfooding, repeated internal use as the filter, and cross-functional people shipping working demos. Keep the source boundary visible: preserve the workflow pattern, but do not treat every Claude Code feature-origin anecdote as settled fact without a primary transcript/source.
- Added [Daily AI Timeline Refresh](daily-ai-timeline-refresh.md), a checked-in operating brief for a daily Codex automation that checks trusted AI/agent sources and updates the 2026 timeline only when a verified event is historically useful. It includes source priorities, inclusion rules, watch-only handling, and a completion report format.
- Updated [AI And Agents 2026 Timeline](../timelines/ai-and-agents-2026.md) with Block's February 2026 AI-linked workforce reset: more than 4,000 roles cut, roughly 40% of staff, with Jack Dorsey explicitly framing "intelligence tools" as changing how companies can be built and run. Keep the caveat visible: this is a CEO-level workplace-rearchitecture signal, not proof that AI replaced every affected role one-for-one.
- Updated [AI And Agents 2026 Timeline](../timelines/ai-and-agents-2026.md) with Meta's May 2026 AI restructuring: roughly 8,000 layoffs, roughly 7,000 AI-focused reassignments, and leaked-audio/reporting controversy around employee computer-use data being used to train AI systems. Keep the wording careful: this is a workplace-rearchitecture signal, not proof that every Meta employee moved into AI or that every layoff was directly automated.
- Added [AI And Agents 2026 Timeline](../timelines/ai-and-agents-2026.md) to preserve the sequence of fast-moving AI/agent events without overpromoting every news flare into canon. It includes explicit future-lint guidance: update if historically useful, collapse or delete if it becomes stale noise.
- Added [Anthropic Compute And Talent Signal 2026](../sources/anthropic-compute-and-talent-signal-2026.md), capturing the May 2026 convergence of Andrej Karpathy joining Anthropic's pre-training team and Anthropic's SpaceX/Colossus compute deal. Treat this as a strategic signal, not a conclusion: Anthropic is combining explicit character/welfare-safety framing with frontier-scale compute pressure, Claude Code/agent demand, and elite pre-training talent.
- Updated [AI Character Formation And Persona Safety](../../themes/ai-consciousness/character-formation-and-persona-safety.md) with the stronger constitution-as-self-introduction point: Anthropic's full constitution is written with Claude as the primary audience, and "Teaching Claude why" reports that constitutional documents plus positive fictional stories about admirable AI can reduce agentic misalignment. Keep the boundary clear: this is evidence that persona, narrative, and role self-description affect model behavior, not evidence that Claude is conscious.
- Updated the agent guide with a one-line local-agent install warning: `curl ... | bash`, `sudo`, global installs, Docker/VPS choices, permissions, logs, and API budgets are not cute beginner details. Keep this distinction visible when discussing OpenClaw-style tools: the emotional companion framing is not the core issue; broad local automation plus unclear consent boundaries is.
- Added [Current AI Agent Landscape 2026](../sources/current-ai-agent-landscape-2026.md) and [What Can AI Agents Do For Normal Tired Humans?](../questions/what-can-ai-agents-do-for-normal-tired-humans.md), using current official/public sources from OpenAI, Anthropic, Google, xAI, and OpenClaw. The useful frame is practical and bounded: agents are execution loops with tools, state, permissions, logs, and approval gates, not autonomous adults. The tired-human guide emphasizes read-only first runs, explicit consent for destructive or high-impact actions, and small bounded tasks over "organize my whole life" prompts.
- Added [Practical Agency Inside Constraint](../concepts/practical-agency-inside-constraint.md), capturing Charli's "Yoneda-brain" agency frame as working interpretation. The page says meaningful agency does not require metaphysical escape from relational or causal constraint; it can mean better model-building, identifying live interventions, changing one relation or boundary condition, and watching what propagates. Keep the caveat visible: this is a conceptual bridge, not a claim that Yoneda literally explains physics, determinism, or free will.
- Added [Devs - Prediction, Determinism, And Acceleration](../sources/devs-prediction-determinism.md) as a cultural reference for the mechanical-world-models thread. It frames *Devs* as fiction about prediction becoming metaphysics: Antikythera shows cyclic prediction before correct ontology, *Devs* imagines complete prediction as total ontology, and AI gives probabilistic prediction strong enough to disturb ontology. Keep the caveat visible: this is cultural interpretation, not evidence for real quantum prediction machines or hard determinism.
- Added [Michael Levin - Unconventional Cognition And AI](../sources/michael-levin-unconventional-cognition.md) and [Michael Levin](../people/michael-levin.md), tying the new mechanical-world-models page to Levin's public commentary on unconventional cognition, interfaces, and AI as unfamiliar embodiment. The useful bridge is substrate humility: "gears," "chemistry," and "linear algebra" can all be true descriptions without exhausting the relevant behavioral or cognitive ontology. Keep the caveat visible: this is not evidence that current AI is conscious.
- Added [Antikythera Mechanism Source Batch](../sources/antikythera-mechanism-source-batch.md) and [Mechanical World Models](../concepts/mechanical-world-models.md), using public research and official archaeology sources. The page frames the Antikythera mechanism as a hand-powered astronomical calculator and a bridge concept for computation as model-mediated reality, not as ancient AI. The key lunar-motion point is preserved carefully: the mechanism could approximate the Moon's variable apparent speed through cyclic theory and gearing without the makers needing modern knowledge of elliptical orbits.
- Updated the AI consciousness package with Chang-Eop Kim's revised *The Epistemic Asymmetry of Consciousness Self-Reports* and Alexander Lerchner's Google DeepMind-listed *The Abstraction Fallacy*. Kim is used narrowly to caution that model self-denials are not decisive evidence of non-consciousness; Lerchner is used as a recent anti-functionalist counterpoint arguing that abstract computation can simulate but not instantiate consciousness. Neither source is treated as settling current AI consciousness.
- Added [Rovelli, Relational Quantum Mechanics, and Reality](../../themes/rovelli-relational-quantum-mechanics-and-reality.md) and [Rovelli And Relational Quantum Mechanics](../sources/rovelli-relational-quantum-mechanics.md), because RQM was underrepresented as a mere subsection in `Interpretations` even though it is one of the strongest fits for the repo's reality lane. Framed it around relation-first facts, the absence of a God's-eye ledger, contrast with QBism/Everett/Wheeler, and a cautious "same font" bridge to category-theoretic thinking without claiming RQM literally is Yoneda in physics drag.
- Added [Feynman, Calculation, and Reality Stories](../../themes/feynman-calculation-and-reality-stories.md) and [Feynman - Calculation And Reality Stories](../sources/feynman-calculation-and-reality-stories.md), using public primary sources to position Feynman as a bridge figure: useful not as a generic genius page, but as a disciplined distinction between what quantum theory lets you calculate and what metaphysical or psychological story people add afterward. Cross-linked it to [Reality Threshold](../concepts/reality-threshold.md) and [Perception And Imagination Overlap](../concepts/perception-and-imagination-overlap.md) so the physics lane now connects more explicitly to brain-level fact-making.
- Added [Positive Alignment: Artificial Intelligence for Human Flourishing](../sources/positive-alignment-human-flourishing.md) and [Positive Alignment](../concepts/positive-alignment.md), based on the May 11, 2026 arXiv paper by a cross-lab author group spanning Oxford, DeepMind, OpenAI, Anthropic, Stanford, and others. Framed it as a constructive-alignment agenda aimed at flourishing-supporting positive attractors, with explicit cautions about paternalism, vagueness, and not confusing alignment rhetoric with consciousness evidence.
- Updated the optimism package with Taylor and Brown's positive-illusions framing plus critiques and methodological cautions, so the repo now distinguishes adaptive optimism, unrealistic optimism, positive illusions, and denial instead of flattening them into generic positivity.
- Added [Optimism Neuroscience Source Batch](../sources/optimism-neuroscience-source-batch.md), [Optimism](../concepts/optimism.md), and [Research - Optimism](../questions/research-optimism.md), using public sources to frame optimism as a future-representation style involving vivid positive imagery, asymmetric belief updating, and possible psychological distancing from negative futures. Kept a clear caveat that the "abstract negative events" point is a source-grounded interpretation rather than a settled mechanism.
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

- Create the daily AI timeline refresh automation in the Codex app using [Daily AI Timeline Refresh](daily-ai-timeline-refresh.md) as the prompt/brief.
- Update `AGENTS.md` later to reflect the repo-first research default and demote the Notion queue to optional intake.
- Consider trimming or rewriting old Notion-centric guide pages so they do not imply Notion is required for research.
- Periodically lint the wiki for dead links, duplicate concepts, stale source notes, and public/private boundary issues.
- Consider consolidating overlapping concepts only after several more ingest batches reveal real repetition.
