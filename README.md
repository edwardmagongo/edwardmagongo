# Edward Magongo

Software Engineer — backend systems and applied ML research. Second-year Computer Science
at the University of York.

[edwardmagongo.com](https://edwardmagongo.com) · [LinkedIn](https://www.linkedin.com/in/edward-magongo) · [Email](mailto:edwardmagongo123@gmail.com)

Open to Software Engineering and Machine Learning Engineering internships, 2026 — UK-based,
open to remote and relocation.

---

## What I've built

**[LedgerAPI](https://github.com/edwardmagongo/LedgerAPI)** — a banking ledger REST API where
concurrent transfers against the same account provably cannot corrupt a balance. Optimistic
locking with a bounded, jittered retry loop; 145 tests including a concurrency suite that was
verified to *fail* when the fix is removed; deployed to AWS ECS Fargate via Terraform with
GitHub Actions CI/CD authenticating through OIDC (no stored AWS keys). Measured — not
estimated — 400+ req/s at 99%+ success under 20-way concurrent contention on a single account,
zero balance discrepancy across 1,000+ reconciled transactions.

`Java 21` `Spring Boot` `PostgreSQL` `Testcontainers` `Terraform` `AWS ECS Fargate` `GitHub Actions`

→ [Live demo](http://ledger-api-alb-1715046521.eu-west-2.elb.amazonaws.com/swagger-ui.html) · [Full README](https://github.com/edwardmagongo/LedgerAPI#readme)

**[QIANets](https://github.com/edwardmagongo/QIANets-Website)** — quantum-inspired model
compression for CNNs (GoogLeNet, DenseNet, ResNet-18), co-authored with five other researchers
and accepted to a NeurIPS 2024 workshop on neural compression.

`Python` `PyTorch`

→ [Paper (arXiv)](https://arxiv.org/abs/2410.10318) · [NeurIPS Poster](https://neurips.cc/virtual/2024/poster/98205)

**[Personal-Portfolio](https://github.com/edwardmagongo/Personal-Portfolio)** — this site.
React, TypeScript, and Vite, with a hand-built scroll/animation stack and a serverless contact
form.

`React` `TypeScript` `Vite` `Vercel`

---

## Experience

**Software Developer · Discern Match** — *May 2026 – Present, Remote*
Shipping LLM-powered features (resonance generation, moderation, onboarding analysis) for a
matchmaking platform: prompt design and structured-output pipelines against the Anthropic API,
evaluated against real user data, plus realtime backend infrastructure (Socket.io, Redis,
PostgreSQL/Prisma, Docker). → [auth-hardening](https://github.com/edwardmagongo/auth-hardening):
a standalone extract of the session-security layer (JWT revocation, login throttling).

**Software Development Intern · Medvice** — *Jul 2024 – Dec 2024, Netherlands (Remote)*
Backend contributor on a 4-person cross-border team: a Flask/SQLAlchemy JSON parser and REST
API producing structured, validated medical data, plus technical documentation of the API,
database, and deployment architecture.

---

## Stack

Languages: TypeScript · Python · Java
Backend: NestJS · Spring Boot · Flask · PostgreSQL · Prisma · Redis
Frontend: React · Next.js · React Native (Expo)
Infra: Docker · Terraform · AWS · GitHub Actions · Vercel

---

## Elsewhere

[github.com/edwardmagongo](https://github.com/edwardmagongo) for everything above, in full.
