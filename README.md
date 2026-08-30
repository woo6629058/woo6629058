## Geonwoo Heo

### Activities.
- `2026.09 -` IT 연합 사이드 프로젝트 동아리 UMC 11기 · Product Engineering 파트 (CUK 운영진)
- `2026.03 - 2026.08` IT 연합 사이드 프로젝트 동아리 [UMC 10기](https://github.com/UMC-CUK-10th) · Spring Boot 파트 (스터디장 & 프로젝트 팀장)
- `2026.03 - 2026.06` GDG on Campus CUK 6기 · Spring Boot 기반 프로젝트 스터디
- `2025.09 - 2026.02` IT 연합 사이드 프로젝트 동아리 [UMC 9기](https://github.com/UMC-CUK-9th) · Spring Boot 파트

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

**2025.12.22 – 2026.02.12 · Backend**

##### 담당 역할

- 가족방·초대 토큰·주간 식단 도메인 개발
- Gemini API 기반 AI 식단 생성 파이프라인 구축
- AI 응답 검증 및 실패 대응 fallback 구현
- k6 기반 성능 측정과 병목 분석

##### 주요 구현

- 가족방의 권한·상태 전이·초대 토큰 생명주기를 고려한 정책 중심 도메인 설계
- `후보군 수집 → AI 호출 → 파싱 → 도메인 검증 → fallback` 구조로 AI 생성 책임 분리
- 알레르기 위반·중복 레시피·비정형 응답을 차단하는 검증 로직 구현
- 단계별 로그와 p95 지표를 기반으로 AI generation time 병목 식별 및 개선

<br/>

#### ♻️ [ReDO](https://github.com/REDO-Team/Back)

> 분리배출은 쉽게, 실천은 보상으로 이어져 환경 보호를 일상의 습관으로 만드는 서비스

**2026.06.29 – 2026.08.21 · Backend · Infrastructure · Monitoring**

##### 담당 역할

- 포인트·리워드·기여도 도메인 개발
- 리워드 구매 동시성 제어 및 데이터 정합성 확보
- AWS 인프라와 CI/CD 파이프라인 구축
- 애플리케이션·인프라 통합 모니터링 구축

##### 주요 구현

- DB 트랜잭션·비관적 락·멱등성 키·Redisson 분산 락을 조합해 포인트와 재고 정합성 보장
- Cache-Aside와 커서 페이지네이션을 적용한 기여도 피드 및 Redis 장애 대응 Fail-Open 구조 구현
- AWS EC2·RDS·S3, Docker Compose, Nginx 기반 운영 환경과 GitHub Actions·GHCR 배포 파이프라인 구축
- Prometheus·Grafana·Loki·Alloy 기반 메트릭·로그 수집과 Discord 장애 알림 구성

<br/>

#### ✈️ [QUESPOT](https://github.com/Quespot/BE)

> 전국 방방곡곡, 미션으로 떠나는 관광 서비스

- **In Progress**

---

### GitHub Analytics.
<div align="left">
  <img height="170" src="https://github-stats-extended.vercel.app/api?username=woo6629058&show_icons=true&theme=dark&hide_border=true"/>
  <img height="170" src="https://streak-stats.demolab.com?user=woo6629058&theme=dark&ring=00FF88&fire=00FF88&currStreakLabel=00FF88&border=30363D&hide_border=true"/>
</div>
