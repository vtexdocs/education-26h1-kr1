# Task planning — KR1 Phase 1 (Testing phase)

## Intro

This document organises tasks for **KR1: Documentation infrastructure for content discoverability** (2026H1). The first phase is the **testing phase**: build a test suite that measures how well users find VTEX knowledge across all discovery paths, using 3 query types: External search (Google), Internal search (Algolia/Proprietary API), Agents (MCP/LLMs), then run a baseline before improvements. Phase 1 runs for **6 weeks** from kick off **2026-02-03**. Detailed scope, paths, and deliverables are in [Planning phase 1 (tests).md](Planning%20phase%201%20(tests).html). Tech writers register queries for the baseline test suite in the [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0).

---

## Epic (parent Jira issue)

- **Name:** KR1 — Documentation infrastructure for content discoverability
- **Description:** Build the foundational documentation infrastructure that makes VTEX content AI-ready, machine-readable, and discoverable across channels. This ensures content can be effectively indexed, retrieved, and surfaced for relevant user intents (Google Search, portal search, AI agents, MCP servers). This epic encompasses all work for KR1.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-06-30
- **Assignee:** Pedro Antunes Costa
- **Priority:** High

---

## Phase 1 — Jira tasks

### Issues + queries (Weeks 1–2)

#### Initial plan + project structure

