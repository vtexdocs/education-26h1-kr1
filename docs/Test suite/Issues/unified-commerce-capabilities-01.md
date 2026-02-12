# Issue: VTEX omnichannel capabilities

| Field | Value |
|-------|--------|
| **issue_id** | unified-commerce-capabilities-01 |
| **persona** | Decision maker |
| **product** | Unified Commerce |
| **user_intent** | What are VTEX's omnichannel capabilities? |
| **expected_doc_url** | https://help.vtex.com/en/docs/tracks/unified-commerce |
| **source** | Command input (user issue + target document URL) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | what are VTEX's omnichannel capabilities |
| familiar | VTEX unified commerce features |
| expert | VTEX unified commerce strategy |

**Array (query_external):**
```json
[
  { "query": "what are VTEX's omnichannel capabilities", "style": "naive" },
  { "query": "VTEX unified commerce features", "style": "familiar" },
  { "query": "VTEX unified commerce strategy", "style": "expert" }
]
```

### B — Internal search (Algolia / Proprietary API)

| style | query |
|-------|--------|
| naive | omnichannel capabilities |
| familiar | unified commerce |
| expert | unified commerce strategy |

**Array (query_internal):**
```json
[
  { "query": "omnichannel capabilities", "style": "naive" },
  { "query": "unified commerce", "style": "familiar" },
  { "query": "unified commerce strategy", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | vtex docs what are omnichannel capabilities |
| familiar | vtex unified commerce |
| expert | unified commerce |

**Array (query_mcp):**
```json
[
  { "query": "vtex docs what are omnichannel capabilities", "style": "naive" },
  { "query": "vtex unified commerce", "style": "familiar" },
  { "query": "unified commerce", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | what omnichannel features does VTEX offer |
| familiar | what is unified commerce in VTEX |
| expert | how does VTEX unified commerce work |

**Array (query_llm):**
```json
[
  { "query": "what omnichannel features does VTEX offer", "style": "naive" },
  { "query": "what is unified commerce in VTEX", "style": "familiar" },
  { "query": "how does VTEX unified commerce work", "style": "expert" }
]
```
