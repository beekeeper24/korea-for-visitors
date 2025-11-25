# 🇰🇷 한국 여행 가이드 API (Backend)

https://korea-travel-guide.vercel.app/ko

> OAuth 인증, AI 채팅, Guest-Guide 매칭이 가능한 한국 여행 가이드 백엔드 (MVP)

## 📋 주요 특징

- **아키텍처**: 도메인 주도 설계 (DDD)
- **기술 스택**: Spring Boot 3.4.1, Kotlin 1.9.25, Spring AI 1.0.0-M6
- **데이터베이스**: H2 (개발용), PostgreSQL (운영용)
- **인증**: OAuth 2.0 (Google, Kakao, Naver)
- **AI**: OpenRouter + 다양한 모델 (경제적, 확장성)

## 🚀 빠른 시작

```bash
# 1. 환경 설정
cp .env.example .env

# 2. 서버 실행
./gradlew bootRun

# 3. API 확인
# - Swagger UI: http://localhost:8080/swagger-ui.html
# - H2 Console: http://localhost:8080/h2-console
```

## 🔀 개발 규칙

### Branch 네이밍
```
{type}/{scope}/{issue-number}
```
**예시**: `feat/be/12`, `fix/fe/23`

### Commit 메시지
```
{type}({scope}): {summary}
```
**예시**: `feat(be): 사용자 API 구현`

### PR 제목
```
{type}({scope}): {summary} (#{issue-number})
```
**예시**: `feat(be): 사용자 API 구현 (#12)`

### 코드 포맷팅 설정
```bash
# 팀원 최초 설정 (1회)
./setup-git-hooks.sh    # Linux/Mac
setup-git-hooks.bat     # Windows

# 수동 실행
./gradlew ktlintCheck   # 검사
./gradlew ktlintFormat  # 자동 수정
```

## 📖 상세 문서

- [📋 개발 규칙 상세](docs/DEVELOPMENT_RULES.md)
- [📋 글로벌 설정 사용법](docs/GLOBAL_CONFIG.md)
- [🔴 Redis 사용 가이드](docs/REDIS_GUIDE.md)
- [🏗️ 프로젝트 구조](docs/project-structure.md)
- [🗄️ ERD 다이어그램](docs/erd-diagram.md)
- [📄 API 명세서](docs/api-specification.yaml)

## 👥 팀 정보

11팀 천기누설 입니다.

---

**마지막 업데이트** | 2025-09-24 | v1.0 (DDD 아키텍처 + Spring AI)