- **Name:** Initial plan + project structure
- **Description:**
  1. Document and communicate the initial plan for Phase 1 (testing phase): scope, timelines, discovery paths (External search, Internal search, Agents), and deliverables. Align with [Planning phase 1 (tests).md](https://github.com/vtexdocs/education-26h1-kr1/blob/master/docs/planning/Planning%20phase%201%20(tests).md).
  2. Set up the project structure in the repo: define folder layout, key documentation locations, and any templates or placeholders needed for the test suite and subsequent work.
  3. Run kick-off meeting

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-05
- **Assignee:** Pedro Antunes Costa
- **Priority:** High

#### Create issue/query template and example row

- **Name:** Create issue/query template and example row
- **Description:**
  1. Define the template for each test-suite row with columns:
     - issue_id, persona, product, user_intent, expected_doc_url
     - query_external, query_internal, query_agents
  2. Document the template and how to fill each field.
  3. Add one complete example row (e.g. guest checkout) so tech writers can follow the same format when submitting issues. The template is used in the [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0).

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-11
- **Assignee:** Pedro Antunes Costa
- **Priority:** High


#### Tech writers submit issues, add query variants, and consolidate test suite artifact (Bárbara Celi)

- **Name:** Issues and queries
- **Description:**
  1. Submit 5–8 issues from your product(s) using the agreed template. For each issue include:
     - Persona, user intent, expected outcome (doc URL), optional source
  2. For each issue, add or refine query variants per query type:
     - External search (Google): natural-language
     - Internal search (Algolia/Proprietary API): keyword-style
     - Agents (MCP/LLMs): natural question
  3. Contribute your rows to the single consolidated test suite artifact: [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0) (columns as per §3.4 of the phase 1 plan).

  *Collectively aim for ~20–32 issues total and persona mix ~40/40/20.*

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-18
- **Assignee:** Bárbara Celi
- **Priority:** High

#### Tech writers submit issues, add query variants, and consolidate test suite artifact (Isabella Veloso Sa)

- **Name:** Issues and queries
- **Description:**
  1. Submit 5–8 issues from your product(s) using the agreed template. For each issue include:
     - Persona, user intent, expected outcome (doc URL), optional source
  2. For each issue, add or refine query variants per query type:
     - External search (Google): natural-language
     - Internal search (Algolia/Proprietary API): keyword-style
     - Agents (MCP/LLMs): natural question
  3. Contribute your rows to the single consolidated test suite artifact: [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0) (columns as per §3.4 of the phase 1 plan).

  *Collectively aim for ~20–32 issues total and persona mix ~40/40/20.*

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-18
- **Assignee:** Isabella Veloso Sa
- **Priority:** High

#### Tech writers submit issues, add query variants, and consolidate test suite artifact (Ricardo José Correia da Silva)

- **Name:** Issues and queries
- **Description:**
  1. Submit 5–8 issues from your product(s) using the agreed template. For each issue include:
     - Persona, user intent, expected outcome (doc URL), optional source
  2. For each issue, add or refine query variants per query type:
     - External search (Google): natural-language
     - Internal search (Algolia/Proprietary API): keyword-style
     - Agents (MCP/LLMs): natural question
  3. Contribute your rows to the single consolidated test suite artifact: [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0) (columns as per §3.4 of the phase 1 plan).

  *Collectively aim for ~20–32 issues total and persona mix ~40/40/20.*

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-18
- **Assignee:** Ricardo José Correia da Silva
- **Priority:** High

#### Tech writers submit issues, add query variants, and consolidate test suite artifact (Pedro Antunes Costa)

- **Name:** Issues and queries
- **Description:**
  1. Submit 5–8 issues from your product(s) using the agreed template. For each issue include:
     - Persona, user intent, expected outcome (doc URL), optional source
  2. For each issue, add or refine query variants per query type:
     - External search (Google): natural-language
     - Internal search (Algolia/Proprietary API): keyword-style
     - Agents (MCP/LLMs): natural question
  3. Contribute your rows to the single consolidated test suite artifact: [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0) (columns as per §3.4 of the phase 1 plan).

  *Collectively aim for ~20–32 issues total and persona mix ~40/40/20.*

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-18
- **Assignee:** Pedro Antunes Costa
- **Priority:** High

#### Verify persona mix in test suite

- **Name:** Verify persona mix in test suite
- **Description:**
  1. Check the consolidated test suite in the [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0) against the target persona distribution:
     - ~40% Store operator
     - ~40% Developer
     - ~20% Decision maker
  2. If the mix is off, adjust rows or request additional issues from tech writers.
  3. Lock the test suite for the building phase once the mix is acceptable.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-18
- **Assignee:** Pedro Antunes Costa
- **Priority:** Medium

---

### Building the tests (Weeks 3–4)

#### Agree unified output format for test results

- **Name:** Agree unified output format for test results
- **Description:**
  1. Finalise the path-agnostic output format (see §4.6 of the phase 1 plan). Example: JSON per run with:
     - run_id
     - results array (each result: issue_id, path, query, top_results)
  2. Document the schema and share it with all path owners.
  3. Confirm that every path owner can produce this format so results can be aggregated and metrics computed uniformly.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-25
- **Assignee:** Pedro Antunes Costa
- **Priority:** High

#### Implement Google Search path runner

- **Name:** Implement Google Search path runner
- **Description:**
  1. Implement a runner for the **Google Search** path (organic web search; no site restriction so we see full discoverability—our docs, community, third-party).
  2. **Method:** Programmatic search (no site restriction). If Google Search API is not available or too costly, run a sample manually and record results in the same format.
  3. **Tool:** Script using Google Search API, or manual recording.
  4. The runner must: read the test suite artifact and *query_external*; run each query; output results in the agreed unified format (see §4.6). For each (issue_id, query, path=google), store: list of (rank, url, title).
  5. Deliver the runner script or workflow so it can be run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** High

#### Implement Algolia (Help Center) path runner

- **Name:** Implement Algolia (Help Center) path runner
- **Description:**
  1. Implement a runner for the **Algolia (Help Center)** path—on-site search on the Help Center. Path ownership is assigned at kickoff.
  2. **Method:** Call Algolia API with the query; capture top N results (e.g. top 5 or 10) with URL/title. Use the Help Center Algolia index.
  3. **Tool:** Script (e.g. Node/JS or Python) using Algolia (or current Help Center portal search) API.
  4. The runner must: read the test suite artifact and *query_internal*; run each query; output results in the agreed unified format (see §4.6). For each (issue_id, query, path), store: list of (rank, url, title).
  5. Deliver the runner script so it can be run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** High

#### Implement Algolia (Dev Portal) path runner

- **Name:** Implement Algolia (Dev Portal) path runner
- **Description:**
  1. Implement a runner for the **Algolia (Dev Portal)** path—on-site search on the Developer Portal. Path ownership is assigned at kickoff.
  2. **Method:** Call Algolia API with the query; capture top N results (e.g. top 5 or 10) with URL/title. Use the Developer Portal Algolia index.
  3. **Tool:** Script (e.g. Node/JS or Python) using Algolia (or current Dev Portal search) API.
  4. The runner must: read the test suite artifact and *query_internal*; run each query; output results in the agreed unified format (see §4.6). For each (issue_id, query, path), store: list of (rank, url, title).
  5. Deliver the runner script so it can be run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** High

#### Implement Proprietary search API path runner

- **Name:** Implement Proprietary search API path runner
- **Description:**
  1. Implement a runner for the **Proprietary search API** path—simple search API used by the MCP; keyword-style queries (Algolia-like). Call the internal search API directly (REST).
  2. **Method:** Call the internal search API with each query; capture top N results (URL/snippet). Use *query_internal*—short, keyword-style queries (e.g. “guest checkout”, “configure payment”), not long natural-language questions. *query_agents* is for the full MCP/LLM experience.
  3. **Tool:** Script that calls the search API with each query. Requires documented endpoints and an accessible route (per alignment with Bruno).
  4. The runner must: read the test suite artifact; run each query; output results in the agreed unified format (see §4.6). For each (issue_id, query, path=api), store: list of (rank, url or doc_ref).
  5. Deliver the runner script so it can be run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** High

#### Implement MCP path runner

- **Name:** Implement MCP path runner
- **Description:**
  1. Implement a runner for the **MCP** path—VTEX docs MCP used inside Cursor or other agents; returns markdown from VTEX content; uses the proprietary search API. Path ownership is assigned at kickoff.
  2. **Method:** Use an agent (e.g. in Cursor) that calls the VTEX docs MCP search tool with the query; capture returned doc refs or snippets.
  3. **Tool:** Script or agent workflow that invokes MCP with each query and logs returned URIs/snippets. Use *query_agents* (natural question) for this path.
  4. The runner must: read the test suite artifact; run each query; output results in the agreed unified format (see §4.6). For each (issue_id, query, path=mcp), store: list of (rank, doc_ref or url).
  5. Deliver the runner script or workflow so it can be run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** High

#### Implement External LLMs path runner

- **Name:** Implement External LLMs path runner
- **Description:**
  1. Implement a runner for the **External LLMs** path—ChatGPT, Claude, etc. using web search or browsing; may hit Help Center or general web. Path ownership is assigned at kickoff.
  2. **Method:** Choose one of: (A) Manual: fixed prompt per query (e.g. “Answer using VTEX docs: [query]”); human records whether the answer pointed to the expected doc. (B) Semi-automated: same prompts + “LLM-as-judge” step (second LLM call scores whether the answer addresses the issue). (C) Programmatic: invoke LLMs via APIs (e.g. OpenRouter or direct OpenAI/Anthropic); run prompts in a script, then evaluate (human or LLM-as-judge).
  3. The runner/workflow must: read the test suite artifact and *query_agents*; run each query; output results in the agreed unified format (see §4.6). For each (issue_id, query, path=llm), store: at least pass/fail or score; optionally link to expected doc. For LLM path, *top_results* can be replaced or complemented by *answer_relevant* (boolean) or *score* (number).
  4. Deliver the runner or workflow so it can be run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** High

#### Run smoke tests — Google Search path

- **Name:** Run smoke tests — Google Search path
- **Description:**
  1. Run smoke tests using a subset of the test suite on the **Google Search** path (programmatic or manual; path=google, output: rank, url, title).
  2. Validate that the output matches the agreed unified format.
  3. Fix any issues in the runner.
  4. Ensure the runner is ready for the full baseline run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** Medium

#### Run smoke tests — Algolia (Help Center) path

- **Name:** Run smoke tests — Algolia (Help Center) path
- **Description:**
  1. Run smoke tests using a subset of the test suite on the **Algolia (Help Center)** path (Algolia API, top N results with URL/title).
  2. Validate that the output matches the agreed unified format.
  3. Fix any issues in the runner.
  4. Ensure the runner is ready for the full baseline run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** Medium

#### Run smoke tests — Algolia (Dev Portal) path

- **Name:** Run smoke tests — Algolia (Dev Portal) path
- **Description:**
  1. Run smoke tests using a subset of the test suite on the **Algolia (Dev Portal)** path (Algolia API, top N results with URL/title).
  2. Validate that the output matches the agreed unified format.
  3. Fix any issues in the runner.
  4. Ensure the runner is ready for the full baseline run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** Medium

#### Run smoke tests — Proprietary search API path

- **Name:** Run smoke tests — Proprietary search API path
- **Description:**
  1. Run smoke tests using a subset of the test suite on the **Proprietary search API** path (REST API, keyword-style queries, path=api, output: rank, url or doc_ref).
  2. Validate that the output matches the agreed unified format.
  3. Fix any issues in the runner.
  4. Ensure the runner is ready for the full baseline run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** Medium

#### Run smoke tests — MCP path

- **Name:** Run smoke tests — MCP path
- **Description:**
  1. Run smoke tests using a subset of the test suite on the **MCP** path (VTEX docs MCP search tool, path=mcp, output: rank, doc_ref or url).
  2. Validate that the output matches the agreed unified format.
  3. Fix any issues in the runner.
  4. Ensure the runner is ready for the full baseline run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** Medium

#### Run smoke tests — External LLMs path

- **Name:** Run smoke tests — External LLMs path
- **Description:**
  1. Run smoke tests using a subset of the test suite on the **External LLMs** path (ChatGPT, Claude, etc.; path=llm; output: pass/fail or score).
  2. Validate that the output matches the agreed unified format.
  3. Fix any issues in the runner or workflow.
  4. Ensure the runner is ready for the full baseline run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** Medium

---

### Running the tests (Week 5)

#### Full baseline run — Google Search path

- **Name:** Full baseline run — Google Search path
- **Description:**
  1. Run the full test suite on the **Google Search** path (path=google; output: rank, url, title).
  2. Capture results in the agreed unified format.
  3. Store raw results (e.g. JSON files) and hand them off for aggregation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Unassigned
- **Priority:** High

#### Full baseline run — Algolia (Help Center) path

- **Name:** Full baseline run — Algolia (Help Center) path
- **Description:**
  1. Run the full test suite on the **Algolia (Help Center)** path (Algolia API, top N results with URL/title).
  2. Capture results in the agreed unified format.
  3. Store raw results (e.g. JSON files) and hand them off for aggregation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Unassigned
- **Priority:** High

#### Full baseline run — Algolia (Dev Portal) path

- **Name:** Full baseline run — Algolia (Dev Portal) path
- **Description:**
  1. Run the full test suite on the **Algolia (Dev Portal)** path (Algolia API, top N results with URL/title).
  2. Capture results in the agreed unified format.
  3. Store raw results (e.g. JSON files) and hand them off for aggregation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Unassigned
- **Priority:** High

#### Full baseline run — Proprietary search API path

- **Name:** Full baseline run — Proprietary search API path
- **Description:**
  1. Run the full test suite on the **Proprietary search API** path (REST API, keyword-style queries; path=api; output: rank, url or doc_ref).
  2. Capture results in the agreed unified format.
  3. Store raw results (e.g. JSON files) and hand them off for aggregation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Unassigned
- **Priority:** High

#### Full baseline run — MCP path

- **Name:** Full baseline run — MCP path
- **Description:**
  1. Run the full test suite on the **MCP** path (VTEX docs MCP search tool; path=mcp; output: rank, doc_ref or url).
  2. Capture results in the agreed unified format.
  3. Store raw results (e.g. JSON files) and hand them off for aggregation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Unassigned
- **Priority:** High

#### Full baseline run — External LLMs path

- **Name:** Full baseline run — External LLMs path
- **Description:**
  1. Run the full test suite on the **External LLMs** path (ChatGPT, Claude, etc.; path=llm; output: pass/fail or score).
  2. Capture results in the agreed unified format.
  3. Store raw results (e.g. JSON files) and hand them off for aggregation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Unassigned
- **Priority:** High

#### Aggregate raw results and compute success metrics

- **Name:** Aggregate raw results and compute success metrics
- **Description:**
  1. Aggregate all path raw results into a single dataset.
  2. Implement the success metric: for each (issue, path), *pass* = expected doc appears in top K (e.g. top 3 or 5).
  3. Compute pass rate:
     - Per path
     - Per persona
     - Overall

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Pedro Antunes Costa
- **Priority:** High

#### Produce baseline report and list of failures

- **Name:** Produce baseline report and list of failures
- **Description:**
  1. Produce the baseline report containing:
     - Table or chart of pass rate per path, per persona, and overall
     - List of failing (issue_id, path, query) for prioritising improvements
     - Short narrative
  2. Use a format that can be reused for “after” runs.
  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Pedro Antunes Costa
- **Priority:** High

---

### Review + mapping gaps (Week 6)

#### Review baseline with team and document gaps (Bárbara Celi)

- **Name:** Review baseline with team and document gaps
- **Description:**
  1. Attend the team review of the baseline report.
  2. Document gaps and improvement ideas based on failure patterns in your area.
  3. Align with the team on findings before prioritisation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-18
- **Assignee:** Bárbara Celi
- **Priority:** Medium

#### Review baseline with team and document gaps (Isabella Veloso Sa)

- **Name:** Review baseline with team and document gaps
- **Description:**
  1. Attend the team review of the baseline report.
  2. Document gaps and improvement ideas based on failure patterns in your area.
  3. Align with the team on findings before prioritisation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-18
- **Assignee:** Isabella Veloso Sa
- **Priority:** Medium

#### Review baseline with team and document gaps (Ricardo José Correia da Silva)

- **Name:** Review baseline with team and document gaps
- **Description:**
  1. Attend the team review of the baseline report.
  2. Document gaps and improvement ideas based on failure patterns in your area.
  3. Align with the team on findings before prioritisation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-18
- **Assignee:** Ricardo José Correia da Silva
- **Priority:** Medium

#### Review baseline with team and document gaps (Pedro Antunes Costa)

- **Name:** Review baseline with team and document gaps
- **Description:**
  1. Attend the team review of the baseline report.
  2. Document gaps and improvement ideas based on failure patterns in your area.
  3. Align with the team on findings before prioritisation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-18
- **Assignee:** Pedro Antunes Costa
- **Priority:** Medium

#### Prioritise next steps and handoff to implementation phase

- **Name:** Prioritise next steps and handoff to implementation phase
- **Description:**
  1. Prioritise improvement ideas (e.g. by path or persona).
  2. Produce a short recommendations deliverable.
  3. Hand off to the implementation phase (or next phase) with clear next steps and owners.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-18
- **Assignee:** Pedro Antunes Costa
- **Priority:** Medium

---

*Phase 2 and later will be added to this document when planned.*
