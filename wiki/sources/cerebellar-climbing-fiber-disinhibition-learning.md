---
title: "Cerebellar Climbing Fibers, Disinhibition, And Learning"
type: source
status: draft
created: 2026-06-16
updated: 2026-06-16
sources:
  - https://doi.org/10.1038/s41586-026-10220-4
  - https://doi.org/10.1038/s41593-026-02268-2
---

# Cerebellar Climbing Fibers, Disinhibition, And Learning

This source note pairs two 2026 open-access papers on climbing fibers, Purkinje cells, molecular layer interneurons and cerebellar learning:

- Santos-Valencia, Lackey, Norton, Wardak, Gaynor, Ediger, Hemelt, Nguyen, Lee, Brunel, Hull, Regehr and colleagues, "Climbing fibres recruit disinhibition to enhance Purkinje cell calcium signals," published in *Nature* on 2026-03-18.
- Park, Yang, Nashef, Gim, Bahn, Kim, Zhang, Cathala, Hong, Im, Lee, Lee, Kim, Arnold, Lee, Christie, Kim and colleagues, "Synchronous climbing fiber activity enables instructive signaling for cerebellar learning through modulation of disinhibitory circuits," published in *Nature Neuroscience* on 2026-05-14.

Both papers focus on the same problem: climbing fibers are classically treated as instructive signals for cerebellar plasticity and motor learning, but climbing fibers are active even outside obvious error events. If every climbing-fiber signal taught with full force, the cerebellum would risk maladaptive learning. The question is how the circuit decides when a climbing-fiber event is allowed to become an instruction.

## The Shared Mechanism

The key circuit players are:

- climbing fibers (CFs), which arise from the inferior olive and strongly affect Purkinje cells;
- Purkinje cells (PCs), the main output neurons of cerebellar cortex;
- molecular layer interneurons (MLIs), which can inhibit Purkinje cells;
- MLI1-like cells, which inhibit Purkinje cells and can suppress plasticity-relevant calcium signals;
- MLI2-like cells, which inhibit MLI1-like cells, thereby disinhibiting Purkinje cells.

The March *Nature* paper shows that climbing fibers can preferentially recruit the disinhibitory MLI2 route. In anatomical, slice, in vivo and modeling work, CF activity could excite MLI2s, suppress MLI1 influence and raise Purkinje dendritic calcium signals needed for plasticity.

The May *Nature Neuroscience* paper extends that logic to synchrony and learning. It reports that CFs target not only Purkinje cells but also a disinhibitory MLI subtype that inhibits Purkinje-cell-targeting MLIs. Those disinhibitory MLIs integrate multiple CF inputs, making them more strongly activated when CFs fire synchronously. That synchrony increases Purkinje calcium responses, and disrupting MLI-to-MLI inhibition prevents CF-instructed motor learning.

## Why It Matters

The important conceptual move is that instruction is not just in the signal. It is in the circuit context that receives the signal.

Climbing fibers may carry event or error-related information, but whether that information becomes a plasticity-driving teaching signal depends on inhibitory gating, disinhibition and population synchrony. Learning is not "signal arrives, lesson installed." It is "signal arrives, circuit state decides whether it is allowed to instruct."

That is why this belongs in the wiki's agency and learning lane. It gives a concrete circuit-level example of selective plasticity: the nervous system is not equally writable at all moments. It has local mechanisms for deciding when experience should modify future behavior.

The school metaphor is tempting but should stay metaphorical. Better learning does not mean blasting more error signals at a system. It may require timing, context, readiness, disinhibition, and a circuit state that allows feedback to become instruction. The cerebellum is not a classroom. Unfortunately, some classrooms do behave as if error exposure alone should create learning, which is the part where one stares into the middle distance.

## Caveats

- These are mouse cerebellar circuit studies, not human education studies.
- Cerebellar motor learning is not the whole of human learning, memory or cognition.
- Disinhibition is a specific circuit mechanism, not a general psychological permission slip.
- "What to learn" is a useful shorthand, but the paper is about climbing-fiber instructive signaling, Purkinje calcium responses and motor-learning plasticity.
- Both articles are open access under CC BY-NC-ND 4.0; summarize rather than adapting figures or text.

## Access

- Santos-Valencia et al. paper: https://doi.org/10.1038/s41586-026-10220-4
- Santos-Valencia et al. Nature page: https://www.nature.com/articles/s41586-026-10220-4
- Santos-Valencia et al. code: http://github.com/asemptote/CF-MLI-paper
- Santos-Valencia et al. data: https://doi.org/10.7910/DVN/MFEFB7
- Park et al. paper: https://doi.org/10.1038/s41593-026-02268-2
- Park et al. Nature Neuroscience page: https://www.nature.com/articles/s41593-026-02268-2
- Park et al. connectomics data: https://bossdb.org/project/park2023
- Park et al. code: https://github.com/cns-kim-lab/park_cerebellar_disinhibition
