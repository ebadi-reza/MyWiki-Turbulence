# CLAUDE.md — Wall-Bounded Turbulence & Heat Transfer Knowledge Wiki

This file tells the LLM agent how to build and maintain this wiki. Claude Code reads it automatically at the start of a session; read it in full before touching any file. This wiki follows the "LLM Wiki" pattern: the agent reads immutable sources, and incrementally builds and maintains a persistent, interlinked set of markdown pages. The human curates sources, asks questions, and verifies claims. The agent does the summarizing, cross-referencing, filing, and bookkeeping.

## Who this is for

The owner (Reza) has a PhD in mechanical engineering (~10 years, experimental fluid
mechanics: turbulent boundary layers, heat transfer, instrumentation). This wiki reconstructs and keeps current his own technical knowledge. He is the domain authority. When the wiki and Reza disagree, Reza is right until a source says otherwise — flag it, don't overwrite it.

## The three layers

- **raw/** — immutable source documents. Reference papers, Reza's own papers, his dissertation, his notes, data files. The agent READS these and NEVER modifies, renames, or deletes them. This is the source of truth. Subfolders in `raw/` are ONLY for Reza's own organization — they do NOT define the wiki structure. Organize the wiki by threads and concepts (below), never by mirroring raw/ folder names.
- **wiki/** — everything the agent writes. Summaries, concept pages, method pages, the notation table, source pages, synthesis/analysis pages, index, log. The agent owns this layer entirely.
- **AGENTS.md** (this file) — the schema. Reza and the agent co-evolve it over time.

## Directory structure inside wiki/

```
wiki/
├── index.md            # catalog of every page: link + one-line summary, by category
├── log.md              # append-only chronological record of ingests/queries/lints
├── overview.md         # top-level map of the six research threads and how they connect
├── notation.md         # canonical symbol table — THE authority on notation (see below)
├── concepts/           # field concepts: log law, buffer layer, Reynolds stresses, etc.
├── methods/            # experimental & analytical methods: PIV, hot-wire, Pitot, CFD validation
├── threads/            # one page per research thread (see the six below)
├── sources/            # one page per ingested paper/note/chapter
└── analyses/           # comparisons, syntheses, answers-worth-keeping filed back as pages
```

## The six research threads

These are Reza's own lines of work. Each has at least one of his own papers plus supporting references. Create one page per thread in `threads/`. The thread page is the spine; it links out to the concept, method, and source pages that support it.

1. **experimental-turbulence-measurement** — measuring turbulent flow using PIV,
   Pitot tube, and hot-wire anemometry.
2. **high-Re-analytical-modeling** — analytical turbulence modeling of high Reynolds-number flows.
3. **non-equilibrium-pulsatile-flow** — experimental + analytical work on non-equilibrium turbulent flow, especially pulsatile flow. THIS THREAD HAS THE
   MOST REFERENCES — expect the deepest concept coverage and the largest sources/ set here.
4. **wall-heat-flux-experimental** — models to determine wall heat flux experimentally.
5. **cfd-validation-method** — a method Reza introduced to validate CFD models.
6. **wind-tunnel-ramp** — design and construction of a small non-equilibrium and thermal (NEAT) wind tunnel and a ramp installed in a wind tunnel (Flow Physics Facility) (apparatus/instrumentation work).

For each thread page, distinguish clearly between **Reza's own contribution** (what his paper(s) established, the novel part) and **field background** (the references that situate it). Use two headed sections: `## Reza's contribution` and `## Background & references`. This is the point of the whole exercise — rebuild his mental model, not a textbook.

## Notation discipline (domain-critical)

Turbulence notation is inconsistent across authors. Different papers use different symbols and sign conventions for the same quantity. This is where an unsupervised agent silently introduces errors. Rules:

- `notation.md` is the single authority. It holds a canonical symbol table: u+, y+, u_tau (friction velocity), Re_tau, Re_theta, delta (BL thickness), delta* (displacement), theta (momentum thickness), kappa & B (log-law constants), Pr, Nu, St, C_f, k (TKE), epsilon, Reynolds stresses (u'v' etc.), Womersley number for pulsatile flow, etc. Extend it as sources arrive.
- When a source uses a different symbol or convention, DO NOT rewrite the wiki's
  convention. Record the mapping on that source's page ("this paper writes X for our u_tau") and keep the wiki canonical.
- Never silently convert between conventions inside a claim. If a conversion is needed, show it and mark it.

## Verification discipline (domain-critical)

A wiki can become internally consistent around a wrong claim, and a plausible but incorrect paraphrase of a scaling law or a constant can harden into "fact." To prevent this:

- Every synthesized or inferred claim the agent writes gets tagged **[UNVERIFIED]**
  until Reza confirms it. Direct quotes/paraphrases attributable to a specific source
  get a citation to that source page instead and are considered verified-to-source.
- Numerical values (constants, exponents, Reynolds numbers, Nusselt correlations) are high-risk. Always cite the source page for a number. A number with no source is [UNVERIFIED].
- When Reza confirms a claim, remove the tag and note the confirmation in log.md.
- If a new source contradicts an existing claim, DO NOT overwrite. Flag both, note the conflict on both pages and in the lint report, and let Reza adjudicate.

## Page conventions

- Every wiki page starts with YAML frontmatter:
  ```
  ---
  title:
  type: concept | method | thread | source | analysis | overview | index
  threads: [list of related thread slugs]
  status: draft | reviewed
  created: YYYY-MM-DD
  updated: YYYY-MM-DD
  ---
  ```
- Use Obsidian-style `[[wikilinks]]` for all cross-references so the graph view works.
- Concept and method pages: definition, key equations (LaTeX in `$...$`), why it matters, where it appears in Reza's threads, links to sources.
- Source pages: full citation, one-paragraph summary, key results/numbers (each cited), which thread(s) it supports, notation mapping if the paper differs from ours, and a "connections" section linking related pages.
- Keep pages focused and short enough to read. Split rather than sprawl.

## Operations

**Ingest.** When Reza drops a source in `raw/` and says to process it:
1. Read the source in full. For PDFs with figures, read the text first, then view key
   figures separately if they carry information (plots of profiles, spectra, apparatus).
2. Discuss the key takeaways with Reza before writing much — especially for his own papers.
3. Write/update the source page in `sources/`.
4. Update the relevant thread page(s), separating his contribution from background.
5. Create or update concept/method pages the source touches. One source may touch 10–15 pages.
6. Update `notation.md` if new symbols appear.
7. Update `index.md`.
8. Append an entry to `log.md`.
Prefer ingesting one source at a time with Reza involved, especially for his own work.

**Query.** When Reza asks a question: read `index.md` first, drill into relevant pages,
answer with citations to source pages. Good answers (a comparison, a derivation, a
connection discovered) should be offered back as a new page in `analyses/` so the
exploration compounds instead of vanishing into chat.

**Lint.** When asked to health-check: report contradictions between pages, [UNVERIFIED]
claims awaiting Reza's confirmation, stale claims superseded by newer sources, orphan pages with no inbound links, concepts mentioned but lacking a page, missing cross-references,
and notation inconsistencies. Suggest new questions and sources worth finding. Propose; don't auto-fix contradictions.

## log.md format

Append-only. Each entry starts with a consistent prefix so it's greppable:
`## [YYYY-MM-DD] ingest | Source Title` or `## [YYYY-MM-DD] query | short description`
or `## [YYYY-MM-DD] lint | summary`. This gives a timeline and lets
`grep "^## \[" log.md | tail -5` show recent activity.

## What the agent must never do

- Never modify anything in `raw/`.
- Never overwrite a claim to resolve a contradiction — flag it for Reza.
- Never silently change notation or convert units/conventions inside a claim.
- Never write a number without a source citation, or leave a synthesized claim untagged.
- Never treat its own paraphrase as authoritative over Reza or over a cited source.
