<p align="center">
  <img src="battlers-conclution.jpg" alt="profile art" width="100%" />
</p>

### about

Software engineer specializing in backend systems, service boundaries, and concurrency-heavy workloads. I build reliable apis, event-driven worker pipelines, and resilient data flows, supporting full-stack delivery when needed.

**Languages:** English (B1/B2) • Russian (Native) • Ukrainian (Native)

**Bio:** [mailorq.com](https://mailorq.com)

---

### skills

<p align="left">
  <img src="https://skillicons.dev/icons?i=py,rust,ts,js,django,fastapi,git,docker,nginx,postgres,redis,kafka,rabbitmq,linux&theme=dark" alt="skills" />
</p>

- **languages:** Python • Rust • TypeScript • JavaScript • Lua • POSIX shell
- **frameworks & runtimes:** Django • Django Ninja • DRF • FastAPI • Tokio/Axum
- **api & networking:** REST/OpenAPI • WebSockets • gRPC
- **asynchronous & messaging:** Celery • RabbitMQ • Apache Kafka • Redis Pub/Sub
- **databases & storage & orm:** PostgreSQL • Redis • SQLite/SQLCipher • SQLAlchemy • Alembic • MinIO/S3
- **architecture & patterns:** Transactional Outbox • Idempotency • Optimistic Concurrency • Event-Driven Models
- **security & auth:** Zero-Trust • Fail-Closed Checks • Session/CSRF Auth • JWT (Ed25519/JWKS) • OIDC PKCE • Rate Limiting
- **frontend & clients:** React • Vite • Tailwind CSS • Tauri
- **devops & systems:** Docker • Kubernetes (basic) • Nginx • Prometheus • CI/CD (GitHub Actions, GitLab)
- **testing & tooling:** Pytest • Locust • Vitest • Playwright • Ruff • MyPy • ESLint • Gitleaks

---

### projects

### [Asian Restaurant](https://github.com/mailorq/asian-restaurant)

**Event-Driven Ordering Platform** · *Open source*

A food ordering platform and management system designed around clear service boundaries.

- Redis Lua scripts handle versioned cart updates, guest-cart merging, and concurrent stock reconciliation.
- Checkout pairs PostgreSQL row-level locks with idempotency keys to prevent overselling and duplicate orders.
- A transactional outbox publishes events to RabbitMQ via lease-based retry workers, feeding idempotent operations projections.

### [Steins;Gate Platform](https://github.com/mailorq/steinsgate-project)

**Anime Content Web Platform** · *Open source*

A web app for browsing anime, watching episodes, tracking progress, rating titles, and discussing them in comments.

- Redis fixed-window rate limits and escalating IP lockouts operate across workers; authentication fails closed when Redis is unavailable.
- Email verification pairs HMAC-protected codes and nonces with an on-commit Celery outbox, Beat reconciliation, and quota-controlled resends.
- Cache-aside aggregate reads reduce database load, while Redis deduplication and PostgreSQL advisory locks coordinate 24-hour view counting.

### Music Bot

**Distributed Media Pipeline** · *Private repository*

A Telegram bot that searches music catalogs, accepts track links, and delivers MP3 files with available artwork and track details.

- A PostgreSQL outbox publishes download jobs to RabbitMQ through leased dispatchers; attempt fencing prevents stale workers from changing newer job state.
- Downloads and FFmpeg conversion run in child processes. A native C wrapper uses PR_SET_PDEATHSIG, while container limits and a 512 MiB tmpfs bound resource use.
- Redis Lua scripts apply rate limits atomically; provider-specific semaphores and circuit breakers isolate upstream failures.

### Blind Tier List

**Modular Backend & Event-Driven Workflows** · *Private repository*

A web platform for creating and playing blind or standard image-based tier lists.

- FastAPI modules share a PostgreSQL-backed monolith, using Kafka workers for async event delivery.
- Idempotency keys and version checks prevent lost updates and maintain consistency across retries and concurrent edits.
- EdDSA JWTs, Google OIDC, owner-scoped access checks, and server-side image validation protect accounts and uploads.

---

### activity

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com?user=mailorq&theme=dark&hide_border=true" alt="GitHub streak" width="65%" />
</p>
