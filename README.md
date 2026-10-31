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

- 가족방·초대·주간 식단 도메인을 권한·상태 전이·초대 토큰 생명주기 중심의 정책으로 설계
- Gemini API 기반 `후보군 수집 → AI 호출 → 파싱 → 도메인 검증 → fallback` 구조로 AI 식단 생성 책임 분리
- 알레르기 위반·중복 레시피·비정형 응답을 차단하는 AI 응답 검증 로직 구현, 검증 실패 시 fallback 식단 제공
- k6 부하 테스트와 구간별 실행 시간 로그로 AI 식단 생성 과정을 `프롬프트 구성 → AI 호출 → 파싱 → 검증 → 저장` 단계별로 측정해 p95 기준 병목 구간 분석

<br/>

#### ♻️ [ReDO](https://github.com/REDO-Team/Back)

> 분리배출은 쉽게, 실천은 보상으로 이어져 환경 보호를 일상의 습관으로 만드는 서비스

**2026.06 – 2026.08 · Backend · Infrastructure · Monitoring**

##### 주요 구현

- DB 트랜잭션·비관적 락·멱등성 키·Redisson 분산 락을 조합해 리워드 구매 동시성 상황에서도 포인트와 재고 정합성 보장
- Cache-Aside와 커서 페이지네이션을 적용한 기여도 피드 구현, Redis 장애 시에도 서비스가 멈추지 않는 Fail-Open 구조 적용
- AWS EC2·RDS·S3, Docker Compose, Nginx 기반 운영 환경과 GitHub Actions·GHCR 기반 CI/CD 파이프라인 구축
- Prometheus·Grafana·Loki·Alloy 기반 메트릭·로그 수집과 Discord 장애 알림 구성
- Docker 기반 공통 k6 환경에 Smoke·Load·Stress 프로파일과 성능 임계치, 원격·쓰기 테스트 안전장치 구축
- 리워드·포인트·기여도 API를 최대 50 VU, 총 36,168건의 요청으로 검증해 `오류율 0%, p95 최대 114.70ms` 달성

<br/>

#### ✈️ [QUESPOT](https://github.com/Quespot/BE)

> 전국 방방곡곡, 미션으로 떠나는 관광 서비스

**2026.08 – 2026.09 · Backend · Infrastructure · Monitoring**

##### 주요 구현

- 이메일·JWT 인증과 Google·Kakao·Naver OAuth 로그인, 계정 연결·해제 및 외부 계정 연동 해제 실패 재시도 구조 구현
- 한국관광공사 TourAPI 기반 `수집 → 스팟 정제·행정구역 매핑 → 미션 후보 생성·검수 → 미션 발행` 데이터 파이프라인 구축
- 거리·카테고리·여행 스타일 기반 미션 탐색·추천과 HMAC 서명 커서 페이지네이션, 지역 스팟·여행 아카이브 조회 구현
- AWS EC2·RDS·ECR·S3, Docker Compose 기반 운영 환경과 GitHub Actions 기반 CI/CD 파이프라인 구축
- Spring Actuator·Prometheus·Grafana Cloud·Alloy 기반 API·JVM·DB 모니터링과 Discord 장애 알림 구성

##### 성능 개선

- 운영과 동일한 힙·커넥션 풀 조건의 Docker 기반 측정 환경과 미션 10만 건 시드, 실제 JWT·Redis 세션 인증을 거치는 k6 부하 테스트 구축
- 요청마다 전체 미션의 거리를 계산·정렬하는 병목을 실행 계획으로 확인하고, 반경 단계 확장과 B-tree 복합 인덱스를 적용해 초당 20명 부하에서 `p95 19.1s → 27ms, 처리량 10.6 → 60 req/s` 개선
- 재측정에서 위도 범위만 좁히는 B-tree의 한계로 미션이 드문 지역의 p95가 4.07s에 머무는 것을 확인하고 공간 인덱스(R-tree)로 전환해 `드문 지역 p95 4.07s → 21ms, 도시 지역 p95 20ms` 달성

<br/>

#### 🤝🏻 [IT:SSUM](https://github.com/IT-SSUM)

> 기부자와 복지기관을 연결하는 물품 기부 매칭 서비스

**2026.10 – 진행 중 · Backend**

##### 주요 구현

- `응답 대기 → 거래중 → 예약중 → 전달 완료` 매칭 상태 전이 설계, 수량 예약·완료·취소 시 비관적 락으로 기부 물품·필요 물품 수량 정합성 보장
- Spring WebSocket·STOMP 기반 거래별 1:1 채팅 구현, `AFTER_COMMIT` 이벤트로 DB 저장이 확정된 메시지만 브로커로 전송해 롤백된 메시지 전달 방지
- 메시지 전송 시 매칭 → 채팅방 순서로 비관적 락을 걸고 거래 상태를 재확인해, 전송 도중 거래가 취소·완료되면 메시지 저장 차단
- S3 Presigned URL 이미지 전송 시 채팅방별 키 범위와 실제 업로드 객체의 크기·형식을 서버에서 재검증해 다른 방 이미지 참조·형식 위장 업로드 차단

---

### GitHub Analytics.
<div align="left">
  <img height="170" src="https://github-stats-extended.vercel.app/api?username=woo6629058&show_icons=true&theme=dark&hide_border=true"/>
  <img height="170" src="https://streak-stats.demolab.com?user=woo6629058&theme=dark&ring=00FF88&fire=00FF88&currStreakLabel=00FF88&border=30363D&hide_border=true"/>
</div>
