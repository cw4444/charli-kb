# Bell, Wigner's Friend, and Observer-Dependent Reality

This repository is a Markdown-first knowledge base on a cluster of quantum-foundations work:

- Bell's theorem and Bell inequalities.
- Wigner's friend and extended Wigner's friend scenarios.
- Časlav Brukner's no-go theorem for observer-independent facts.
- Experimental and theoretical work on local observer-independence and local friendliness.
- Interpretations that either accept, resist, or dissolve observer-dependent facts.
- Speculative extensions, including whether AI systems could count as observers in any physically meaningful sense.

The central question is:

> How are Bell inequalities related to Brukner's Wigner's-friend work, local observer-independence, local friendliness, and observer-dependent reality?

Short answer: Bell inequalities constrain theories that try to preserve local hidden-variable-style explanations of correlations. Brukner-style and local-friendliness inequalities reuse the Bell logic, but replace or weaken "pre-existing hidden variables" with assumptions about whether observed events are absolute, observer-independent facts. Violations of these inequalities do not prove that everyday reality is unreal. They show that, if standard quantum theory applies to the relevant systems and if assumptions such as locality, free choice, and universal observability of records are retained, then not every observer's measurement outcome can be treated as a single shared fact in one observer-independent story.

## Why This Matters To Charli

This topic sits directly on the fault line between "reality as one public database" and "reality as relational, agent-indexed, or context-dependent."

For Charli's observer-dependent reality thread, the useful lesson is not the slogan "objective reality does not exist." That overstates the science. The durable insight is more precise:

- Quantum theory can force a distinction between facts-for-an-observer and facts-in-a-single-global-ledger.
- Bell-style reasoning turns metaphysical intuitions into testable or at least formally checkable constraints.
- Extended Wigner's-friend arguments ask whether observers themselves can be treated as quantum systems without breaking ordinary ideas about facts.
- AI-as-observer questions should start from operational roles such as record-making, information update, memory, agency, and communication, not from consciousness hype.

This wiki separates experimentally grounded claims from interpretive and philosophical claims so the thread can grow without becoming vague mysticism.

## Structure

```text
sources/source-index.md       Annotated bibliography.
sources/sources.csv           Tabular source metadata.
sources/sources.json          Structured source metadata for agents.
themes/                       Explanatory topic pages.
maps/concept-map.md           Plain-English map.
maps/concept-map.mmd          Mermaid concept graph.
reading-paths/                Suggested route from beginner to advanced.
open-questions.md             Research questions and unresolved tensions.
glossary.md                   Short definitions.
public/index.html             Optional static HTML version.
```

## Start Here

1. Read [themes/bell-inequalities.md](themes/bell-inequalities.md) for the Bell logic.
2. Read [themes/wigners-friend.md](themes/wigners-friend.md) for the observer setup.
3. Read [themes/observer-independent-facts.md](themes/observer-independent-facts.md) for Brukner and Proietti.
4. Read [themes/local-friendliness.md](themes/local-friendliness.md) for the stronger Bong/Cavalcanti/Wiseman/Pryde framework.
5. Read [themes/interpretations.md](themes/interpretations.md) to see how different interpretations pay different prices.

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

## Publishing

For GitHub Pages, publish the repo root or the `public/` folder, depending on the Pages setting. For Vercel or Netlify, no framework is required; serve `public/index.html` as a static file.

## Caveat

This is a research wiki, not a settled physics textbook. It cites primary and review sources where possible, marks speculative material, and keeps controversial claims tied to their assumptions.
