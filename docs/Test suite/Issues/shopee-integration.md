# Issue: Shopee — Integrate store with Shopee

| Field | Value |
|-------|--------|
| **issue_id** | shopee-integration-01 |
| **persona** | Store operator |
| **product** | Marketplace / Integrations |
| **user_intent** | How to integrate my VTEX store with Shopee so I can sell on the Shopee marketplace. |
| **expected_doc_url** | https://help.vtex.com/en/docs/tracks/install-and-configure-shopee-connector |
| **source** | Command input (user issue) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | connect my VTEX online store to Shopee so I can sell there |
| familiar | VTEX Shopee marketplace connector setup |
| expert | install and configure Shopee connector VTEX |

**Array (query_external):**
```json
[
  { "query": "connect my VTEX online store to Shopee so I can sell there", "style": "naive" },
  { "query": "VTEX Shopee marketplace connector setup", "style": "familiar" },
  { "query": "install and configure Shopee connector VTEX", "style": "expert" }
]
```

### B — Internal search (Algolia/Proprietary API)

| style | query |
|-------|--------|
| naive | connect store Shopee sell |
| familiar | Shopee connector configure marketplace |
| expert | install configure Shopee connector VTEX |

**Array (query_internal):**
```json
[
  { "query": "connect store Shopee sell", "style": "naive" },
  { "query": "Shopee connector configure marketplace", "style": "familiar" },
  { "query": "install configure Shopee connector VTEX", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | how to connect my store to Shopee |
| familiar | configure Shopee connector marketplace integration |
| expert | install and configure Shopee connector |

**Array (query_mcp):**
```json
[
  { "query": "how to connect my store to Shopee", "style": "naive" },
  { "query": "configure Shopee connector marketplace integration", "style": "familiar" },
  { "query": "install and configure Shopee connector", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | How can I sell on Shopee with my VTEX store? |
| familiar | How do I set up the VTEX Shopee connector in Admin? |
| expert | How do I install and configure the Shopee connector for VTEX? |

**Array (query_llm):**
```json
[
  { "query": "How can I sell on Shopee with my VTEX store?", "style": "naive" },
  { "query": "How do I set up the VTEX Shopee connector in Admin?", "style": "familiar" },
  { "query": "How do I install and configure the Shopee connector for VTEX?", "style": "expert" }
]
```
