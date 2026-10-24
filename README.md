# Hi, I'm @Clar17y

I am a technology and engineering leader in electronic trading, working with teams building high-throughput trading systems. My interests span distributed systems, developer productivity and the role of AI agents in software engineering.

Outside work, I build products and the tools used to deliver them. My current focus is AI engineering leadership in practice: combining architectural judgement, clear ownership, independent review and automated validation with increasingly capable coding agents.

## [Parallel Forge](https://github.com/Clar17y/parallel-forge)

**A local-first control plane for durable, reviewable agent-assisted software delivery.**

Forge began as the engineering system for Parallel and is designed to work independently with other repositories. Its implemented capabilities include:

- Durable PostgreSQL workflow state, audit events and stored evidence, surfaced through a Next.js operator dashboard.
- Managed Git worktrees, isolated database resources and subscription-backed CLI orchestration across Codex, Claude Code, Antigravity and Muse Code.
- v0.3 epic delivery: saved brainstorming, versioned requirements and dependency-aware work items, with verified prerequisite integration and explicitly enabled sequential delivery through human approval gates.
- Task usage monitoring with configurable warnings, checkpoints, optional hard limits and historical reports.

The newer [direct autonomous runs](https://github.com/Clar17y/parallel-forge/pull/142) use provider CLIs' native tools inside managed worktrees. Forge supervises sessions, runs project checks, coordinates cross-provider review and bounded repairs, then opens pull requests and handles review feedback. Merging remains an explicit owner action.

**Status:** Active development. [v0.3 functionality is merged into `main`](https://github.com/Clar17y/parallel-forge/blob/main/docs/v0.3-release.md), but v0.3 has not been tagged or published. Direct autonomous runs were merged subsequently.

## [codex-agent-framework](https://github.com/Clar17y/codex-agent-framework)

**Activity-based routing for bounded coding work across multiple providers.**

The framework routes planning, implementation, testing, verification and review across OpenAI Codex CLI, Claude Code, Google Antigravity and Muse Code. It supports Codex and Claude Code as the primary host, preserving the user's selected primary model.

Editable routing profiles, shared provider quota state and controlled fallback coordinate work on one machine. Task contracts define file ownership, acceptance criteria and checks; restricted read/search roles support analysis, while independent review uses a saved candidate and Jev evidence. Writer claims prevent overlapping assignments while a previous run's completion remains uncertain.

## Parallel

**Community-driven commuter intelligence. Private and prelaunch.**

Parallel combines live transport data with insights from people travelling. It is designed to help commuters understand disruption, compare journey options and coordinate with friends.

The architecture connects National Rail Darwin ingestion over Kafka to PostgreSQL/PostGIS and Redis, an Express API with Server-Sent Events, and a Next.js PWA. A separate scheduler handles historical performance synchronisation, disruption polling and lifecycle cleanup.

## [Savvy Hampers Inventory Manager](https://github.com/Clar17y/InventoryManagement)

**Production inventory and profitability software for an Etsy business.**

Used day to day, the application replaces spreadsheet-based stock and sales management. It supports lot and expiry tracking, barcode scanning, hamper availability calculations, automatic stock consumption, Etsy integration, and margin and expense reporting.

Built with React, TypeScript, Express and PostgreSQL, using Prisma for data access.

## Football projects

**[Grassroots football analytics](https://github.com/Clar17y/Football-Events)** grew from spreadsheets used to understand my son's team into tooling for match recording and analysis, including an offline-capable React/TypeScript PWA. The project is largely parked while I focus on Parallel and AI engineering tools.

**[Experimental football video analysis](https://github.com/Clar17y/Football-Video-Analyser)** explored extracting match data from footage using Python, YOLOv8 and ByteTrack. Detection and tracking were implemented; reliable player identity through camera movement, occlusion and re-entry remained the harder problem. Further development is parked.

## Technologies

| Area | Core technologies |
| --- | --- |
| Languages | Java, TypeScript, Python, SQL |
| Applications | React, Next.js, Express, FastAPI, Spring Boot |
| Data and messaging | PostgreSQL, Redis, Kafka |
| Delivery and operations | Docker, GitHub Actions, Prometheus, Grafana |

