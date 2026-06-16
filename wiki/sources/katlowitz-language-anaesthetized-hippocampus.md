---
title: "Katlowitz et al. - Language And Plasticity In The Anaesthetized Human Hippocampus"
type: source
status: draft
created: 2026-06-16
updated: 2026-06-16
sources:
  - https://doi.org/10.1038/s41586-026-10448-0
---

# Katlowitz et al. - Language And Plasticity In The Anaesthetized Human Hippocampus

Kalman A. Katlowitz and colleagues published "Plasticity and language in the anaesthetized human hippocampus" in *Nature* on 2026-05-06. Nature marks the article open access and lists an author correction published on 2026-06-11.

The study used high-density Neuropixels microelectrodes to record single-unit and local-field-potential activity from the human hippocampus during epilepsy surgery. The recordings came from seven anaesthetized patients undergoing anterior temporal lobectomy, before mesial temporal resection. Three patients heard pure-tone oddball sequences; four heard 10-20 minutes of natural speech from podcast episodes.

## What They Found

The tone experiments showed that auditory discrimination did not simply vanish under general anaesthesia. Many hippocampal units responded to tones, some encoded tone identity, and population activity carried oddball information. More interestingly, the oddball representation became more distinct over roughly 10 minutes, suggesting representational plasticity rather than a static sensory echo.

The authors also trained a recurrent neural network on a related tone-discrimination task. The model could represent oddball context despite being trained on tone identity, which the authors use as a mechanistic illustration that local recurrent dynamics can generate context-sensitive representations without needing executive control.

The language result is the reason this belongs here. In the four natural-speech patients, hippocampal single units and LFPs carried information about word frequency, semantic embeddings, semantic categories, part of speech, and surprisal. The authors also report that neural responses carried information about recent words and upcoming words. They are careful that this need not mean active prediction in the conscious sense; contextualization alone may explain some of it.

## Why It Matters

The paper is evidence that complex sensory and language-related processing can persist during anaesthesia-induced loss of consciousness. That is not the same as saying the patient consciously understood the podcast. It means the boundary between "unconscious" and "no high-level processing" is much messier than the folk version.

For the wiki's language-and-identity thread, the useful point is narrow but sharp: linguistic structure can be neurally processed below reportable awareness. Some of the machinery that maps sound into semantic and grammatical relationships may keep running without a conscious narrative owner sitting on top of it.

For the AI-consciousness thread, the paper is a biological caution against cheap consciousness tests. Decodable semantic and predictive structure is important evidence about processing, but it is not by itself proof of subjective experience. Same font, not same theorem.

## Caveats

- The sample is small: seven neurosurgical patients, with language data from four.
- These were epilepsy-surgery patients under anaesthesia, not healthy awake listeners.
- The hippocampus contributes to language and memory, but it is not the whole language system.
- The study shows preserved neural encoding and plasticity, not conscious comprehension.
- The author correction should be checked if relying on any specific figure, label, or statistical detail.
- Open access does not mean "copy the paper into the wiki"; this note summarizes in original words and links to the version of record.

## Links

- Paper: https://doi.org/10.1038/s41586-026-10448-0
- Nature article page: https://www.nature.com/articles/s41586-026-10448-0
- Code repository: https://github.com/NuttidaLab/rnn_oddball
