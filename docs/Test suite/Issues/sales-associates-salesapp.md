# Issue: Manage sales associates in VTEX Sales App

| Field | Value |
|-------|--------|
| **issue_id** | sales-associates-salesapp-01 |
| **persona** | Store Admin |
| **product** | VTEX Sales App / Omnichannel |
| **user_intent** | How to manage sales associates in VTEX Sales App (add, edit, inactivate) |
| **expected_doc_url** | https://help.vtex.com/en/docs/tracks/managing-sales-associates-in-vtex-sales-app |
| **source** | Command input (target document URL) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | how to add store employees to my point of sale app |
| familiar | VTEX Sales App add sales associates |
| expert | managing sales associates in VTEX Sales App |

**Array (query_external):**
```json
[
  { "query": "how to add store employees to my point of sale app", "style": "naive" },
  { "query": "VTEX Sales App add sales associates", "style": "familiar" },
  { "query": "managing sales associates in VTEX Sales App", "style": "expert" }
]
```

### B — Internal search (Algolia/Proprietary API)

| style | query |
|-------|--------|
| naive | add employees store app |
| familiar | sales associates Sales App |
| expert | managing sales associates VTEX Sales App |

**Array (query_internal):**
```json
[
  { "query": "add employees store app", "style": "naive" },
  { "query": "sales associates Sales App", "style": "familiar" },
  { "query": "managing sales associates VTEX Sales App", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | how to register store staff in the sales app |
| familiar | add sales associate to VTEX Sales App |
| expert | managing sales associates in VTEX Sales App |

**Array (query_mcp):**
```json
[
  { "query": "how to register store staff in the sales app", "style": "naive" },
  { "query": "add sales associate to VTEX Sales App", "style": "familiar" },
  { "query": "managing sales associates in VTEX Sales App", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | How do I add my store employees to the sales app so they can use it? |
| familiar | How do I add and manage sales associates in VTEX Sales App? |
| expert | How do I manage sales associates in VTEX Sales App? |

**Array (query_llm):**
```json
[
  { "query": "How do I add my store employees to the sales app so they can use it?", "style": "naive" },
  { "query": "How do I add and manage sales associates in VTEX Sales App?", "style": "familiar" },
  { "query": "How do I manage sales associates in VTEX Sales App?", "style": "expert" }
]
```
