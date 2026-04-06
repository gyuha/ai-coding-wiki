# Nyquist Validation

## Summary

[[Nyquist Validation]]은 현재 소스군에서 [[GSD]]의 계획 단계 품질 게이트로 설명된다. 핵심 아이디어는 코드를 쓰기 전에 요구사항 대비 테스트 계획의 커버리지가 충분한지 점검하는 것이다.

## Core idea

2026-03-10 소스는 Nyquist validation을 요구사항과 테스트 계획을 매핑하고, 커버리지 점수를 계산하며, 누락된 테스트를 보완 권고로 되돌리는 구조로 설명한다. 즉 구현 후 테스트가 아니라, 구현 전 계획 검증이 중심이다.

## Relation to planning

2026-03-19 소스는 planner → checker → revise 루프를 강조하면서, 잘못된 코드를 디버깅하기 전에 잘못된 계획을 먼저 잡아내는 방향을 설명한다. 이 맥락에서 Nyquist validation은 checker가 확인하는 검증 철학의 일부로 이해하는 편이 맞다.

## Related behavior

- 계획을 독립적인 검증 대상으로 취급한다.
- 테스트 계획이 요구사항을 충분히 덮는지 본다.
- 필요하면 `/gsd:validate-phase` 같은 소급 검증 흐름으로도 이어질 수 있다.

## Related pages

- [[GSD]]
- [[Context Rot]]

## Sources

- [[2026-03-10 GSD Get Shit Done Context Engineering]]
- [[2026-03-19 GSD Multi Agent Plan Verification Update]]
