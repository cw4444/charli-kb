---
title: "Inference Speed Development"
type: concept
status: draft
created: 2026-04-28
updated: 2026-05-11
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

## Felt-Speed Spillover

Inference-speed work can create [Cognitive Latency Shock](cognitive-latency-shock.md): once a person gets used to AI matching their research/build pace, ordinary knowledge work may feel slow, boring, or under-instrumented. That is a real productivity and perception shift, but it also creates verification debt and social impatience if the person starts expecting all reality to move at agent speed.

## Related

- [Agentic Engineering](agentic-engineering.md)
- [Agent Friendly Repositories](agent-friendly-repositories.md)
- [Cognitive Latency Shock](cognitive-latency-shock.md)
