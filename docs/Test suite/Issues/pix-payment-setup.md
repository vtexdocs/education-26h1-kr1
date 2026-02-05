# Issue: Set up PIX payment in my VTEX store

| Field | Value |
|-------|--------|
| **issue_id** | pix-payment-01 |
| **persona** | Store operator |
| **product** | Payments |
| **user_intent** | Set up PIX payment in my VTEX store |
| **expected_doc_url** | https://newhelp.vtex.com/en/docs/tutorials/setting-up-payments-with-bluepay |
| **source** | Command input (user issue) |

*Note: PIX can be enabled via several payment providers (e.g. BluePay, PagoExpress, Pay4Fun, Shipay). The URL above is one representative tutorial; success may also be measured against other provider setup docs or a generic payment-provider overview.*

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | accept instant bank transfers from customers in my online store |
| familiar | enable PIX payment in my VTEX store |
| expert | how to set up PIX payment provider in VTEX |

**Array (query_external):**
```json
[
  { "query": "accept instant bank transfers from customers in my online store", "style": "naive" },
  { "query": "enable PIX payment in my VTEX store", "style": "familiar" },
  { "query": "how to set up PIX payment provider in VTEX", "style": "expert" }
]
```

### B — Internal search (Algolia/Proprietary API)

| style | query |
|-------|--------|
| naive | payment instant transfer online store |
| familiar | PIX payment VTEX provider setup |
| expert | set up PIX payment provider VTEX Store Settings |

**Array (query_internal):**
```json
[
  { "query": "payment instant transfer online store", "style": "naive" },
  { "query": "PIX payment VTEX provider setup", "style": "familiar" },
  { "query": "set up PIX payment provider VTEX Store Settings", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | how to accept PIX payments in my store |
| familiar | configure PIX payment provider VTEX |
| expert | setting up payments with PIX provider VTEX |

**Array (query_mcp):**
```json
[
  { "query": "how to accept PIX payments in my store", "style": "naive" },
  { "query": "configure PIX payment provider VTEX", "style": "familiar" },
  { "query": "setting up payments with PIX provider VTEX", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | How can I let customers pay with PIX in my store? |
| familiar | How do I set up PIX payment in my VTEX store? |
| expert | How do I configure a PIX payment provider in VTEX Admin? |

**Array (query_llm):**
```json
[
  { "query": "How can I let customers pay with PIX in my store?", "style": "naive" },
  { "query": "How do I set up PIX payment in my VTEX store?", "style": "familiar" },
  { "query": "How do I configure a PIX payment provider in VTEX Admin?", "style": "expert" }
]
```
