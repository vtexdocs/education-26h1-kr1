# Task planning — KR1 Phase 1 (Testing phase)

## Intro

This document organises tasks for **KR1: Documentation infrastructure for content discoverability** (2026H1). The first phase is the **testing phase**: build a test suite that measures how well users find VTEX knowledge across all discovery paths, using 4 query types: External search (Google), Internal search (Algolia/Proprietary API), MCP (proprietary docs), External LLMs, then run a baseline before improvements. Phase 1 runs for **6 weeks** from kick off **2026-02-03**. Detailed scope, paths, and deliverables are in [Phase 1 - Testing](Phase%201%20-%20Testing.md). Tech writers register queries for the baseline test suite in the [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0).

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

#### [Initial plan + project structure](https://vtex-dev.atlassian.net/browse/EDU-17422) — EDU-17422 (Resolved)

- **Name:** Initial plan + project structure
- **Jira issue:** [EDU-17422](https://vtex-dev.atlassian.net/browse/EDU-17422)
- **Status:** Resolved
- **Description:**
  1. Document and communicate the initial plan for Phase 1 (testing phase): scope, timelines, discovery paths (External search, Internal search, MCP, External LLMs), and deliverables. Align with [Phase 1 - Testing](https://github.com/vtexdocs/education-26h1-kr1/blob/master/docs/Planning/Phase%201%20-%20Testing.md).
  2. Set up the project structure in the repo: define folder layout, key documentation locations, and any templates or placeholders needed for the test suite and subsequent work.
  3. Run kick-off meeting

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-05
- **Assignee:** Pedro Antunes Costa
- **Priority:** High

#### [Create issue/query template and example row](https://vtex-dev.atlassian.net/browse/EDU-17423) — EDU-17423 (Resolved)

- **Name:** Create issue/query template and example row
- **Jira issue:** [EDU-17423](https://vtex-dev.atlassian.net/browse/EDU-17423)
- **Status:** Resolved
- **Description:**
  1. Define the template for each test-suite row with columns and cell format as in [Phase 1 - Testing](Phase%201%20-%20Testing.md) §3.4 and §3.4.1 (Spreadsheet data format): issue_id, persona, product, user_intent, expected_doc_url; query_external, query_internal, query_mcp, query_llm (each query column = stringified JSON array of 3 objects with `query` and `style`).
  2. Document the template and how to fill each field.
  3. Add one complete example row (e.g. guest checkout) so tech writers can follow the same format when submitting issues. The template is used in the [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0).

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-11
- **Assignee:** Pedro Antunes Costa
- **Priority:** High


#### [Issues and queries (Bárbara Celi)](https://vtex-dev.atlassian.net/browse/EDU-17427) — EDU-17427 (To Do)

- **Name:** Issues and queries
- **Jira issue:** [EDU-17427](https://vtex-dev.atlassian.net/browse/EDU-17427)
- **Status:** To Do
- **Description:**
  1. Submit 5–8 issues from your product(s) using the agreed template. For each issue include:
     - Persona, user intent, expected outcome (doc URL), optional source
  2. For each issue, add or refine query variants per query type:
     - External search (Google): natural-language
     - Internal search (Algolia/Proprietary API): keyword-style
     - MCP (proprietary docs): MCP-appropriate phrasing
- External LLMs: user-style questions
  3. Contribute your rows to the single consolidated test suite artifact: [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0) (columns as per §3.4 of the phase 1 plan).

  *Collectively aim for ~20–32 issues total and persona mix ~40/40/20.*

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-18
- **Assignee:** Bárbara Celi
- **Priority:** High

#### [Issues and queries (Isabella Veloso Sa)](https://vtex-dev.atlassian.net/browse/EDU-17425) — EDU-17426 (In Progress)

- **Name:** Issues and queries
- **Jira issue:** [EDU-17425](https://vtex-dev.atlassian.net/browse/EDU-17425)
- **Status:** In Progress
- **Description:**
  1. Submit 5–8 issues from your product(s) using the agreed template. For each issue include:
     - Persona, user intent, expected outcome (doc URL), optional source
  2. For each issue, add or refine query variants per query type:
     - External search (Google): natural-language
     - Internal search (Algolia/Proprietary API): keyword-style
     - MCP (proprietary docs): MCP-appropriate phrasing
- External LLMs: user-style questions
  3. Contribute your rows to the single consolidated test suite artifact: [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0) (columns as per §3.4 of the phase 1 plan).

  *Collectively aim for ~20–32 issues total and persona mix ~40/40/20.*

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-18
- **Assignee:** Isabella Veloso Sa
- **Priority:** High

#### [Issues and queries (Ricardo José Correia da Silva)](https://vtex-dev.atlassian.net/browse/EDU-17425) — EDU-17425 (Editing)

- **Name:** Issues and queries
- **Jira issue:** [EDU-17425](https://vtex-dev.atlassian.net/browse/EDU-17425)
- **Status:** Editing
- **Description:**
  1. Submit 5–8 issues from your product(s) using the agreed template. For each issue include:
     - Persona, user intent, expected outcome (doc URL), optional source
  2. For each issue, add or refine query variants per query type:
     - External search (Google): natural-language
     - Internal search (Algolia/Proprietary API): keyword-style
     - MCP (proprietary docs): MCP-appropriate phrasing
- External LLMs: user-style questions
  3. Contribute your rows to the single consolidated test suite artifact: [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0) (columns as per §3.4 of the phase 1 plan).

  *Collectively aim for ~20–32 issues total and persona mix ~40/40/20.*

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-18
- **Assignee:** Ricardo José Correia da Silva
- **Priority:** High

#### [Issues and queries (Pedro Antunes Costa)](https://vtex-dev.atlassian.net/browse/EDU-17424) — EDU-17424 (Reviewing)

- **Name:** Issues and queries
- **Jira issue:** [EDU-17424](https://vtex-dev.atlassian.net/browse/EDU-17424)
- **Status:** Reviewing
- **Description:**
  1. Submit 5–8 issues from your product(s) using the agreed template. For each issue include:
     - Persona, user intent, expected outcome (doc URL), optional source
  2. For each issue, add or refine query variants per query type:
     - External search (Google): natural-language
     - Internal search (Algolia/Proprietary API): keyword-style
     - MCP (proprietary docs): MCP-appropriate phrasing
- External LLMs: user-style questions
  3. Contribute your rows to the single consolidated test suite artifact: [baseline test suite spreadsheet](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0) (columns as per §3.4 of the phase 1 plan).

  *Collectively aim for ~20–32 issues total and persona mix ~40/40/20.*

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-02-18
- **Assignee:** Pedro Antunes Costa
- **Priority:** High

#### [Verify persona mix in test suite](https://vtex-dev.atlassian.net/browse/EDU-17428) — EDU-17428 (To Do)

- **Name:** Verify persona mix in test suite
- **Jira issue:** [EDU-17428](https://vtex-dev.atlassian.net/browse/EDU-17428)
- **Status:** To Do
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

#### [Agree unified output format for test results](https://vtex-dev.atlassian.net/browse/EDU-17429) — EDU-17429 (To Do)

- **Name:** Agree unified output format for test results
- **Jira issue:** [EDU-17429](https://vtex-dev.atlassian.net/browse/EDU-17429)
- **Status:** To Do
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

#### [Implement Google Search path runner](https://vtex-dev.atlassian.net/browse/EDU-17430) — EDU-17430 (Backlog)

- **Name:** Implement Google Search path runner
- **Jira issue:** [EDU-17430](https://vtex-dev.atlassian.net/browse/EDU-17430)
- **Status:** Backlog
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

#### [Implement Algolia (Help Center) path runner](https://vtex-dev.atlassian.net/browse/EDU-17431) — EDU-17431 (Duplicated)

- **Name:** Implement Algolia (Help Center) path runner
- **Jira issue:** [EDU-17431](https://vtex-dev.atlassian.net/browse/EDU-17431)
- **Status:** Duplicated
- **Description:**
  *This task's scope was merged into EDU-17433 due to similar methodology and identical queries.*

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** High

#### [Implement Algolia (Dev Portal) path runner](https://vtex-dev.atlassian.net/browse/EDU-17432) — EDU-17432 (Duplicated)

- **Name:** Implement Algolia (Dev Portal) path runner
- **Jira issue:** [EDU-17432](https://vtex-dev.atlassian.net/browse/EDU-17432)
- **Status:** Duplicated
- **Description:**
  *This task's scope was merged into EDU-17433 due to similar methodology and identical queries.*

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** High

#### [Implement Proprietary search API path runner](https://vtex-dev.atlassian.net/browse/EDU-17433) — EDU-17433 (Backlog)

- **Name:** Implement Proprietary search API path runner
- **Jira issue:** [EDU-17433](https://vtex-dev.atlassian.net/browse/EDU-17433)
- **Status:** Backlog
- **Description:**
  1. Implement runners for the **Algolia (Help Center)** path (on-site search on the Help Center), **Algolia (Dev Portal)** path (on-site search on the Developer Portal), and **Proprietary search API** path (simple search API used by the MCP; keyword-style queries). The methodology is similar across all three paths and they use the same queries.
  2. **Method:** 
     - with each query; capture top N results (URL/snippet). Use *query_internal*—short, keyword-style queries (e.g. “guest checkout”, “configure payment”), not long natural-language questions. *query_mcp* and *query_llm* are for the MCP and External LLMs paths respectively.
  3. **Tool:** Scripts (e.g. Node/JS or Python) using Algolia API for Help Center and Dev Portal, and a script that calls the search API for the Proprietary search API path. Requires documented endpoints and an accessible route (per alignment with Bruno).
  4. The runners must: read the test suite artifact and *query_internal*; run each query; output results in the agreed unified format (see §4.6). For each (issue_id, query, path), store: list of (rank, url, title) for Algolia paths, or list of (rank, url or doc_ref) for the API path.
  5. Deliver the runner scripts so they can be run in Week 5.

  *Note: This task merges the scope of EDU-17431 and EDU-17432, which were consolidated here due to similar methodology and identical queries.*

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** High

#### [Implement MCP path runner](https://vtex-dev.atlassian.net/browse/EDU-17434) — EDU-17434 (Backlog)

- **Name:** Implement MCP path runner
- **Jira issue:** [EDU-17434](https://vtex-dev.atlassian.net/browse/EDU-17434)
- **Status:** Backlog
- **Description:**
  1. Implement a runner for the **MCP** path—VTEX docs MCP used inside Cursor or other agents; returns markdown from VTEX content; uses the proprietary search API. Path ownership is assigned at kickoff.
  2. **Method:** Use an agent (e.g. in Cursor) that calls the VTEX docs MCP search tool with the query; capture returned doc refs or snippets.
  3. **Tool:** Script or agent workflow that invokes MCP with each query and logs returned URIs/snippets. Use *query_mcp* for this path.
  4. The runner must: read the test suite artifact; run each query; output results in the agreed unified format (see §4.6). For each (issue_id, query, path=mcp), store: list of (rank, doc_ref or url).
  5. Deliver the runner script or workflow so it can be run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** High

#### [Implement External LLMs path runner](https://vtex-dev.atlassian.net/browse/EDU-17435) — EDU-17435 (To Do)

- **Name:** Implement External LLMs path runner
- **Jira issue:** [EDU-17435](https://vtex-dev.atlassian.net/browse/EDU-17435)
- **Status:** To Do
- **Description:**
  1. Implement a runner for the **External LLMs** path—ChatGPT, Claude, etc. using web search or browsing; may hit Help Center or general web. Path ownership is assigned at kickoff.
  2. **Method:** Choose one of: (A) Manual: fixed prompt per query (e.g. “Answer using VTEX docs: [query]”); human records whether the answer pointed to the expected doc. (B) Semi-automated: same prompts + “LLM-as-judge” step (second LLM call scores whether the answer addresses the issue). (C) Programmatic: invoke LLMs via APIs (e.g. OpenRouter or direct OpenAI/Anthropic); run prompts in a script, then evaluate (human or LLM-as-judge).
  3. The runner/workflow must: read the test suite artifact and *query_llm*; run each query; output results in the agreed unified format (see §4.6). For each (issue_id, query, path=llm), store: at least pass/fail or score; optionally link to expected doc. For LLM path, *top_results* can be replaced or complemented by *answer_relevant* (boolean) or *score* (number).
  4. Deliver the runner or workflow so it can be run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** High

#### [Run smoke tests — Google Search path](https://vtex-dev.atlassian.net/browse/EDU-17436) — EDU-17436 (Backlog)

- **Name:** Run smoke tests — Google Search path
- **Jira issue:** [EDU-17436](https://vtex-dev.atlassian.net/browse/EDU-17436)
- **Status:** Backlog
- **Description:**
  1. Run smoke tests using a subset of the test suite on the **Google Search** path (programmatic or manual; path=google, output: rank, url, title).
  2. Validate that the output matches the agreed unified format.
  3. Fix any issues in the runner.
  4. Ensure the runner is ready for the full baseline run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** Medium

#### [Run smoke tests — Algolia (Help Center) path](https://vtex-dev.atlassian.net/browse/EDU-17437) — EDU-17437 (Backlog)

- **Name:** Run smoke tests — Algolia (Help Center) path
- **Jira issue:** [EDU-17437](https://vtex-dev.atlassian.net/browse/EDU-17437)
- **Status:** Backlog
- **Description:**
  1. Run smoke tests using a subset of the test suite on the **Algolia (Help Center)** path (Algolia API, top N results with URL/title).
  2. Validate that the output matches the agreed unified format.
  3. Fix any issues in the runner.
  4. Ensure the runner is ready for the full baseline run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** Medium

#### [Run smoke tests — Algolia (Dev Portal) path](https://vtex-dev.atlassian.net/browse/EDU-17438) — EDU-17438 (Backlog)

- **Name:** Run smoke tests — Algolia (Dev Portal) path
- **Jira issue:** [EDU-17438](https://vtex-dev.atlassian.net/browse/EDU-17438)
- **Status:** Backlog
- **Description:**
  1. Run smoke tests using a subset of the test suite on the **Algolia (Dev Portal)** path (Algolia API, top N results with URL/title).
  2. Validate that the output matches the agreed unified format.
  3. Fix any issues in the runner.
  4. Ensure the runner is ready for the full baseline run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** Medium

#### [Run smoke tests — Proprietary search API path](https://vtex-dev.atlassian.net/browse/EDU-17439) — EDU-17439 (Backlog)

- **Name:** Run smoke tests — Proprietary search API path
- **Jira issue:** [EDU-17439](https://vtex-dev.atlassian.net/browse/EDU-17439)
- **Status:** Backlog
- **Description:**
  1. Run smoke tests using a subset of the test suite on the **Proprietary search API** path (REST API, keyword-style queries, path=api, output: rank, url or doc_ref).
  2. Validate that the output matches the agreed unified format.
  3. Fix any issues in the runner.
  4. Ensure the runner is ready for the full baseline run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** Medium

#### [Run smoke tests — MCP path](https://vtex-dev.atlassian.net/browse/EDU-17440) — EDU-17440 (Backlog)

- **Name:** Run smoke tests — MCP path
- **Jira issue:** [EDU-17440](https://vtex-dev.atlassian.net/browse/EDU-17440)
- **Status:** Backlog
- **Description:**
  1. Run smoke tests using a subset of the test suite on the **MCP** path (VTEX docs MCP search tool, path=mcp, output: rank, doc_ref or url).
  2. Validate that the output matches the agreed unified format.
  3. Fix any issues in the runner.
  4. Ensure the runner is ready for the full baseline run in Week 5.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-04
- **Assignee:** Unassigned
- **Priority:** Medium

#### [Run smoke tests — External LLMs path](https://vtex-dev.atlassian.net/browse/EDU-17441) — EDU-17441 (Backlog)

- **Name:** Run smoke tests — External LLMs path
- **Jira issue:** [EDU-17441](https://vtex-dev.atlassian.net/browse/EDU-17441)
- **Status:** Backlog
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

#### [Full baseline run — Google Search path](https://vtex-dev.atlassian.net/browse/EDU-17442) — EDU-17442 (Backlog)

- **Name:** Full baseline run — Google Search path
- **Jira issue:** [EDU-17442](https://vtex-dev.atlassian.net/browse/EDU-17442)
- **Status:** Backlog
- **Description:**
  1. Run the full test suite on the **Google Search** path (path=google; output: rank, url, title).
  2. Capture results in the agreed unified format.
  3. Store raw results (e.g. JSON files) and hand them off for aggregation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Unassigned
- **Priority:** High

#### [Full baseline run — Algolia (Help Center) path](https://vtex-dev.atlassian.net/browse/EDU-17443) — EDU-17443 (Backlog)

- **Name:** Full baseline run — Algolia (Help Center) path
- **Jira issue:** [EDU-17443](https://vtex-dev.atlassian.net/browse/EDU-17443)
- **Status:** Backlog
- **Description:**
  1. Run the full test suite on the **Algolia (Help Center)** path (Algolia API, top N results with URL/title).
  2. Capture results in the agreed unified format.
  3. Store raw results (e.g. JSON files) and hand them off for aggregation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Unassigned
- **Priority:** High

#### [Full baseline run — Algolia (Dev Portal) path](https://vtex-dev.atlassian.net/browse/EDU-17444) — EDU-17444 (Backlog)

- **Name:** Full baseline run — Algolia (Dev Portal) path
- **Jira issue:** [EDU-17444](https://vtex-dev.atlassian.net/browse/EDU-17444)
- **Status:** Backlog
- **Description:**
  1. Run the full test suite on the **Algolia (Dev Portal)** path (Algolia API, top N results with URL/title).
  2. Capture results in the agreed unified format.
  3. Store raw results (e.g. JSON files) and hand them off for aggregation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Unassigned
- **Priority:** High

#### [Full baseline run — Proprietary search API path](https://vtex-dev.atlassian.net/browse/EDU-17445) — EDU-17445 (Backlog)

- **Name:** Full baseline run — Proprietary search API path
- **Jira issue:** [EDU-17445](https://vtex-dev.atlassian.net/browse/EDU-17445)
- **Status:** Backlog
- **Description:**
  1. Run the full test suite on the **Proprietary search API** path (REST API, keyword-style queries; path=api; output: rank, url or doc_ref).
  2. Capture results in the agreed unified format.
  3. Store raw results (e.g. JSON files) and hand them off for aggregation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Unassigned
- **Priority:** High

#### [Full baseline run — MCP path](https://vtex-dev.atlassian.net/browse/EDU-17446) — EDU-17446 (Backlog)

- **Name:** Full baseline run — MCP path
- **Jira issue:** [EDU-17446](https://vtex-dev.atlassian.net/browse/EDU-17446)
- **Status:** Backlog
- **Description:**
  1. Run the full test suite on the **MCP** path (VTEX docs MCP search tool; path=mcp; output: rank, doc_ref or url).
  2. Capture results in the agreed unified format.
  3. Store raw results (e.g. JSON files) and hand them off for aggregation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Unassigned
- **Priority:** High

#### [Full baseline run — External LLMs path](https://vtex-dev.atlassian.net/browse/EDU-17447) — EDU-17447 (Backlog)

- **Name:** Full baseline run — External LLMs path
- **Jira issue:** [EDU-17447](https://vtex-dev.atlassian.net/browse/EDU-17447)
- **Status:** Backlog
- **Description:**
  1. Run the full test suite on the **External LLMs** path (ChatGPT, Claude, etc.; path=llm; output: pass/fail or score).
  2. Capture results in the agreed unified format.
  3. Store raw results (e.g. JSON files) and hand them off for aggregation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-11
- **Assignee:** Unassigned
- **Priority:** High

#### [Aggregate raw results and compute success metrics](https://vtex-dev.atlassian.net/browse/EDU-17448) — EDU-17448 (Backlog)

- **Name:** Aggregate raw results and compute success metrics
- **Jira issue:** [EDU-17448](https://vtex-dev.atlassian.net/browse/EDU-17448)
- **Status:** Backlog
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

#### [Produce baseline report and list of failures](https://vtex-dev.atlassian.net/browse/EDU-17449) — EDU-17449 (Backlog)

- **Name:** Produce baseline report and list of failures
- **Jira issue:** [EDU-17449](https://vtex-dev.atlassian.net/browse/EDU-17449)
- **Status:** Backlog
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

#### [Review baseline with team and document gaps (Bárbara Celi)](https://vtex-dev.atlassian.net/browse/EDU-17450) — EDU-17450 (Backlog)

- **Name:** Review baseline with team and document gaps
- **Jira issue:** [EDU-17450](https://vtex-dev.atlassian.net/browse/EDU-17450)
- **Status:** Backlog
- **Description:**
  1. Attend the team review of the baseline report.
  2. Document gaps and improvement ideas based on failure patterns in your area.
  3. Align with the team on findings before prioritisation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-18
- **Assignee:** Bárbara Celi
- **Priority:** Medium

#### [Review baseline with team and document gaps (Isabella Veloso Sa)](https://vtex-dev.atlassian.net/browse/EDU-17451) — EDU-17451 (Backlog)

- **Name:** Review baseline with team and document gaps
- **Jira issue:** [EDU-17451](https://vtex-dev.atlassian.net/browse/EDU-17451)
- **Status:** Backlog
- **Description:**
  1. Attend the team review of the baseline report.
  2. Document gaps and improvement ideas based on failure patterns in your area.
  3. Align with the team on findings before prioritisation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-18
- **Assignee:** Isabella Veloso Sa
- **Priority:** Medium

#### [Review baseline with team and document gaps (Ricardo José Correia da Silva)](https://vtex-dev.atlassian.net/browse/EDU-17452) — EDU-17452 (Backlog)

- **Name:** Review baseline with team and document gaps
- **Jira issue:** [EDU-17452](https://vtex-dev.atlassian.net/browse/EDU-17452)
- **Status:** Backlog
- **Description:**
  1. Attend the team review of the baseline report.
  2. Document gaps and improvement ideas based on failure patterns in your area.
  3. Align with the team on findings before prioritisation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-18
- **Assignee:** Ricardo José Correia da Silva
- **Priority:** Medium

#### [Review baseline with team and document gaps (Pedro Antunes Costa)](https://vtex-dev.atlassian.net/browse/EDU-17453) — EDU-17453 (Backlog)

- **Name:** Review baseline with team and document gaps
- **Jira issue:** [EDU-17453](https://vtex-dev.atlassian.net/browse/EDU-17453)
- **Status:** Backlog
- **Description:**
  1. Attend the team review of the baseline report.
  2. Document gaps and improvement ideas based on failure patterns in your area.
  3. Align with the team on findings before prioritisation.

  *Project repo:* [education-26h1-kr1](https://github.com/vtexdocs/education-26h1-kr1)
- **Due date:** 2026-03-18
- **Assignee:** Pedro Antunes Costa
- **Priority:** Medium

#### [Prioritise next steps and handoff to implementation phase](https://vtex-dev.atlassian.net/browse/EDU-17454) — EDU-17454 (Backlog)

- **Name:** Prioritise next steps and handoff to implementation phase
- **Jira issue:** [EDU-17454](https://vtex-dev.atlassian.net/browse/EDU-17454)
- **Status:** Backlog
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
