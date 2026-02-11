# Issue: Payment settlement types

| Field | Value |
|-------|--------|
| **issue_id** | settlement-payment-01 |
| **persona** | Decision Maker |
| **product** | Payments |
| **user_intent** | Understand what types of payment settlement are at VTEX. |
| **expected_doc_url** | https://help.vtex.com/en/docs/tutorials/payment-settlement-types |
| **source** | Command input (user issue) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | types of payment settlement in vtex |
| familiar | vtex payment settlement types |
| expert | payment settlement types vtex |

**Array (query_external):**
```json
[
  { "query": "types of payment settlement in vtex", "style": "naive" },
  { "query": "vtex payment settlement types", "style": "familiar" },
  { "query": "payment settlement types vtex", "style": "expert" }
]
```

### B — Internal search (Algolia / Proprietary API)

| style | query |
|-------|--------|
| naive | payment settlement types |
| familiar | settlement types |
| expert | payment settlement types |

**Array (query_internal):**
```json
[
  { "query": "payment settlement types", "style": "naive" },
  { "query": "settlement types", "style": "familiar" },
  { "query": "payment settlement types", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | vtex docs on payment settlement types |
| familiar | vtex payment settlement types guide |
| expert | payment settlement types |

**Array (query_mcp):**
```json
[
  { "query": "vtex docs on payment settlement types", "style": "naive" },
  { "query": "vtex payment settlement types guide", "style": "familiar" },
  { "query": "payment settlement types", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | what types of payment settlement does vtex have |
| familiar | explain payment settlement types in vtex |
| expert | what are the payment settlement types at vtex |

**Array (query_llm):**
```json
[
  { "query": "what types of payment settlement does vtex have", "style": "naive" },
  { "query": "explain payment settlement types in vtex", "style": "familiar" },
  { "query": "what are the payment settlement types at vtex", "style": "expert" }
]
```
