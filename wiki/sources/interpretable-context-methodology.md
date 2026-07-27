---
title: "Interpretable Context Methodology"
type: source
status: draft
created: 2026-05-21
updated: 2026-07-27
source_path: https://arxiv.org/abs/2603.16021
---

# Interpretable Context Methodology

## Metadata

- Title: "Interpretable Context Methodology: Folder Structure as Agentic Architecture"
- Authors: Jake Van Clief and David McDermott
- Venue: arXiv, `2603.16021`
- Submitted: 2026-03-17
- Revised: 2026-03-18
- URLs: <https://arxiv.org/abs/2603.16021>, <https://ar5iv.labs.arxiv.org/html/2603.16021>
- Access note: public arXiv paper. The paper references an MIT-licensed GitHub repository at `https://github.com/RinDig/Interpretable-Context-Methodology-ICM-`; checked on 2026-05-21 and the URL returned GitHub 404.

## Summary

Van Clief and McDermott argue that many AI workflow builders are using multi-agent orchestration frameworks for jobs that are actually sequential, reviewable, and repeatable. Their proposed Interpretable Context Methodology (ICM) uses folders, Markdown contracts, and local scripts as the architecture: numbered folders encode stages, `CONTEXT.md` files define what each stage reads and writes, and plain files become the handoff surface between agent work and human review.

The paper is most useful here because it gives a formal name to something this wiki already leans toward: agent systems do not always need a complicated harness. Sometimes the durable system is the folder structure, the source-aware Markdown, the scripts that do boring mechanical work, and the human who reviews each intermediate artifact.

## Key Claims

- For sequential human-reviewed workflows, orchestration can live in the filesystem rather than in a framework.
- Numbered stage folders can encode execution order.
- Stage-level `CONTEXT.md` files can act as contracts: inputs, process, outputs.
- Markdown and JSON are useful interfaces because humans, scripts, Git, and agents can all inspect them.
- Local scripts should handle mechanical tasks that do not need a model.
- Context should be scoped by stage rather than loaded as one giant monolithic prompt.
- The method separates stable reference material from per-run working artifacts.
- Human review gates become natural because every intermediate output is a readable file.
- The approach is complementary to MCP: MCP connects tools and data sources; ICM structures which context an agent sees at each stage.

## The Five-Layer Context Pattern

The paper describes a five-layer hierarchy:

- Layer 0: global workspace identity, often `CLAUDE.md`.
- Layer 1: workspace routing, often top-level `CONTEXT.md`.
- Layer 2: stage contracts, usually each stage's `CONTEXT.md`.
- Layer 3: stable reference material, such as voice, design, domain, or convention files.
- Layer 4: working artifacts, such as source material, previous-stage outputs, drafts, and run-specific files.

For this wiki, the useful translation is:

- `AGENTS.md` and `wiki/meta/current-state.md` tell the agent where it is and what kind of system this is.
- `skills/` define repeatable workflows.
- `wiki/sources/` preserves source summaries.
- `wiki/concepts/`, `wiki/questions/`, and theme pages hold distilled reusable knowledge.
- `wiki/log.md` is the inspectable audit trail.

That is already close to ICM in spirit, though this repo is a knowledge base rather than a numbered production pipeline.

Google Cloud's later [Open Knowledge Format](google-open-knowledge-format.md) gives the pattern an external interoperability counterpart: Markdown, frontmatter, normal links, indexes, and logs can be not only a local workflow architecture but a portable bundle that different agents and knowledge tools consume. ICM remains the more specific workflow method; OKF is the thinner exchange contract.

## Evidence And Limits

The paper reports working implementations in content production, slide-deck generation, academic research workflows, and policy analysis. It also reports early practitioner observations, including self-reported intervention patterns from 33 practitioners and a small anecdote about non-coders creating workspaces.

The limits are important:

- The observations are informal rather than controlled measurement.
- The practitioner community is self-selected.
- Most active use is concentrated in content production.
- The paper's testing used Claude Opus 4.6 and Sonnet 4.6, so cross-model generalization remains open.
- The claim that stage-scoped context improves output quality is plausible and supported by context research, but not yet proven by controlled comparison against monolithic prompting.
- ICM is not a replacement for real-time multi-agent collaboration, high-concurrency systems, or complex automated branching.

## Useful For

- [Filesystem Agent Architecture](../concepts/filesystem-agent-architecture.md)
- [Agentic Engineering](../concepts/agentic-engineering.md)
- [Agent Friendly Repositories](../concepts/agent-friendly-repositories.md)
- [Agent Prompting](../concepts/agent-prompting.md)
- [Queryable Organization](../concepts/queryable-organization.md)
- [Google Open Knowledge Format](google-open-knowledge-format.md)
