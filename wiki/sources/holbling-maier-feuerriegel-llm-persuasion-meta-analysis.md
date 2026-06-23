---
title: "Hölbling et al. - Meta-Analysis Of LLM Persuasion"
type: source
status: draft
created: 2026-06-23
updated: 2026-06-23
authors:
  - Lukas Hölbling
  - Sebastian Maier
  - Stefan Feuerriegel
sources:
  - https://doi.org/10.1038/s41598-025-30783-y
  - https://www.nature.com/articles/s41598-025-30783-y
  - https://arxiv.org/html/2606.16475v1
---

# Hölbling et al. - Meta-Analysis Of LLM Persuasion

## Summary

Hölbling, Maier, and Feuerriegel's 2025 open-access *Scientific Reports* meta-analysis asks a question that headlines usually bulldoze: are LLMs more persuasive than humans *on average*? Based on seven eligible studies, 17,422 participants, and 12 effect-size estimates, the answer was no clear overall difference (Hedges' g = 0.02, p = .530).

That is not a reassuring "therefore no problem" result. The studies were highly heterogeneous (I² = 75.97%), meaning that model, domain, format, content, and outcome definition mattered greatly. The authors' combined contextual model explained much of that between-study variation, but the evidence base was too small to confidently isolate which single ingredient did the work.

The durable takeaway is conditional, not binary: LLMs can be persuasive, but whether they outperform a human depends on how the interaction is designed and what kind of persuasion is being measured.

## What It Reviewed

The authors searched Web of Science, ACM Digital Library, arXiv, SSRN, and OSF through 2025-05-22. They required direct experimental comparisons between LLM-generated and human-generated persuasive communication, leaving seven publications after a stringent screen.

The included evidence varied across early GPT-3 / GPT-3.5, GPT-4-family, and Claude 3-family models; one-shot messages and adaptive multi-turn conversations; politics, health, propaganda, quizzes, and mixed domains; and attitude change, behavioral intention, compliance, policy support, and perceived-message-effectiveness measures.

The last category is a proper nuisance: saying a message seems persuasive is not the same thing as changing a real belief or behavior. The meta-analysis prioritised outcomes closer to behavioral change where possible.

## What The Paper Suggests

The review's qualitative synthesis suggests a plausible division of labor. LLM messages often leaned toward analytical reasoning and informational coherence; human messages were often more emotionally vivid or personally engaging. The authors therefore suggest LLMs may shine where evidence-heavy reasoning and elaboration matter, while humans may retain advantages where emotional resonance, relational trust, identity, or narrative authenticity do the persuading.

This is a hypothesis map rather than a final settled mechanism. Individual moderator tests were not significant, likely in part because there were only seven studies. The combined model is suggestive, but with many predictors and few studies it can overfit. The honest answer is still "when, not if"—and exactly which conditions make the difference remains an open empirical question.

## Why The 2026 Expert-Human Result Does Not Cancel It

Hackenburg, Wagner, Hewitt, Tappin, Saunders, Kirk, Margetts, and Summerfield's June 2026 arXiv preprint, [AI systems out-persuade expert humans](https://arxiv.org/html/2606.16475v1), is later than the meta-analysis's search cutoff and tests a much stronger contemporary setup: four preregistered experiments with 18,978 conversations from 6,923 people, comparing frontier AI with laypeople, tournament-selected persuaders, world-championship debaters, and professional canvassers.

The preprint reports an AI advantage even against elite human persuaders, including a real-money donation task. Its most useful mechanism clue is throughput: AI produced longer, faster, more information-dense replies. When the researchers constrained it to human-length messages and human writing speed, the advantage over coached elite debaters was no longer significant.

So the later result does not mean the meta-analysis was wrong. It narrows the likely story: as model capability and especially conversational throughput rise, the old context-sensitive average can turn into a strong advantage in live, fact-dense interactive contests. The arXiv work remains a preprint, and its societal claims should not be confused with a general proof that AI wins every argument, every culture, or every real-world political contest.

## Safety And Governance Relevance

LLM persuasion cuts both ways: models can help explain complex evidence, support education, and make public-interest information more accessible; the same adaptive conversation can scale targeted manipulation, misinformation, coercive persuasion, scams, political influence, or unhealthy dependence.

This is the human-facing mirror image of [Meincke et al. - Persuading LLMs To Comply With Objectionable Requests](meincke-duckworth-cialdini-persuading-llms.md). One line of work asks how people can socially influence models; this one asks when models can influence people. In both directions, conversational design, relationship cues, information density, personalization, and context become a safety surface.

## Caveats

- The meta-analysis includes only seven studies and 12 effect sizes; its moderator evidence is exploratory and underpowered.
- The search cutoff was May 2025, before the newest model generations and before the 2026 expert-human preprint.
- Most samples were English-speaking, U.S.-centric, online convenience samples; broad cultural generalisation would be reckless.
- Persuasion outcomes are not interchangeable: perceived quality, stated attitude, intention, compliance, and real action are different things.
- The 2026 comparison study is a preprint, with controlled topics, incentives, and study populations; it is strong new evidence, not the final global scoreboard.

## Useful For

- [Meincke et al. - Persuading LLMs To Comply With Objectionable Requests](meincke-duckworth-cialdini-persuading-llms.md)
- [AI And Agents 2026 Timeline](../timelines/ai-and-agents-2026.md)
