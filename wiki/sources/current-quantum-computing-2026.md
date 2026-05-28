---
title: "Current Quantum Computing 2026"
type: source
status: draft
created: 2026-05-28
updated: 2026-05-28
source_type: public-source-batch
primary_sources:
  - "Google Quantum AI, Meet Willow, our state-of-the-art quantum chip, 2024-12-09, https://blog.google/technology/research/google-willow-quantum-chip/"
  - "Google Quantum AI and collaborators, Quantum error correction below the surface code threshold, Nature, 2024-12-09, https://www.nature.com/articles/s41586-024-08449-y"
  - "Microsoft, Majorana 1: The world's first quantum processor powered by topological qubits, 2025-02-19, https://azure.microsoft.com/en-us/blog/quantum/2025/02/19/majorana-1-the-worlds-first-quantum-processor-powered-by-topological-qubits/"
  - "Microsoft and collaborators, Interferometric single-shot parity measurement in InAs-Al hybrid devices, Nature, 2025-02-19, https://www.nature.com/articles/s41586-024-08445-2"
  - "Henry F. Legg, Comment on InAs-Al hybrid devices passing the topological gap protocol, arXiv, 2025-02-26, https://arxiv.org/abs/2502.19560"
  - "Henry F. Legg, Comment on Interferometric single-shot parity measurement in InAs-Al hybrid devices, arXiv, 2025-03-11, https://arxiv.org/abs/2503.08944"
  - "IBM, The next era of quantum computing is here: IBM Quantum System Two, 2023-12-04, https://www.ibm.com/quantum/blog/quantum-roadmap-2033"
  - "IBM, IBM charts path to practical quantum advantage, 2025-06-10, https://www.ibm.com/quantum/blog/large-scale-ftqc"
  - "IBM, Quantum-centric supercomputing: The next wave of computing, 2026, https://www.ibm.com/quantum/blog/quantum-centric-supercomputing"
  - "IBM Quantum, IBM Quantum roadmap, accessed 2026-05-28, https://www.ibm.com/roadmaps/quantum"
  - "DARPA, US2QC program information, accessed 2026-05-28, https://www.darpa.mil/research/programs/underexplored-systems-for-utility-scale-quantum-computing"
sources:
  - https://blog.google/technology/research/google-willow-quantum-chip/
  - https://www.nature.com/articles/s41586-024-08449-y
  - https://azure.microsoft.com/en-us/blog/quantum/2025/02/19/majorana-1-the-worlds-first-quantum-processor-powered-by-topological-qubits/
  - https://www.nature.com/articles/s41586-024-08445-2
  - https://arxiv.org/abs/2502.19560
  - https://arxiv.org/abs/2503.08944
  - https://www.ibm.com/quantum/blog/quantum-roadmap-2033
  - https://www.ibm.com/quantum/blog/large-scale-ftqc
  - https://www.ibm.com/quantum/blog/quantum-centric-supercomputing
  - https://www.ibm.com/roadmaps/quantum
  - https://www.darpa.mil/research/programs/underexplored-systems-for-utility-scale-quantum-computing
---

# Current Quantum Computing 2026

## Summary

The most useful 2024-2026 quantum-computing story is not raw qubit count. It is the move from impressive but noisy physical qubits toward logical qubits, error correction, and roadmaps for fault-tolerant machines.

Google, Microsoft, and IBM are pushing different bets:

- Google is showing strong surface-code error-correction progress with Willow.
- Microsoft is betting on topological qubits and Majorana-based hardware, with a bigger uncertainty penalty.
- IBM is building a public industrial roadmap toward larger error-corrected systems and quantum-centric supercomputing.

The careful summary: quantum computing is advancing, but useful fault-tolerant quantum computing is still an engineering program, not a solved product.

## Primary-Source Claims

### Google Willow

Google announced Willow in December 2024. Hartmut Neven framed it around two claims: a benchmark result that would take an impractically long time on a leading classical supercomputer, and a more important error-correction result where larger surface-code patches performed better than smaller ones.

The Nature paper is the stronger source for this wiki. It reports quantum error correction below the surface-code threshold using superconducting qubits, meaning that scaling the code distance reduced logical error rates rather than making the system worse. That is the serious bit. The benchmark headline is flashy; below-threshold error correction is the road-to-usefulness signal.

### Microsoft Majorana 1

Microsoft announced Majorana 1 in February 2025 as a topological-qubit processor based on a claimed topoconductor platform. The official pitch is that topological qubits could make error correction far cheaper if the hardware works as hoped.

