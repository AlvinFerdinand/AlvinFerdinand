### Hi, I'm Alvin Ferdinand 👋

Python & Web Developer. I build backend systems, data pipelines and applied-AI
tools that real businesses run on every day — ERPs, retail point-of-sale,
accounting integrations, and computer-vision tooling in production use.

- 🎓 **Computer Science**, Soegijapranata Catholic University — GPA 3.70
- 💼 Built production systems for **GSI Group** (accounting data pipelines),
  **Zuliya Group** (multi-module ERP) and **Optik Rizki Eye Plus** (retail POS)
- 🧠 **Bangkit Academy** — Machine Learning path (TensorFlow, Google Cloud)
- 👨‍🏫 Taught Python, web, Android (Kotlin/Java) and ML for a year at **Timedoor Academy**
- 🌐 Portfolio: **[alvinferdinand.github.io](https://alvinferdinand.github.io)**
- 📍 Semarang, Indonesia · **open to work**

`Python` `PHP/Laravel` `Go` `JavaScript/TypeScript` `React & React Native`
`MySQL` `PostgreSQL` `BigQuery` `TensorFlow`

---

### 🔎 Demo repos — the code

Clean-room rebuilds of patterns from the production systems below. The real
code, data and schemas belong to those companies and are **not** published;
these are written from scratch on invented data so the engineering decisions
can be shown, run and tested in the open. Every repo states which system it
came from, and every one is CI-tested.

| Repo | What it demonstrates | Tests |
|---|---|---|
| [**branch-stock-transfer-demo**](https://github.com/AlvinFerdinand/branch-stock-transfer-demo) [![CI](https://github.com/AlvinFerdinand/branch-stock-transfer-demo/actions/workflows/ci.yml/badge.svg)](https://github.com/AlvinFerdinand/branch-stock-transfer-demo/actions) | Retail POS: inter-branch transfer handshake (stock leaves on send, arrives on receipt), append-only movement ledger, canonical item keys | 21 |
| [**scoped-permission-system-demo**](https://github.com/AlvinFerdinand/scoped-permission-system-demo) [![CI](https://github.com/AlvinFerdinand/scoped-permission-system-demo/actions/workflows/ci.yml/badge.svg)](https://github.com/AlvinFerdinand/scoped-permission-system-demo/actions) | ERP architecture: permissions scoped by module **and** region; one workflow definition serving regions with different approval stages | 18 |
| [**ocr-form-reader-demo**](https://github.com/AlvinFerdinand/ocr-form-reader-demo) [![CI](https://github.com/AlvinFerdinand/ocr-form-reader-demo/actions/workflows/ci.yml/badge.svg)](https://github.com/AlvinFerdinand/ocr-form-reader-demo/actions) | Photographed form → structured digits, tuned for **zero wrong readings**; refuses to guess rather than returning garbage. NumPy only | 14 |
| [**fifo-cogs-engine-demo**](https://github.com/AlvinFerdinand/fifo-cogs-engine-demo) [![CI](https://github.com/AlvinFerdinand/fifo-cogs-engine-demo/actions/workflows/ci.yml/badge.svg)](https://github.com/AlvinFerdinand/fifo-cogs-engine-demo/actions) | FIFO cost-of-goods engine with explicit handling for the case most implementations get wrong: a sale that outruns the stock on hand | 8 |
| [**rest-sync-pipeline-demo**](https://github.com/AlvinFerdinand/rest-sync-pipeline-demo) [![CI](https://github.com/AlvinFerdinand/rest-sync-pipeline-demo/actions/workflows/ci.yml/badge.svg)](https://github.com/AlvinFerdinand/rest-sync-pipeline-demo/actions) | Reliable incremental REST sync: paginate by id not date, idempotent upsert, completeness verified against the source's own row count | 6 |
| [**jwt-auth-filter-demo**](https://github.com/AlvinFerdinand/jwt-auth-filter-demo) [![CI](https://github.com/AlvinFerdinand/jwt-auth-filter-demo/actions/workflows/ci.yml/badge.svg)](https://github.com/AlvinFerdinand/jwt-auth-filter-demo/actions) | Spring Boot 3 / Spring Security 6 JWT auth filter from scratch — a learning build, not a rebuild of shipped work | 3 |

---

### 🏗️ Production work — the systems

Company-owned code, so described rather than shown.

**Data pipelines & integrations** · *GSI Group*
- Two-way integration between Accurate Online's accounting API and Google
  BigQuery: token + per-request signature auth, pagination swept by document
  **id** rather than date (a date filter silently skips back-dated records),
  idempotent loads verified against the source API's own row count.
- Read-only XML-RPC bridge into Odoo for downstream reconciliation.
- FIFO cost-of-goods engine reconstructing per-item COGS from inventory
  layers, validated against the accounting journal as referee —
  **963 of 963 documents matched**.

**Multi-module ERP** · *Zuliya Group*
- In daily production use across several business lines: approval workflows,
  attendance with photo/GPS capture, asset register, executive dashboards.
- Permission architecture scoped per module **and** per region, so one
  workflow definition serves branches with different rules instead of forking
  the codebase per branch.
- Rewrote an executive dashboard's aggregation after it was timing out at
  **86.5s** and being killed by the gateway — **6.0s** now.
- Photo-to-data pipeline reading handwritten field forms from phone photos:
  perspective correction → grid segmentation → per-cell recognition with a
  voting ensemble, tuned for **zero wrong readings** over maximum coverage.

**Retail point-of-sale** · *Optik Rizki Eye Plus*
- POS and stock system across dozens of branches: sales, inter-branch stock
  transfers with scan-based receipt confirmation, and a stock movement trail.
- Moved price resolution server-side after finding the server trusted a price
  posted by the browser — an invalid master price now blocks the save outright.

**Go backends & AI tooling**
- Two Go services in production: an internal HR/candidate-assessment platform
  (React + TypeScript + Vite frontend, PostgreSQL, enforced row-level
  security) and a mobile inventory system behind nginx + systemd.
- Natural-language query tool over BigQuery: a deterministic engine answers
  known question shapes first and a tiered set of LLMs handles the rest, with
  causal and hypothetical questions explicitly flagged so a model's reasoning
  is never presented as measured fact.
- React Native inventory app with device-camera capture, sharing one backend
  with its web counterpart through database views instead of duplicated logic.

---

### 📚 Currently learning
Angular 19 + Ionic and Spring Boot 3 / Java 21 — deliberately filling the gap
on the Java/Angular side rather than staying in the stacks I already know.

### 📫 Reach me
📧 alvinferdinand2004@gmail.com · 📱 +62 857-0254-2793
· 💼 [LinkedIn](https://linkedin.com/in/alvin-ferdinand-647102335)
· 🌐 [alvinferdinand.github.io](https://alvinferdinand.github.io)
