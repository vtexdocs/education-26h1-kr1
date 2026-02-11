# Issue: Payment refunds

| Field | Value |
|-------|--------|
| **issue_id** | refund-payment-01 |
| **persona** | Decision Maker |
| **product** | Payments |
| **user_intent** | Identify how the payment refund was made at VTEX. |
| **expected_doc_url** | https://help.vtex.com/docs/tutorials/payment-refunds |
| **source** | Command input (user issue) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | how to see how a payment refund was made in vtex |
| familiar | identify payment refund method vtex |
| expert | payment refunds vtex |

**Array (query_external):**
```json
[
  { "query": "how to see how a payment refund was made in vtex", "style": "naive" },
  { "query": "identify payment refund method vtex", "style": "familiar" },
  { "query": "payment refunds vtex", "style": "expert" }
]
```

### B — Internal search (Algolia / Proprietary API)

| style | query |
|-------|--------|
| naive | payment refunds |
| familiar | refund method |
| expert | payment refunds |

**Array (query_internal):**
```json
[
  { "query": "payment refunds", "style": "naive" },
  { "query": "refund method", "style": "familiar" },
  { "query": "payment refunds", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | vtex docs on payment refunds |
| familiar | vtex payment refunds guide |
| expert | payment refunds |

**Array (query_mcp):**
```json
[
  { "query": "vtex docs on payment refunds", "style": "naive" },
  { "query": "vtex payment refunds guide", "style": "familiar" },
  { "query": "payment refunds", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | how do i identify how a payment refund was made in vtex |
| familiar | where can i see refund details in vtex payments |
| expert | how to identify payment refunds in vtex |

**Array (query_llm):**
```json
[
  { "query": "how do i identify how a payment refund was made in vtex", "style": "naive" },
  { "query": "where can i see refund details in vtex payments", "style": "familiar" },
  { "query": "how to identify payment refunds in vtex", "style": "expert" }
]
```
