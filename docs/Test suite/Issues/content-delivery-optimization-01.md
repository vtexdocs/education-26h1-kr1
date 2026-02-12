# Issue: Content delivery optimization

| Field | Value |
|-------|--------|
| **issue_id** | content-delivery-optimization-01 |
| **persona** | Decision maker |
| **product** | Cloud Infrastructure / Platform |
| **user_intent** | how does vtex handle content delivery optimization? |
| **expected_doc_url** | https://developers.vtex.com/docs/guides/cloud-infrastructure |
| **source** | Command input (user issue + target document URL) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | how does VTEX handle content delivery optimization |
| familiar | VTEX CDN content delivery network performance |
| expert | VTEX cloud infrastructure content delivery optimization |

**Array (query_external):**
```json
[
  { "query": "how does VTEX handle content delivery optimization", "style": "naive" },
  { "query": "VTEX CDN content delivery network performance", "style": "familiar" },
  { "query": "VTEX cloud infrastructure content delivery optimization", "style": "expert" }
]
```

### B — Internal search (Algolia / Proprietary API)

| style | query |
|-------|--------|
| naive | content delivery optimization |
| familiar | CDN caching content delivery |
| expert | cloud infrastructure content delivery optimization |

**Array (query_internal):**
```json
[
  { "query": "content delivery optimization", "style": "naive" },
  { "query": "CDN caching content delivery", "style": "familiar" },
  { "query": "cloud infrastructure content delivery optimization", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | vtex docs how does content delivery optimization work |
| familiar | vtex content delivery CDN |
| expert | cloud infrastructure content delivery |

**Array (query_mcp):**
```json
[
  { "query": "vtex docs how does content delivery optimization work", "style": "naive" },
  { "query": "vtex content delivery CDN", "style": "familiar" },
  { "query": "cloud infrastructure content delivery", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | how does VTEX optimize content delivery |
| familiar | how does VTEX handle CDN and content caching |
| expert | what is VTEX's content delivery optimization strategy including CDN router and cache layers |

**Array (query_llm):**
```json
[
  { "query": "how does VTEX optimize content delivery", "style": "naive" },
  { "query": "how does VTEX handle CDN and content caching", "style": "familiar" },
  { "query": "what is VTEX's content delivery optimization strategy including CDN router and cache layers", "style": "expert" }
]
```
