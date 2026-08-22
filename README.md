<img src="https://capsule-render.vercel.app/api?type=waving&color=0:7f5af0,100:2cb67d&height=120&section=header"/>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?color=7F5AF0&size=28&center=true&vCenter=true&width=600&lines=Backend+Engineer;Spring+Boot+%2B+Spring+AI;Concurrency+%26+Secure+API+Design;Building+Production-Style+Systems"/>
</p>

# 💫 About Me

Backend engineer building production-style systems with Spring Boot — focused on
concurrency control, secure API design, and clean layered architecture.
IT undergrad at L.D. College of Engineering, Ahmedabad (2027).

## 🔭 Currently Working On

**QuerySense** — an LLM-powered SQL analytics agent
- Schema-grounded NL→SQL generation via pgvector embedding similarity search
- Parser-level query safety with JSQLParser + isolated read-only datasource
- Multi-service Docker Compose stack with health-checked startup ordering

## 🚧 Featured Projects

### 🔹 QuerySense — Intelligent SQL Analytics Agent *(In Progress)*
`Spring AI` `PostgreSQL` `pgvector` `Redis` `Docker`
- Converts natural-language business questions into SQL using Spring AI with Llama 3.3 via Groq
- Grounds generation on database schema context retrieved through pgvector embedding search
- Enforces SQL safety on LLM output via JSQLParser validation before execution
- Dedicated read-only analytics datasource isolates AI-executed queries from the app database
- Orchestrated Spring Boot + dual PostgreSQL + Redis + Ollama embedding server via Docker Compose

### 🔹 Ticket Booking System
`Spring Boot` `PostgreSQL` `Redis` `Resilience4j` `Flyway` `JUnit 5`
- High-concurrency booking backend built as a modular monolith
- Pessimistic locking (`PESSIMISTIC_WRITE`) as the correctness guarantee, Redis soft locking
  (`SET NX EX`) as an optimization layer — falls back to DB locking if Redis is unavailable
- Validated with an 8-thread / 1-seat concurrency test (ExecutorService + CountDownLatch):
  exactly 1 booking persisted, 0 race conditions, stable across `@RepeatedTest(3)`
- Resilience4j Circuit Breaker + Retry on payment calls with explicit aspect ordering;
  circuit opens at 50% failure rate over a 5-call sliding window
- Idempotency keys on booking endpoints, results cached in Redis for 24h
- 6 versioned Flyway migrations · 80+ automated tests · Docker Compose · deployed on Railway

### 🔹 Secure Engineer Management API
`Spring Boot` `Spring Security` `PostgreSQL` `Docker` `JUnit 5` `Mockito`
- 10+ secured endpoints on a layered architecture (Controller → Service → Repository)
- JWT authentication + method-level RBAC via `@PreAuthorize` (ADMIN/USER)
- Dynamic filtering with JPA Specifications, server-side pagination & sorting
- DTO layer to eliminate sensitive field exposure from API responses
- Centralized exception handling via `@RestControllerAdvice` — 7 custom exception types
  mapped to 400/401/403/404/409
- 90%+ service-layer test coverage, MockMvc integration tests, Swagger/OpenAPI docs
- Deployed on Render with Neon PostgreSQL

<p align="center">
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white"/>
  <img src="https://img.shields.io/badge/REST_APIs-02569B?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/JWT_Security-FC4C02?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Spring_AI-0F9D58?style=for-the-badge"/>
</p>

## 🌱 Currently Learning

- Retrieval grounding for LLM applications (embeddings, schema context, safety layers)
- Hibernate/JPA internals — fetch strategies, N+1, transaction propagation
- SQL beyond CRUD — joins, aggregation, window functions

## 🤝 Open to Collaboration

- Backend system design
- Concurrency-safe REST architecture
- Spring AI / LLM-backed developer tooling

## 🌐 Socials

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pranshu-patel-gec-ldce-it-dte)
[![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:pranshu2853@gmail.com)

## 💻 Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=java,spring,postgres,mysql,redis,docker,git,maven,js,react,html,css&theme=dark" />
</p>

## 📊 GitHub Stats

![](https://github-readme-stats.vercel.app/api?username=pranshu-2853&theme=nightowl&hide_border=false&include_all_commits=false&count_private=false)
![](https://streak-stats.demolab.com?user=pranshu-2853&theme=nightowl&hide_border=false)
![](https://github-readme-stats.vercel.app/api/top-langs/?username=pranshu-2853&theme=nightowl&hide_border=false&layout=compact)

## ⚡ GitHub Activity Graph

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=pranshu-2853&theme=tokyo-night"/>
</p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:7f5af0,100:2cb67d&height=120&section=footer"/>
