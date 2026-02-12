# Issue: How does VTEX support work

| Field | Value |
|-------|--------|
| **issue_id** | support-work-01 |
| **persona** | Decision maker |
| **product** | Support / Operational |
| **user_intent** | How does VTEX support work? |
| **expected_doc_url** | https://help.vtex.com/docs/tutorials/how-does-vtex-support-work |
| **source** | Command input (target document URL) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | how does VTEX support work |
| familiar | VTEX support system how to get help |
| expert | VTEX support plans ticket system |

**Array (query_external):**
```json
[
  { "query": "how does VTEX support work", "style": "naive" },
  { "query": "VTEX support system how to get help", "style": "familiar" },
  { "query": "VTEX support plans ticket system", "style": "expert" }
]
```

### B — Internal search (Algolia / Proprietary API)

| style | query |
|-------|--------|
| naive | support help |
| familiar | VTEX support ticket |
| expert | support plans ticket system |

**Array (query_internal):**
```json
[
  { "query": "support help", "style": "naive" },
  { "query": "VTEX support ticket", "style": "familiar" },
  { "query": "support plans ticket system", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | vtex docs how does support work |
| familiar | vtex support |
| expert | support work |

**Array (query_mcp):**
```json
[
  { "query": "vtex docs how does support work", "style": "naive" },
  { "query": "vtex support", "style": "familiar" },
  { "query": "support work", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | how do I get support from VTEX |
| familiar | how does VTEX support system work |
| expert | what are VTEX support plans and how do tickets work |

**Array (query_llm):**
```json
[
  { "query": "how do I get support from VTEX", "style": "naive" },
  { "query": "how does VTEX support system work", "style": "familiar" },
  { "query": "what are VTEX support plans and how do tickets work", "style": "expert" }
]
```
