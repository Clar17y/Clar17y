# 👋 Hi, I'm @Clar17y

Technology and engineering leader working in electronic trading, with a particular interest in **AI-assisted software engineering, distributed systems, developer productivity, and building useful products from scratch**.

Professionally, I lead engineering teams working across high-throughput trading systems and have increasingly focused on how **agentic AI changes the software development lifecycle**.

Outside work, I build products to explore that in practice. I use tools including **OpenAI Codex, Claude Code, GitHub Copilot and Devin**, often combining multiple agents for implementation, review, testing and architectural challenge.

My projects have evolved from small Python experiments into full-stack applications, distributed services and production systems.

---

# 🚆 Parallel

**Community-driven commuter intelligence. Think Waze for commuting.**

Parallel is a pre-launch platform designed to help commuters make better decisions using a combination of real-time transport data and insight from people currently travelling.

Users will be able to:

* Connect with friends and coordinate journeys
* See disruption information as it develops
* Share live observations from trains and stations
* Compare journey options using real-world network conditions
* Combine community reports with official transport data

### Architecture

```text
National Rail Darwin Kafka
        ↓
Ingestion Worker
        ↓
PostgreSQL + Redis
        ↓
Express REST API / SSE
        ↓
Next.js PWA
```

A separately deployed scheduler manages historical performance synchronisation, disruption polling and lifecycle cleanup using PostgreSQL/Redis leases for single-instance job execution.

### Technology

| Layer                | Technology                                                     |
| -------------------- | -------------------------------------------------------------- |
| Runtime              | Node.js 24, TypeScript, npm workspaces                         |
| Frontend             | Next.js, React, Tailwind CSS                                   |
| Client Data          | TanStack React Query                                           |
| PWA                  | Serwist service worker                                         |
| Maps                 | MapLibre GL, PMTiles                                           |
| API                  | Express REST services                                          |
| Realtime             | Server-Sent Events, Redis Pub/Sub                              |
| Data Ingestion       | KafkaJS, National Rail Darwin                                  |
| Database             | PostgreSQL / PostGIS on Neon                                   |
| Data Access          | Drizzle ORM                                                    |
| Cache & Coordination | Redis on Upstash                                               |
| Authentication       | Better Auth                                                    |
| Validation           | Zod                                                            |
| Monitoring           | Prometheus, Grafana                                            |
| Hosting              | Vercel, Render                                                 |
| Testing              | Vitest, React Testing Library, Supertest, Playwright, axe-core |
| CI / Quality         | GitHub Actions, Oxlint, dependency auditing                    |

The system is tested beyond normal functional coverage, including **load, soak, reconnect-storm, resilience, recovery and database migration drills**.

External integrations include National Rail Rail Data Marketplace, Darwin live data, HSP historical performance, Transport for London and Resend.

Source is currently private while the product remains pre-launch.

---

# 🟣 Savvy Hampers Inventory & Profitability Platform

A production inventory and profitability application built for a real Etsy-based business and used day-to-day.

It replaced a substantial amount of spreadsheet-based stock and sales management.

### Features

* Lot-based stock management and expiry tracking
* Barcode scanning
* Product and hamper composition
* Real-time "can make" calculations
* Automatic inventory consumption
* Etsy order integration
* Margin and profitability calculations
* Etsy fee and offsite-ad reconciliation
* Monthly invoice ingestion
* Business expense tracking
* Low-stock and expiry monitoring
* Sales and profitability analytics
* Historical spreadsheet imports

### Architecture & Technology

Built as a Spring Boot application backed by PostgreSQL and hosted on Render, with Neon used for database infrastructure and GitHub Actions handling automated database backup workflows.

This project is actively used by the business rather than being a demonstration application.

---

# ⚽ Grassroots Football Analytics

This started as a way to better understand my son's grassroots football team.

The original data lived in spreadsheets and was manually structured to make statistical analysis possible. That evolved into PostgreSQL-backed tooling and eventually a React/TypeScript application for recording and analysing matches.

The project explored:

* Match event modelling
* Player and team analytics
* Goalkeeper statistics
* Live event capture
* Offline-first PWA architecture
* Data import and reporting
* Automated testing
* AI-assisted development workflows

Development accelerated significantly as coding agents improved, eventually moving from individual AI-generated changes to **multi-agent workflows with independent implementation and adversarial code review**.

The project is now largely parked while I focus on Parallel and other systems.

---

# 🎥 Experimental Football Video Analysis

I also explored whether grassroots match footage could automatically produce the event data used by the football analytics application.

I built an initial computer-vision pipeline and proved parts of the concept, but ultimately parked the project.

The interesting engineering conclusion was that detection was not the hardest problem. **Persistent player identity across a moving camera, occlusion and players repeatedly entering and leaving frame** made reliable attribution substantially more difficult.

The amount of labelled training data required also made further investment difficult to justify for the use case.

Sometimes the useful outcome of an experiment is deciding not to build the product.

---

# 🤖 AI-Assisted Engineering

A major area of interest for me is how software engineering changes when AI agents become active participants in the development lifecycle.

My workflows increasingly involve:

* Breaking architecture into independently executable work
* Parallel agent implementation
* Repository-level instructions and engineering standards
* Automated test generation
* Agent-driven refactoring
* Static-analysis remediation
* Cross-model code review
* Adversarial review between agents
* Human validation and architectural decision-making
* CI/CD as the final quality gate rather than trusting generated code

I am particularly interested in the shift from using AI as **autocomplete** toward using agents as an **engineering workforce that still requires architecture, direction, constraints, review and accountability**.

---

# 🧰 Technologies I Work With

**Languages**

Java • TypeScript • Python • SQL

**Web & APIs**

Next.js • React • Spring Boot • Express • REST • SSE

**Data & Messaging**

PostgreSQL • Oracle • Redis • Kafka • Solace • TibcoRV • KDB/Q

**Infrastructure & Operations**

Vercel • Render • Neon • Upstash • Docker Compose • GitHub Actions • Prometheus • Grafana

**Testing**

JUnit • Selenium • Vitest • Playwright • React Testing Library • Supertest

**AI Engineering**

OpenAI Codex • Claude Code • GitHub Copilot • Cognition Devin

---

## Current Focus

Building **Parallel**, exploring modern distributed application architecture, and pushing further into **agentic software engineering and AI-enabled engineering leadership**.
