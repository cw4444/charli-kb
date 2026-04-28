---
title: "Peter Steinberger Agentic Engineering Batch"
type: source
status: draft
created: 2026-04-28
updated: 2026-04-28
source_type: web-articles
author: "Peter Steinberger"
platform: "steipete.me"
license_note: "Site footer says posts are CC BY 4.0 and code is MIT."
source_urls:
  - https://steipete.me/posts/just-talk-to-it
  - https://steipete.me/posts/2025/shipping-at-inference-speed
sources:
  - "Notion: Peter Just talk to it"
  - "Notion: Peter Shipping at Inference speed"
---

# Peter Steinberger Agentic Engineering Batch

## Metadata

- Author: Peter Steinberger
- Articles:
  - "Just Talk To It - the no-bs Way of Agentic Engineering" (2025-10-14)
  - "Shipping at Inference-Speed" (2025-12-28)
- Topic: practical agentic software engineering workflows
- Access note: read from public web articles linked in Notion queue rows.

## Summary

This batch is useful because it describes a mature working style for coding with agents. The durable point is not the tool preference or timeline drama; it is the workflow shift from manual coding to steering, reviewing, and designing systems that agents can operate inside.

The recurring claims are:

- Treat the agent as a capable collaborator and talk to it directly.
- Reduce ceremony when plain-language steering works.
- Keep blast radius small enough that commits and failures are recoverable.
- Make the codebase easy for agents to navigate: clear docs, obvious file structure, CLIs, tests, and fast feedback loops.
- Use screenshots and concrete artifacts when words are slower than showing the model the problem.
- Prefer workflows where agents can verify their own work through commands, tests, CLIs, or browser checks.
- Expect the human bottleneck to move toward judgment, dependency choice, system design, and taste.

## Useful Synthesis

The best transferable idea is agent-readable infrastructure. A project becomes easier to work on when it has local commands, docs, small scopes, and obvious conventions. This applies beyond software: `charli-kb` is also being shaped so agents can read the index, inspect sources, synthesize pages, and leave an audit trail.

## De-Emphasized

- Tool rivalry and Twitter-linked commentary.
- Claims about specific models as permanent truths; this area changes quickly.
- Personal setup details that only matter for Steinberger's stack.
- Phone/remote-work automation details that are interesting but not central to this wiki right now.

## Useful For

- [Agentic Engineering](../concepts/agentic-engineering.md)
- [Agent Friendly Repositories](../concepts/agent-friendly-repositories.md)
- [Inference Speed Development](../concepts/inference-speed-development.md)
- [Peter Steinberger](../people/peter-steinberger.md)
