# Issue: Implement Live Shopping for FastStore

| Field | Value |
|-------|--------|
| **issue_id** | live-shopping-faststore-01 |
| **persona** | Developer |
| **product** | FastStore / Live Shopping |
| **user_intent** | How to implement Live Shopping on a FastStore storefront |
| **expected_doc_url** | https://developers.vtex.com/docs/guides/faststore/storefront-features-implementing-live-shopping-for-faststore |
| **source** | Command input (target document URL) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | how to add live video streaming to my online store |
| familiar | VTEX FastStore live shopping setup |
| expert | implementing live shopping for FastStore VTEX |

**Array (query_external):**
```json
[
  { "query": "how to add live video streaming to my online store", "style": "naive" },
  { "query": "VTEX FastStore live shopping setup", "style": "familiar" },
  { "query": "implementing live shopping for FastStore VTEX", "style": "expert" }
]
```

### B — Internal search (Algolia/Proprietary API)

| style | query |
|-------|--------|
| naive | live video streaming store |
| familiar | FastStore live shopping |
| expert | live shopping FastStore implementation |

**Array (query_internal):**
```json
[
  { "query": "live video streaming store", "style": "naive" },
  { "query": "FastStore live shopping", "style": "familiar" },
  { "query": "live shopping FastStore implementation", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | how to stream live video on my store website |
| familiar | add live shopping player to FastStore |
| expert | implementing Live Shopping for FastStore |

**Array (query_mcp):**
```json
[
  { "query": "how to stream live video on my store website", "style": "naive" },
  { "query": "add live shopping player to FastStore", "style": "familiar" },
  { "query": "implementing Live Shopping for FastStore", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | How can I add a live streaming feature to my ecommerce website? |
| familiar | How do I set up live shopping on my VTEX FastStore site? |
| expert | How do I implement Live Shopping for FastStore in VTEX? |

**Array (query_llm):**
```json
[
  { "query": "How can I add a live streaming feature to my ecommerce website?", "style": "naive" },
  { "query": "How do I set up live shopping on my VTEX FastStore site?", "style": "familiar" },
  { "query": "How do I implement Live Shopping for FastStore in VTEX?", "style": "expert" }
]
```
