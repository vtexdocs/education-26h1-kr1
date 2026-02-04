# 26H1 KR 1 — Testing phase plan

| Field    | Value |
| :------- | :---- |
| Created  | Feb 3, 2026 |
| Champion | [Pedro Antunes Costa](mailto:pedro.costa@vtex.com) |
| Duration | 6 weeks |
| Parent   | [KR 1 — First steps plan](KR%201%20-%20First%20steps%20plan.html) |

This document plans the **testing phase** of KR 1: building a test suite that measures how well users find VTEX knowledge across all discovery paths, then running a baseline before improvements.

---

## 1. Purpose and scope

**Goal:** Establish a repeatable way to measure search/knowledge-finding effectiveness across every path users use to find VTEX docs. Run a baseline so we can prioritise improvements and compare before/after.

**In scope:** Knowledge-finding paths are set (§2). We start with **issues + queries** → build a method to run tests → define and apply success metrics → produce a baseline report.

**Out of scope:** Implementing search improvements; full automation in CI (can follow later).

---

## 2. Knowledge-finding paths and query types

These are the ways users (and agents) can find VTEX knowledge. We test all of them. We use **3 query types**; each path uses one of these types.

| Query type | Paths that use it | Description |
|------------|-------------------|-------------|
| **External search (Google)** | Google Search | Organic web search; users often land on Help Center or Developer Portal via Google. No site: restriction so we see full discoverability (our docs, community, third-party). Entry: google.com |
| **Internal search (Algolia/Proprietary API)** | Portal search, Proprietary search API | On-site search (e.g. Algolia) on Help Center and/or Developer Portal; or direct calls to the simple search API (keyword-style, Algolia-like). Entry: in-portal search box or REST API. |
| **Agents (MCP/LLMs)** | MCP, External LLMs | VTEX docs MCP used inside Cursor or other agents (returns markdown from VTEX content); or ChatGPT, Claude, etc. using web search/browsing. Entry: agent calls MCP search tool, or user asks LLM. |

**Paths (surfaces we test):** Google Search | Portal search | Proprietary search API | MCP | External LLMs.

**Optional (if in scope later):** In-product search, API reference–specific search.

**Why 3 query types:** Tech writers fill one query array per type (external, internal, agents). The *wording* varies by type (e.g. natural-language for external/agents, keyword-style for internal), but we avoid duplicating query fields across five paths.

---

## 3. Issue and query collection

### 3.1 Personas

Issues should cover different user personas so the test suite reflects how real users find knowledge. Target proportion of issues per persona:

| Persona | Description | Target share |
|---------|-------------|--------------|
| **Store operator** | Admin panel tasks, catalog management, payment method setup, inventory management, etc. | 40% |
| **Developer** | Storefront customization, Backoffice integration, APIs, etc. | 40% |
| **Decision maker** | Checking platform capabilities, security, compliance, etc. | 20% |

We plan the **persona mix from the start**: when collecting issues, tech writers tag each with a persona and we aim for the suite to land in these proportions (~40 / ~40 / ~20) from the first round (see §3.3 scope).

### 3.2 Where issues come from

Tech writers propose **user issues** (problems or intents) within their product scope. Sources:

- **Documentation analytics:** Most viewed docs, search logs, high exit rates, Google search console.
- **Product knowledge:** Known pain points, stakeholder insights, complex or high-risk features.

Each issue is a concrete situation a user might face (e.g. “How do I configure X?”, “Why does Y fail when Z?”).

### 3.3 Process

1. **Scope:** Four tech writers, each specializing in 1–2 products. Each TW contributes **5–8 issues** from their product(s) (~20–32 issues total). Plan **persona mix from the start:** when collecting issues, aim for ~40% Store operator, ~40% Developer, ~20% Decision maker (e.g. each TW plans their contribution with this mix in mind, or we assign persona quotas at kickoff so the consolidated suite lands in these proportions).
2. **Template:** For each issue, tech writers fill:
   - **Issue ID** (e.g. `P1-01`)
   - **Persona** (Store operator | Developer | Decision maker)
   - **Product / vertical**
   - **User intent** (short description)
   - **Expected outcome:** Doc URL or doc ID (and optionally section) that should be found.
   - **Source** (optional): e.g. “top 5 most viewed”, “support ticket pattern”.
