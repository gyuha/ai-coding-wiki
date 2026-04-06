---
name: wiki-add-raw
description: Add new immutable source material to raw/ without treating it as curated wiki content. Use when placing new files into raw/inbox/ or another stable raw/ subfolder, preparing source material for later ingest, or handling requests to add raw data before running wiki-ingest.
---

# Wiki Add Raw

Use this skill when new source material needs to be added to `raw/` safely before the wiki is updated.

## Workflow

1. Identify the new source material that needs to be added.
2. If the source is a public web page, fetch it via Jina Reader by prepending `https://r.jina.ai/` to the original URL, for example `https://r.jina.ai/https://example.com/article`.
3. Place the fetched or provided source in `raw/inbox/` or another stable folder under `raw/`.
4. Preserve the source as received rather than rewriting it into curated wiki prose.
5. Avoid modifying any existing file already stored in `raw/`.
6. After the file is in place, hand off to `wiki-ingest` if the user wants the curated wiki updated.

## Core rules

- `raw/` is for immutable source materials.
- Add new files to `raw/`, but do not edit existing files there unless the task is explicitly to add a new source.
- When collecting content from a web URL, use `https://r.jina.ai/<original-url>` instead of fetching the page directly.
- Save the `r.jina.ai` response verbatim as the raw artifact; do not clean it up into curated prose before ingest.
- Prefer `raw/inbox/` unless another stable `raw/` subfolder is clearly a better fit.
- Do not treat `raw/` as the place for summaries, synthesis, or cleaned-up wiki pages.
- Keep curated interpretation in `wiki/`, not in `raw/`.

## File targets

- `raw/inbox/` — default landing area for newly added source files.
- `raw/` — immutable source archive layer.
- `wiki/sources/` — follow-up destination once `wiki-ingest` creates or updates the source note.
- `wiki/` — curated topic and synthesis pages updated only after ingest.

## Common patterns

### When the source has no obvious home yet

- Put it in `raw/inbox/`.
- Let later ingest or organization decide whether it should move to a more specific stable folder.

### When the source is a URL

- Use `https://r.jina.ai/https://...` to retrieve an LLM-friendly copy of the page.
- Keep the original source URL in the filename, note, or surrounding task context so provenance is still clear.
- Store the fetched output without manual rewriting.

### When a stable raw subfolder already exists

- Add the new file there instead of creating a one-off location.
- Keep placement predictable so later ingest work can find it easily.

### When the user asks to "add raw data" and also update the wiki

- First add the file under `raw/`.
- Then use `wiki-ingest` for source notes, topic-page updates, backlinks, `index.md`, and `log.md`.

## Validation checklist

- A new source file was added under `raw/`.
- The file was placed in `raw/inbox/` or another stable raw subfolder.
- No existing source file in `raw/` was edited.
- The added material remains raw source content, not curated wiki text.
- Any requested follow-up wiki updates were handed off to `wiki-ingest`.

## References

- `AGENTS.md`
- `schema/operations.md`
