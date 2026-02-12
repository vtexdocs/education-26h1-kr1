# Register all issue docs to test suite spreadsheet

## Overview

Read all issue markdown files from `docs/Test suite/Issues/` directory, parse their content, and register each issue as a new row in the test suite spreadsheet using the sheets-zap MCP tool. Only register issues that are not already present in the spreadsheet (check by `issue_id`).

## Actions

### 1. Read all issue files

- List all `.md` files in `docs/Test suite/Issues/` directory
- Read each markdown file to extract issue data and query arrays

### 2. Parse each issue file

Each markdown file follows this structure:

- **Issue metadata** (in a table at the top):
  - `issue_id` (string, e.g., `conciliations-payment-01`)
  - `persona` (string: `Store operator` | `Developer` | `Decision maker`)
  - `product` (string, e.g., `Payments`)
  - `user_intent` (string, short description)
  - `expected_doc_url` (string, full URL)
  - `source` (optional string)

- **Query arrays** (in JSON code blocks):
  - `query_external` — Array for External search (Google), format: `[{"query":"...","style":"naive"},{"query":"...","style":"familiar"},{"query":"...","style":"expert"}]`
  - `query_internal` — Array for Internal search (Algolia/Proprietary API), same format
  - `query_mcp` — Array for MCP (proprietary docs), same format
  - `query_llm` — Array for External LLMs, same format

**Parsing instructions:**
- Extract issue metadata from the table (lines starting with `| **issue_id**`, `| **persona**`, etc.)
- Extract each query array from JSON code blocks (look for sections like `**Array (query_external):**` followed by a JSON code block)
- Parse the JSON arrays to ensure they're valid (each should have exactly 3 objects with `query` and `style` fields)
- If a query type is missing (no array found), leave that column empty for that issue

### 3. Check existing spreadsheet entries

- Use sheets-zap MCP to read the spreadsheet and get all existing `issue_id` values
- **Spreadsheet ID:** `1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg`
- **Worksheet name:** `Issues and queries` (default)
- Filter out any issues that already exist in the spreadsheet (match by `issue_id`)

### 4. Register new issues

For each issue that is NOT already in the spreadsheet:

- Use the **sheets-zap** MCP tool `google_sheets_create_spreadsheet_row` to add one row
- **Spreadsheet:** `1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg` (or full URL: `https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit`)
- **Worksheet:** `Issues and queries`

- **Row data format** (columns in this order):
  1. `issue_id` — Plain text (e.g., `conciliations-payment-01`)
  2. `persona` — Plain text (`Store operator` | `Developer` | `Decision maker`)
  3. `product` — Plain text (e.g., `Payments`)
  4. `user_intent` — Plain text (short description)
  5. `expected_doc_url` — Plain text (full URL)
  6. `query_external` — **Stringified JSON array**: `[{"query":"...","style":"naive"},{"query":"...","style":"familiar"},{"query":"...","style":"expert"}]` (or empty if not present)
  7. `query_internal` — Same format (or empty if not present)
  8. `query_mcp` — Same format (or empty if not present)
  9. `query_llm` — Same format (or empty if not present)

- **Important:** Query columns must contain **stringified JSON arrays**, not plain text. Each array should have exactly 3 objects, one per style (naive, familiar, expert).

- In the **instructions** parameter, describe what you're adding: "Adding issue [issue_id] with persona [persona], product [product], and query arrays for [list query types present]"

- Include **output_hint**: "confirmation that the row was created and its row number"

### 5. Report results

After processing all files:
- Report how many issues were found
- Report how many were already in the spreadsheet (skipped)
- Report how many were successfully added
- List any issues that failed to parse or register (with error details)

## Resources

- **Test suite spreadsheet:** [KR1 test suite](https://docs.google.com/spreadsheets/d/1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg/edit?gid=0#gid=0)
- **Spreadsheet ID:** `1PbbIDcIhRnBQJPQzA-N-lifxURH_ywohXUqd9nAldZg`
- **Worksheet name:** `Issues and queries`
- **Issue files location:** `docs/Test suite/Issues/*.md`
- **Reference:** Spreadsheet data format is defined in `docs/Planning/Phase 1 - Testing.md` (§3.4.1)

## Notes

- If an issue file is missing a query array for a particular query type, leave that column empty (don't add an empty array)
- Ensure persona values match exactly: `Store operator`, `Developer`, or `Decision maker` (case-sensitive)
- Query arrays must be stringified JSON (as a string value in the cell), not parsed JSON objects
- Process issues one at a time to avoid rate limiting or errors
