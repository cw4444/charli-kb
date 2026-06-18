---
title: "World Properties Without World Models"
type: source
status: draft
created: 2026-06-18
updated: 2026-06-18
authors:
  - Elan Barenholtz
sources:
  - https://arxiv.org/abs/2603.04317
  - https://arxiv.org/html/2603.04317v1
  - https://github.com/elanbarenholtz/static-embeddings-space-time
---

# World Properties Without World Models

## Summary

Elan Barenholtz's 2026 arXiv preprint, "World Properties without World Models: Recovering Spatial and Temporal Structure from Co-occurrence Statistics in Static Word Embeddings," tests whether probe-recoverable geography and chronology in language models necessarily imply world-model-like internal representations.

The paper's answer is a careful "not by itself." Using the same broad family of linear ridge-regression probes, Barenholtz shows that static co-occurrence embeddings such as GloVe and Word2Vec already preserve substantial geographic signal and weaker but reliable temporal signal.

The useful result is not anti-world-model chest-beating. It is a calibration point: if simple static embeddings can recover latitude, longitude, temperature, and coarse historical era from text co-occurrence alone, then linear decodability from richer LLM hidden states is not enough to prove that the model has moved beyond text into a qualitatively separate world model.

## Core Claim

Text is not a thin symbolic layer floating above the world. It is full of compressed traces of geography, climate, culture, history, and social use.

That means co-occurrence statistics can preserve worldly structure without any explicit grounding, sensorimotor access, or contextual inference. A city name sits near country names, climate words, cultural words, regional terms, and historically patterned vocabulary. Those relations form a statistical imprint of the world.

The paper pushes against a too-fast inference:

> A probe can recover space or time from hidden states, therefore the model must have a world model.

Barenholtz's counter is narrower and stronger:

> A probe can recover space or time from static embeddings too, so probe recoverability alone cannot distinguish a genuine representational advance from structure already latent in text.

## Evidence

The study applies ridge-regression probes to static 300-dimensional embeddings:

- GloVe 6B 300d, trained on Wikipedia 2014 and Gigaword 5;
- Word2Vec Google News 300d, trained on Google News.

For 100 world cities, latitude, longitude, and mean annual temperature are linearly recoverable from the embeddings. Population, GDP per capita, and elevation are not reliably recovered, which matters because it suggests the probe is not simply extracting arbitrary real-world attributes from any city name.

For 194 historical figures, birth year, death year, and midlife year are also recoverable, but only coarsely. The temporal result distinguishes ancient, medieval, and modern eras better than it recovers precise chronology.

The strongest interpretability piece is the semantic analysis. City-temperature structure tracks word-neighborhood gradients: warm-city embeddings are closer to tropical/ecological/developing-world vocabulary, while cold-city embeddings are closer to northern European cultural and winter-climate vocabulary. Temporal structure similarly tracks era-associated words such as ancient, Greek, mythology, industrial, and revolution.

Subspace ablations strengthen the point. Removing semantic subspaces for country names, climate/weather terms, and regional terms degrades geographic and temperature recovery far more than random subspace removal of the same dimensionality.

## Why It Matters

This is the distributional-semantics companion to Barenholtz's [The Disappearing Ground](barenholtz-disappearing-ground.md).

The essay version says language has more autogenerative relational structure than crude grounding objections admit. This preprint gives the technical version: even old static embeddings preserve enough relational structure to recover parts of geography and history.

It also sits beside [Representational Geometry](../concepts/representational-geometry.md). Geometry can make worldly variables decodable, but decodability has to be interpreted against baselines. If static co-occurrence space already contains a compressed map-like signal, then richer LLM geometry needs stronger evidence before we call it a world model.

The clean rule is:

- **decodability matters;**
- **baselines matter just as much;**
- **text may already contain more world-structure than "mere text" rhetoric allows;**
- **world-model claims need evidence beyond linear probe success.**

## Relation To World Models

This paper does not show that LLMs lack world models.

It shows that one popular evidence route is underpowered. If the claim is "LLMs have linear representations of space and time," static embeddings are a serious control. If the claim is "LLMs build additional structured, compositional, usable spatial/temporal models," then the evidence needs to show generalization, manipulation, resolution, or behavior that exceeds co-occurrence baselines.

That is a better bar. Less exciting for press releases. Tragic.

## Relation To Charli's Current Barenholtz Lane

The current cluster now has three different jobs:

- [The Disappearing Ground](barenholtz-disappearing-ground.md): language-grounding and meaning-as-use argument.
- [World Properties Without World Models](world-properties-without-world-models-static-embeddings.md): static co-occurrence can preserve compressed worldly structure.
- [Trajectory Dynamics In Language Model Hidden States](trajectory-dynamics-hidden-states-reading-costs.md): dynamic hidden-state trajectories predict human reading cost beyond surprisal.

Together, they make one careful shape:

> Language is not "just words" if words preserve structured relations to world, use, and processing. But preserving structure is not the same as being conscious, embodied, or ontologically complete.

## Caveats

- This is an arXiv preprint.
- The city and historical-figure datasets are much smaller than some LLM-probing datasets.
- The comparison with LLM world-model papers is methodological, not a matched head-to-head benchmark.
- Static embeddings are a lower bound on what distributional text statistics can contain, not a full account of what contextual models learn.
- Temporal recovery is coarse, not precise historical dating.
- Averaged vectors for multi-word city names and surname choices for historical figures can introduce artifacts.
- Linear probe success is not proof that the system explicitly uses the decoded variable.

## Useful For

- [Representational Geometry](../concepts/representational-geometry.md)
- [Relational Meaning And Hidden Signals](../concepts/relational-meaning-and-hidden-signals.md)
- [Reality As Relational Constraint](../concepts/reality-as-relational-constraint.md)
- [Interpretability And Whether Internal States Matter](../../themes/ai-consciousness/interpretability.md)

## Do Not Overclaim

- Do not say this disproves LLM world models.
- Do not say static embeddings understand geography.
- Do not say text contains the whole world.
- Do not say linear probes are useless.
- Do not treat decodability as consciousness, grounding, or explicit reasoning.
- Do not use "mere statistics" as if statistics cannot preserve real structure. Apparently they can. Rude, but there it is.
