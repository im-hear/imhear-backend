# imhear-backend

ImHear의 Java 21 · Spring Boot · MySQL · Redis · Kafka 저장소입니다. 담당 범위는 B의 인증·권한·모의계좌·거래·알림·SSE, A의 금융 조회 계약입니다.

## 계약과 검증

사용자 승인, 멱등성, 착오 방지 검사는 Spring Boot가 담당한다. 주문, 잔고, 원장 및 Outbox 일관성은 MySQL 트랜잭션에서 보장한다.

인수 검증 기준은 타 사용자 승인 거부, 동시 중복 승인에서 체결 1건, stale 시세 거절, SSE 재연결과 사용자별 이력 격리입니다.

현재 폴더에는 협업 설정이 들어 있습니다. 서비스 코드와 테스트 하네스가 추가되면 이 위치에 설치, 실행, 검사 명령을 기록합니다. 네 저장소를 함께 여는 경우 상위 작업공간의 `docs/architecture/README.md`와 `docs/team-workflow.md`에서 공용 설계와 PR 흐름을 확인할 수 있습니다.

[에이전트 개발 지침](AGENTS.md)
