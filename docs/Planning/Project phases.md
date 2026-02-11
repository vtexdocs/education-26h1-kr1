# KR1 — Project phases

| Field | Value |
| :---- | :---- |
| Created | Feb 11, 2026 |
| Champion | [Pedro Antunes Costa](mailto:pedro.costa@vtex.com) |
| Epic | [EDU-17421 — KR1 Documentation infrastructure](https://vtex-dev.atlassian.net/browse/EDU-17421) |
| Epic due date | 2026-06-30 |

This document outlines the project phases for **KR1: Documentation infrastructure for content discoverability** beyond Phase 1 (testing phase). Phase 1 establishes baseline measurements; subsequent phases implement improvements based on those findings.

---

## Context

**KR1 Objective:** Build the foundational documentation infrastructure that makes VTEX content AI-ready, machine-readable, and discoverable across channels. This ensures content can be effectively indexed, retrieved, and surfaced for relevant user intents, regardless of the entry point (Google Search, portal search, AI agents, MCP servers).

**Strategic alignment:**
- **Objective 1 (A):** Documentation is "AI-ready" and serves as the primary context for any agent building on VTEX
- **Objective 4 (A):** Users find answers through AI-assisted search without navigating multiple sources

**Current status:** Phase 1 (testing phase) is in progress (6 weeks, Feb 3–Mar 18, 2026). This outline will be refined based on Phase 1 baseline findings.

---

## Timeline

| Phase | Duration | Start date | Status | Purpose |
|-------|----------|------------|--------|---------|
| **1: Testing** | 6 weeks | Feb 3, 2026 | In progress | Establish baseline measurement across all discovery paths |
| **2: Implementation** | 8 weeks | Mar 18, 2026 | Planned | Implement improvements based on baseline findings |
| **3: Validation** | 4 weeks | May 13, 2026 | Planned | Validate improvements with follow-up test runs |
| **4: Reporting & handoff** | 4 weeks | Jun 10, 2026 | Planned | Interpret results, create reports, present findings, and define next steps and guidelines |

---

## Phase 1: Testing (current)

**Duration:** 6 weeks (Feb 3–Mar 18, 2026)  
**Status:** In progress

**Purpose:** Establish a repeatable way to measure search/knowledge-finding effectiveness across every path users use to find VTEX docs. Run a baseline so we can prioritise improvements and compare before/after.

**Detailed plan:** See [Phase 1 - Testing](Phase%201%20-%20Testing.md) for the complete testing phase plan.

**Key deliverables:**
- Test suite artifact (~20–32 issues with queries)
- Path runners (4 paths: Google Search, Portal search, MCP, External LLMs)
- Baseline report (pass rates per path, per persona, overall)
- Prioritised recommendations for improvements

**Discovery paths tested:**
1. Google Search (organic web search)
2. Portal search (Algolia on Help Center / Developer Portal / Proprietary search API)
4. MCP (VTEX docs MCP for Cursor/agents)
5. External LLMs (ChatGPT, Claude, etc.)

**Outcome:** Baseline metrics and prioritised list of gaps to address.

---

## Phase 2: Implementation (planned)

**Duration:** 8 weeks  
**Start:** After Phase 1 completion (Mar 18, 2026)  
**Status:** Planned (scope will be refined based on Phase 1 findings)

### Purpose

Implement improvements to address gaps identified in Phase 1 baseline. Focus on highest-impact areas that improve discoverability across discovery paths.

### Scope (to be refined based on Phase 1 findings)

Improvements will likely fall into these categories:

#### 2.1 Content structure and metadata
- **Potential work:** Enhance content structure, metadata, semantic markup (e.g. schema.org), and tagging to improve indexing and retrieval
- **Impact:** Improves all discovery paths (especially Google Search, portal search, MCP)
- **Dependencies:** Content standards, tooling for metadata management

#### 2.2 Search infrastructure
- **Potential work:** Optimise search algorithms, indexing, ranking, query understanding for portal search and proprietary API
- **Impact:** Improves Portal search, Proprietary search API, MCP
- **Dependencies:** Access to search infrastructure, Algolia configuration, proprietary API capabilities

#### 2.3 Content discoverability
- **Potential work:** Improve content organisation, cross-linking, navigation, and surface content in relevant contexts
- **Impact:** Improves all paths, especially Google Search and portal search
- **Dependencies:** Content architecture decisions, CMS capabilities

#### 2.4 MCP and AI agent optimization
- **Potential work:** Enhance MCP search capabilities, content format for AI consumption, semantic search improvements
- **Impact:** Improves MCP path, External LLMs (indirectly)
- **Dependencies:** MCP infrastructure, content format standards

#### 2.5 External search optimization
- **Potential work:** SEO improvements, structured data, content syndication, sitemap optimization
- **Impact:** Improves Google Search, External LLMs
- **Dependencies:** SEO tools, content publishing workflows

### Prioritization approach

1. **High-impact, low-effort:** Quick wins that improve multiple paths
2. **High-impact, high-effort:** Strategic improvements requiring more investment
3. **Path-specific:** Focus on paths with lowest baseline pass rates
4. **Persona-specific:** Address gaps for underserved personas (if identified in Phase 1)

### Key deliverables (estimated)

- Improvement implementation plan (prioritised based on Phase 1 findings)
- Implemented improvements (code, configuration, content changes)
- Updated test suite (if new issues/queries are added)
- Progress tracking against baseline metrics

### Success criteria

- Improvements implemented for top-priority gaps
- Test suite can be re-run to measure progress
- Clear documentation of changes made

---

## Phase 3: Validation (planned)

**Duration:** 4 weeks  
**Start:** After Phase 2 completion  
**Status:** Planned

### Purpose

Validate that Phase 2 improvements have increased discoverability by re-running the test suite and comparing results to Phase 1 baseline.

### Scope

1. **Re-run test suite:** Execute all path runners with the same test suite from Phase 1
2. **Compare metrics:** Calculate pass rates per path, per persona, overall; compare to baseline
3. **Identify remaining gaps:** Document any issues that still fail after improvements
4. **Analyze patterns:** Understand which improvements were most effective

### Key deliverables

- Post-improvement test results (same format as baseline)
- Comparison report (before/after metrics)
- Analysis of improvement effectiveness
- Updated prioritization for remaining gaps

### Success criteria

- Measurable improvement in pass rates (target: +X% per path, to be set based on baseline)
- Clear understanding of what worked and what didn't
- Prioritized list of remaining gaps (if any)

---

## Phase 4: Reporting & handoff (planned)

**Duration:** 4 weeks  
**Start:** After Phase 3 completion  
**Status:** Planned

### Purpose

Interpret Phase 3 validation results, create comprehensive reports, present findings to stakeholders, and define next steps and guidelines for the team to continue improving content discoverability.

### Scope

1. **Interpret results:** Analyze Phase 3 validation data, compare to baseline and Phase 2 improvements, identify patterns and insights
2. **Create reports:** Produce comprehensive reports documenting:
   - Overall project outcomes and metrics
   - Comparison of baseline vs. post-improvement results
   - Analysis of what worked and what didn't
   - Remaining gaps and opportunities
3. **Present to team:** Share findings with Education team and relevant stakeholders:
   - Project summary and key achievements
   - Metrics and improvements achieved
   - Lessons learned
   - Recommendations for ongoing work
4. **Define next steps and guidelines:** Establish:
   - Guidelines for maintaining and improving content discoverability
   - Process for ongoing test suite maintenance and expansion
   - Recommendations for future improvements
   - Handoff documentation for continuous improvement

### Key deliverables

- Comprehensive project report (baseline → Phase 2 → Phase 3 comparison)
- Presentation materials for team/stakeholder review
- Guidelines document for content discoverability best practices
- Next steps and recommendations document
- Handoff documentation (test suite maintenance, measurement process)

### Success criteria

- Clear understanding of project outcomes and impact
- Team alignment on findings and recommendations
- Actionable guidelines established for ongoing work
- Smooth handoff for continuous improvement

---