3. **Queries per query type:** We use **3 query types** (§2). For each issue we use the **same format**: an **array** of query objects (`query` + optional `style`). For each issue, **we need exactly one query of each style per query type**: one **naive**, one **familiar**, one **expert**. So each query type’s array has exactly 3 entries per issue. Query **styles** (same for all types):
   - **naive** — Plain-language goal or problem; no product jargon (e.g. “checkout without saving customer profile”).
   - **familiar** — Some product/domain terms; not the exact feature name (e.g. “guest checkout VTEX”, “anonymous checkout”).
   - **expert** — Official or canonical phrasing; close to doc/feature name (e.g. “how to enable guest checkout”).

   The *wording* varies by query type: natural-language for **External search** and **Agents**; keyword-style for **Internal search**. Paths then use the appropriate array (Google → external; Portal & API → internal; MCP & LLMs → agents).

Tech writers propose one query of each style (naive, familiar, expert) per query type; the team refines and verifies that each issue has exactly one of each style per query type.

### 3.3.1 Cursor command: generate-knowledge-queries

To speed up query creation, use the **generate-knowledge-queries** Cursor command (`.cursor/commands/generate-knowledge-queries.md`). It generates one naive, one familiar, and one expert query per selected query type, then optionally adds the issue as a row to the test suite spreadsheet.

**Usage:** Invoke the command and provide (or reply when prompted):

1. **User issue or target document** (required) — Short user intent (e.g. “How to enable guest checkout”) or the URL/markdown of the doc that should be found (the command infers the issue).
2. **Query type(s)** (required) — Reply with one or more letters:
   - **A** — External search (Google)
   - **B** — Internal search (Algolia/Proprietary API)
   - **C** — Agents (MCP/LLMs)

**Example:** Run the command, then when asked for query types reply e.g. `A B C`. The command produces a Markdown file with the issue and the three queries per type, then asks whether to add the issue as a new row in the [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0).

Full behaviour, inputs, and spreadsheet details are in `.cursor/commands/generate-knowledge-queries.md`.

### 3.4 Proposed structure (artifact)

A single **test suite artifact** (e.g. spreadsheet or JSON). Tech writers register issues and queries in the [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0). Each issue has one row (or one object); **query fields are arrays** of objects with `query` and optional `style`:

| Field | Type | Description |
|-------|------|-------------|
| issue_id | string | e.g. `P1-01` |
| persona | string | Store operator \| Developer \| Decision maker |
| product | string | Product / vertical |
| user_intent | string | Short description |
| expected_doc_url | string | Ground truth for success measurement (see §5) |
| query_external | array | `[{ "query": "...", "style": "naive"\|"familiar"\|"expert" }, ...]` — **one of each style** per issue; used for **External search (Google)**; wording natural-language |
| query_internal | array | `[{ "query": "...", "style": "naive"\|"familiar"\|"expert" }, ...]` — **one of each style** per issue; used for **Internal search** (Portal + Proprietary API); wording keyword-style |
| query_agents | array | `[{ "query": "...", "style": "naive"\|"familiar"\|"expert" }, ...]` — **one of each style** per issue; used for **Agents** (MCP + External LLMs); wording natural questions and intent phrases |

- **expected_doc_url** = ground truth for success measurement (see §5).
- **query_external** = used by Google Search path. **query_internal** = used by Portal search and Proprietary search API paths. **query_agents** = used by MCP and External LLMs paths.
- Each query array: **query** (string), **style** (optional: `naive` \| `familiar` \| `expert`). **Exactly one query of each style** per issue, per query type—so 3 entries per query type per issue. Runners iterate over the relevant array per path; results can be aggregated per path and per style.

