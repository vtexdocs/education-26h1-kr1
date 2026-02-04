# Generate knowledge-finding queries for test suite

## Overview

Generate query arrays for the KR1 testing phase: one **naive**, one **familiar**, and one **expert** query per knowledge-finding path, then optionally add the issue as a row to the test suite spreadsheet. Follow the structure in `docs/planning/Planning phase 1 (tests).md` (§3.3–3.4).

## Input (from command params or user)

The agent receives the command; the user may append parameters after the command name (e.g. `/generate-knowledge-queries guest checkout https://help.vtex.com/.../guest-checkout A B`).

1. **User issue OR target document** (required)
   - **User issue:** Short description of the user intent (e.g. "How to enable guest checkout").
   - **Target document:** Markdown content or URL of the doc that should be found (expected outcome). Use this to infer the user issue and generate queries that should surface this doc.

2. **Knowledge-finding path(s)** (required)
   - One or more paths. If not provided, ask the user with **lettered options** so they can reply with one or more letters (e.g. "A C E"):

   **A** — Google Search  
   **B** — Portal search  
   **C** — Proprietary search API  
   **D** — MCP  
   **E** — External LLMs  

   Paths **D** and **E** share the same query array (`query_mcp_llm`). Paths **B** and **C** share wording style (keyword-style) but have separate arrays (`query_portal`, `query_api`).

## Actions

### 1. Collect missing params

- If **user issue / target document** is missing: ask the user to provide either a short user intent description or a target doc (markdown or URL).
- If **knowledge-finding path(s)** are missing: ask with the lettered list above and say they can answer with one or more letters (e.g. "A", "A B", "A B C D E").

### 2. Generate queries

- If the user gave a **target document** (URL or markdown): infer the user issue (product, user intent, expected_doc_url) from the doc; you may ask for issue_id, persona, and product if not inferrable.
- For **each selected path**, generate **exactly three queries**, one per type:
  - **naive** — Plain-language goal or problem; no product jargon.
  - **familiar** — Some product/domain terms; not the exact feature name.
  - **expert** — Official or canonical phrasing; close to doc/feature name.
- **Wording by path:**
  - **Google (A):** Mix of natural-language and keyword-style.
  - **Portal (B) / API (C):** Short, keyword-style.
  - **MCP (D) / LLMs (E):** Natural questions and intent phrases (same array `query_mcp_llm` for both).
- Output format per path: array of objects `[{ "query": "...", "style": "naive"|"familiar"|"expert" }, ...]` with exactly 3 elements.

### 3. Create Markdown document

- Create a new `.md` file (e.g. in `docs/planning/issues/` or a path you propose) containing:
  - **Issue:** issue_id, persona, product, user_intent, expected_doc_url (and optional source).
  - **Queries:** for each selected path, the path name and the three queries (naive, familiar, expert) in a clear table or list.
- Save the file and tell the user where it is.

### 4. Ask about spreadsheet

- Ask the user: **Do you want this issue added as a new row in the test suite spreadsheet?**
  - **Y** — Yes, add a row (agent will use sheets-zap MCP).
  - **N** — No, only the Markdown doc is needed.
  - **L** — Yes, but first show me the row data so I can paste it elsewhere.

### 5. If user said Y (add row)

- Use the **user-sheets-zap** MCP tool `google_sheets_create_spreadsheet_row` to add one row with:
  - issue_id, persona, product, user_intent, expected_doc_url
  - query_google, query_portal, query_api, query_mcp_llm (each as the stringified JSON array of 3 query objects, or in the format the spreadsheet expects)
- For paths the user did **not** select, leave that path’s column empty in the row (or ask the user).
- **Spreadsheet:** Use the test suite spreadsheet below. Pass **spreadsheet** = `1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg` (or the full URL). Default **worksheet** has name='Issues and queries'; if the sheet has a different name, use that as **worksheet**. Only ask the user for spreadsheet/worksheet if they want a different target.
- In **instructions**, describe the row: issue fields + the query arrays for the selected paths. Include **output_hint** describing what you want back (e.g. "confirmation that the row was created and its row number").

## Output

- **Always:** Markdown document with the issue and all generated queries for the selected paths.
- **If user chose Y:** One new row in the test suite spreadsheet (via sheets-zap).
- **If user chose L:** Same row data shown in chat for the user to copy.

## Resources

- **Test suite spreadsheet:** [KR1 test suite](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0) — spreadsheet ID: `1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg`. Use this when adding a row (step 5).

## Reference

- Query structure and path list: `docs/planning/Planning phase 1 (tests).md` (§2, §3.3, §3.4, Appendix A).
- Cursor commands: [Commands](https://cursor.com/docs/context/commands).
