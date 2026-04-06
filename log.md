# Log

Append-only operational log.

## [2026-04-06] scaffold | Initial vault structure

- Created the initial llm-wiki scaffold.
- Added core directories for raw sources, wiki pages, and schema rules.
- Added `index.md`, `log.md`, and `AGENTS.md`.

## [2026-04-06] ingest | GSD context engineering article

- Added source note `wiki/sources/2026-03-26 GSD Context Engineering for Coding Agents.md` from `raw/inbox/2026-03-26 GSD - AI 코딩 에이전트의 컨텍스트 붕괴를 해결하는 워크플로우 시스템.md`.
- Added `wiki/entities/GSD.md` and `wiki/concepts/Context Rot.md` as the first reusable curated pages from this source.
- Updated `index.md` to expose the new source, concept, and entity pages.

## [2026-04-06] ingest | GSD primary technical guide

- Added source note `wiki/sources/2026-03-10 GSD Get Shit Done Context Engineering.md` from `raw/inbox/2026-03-10-gsd-get-shit-done-context-engineering.md`.
- Expanded `wiki/entities/GSD.md` with file-based planning architecture, wave execution, brownfield mapping, runtime support, and verification details.
- Updated `wiki/concepts/Context Rot.md` and added `wiki/concepts/Nyquist Validation.md` to capture the source's more concrete mitigation and coverage-planning model.
- Updated `index.md` to expose the new source and concept pages.

## [2026-04-07] repair | Restore missing GSD curated cluster

- Restored missing curated pages referenced by `index.md` and `log.md`: two GSD source notes, `wiki/entities/GSD.md`, `wiki/concepts/Context Rot.md`, and `wiki/concepts/Nyquist Validation.md`.
- Repaired the on-disk curated layer so the existing GSD cluster once again matches the catalog and audit log.

## [2026-04-07] ingest | GSD multi-agent plan verification update

- Added source note `wiki/sources/2026-03-19 GSD Multi Agent Plan Verification Update.md` from `raw/inbox/2026-03-19-gsd-update-multi-agent-plan-verification.md`.
- Expanded the repaired GSD cluster with the March 19 update's focus on multi-agent orchestration, planner→checker→revise, `/gsd:verify-work`, and discuss-phase strengthening.
- Updated `index.md` so the new source is discoverable alongside the restored GSD pages.
