# GSD

## Summary

[[GSD]] \(Get Shit Done\)는 AI 코딩 에이전트를 위한 워크플로우 레이어이자 컨텍스트 엔지니어링 시스템으로 설명된다. Claude Code, OpenCode, Gemini CLI, Codex 같은 런타임 위에서 동작하며, 계획·상태·검증을 파일 기반으로 구조화해 [[Context Rot]]를 줄이려는 접근이 핵심이다.

## Core idea

현재 소스군이 공통으로 말하는 중심 문제는 장기 세션에서의 컨텍스트 오염이다. GSD는 이 문제를 한 대화에 모든 것을 싣는 방식 대신, 파일 기반 상태 관리와 전문 서브에이전트 분업으로 해결하려 한다.

## Workflow shape

현재 소스 기준 GSD의 기본 흐름은 다음과 같다.

- 코드베이스 파악 또는 프로젝트 초기화
- 요구사항 논의
- 계획 수립
- 계획 검증
- 실행
- 사용자 확인 및 결과 검증
- 실패 시 수정 계획과 재실행

즉 GSD는 “코드부터 쓰는 흐름”보다 “연구 → 계획 → 실행 → 검증 → 복구”를 시스템화하는 쪽에 가깝다.

## File-based planning architecture

2026-03-10 소스는 GSD의 구조를 `.planning/` 중심으로 구체화한다. 핵심 파일은 다음과 같다.

- `PROJECT.md` — 프로젝트 비전, 기술 스택, 아키텍처 결정
- `REQUIREMENTS.md` — 기능/비기능 요구사항과 제약
- `STATE.md` — 현재 단계와 마일스톤 상태
- `config.json` — 모델 프로파일, 워크플로우 토글, git 전략
- `plans/` — XML 기반 구현 계획

이 구조의 의미는 지시를 채팅에만 남기지 않고, 후속 에이전트가 다시 읽을 수 있는 형태로 상태를 외부화한다는 데 있다.

## Execution and verification model

현재 소스군이 강조하는 실행·검증 특징은 다음과 같다.

- 의존성 기반 웨이브 실행
- 태스크 단위 원자적 git 커밋
- planner → checker → revise 루프를 통한 계획 검증
- `/gsd:verify-work`를 통한 구현 후 사용자 확인과 실패 복구 루프
- [[Nyquist Validation]]을 통한 요구사항 대비 테스트 계획 커버리지 점검

특히 2026-03-19 소스는 verify-work를 단순 테스트 실행이 아니라, UAT → 디버그 → 수정 계획 → 재실행으로 이어지는 운영 루프로 설명한다.

## Multi-agent orchestration

2026-03-19 소스는 GSD의 최근 변화로 멀티 에이전트 오케스트레이션 강화를 강조한다. 여기서 중요한 포인트는 병렬 실행 자체보다, 메인 세션을 얇게 유지하고 리서치·계획·실행·검증을 fresh context 서브에이전트로 분리하는 품질 제어 구조라는 점이다.

## Brownfield and runtime support

2026-03-10 소스는 GSD가 브라운필드 코드베이스에서도 `/gsd:map-codebase`를 통해 `STACK.md`, `ARCHITECTURE.md`, `CONVENTIONS.md`, `CONCERNS.md`를 생성한다고 설명한다. 또한 Claude Code, OpenCode, Gemini CLI, Codex 등 멀티 런타임 지원을 전제로 서술한다.

## Claimed strengths

- 구현 전에 사고와 요구사항을 구조화한다.
- 프로젝트 상태를 파일에 남겨 신선한 컨텍스트 재시작이 가능하다.
- 실행과 검증을 분리해 품질과 복구성을 높인다.
- 멀티 에이전트 구조를 속도뿐 아니라 컨텍스트 오염 제어 장치로 사용한다.

## Limits and cautions

- 작은 단일 수정에는 과도할 수 있다.
- 터미널 중심 워크플로우라 GUI 선호 환경과는 맞지 않을 수 있다.
- 현재 근거는 모두 2차 기사이므로, 운영 세부사항은 upstream 문서 기준으로 재확인하는 편이 안전하다.

## Related pages

- [[Context Rot]]
- [[Nyquist Validation]]

## Sources

- [[2026-03-10 GSD Get Shit Done Context Engineering]]
- [[2026-03-19 GSD Multi Agent Plan Verification Update]]
- [[2026-03-26 GSD Context Engineering for Coding Agents]]
