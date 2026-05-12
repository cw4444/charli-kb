# Charli KB

This repository is a plain Markdown research wiki about two durable lanes:

- **AI:** agents, model welfare, AI consciousness, persona safety, agentic engineering, queryable knowledge systems, and how AI changes the speed and shape of work.
- **Reality:** quantum foundations, observer-dependent facts, Wigner's friend, Bell inequalities, perception, reality monitoring, and the limits of simple observer-independent fact talk.

The overlap is where the wiki gets most interesting: observers, agents, records, self-models, public facts, private experience, and the question of how minds or machines build reality-facing models.

This is not an Obsidian vault and not a dumping ground. Raw material goes in `raw/`; durable public-safe synthesis goes into `wiki/`, `themes/`, `sources/`, `maps/`, and `reading-paths/`.

## Start Here

- [Wiki Index](wiki/index.md): catalog of generated wiki pages.
- [Current State](wiki/meta/current-state.md): short handoff for future agents.
- [Wiki Log](wiki/log.md): append-only record of meaningful changes.

## Main Research Packages

### AI Consciousness, Model Welfare, And Personhood

- [AI Consciousness And Model Welfare](themes/ai-consciousness/overview.md): balanced public-source package on AI consciousness, model welfare, self-reports, agency, interpretability, moral patienthood, company positions, and skeptical arguments.
- [AI Character Formation And Persona Safety](themes/ai-consciousness/character-formation-and-persona-safety.md): Anthropic-centered thread connecting Teaching Claude Why, persona vectors, agentic misalignment, constitutions, and model character as a safety surface.
- [Mind Children - Hans Moravec](wiki/sources/mind-children-hans-moravec.md): source note on Moravec's 1988 AI/posthumanist book.

### Agentic Work And Knowledge Systems

- [Agentic Engineering](wiki/concepts/agentic-engineering.md): software and knowledge work organized around steering AI agents.
- [Agentic Work Rearchitecture](wiki/concepts/agentic-work-rearchitecture.md): redesigning work so agents take on execution while humans own direction, judgment, verification, and consequences.
- [Agent Friendly Repositories](wiki/concepts/agent-friendly-repositories.md): repo conventions that let agents inspect, edit, verify, and report.
- [Queryable Organization](wiki/concepts/queryable-organization.md): work artifacts structured so humans and agents can ask evidence-backed questions.
- [Inference Speed Development](wiki/concepts/inference-speed-development.md): development where model runtime, context quality, and human judgment become the bottlenecks.
- [Cognitive Latency Shock](wiki/concepts/cognitive-latency-shock.md): felt disorientation when AI collapses the loop between thought, search, synthesis, structure, and artifact.

### Quantum Foundations And Observer-Dependent Reality

This package connects:

- Bell's theorem and Bell inequalities.
- Wigner's friend and extended Wigner's friend scenarios.
- Časlav Brukner's no-go theorem for observer-independent facts.
- Experimental and theoretical work on local observer-independence and local friendliness.
- Interpretations that either accept, resist, or dissolve observer-dependent facts.
- Adjacent views such as QBism and all-at-once/global-constraint approaches to law and time.

Start with:

1. [Bell Inequalities](themes/bell-inequalities.md)
2. [Wigner's Friend](themes/wigners-friend.md)
3. [Observer-Independent Facts](themes/observer-independent-facts.md)
4. [Local Friendliness](themes/local-friendliness.md)
5. [Interpretations](themes/interpretations.md)
6. [QBism, Global Constraints, and Observer-Dependent Reality](themes/qbism-adlam-observer-dependent-reality.md)
7. [Many-Worlds, Wheeler, and Observer-Dependent Reality](themes/many-worlds-and-observer-dependent-reality.md)

Short answer for the physics package: Bell inequalities constrain theories that try to preserve local hidden-variable-style explanations of correlations. Brukner-style and local-friendliness inequalities reuse the Bell logic, but replace or weaken "pre-existing hidden variables" with assumptions about whether observed events are absolute, observer-independent facts. Violations of these inequalities do not prove that everyday reality is unreal. They show that, if standard quantum theory applies to the relevant systems and if assumptions such as locality, free choice, and universal observability of records are retained, then not every observer's measurement outcome can be treated as a single shared fact in one observer-independent story.

## Repository Structure

```text
raw/                         Local curated source material. Read but do not publish directly.
wiki/                        Agent-maintained Markdown knowledge base.
wiki/index.md                Content-oriented catalog.
wiki/log.md                  Chronological activity log.
wiki/meta/current-state.md   Lightweight handoff for future agents.
themes/                      Larger research-package topic pages.
sources/                     Source indexes and structured bibliographies.
maps/                        Concept maps.
reading-paths/               Suggested reading routes.
skills/                      Optional local agent skills.
public/                      Optional static HTML output for selected packages.
```

## Working Rules

- Do not copy copyrighted, paywalled, private, or sensitive source text into the public wiki.
- Summarize in original words and cite source locations.
- Treat `raw/` as non-public working material by default.
- Prefer primary sources for science, technology, philosophy, and research claims.
- Clearly separate source claims, commentary, and Charli's interpretation/speculation.
- Update [wiki/index.md](wiki/index.md), [wiki/log.md](wiki/log.md), and [wiki/meta/current-state.md](wiki/meta/current-state.md) after meaningful wiki changes.
- Commit and push agreed public-safe wiki updates after verification unless publication risk is unclear.

## Preview Locally

Markdown needs no build step. Open the files directly on GitHub or in any editor.

For the optional HTML page:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/public/
```

The HTML uses Mermaid from a CDN for the diagram. Without internet, the text and table still work, but the diagram may not render.

## Caveat

This is a research wiki, not a settled textbook. It cites primary and review sources where possible, marks speculative material, and keeps controversial claims tied to their assumptions.
