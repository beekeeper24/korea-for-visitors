# 한국 여행 가이드 API

외국인 관광객을 위한 한국 여행 가이드 서비스의 백엔드 API입니다.
소셜 로그인, AI 여행 도우미, 여행 정보 조회, 게스트-가이드 매칭, 실시간 채팅 기능을 담당합니다.

[서비스 바로가기](https://korea-travel-guide.vercel.app/ko)

---

## 프로젝트 소개

`korea-for-visitors`는 한국을 방문하는 외국인 관광객이 여행 정보를 더 쉽게 찾고, 현지 가이드와 연결될 수 있도록 만든 팀 MVP 프로젝트입니다.

이 저장소는 서비스의 백엔드 영역을 담당하며, 인증/인가, AI 채팅, 관광/날씨 데이터 연동, 유저/가이드 도메인, 채팅방 및 메시지 흐름, API 문서화를 포함합니다.

---

## 주요 기능

- Google, Kakao, Naver OAuth2 기반 소셜 로그인
- JWT 기반 인증/인가 처리
- Spring AI 기반 AI 여행 상담 기능
- 관광지/날씨 정보 조회를 위한 AI Tool 연동
- 게스트와 가이드 매칭을 위한 사용자/가이드 도메인
- WebSocket 기반 실시간 채팅 구조
- RabbitMQ 기반 메시지 발행 구조
- Redis 기반 캐싱 및 세션 관리
- PostgreSQL 운영 DB, H2 개발 DB 지원
- Swagger/OpenAPI 기반 API 문서 제공

---

## 기술 스택

| 구분 | 기술 |
| --- | --- |
| Language | Kotlin 1.9.25, Java 21 |
| Framework | Spring Boot 3.4.1, Spring Security, Spring Data JPA |
| AI | Spring AI 1.1.0-M2, OpenRouter/OpenAI 호환 API |
| Database | PostgreSQL, H2 |
| Realtime / Messaging | WebSocket, RabbitMQ |
| Cache / Session | Redis, Spring Session Redis |
| Docs / Quality | springdoc-openapi, ktlint, JUnit5, MockK |

---

## 아키텍처 특징

- 도메인별 패키지 구조로 API, 서비스, 엔티티, 저장소 책임 분리
- Spring Security와 OAuth2 Client를 활용한 다중 소셜 로그인 구성
- 여행 지역/콘텐츠 타입/언어/프롬프트 설정을 YAML로 관리
- 관광/날씨 API를 AI 도구로 연결해 대화형 여행 정보 제공
- 개발 환경과 운영 환경의 DB 설정 분리
- Swagger UI를 통해 프론트엔드와 빠르게 API 계약 확인 가능

---

## 실행 방법

```bash
# 1. 환경 변수 설정
cp .env.example .env

# 2. 서버 실행
./gradlew bootRun

# 3. API 문서 확인
# http://localhost:8080/swagger-ui.html
```

---

## 개발 명령어

```bash
# 테스트 실행
./gradlew test

# Kotlin 포맷 검사
./gradlew ktlintCheck

# Kotlin 포맷 자동 수정
./gradlew ktlintFormat
```

---

## 문서

- [개발 규칙](docs/DEVELOPMENT_RULES.md)
- [글로벌 설정 가이드](docs/GLOBAL_CONFIG.md)
- [Redis 사용 가이드](docs/REDIS_GUIDE.md)
- [프로젝트 구조](docs/project-structure.md)
- [ERD 다이어그램](docs/erd-diagram.md)
- [API 명세서](docs/api-specification.yaml)

---

## 팀 정보

11팀 천기누설
