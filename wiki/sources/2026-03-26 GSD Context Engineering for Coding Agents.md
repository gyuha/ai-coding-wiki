# 2026-03-26 GSD Context Engineering for Coding Agents

## Source

- Title: GSD: AI 코딩 에이전트의 컨텍스트 붕괴를 해결하는 워크플로우 시스템
- Site: gyuha.com
- Published: 2026-03-26
- URL: https://gyuha.com/post/2026/03/2026-03-26-gsd-context-engineering-coding-agents/
- Raw artifact: [[raw/inbox/2026-03-26 GSD - AI 코딩 에이전트의 컨텍스트 붕괴를 해결하는 워크플로우 시스템.md]]
- Source type: secondary article summarizing a video and project positioning, not primary GSD documentation.

## Summary

This source presents [[GSD]] (Get Shit Done) as an open-source workflow layer that sits on top of AI coding tools such as Claude Code, Codex, Gemini CLI, OpenCode, Copilot, Cursor, and Antigravity. Its main framing is that long-running agent sessions suffer from [[Context Rot]], and that GSD mitigates that degradation by breaking work into explicit phases, storing project memory outside chat, and reintroducing verification as a first-class step.

## Key claims from the source

- GSD is positioned as a workflow and context-engineering layer rather than a new IDE or a new model.
- The article highlights a command flow built around `/gsd map-codebase`, `/gsd new-project`, `/gsd discuss-phase`, `/gsd plan-phase`, `/gsd execute-phase`, `/gsd verify-work`, and `/gsd next`.
- Planning is intentionally broken into small units so agents can operate inside fresher context windows instead of one long conversation.
- Execution is described as dependency-aware and parallel where work items are independent.
- Verification is described as going beyond compile or test success into user-visible scenario checks.
- The workflow is framed as especially useful for solo developers, indie hackers, and medium-to-large multi-phase projects.

## Caveats

- This is a secondary summary source. Installation details, exact command names, and project popularity claims should be checked against primary GSD documentation before being reused operationally.
- The source explicitly treats `--dangerously-skip-permissions` as a caution area rather than a universally safe default.
- The article argues that the workflow is overkill for very small edits such as simple renames, isolated bug fixes, or single-component changes.

## Related pages

- [[GSD]]
- [[Context Rot]]
