# 2026-03-26 GSD Context Engineering for Coding Agents

## Source

- Title: GSD: AI 코딩 에이전트의 컨텍스트 붕괴를 해결하는 워크플로우 시스템
- Site: gyuha.com
- Published: 2026-03-26
- URL: https://gyuha.com/post/2026/03/2026-03-26-gsd-context-engineering-coding-agents/
- Raw artifact: [[raw/inbox/2026-03-26-gsd-context-engineering-coding-agents.md]]
- Source type: GSD의 포지셔닝과 핵심 워크플로우를 요약한 2차 기사

## Summary

이 소스는 [[GSD]]를 Claude Code, Codex, Gemini CLI, OpenCode 같은 AI 코딩 도구 위에 올라가는 워크플로우 레이어로 설명한다. 특히 긴 세션에서 발생하는 [[Context Rot]] 문제를 발견-계획-실행-검증 분리와 파일 기반 상태 관리로 완화하려는 도구라는 점을 강조한다.

## Key claims from the source

- GSD는 새로운 IDE가 아니라 기존 AI 코딩 도구 위의 컨텍스트 엔지니어링 레이어다.
- `/gsd map-codebase`, `/gsd new-project`, `/gsd discuss-phase`, `/gsd plan-phase`, `/gsd execute-phase`, `/gsd verify-work`, `/gsd next` 같은 흐름을 중심으로 소개된다.
- 계획은 작고 원자적인 단위로 나뉘어 신선한 컨텍스트에서 실행되도록 설계된다.
- 실행은 의존성에 따라 병렬 또는 순차 웨이브로 조직된다.
- 검증은 단순 테스트 통과가 아니라 사용자 시나리오 확인까지 포함해야 한다고 설명한다.
- 작은 작업에는 과도할 수 있지만, 중대형 기능과 다단계 프로젝트에는 유용하다는 평가를 제시한다.

## Caveats

- 이 소스는 비디오와 프로젝트 소개를 바탕으로 정리한 2차 기사다.
- 설치 세부사항, 인기 지표, 일부 명령 설명은 upstream 문서로 다시 확인하는 편이 안전하다.
- `--dangerously-skip-permissions` 같은 운영 판단은 기사 수준 정보만으로 일반화하면 위험하다.

## Related pages

- [[GSD]]
- [[Context Rot]]
