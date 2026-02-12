# Issue: Lookup orders by invoice creation date

| Field | Value |
|-------|--------|
| **issue_id** | orders-api-invoice-date-01 |
| **persona** | Developer |
| **product** | Orders API |
| **user_intent** | How to lookup/filter orders by the date of invoice creation. |
| **expected_doc_url** | https://developers.vtex.com/docs/api-reference/orders-api#get-/api/oms/pvt/orders |
| **source** | Command input (target document URL) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | how to find orders by invoice date in VTEX |
| familiar | VTEX orders api filter by invoice creation date |
| expert | VTEX orders api get orders by invoice date |

**Array (query_external):**
```json
[
  { "query": "how to find orders by invoice date in VTEX", "style": "naive" },
  { "query": "VTEX orders api filter by invoice creation date", "style": "familiar" },
  { "query": "VTEX orders api get orders by invoice date", "style": "expert" }
]
```

### B — Internal search (Algolia / Proprietary API)

| style | query |
|-------|--------|
| naive | orders invoice date filter |
| familiar | get orders by invoice creation date |
| expert | orders api invoice date |

**Array (query_internal):**
```json
[
  { "query": "orders invoice date filter", "style": "naive" },
  { "query": "get orders by invoice creation date", "style": "familiar" },
  { "query": "orders api invoice date", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | vtex docs orders api filter by invoice creation date |
| familiar | vtex orders api invoice date filter |
| expert | orders api get orders invoice date |

**Array (query_mcp):**
```json
[
  { "query": "vtex docs orders api filter by invoice creation date", "style": "naive" },
  { "query": "vtex orders api invoice date filter", "style": "familiar" },
  { "query": "orders api get orders invoice date", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | how do i find orders created on a specific invoice date in vtex |
| familiar | what api endpoint lets me filter orders by invoice creation date in vtex |
| expert | how to query orders by invoice date using vtex orders api |

**Array (query_llm):**
```json
[
  { "query": "how do i find orders created on a specific invoice date in vtex", "style": "naive" },
  { "query": "what api endpoint lets me filter orders by invoice creation date in vtex", "style": "familiar" },
  { "query": "how to query orders by invoice date using vtex orders api", "style": "expert" }
]
```
