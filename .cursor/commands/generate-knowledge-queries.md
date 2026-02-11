# Generate knowledge-finding queries for test suite

## Overview

Generate query arrays for the KR1 testing phase: one **naive**, one **familiar**, and one **expert** query per **query type** (External search, Internal search, MCP, External LLMs), then optionally add the issue as a row to the test suite spreadsheet. Follow the structure in `docs/Planning/Phase 1 - Testing.md` (§3.3–3.4).

## Input (from command params or user)

The agent receives the command; the user may append parameters after the command name (e.g. `/generate-knowledge-queries guest checkout https://help.vtex.com/.../guest-checkout A B`).

1. **User issue OR target document** (required)
   - **User issue:** Short description of the user intent (e.g. "How to enable guest checkout").
   - **Target document:** Markdown content or URL of the doc that should be found (expected outcome). Use this to infer the user issue and generate queries that should surface this doc. If only a topic/description is provided without a URL, use the **vtexdocs MCP** to search for and retrieve the relevant VTEX documentation URL.

2. **Query type(s)** (optional, default: all)
   - One or more query types. If not provided, the agent generates queries for **all** query types (A, B, C, D). To restrict, the user may append one or more letters (e.g. "A B C"):

   **A** — External search (Google)  
   **B** — Internal search (Algolia/Proprietary API)  
   **C** — MCP (proprietary docs)  
   **D** — External LLMs  

   Each query type maps to one array: `query_external`, `query_internal`, `query_mcp`, `query_llm`. Paths use these arrays: Google → external; Portal & API → internal; MCP → query_mcp; External LLMs → query_llm.

## Actions

### 1. Collect missing params

- If **user issue / target document** is missing: ask the user to provide either a short user intent description or a target doc (markdown or URL).
- If **query type(s)** are not provided: treat as **all** query types (A, B, C, D) and generate queries for all four. Do not ask the user.

### 2. Generate queries

- If the user gave a **target document** (URL or markdown): infer the user issue (product, user intent, expected_doc_url) from the doc; you may ask for issue_id, persona, and product if not inferrable.
- **expected_doc_url:** If the user provided a document topic or description but not a URL, use the **vtexdocs MCP** (`mcp_vtexdocs_search_documentation` and `mcp_vtexdocs_fetch_document`) to search for and retrieve the relevant VTEX documentation URL. Use this URL as the `expected_doc_url` field.
- **persona:** Must be one of: `'Developer'`, `'Store operator'`, `'Decision maker'`. Determine the persona based on the user intent or document content:
  - **`'Store operator'`** — Admin panel tasks, catalog management, payment method setup, inventory management, order management, configuration tasks in the VTEX admin interface. Examples: "How to configure payment methods", "Setting up product catalog", "Managing orders".
  - **`'Developer'`** — Storefront customization, Backoffice integration, APIs, development tasks, code integration, technical implementation. Examples: "How to customize storefront", "API integration", "Backoffice app development".
  - **`'Decision maker'`** — Checking platform capabilities, security, compliance, business features, strategic evaluation, platform comparison. Examples: "VTEX security features", "Platform compliance", "What capabilities does VTEX offer".
  - If the persona cannot be inferred from the user intent or document content, ask the user to specify which persona applies.
- For **each selected query type**, generate **exactly three queries**, one per style:
  - **naive** — Plain-language goal or problem; no product jargon.
  - **familiar** — Some product/domain terms; not the exact feature name.
  - **expert** — Official or canonical phrasing; close to doc/feature name.
- **Wording by query type:**
  - **External search (A):** Natural-language.
  - **Internal search (B):** Short, keyword-style.
  - **MCP (C):** MCP-appropriate phrasing (how the MCP is invoked).
  - **External LLMs (D):** User-style questions (how users ask ChatGPT, Claude, etc.).
- Output format per query type: array of objects `[{ "query": "...", "style": "naive"|"familiar"|"expert" }, ...]` with exactly 3 elements.

### 3. Create Markdown document

- Create a new `.md` file (e.g. in `docs/test-suite/issues/` or a path you propose) containing:
  - **Issue:** issue_id, persona (must be one of: `'Developer'`, `'Store operator'`, `'Decision maker'` — see persona decision criteria in step 2), product, user_intent, expected_doc_url (and optional source).
  - **Queries:** for each selected query type, the type name and the three queries (naive, familiar, expert) in a clear table or list.
- Save the file and tell the user where it is.

### 4. Ask about spreadsheet

- Ask the user: **Do you want this issue added as a new row in the test suite spreadsheet?**
  - **Y** — Yes, add a row (agent will use sheets-zap MCP).
  - **N** — No, only the Markdown doc is needed.
  - **L** — Yes, but first show me the row data so I can paste it elsewhere.

### 5. If user said Y (add row)

- Use the **user-sheets-zap** MCP tool `google_sheets_create_spreadsheet_row` to add one row with columns matching the spreadsheet data format (see Planning phase 1 §3.4.1):
  - **Issue columns:** issue_id, persona, product, user_intent, expected_doc_url (plain text).
  - **Query columns:** query_external, query_internal, query_mcp, query_llm. For each query type in scope (all four when none were specified; otherwise only the ones the user specified), put in the cell the **stringified JSON array** of exactly 3 objects: `[{"query":"...","style":"naive"},{"query":"...","style":"familiar"},{"query":"...","style":"expert"}]`. For query types not in scope, leave that column empty.
- **Spreadsheet:** Use the test suite spreadsheet below. Pass **spreadsheet** = `1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg` (or the full URL). Default **worksheet** has name='Issues and queries'; if the sheet has a different name, use that as **worksheet**. Only ask the user for spreadsheet/worksheet if they want a different target.
- In **instructions**, describe the row: issue fields + the query arrays for the selected query types. Include **output_hint** describing what you want back (e.g. "confirmation that the row was created and its row number").

## Output

- **Always:** Markdown document with the issue and all generated queries for the selected query types.
- **If user chose Y:** One new row in the test suite spreadsheet (via sheets-zap).
- **If user chose L:** Same row data shown in chat for the user to copy.

## Resources

- **Test suite spreadsheet:** [KR1 test suite](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0) — spreadsheet ID: `1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg`. Use this when adding a row (step 5).

## Reference

- Query structure and query types: `docs/Planning/Phase 1 - Testing.md` (§2, §3.3, §3.4, Appendix A).
- Persona definitions and target proportions: `docs/Planning/Phase 1 - Testing.md` (§3.1).
- Cursor commands: [Commands](https://cursor.com/docs/context/commands).
