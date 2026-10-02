### Hi, I'm Alvin Ferdinand 👋

Python & Web Developer — I build backend systems, data pipelines, and applied-AI tools that run real business operations, not demo projects.

- 🎓 Computer Science, Soegijapranata Catholic University (GPA 3.70)
- 💼 IT Intern @ GSI — ERP modules, API integrations, internal tooling
- 🧠 Bangkit Academy — Machine Learning path (TensorFlow, GCP)
- 🌐 [kotaatlas.netlify.app](https://kotaatlas.netlify.app) · [LinkedIn](https://linkedin.com/in/alvin-ferdinand-647102335)

---

#### What I've built (production systems — code is company-owned, so described here rather than shown)

**API Integrations & Data Pipelines**
- Two-way integration: Accurate Online (accounting ERP) ↔ Google BigQuery — token+signature auth, pagination swept by document ID (not date, which silently skips back-dated records), idempotent loads verified against the source API's own row count.
- Read-only XML-RPC bridge into Odoo for downstream reconciliation.
- FIFO cost-of-goods engine reconstructing per-item COGS from inventory layers, validated against the company's accounting journal as referee — **963 of 963 documents matched**.

**Backend Systems**
- Multi-module ERP (Laravel/MySQL) in daily production use across several business lines — approval workflows, attendance with photo/GPS capture, asset register, executive dashboards.
- Scoped permission architecture: access granted per module *and* per region, not globally — one workflow definition serves branches with different rules instead of forking the codebase.
- Rewrote an executive dashboard's SQL aggregation after it was timing out at 86.5s (killed by the gateway) — runs in 6.0s now.
- Two Go backends in production: an internal HR/candidate-assessment platform (React + TypeScript + Vite frontend, PostgreSQL) and a mobile inventory system (Supabase/PostgreSQL with enforced RLS, deployed behind nginx + systemd).

**Computer Vision & AI**
- Photo-to-data pipeline reading handwritten field forms from phone photos: perspective correction → grid segmentation → per-cell recognition with an 8-way voting ensemble. Tuned deliberately for **zero wrong readings** over maximum coverage — a silent wrong number costs more than an empty one.
- Natural-language query tool over BigQuery — a deterministic engine answers known question shapes first, a tiered set of LLMs handles the rest, with causal/hypothetical questions explicitly flagged so a model's reasoning is never presented as measured fact.

**Mobile**
- React Native inventory app with device-camera capture, sharing one backend with its web counterpart through database views instead of duplicated logic.

---

#### Currently learning
Angular 19 + Ionic + Spring Boot 3 (Java 21) — deliberately filling the gap on the Java/Angular side of the stack.

#### Reach me
📧 alvinferdinand2004@gmail.com · 📱 +62 857-0254-2793
