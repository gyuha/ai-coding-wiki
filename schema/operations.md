# Operations

## Ingest workflow

1. Put source files into `raw/inbox/` or another stable folder under `raw/`.
2. Create a source note in `wiki/sources/`.
3. Update any relevant concept, entity, and synthesis pages.
4. Update `index.md`.
5. Append an event to `log.md`.

## Query workflow

1. Start from `index.md`.
2. Read relevant wiki pages.
3. Answer from the compiled wiki, not raw files, unless deeper verification is needed.
4. If the result is reusable, save it in `wiki/syntheses/`.

## Lint workflow

Review the vault for:

- missing backlinks
- duplicate concepts
- contradicting claims
- pages with weak summaries
- pages mentioned often but not yet created
