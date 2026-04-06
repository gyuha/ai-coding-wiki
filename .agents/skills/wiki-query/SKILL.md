---
name: wiki-query
description: Answer questions from this vault using the curated wiki as the source of truth. Use when responding from wiki/, tracing related pages through index.md, citing page names, or deciding whether a reusable answer should become a synthesis page.
---

# Wiki Query

Use this skill when answering from the vault rather than from raw sources or unstored reasoning.

## Workflow

1. Read `index.md` first to understand the vault structure.
2. Read only the wiki pages relevant to the question.
3. Answer using citations to page names.
4. If the answer is broadly reusable, save it as a page in `wiki/syntheses/`.
5. If a new synthesis page was added or a page changed substantially, update `index.md`.
6. If the query produced a major reusable artifact, append a short entry to `log.md`.

## Scope

- Prefer `wiki/` as the working knowledge layer.
- Use `index.md` to find the right pages before expanding the search.
- Avoid reading unrelated notes just because they exist.
- Use source pages when needed, but only after grounding the search through the wiki structure.

## Citation pattern

Cite page names directly in the answer.

Example:

```markdown
The vault treats `raw/` as immutable and expects ingest work to flow through `wiki/sources/` and the curated wiki layers. See [[2026-04-06 Example Source]], [[Model Comparison]], and [[Research Thesis]].
```

If the response is conversational rather than a saved note, plain page-name citations are also acceptable as long as the referenced pages are clear and traceable.

## When to save a synthesis

Create or update a page in `wiki/syntheses/` when:

- the answer combines multiple pages into a reusable explanation,
- the result is likely to be useful again,
- or the answer becomes a durable reference rather than a one-off reply.

Prefer updating an existing synthesis over creating a duplicate.

## Common mistakes

- Skipping `index.md` and searching the vault blindly.
- Reading far more pages than the question needs.
- Answering without citing page names.
- Creating a new synthesis for a topic that already has a suitable page.
- Forgetting to update `index.md` after adding a synthesis page.

## Validation checklist

- `index.md` was read first.
- Only relevant wiki pages were read.
- The final answer cites page names.
- Any reusable synthesis was stored in `wiki/syntheses/`.
- `index.md` and `log.md` were updated when the query created a durable artifact.

## References

- `AGENTS.md`
