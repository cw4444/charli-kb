---
title: "Inference Speed Development"
type: concept
status: draft
created: 2026-04-28
updated: 2026-04-28
sources:
  - ../sources/peter-steinberger-agentic-engineering-batch.md
---

# Inference Speed Development

Inference speed development is the shift that happens when the limiting factor in software work becomes model runtime, context quality, and human judgment rather than hand-written code volume.

In this mode:

- The human queues or steers tasks.
- The agent reads, edits, tests, and reports.
- The human watches for wrong direction, large blast radius, bad dependencies, or poor taste.
- Faster feedback loops matter more than perfect upfront specification.
- CLI-first interfaces are valuable because agents can call them directly and verify results.

The concept should not be read as "stop reading code." It is better framed as selective review: read architecture, boundaries, risky changes, and key diffs; let agents handle routine implementation and refactoring when tests and local checks exist.

## Related

- [Agentic Engineering](agentic-engineering.md)
- [Agent Friendly Repositories](agent-friendly-repositories.md)
