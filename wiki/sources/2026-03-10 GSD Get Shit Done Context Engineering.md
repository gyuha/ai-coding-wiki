# 2026-03-10 GSD Get Shit Done Context Engineering

## Source

- Title: GSD \(Get Shit Done\) — AI 코딩 에이전트를 위한 컨텍스트 엔지니어링 & 스펙 기반 개발 시스템 완전 가이드
- Site: gyuha.com
- Published: 2026-03-10
- URL: raw frontmatter에 canonical URL이 명시되어 있지 않아 미확인
- Raw artifact: [[raw/inbox/2026-03-10-gsd-get-shit-done-context-engineering.md]]
- Source type: upstream 저장소와 사용자 가이드를 바탕으로 GSD의 구조를 정리한 2차 기술 가이드

## Summary

이 소스는 [[GSD]]를 단순한 워크플로우 소개가 아니라, 메타 프롬프팅·컨텍스트 엔지니어링·스펙 기반 개발 시스템으로 설명한다. 핵심은 context rot를 줄이기 위해 계획과 상태를 파일로 외부화하고, 전문 서브에이전트가 신선한 컨텍스트에서 연구·계획·실행·검증을 분리해 수행하도록 만드는 구조다.

## Key claims from the source

- GSD는 `PROJECT.md`, `REQUIREMENTS.md`, `STATE.md`, `config.json`, `plans/` 같은 `.planning/` 파일을 통해 프로젝트 상태를 구조화한다.
- 실행은 웨이브 기반으로 조직되며, 독립 태스크는 병렬로, 의존성이 있는 태스크는 순차로 처리된다.
- 태스크 단위 원자적 git 커밋을 통해 롤백성과 변경 추적성을 높이려 한다.
- GSD는 연구자, 플래너, 플랜 체커, 실행자, 검증자, Nyquist 검증자 등 역할 분리형 서브에이전트 모델을 사용한다.
- [[Nyquist Validation]]은 요구사항 대비 테스트 계획의 커버리지를 코드 작성 전에 점검하는 계획 단계 품질 게이트로 제시된다.
- `/gsd:map-codebase`를 통해 브라운필드 코드베이스에서도 `STACK.md`, `ARCHITECTURE.md`, `CONVENTIONS.md`, `CONCERNS.md`를 생성해 일관된 후속 작업을 돕는다.
- `/gsd:quick`과 `config.json`을 통해 작은 작업과 속도/품질 프리셋도 지원한다.
- Claude Code, OpenCode, Gemini CLI, Codex를 포함한 멀티 런타임 지원을 지향한다.

## Caveats

- 이 문서는 GSD 저장소와 문서를 요약한 2차 가이드이며, 운영 세부사항은 upstream 문서로 재검증하는 편이 안전하다.
- 커뮤니티 규모, 생태계, 포트 상태 같은 정보는 시간이 지나면 빠르게 바뀔 수 있다.
- 시스템을 호의적으로 서술하는 기술 요약이므로 실제 도입 비용과 팀 적합성은 별도 판단이 필요하다.

## Related pages

- [[GSD]]
- [[Context Rot]]
- [[Nyquist Validation]]
