# Register all issue docs to test suite spreadsheet

## Overview

Read all issue markdown files from `docs/Test suite/Issues/` directory, parse their content, and register each issue as a new row in the test suite spreadsheet using the sheets-zap MCP tool. Only register issues that are not already present in the spreadsheet (check by `issue_id`).

## Actions

### 1. Read all issue files

- List all `.md` files in `docs/Test suite/Issues/` directory
- Read each markdown file to extract issue data and query arrays

### 2. Parse each issue file

Each markdown file follows this structure:

- **Issue metadata** (in a markdown table at the top):
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

**Detailed parsing instructions:**

#### Step 2.1: Extract issue metadata from the table

The table format is:
```
| Field | Value |
|-------|--------|
| **issue_id** | conditions-payment-01 |
| **persona** | Store operator |
| **product** | Payments |
| **user_intent** | How to configure special conditions... |
| **expected_doc_url** | https://help.vtex.com/... |
```

**Extraction method:**
- Find the markdown table (starts with `| Field | Value |`)
- For each row, extract the value from the **second column** (after the `|`)
- Map field names to variables:
  - Row containing `**issue_id**` → extract the value after the second `|` (e.g., `conditions-payment-01`)
  - Row containing `**persona**` → extract the value (e.g., `Store operator`)
  - Row containing `**product**` → extract the value (e.g., `Payments`)
  - Row containing `**user_intent**` → extract the value (e.g., `How to configure special conditions for payment methods registered in my VTEX store.`)
  - Row containing `**expected_doc_url**` → extract the value (e.g., `https://help.vtex.com/docs/tutorials/special-conditions`)
- **Important:** Extract the actual text value, not the markdown formatting. Strip any leading/trailing whitespace.

#### Step 2.2: Extract query arrays from JSON code blocks

Each query type has a section like:
```
**Array (query_external):**
```json
[
  { "query": "...", "style": "naive" },
  { "query": "...", "style": "familiar" },
  { "query": "...", "style": "expert" }
]
```
```

**Extraction method:**
- Search for text patterns: `**Array (query_external):**`, `**Array (query_internal):**`, `**Array (query_mcp):**`, `**Array (query_llm):**`
- After finding each pattern, locate the next JSON code block (between ` ```json` and ` ``` `)
- **Extract the entire JSON array as a string** (including the brackets `[` and `]`, and all objects inside)
- Parse the JSON to validate it's valid (should be an array with exactly 3 objects, each with `query` and `style` fields)
- **Convert the JSON array to a stringified format** for the spreadsheet: use `JSON.stringify()` or manually format as a single-line string like: `[{"query":"...","style":"naive"},{"query":"...","style":"familiar"},{"query":"...","style":"expert"}]`
- If a query type section is missing or has no JSON code block, leave that variable empty/null

**Example extraction:**
- Find `**Array (query_external):**`
- Extract JSON from code block: `[\n  { "query": "how to set special conditions...", "style": "naive" },\n  ...\n]`
- Stringify to: `[{"query":"how to set special conditions for payment methods in vtex","style":"naive"},{"query":"configure special payment conditions vtex","style":"familiar"},{"query":"special conditions vtex payments","style":"expert"}]`
- Store this stringified JSON in the `query_external` variable

#### Step 2.3: Validate parsed data

Before proceeding, verify:
- All required fields are extracted: `issue_id`, `persona`, `product`, `user_intent`, `expected_doc_url`
- Each query array (if present) is a valid JSON string with exactly 3 objects
- Persona value matches exactly: `Store operator`, `Developer`, or `Decision maker` (case-sensitive)

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
  1. `issue_id` — Plain text string (e.g., `conciliations-payment-01`)
  2. `persona` — Plain text string (`Store operator` | `Developer` | `Decision maker`)
  3. `product` — Plain text string (e.g., `Payments`)
  4. `user_intent` — Plain text string (the full description text, e.g., `How to configure special conditions for payment methods registered in my VTEX store.`)
  5. `expected_doc_url` — Plain text string (the full URL, e.g., `https://help.vtex.com/docs/tutorials/special-conditions`)
  6. `query_external` — **Stringified JSON array as a single string**: `[{"query":"how to set special conditions for payment methods in vtex","style":"naive"},{"query":"configure special payment conditions vtex","style":"familiar"},{"query":"special conditions vtex payments","style":"expert"}]` (or empty string `""` if not present in the file)
  7. `query_internal` — Same format: stringified JSON array as a single string (or empty string `""` if not present)
  8. `query_mcp` — Same format: stringified JSON array as a single string (or empty string `""` if not present)
  9. `query_llm` — Same format: stringified JSON array as a single string (or empty string `""` if not present)

