# Edward Magongo

Software Engineer — backend systems and applied ML research. Second-year Computer Science
at the University of York.

[edwardmagongo.com](https://edwardmagongo.com) · [LinkedIn](https://www.linkedin.com/in/edward-magongo) · [Email](mailto:edwardmagongo123@gmail.com)

Open to Software Engineering and Machine Learning Engineering internships, 2026 — UK-based,
open to remote and relocation.

---

## What I've built

**[CausalPulse](https://github.com/edwardmagongo/causalpulse)** — a causal inference and
experimentation platform built around the part that is actually hard: knowing when *not* to
believe an estimator. A scenario's true effect is computed from its realised potential outcomes
rather than taken from its label, and an import-linter contract forbids every estimator package
from importing the simulation code, so nothing can be tuned against the answer it is scored on.
Twelve estimators, each checked where it should fail as well as where it should succeed —
two-way fixed effects shown breaking under staggered adoption with the Goodman–Bacon
decomposition explaining why, synthetic control pushed outside its donors' convex hull,
reference parity against `statsmodels`, `pysyncon` and `econml`. A pre-registered 4,000-cell
benchmark over ten estimators and thirteen scenarios met seven of its eight expectations; the
eighth was a real bug, an outcome likelihood that was always Gaussian. Real data then found
what simulation could not: LaLonde and Proposition 99 surfaced a propensity fit that depended
on a column's units and a donor-weight solver that reported success without ever leaving its
starting point. The language-model layer cannot invent a number — every value in a narrative is
a placeholder verified against a fact table — and a 200-interpretation study with 150
hand-labelled statements reports its own judge's 5.1% sensitivity as the weakness it is rather
than quietly dropping it. 3,938 Python tests, 512 dashboard unit tests, 25 browser tests.

`Python 3.13` `statsmodels` `scikit-learn` `JAX` `NumPyro` `FastAPI` `PostgreSQL` `Redis` `Next.js` `Docker` `Terraform` `AWS`

→ [Full README](https://github.com/edwardmagongo/causalpulse#readme)

**[EdgeFlow](https://github.com/edwardmagongo/EdgeFlow)** — a concurrent C++20 telemetry
pipeline: simulated devices → TCP gateway → bounded queue → worker pool → batcher → sink. Each
backpressure policy is characterised by measurement past the throughput knee a saturating load
generator located, not by argument, and the lock-free queue is benchmarked head-to-head against
the mutex one rather than assumed to win. Latency attribution put 73.9–88.3% of the sink's round
trip in I/O wait; removing the single-in-flight limit returned a measured +29.5%. 185 tests, run
under AddressSanitizer and ThreadSanitizer as well as plain — a green suite that has never been
under TSan says little about a lock-free queue. Terraform provisions the full AWS stack, verified
end to end against the live endpoint with the gateway's counters reconciling exactly against the
backend's.

`C++20` `Boost.Asio` `CMake` `NestJS` `PostgreSQL` `Redis` `React` `Terraform` `AWS ECS Fargate`

→ [Full README](https://github.com/edwardmagongo/EdgeFlow#readme)

**[LedgerAPI](https://github.com/edwardmagongo/LedgerAPI)** — a banking ledger REST API where
concurrent transfers against the same account provably cannot corrupt a balance. Optimistic
locking with a bounded, jittered retry loop; 145 tests including a concurrency suite that was
verified to *fail* when the fix is removed; deployed to AWS ECS Fargate via Terraform with
GitHub Actions CI/CD authenticating through OIDC (no stored AWS keys). Measured — not
estimated — 400+ req/s at 99%+ success under 20-way concurrent contention on a single account,
zero balance discrepancy across 1,000+ reconciled transactions.

`Java 21` `Spring Boot` `PostgreSQL` `Testcontainers` `Terraform` `AWS ECS Fargate` `GitHub Actions`

→ [Live demo](http://ledger-api-alb-1715046521.eu-west-2.elb.amazonaws.com/swagger-ui.html) · [Full README](https://github.com/edwardmagongo/LedgerAPI#readme)

**[TfL-Pulse](https://github.com/edwardmagongo/TfL-Pulse)** — a scheduled ingestion pipeline over
TfL's live Arrivals API, turning a noisy stream of repeated, expiring predictions into clean,
deduplicated lifecycle records in Postgres. 36 tests (unit + Testcontainers integration against
real captured API responses, no live network calls in the suite); runs on a GitHub Actions cron
every ~5 minutes.

`TypeScript` `PostgreSQL` `Testcontainers` `Jest` `GitHub Actions`

→ [Full README](https://github.com/edwardmagongo/TfL-Pulse#readme)

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
Sole engineer on a three-client platform: a 60-screen React Native (Expo) app, a Next.js marketing
site, and an admin console over a NestJS/PostgreSQL backend of 131 endpoints and 30 data models,
guarded by 1,150+ tests and blocking security checks in CI. Realtime Socket.io chat, load-tested at
1,000 concurrent connections (100% connection success, 99.3% delivery at 85 msgs/sec); 1:1 WebRTC
calling on LiveKit with end-to-end-encrypted media behind native CallKit/ConnectionService ring UI;
a session-security layer with Argon2, refresh-token rotation with reuse detection, Redis-backed
revocation, TOTP and OAuth; and LLM features (match resonance, moderation) on the Anthropic API,
with an automated evaluation harness reaching 0.989 F1 over 152 labeled cases.

**Software Development Intern · Medvice** — *Jun 2024 – Aug 2024, Netherlands (Remote)*
Backend contributor on a 4-person cross-border team: a Flask/SQLAlchemy JSON parser and REST
API producing structured, validated medical data, plus technical documentation of the API,
database, and deployment architecture.

---

## Stack

Languages: TypeScript · Python · Java
Backend: NestJS · Spring Boot · Flask · PostgreSQL · Prisma · Redis
Frontend: React · Next.js · React Native (Expo) · TanStack Query · WebRTC (LiveKit)
Infra: Docker · Terraform · AWS · GitHub Actions · Vercel

---

## Elsewhere

[github.com/edwardmagongo](https://github.com/edwardmagongo) for everything above, in full.
