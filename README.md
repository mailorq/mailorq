<p align="center">
  <img src="sayo-yasuda.jpg" alt="sayo-yasuda" width="97%" />
</p>

### about

16 year old software engineer focused on backend systems, service boundaries, concurrency, and load-oriented architecture. I build reliable apis, workers, and data flows, with frontend work where the product requires it.

[mailorq.com](https://mailorq.com)

---

### skills

<p align="left">
  <img src="https://skillicons.dev/icons?i=py,rust,ts,js,django,fastapi,tauri,react,docker,postgres,redis,kafka,rabbitmq,linux&theme=dark" alt="skills" />
</p>

- **languages**: Python • Rust • TypeScript • JavaScript • SQL • Lua • POSIX shell
- **backend & architecture**: Django • Django Ninja • DRF • FastAPI • REST/OpenAPI • WebSockets • Celery • RabbitMQ • Kafka • Redis • transactional outbox • idempotency • optimistic concurrency • microservices • monoliths
- **data & storage**: PostgreSQL • Redis • SQLite/SQLCipher • SQLAlchemy • Alembic • S3 compatible storage
- **devops & systems**: Docker • Docker Compose • Kubernetes (basic) • Nginx • Prometheus • GitHub Actions • Linux
- **frontend & clients**: React • Vite • Tailwind CSS • React Router • Tauri 
- **testing & reliability**: Pytest • Locust • Vitest • Playwright • Ruff • MyPy • Rate Limiting • CSRF/Session Auth • JWT/RS256

---

### projects

#### [Asian Restaurant](https://github.com/mailorq/asian_restaurant)

**Event-Driven Ordering Platform** - *Personal project · backend & architecture*

A web app for ordering pan-asian food: users browse the menu, manage a cart, place orders, and view their order history; staff can manage orders, inventory, and customer data. The system combines a Django backend, React frontend, separate operations service, PostgreSQL, Redis, and RabbitMQ.

- Lua-backed Redis cart operations handle concurrent updates, guest-to-user merging, and stock reconciliation.
- Checkout protects inventory with row locks and idempotency checks.
- Order events use a transactional outbox before publishing to RabbitMQ.

#### [Steins;Gate Fan Platform](https://github.com/mailorq/SteinsGate_project)

**Full-Stack Web Application** - *Personal project · complete*

A fan website for watching the full *Steins;Gate* anime series and movie, tracking viewing progress, rating titles, and discussing episodes through comments. It combines a typed React frontend with a Django backend and a production-shaped Docker deployment.

- The OpenAPI schema generates the typed frontend API client.
- Redis provides shared rate limits, lockout controls, and aggregate caching.
- The repository includes CSRF-protected session flows, email verification, CI checks, and a Locust load-test scenario.

#### [Hyprland Dots](https://github.com/mailorq/hyprland-dots)

**Linux Desktop Configuration & Release Tooling** - *Additional project*

A ready-to-deploy Hyprland and Wayland desktop setup with a visual theme, status bar profiles, launcher, terminal, notifications, and wallpaper management. It also provides a controlled installer for applying the configuration without touching unrelated system files.

- The POSIX installer supports dry runs, preflight checks, backups, atomic publication, and restore.
- Python generators and validators produce component configs, SHA-256 deployment manifests, and release gates.

---

### activity

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=mailorq&theme=dark&hide_border=true" alt="GitHub streak" width="65%" />
</p>
