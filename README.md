<p align="center">
  <img src="battlers-conclution.jpg" alt="profile art" width="100%" />
</p>

### about

16 year old software engineer focused on backend systems, service boundaries, concurrency, and load-oriented architecture. I build reliable apis, workers, and data flows, with frontend work where the product requires it.

**Languages:** English (B1/B2) • Russian (Native) • Ukrainian (Native)

**Bio:** [mailorq.com](https://mailorq.com)

---

### skills

<p align="left">
  <img src="https://skillicons.dev/icons?i=py,rust,ts,js,django,fastapi,git,docker,nginx,postgres,redis,kafka,rabbitmq,linux&theme=dark" alt="skills" />
</p>

- **languages**: Python • Rust • TypeScript • JavaScript • Lua • POSIX shell
- **backend frameworks & runtimes**: Django • Django Ninja • DRF • FastAPI • Tokio/Axum
- **api & networking**: REST/OpenAPI • WebSockets • gRPC • HTTPX
- **asynchronous & messaging**: Celery • RabbitMQ • Apache Kafka • Redis Pub/Sub
- **databases & storage & orm**: SQL • PostgreSQL • Redis • SQLite/SQLCipher • SQLAlchemy • Alembic • MinIO • S3
- **architecture & patterns**: Service Layer • CQRS • Transactional Outbox • Idempotency • Optimistic Concurrency • State Machines
- **security & authentication**: Zero-Trust • Fail-Closed Checks • Session/CSRF Authentication • JWT/RS256 • Rate Limiting
- **frontend & clients**: React • Vite • Tailwind CSS • Tauri
- **devops & systems**: Docker • Docker Compose • Kubernetes (basic) • Nginx • Prometheus • GitHub Actions • GitLab CI/CD • Linux
- **testing & tooling**: Pytest • Locust • Vitest • Playwright • Ruff • MyPy • ESLint • Gitleaks

---

### projects

#### [Asian Restaurant](https://github.com/mailorq/asian_restaurant)

**Event-Driven Ordering Platform** - *Personal project*

A Django/Django Ninja ordering system split between ordering and operations services, backed by PostgreSQL, Redis, and RabbitMQ. Its backend centers on concurrent cart updates, safe checkout, and event-driven operations read models.

- Redis Lua scripts implement versioned cart updates, guest-cart merging, and stock reconciliation.
- Checkout combines database row locks with idempotency checks to prevent overselling and duplicate order creation.
- A transactional outbox publishes to RabbitMQ; lease-based retry workers feed idempotent, version-fenced operations projections.

#### [Steins;Gate Platform](https://github.com/mailorq/SteinsGate_project)

**Anime Content Web Platform** - *Personal project*

A *Steins;Gate* fan platform, built with Django Ninja, PostgreSQL, and Redis; implementation focuses on shared abuse controls, secure session flows, and consistency-aware caching.

- Redis fixed-window rate limits and escalating IP lockouts are shared across workers; authentication checks fail closed when Redis is unavailable.
- Email verification pairs HMAC-hashed codes and nonces with an on-commit Celery outbox, Beat reconciliation, and quota-enforced resend controls.
- Cache-aside aggregate reads pair with database deduplication and PostgreSQL advisory locks for 24-hour view counting.

#### [Hyprland Dots](https://github.com/mailorq/hyprland-dots)

**Linux Desktop Configuration** - *Additional project*

A modular Hyprland configuration distributed through a checksum-verified POSIX installer, with Lua configuration and Python release tooling.

- The installer defaults to dry-run, validates conflicts, supports backups and restore, and publishes files via atomic per-file rename.
- Python generators and validators produce component configs and SHA-256 manifests used by release gates.

---

### activity

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com?user=mailorq&theme=dark&hide_border=true" alt="GitHub streak" width="65%" />
</p>