---

## 4. Test execution

We run tests **in parallel by path**: each of the four team members owns 1–2 knowledge-finding paths (build runner, run suite, capture results). Shared test suite artifact and unified output format (§4.6) so we can aggregate and compute metrics.

**Path ownership (to be assigned):**

| Path | Owner |
|------|--------|
| Google Search | TBD |
| Portal search | TBD |
| Proprietary search API | TBD |
| MCP | TBD |
| External LLMs | TBD |

*Each person owns 1–2 paths; assign so workload is even.*

### 4.1 Portal search (Algolia)

- **Method:** Call Algolia API with the query; capture top N results (e.g. top 5 or 10) with URL/title.
- **Tool:** Script (e.g. Node/JS or Python) using Algolia (or current portal search) API.
- **Query source:** **query_internal** (Internal search).
- **Output:** For each (issue_id, query, path=portal), store: list of (rank, url, title). Run every query in **query_internal** for each issue.

### 4.2 Proprietary search API (used by MCP)

- **Method:** Call the internal search API directly (REST). This API is **one** source of knowledge used by the MCP (not the only one); it is a **simple search** (keyword-style). Testing it in isolation lets us measure this path and compare with portal (Algolia) and full MCP. Enables future use (e.g. portal replacement).
- **Tool:** Script that calls the search API with each query; capture top N results (URL/snippet).
- **Query source:** **query_internal** (Internal search).
- **Output:** For each (issue_id, query, path=api), store: list of (rank, url or doc_ref). Run every query in **query_internal** for each issue.
- **Note:** Requires documented endpoints and an accessible route (per alignment with Bruno).

### 4.3 MCP

- **Method:** Use an agent (e.g., in Cursor) that calls the VTEX docs MCP search tool with the query; capture returned doc refs or snippets.
- **Tool:** Script or agent workflow that invokes MCP with each query and logs returned URIs/snippets.
- **Query source:** **query_agents** (Agents).
- **Output:** For each (issue_id, query, path=mcp), store: list of (rank, doc_ref or url). Run every query in **query_agents** for each issue.

### 4.4 Google Search

- **Method:** Programmatic search (no site restriction).
- **Tool:** Google Search API or manual.
- **Query source:** **query_external** (External search).
- **Output:** For each (issue_id, query, path=google), store: list of (rank, url, title). Run every query in **query_external** for each issue.
- **Note:** If API is not available or too costly, run a sample manually and record results in the same format.

### 4.5 External LLMs (ChatGPT, Claude, etc.)

