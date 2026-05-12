# Korea for Visitors API

Backend API for a Korea travel guide service aimed at international visitors.
It supports social login, AI travel assistance, and guest-guide matching features for the service at:

[Live service](https://korea-travel-guide.vercel.app/ko)

## Overview

Korea for Visitors is a team MVP project that connects visitors with useful Korea travel information and local guide interactions. This repository focuses on the backend system: authentication, AI chat, matching, realtime communication, and API documentation.

## Key Features

- Social login with OAuth 2.0: Google, Kakao, and Naver
- AI travel assistant using Spring AI and OpenRouter-compatible models
- Tour and weather data lookup through dedicated AI tools
- Guest-guide matching flow for visitor and guide interactions
- Realtime chat foundation with WebSocket and RabbitMQ
- Redis-based caching/session support
- PostgreSQL production database support with H2 for local development
- Swagger/OpenAPI documentation for API exploration
- DDD-inspired package structure with Kotlin and Spring Boot

## Tech Stack

| Area | Stack |
| --- | --- |
| Language | Kotlin 1.9.25, Java 21 |
| Framework | Spring Boot 3.4.1, Spring Security, Spring Data JPA |
| AI | Spring AI 1.1.0-M2, OpenRouter/OpenAI-compatible API |
| Database | PostgreSQL, H2 |
| Realtime / Messaging | WebSocket, RabbitMQ |
| Cache / Session | Redis, Spring Session Redis |
| Docs / Quality | springdoc-openapi, ktlint, JUnit5, MockK |

## Architecture Notes

- Domain-oriented structure to keep business logic separated from API and infrastructure concerns
- Spring Security and OAuth clients for multi-provider authentication
- YAML-driven travel metadata and prompts converted into build-time configuration constants
- Separate local and production database profiles
- API documentation exposed through Swagger UI for faster frontend/backend collaboration

## Getting Started

```bash
# 1. Configure environment variables
cp .env.example .env

# 2. Run the backend server
./gradlew bootRun

# 3. Open API documentation
# http://localhost:8080/swagger-ui.html
```

## Development Commands

```bash
# Run tests
./gradlew test

# Check Kotlin formatting
./gradlew ktlintCheck

# Apply Kotlin formatting
./gradlew ktlintFormat
```

## Documentation

- [Development rules](docs/DEVELOPMENT_RULES.md)
- [Global configuration guide](docs/GLOBAL_CONFIG.md)
- [Redis guide](docs/REDIS_GUIDE.md)
- [Project structure](docs/project-structure.md)
- [ERD diagram](docs/erd-diagram.md)
- [API specification](docs/api-specification.yaml)

## Team

Team 11, Cheongi Nuseol.
