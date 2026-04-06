# LLM Wiki Maintainer

This vault follows a three-layer model:

1. `raw/` — immutable source materials.
2. `wiki/` — curated, interlinked markdown pages maintained by the agent.
3. `schema/` — operating rules, templates, and maintenance conventions.

## Core rules

- Never edit files in `raw/` except to add new sources.
- Prefer updating existing pages in `wiki/` over creating duplicates.
- Keep `index.md` updated when pages are added, renamed, or substantially changed.
- Append a short entry to `log.md` for every ingest, major query artifact, or lint pass.
- Use Obsidian wiki links (`[[Page Name]]`) for cross-references whenever possible.
- Write documents in this vault in Korean.
- Use Mermaid charts whenever possible when representing flows or structure.
- Surface contradictions explicitly instead of silently overwriting older claims.

## Standard operations

### Ingest

When a new source is added:

1. Read the source from `raw/`.
2. Create or update a source page in `wiki/sources/`.
3. Update any affected topic/entity/synthesis pages in `wiki/`.
4. Add backlinks and cross-links.
5. Update `index.md`.
6. Append an entry to `log.md`.

### Query

When answering from the wiki:

1. Read `index.md` first.
2. Read only the relevant wiki pages.
3. Answer with citations to page names.
4. If the answer is broadly reusable, save it back as a page in `wiki/syntheses/`.

### Lint

Periodically check for:

- orphan pages
- stale claims
- missing cross-links
- duplicate pages
- unresolved contradictions
- concepts that deserve dedicated pages

## Naming guidance

- Use short, stable page names.
- Prefer one topic per page.
- For source notes, use `YYYY-MM-DD Title` when a date is known.
- For syntheses, use descriptive names like `Model Comparison` or `Research Thesis`.
