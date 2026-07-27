---
title: "Google Open Knowledge Format"
type: source
status: draft
created: 2026-07-27
updated: 2026-07-27
sources:
  - "Google Cloud: Introducing the Open Knowledge Format, 2026-06-12"
  - "GoogleCloudPlatform knowledge-catalog OKF v0.2 specification, checked 2026-07-27"
---

# Google Open Knowledge Format

## Metadata

- Title: "Introducing the Open Knowledge Format"
- Authors: Sam McVeety and Amir Hormati
- Publisher: Google Cloud
- Published: 2026-06-12
- Blog URL: <https://cloud.google.com/blog/products/data-analytics/how-the-open-knowledge-format-can-improve-data-sharing>
- Specification/repository: <https://github.com/GoogleCloudPlatform/knowledge-catalog/tree/main/okf>
- Access note: public Google Cloud announcement and public implementation/specification. OKF v0.1 was announced in the post; the repository now labels the specification v0.2, so version-specific requirements may have changed.

## Summary

Google Cloud introduced the Open Knowledge Format (OKF), an open, vendor-neutral format for agent- and human-readable knowledge. The company explicitly frames it as a formalisation of Andrej Karpathy's LLM-wiki pattern: a directory of Markdown files with YAML frontmatter, ordinary Markdown links, and optional `index.md` and `log.md` files.

This matters because it converts a useful repo habit into a proposed interoperability surface. Instead of agents repeatedly reconstructing context from proprietary catalog APIs, scattered wikis, code comments, and senior-engineer memory, an organization can ship a portable knowledge bundle that people, agents, search tools, static viewers, and different model providers can all read. Google says its Knowledge Catalog can ingest OKF and serve it to agents, but the format itself is not tied to Google Cloud or any SDK.

## What OKF Standardises

- One concept per Markdown file, organised in a directory hierarchy; the path supplies the concept identity.
- YAML frontmatter for small queryable fields. The initial post names type, title, description, resource, tags, and timestamp; the later v0.2 repository also describes provenance, verification, status, and freshness fields.
- Standard Markdown links between concept files, producing a graph richer than folder hierarchy alone.
- Optional `index.md` navigation files for progressive disclosure and `log.md` files for chronological changes.
- A deliberately small required surface: the original v0.1 post says every concept needs a type, while producers may add their own fields and body structure.
- Producer/consumer independence: humans, agents, metadata-export pipelines, static sites, search indexes, and other LLMs can write or consume the same files without a proprietary translation layer.

## Why It Matters Here

This is the external standard-shaped version of the design already used by this wiki and described by [Interpretable Context Methodology](interpretable-context-methodology.md). The parallel is almost comically exact: Markdown pages, frontmatter, normal links, an index, a log, Git-friendly review, and progressive context loading.

It also completes the 2026 context-engineering convergence in a third layer:

- Anthropic and OpenAI say capable models should inspect a legible environment instead of being force-fed repetitive prompt bulk.
- ICM describes how folders, contracts, and readable artifacts can structure that environment.
- Google proposes that the environment itself can be a portable interchange format across agents, tools, and organizations.

The useful claim is not that every Markdown folder is now automatically interoperable, or that OKF has won adoption. It is that a major cloud provider has publicly endorsed the LLM-wiki shape as standard-worthy infrastructure rather than a quirky individual workflow.

## Limits

- OKF v0.1/v0.2 is an emerging specification, not evidence of broad cross-vendor adoption or a settled industry standard.
- A portable format does not solve accuracy, staleness, access control, private-data leakage, source quality, or malicious instructions embedded in content.
- The Google reference agent and visualiser are proofs of concept; the format does not require Google tooling, BigQuery, a graph viewer, or any particular model.
- Markdown/YAML makes knowledge inspectable, not automatically correct. Provenance and review remain actual jobs. Tragically, the files do not become adults merely because they have frontmatter.

## Useful For

- [Filesystem Agent Architecture](../concepts/filesystem-agent-architecture.md)
- [Agent Friendly Repositories](../concepts/agent-friendly-repositories.md)
- [Interpretable Context Methodology](interpretable-context-methodology.md)
- [AI And Agents 2026 Timeline](../timelines/ai-and-agents-2026.md)