The Nature paper reports interferometric single-shot parity measurement in InAs-Al hybrid devices. That supports part of Microsoft's topological-qubit program, but it is not the same as demonstrating a large, useful, fault-tolerant quantum computer. Microsoft's framing is strategically important and scientifically interesting, but it needs the harsh caveat: this is exactly where "trust me bro" instincts are useful. Topological quantum computing has a history of difficult claims, retractions, and replication pressure.

Henry F. Legg published two 2025 arXiv comments that sharpen the caveat. The first challenges Microsoft's 2023 topological gap protocol, arguing that the protocol lacks stable definitions of "gap" and "topological" and can depend heavily on parameter choices such as magnetic-field range, bias-voltage range, data resolution, and cutter-voltage pairs. The second targets the 2025 Nature parity-readout paper more directly, arguing that the same protocol can classify the relevant regions differently depending on parameters and that public conductance data do not show a clear superconducting gap in the regions where parity readout occurred.

This does not by itself prove Microsoft is wrong. It does mean the Microsoft claim is contested at the level that matters: the diagnostic machinery used to say the device is in the right topological regime.

### IBM Roadmap

IBM's public roadmap matters because it gives the field an industrial structure: modular systems, quantum-centric supercomputing, middleware, error mitigation, and a path toward larger error-corrected machines.

IBM's 2025 roadmap update introduced named systems such as Loon, Kookaburra, Cockatoo, and Starling. Starling is framed as a planned fault-tolerant system for 2029, with IBM claiming it will be able to run about 100 million quantum gates on 200 logical qubits. IBM also frames Nighthawk as a nearer-term processor aimed at larger quantum circuits before full fault tolerance.

IBM's 2026 quantum-centric-supercomputing framing adds the classical integration layer: quantum machines are expected to sit beside CPUs, GPUs, and HPC systems rather than replace ordinary computers. That matters because useful quantum computing will likely look like specialized accelerators embedded in larger workflows, not a shiny standalone box that fixes everything before lunch.

This does not prove IBM will hit the dates. It does show where IBM thinks practical advantage comes from: not one magical chip, but architecture, interconnects, software, error correction, and classical/HPC integration.

### DARPA And Independent Validation

DARPA's US2QC program is useful as a reality check because it is explicitly about evaluating underexplored paths to utility-scale quantum computing. Microsoft and other hardware approaches have been associated with this kind of validation pathway. For this wiki, that matters because company blogs alone are commercial documents. Independent stress-testing is the adult supervision.

## Useful Synthesis

Quantum computing currently looks less like a single race and more like several incompatible engineering bets:

- superconducting circuits: Google, IBM, and others;
- topological qubits: Microsoft;
- trapped ions: Quantinuum and IonQ-style approaches;
- neutral atoms: Atom Computing, QuEra, Pasqal, and academic groups;
- photonics: PsiQuantum and Xanadu-style approaches.

The shared problem is error. Physical qubits are fragile. A useful machine needs logical qubits protected by error correction, and logical qubits require many physical qubits plus fast control, calibration, decoding, and classical integration.

That makes this a good bridge topic for the wiki. Quantum foundations ask what quantum theory means. Quantum computing asks what quantum theory can be engineered to do.

## Do Not Overclaim

- Do not treat quantum computing as proof of many-worlds, observer-dependent reality, or consciousness-linked physics.
- Do not treat benchmark supremacy claims as the same thing as practical usefulness.
- Do not treat Microsoft's topological-qubit announcement as settled until the hardware claims survive independent validation and scaling.
- Do not reduce the Microsoft criticism to vibes. Legg's critique is specifically about the reliability of the topological gap protocol and the evidence for a superconducting/topological gap in the relevant device regions.
- Do not treat IBM's roadmap as a guarantee; it is a public engineering plan.
- Do not say "quantum computers break all encryption now." Useful cryptanalytic quantum computers remain a future threat, though serious enough for post-quantum cryptography migration.
- Do not collapse quantum foundations and quantum computing into the same topic. They share formal machinery, but the questions are different.

## Useful For

- [Fault-Tolerant Quantum Computing](../concepts/fault-tolerant-quantum-computing.md)
- [Research - Quantum Computing 2026](../questions/research-quantum-computing-2026.md)
- [Feynman, Calculation, and Reality Stories](../../themes/feynman-calculation-and-reality-stories.md)
- [Mechanical World Models](../concepts/mechanical-world-models.md)
