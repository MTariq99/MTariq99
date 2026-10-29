# Hey, I'm Tariq 👋

**Backend engineer (Go).** I build the parts of a system that have to keep working: live tracking, gRPC microservices, event pipelines, and the plumbing behind the dashboard.

I've spent 5+ years doing that in Go and Node.js, most recently on logistics platforms for the Government of Oman. Lately I've been pointing the same instincts at LLM backends: retrieval, grounded answers, evals, and keeping the model on a short leash.

I haven't shipped AI professionally yet. What I have done is build it end to end on my own, with the same care I'd give a payments service. Both projects below are public, so you can judge the code instead of taking my word for it.

---

## What I'm working on right now

**At work:** backend services for large government logistics projects. That means live driver and cargo tracking with location updates every five seconds, a system of 10+ gRPC microservices (SSO, configuration, profiling, email, notifications), APIs around route optimization and delivery scheduling, and payment gateway integration over gRPC.

**On my own time:**
- Running Retrievion's evaluation suite on a real test set and writing up what the numbers say, including where it fails.
- Adding cross-encoder reranking to Retrievion.
- Hardening DispatchAI: approval workflows, audit trail, and key rotation.

<!-- TODO: once you have Retrievion eval numbers, add them here as a one-liner, e.g. "Latest Retrievion run: Recall@5 = __, MRR = __ on __ questions." -->

---

## Projects worth two minutes

### [Retrievion](https://github.com/MTariq99/retrievion): grounded Q&A over private PDFs
A multi-tenant RAG backend in Go. You upload PDFs, ask questions, and get streamed answers with citations that resolve to the exact chunk, document, and page.

- Ingestion runs asynchronously through RabbitMQ (with a dead-letter queue), so uploads never block and failures don't vanish.
- Retrieval is hybrid: pgvector (HNSW) plus Postgres full-text search, merged with Reciprocal Rank Fusion and trimmed to a token budget.
- It ships with its own evals (Precision@K, Recall@K, MRR, and LLM-judged faithfulness) so I can tell whether a change made answers better or just different.

`Go · PostgreSQL · pgvector · Redis · RabbitMQ · Gemini · Prometheus · OpenTelemetry`
Status: working prototype, reranking is next.

<!-- TODO: if you add a screenshot or a short demo GIF of a streamed, cited answer, put it here. It will do more than any bullet. -->

### [DispatchAI](https://github.com/MTariq99/dispatchai): LLMs propose, your app decides
An orchestration engine that lets an LLM suggest tool calls while your application stays in charge of what actually runs. My rule: the model never gets to authorize itself.

- Every request is signed (ECDSA P-256) with timestamp checks, nonce-based replay protection, and the request body bound to the signature.
- Runs and tool calls are idempotent, so retries don't double-fire.
- Provider-agnostic LLM interface with a Gemini adapter (ports and adapters).

`Go · ECDSA · API security · Idempotency · LLM integration`
Status: early-stage prototype, being hardened. It does not claim exactly-once effects on external systems, and says so.

---

## What I work with

**Languages:** Go (my daily driver), Node.js, TypeScript, JavaScript

**Services & APIs:** gRPC, REST, Gin, Express, microservices, clean architecture, API and system design

**Real-time & messaging:** Kafka, RabbitMQ, WebSockets, Socket.IO, event-driven design

**Data:** PostgreSQL (including pgvector), MySQL, MongoDB, Redis, query and index tuning

**Ship & run:** Docker, Kubernetes, CI/CD, blue-green and zero-downtime releases, Linux, Prometheus, Grafana, Temporal

**Domains:** government and enterprise systems, payments, real-time tracking, SaaS

---

## Where I've worked

- **Target Energy Solutions**, Backend Engineer (Go), Jul 2025 to now: Government of Oman logistics, live tracking, gRPC microservices.
- **ZAMH Technologies**, Backend Developer (Go & Node.js), Sep 2024 to Jun 2025: Redis caching, real-time chat and notifications over WebSockets, Prometheus and Grafana monitoring.
- **CapregSoft**, Backend Developer (Go & Node.js), Jan 2023 to Aug 2024: bulk email verification platform, query and index tuning, blue-green deployments.
- **Freelance**, Backend Developer (Go), Apr 2021 to Jan 2023: event-driven microservices on Kafka and RabbitMQ, gRPC between services.

Full details are in my [résumé](https://github.com/MTariq99/MTariq99/raw/main/assets/Muhammad_Tariq_Resume_AI.pdf).

---

## What I'm looking for

Remote backend roles where I can own services end to end, ideally Go-first. I'm especially interested in teams building AI features on top of solid backends, where retrieval, evaluation, and security matter as much as the model.

---

## Say hi

I'm based in Islamabad (UTC+5), currently working on-site, and open to remote roles.

📧 [Email](mailto:tariqwc99@gmail.com)

💼 [LinkedIn](https://www.linkedin.com/in/mtariq99/)

🌐 [Portfolio](https://muhammad-tariq.vercel.app/)

📄 [Résumé](https://github.com/MTariq99/MTariq99/raw/main/assets/Muhammad_Tariq_Resume_AI.pdf)
