## Geonwoo Heo

### Activities.
- `2026.09 -` 대학생 IT 연합 사이드 프로젝트 동아리 [UMC 11기](https://github.com/UMC-CUK-11th) · Product Engineering 파트 (운영진 & 스터디장)
- `2026.03 - 2026.08` 대학생 IT 연합 사이드 프로젝트 동아리 [UMC 10기](https://github.com/UMC-CUK-10th) · Spring Boot 파트 (스터디장 & 프로젝트 팀장)
- `2026.03 - 2026.06` GDG on Campus CUK 6기 · Spring Boot 기반 프로젝트 스터디
- `2025.09 - 2026.02` 대학생 IT 연합 사이드 프로젝트 동아리 [UMC 9기](https://github.com/UMC-CUK-9th) · Spring Boot 파트

<br/>

### Skills.
<p>
  <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white"/>
  <br/>
  <img src="https://img.shields.io/badge/Amazon%20AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/>
</p>

<br/>

### Featured Projects.

#### 🍽️ [URISIK](https://github.com/Urisik-serv/URISIK_BACKEND)

> 알레르기와 식습관이 서로 다른 가족을 위한 AI 기반 맞춤형 식단 관리 서비스

**2025.12 – 2026.02 · Backend**

##### 주요 구현

- 주간 식단 `임시 → 확정` 전이에 락·주차별 유니크 제약을 적용해 중복 생성·이중 확정 차단
- Gemini API 기반 `후보군 수집 → AI 호출 → 파싱 → 도메인 검증 → fallback` 구조로 AI 식단 생성 책임 분리
- 안전 후보군 제한·AI 응답 검증·fallback 식단을 조합해 알레르기 위반·중복 레시피·비정형 응답이 사용자에게 노출되는 문제 차단
- k6·구간별 실행 시간 로그로 AI 식단 생성 과정의 단계별 p95를 측정해 병목 구간 분석

<br/>

#### ♻️ [ReDO](https://github.com/REDO-Team/Back)

> 분리배출은 쉽게, 실천은 보상으로 이어져 환경 보호를 일상의 습관으로 만드는 서비스

**2026.06 – 2026.08 · Backend · Infrastructure · Monitoring**

##### 주요 구현

- Redisson 분산 락·비관적 락·멱등성 키를 조합해 리워드 구매 동시성·중복 요청 상황에서도 포인트와 재고 정합성 보장
- 기여도 피드에 Cache-Aside·커서 페이지네이션 적용, Redis 장애 시 DB 조회로 전환하는 Fail-Open 구조 설계
- AWS EC2·RDS·S3, Docker Compose, Nginx 기반 운영 환경과 GitHub Actions·GHCR 기반 CI/CD 파이프라인 구축
- Prometheus·Grafana·Loki·Alloy 기반 메트릭·로그 수집과 Discord 장애 알림 구성
- Docker 기반 공통 k6 환경에 Smoke·Load·Stress 프로파일과 성능 임계치, 원격·쓰기 테스트 안전장치 구축
- 리워드·포인트·기여도 API를 최대 50 VU, 총 36,168건의 요청으로 검증해 `오류율 0%, p95 최대 114.70ms` 달성

<br/>

#### ✈️ [QUESPOT](https://github.com/Quespot/BE)

> 관광지를 직접 방문해 미션을 수행하며 지역을 탐험하는 참여형 관광 서비스

**2026.08 – 2026.11 · Backend · Infrastructure · Monitoring**

##### 주요 구현

- JWT 세션 ID를 Redis 세션과 대조하는 인증 구조로 로그아웃·탈퇴 시 액세스 토큰 즉시 무효화
- Outbox 패턴·지수 백오프 재시도로 소셜 연동 해제 실패 시에도 외부 연동 잔존 방지
- TourAPI 기반 `수집 → 정제·행정구역 매핑 → 후보 검수 → 미션 발행` 파이프라인 구축, 체크포인트·호출 한도 관리로 중단 지점부터 재개
- 미션 목록 조회 조건·정렬 seed를 HMAC 서명 커서에 바인딩해 조건 변경·위조 커서 재사용과 페이지 간 중복·누락 방지
- AWS EC2·RDS·ECR·S3, Docker Compose 기반 운영 환경과 GitHub Actions 기반 CI/CD 파이프라인 구축
- Spring Actuator·Prometheus·Grafana Cloud·Alloy 기반 API·JVM·DB 모니터링과 Discord 장애 알림 구성

##### 성능 개선

- Docker·k6로 운영과 동일한 힙·커넥션 풀 조건과 실제 JWT·Redis 세션 인증을 재현한 부하 테스트 환경 구축
- `EXPLAIN ANALYZE`로 전체 미션 거리 계산·정렬 병목 확인
  - 반경 단계 확장·B-tree 복합 인덱스로 미션 10만 건·초당 20명 부하에서 `p95 19.1s → 27ms, 처리량 10.6 → 60 req/s` 개선
- 드문 지역에서 위도 범위만 좁히는 B-tree 한계 확인
  - 공간 인덱스(R-tree)로 `드문 지역 p95 4.07s → 21ms, 도시 지역 p95 20ms` 달성
- TourAPI 파이프라인의 건별 트랜잭션·전체 재처리 병목 확인
  - 변경분 선별·청크 트랜잭션으로 4만 건 기준 `재동기화 36.2s → 0.92s, 최초 적재 150s → 30s` 단축

<br/>

#### 🤝🏻 [IT:SSUM](https://github.com/IT-SSUM/BE)

> 기부자와 복지기관을 연결하는 물품 기부 매칭 서비스

**2026.10 – 진행 중 · Backend**

##### 주요 구현

- `응답 대기 → 거래중 → 예약중 → 전달 완료` 매칭 상태 전이 설계, 비관적 락으로 매칭 동시성 상황에서도 기부·필요 물품 수량 정합성 보장
- 거래별 1:1 STOMP 채팅 메시지를 `AFTER_COMMIT` 이벤트로 발행해 롤백된 메시지 전달 방지
- 매칭·채팅방 비관적 락과 상태 재검증을 조합해 거래 취소·완료 중 전송된 메시지의 저장 차단
- S3 Presigned URL 조건부 업로드와 서버 측 객체 검증을 조합해 이미지 덮어쓰기·위장 업로드·타 채팅방 이미지 참조 차단

---

### GitHub Analytics.
<div align="left">
  <img height="170" src="https://github-stats-extended.vercel.app/api?username=woo6629058&show_icons=true&theme=dark&hide_border=true"/>
  <img height="170" src="https://streak-stats.demolab.com?user=woo6629058&theme=dark&ring=00FF88&fire=00FF88&currStreakLabel=00FF88&border=30363D&hide_border=true"/>
</div>
