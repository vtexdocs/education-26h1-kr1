# Issue: Orders Feed (Feed v3)

| Field | Value |
|-------|--------|
| **issue_id** | orders-feed-01 |
| **persona** | Developer |
| **product** | Orders / Order Management |
| **user_intent** | How to use the order feed (Feed v3) to track order updates and build order integrations (vs List orders). |
| **expected_doc_url** | https://developers.vtex.com/docs/guides/orders-feed |
| **source** | Target document (command input) |

---

## Queries by path

### A — Google Search

| style | query |
|-------|--------|
| naive | get order updates as they happen instead of checking every order |
| familiar | VTEX order feed integration track status changes |
| expert | VTEX Feed v3 order feed configuration guide |

**Array (query_google):**
```json
[
  { "query": "get order updates as they happen instead of checking every order", "style": "naive" },
  { "query": "VTEX order feed integration track status changes", "style": "familiar" },
  { "query": "VTEX Feed v3 order feed configuration guide", "style": "expert" }
]
```

### B — Portal search

| style | query |
|-------|--------|
| naive | order updates events feed |
| familiar | order feed filter queue configure |
| expert | Feed v3 orders feed |

**Array (query_portal):**
```json
[
  { "query": "order updates events feed", "style": "naive" },
  { "query": "order feed filter queue configure", "style": "familiar" },
  { "query": "Feed v3 orders feed", "style": "expert" }
]
```

### C — Proprietary search API

| style | query |
|-------|--------|
| naive | orders feed events |
| familiar | feed v3 filter queue orders |
| expert | orders feed configuration API |

**Array (query_api):**
```json
[
  { "query": "orders feed events", "style": "naive" },
  { "query": "feed v3 filter queue orders", "style": "familiar" },
  { "query": "orders feed configuration API", "style": "expert" }
]
```

### D — MCP (query_mcp_llm)

| style | query |
|-------|--------|
| naive | I need to know when orders change so I can sync with my system. How do I get order updates? |
| familiar | How do I configure the VTEX order feed to get order status updates for my integration? |
| expert | How do I set up Feed v3 for orders and what's the difference from List orders and Hook? |

**Array (query_mcp_llm):**
```json
[
  { "query": "I need to know when orders change so I can sync with my system. How do I get order updates?", "style": "naive" },
  { "query": "How do I configure the VTEX order feed to get order status updates for my integration?", "style": "familiar" },
  { "query": "How do I set up Feed v3 for orders and what's the difference from List orders and Hook?", "style": "expert" }
]
```
