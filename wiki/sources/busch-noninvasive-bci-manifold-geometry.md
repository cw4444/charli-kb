---
title: "Busch et al. - Noninvasive BCI Learning And Manifold Geometry"
type: source
status: draft
created: 2026-06-13
updated: 2026-06-13
source_type: journal-article
authors:
  - Erica L. Busch
  - E. Chandra Fincke
  - Guillaume Lajoie
  - Smita Krishnaswamy
  - Nicholas B. Turk-Browne
primary_source: "Busch et al., Nature Neuroscience, 2026, Human learning of noninvasive brain-computer interfaces via manifold geometry, https://doi.org/10.1038/s41593-026-02311-2"
sources:
  - "Nature ReadCube share link and article metadata/abstract, https://rdcu.be/fob3N, accessed 2026-06-13"
  - "Crossref metadata for DOI 10.1038/s41593-026-02311-2, accessed 2026-06-13"
  - "OpenAlex metadata for DOI 10.1038/s41593-026-02311-2, accessed 2026-06-13"
  - "Dryad dataset DOI 10.5061/dryad.9cnp5hr0w, accessed 2026-06-13"
  - "GitHub repositories avatarRT_task, avatarRT_analysis, MRAE, and KrishnaswamyLab/TPHATE; Zenodo DOI 10.5281/zenodo.7637522, accessed 2026-06-13"
---

# Busch et al. - Noninvasive BCI Learning And Manifold Geometry

Erica L. Busch, E. Chandra Fincke, Guillaume Lajoie, Smita Krishnaswamy, and Nicholas B. Turk-Browne published [Human learning of noninvasive brain-computer interfaces via manifold geometry](https://doi.org/10.1038/s41593-026-02311-2) in *Nature Neuroscience* on 2026-06-09.

The paper matters here because it turns representational geometry into an interface-design constraint. The question is not only whether brain activity contains decodable structure. It is whether a person can learn to control a brain-computer interface when the control mapping follows, or violates, the geometry of their own neural activity.

## Core Claim

Participants used real-time fMRI neurofeedback to control an avatar in a virtual navigation task by modulating activity in brain regions associated with spatial navigation.

The authors extracted each participant's intrinsic neural manifold using data-diffusion methods and then perturbed the mapping between fMRI activity patterns and avatar movement. Participants regained control when the new mapping used high-variance directions within the intrinsic manifold. They did not successfully relearn control when the mapping was outside that manifold.

The durable point: BCI learning was constrained by the geometry of reachable brain states. The interface worked better when the control axes were aligned with patterns the brain could naturally vary, rather than arbitrary directions imposed from outside.

## Why It Matters

This is a useful bridge between brain-computer interfaces, neurofeedback, and [Representational Geometry](../concepts/representational-geometry.md).

The study suggests that a noninvasive BCI should not merely decode whatever signal is available. It should also respect the user's existing neural-state geometry. In plain English: train the interface around control directions the person can actually reach, not around axes that look mathematically convenient and then ask the brain to become a different machine for your software. That usually goes about as well as expected.

For this wiki, the clean idea is:

- geometry can be descriptive, showing how brain states are organized;
- geometry can be predictive, showing which remappings are learnable;
- geometry can be practical, shaping how a neurotechnology should be designed.

## Code And Data Trail

The article reports several public artifacts:

- [Dryad dataset](https://doi.org/10.5061/dryad.9cnp5hr0w): public data/code record for the paper, published 2026-04-01 and marked CC0. The dataset is large, including an approximately 38.82 GB subject-data archive plus a README.
- [`ericabusch/avatarRT_task`](https://github.com/ericabusch/avatarRT_task): task code for the avatar real-time task. The article describes the task as programmed in C# for Unity 2019.4.12f1. GitHub did not report a declared licence in this pass.
- [`ericabusch/avatarRT_analysis`](https://github.com/ericabusch/avatarRT_analysis): experiment, preprocessing, and analysis scripts. GitHub did not report a declared licence in this pass.
- [`ericabusch/MRAE`](https://github.com/ericabusch/MRAE): manifold-regularized autoencoder code for fMRI time-series data. GitHub did not report a declared licence in this pass.
- [`KrishnaswamyLab/TPHATE`](https://github.com/KrishnaswamyLab/TPHATE): T-PHATE package. Zenodo records the archived software under [DOI 10.5281/zenodo.7637522](https://doi.org/10.5281/zenodo.7637522), while the GitHub repository contains a custom non-commercial Yale licence. Reuse should respect the stricter visible licence unless clarified.
- [rtCloud](https://rt-cloud.readthedocs.io/): open-source real-time fMRI framework used for the experiment.

## Access Note

The Nature sharing link `https://rdcu.be/fob3N` worked for article metadata, abstract, references, and ReadCube-style access. It is not the same as open access.

OpenAlex marked the article closed, and Crossref licence metadata showed Springer Nature text-and-data-mining terms rather than a permissive open-access licence. The article page states an exclusive licence to Springer Nature America, Inc. The wiki therefore uses public metadata, abstract-level claims, and linked code/data records, not copied article text.

## Do Not Overclaim

- This is a real-time fMRI study, not a consumer wearable BCI.
- fMRI is expensive, slow, and infrastructure-heavy.
- Controlling an avatar through spatial-navigation regions is not mind reading.
- The study supports a constrained learning claim for this BCI task; it does not prove that all human learning is governed by one simple manifold.
- A useful neural manifold is not a soul map, a telepathy channel, or a shortcut to ignoring subject-specific training.
- Public code visibility is not the same as permission to reuse code; licences still matter, because lawyers need hobbies too.

## Related Pages

- [Representational Geometry](../concepts/representational-geometry.md)
- [Representational Geometry In Brains And LLMs](representational-geometry-brains-and-llms.md)
- [Neuroscience](../../themes/neuroscience/overview.md)
