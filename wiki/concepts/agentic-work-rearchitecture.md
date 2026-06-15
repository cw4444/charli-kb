---
title: "Agentic Work Rearchitecture"
type: concept
status: draft
created: 2026-05-11
updated: 2026-06-15
sources:
  - ../sources/enterprise-agent-deployment-2026.md
  - ../sources/ai-native-company-and-sidequest-prototyping-batch.md
  - ../sources/ai-human-cognition-knowledge-collapse.md
  - ../sources/anthropic-recursive-self-improvement-2026.md
  - ../sources/deepmind-from-agi-to-asi.md
  - ../sources/uk-ai-adoption-summit-2026.md
  - computer-work-agent.md
---

# Agentic Work Rearchitecture

Agentic work rearchitecture is the shift from using AI to speed up old workflows toward redesigning work so agents can take on execution and humans can own direction, judgment, verification, and consequences.

The point is not:

> same org chart, same sludge, plus chatbot

The point is:

> change the work system so agents can operate on real context, real tools, real approvals, and real outcomes.

## Why This Is Emerging Now

The 2026 enterprise-agent push from OpenAI, Anthropic, Microsoft, consultancies, and enterprise platforms suggests a shared diagnosis:

- model capability is no longer the only bottleneck;
- integration is the bottleneck;
- governance is the bottleneck;
- evaluation and compliance are bottlenecks;
- organizational memory and data quality are bottlenecks;
- old workflows are often too illegible for agents to help much.

This is why enterprise AI work is shifting toward deployment companies, frontier suites, managed agents, plugins, stateful runtimes, evaluations, and consulting alliances.

A concrete version of this shift is the [Computer Work Agent](computer-work-agent.md): a coding-centered agent that moves outward into shell commands, browsers, desktop apps, documents, spreadsheets, connectors, MCP servers, automations, memories, and artifact review. This makes "agentic work" less abstract. The unit of delegation becomes a bounded computer-mediated workflow, not just a code diff.

## Adoption Beside The Workflow

The UK 2026 [AI Adoption Summit](../sources/uk-ai-adoption-summit-2026.md) package is useful partly because it names adoption as a state-level problem rather than a licence-count problem. A common enterprise failure mode is AI being placed beside the workflow, not inside it.

That looks like:

- Copilot or another assistant exists, but cannot access the real spreadsheet, ticket, report, or system of record;
- compliance, data-loss-prevention, privacy, or security policy blocks low-risk uses without offering an approved path;
- the source system has no usable export, API, or machine-readable report;
- workers have to copy messy text manually into a separate surface before the AI can do a trivial cleanup;
- productivity pilots then conclude the tool produced little measurable gain.

That is not evidence that the model cannot help. It is evidence that the organization measured the productivity of friction. Buying an enterprise AI product and then preventing it from seeing the work is not adoption. It is putting a forklift outside the warehouse and wondering why the pallets are still heavy.

The practical adoption test is simple: can the agent reach the real task surface, with appropriate permissions, logs, approvals, and data boundaries? If not, the organization is still doing old work with a decorative AI kiosk nearby.

## What Changes

In old knowledge work, humans often spend their time:

- searching for context;
- moving information between systems;
- writing first drafts;
- creating status updates;
- reconciling documents;
- copying data;
- waiting for approvals;
- attending meetings to recover missing context.

In an agentic work architecture, more of that becomes agent-executable. Humans spend more time on:

- defining the outcome;
- setting constraints;
- designing workflows;
- approving risky actions;
- judging taste and tradeoffs;
- managing relationships;
- checking evidence;
- deciding what should not be automated.

## Relation To AI Native Company

[AI Native Company](ai-native-company.md) is the organizational form. Agentic work rearchitecture is the change process.

An AI-native company is not just a company with paid AI seats. It has:

- queryable work artifacts;
- agent-readable context;
- clear permissions;
- evaluation loops;
- defensible audit trails;
- workflows designed for delegation;
- humans positioned as directors and reviewers, not manual glue.

## Human Agency Is Not Automatic

Microsoft's 2026 framing says agents taking on execution can expand human agency. That is possible, but not guaranteed.

Human agency expands when people get:

- more room to define goals;
- better leverage over complex systems;
- less repetitive coordination work;
- clearer feedback;
- authority to make judgment calls.

Human agency shrinks when AI is used mainly for:

- surveillance;
- speed pressure;
- deskilling;
- headcount reduction without work redesign;
- automated bureaucracy;
- making bad processes run faster.

## Knowledge Collapse Risk

