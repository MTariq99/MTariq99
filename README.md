 <div align="center">

  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=15&duration=3500&pause=1400&color=67E8F9&center=true&vCenter=true&width=620&lines=Go+Backend+Engineer;Distributed+Systems+%26+Microservices;AI%2FLLM+Application+Engineering" alt="Professional headline" />

  <h1>Muhammad Tariq</h1>

  <p>
    <strong>Backend Engineer (Go) · AI/LLM Application Engineering</strong>
  </p>

  Building reliable backend systems and exploring practical AI applications.
  <br />
  Islamabad, Pakistan

  <br /><br />

  <a href="https://muhammad-tariq.vercel.app/">Portfolio ↗</a>
  &nbsp; · &nbsp;
  <a href="https://github.com/MTariq99">GitHub ↗</a>
  &nbsp; · &nbsp;
  <a href="https://github.com/MTariq99/MTariq99/raw/main/assets/Muhammad_Tariq_Resume_AI.pdf">Resume ↗</a>
  &nbsp; · &nbsp;
  <a href="https://www.linkedin.com/in/mtariq99/">LinkedIn ↗</a>

</div>

<br />

## About

Backend engineer with **5+ years of professional experience** building Go and Node.js distributed systems, gRPC microservices, event-driven pipelines, and real-time platforms.

I'm expanding into AI application engineering through personal projects focused on retrieval-augmented generation, grounded LLM responses, evaluation, and secure tool orchestration.

My focus is on integrating AI into backend systems without compromising security, reliability, or application-owned business logic.

## Selected work

### `01` &nbsp; Retrievion

**Multi-tenant RAG backend · Go**

A working prototype for grounded question answering over private PDFs, with asynchronous ingestion, hybrid retrieval, citations, and evaluation.

**Retrieval & ingestion**
- Tenant-scoped SHA-256 deduplication and versioned document storage using Backblaze B2.
- RabbitMQ ingestion jobs with a dead-letter queue, page-aware parent/child chunking, and batched Gemini embeddings.
- PostgreSQL hybrid retrieval using pgvector cosine similarity with HNSW and full-text search with GIN.
- Reciprocal Rank Fusion (RRF) and a token-bounded context budget.

**Grounded generation & evaluation**
- Server-Sent Events (SSE) streaming with citation resolution to source chunks, documents, and pages.
- Dataset-driven evaluation measuring Precision@K, Recall@K, and MRR.
- LLM-as-judge faithfulness evaluation, persisted results, and baseline comparisons.
- Prometheus metrics, OpenTelemetry, and Sentry instrumentation.

<sub>Go · PostgreSQL · pgvector · Redis · RabbitMQ · Gemini · Prometheus</sub>

[View source code →](https://github.com/MTariq99/retrievion)

<sub>Status: working prototype. Evaluation results are not yet reported; cross-encoder reranking and additional hardening remain planned.</sub>

---

### `02` &nbsp; DispatchAI

**LLM orchestration engine · Go**

An early-stage orchestration engine that connects LLM-generated tool proposals to host-owned application logic through explicit integration boundaries.

**Orchestration & security**
- Bounded tool-calling loop, conversation coordination, and a versioned per-integration tool registry.
- ECDSA P-256 / SHA-256 signed requests with timestamp validation and nonce-based replay protection.
- Request-body hash binding and integration key enrollment.
- Request idempotency using fingerprints, run lifecycle management, and tool-call idempotency keyed by run and call ID.
- Ports-and-adapters architecture with a provider-agnostic LLM interface and Gemini adapter.

**Design principle**

LLMs propose actions; the host application remains responsible for validating and authorizing tool calls. Exactly-once effects across external host systems are not guaranteed.

<sub>Go · LLM Integration · ECDSA · API Security · Idempotency</sub>

[View source code →](https://github.com/MTariq99/dispatchai)

<sub>Status: early-stage prototype. Approval workflows, audit and observability, key rotation, and further security hardening remain planned.</sub>

---

## Professional experience

**Target Technologies Pakistan**  
*Backend Engineer (Go) · July 2025 – Present*

- Develop backend services for Government of Oman projects, including live driver and cargo tracking with location updates every five seconds.
- Work across an architecture of 10+ gRPC microservices, including SSO, configuration, profiling, email, and notifications.
- Build APIs around route optimization and delivery scheduling services.
- Integrate payment gateway functionality through gRPC clients.

**ZAMH Technologies LLC**  
*Backend Developer (Go & Node.js) · September 2024 – June 2025*

- Developed backend APIs, application business logic, and database access improvements.
- Implemented Redis caching and real-time chat and notification functionality using WebSockets.
- Monitored application performance and service health using Prometheus and Grafana.
- Investigated production issues and improved reliability through testing, refactoring, and code reviews.

**Earlier experience:** Backend Developer at CapregSoft Ltd. (2023–2024) and Freelance Backend Engineer (2021–2023), working with Go, Node.js, event-driven architectures, Kafka, RabbitMQ, and gRPC.

## Engineering toolkit

**Languages**

Go · TypeScript · JavaScript · SQL

**Backend & distributed systems**

gRPC · REST APIs · Microservices · WebSockets · Socket.IO · Event-driven architecture

**Databases & messaging**

PostgreSQL · pgvector · Redis · MySQL · MongoDB · Kafka · RabbitMQ

**AI / LLM application engineering**

RAG · Embeddings · Hybrid retrieval · Reciprocal Rank Fusion · Grounded generation · Citation resolution · SSE streaming · Tool calling · Retrieval evaluation

**Security & reliability**

ECDSA P-256 request signing · Replay protection · JWT and opaque-token authentication · Permission-based access control · Prometheus · Grafana · OpenTelemetry · Sentry

**Infrastructure**

Docker · Docker Compose · CI/CD · Linux · Git · Temporal

---

## Education

**International Islamic University Islamabad**  
Bachelor of Science in Software Engineering

## Contact

Interested in backend engineering, distributed systems, and practical AI applications.

<div align="center">

  <a href="mailto:tariqwc99@gmail.com">Email</a>
  &nbsp; · &nbsp;
  <a href="https://www.linkedin.com/in/mtariq99/">LinkedIn</a>
  &nbsp; · &nbsp;
  <a href="https://github.com/MTariq99">GitHub</a>
  &nbsp; · &nbsp;
  <a href="https://muhammad-tariq.vercel.app/">Portfolio</a>

  <br /><br />

  <sub>Reliable systems. Grounded AI. Thoughtful engineering.</sub>

</div>
