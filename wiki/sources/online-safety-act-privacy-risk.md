---
title: "Online Safety Act Privacy Risk"
type: source
status: draft
created: 2026-06-12
updated: 2026-06-12
sources:
  - https://arxiv.org/abs/2606.05273
---

# Online Safety Act Privacy Risk

Mehta, Jalilzade, Kalameyets, Owens, Juarez, Aidinlis, Shi, and Elmas posted the arXiv preprint [Online Safety Regulation Increases Privacy Risk: Evidence from the UK Online Safety Act](https://arxiv.org/abs/2606.05273) on 2026-06-03.

The paper studies whether UK Online Safety Act milestones changed public behaviour around VPNs and privacy. It focuses on three regulatory events:

- Royal Assent for the Online Safety Act in October 2023;
- Ofcom illegal-content enforcement duties becoming active in March 2025;
- mandatory age assurance for adult and child-safety duties taking effect from 2025-07-25.

## Core Claim

The paper argues that online-safety regulation can create secondary privacy risk. The mechanism is not "safety law directly steals data." It is displacement: when age assurance or access controls make people distrust the regulated surface, some users move toward circumvention tools such as VPNs. That can preserve access or perceived privacy, but it also creates new intermediaries with their own logging, retention, sharing, and opacity problems.

## Evidence Used

The authors combine:

- Reddit discourse from VPN-related and UK politics communities from October 2021 to October 2025;
- Google Trends data for UK VPN search interest;
- Bayesian Structural Time Series / CausalImpact-style counterfactual modelling around OSA milestones;
- topic modelling, sentiment analysis, and LLM-assisted relevance/topic classification;
- privacy-policy analysis of 69 unique VPN services.

The study reports stepwise increases in VPN-related discourse and UK VPN search interest around OSA milestones. It also finds that UK users framed VPN use mainly around privacy, surveillance, censorship, and distrust of age-verification intermediaries, not only around getting access to blocked content.

For the VPN-provider analysis, the authors classified 26 services as low risk, 35 as medium risk, and 8 as high risk based on disclosed privacy-policy markers such as traffic logging, metadata logging, retention, third-party sharing, tracking identifiers, and policy vagueness. They found VPN attention rose across risk categories rather than shifting only toward high-risk providers.

## Why It Matters Here

This is useful evidence for the UK age-assurance/device-safety lane in the 2026 timeline.

The June 2026 device-level nudity-blocking proposal is not identical to the Online Safety Act rollout studied here. Still, the paper gives a live empirical warning: access-control regimes should be judged not only by whether platforms comply, but by what users do next. If users respond with VPNs, age-workarounds, jurisdiction shifting, or distrust of verification intermediaries, policy can move risk rather than remove it.

That is especially relevant when proposals move from websites and apps into device/OS-level controls. The more child-safety enforcement depends on age state, identity proof, content classification, camera behavior, or app/device defaults, the more important it becomes to measure displacement, evasion, privacy side effects, and trust collapse.

## Caveats

- This is a June 2026 arXiv preprint, not a settled regulatory evaluation.
- Reddit users are younger, more technical, and more privacy-politics aware than the general public.
- The UK-resident filter is a proxy based on subreddit participation, not confirmed residency.
- Google Trends measures attention, not confirmed VPN installation or use.
- The VPN risk analysis is based on public privacy policies, which may understate or obscure actual practices.
- The paper studies OSA milestones through October 2025 data, not the June 2026 whole-device nudity-blocking proposal.

## Useful Wiki Translation

Age assurance is not just a compliance checkbox. It is a behavioural intervention.

If people experience age checks as identity surveillance, they may route around them. That can weaken the child-safety goal, move adults and children into less accountable privacy tools, and create fresh data-risk surfaces. Regulators need to measure the workaround layer, not just declare the platform layer compliant and go home for tea.
