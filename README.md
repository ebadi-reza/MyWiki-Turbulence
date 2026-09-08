# Wall-Bounded Turbulence & Heat Transfer — Knowledge Wiki

A personal, interlinked knowledge base reconstructing Reza Ebadi's research in  fluid mechanics — turbulent boundary layers, heat transfer, and instrumentation — built with the "LLM Wiki" pattern (immutable sources in, a maintained set of interlinked Markdown pages out).

## Layout

- **`wiki/`** — the knowledge base. Markdown with Obsidian-style `[[wikilinks]]` and LaTeX math.
  Start at [`wiki/overview.md`](wiki/overview.md) (map of the six research threads) and
  [`wiki/index.md`](wiki/index.md) (catalog of every page).
- **`raw/`** — immutable source documents (papers, dissertation, notes). **Not tracked in git**
  (see `.gitignore`): large PDFs / publisher-copyright material, kept local.
- **`CLAUDE.md`** — the schema and operating instructions for how the wiki is built and maintained.

## Inside `wiki/`

| Path | What |
|---|---|
| `overview.md` | Top-level map of the six threads and how they connect |
| `index.md` | Catalog of every page, by category |
| `notation.md` | Canonical symbol table (the authority on notation) |
| `log.md` | Append-only ingest / query / lint history |
| `threads/` | One page per research thread |
| `concepts/` | Field concepts (log law, four-layer structure, UMZ/VF, …) |
| `methods/` | Experimental & analytical methods (PIV, hot-wire, DNS, …) |
| `sources/` | One page per ingested paper / chapter |
| `analyses/` | Comparisons and syntheses filed back from questions |

## Viewing

Open the folder as an **Obsidian vault** for graph view, backlinks, and math rendering. (A static
website — e.g. via Quartz — is a possible future step; only `wiki/` would be published.)
