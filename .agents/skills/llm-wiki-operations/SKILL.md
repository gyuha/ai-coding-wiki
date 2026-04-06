---
name: llm-wiki-operations
description: Use when working inside this Obsidian llm-wiki vault to ingest new raw sources, answer questions from the compiled wiki, or lint the knowledge base for orphans, duplicates, stale claims, missing links, and contradictions. Trigger on requests to ingest sources, update the wiki, answer from the vault, refresh index/log, or health-check the wiki.
---

# LLM Wiki Operations

This skill operationalizes the `Standard operations` in this repository's `AGENTS.md` for the local Obsidian vault.

## Vault model

There are three layers:

1. `raw/` — immutable source material
2. `wiki/` — curated markdown maintained by the agent
3. `schema/` — templates, rules, and operating conventions

Important top-level files:

- `index.md` — catalog of the wiki
- `log.md` — append-only activity log
- `AGENTS.md` — governing rules for the vault

## Non-negotiable rules

- Never edit files in `raw/` except to add new sources.
- Prefer updating existing pages in `wiki/` over creating duplicates.
- Keep `index.md` current when pages are added, renamed, or materially changed.
- Append a short entry to `log.md` for every ingest, major query artifact, or lint pass.
- Use Obsidian wiki links like `[[Page Name]]` whenever possible.
- Surface contradictions explicitly instead of silently overwriting older claims.

## Routing guide

| User intent | Workflow |
| --- | --- |
| Add a paper, article, note, transcript, or source file | Ingest |
| Ask what the wiki says about a topic | Query |
| Audit, clean up, or health-check the vault | Lint |

## Ingest workflow

Use this when a new source is added under `raw/`.

1. Read the source from `raw/`.
2. Create or update a source page in `wiki/sources/`.
3. Update any affected topic, entity, or synthesis pages in `wiki/`.
4. Add backlinks and cross-links.
5. Update `index.md`.
6. Append an entry to `log.md`.

### Ingest conventions

- Prefer source page names like `YYYY-MM-DD Title` when a date is known.
- Reuse existing concept/entity/synthesis pages before creating new ones.
- If a new source changes the interpretation of an older claim, record the change explicitly.
- Keep source summaries factual; save broader interpretation to concept or synthesis pages.

## Query workflow

Use this when answering from the maintained wiki rather than raw materials.

1. Read `index.md` first.
2. Read only the relevant wiki pages.
3. Answer with citations to page names.
4. If the answer is broadly reusable, save it to `wiki/syntheses/`.

### Query conventions

- Prefer the compiled wiki over re-deriving answers from raw sources.
- If the wiki is incomplete, say what is missing instead of guessing.
- Cite page names directly in the answer so the user can navigate the vault.
- If a query produces a reusable comparison, thesis, or summary, file it back into the wiki.

## Lint workflow

Use this for periodic maintenance and health checks.

Check for:

- orphan pages
- stale claims
- missing cross-links
- duplicate pages
- unresolved contradictions
- concepts that deserve dedicated pages

### Lint conventions

- Prefer explicit fixes over vague notes when the correction is obvious.
- If duplicate pages should be merged but the merge is non-trivial, report the conflict clearly.
- Keep the wiki navigable by repairing missing cross-links and missing index coverage.
- Log major lint passes in `log.md`.

## Naming guidance

- Use short, stable page names.
- Prefer one topic per page.
- For syntheses, use descriptive names like `Model Comparison` or `Research Thesis`.

## Done criteria

Before considering the task complete, verify that:

- all intended wiki page updates were made
- `index.md` reflects any new or renamed pages
- `log.md` includes the operation when required
- links use Obsidian wiki-link style where possible
- contradictions are surfaced rather than flattened away
