---
title: "Research - Quantum Computing 2026"
type: question
status: draft
created: 2026-05-28
updated: 2026-05-28
question: "What are the latest useful developments in quantum computing, especially Google, Microsoft, and IBM?"
sources:
  - ../sources/current-quantum-computing-2026.md
  - ../concepts/fault-tolerant-quantum-computing.md
---

# Research - Quantum Computing 2026

## Overview

The latest useful quantum-computing story is a shift from "can we make a quantum device do something weird?" to "can we make enough reliable logical qubits to run useful computations?"

Google, Microsoft, and IBM are all relevant, but they should not be read as doing the same thing.

Google's Willow result is the cleanest recent error-correction signal. Microsoft is making a high-upside topological-qubit bet that still needs independent validation. IBM is publishing the clearest industrial roadmap toward fault-tolerant systems and quantum-centric supercomputing.

## Key Findings

### 1. Google Willow is important because of error correction

Google's December 2024 Willow announcement had a flashy benchmark claim, but the durable part is the error-correction result.

The primary Nature paper reports below-threshold quantum error correction using the surface code. In plain English: when Google made the encoded system bigger, the logical error rate went down. That is the direction needed for fault-tolerant machines.

This does not mean Google has delivered a useful general-purpose quantum computer. It means one of the most important scaling tests moved in the right direction.

### 2. Microsoft's Majorana claim is interesting but should stay under suspicion

Microsoft's February 2025 Majorana 1 announcement says the company has built a topological-qubit processor based on a topoconductor platform.

If topological qubits work at scale, they could reduce error-correction overhead. That is the attraction.

The caution is equally important. The Nature paper supports a piece of the measurement and device story, not a finished utility-scale computer. Topological quantum computing has a long history of hard-to-verify claims. The right stance is not dismissal, but raised-eyebrow patience: show the scaling, show the validation, show the logical qubits.

### 3. IBM is trying to make quantum computing look like infrastructure

IBM's roadmap is less cinematic but more system-shaped.

IBM is aiming at modular systems, larger processors, quantum-centric supercomputing, and eventually fault-tolerant machines. Its public roadmap names systems such as Nighthawk, Loon, Kookaburra, Cockatoo, and Starling. Starling is framed as the late-decade fault-tolerant target.

The important IBM signal is that practical quantum computing is not one chip. It is processors, cryogenics, control systems, error correction, compilers, classical compute, and workflows. IBM's 2026 quantum-centric-supercomputing framing makes that explicit: quantum systems are expected to work alongside CPUs, GPUs, and HPC infrastructure.

### 4. The field is broader than Google, Microsoft, and IBM

Trapped-ion, neutral-atom, and photonic systems are also live contenders. The hardware race is still plural.

That matters because "quantum computing" is not one technology. It is a family of attempts to make controllable quantum systems compute reliably.

### 5. The best near-term test is logical performance

The useful questions are:

- How many logical qubits exist?
- What is the logical error rate?
- How many logical gates can be run?
- Can the architecture scale?
- Has an independent group validated the core claim?
- Is the benchmark tied to a real use case?

If a press release dodges those questions, lovely, into the bin with it.

## Working Interpretation

Quantum computing now belongs in this wiki because it sits between the existing quantum-foundations lane and the mechanical-world-models lane.

The foundations pages ask what quantum theory means. Quantum computing asks what quantum theory can be made to do when humans build machines around it.

The current sober view:

- Google has the strongest recent public error-correction milestone.
- Microsoft has the most dramatic high-risk hardware bet.
- IBM has the clearest public infrastructure roadmap.
- Nobody has yet delivered the boring, undeniable thing: a broadly useful fault-tolerant quantum computer.

## Do Not Overclaim

- Do not treat Willow as proof that useful quantum computing has arrived.
- Do not treat Majorana 1 as settled fact just because Microsoft said it loudly.
- Do not treat IBM's roadmap dates as destiny.
- Do not treat quantum computing as evidence for any one interpretation of quantum mechanics.
- Do not use this as proof of consciousness, many-worlds, manifestation, or "the universe is a computer" sludge.

## Sources

- [Current Quantum Computing 2026](../sources/current-quantum-computing-2026.md)
- [Fault-Tolerant Quantum Computing](../concepts/fault-tolerant-quantum-computing.md)

## Open Questions

- Which hardware route will produce the first independently convincing large logical-qubit system?
- Will topological qubits scale, or will the proof burden eat the advantage?
- Which applications will matter first: chemistry, materials, cryptanalysis, optimization, or scientific simulation?
- How should this wiki connect engineered quantum computation to observer-dependent-reality pages without muddling foundations and hardware?
