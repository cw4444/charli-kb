---
title: "Choudhari et al. - Brain-Controlled Selective Hearing"
type: source
status: draft
created: 2026-06-16
updated: 2026-06-16
sources:
  - https://doi.org/10.1038/s41593-026-02281-5
---

# Choudhari et al. - Brain-Controlled Selective Hearing

Vishal Choudhari, Maximilian Nentwich, Sarah Johnson, Jose L. Herrero, Stephan Bickel, Ashesh D. Mehta, Daniel Friedman, Adeen Flinker, Edward F. Chang, Nima Mesgarani and colleagues published "Real-time brain-controlled selective hearing enhances speech perception in multi-talker environments" in *Nature Neuroscience* on 2026-05-11.

Nature marks the article open access under CC BY-NC-ND 4.0. Source data are provided, but the full participant data are available only on request because of privacy and ethical restrictions. Offline analysis code is available through NapLib, and the real-time closed-loop experiment code is public on GitHub.

## What They Did

The study tested auditory attention decoding (AAD): using a listener's brain signals to identify which speaker they are attending to, then selectively amplifying that speaker.

Four epilepsy-monitoring participants with intracranial EEG listened to two simultaneous, spatially separated conversations in noisy multi-talker scenes. The system learned participant-specific models that reconstructed the temporal envelope of attended speech from low-frequency and high-gamma neural features. In real time, it compared the reconstructed envelope with the competing speech streams, inferred the attended talker and adjusted gain so that the attended talker was amplified.

The authors tested three situations:

- turning the system on mid-trial;
- instructed attention switches;
- self-initiated attention shifts.

## What They Found

The closed-loop system improved the listening experience. It decoded attention above chance, translated decoding into real-time target-to-masker gain changes and improved speech intelligibility. Participants strongly preferred the system-on condition, and pupil data from two participants suggested reduced listening effort.

The system also tracked attention shifts. It adapted when participants were instructed to switch focus, and it could follow natural self-initiated shifts between talkers.

The study also included a deliberately reversed condition in which the system suppressed the attended talker and amplified the unattended one. That condition hurt performance, which is exactly the kind of grim little control result that makes the main claim less hand-wavy.

## Why It Matters

This is a direct neurotechnology version of selective attention. The paper shows that attended speech is not just subjectively "what you chose to listen to"; it has a cortical signature strong enough to steer a real-time assistive system.

For the wiki's perception lane, the result belongs beside active vision. Hearing is also not passive recording. In a multi-talker scene, the auditory system is selecting a target stream, suppressing or deprioritizing competitors and building a usable perceptual object out of acoustic chaos.

For assistive technology, the paper is a benchmark rather than a consumer product. Current hearing aids often amplify too broadly because they do not know the listener's intent. This work shows the principle: a future hearing device may need to infer what the listener is trying to attend to, not merely make everything louder.

Charli's Samuel Roukin-at-a-rave version is the household translation: if one voice is motivationally and attentively privileged enough, the brain may give that stream better tracking. This paper does not prove fandom creates superhearing. It does show why "I heard *that* voice through the noise" is not mystical; attention changes the signal.

## Caveats

- The study used intracranial EEG in four neurosurgical patients, not a consumer hearing-aid setup.
- Participants had self-reported normal hearing; this is not yet evidence of real-world benefit for hearing-aid users.
- Intracranial recordings are a high-resolution benchmark, not a practical everyday interface for most people.
- The system still depended on decoding accuracy, attention engagement, smoothing and task structure.
- Open access is CC BY-NC-ND; summarize rather than adapting article text or figures.

## Links

- Paper: https://doi.org/10.1038/s41593-026-02281-5
- Nature article page: https://www.nature.com/articles/s41593-026-02281-5
- Real-time closed-loop code: https://github.com/naplab/Real-Time-Brain-Controlled-Hearing
- NapLib toolbox: https://naplib-python.readthedocs.io
