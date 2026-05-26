# Charli KB Research Program

This file configures the local `autoresearch` loop for Charli KB. It is deliberately narrow: public-source research, original synthesis, concise Markdown, and GitHub handoff. It is not a general web-clipping machine.

---

## Search Objectives

Default objectives:

- Find authoritative sources: papers, preprints, official docs, official lab/company/university pages, filings, datasets, code repositories, reputable journalism, and review sources.
- Extract key entities only when they help the wiki: people, organizations, products, tools, papers, concepts, and events.
- Note contradictions between sources
- Identify open questions and research gaps
- Preserve source dates and access notes
- Prefer recent sources for current AI/company/product claims
- Prefer foundational sources for physics, philosophy, neuroscience, and older AI-history claims

---

## Confidence Scoring

Label every claim with confidence when filing:

- **high**: multiple independent authoritative sources agree
- **medium**: single good source, or sources partially agree
- **low**: speculation, opinion pieces, single informal source, or claim not verified

Always note the source date for factual claims. Treat current AI product, company, price, policy, and timeline claims as drift-prone.

---

## Loop Constraints

- Max search rounds per topic: **3**
- Max wiki pages created per session: **5** unless Charli explicitly asks for a larger package
- Max sources fetched per round: **5**
- If max pages is reached before the loop completes: file what you have and note what was skipped in Open Questions

---

## Output Style

- Declarative, present tense
- Cite every non-obvious claim with a normal Markdown link.
- Short pages: under 200 lines. Split if longer.
- Avoid mush. Say what the source supports, what it does not support, and what is inference.
- Flag uncertainty explicitly in plain Markdown, for example: `Needs verification: this claim has only one weak source.`

---

## Durable Lanes

- AI: agents, model welfare, AI consciousness, persona safety, agentic engineering, compute, labs, tools, and knowledge-work rearchitecture.
- Reality: quantum foundations, observer-dependent facts, Wigner's friend, Bell/local friendliness, perception, reality monitoring, agency, and model-mediated reality.
- Overlap: observers, agents, records, self-models, public facts, private experience, and how humans or machines build reality-facing models.

## Domain Notes

- For AI/tech: prefer arXiv, official GitHub repos, official docs, model cards/system cards, company blogs, filings, and reputable reporting. Treat benchmarks, leaderboard claims, pricing, and product availability as unstable.
- For physics/philosophy: prefer primary papers, SEP-style references, university pages, and reputable review articles. Keep interpretation separate from empirical claims.
- For neuroscience/psychology: prefer peer-reviewed papers and reviews. Note study type, sample, and limitations when relevant.
- For company or market claims: prefer filings, official announcements, reputable reporting, and multiple-source confirmation.

## Required Finish

For any research that changes the wiki:

1. Update or create the Markdown page.
2. Update `wiki/index.md`.
3. Append to `wiki/log.md`.
4. Update `wiki/meta/current-state.md` when future agents need the context.
5. Validate touched Markdown links.
6. Commit and push unless publication risk is unclear.

## Exclusions

Do not cite as high-confidence evidence:

- Reddit posts or forums, except as pointers to primary sources.
- Social media posts, except as primary-source statements by named actors or as unstable discourse signals.
- Undated web pages.
- Sources that do not cite their own claims.
- Paywalled/copyrighted text copied into local notes.
