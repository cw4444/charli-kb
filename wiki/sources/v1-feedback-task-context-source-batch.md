---
title: "V1 Feedback And Task Context Source Batch"
type: source
status: draft
created: 2026-06-16
updated: 2026-06-16
sources:
  - https://doi.org/10.1038/s41467-025-62279-8
  - https://doi.org/10.1038/s41467-023-43432-7
  - https://doi.org/10.1038/s41467-023-42441-w
---

# V1 Feedback And Task Context Source Batch

This source batch groups three open-access *Nature Communications* papers that sit beside Li et al.'s closed 2026 V1 internal-state paper. Together they support the same useful warning: primary visual cortex is not a neutral camera cable. V1 participates in feedback, task-adaptive routing, context representation and scene parsing.

## Xin, Yan and Li 2025

Ye Xin, Yin Yan and Wu Li published "A central and unified role of corticocortical feedback in parsing visual scenes" in *Nature Communications* on 2025-07-28.

In behaving macaques, the authors reversibly inactivated V4 using cooling while recording from retinotopically matched V1. Monkeys performed figure-ground tasks involving contours, orientation singletons and surfaces. V4 cooling impaired contour-detection behavior and altered late V1 contextual modulation.

The main claim is that V4-to-V1 feedback plays a central role in figure-ground organization across different grouping and segmentation processes. The feedback had dissociable facilitatory and inhibitory components, with different spatial distributions, timing and polarity. It operated largely independently of V1 neurons' local feature selectivity and mainly modified late response phases.

Access note: open access under CC BY-NC-ND 4.0. Source data are provided, while raw neural spiking datasets are available from the authors on request because of custom binary formats. The authors report no custom code central to the conclusions.

## Haimerl et al. 2023

Caroline Haimerl, Douglas A. Ruff, Marlene R. Cohen, Cristina Savin, Eero P. Simoncelli and colleagues published "Targeted V1 comodulation supports task-adaptive sensory decisions" in *Nature Communications* on 2023-11-30.

The paper studies monkeys performing a visual discrimination task. The authors report low-dimensional, rapidly fluctuating gain modulation in V1. This modulation was stronger in task-informative neurons, could be decoded after few training trials and was also present in simultaneously recorded MT units. Their hierarchical model suggests such labels can help downstream systems adapt readout even after intervening processing stages.

The useful bridge is that V1 population activity can carry task-targeted modulation that helps route useful sensory information for decisions. The point is not just "V1 encodes the image"; it is that V1 activity may also make task-relevant information easier for downstream circuits to find.

Access note: open access under CC BY 4.0. Some previously published data are available upon reasonable request; an example PLDS-model dataset is on figshare; modeling code is public on GitHub.

## Hajnal et al. 2023

Márton Albert Hajnal, Duy Tran, Michael Einstein, Mauricio Vallejo Martelo, Karen Safaryan, Pierre-Olivier Polack, Peyman Golshani, Gergő Orbán and colleagues published "Continuous multiplexed population representations of task context in the mouse primary visual cortex" in *Nature Communications* on 2023-10-21.

The authors trained mice on a context-switching cross-modal decision task in which performance depended on inferring task context. They found that V1 represented task context in a behaviorally relevant way, independent of movement. Crucially, visual and context signals were multiplexed into orthogonal population subspaces. Auditory and choice signals were also multiplexed separately.

The useful bridge is that V1 can carry visual, contextual, auditory and choice-related variables without simply overwriting the visual representation. Mouse V1 is not a miniature human mind, but it is a good warning against treating primary visual cortex as a pure visual-feature stage.

Access note: open access under CC BY 4.0. Behavioral, spike-sorted electrophysiology and movement data are available on Zenodo; behavior and analysis code are public on GitHub.

## Why This Batch Matters

Placed beside [Li et al. - Internal States And V1 Behavior Covariation](li-internal-states-v1-behavior.md), these papers make a clean active-perception stack:

- V1 can be modulated by internal state and gain.
- V1 can be shaped by feedback from higher visual cortex during scene parsing.
- V1 can carry task-targeted comodulation that helps downstream readout.
- V1 can multiplex visual input with task context, auditory signals and choice variables.

That does not mean V1 invents reality. It means early visual processing is already embedded in task, context, feedback and state. The world arrives, but it arrives through a system that is actively routing, weighting and organizing it.

## Caveats

- Two papers use macaques and one uses mice; species and task boundaries matter.
- V1 feedback and context effects do not mean perception is arbitrary.
- A task-context signal in mouse V1 is not a human self-model.
- Modulation, feedback and multiplexing are circuit/computation claims, not proof of conscious visual experience.
- Licence details differ: Xin et al. 2025 is CC BY-NC-ND, while Haimerl et al. 2023 and Hajnal et al. 2023 are CC BY.

## Links

- Xin et al. 2025: https://doi.org/10.1038/s41467-025-62279-8
- Haimerl et al. 2023: https://doi.org/10.1038/s41467-023-43432-7
- Haimerl et al. code: https://github.com/CarolineHaimerl27/modulator_guided_decoding
- Hajnal et al. 2023: https://doi.org/10.1038/s41467-023-42441-w
- Hajnal et al. data: https://zenodo.org/record/7900224
- Hajnal et al. behavior code: https://github.com/golshanilab/AttentionTask.git
- Hajnal et al. analysis code: https://github.com/CSNLWigner/mouse-v1-context
- Hajnal et al. movement analysis code: https://github.com/CSNLWigner/mouse-v1-context-movement
