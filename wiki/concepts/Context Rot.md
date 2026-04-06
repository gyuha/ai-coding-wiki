# Context Rot

## Summary

[[Context Rot]]는 긴 AI 코딩 세션이 진행되면서 모델이 이전 결정을 잊고, 관련 없는 코드를 건드리고, 점점 덜 유용한 출력을 내는 현상을 가리킨다. 현재 소스군에서는 GSD가 다루려는 핵심 문제로 반복해서 등장한다.

## Symptoms

현재 소스 기준 context rot의 대표적 징후는 다음과 같다.

- 응답 품질 저하와 짧아지는 출력
- 앞서 내린 결정의 망각
- 무관한 코드 변경이나 일관성 붕괴
- 사용자가 에이전트를 돕기보다 감시하는 데 더 많은 시간을 쓰게 되는 상황

## Mitigation patterns

현재 소스군은 다음과 같은 완화 패턴을 공통적으로 제시한다.

- 긴 단일 세션 대신 bounded phase로 분리하기
- 요구사항, 계획, 상태를 파일에 기록해 외부화하기
- 실행 전에 계획 자체를 검증하기
- heavy lifting을 fresh context 서브에이전트로 분산하기
- 구현 후 사용자 확인과 실패 복구까지를 워크플로우 안에 포함하기

2026-03-19 소스는 특히 멀티 에이전트 구조의 가치를 병렬 속도보다 “메인 컨텍스트 창을 얇게 유지하는 것”에 둔다. 이 점에서 context rot 완화는 단순한 요령이 아니라, 시스템 구조 문제로 다뤄진다.

## Related pages

- [[GSD]]
- [[Nyquist Validation]]

## Sources

- [[2026-03-10 GSD Get Shit Done Context Engineering]]
- [[2026-03-19 GSD Multi Agent Plan Verification Update]]
- [[2026-03-26 GSD Context Engineering for Coding Agents]]
