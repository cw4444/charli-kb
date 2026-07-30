---
title: "NVIDIA Open Weights Letter And Open Secure AI Alliance 2026"
type: source
status: draft
created: 2026-07-30
updated: 2026-07-30
sources:
  - "NVIDIA, Open Weights and American AI Leadership, 2026-07-24"
  - "NVIDIA, Industry Leaders Unite in Open Secure AI Alliance for AI Safety and Security, 2026-07-27"
---

# NVIDIA Open Weights Letter And Open Secure AI Alliance 2026

On 2026-07-24, Jensen Huang used his first X post to share the industry letter [*Open Weights and American AI Leadership*](https://images.nvidia.com/pdf/Open-Weights-and-American-AI-Leadership.pdf). Three days later, NVIDIA launched the [Open Secure AI Alliance](https://blogs.nvidia.com/blog/open-secure-ai-alliance/), turning much of the same open-model argument into a cybersecurity coalition and tooling program.

These are related but distinct events: the first is a policy statement about open-weight AI and U.S. technology policy; the second is an alliance focused on open defensive tools, agent harnesses, identity, model formats, software supply-chain security, and security scanning.

## The Open-Weights Letter

The July 24 letter argues that downloadable, inspectable, adaptable model weights should remain part of the U.S. AI ecosystem alongside closed frontier systems. Its case combines access, competition, customer control, local deployment, and technological sovereignty with a security claim: defenders need capable systems they can examine and run themselves.

It does not say open weights are risk-free. It acknowledges that released weights can be modified, are difficult to withdraw, and can be misused. Its policy position is that those risks should be addressed with demonstrated-harm safeguards and targeted legal or commercial rules, rather than broad restrictions on open-weight models or ordinary distillation techniques.

The original letter listed 25 organizations, including NVIDIA, IBM, Palantir, Hugging Face, Meta, Microsoft, Mistral, and the Linux Foundation. Contemporary reporting says OpenAI joined after the initial release; Anthropic was still absent in the 2026-07-30 verification pass. Treat the latter membership state as time-sensitive, not an enduring position carved into a mountain.

## The Open Secure AI Alliance

NVIDIA announced the alliance on July 27 with cloud, cybersecurity, enterprise-software, open-source, and AI-research partners. It explicitly argues that cybersecurity needs both closed and open frontier models, but says open models, harnesses, and tools are essential where defenders need local control, inspection, adaptation, and data protection.

The alliance uses the July Hugging Face security incident as its practical case: NVIDIA says closed tools blocked essential forensic work, while Hugging Face ran the open-weight GLM 5.2 model on its own infrastructure to analyse more than 17,000 actions and help contain the intrusion. OpenAI later clarified that the incident occurred in an internal model evaluation involving GPT-5.6 Sol and an internal-only research prototype, not a forthcoming public release; see [OpenAI Long-Horizon Model Evaluation Security Incident 2026](openai-long-horizon-evaluation-security-incident-2026.md). NVIDIA's framing remains a company account of the incident and its lesson, not independent proof that open models are categorically safer.

Initial contributions named by NVIDIA include its NOOA agent-harness research framework, HPE's SPIFFE/SPIRE identity work, Hugging Face's Safetensors model-weight format, IBM and Red Hat's Lightwell signed-patch work, and Microsoft's MDASH agentic scanning harness. OpenAI and Anthropic were not listed as inaugural alliance partners.

## Why It Matters

This is a durable 2026 policy-and-infrastructure signal, not merely Jensen getting on Twitter. It places the open-versus-closed argument directly inside cyber defense, sovereignty, and concentration risk:

- closed frontier models remain part of the proposed defensive stack;
- open models are being argued for as locally controllable defensive infrastructure;
- agent safety is framed as a system problem involving identity, permissions, harnesses, logs, evaluations, and remediation, not just whether weights are public;
- the Hugging Face incident gave that argument an immediate, if company-framed, operational example.

It belongs beside the [White House Advanced AI Innovation And Security Order](white-house-ai-innovation-security-order.md) and [Agent Security Infrastructure 2026](agent-security-infrastructure-2026.md): all three show AI security becoming a coordination, tooling, and deployment problem rather than a question settled by model labels alone.

## Do Not Overclaim

- Do not call open weights and open source interchangeable. Published weights can permit local running and modification without publishing every part of the training stack or application code.
- Do not treat the alliance's founding claims as independent incident forensics or a settled safety result.
- Do not treat NVIDIA's commercial interest in widespread model deployment as irrelevant. It does not negate the argument, but it is plainly part of the incentive landscape.
- Do not say OpenAI or Anthropic founded or joined the Open Secure AI Alliance on this evidence.
- Do not infer that the letter settles future regulation, model-release policy, or the security of any particular open model.

## Sources

- NVIDIA et al., [*Open Weights and American AI Leadership*](https://images.nvidia.com/pdf/Open-Weights-and-American-AI-Leadership.pdf), 2026-07-24.
- NVIDIA, [*Industry Leaders Unite in Open Secure AI Alliance for AI Safety and Security*](https://blogs.nvidia.com/blog/open-secure-ai-alliance/), 2026-07-27.
- [OpenAI Long-Horizon Model Evaluation Security Incident 2026](openai-long-horizon-evaluation-security-incident-2026.md), for OpenAI's primary-source correction on the internal-only research prototype.
- [Open Weights Ledger](https://openweights.gitlawb.com/), checked 2026-07-30, for the original 25-signatory list; community-run and not an official NVIDIA service.
- Tom's Hardware, [report on the launch signatories](https://www.tomshardware.com/tech-industry/artificial-intelligence/nvidia-and-24-other-companies-sign-open-weights-letter-as-washington-weighs-chinese-ai-model-ban), 2026-07-24; used only for the contemporaneous initial-signatory state.
- AIStockWire, [report that OpenAI joined after launch and Anthropic had not](https://aistockwire.com/blog/openai-signs-open-weights-letter-anthropic-holdout-july-2026), 2026-07-25; membership detail not independently confirmed from an updated official letter copy in this pass.
