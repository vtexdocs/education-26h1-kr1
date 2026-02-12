# Issue: Search and investigate audit events

| Field | Value |
|-------|--------|
| **issue_id** | audit-search-01 |
| **persona** | Store operator |
| **product** | Audit / Storage |
| **user_intent** | How to search and investigate audit events to track operations, authors, and timestamps in VTEX Admin. |
| **expected_doc_url** | https://help.vtex.com/pt/docs/tutorials/audit |
| **source** | Command input (target document URL) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | how to search audit events in vtex |
| familiar | vtex audit log search |
| expert | vtex audit events |

**Array (query_external):**
```json
[
  { "query": "how to search audit events in vtex", "style": "naive" },
  { "query": "vtex audit log search", "style": "familiar" },
  { "query": "vtex audit events", "style": "expert" }
]
```

### B — Internal search (Algolia / Proprietary API)

| style | query |
|-------|--------|
| naive | audit events search |
| familiar | audit log |
| expert | audit |

**Array (query_internal):**
```json
[
  { "query": "audit events search", "style": "naive" },
  { "query": "audit log", "style": "familiar" },
  { "query": "audit", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | vtex docs on audit events |
| familiar | vtex audit search |
| expert | audit |

**Array (query_mcp):**
```json
[
  { "query": "vtex docs on audit events", "style": "naive" },
  { "query": "vtex audit search", "style": "familiar" },
  { "query": "audit", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | how do i search audit events in vtex |
| familiar | how to find audit logs in vtex admin |
| expert | how to search audit events in vtex |

**Array (query_llm):**
```json
[
  { "query": "how do i search audit events in vtex", "style": "naive" },
  { "query": "how to find audit logs in vtex admin", "style": "familiar" },
  { "query": "how to search audit events in vtex", "style": "expert" }
]
```
