<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&color=7F5AF0&size=28&center=true&vCenter=true&width=650&height=45&lines=Backend+Engineer;Spring+Boot+%2B+Spring+AI;Concurrency+%26+Secure+API+Design;Building+Production-Style+Systems"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <a href="https://www.linkedin.com/in/pranshu-patel-gec-ldce-it-dte">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white"/>
  </a>
  <a href="mailto:pranshu2853@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white"/>
  </a>
</p>

---

# 💫 About Me

Backend engineer building production-style systems with Spring Boot — focused on
concurrency control, secure API design, and clean layered architecture.
IT undergrad at L.D. College of Engineering, Ahmedabad (2027).

## 🔭 Currently Working On

**QuerySense** — an LLM-powered SQL analytics agent
- Schema-grounded NL→SQL generation via pgvector embedding similarity search
- Parser-level query safety with JSQLParser + isolated read-only datasource
- Multi-service Docker Compose stack with health-checked startup ordering

---

## 🚧 Featured Projects

### 🔹 QuerySense — Intelligent SQL Analytics Agent *(In Progress)*

<!-- Uncomment once the repo is pushed public -->
<!-- [![Repo](https://img.shields.io/badge/Code-181717?style=flat-square&logo=github)](https://github.com/pranshu-2853/querysense) -->

`Spring AI` `PostgreSQL` `pgvector` `Redis` `Docker`

- Converts natural-language business questions into SQL using Spring AI with Llama 3.3 via Groq
- Grounds generation on database schema context retrieved through pgvector embedding search
- Enforces SQL safety on LLM output via JSQLParser validation before execution
- Dedicated read-only analytics datasource isolates AI-executed queries from the app database
- Orchestrated Spring Boot + dual PostgreSQL + Redis + Ollama embedding server via Docker Compose

### 🔹 Ticket Booking System

[![Repo](https://img.shields.io/badge/Code-181717?style=flat-square&logo=github)](https://github.com/pranshu-2853/ticket-booking-system)

`Spring Boot` `PostgreSQL` `Redis` `Resilience4j` `Flyway` `JUnit 5`

- High-concurrency booking backend built as a modular monolith
- Pessimistic locking (`PESSIMISTIC_WRITE`) as the correctness guarantee, Redis soft locking
  (`SET NX EX`) as an optimization layer — falls back to DB locking if Redis is unavailable
- Validated with an 8-thread / 1-seat concurrency test (ExecutorService + CountDownLatch):
  exactly 1 booking persisted, 0 race conditions, stable across `@RepeatedTest(3)`
- Resilience4j Circuit Breaker + Retry on payment calls with explicit aspect ordering;
  circuit opens at 50% failure rate over a 5-call sliding window
- Idempotency keys on booking endpoints, results cached in Redis for 24h
- 6 versioned Flyway migrations · 80+ automated tests · Docker Compose · deployed on Render

### 🔹 Secure Engineer Management API

[![Repo](https://img.shields.io/badge/Code-181717?style=flat-square&logo=github)](https://github.com/pranshu-2853/secure-engineer-management-api)

`Spring Boot` `Spring Security` `PostgreSQL` `Docker` `JUnit 5` `Mockito`

- 10+ secured endpoints on a layered architecture (Controller → Service → Repository)
- JWT authentication + method-level RBAC via `@PreAuthorize` (ADMIN/USER)
- Dynamic filtering with JPA Specifications, server-side pagination & sorting
- DTO layer to eliminate sensitive field exposure from API responses
- Centralized exception handling via `@RestControllerAdvice` — 7 custom exception types
  mapped to 400/401/403/404/409
- 90%+ service-layer test coverage, MockMvc integration tests, Swagger/OpenAPI docs
- Deployed on Render with Neon PostgreSQL

---

## 💻 Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=java,spring,postgres,mysql,redis,docker,git,maven,js,react,html,css&theme=dark" />
</p>

## 🌱 Currently Learning

- Retrieval grounding for LLM applications (embeddings, schema context, safety layers)
- Hibernate/JPA internals — fetch strategies, N+1, transaction propagation
- SQL beyond CRUD — joins, aggregation, window functions

## 🤝 Open to Collaboration

- Backend system design
- Concurrency-safe REST architecture
- Spring AI / LLM-backed developer tooling
- Full-stack work where the backend is Java — comfortable with React on the frontend
    

---

<p align="center">
  <sub>Ahmedabad, India · Open to backend engineering roles</sub>
</p>
