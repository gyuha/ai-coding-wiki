---
name: wiki-ingest
description: Create or update wiki pages when new source material is added to this vault. Use when adding files under raw/, ingesting new material into wiki/sources/, updating affected topic pages, or bringing index.md and log.md into sync after source ingestion.
---

# Wiki Ingest

Use this skill when a new source is added to `raw/` and the vault needs to absorb it into the curated wiki.

## Workflow

1. Read the new source from `raw/`.
2. Create or update the matching source page in `wiki/sources/`.
3. Update any affected topic, entity, or synthesis pages in `wiki/`.
4. Add backlinks and cross-links using Obsidian wikilinks such as `[[Page Name]]`.
5. Update `index.md` if pages were added, renamed, or substantially changed.
6. Append a short ingest entry to `log.md`.

## Core rules

- Never edit existing files in `raw/` except to add new source materials.
- Prefer updating an existing wiki page over creating a duplicate.
- Surface contradictions explicitly instead of silently replacing older claims.
- Keep page names short and stable.
- Prefer one topic per page.
- For source pages, use `YYYY-MM-DD Title` when a date is known.

## File targets

- `raw/` — source material only; treat as immutable after ingest.
- `wiki/sources/` — source note for the ingested material.
- `wiki/` — topic, entity, and synthesis pages affected by the source.
- `index.md` — top-level navigation and page discovery.
- `log.md` — short audit trail of ingest activity.

## Common patterns

### When a source is entirely new

- Create a new page in `wiki/sources/`.
- Link it from the relevant topic pages.
- Add it to `index.md` if the vault structure or coverage changed materially.

### When a source updates an existing topic

- Update the existing topic page first.
- Add the new source page or expand the existing source page.
- Preserve prior claims when they still matter, and call out any contradiction clearly.

### When deciding whether to create a new page

Create a new page only when the concept deserves its own stable topic. If the content mainly extends an existing page, update that page instead.

## Validation checklist

- The source was read from `raw/`, not summarized from memory.
- A source page exists or was updated in `wiki/sources/`.
- Affected wiki pages were updated with relevant backlinks and cross-links.
- `index.md` was updated if discoverability changed.
- `log.md` contains a short ingest entry.
- No existing file in `raw/` was edited.

## References

- `AGENTS.md`
