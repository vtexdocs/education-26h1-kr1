# education-26h1-kr1

Project for **KR1: Documentation infrastructure for content discoverability** (VTEX Education, 2026H1).

## Purpose

Build the foundational documentation infrastructure that makes VTEX content AI-ready, machine-readable, and discoverable across channels. Content should be effectively indexed, retrieved, and surfaced for relevant user intents (Google Search, portal search, proprietary search API, MCP, external LLMs).

## Phase 1 — Testing

Phase 1 establishes a **repeatable way to measure** how well users find VTEX knowledge across all discovery paths, then runs a **baseline** before improvements.

- **Duration:** 6 weeks (kick off 2026-02-03)
- **Deliverables:** Issue/query template, consolidated test suite (~20–32 issues), path runners, unified output format, baseline report

Discovery paths in scope:

| Path | Description |
|------|-------------|
| Google Search | Organic web search; users land on Help Center or Developer Portal |
| Portal search | On-site search (e.g. Algolia) on Help Center / Developer Portal |
| Proprietary search API | REST search API (keyword-style); used by MCP |
| MCP | VTEX docs MCP (Cursor and other agents) |
| External LLMs | ChatGPT, Claude, etc. using web search or browsing |

## Docs

| Document | Description |
|----------|-------------|
| [2026H1 KRs proposal](docs/planning/2026H1%20KRs%20proposal.md) | Education team 2026 KRs and KR1 context |
| [Planning phase 1 (tests)](docs/planning/Planning%20phase%201%20(tests).md) | Phase 1 scope, paths, test-suite structure, metrics |
| [Task planning KR1 Phase 1](docs/planning/Task%20planning%20KR1%20Phase%201.md) | Jira tasks, ownership, and timeline for Phase 1 |

## Team

- **Champion:** Pedro Antunes Costa  
- **Team:** Bárbara Celi, Isabella Veloso Sa, Ricardo José Correia da Silva  

**Jira epic:** [EDU-17421 — KR1 Documentation infrastructure](https://vtex-dev.atlassian.net/browse/EDU-17421)  
**Epic due date:** 2026-06-30