- **Method:** Harder to automate. Options:
  - **A. Manual:** Fixed prompt per query (e.g. “Answer using VTEX docs: [query]”); human records whether the answer pointed to the expected doc.
  - **B. Semi-automated:** Same prompts, but “LLM-as-judge” step: second LLM call that scores whether the answer addresses the issue (e.g. 1–5 or binary). Maybe Cursor commands can help here.
  - **C. Programmatic:** Invoke LLMs via APIs (e.g. [OpenRouter](https://openrouter.ai/docs) for a single endpoint to ChatGPT/Claude and others, or direct OpenAI/Anthropic APIs); run prompts in a script, then evaluate results (human or LLM-as-judge).
- **Query source:** **query_agents** (Agents).
- **Output:** For each (issue_id, query, path=llm), store: at least pass/fail or score; optionally link to expected doc. Run every query in **query_agents** for each issue.

*Each path owner chooses manual vs automated (e.g. Google/LLMs can start as sample or manual) and implements accordingly.*

### 4.6 Output format (unified)

Store results in a simple, path-agnostic format so we can compute metrics the same way for every path. Example (JSON per run):

One result object per (issue_id, path, query). Optional `query_style` allows reporting pass rate by style (naive / familiar / expert).

```json
{
  "run_id": "baseline-2026-02",
  "results": [
    {
      "issue_id": "P1-01",
      "path": "portal",
      "query": "configure Y",
      "query_style": "expert",
      "top_results": [
        { "rank": 1, "url": "https://...", "title": "..." },
        { "rank": 2, "url": "https://...", "title": "..." }
      ]
    }
  ]
}
```

For LLM path, `top_results` can be replaced or complemented by a single `answer_relevant` (boolean) or `score` (number).

---

## 5. Success measurement

### 5.1 Ground truth

For each issue, **expected outcome** = one primary doc (URL or ID) that should be found. Tech writers set this when submitting the issue. Optionally: list of “acceptable” alternative docs.

### 5.2 Metric

- **Primary:** For each (issue, path), **pass** = expected doc appears in **top K** results (e.g. top 3 or top 5). **Fail** = it does not.
- **Aggregate:** 
  - **Per path:** % of queries that pass (e.g. “Portal: 70%”, “MCP: 55%”).
  - **Per persona:** % of queries that pass (e.g. Store operator: 72%, Developer: 65%, Decision maker: 80%) so we see if one persona is underserved.
  - **Per query style:** % that pass for naive vs familiar vs expert (so we see if “less sophisticated” queries are underserved).
  - **Overall:** % across all (issue, path, query) combinations.
- **Optional:** Relevance score (1–5) for ranking quality; can be added later (human or LLM judge).

### 5.3 Baseline report

- Table or chart: pass rate per path, per persona, and overall.
- List of failing (issue_id, path, query) for prioritising improvements.
- Same format can be reused for “after” runs to compare before/after.

---

## 6. Timeline (6 weeks)

| Phase | Duration | Focus | Tasks |
|-------|----------|--------|--------|
| **Issues + queries** | 2 weeks | Collect and consolidate | **Week 1:** Create issue/query template and example row; kickoff with tech writers (scope = each TW 5–8 issues; persona mix ~40/40/20 from the start). TWs submit issues with expected doc and persona. **Week 2:** Team adds queries per path (one of each type—naive, familiar, expert—per issue, per finding path); consolidate test suite artifact (spreadsheet/JSON); verify persona mix. |
| **Building the tests** | 2 weeks | Runners (parallel by path) | **Week 3:** Agree unified output format (§4.6). Each path owner implements runner for their path(s) in parallel. **Week 4:** Run smoke tests per path; fix issues; runners ready. |
| **Running the tests** | 1 week | Baseline run | **Week 5:** Each owner runs full test suite on their path(s); capture results in unified format. Aggregate raw results. Implement success metric; compute pass rate per path, per persona, overall; produce baseline report and list of failures. |
| **Review + mapping gaps** | 1 week | Handoff | **Week 6:** Review baseline with team; document gaps and improvement ideas; prioritise next steps; handoff to implementation phase. |

*Concrete start date to be set when kickoff is scheduled.*

---

## 7. Deliverables

| Deliverable | Description |
|-------------|-------------|
| **Test suite artifact** | Structured list of issues + queries + expected outcomes (e.g. spreadsheet or JSON). |
| **Runners** | Scripts or flows to run queries on all knowledge-finding paths. |
| **Baseline results** | Raw results (e.g. JSON) for the first full run. |
| **Baseline report** | Pass rate per path and overall; list of failing (issue, path, query); short narrative. |
| **Recommendations** | Prioritised improvement ideas based on failure patterns. |

---

## 8. Appendix

### A. Example issue/query row

| issue_id | persona | product | user_intent | expected_doc_url | query_external | query_internal | query_agents |
|----------|---------|---------|-------------|------------------|----------------|----------------|--------------|
| HC-01 | Store operator | Checkout | How to enable guest checkout | https://help.vtex.com/…/guest-checkout | enable guest checkout VTEX | guest checkout | How do I enable guest checkout? |

