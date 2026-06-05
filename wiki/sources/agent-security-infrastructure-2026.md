---
title: "Agent Security Infrastructure 2026"
type: source
status: draft
created: 2026-06-04
updated: 2026-06-05
sources:
  - "GitHub: Cloud and local sandboxes for GitHub Copilot now in public preview, 2026-06-02"
  - "Microsoft Foundry: Build agents you can trust across any framework with open evals and a control standard, 2026-06-02"
  - "Anthropic: What we learned mapping a year's worth of AI-enabled cyber threats, 2026-06-03"
  - "Anthropic: Expanding Project Glasswing, 2026-06-02"
  - "Microsoft Security Blog: Updating the taxonomy of failure modes in agentic AI systems, 2026-06-04"
---

# Agent Security Infrastructure 2026

By June 2026, agent security was becoming a product and standards layer rather than a footnote attached to model capability.

The durable pattern is straightforward: agents can run tools, execute commands, modify files, call other systems, and chain decisions. That makes isolation, policy, evaluation, observability, and human control part of the agent itself.

## Secure Execution

GitHub moved cloud and local sandboxes for Copilot into public preview on 2026-06-02.

- local Copilot shell execution can run with restricted filesystem, network, and system access;
- organizations can centrally configure local sandbox policy;
- cloud sessions run in isolated, ephemeral Linux environments;
- cloud sessions inherit existing Copilot cloud-agent policies.

This is a useful product-level acknowledgement that agentic coding needs an execution boundary, not merely a polite prompt asking the model to behave.

Source:

- [GitHub: Cloud and local sandboxes for GitHub Copilot now in public preview](https://github.blog/changelog/2026-06-02-cloud-and-local-sandboxes-for-github-copilot-now-in-public-preview/)

## Policy, Evaluation, And Runtime Controls

Microsoft announced an open trust stack for agents at Build 2026.

- **ASSERT** is an open-source framework that turns organizational policies into agent-specific evaluation scenarios.
- **Agent Control Specification (ACS)** is a portable runtime-control specification covering input, model, state, tool-execution, and output checkpoints.
- Microsoft also described tracing, evaluations, guardrail setup, data protection, and production observability as parts of the same operating loop.

The important move is from generic safety language toward versionable, inspectable controls and tests that can travel across frameworks.

Source:

- [Microsoft Foundry: Build agents you can trust across any framework with open evals and a control standard](https://devblogs.microsoft.com/foundry/build-2026-open-trust-stack-ai-agents/)

## Agent Failure Modes Become System-Level

On 2026-06-04, the Microsoft AI Red Team published an updated taxonomy of failure modes in agentic AI systems, based on a year of red-team work against deployed systems.

The update matters because it moves the risk frame beyond ordinary prompt injection. Microsoft added seven new categories:

- agentic supply-chain compromise;
- goal hijacking;
- inter-agent trust escalation;
- computer-use-agent visual attacks;
- session context contamination;
- MCP / plugin abuse;
- capability or architecture disclosure.

The security shape is getting less cute. Agents now ingest plugin registries, MCP servers, prompt templates, tool descriptions, and third-party integrations as operational inputs. Those inputs can become a supply chain even when the payload is natural language rather than executable code.

Microsoft also says several red-team engagements showed zero-click end-to-end chains from external input to high-impact outcomes such as exfiltration or lateral movement. That does not mean every agent is doomed. It does mean model-level evaluation is not enough when the deployed system includes tools, persistent sessions, memory, approvals, subagents, UI surfaces, and external content.

Source:

- [Microsoft Security Blog: Updating the taxonomy of failure modes in agentic AI systems](https://www.microsoft.com/en-us/security/blog/2026/06/04/updating-taxonomy-failure-modes-agentic-ai-systems-year-red-teaming-taught-us/)

## Offensive Cyber Pressure

Anthropic published an analysis of 832 accounts banned for malicious cyber activity between March 2025 and March 2026.

Anthropic says AI use shifted deeper into post-compromise activity, the share of actors scored medium risk or higher rose from 33% in the first six months to 56% in the second, and higher-risk actors increasingly built scaffolding that let models chain attack stages with minimal human input.

Anthropic's sharper claim is that MITRE ATT&CK does not yet fully capture agentic orchestration: sequential action, real-time decision-making, and execution without continuous human intervention.

Source:

- [Anthropic: What we learned mapping a year's worth of AI-enabled cyber threats](https://www.anthropic.com/news/AI-enabled-cyber-threats-mitre-attack)

## Defensive Cyber Pressure

Anthropic also expanded Project Glasswing from roughly 50 initial partners to about 150 organizations across more than 15 countries, including power, water, healthcare, communications, hardware, and shared software vendors.

This sits beside the offensive-pressure story. Frontier models are being pushed into both vulnerability discovery and attacker workflows, so disclosure, patching, safeguards, standards, and execution controls are becoming one connected capacity problem.

Source:

- [Anthropic: Expanding Project Glasswing](https://www.anthropic.com/news/expanding-project-glasswing)

## Do Not Overclaim

- Do not treat a sandbox as complete safety. Policy configuration, credentials, network access, tool design, and escape vulnerabilities still matter.
- Do not treat open specifications as adopted standards merely because Microsoft wants broad adoption.
- Do not treat the updated Microsoft taxonomy as proof of universal compromise. It is a red-team-derived threat model and evidence summary, not a census of all deployments.
- Do not reduce agent security to prompt injection. MCP/plugin trust, session history, visual computer-use surfaces, approval design, agent identity, and tool provenance are now part of the security boundary.
- Do not treat Anthropic's banned-account dataset as a census of all AI-enabled cyber activity.
- Do not confuse defensive capability with harmless capability. The same model skills can matter offensively.
- Do not assume controls replace human accountability for high-impact agent actions.

## Related Pages

- [AI And Agents 2026 Timeline](../timelines/ai-and-agents-2026.md)
- [Current AI Agent Landscape 2026](current-ai-agent-landscape-2026.md)
- [White House Advanced AI Innovation And Security Order](white-house-ai-innovation-security-order.md)
- [What Can AI Agents Do For Normal Tired Humans?](../questions/what-can-ai-agents-do-for-normal-tired-humans.md)
