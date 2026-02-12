# Issue: Solve product indexing problems

| Field | Value |
|-------|--------|
| **issue_id** | product-indexing-01 |
| **persona** | Store operator |
| **product** | Catalog / Search |
| **user_intent** | How to solve product indexing problems |
| **expected_doc_url** | https://help.vtex.com/en/tutorial/understanding-how-indexation-works |
| **source** | Command input (user issue) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | my products are not updating in search results on my VTEX store |
| familiar | VTEX product indexing issues troubleshooting |
| expert | VTEX catalog indexing problems solution |

**Array (query_external):**
```json
[
  { "query": "my products are not updating in search results on my VTEX store", "style": "naive" },
  { "query": "VTEX product indexing issues troubleshooting", "style": "familiar" },
  { "query": "VTEX catalog indexing problems solution", "style": "expert" }
]
```

### B — Internal search (Algolia/Proprietary API)

| style | query |
|-------|--------|
| naive | products not updating search |
| familiar | product indexing issues |
| expert | catalog indexing troubleshooting |

**Array (query_internal):**
```json
[
  { "query": "products not updating search", "style": "naive" },
  { "query": "product indexing issues", "style": "familiar" },
  { "query": "catalog indexing troubleshooting", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | why are my product changes not showing up in search |
| familiar | troubleshoot product indexing VTEX |
| expert | solve product indexing problems VTEX catalog |

**Array (query_mcp):**
```json
[
  { "query": "why are my product changes not showing up in search", "style": "naive" },
  { "query": "troubleshoot product indexing VTEX", "style": "familiar" },
  { "query": "solve product indexing problems VTEX catalog", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | Why aren't my product updates appearing when customers search my store? |
| familiar | How do I fix product indexing issues in VTEX? |
| expert | How do I solve product indexing problems in VTEX? |

**Array (query_llm):**
```json
[
  { "query": "Why aren't my product updates appearing when customers search my store?", "style": "naive" },
  { "query": "How do I fix product indexing issues in VTEX?", "style": "familiar" },
  { "query": "How do I solve product indexing problems in VTEX?", "style": "expert" }
]
```
