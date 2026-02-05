# Issue: Integrate catalog from SAP

| Field | Value |
|-------|--------|
| **issue_id** | sap-catalog-01 |
| **persona** | Developer |
| **product** | Catalog / Backend integrations |
| **user_intent** | How to integrate product catalog from SAP (ERP) with VTEX. |
| **expected_doc_url** | https://newhelp.vtex.com/en/docs/tracks/backend-integrations |
| **source** | Command input (user issue) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | bring my product catalog from my business software into my online store |
| familiar | sync SAP product catalog to VTEX store |
| expert | integrate catalog from SAP ERP to VTEX |

**Array (query_external):**
```json
[
  { "query": "bring my product catalog from my business software into my online store", "style": "naive" },
  { "query": "sync SAP product catalog to VTEX store", "style": "familiar" },
  { "query": "integrate catalog from SAP ERP to VTEX", "style": "expert" }
]
```

### B — Internal search (Algolia/Proprietary API)

| style | query |
|-------|--------|
| naive | product catalog business software online store |
| familiar | SAP catalog VTEX sync integration |
| expert | integrate catalog SAP ERP VTEX backend |

**Array (query_internal):**
```json
[
  { "query": "product catalog business software online store", "style": "naive" },
  { "query": "SAP catalog VTEX sync integration", "style": "familiar" },
  { "query": "integrate catalog SAP ERP VTEX backend", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | how to get product catalog from my ERP into VTEX |
| familiar | SAP catalog integration with VTEX backend |
| expert | integrate catalog from SAP VTEX backend integrations |

**Array (query_mcp):**
```json
[
  { "query": "how to get product catalog from my ERP into VTEX", "style": "naive" },
  { "query": "SAP catalog integration with VTEX backend", "style": "familiar" },
  { "query": "integrate catalog from SAP VTEX backend integrations", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | How do I get my product catalog from SAP into my VTEX store? |
| familiar | How do I sync my SAP product catalog with VTEX? |
| expert | How do I integrate the catalog from SAP ERP to VTEX? |

**Array (query_llm):**
```json
[
  { "query": "How do I get my product catalog from SAP into my VTEX store?", "style": "naive" },
  { "query": "How do I sync my SAP product catalog with VTEX?", "style": "familiar" },
  { "query": "How do I integrate the catalog from SAP ERP to VTEX?", "style": "expert" }
]
```
