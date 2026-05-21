---
title: "Codex Goals"
type: concept
status: draft
created: 2026-05-21
updated: 2026-05-21
sources:
  - ../sources/openai-codex-for-everyday-work.md
---

# Codex Goals

Codex Goals are persistent, thread-scoped objectives that keep Codex working toward a defined outcome across turns.

The important distinction:

- a prompt says: do this next thing;
- a Goal says: keep working until this outcome is true, or until the evidence says the work is blocked.

Goals are useful when the next step depends on what Codex learns while working: debugging, profiling, benchmarking, reproducing a bug, investigating a research question, or iterating toward a verified artifact.

## Goal As Completion Contract

OpenAI's cookbook frames a Goal as a user-controlled completion contract, not background autonomy without boundaries.

A good Goal defines:

- **Outcome:** what should be true when done;
- **Verification surface:** test, benchmark, report, artifact, command output, source material, or other evidence;
- **Constraints:** what must not regress;
- **Boundaries:** allowed files, tools, data, repos, or resources;
- **Iteration policy:** how Codex should decide what to try next;
- **Blocked stop condition:** when Codex should stop and report that no defensible path remains.

This is the useful template:

```text
/goal <desired end state> verified by <specific evidence> while preserving <constraints>. Use <allowed inputs, tools, or boundaries>. Between iterations, <how Codex should choose the next best action>. If blocked or no valid paths remain, <what Codex should report and what would unlock progress>.
```

## Good And Bad Goals

Weak:

```text
/goal Improve performance
```

Stronger:

```text
/goal Reduce p95 latency below 120 ms on the checkout benchmark while keeping the correctness test suite green.
```

Even stronger:

```text
/goal Reduce p95 checkout latency below 120 ms, verified by the checkout benchmark, while keeping the correctness suite green. Use only the checkout service, benchmark fixtures, and related tests. Between iterations, record what changed, what the benchmark showed, and the next best experiment to try. If the benchmark cannot run or no valid paths remain, stop with the attempted paths, the evidence gathered, the blocker, and the next input needed.
```

The strong version gives Codex room to explore without letting it declare victory from vibes.

## Research Goals

Goals are especially useful for research because research often cannot be "proved done" in a simple binary way.

A strong research Goal should define:

- the claim inventory;
- the evidence standard;
- what counts as exact reproduction;
- what counts as approximate or proxy support;
- what should be labeled blocked;
- what final artifact should separate confirmed findings from uncertainty.

Useful pattern:

```text
/goal Produce the strongest evidence-backed answer using available public sources and local materials. Map claims to evidence, verify what can be verified, label blocked claims, and end with a report separating confirmed findings, support-only evidence, blocked claims, and remaining uncertainty.
```

That pattern fits this wiki. It can prevent the agent from turning a fuzzy research hunch into an overconfident page.

## Why This Matters

Goals make Codex more useful because the objective persists while the evidence changes. If a test fails, benchmark improves but misses threshold, source cannot be verified, or artifact does not build, Codex can keep the original finish line in view.

But the same persistence makes boundaries more important. A Goal should not be broad like "fix the whole project" or "research AI." It should be narrow enough to audit and broad enough to let Codex choose the next useful action.

## Do Not Overclaim

- Do not treat Goals as autonomous delegation without supervision.
- Do not use Goals when a one-off prompt is enough.
- Do not mark a Goal complete without checking evidence.
- Do not let budget limits masquerade as completion.
- Do not use a Goal for high-impact actions without approval gates.

The safe version is: persistent objective, explicit verifier, bounded tools, and evidence-based completion.

## Related Pages

- [OpenAI Codex For Everyday Work](../sources/openai-codex-for-everyday-work.md)
- [Computer Work Agent](computer-work-agent.md)
- [Agent Prompting](agent-prompting.md)
- [How Can Normal Humans Use Codex?](../questions/how-can-normal-humans-use-codex.md)
- [Agentic Work Rearchitecture](agentic-work-rearchitecture.md)
