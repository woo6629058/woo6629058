<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:000000,100:00ff88&height=140&section=header&text=GEONWOO%27s%20GitHub&fontSize=32&fontColor=00ff88&animation=fadeIn&fontAlignY=35"/>

---

## 🛠 Tech Stack

<div align="center">

<img src="https://img.shields.io/badge/Java%2017-007396?style=for-the-badge&logo=openjdk&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring%20Data%20JPA-59666C?style=for-the-badge&logo=hibernate&logoColor=white"/>

<br/>

<img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
<img src="https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white"/>
<img src="https://img.shields.io/badge/Redisson-B82025?style=for-the-badge&logo=redis&logoColor=white"/>

<br/>

<img src="https://img.shields.io/badge/AWS%20EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white"/>
<img src="https://img.shields.io/badge/AWS%20RDS-527FFF?style=for-the-badge&logo=amazonrds&logoColor=white"/>
<img src="https://img.shields.io/badge/AWS%20S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white"/>

<br/>

<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"/>
<img src="https://img.shields.io/badge/GHCR-181717?style=for-the-badge&logo=github&logoColor=white"/>
<img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white"/>

<br/>

<img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white"/>
<img src="https://img.shields.io/badge/Loki-F46800?style=for-the-badge&logo=grafana&logoColor=white"/>
<img src="https://img.shields.io/badge/k6-7D64FF?style=for-the-badge&logo=k6&logoColor=white"/>

</div>

---

## 🌟 Featured Projects

### 🍽️ [URISIK](https://github.com/Urisik-serv/URISIK_BACKEND)

> 알레르기와 식습관이 서로 다른 가족을 위한 AI 기반 맞춤형 식단 관리 서비스

**2025.12.22 – 2026.02.12 · Backend**

#### 담당 역할

- 가족방·초대 토큰·주간 식단 도메인 설계
- Gemini API 기반 AI 식단 생성 파이프라인 설계
- AI 응답 검증 및 실패 대응 fallback 구현
- k6 기반 성능 측정과 병목 분석

#### 주요 구현

- 가족방의 권한·상태 전이·초대 토큰 생명주기를 고려한 정책 중심 도메인 설계
- `후보군 수집 → AI 호출 → 파싱 → 도메인 검증 → fallback` 구조로 AI 생성 책임 분리
- 알레르기 위반·중복 레시피·비정형 응답을 차단하는 검증 로직 구현
- 단계별 로그와 p95 지표를 기반으로 AI generation time 병목 식별 및 개선

<br/>

### ♻️ [ReDO](https://github.com/REDO-Team/Back)

> 분리배출 정보를 쉽고 빠르게 제공하고, 실천에 대한 보상을 통해 사용자의 행동을 유도하는 서비스

**2026.06.29 – 2026.08.21 · Backend · Infrastructure · Monitoring**

#### 담당 역할

- 포인트·리워드·기여도 도메인 개발
- 리워드 구매 동시성 제어 및 데이터 정합성 확보
- AWS 인프라와 CI/CD 파이프라인 구축
- 애플리케이션·인프라 통합 모니터링 구축

#### 주요 구현

- DB 트랜잭션·비관적 락·멱등성 키·Redisson 분산 락을 조합해 포인트와 재고 정합성 보장
- Cache-Aside와 커서 페이지네이션을 적용한 기여도 피드 및 Redis 장애 대응 Fail-Open 구조 구현
- AWS EC2·RDS·S3, Docker Compose, Nginx 기반 운영 환경과 GitHub Actions·GHCR 배포 파이프라인 구축
- Prometheus·Grafana·Loki·Alloy 기반 메트릭·로그 수집과 Discord 장애 알림 구성

<br/>

### ✈️ [QUESPOT](https://github.com/Quespot/BE)

> **In Progress**

---

## 🚀 Activities & Learning

<table align="center" width="85%">
  <colgroup>
    <col width="40%"/>
    <col width="60%"/>
  </colgroup>
  <thead>
    <tr>
      <th align="center">Education &amp; Activities</th>
      <th align="center">Learning Log</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center">
        <strong>가톨릭대학교</strong><br/>
        미디어기술콘텐츠학과, 컴퓨터정보공학부 (GPA 3.87/4.5)<br/>
        <code>2022.03 ~</code>
      </td>
      <td align="center">
        <strong>
          <a href="https://github.com/woo6629058/hello-spring">hello-spring</a>
        </strong><br/>
        Spring Boot, MVC 및 데이터베이스 접근 기술
      </td>
    </tr>
    <tr>
      <td align="center">
        <strong>UMC 9·10·11th</strong><br/>
        SpringBoot 파트 활동<br/>
        <code>2025.09 ~</code>
      </td>
      <td align="center">
        <strong>
          <a href="https://github.com/woo6629058/core">core</a>
        </strong><br/>
        객체 지향 설계와 Spring 핵심 원리
      </td>
    </tr>
    <tr>
      <td align="center">
        <strong>GDGoC 6th</strong><br/>
        공모전 스터디(SpringBoot) 활동<br/>
        <code>2026.03 ~ 2026.06</code>
      </td>
      <td align="center">
        <strong>
          <a href="https://github.com/woo6629058/jpashop">jpashop</a>
        </strong><br/>
        Spring Boot와 JPA를 활용한 웹 애플리케이션 개발
      </td>
    </tr>
  </tbody>
</table>

---

## 📈 GitHub Analytics

<div align="center">

<img width="49%" src="https://github-readme-stats.vercel.app/api?username=woo6629058&show_icons=true&title_color=00ff88&text_color=ffffff&icon_color=00ff88&bg_color=0d1117&border_color=30363d"/>
<img width="49%" src="https://streak-stats.demolab.com?user=woo6629058&theme=dark&ring=00FF88&fire=00FF88&currStreakLabel=00FF88&border=30363D"/>

<br/>

<img width="45%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=woo6629058&layout=compact&title_color=00ff88&text_color=ffffff&bg_color=0d1117&border_color=30363d"/>

</div>

---

## 📫 Connect

<div align="center">

<a href="mailto:woo6629058@catholic.ac.kr">
  <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>
<a href="https://velog.io/@dev_geonwoo">
  <img src="https://img.shields.io/badge/Velog-20C997?style=for-the-badge&logo=velog&logoColor=white"/>
</a>
<a href="https://github.com/woo6629058">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

</div>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:00ff88,100:000000&height=120&section=footer"/>