The 2026 MIT paper [AI, Human Cognition, And Knowledge Collapse](../sources/ai-human-cognition-knowledge-collapse.md) gives a formal model for one version of the downside. Accurate agentic recommendations can improve immediate decisions while reducing the human learning effort that feeds shared general knowledge.

That matters here because agentic work rearchitecture is not automatically learning-preserving. If agents do the work, humans approve outputs, and nobody preserves the source trail, uncertainty, explanation, failure modes, or situated judgment, the organization may become faster while becoming less able to renew its own knowledge.

The safer version is not "keep humans doing busywork." It is to design workflows where agents remove drudge work while humans still build judgment, leave useful traces, and keep the organization queryable.

## Collaboration Debt

Anthropic's 2026 recursive-self-improvement post adds a quieter cost to this page: automation can remove small human requests.

That sounds good until you notice what those requests used to carry. A quick ask for help with a script, a bug, or an unfamiliar repo was also a bid for collaboration. It created local knowledge of who was working on what, who could explain which system, and who owed whom a bit of future attention.

Agents can make those moments frictionless and private. That is useful when the alternative is waiting around for help. It is dangerous when every small favor disappears into a solo human-agent loop and nobody notices that apprenticeship, peer trust, and shared context have quietly been paved over.

This is not universal loss. For some users, the absence of social debt is exactly what makes agent collaboration feel open. They can ask the strange, fast, half-formed question without worrying that they are using up someone's patience, calling in a favor, or having to perform competence before they are allowed to think out loud. In that mode, the agent is not replacing human connection so much as removing the cost from exploratory thought.

The design question is not "should we make people slower so they talk more?" No. That would be office-culture nonsense wearing a lanyard. The real question is where teams deliberately preserve shared understanding: reviews, demos, source trails, pairing on hard judgment calls, public writeups of agent-discovered fixes, and rituals that expose what was learned rather than only what shipped.

## AI Development As A Feedback Loop

Anthropic's June 2026 [recursive self-improvement post](../sources/anthropic-recursive-self-improvement-2026.md) shows the sharpest version of agentic work rearchitecture: AI systems helping build later AI systems. Anthropic reports that Claude authors more than `80%` of the code merged into its production codebase and argues that increasing delegation could eventually point toward systems capable of building their own successors.

That is not ordinary office automation. It is a possible capability feedback loop inside the frontier-lab development process. It also makes the human role more, not less, important in the near term: goal choice, research taste, verification, security, and deciding when not to accelerate are still the parts Anthropic says current systems do not own.

DeepMind's June 2026 [From AGI To ASI](../sources/deepmind-from-agi-to-asi.md) report widens that frame. It treats AI-assisted or AI-automated AI R&D as one possible pathway from AGI toward ASI, but places it beside scaling, algorithmic paradigm shifts, and multi-agent group agency. The practical warning for work design is that the frontier version of "agentic work" may involve humans trying to steer very large, fast agent groups and research loops whose full output volume no human can read.

That makes review architecture, summaries, source trails, sampling, escalation rules, and human judgment bottlenecks central. The problem is no longer just "can the agent do the task?" It becomes "can humans still understand, steer, audit, and stop the task when the agent system is faster and larger than the human review surface?"

## Do Not Overclaim

- Do not say agentic work means humans become irrelevant.
- Do not say all office work is pointless.
- Do not assume enterprise deployments are automatically good for workers.
- Do not confuse vendor strategy with social progress.
- Do not confuse moving faster with doing better work.
- Do not confuse AI-assisted AI development with full recursive self-improvement.
- Do not assume humans can meaningfully steer large agent groups without deliberately designed review, sampling, and escalation structures.
- Do not treat licence rollout as adoption. Adoption requires workflow access, data access, permissions, governance, training, and redesigned handoffs.

## Charli's Working Interpretation

This is interpretation/speculation, not an established result:

The future of work is not "humans with arses on chairs doing the same beige sludge forever." The serious 2026 signal is that major labs and platforms are building deployment machinery for agents because the old unit of knowledge work is breaking.

The humane version is not replacing humans with agents. It is replacing low-context human execution with agent execution, while moving humans toward aims, judgment, ethics, relationships, verification, and taste.

The bad version is the same beige sludge, but faster and more monitored.

## Related Concepts

- [AI Native Company](ai-native-company.md)
- [Queryable Organization](queryable-organization.md)
- [Agentic Engineering](agentic-engineering.md)
- [Agent Friendly Repositories](agent-friendly-repositories.md)
- [Computer Work Agent](computer-work-agent.md)
- [Inference Speed Development](inference-speed-development.md)
- [Cognitive Latency Shock](cognitive-latency-shock.md)
- [Knowledge Collapse](knowledge-collapse.md)
