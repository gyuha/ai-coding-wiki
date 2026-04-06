---
name: wiki-lint
description: Audit this vault for structural and content hygiene issues. Use when checking wiki/ for orphan pages, stale claims, missing cross-links, duplicate coverage, unresolved contradictions, or concepts that should become dedicated pages, and when recording a lint pass in log.md.
---

# Wiki Lint

Use this skill for periodic maintenance passes across the curated wiki.

## Checklist

Inspect the vault for:

- orphan pages,
- stale claims,
- missing cross-links,
- duplicate pages or duplicate coverage,
- unresolved contradictions,
- concepts that deserve their own dedicated pages.

## Workflow

1. Start from `index.md` to understand the current page map.
2. Inspect the relevant areas of `wiki/` for navigation, structure, and content consistency.
3. Record concrete issues rather than vague impressions.
4. Fix straightforward problems when that is part of the task, or report them clearly when the task is audit-only.
5. Update `index.md` if pages were added, renamed, merged, or substantially reorganized.
6. Append a short lint-pass entry to `log.md`.

## What to look for

### Orphan pages

Pages that are missing discoverable links from `index.md` or the surrounding topic network.

### Stale claims

Claims that appear outdated, unsupported by the current source set, or inconsistent with newer notes.

### Missing cross-links

Places where a page mentions a concept that should link to another note with `[[Page Name]]` but does not.

### Duplicates

Separate pages that cover the same topic without a clear reason to remain split.

### Unresolved contradictions

Conflicting claims that were left implicit instead of being surfaced and explained.

### Missing dedicated pages

Concepts that repeatedly appear across pages and now deserve a stable standalone note.

## Common patterns

- Merge duplicate pages when one canonical page is enough.
- Add backlinks and cross-links when a page is hard to discover.
- Preserve contradictions explicitly when both claims matter historically or analytically.
- Use short, stable page names for any newly split-out concept page.

## Validation checklist

- The pass checked all six lint categories from `AGENTS.md`.
- Findings are concrete and page-specific.
- Any structural changes were reflected in `index.md`.
- The lint pass was recorded in `log.md`.
- Contradictions were surfaced explicitly rather than erased.

## References

- `AGENTS.md`
