# Issue: Split payment

| Field | Value |
|-------|--------|
| **issue_id** | split-payment-01 |
| **persona** | Decision Maker |
| **product** | Payments |
| **user_intent** | Understand how the payment split works at VTEX. |
| **expected_doc_url** | https://help.vtex.com/docs/tutorials/split-payment |
| **source** | Command input (user issue) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | how does payment split work in vtex |
| familiar | vtex payment split explained |
| expert | split payment vtex |

**Array (query_external):**
```json
[
  { "query": "how does payment split work in vtex", "style": "naive" },
  { "query": "vtex payment split explained", "style": "familiar" },
  { "query": "split payment vtex", "style": "expert" }
]
```

### B — Internal search (Algolia / Proprietary API)

| style | query |
|-------|--------|
| naive | split payment |
| familiar | payment split |
| expert | split payment |

**Array (query_internal):**
```json
[
  { "query": "split payment", "style": "naive" },
  { "query": "payment split", "style": "familiar" },
  { "query": "split payment", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | vtex docs on split payment |
| familiar | vtex split payment guide |
| expert | split payment |

**Array (query_mcp):**
```json
[
  { "query": "vtex docs on split payment", "style": "naive" },
  { "query": "vtex split payment guide", "style": "familiar" },
  { "query": "split payment", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | how do i understand payment split in vtex |
| familiar | explain how payment split works in vtex |
| expert | how does vtex split payment work |

**Array (query_llm):**
```json
[
  { "query": "how do i understand payment split in vtex", "style": "naive" },
  { "query": "explain how payment split works in vtex", "style": "familiar" },
  { "query": "how does vtex split payment work", "style": "expert" }
]
```
