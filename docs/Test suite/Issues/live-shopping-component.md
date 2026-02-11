# Issue: Place Live Shopping component on storefront

| Field | Value |
|-------|--------|
| **issue_id** | live-shopping-component-01 |
| **persona** | Store Admin |
| **product** | Live Shopping / Storefront |
| **user_intent** | How to place the Live Shopping component on the storefront |
| **expected_doc_url** | https://help.vtex.com/en/docs/tracks/placing-the-live-shopping-component |
| **source** | Command input (target document URL) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | how to add live video player to my ecommerce website |
| familiar | VTEX Live Shopping component setup storefront |
| expert | placing the Live Shopping component VTEX |

**Array (query_external):**
```json
[
  { "query": "how to add live video player to my ecommerce website", "style": "naive" },
  { "query": "VTEX Live Shopping component setup storefront", "style": "familiar" },
  { "query": "placing the Live Shopping component VTEX", "style": "expert" }
]
```

### B — Internal search (Algolia/Proprietary API)

| style | query |
|-------|--------|
| naive | add video player store |
| familiar | Live Shopping component storefront |
| expert | placing Live Shopping component |

**Array (query_internal):**
```json
[
  { "query": "add video player store", "style": "naive" },
  { "query": "Live Shopping component storefront", "style": "familiar" },
  { "query": "placing Live Shopping component", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | how to put a live streaming player on my store page |
| familiar | add Live Shopping component to storefront VTEX |
| expert | placing the Live Shopping component |

**Array (query_mcp):**
```json
[
  { "query": "how to put a live streaming player on my store page", "style": "naive" },
  { "query": "add Live Shopping component to storefront VTEX", "style": "familiar" },
  { "query": "placing the Live Shopping component", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | How do I add a live video player to my online store homepage? |
| familiar | How do I add the Live Shopping component to my VTEX store? |
| expert | How do I place the Live Shopping component on my VTEX storefront? |

**Array (query_llm):**
```json
[
  { "query": "How do I add a live video player to my online store homepage?", "style": "naive" },
  { "query": "How do I add the Live Shopping component to my VTEX store?", "style": "familiar" },
  { "query": "How do I place the Live Shopping component on my VTEX storefront?", "style": "expert" }
]
```
