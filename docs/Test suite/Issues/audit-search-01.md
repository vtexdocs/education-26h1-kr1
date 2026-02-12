# Issue: Search and investigate audit events

| Field | Value |
|-------|--------|
| **issue_id** | audit-search-01 |
| **persona** | Decision maker |
| **product** | Audit / Storage |
| **user_intent** | Evaluate VTEX platform audit capabilities for security and compliance requirements. |
| **expected_doc_url** | https://help.vtex.com/pt/docs/tutorials/audit |
| **source** | Command input (target document URL) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | does vtex have audit logging capabilities |
| familiar | vtex audit trail security compliance |
| expert | vtex audit platform security features |

**Array (query_external):**
```json
[
  { "query": "does vtex have audit logging capabilities", "style": "naive" },
  { "query": "vtex audit trail security compliance", "style": "familiar" },
  { "query": "vtex audit platform security features", "style": "expert" }
]
```

### B — Internal search (Algolia / Proprietary API)

| style | query |
|-------|--------|
| naive | audit capabilities security |
| familiar | audit trail compliance |
| expert | audit |

**Array (query_internal):**
```json
[
  { "query": "audit capabilities security", "style": "naive" },
  { "query": "audit trail compliance", "style": "familiar" },
  { "query": "audit", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | vtex docs on audit capabilities and security |
| familiar | vtex audit trail features |
| expert | audit |

**Array (query_mcp):**
```json
[
  { "query": "vtex docs on audit capabilities and security", "style": "naive" },
  { "query": "vtex audit trail features", "style": "familiar" },
  { "query": "audit", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | what audit capabilities does vtex provide |
| familiar | how does vtex handle audit trails and compliance |
| expert | what audit and security features are available in vtex |

**Array (query_llm):**
```json
[
  { "query": "what audit capabilities does vtex provide", "style": "naive" },
  { "query": "how does vtex handle audit trails and compliance", "style": "familiar" },
  { "query": "what audit and security features are available in vtex", "style": "expert" }
]
```