- **CRITICAL:** 
  - Query columns must contain **the actual stringified JSON array**, not the word "arrays" or any placeholder text
  - The JSON should be formatted as a single-line string (no newlines, but spaces are OK)
  - Example of correct format: `[{"query":"text here","style":"naive"},{"query":"text here","style":"familiar"},{"query":"text here","style":"expert"}]`
  - If a query type is missing from the file, pass an empty string `""` for that column, not `null` or `undefined`

- In the **instructions** parameter, provide clear instructions like: "Create a new row with issue_id='[value]', persona='[value]', product='[value]', user_intent='[value]', expected_doc_url='[value]', query_external='[stringified JSON]', query_internal='[stringified JSON]', query_mcp='[stringified JSON]', query_llm='[stringified JSON]'. Use empty string for any query columns that are missing."

- Include **output_hint**: "confirmation that the row was created with all 9 columns filled correctly, showing the row number"

- **Before calling the tool, verify:**
  - You have extracted actual text values for `user_intent` and `expected_doc_url` (not empty/null)
  - You have extracted actual stringified JSON arrays for query columns (not the word "arrays" or any placeholder)
  - Each query JSON string starts with `[` and ends with `]` and contains exactly 3 objects

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

## Example: Expected data format

For the file `conditions-payment-01.md`, after parsing you should have:

**Issue metadata:**
- `issue_id` = `"conditions-payment-01"`
- `persona` = `"Store operator"`
- `product` = `"Payments"`
- `user_intent` = `"How to configure special conditions for payment methods registered in my VTEX store."`
- `expected_doc_url` = `"https://help.vtex.com/docs/tutorials/special-conditions"`

**Query arrays (stringified JSON strings):**
- `query_external` = `"[{\"query\":\"how to set special conditions for payment methods in vtex\",\"style\":\"naive\"},{\"query\":\"configure special payment conditions vtex\",\"style\":\"familiar\"},{\"query\":\"special conditions vtex payments\",\"style\":\"expert\"}]"`
- `query_internal` = `"[{\"query\":\"special conditions payments\",\"style\":\"naive\"},{\"query\":\"payment method conditions\",\"style\":\"familiar\"},{\"query\":\"special conditions\",\"style\":\"expert\"}]"`
- `query_mcp` = `"[{\"query\":\"vtex docs on special conditions for payments\",\"style\":\"naive\"},{\"query\":\"vtex special payment conditions setup\",\"style\":\"familiar\"},{\"query\":\"special conditions\",\"style\":\"expert\"}]"`
- `query_llm` = `"[{\"query\":\"how do i configure special conditions for payment methods in vtex\",\"style\":\"naive\"},{\"query\":\"steps to set special conditions for vtex payment methods\",\"style\":\"familiar\"},{\"query\":\"how to configure special conditions for payment methods in vtex\",\"style\":\"expert\"}]"`

**When passing to sheets-zap:**
- Pass each of these as separate field values
- The query arrays are **strings** containing JSON, not JSON objects themselves
- Use the actual extracted values, not placeholders or descriptions

## Notes

- If an issue file is missing a query array for a particular query type, use an empty string `""` for that column (not `null`, `undefined`, or the word "arrays")
- Ensure persona values match exactly: `Store operator`, `Developer`, or `Decision maker` (case-sensitive)
- Query arrays must be stringified JSON (as a string value in the cell), not parsed JSON objects
- Process issues one at a time to avoid rate limiting or errors
- **DO NOT** use placeholder text like "arrays" or "query data" - always extract and use the actual JSON string from the file
