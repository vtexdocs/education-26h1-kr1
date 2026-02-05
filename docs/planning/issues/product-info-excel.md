# Issue: Product information in Excel

| Field | Value |
|-------|--------|
| **issue_id** | product-excel-01 |
| **persona** | Store operator |
| **product** | Catalog / Products |
| **user_intent** | The user needs to obtain all product information in Excel. |
| **expected_doc_url** | TBD — add VTEX Help or Developer doc URL for catalog/product export to Excel |
| **source** | Command input (user issue) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | get all my products in a spreadsheet |
| familiar | VTEX export catalog to Excel |
| expert | export all product information to Excel VTEX |

**Array (query_external):**
```json
[
  { "query": "get all my products in a spreadsheet", "style": "naive" },
  { "query": "VTEX export catalog to Excel", "style": "familiar" },
  { "query": "export all product information to Excel VTEX", "style": "expert" }
]
```

### B — Internal search (Algolia / Proprietary API)

| style | query |
|-------|--------|
| naive | product export excel spreadsheet |
| familiar | catalog export Excel download |
| expert | export products Excel VTEX catalog |

**Array (query_internal):**
```json
[
  { "query": "product export excel spreadsheet", "style": "naive" },
  { "query": "catalog export Excel download", "style": "familiar" },
  { "query": "export products Excel VTEX catalog", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | how to get product data in excel |
| familiar | VTEX catalog export to spreadsheet |
| expert | export product information to Excel VTEX |

**Array (query_mcp):**
```json
[
  { "query": "how to get product data in excel", "style": "naive" },
  { "query": "VTEX catalog export to spreadsheet", "style": "familiar" },
  { "query": "export product information to Excel VTEX", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | How can I get a list of all my products in Excel? |
| familiar | How do I export my VTEX product catalog to Excel? |
| expert | What's the way to export all product information to Excel in VTEX? |

**Array (query_llm):**
```json
[
  { "query": "How can I get a list of all my products in Excel?", "style": "naive" },
  { "query": "How do I export my VTEX product catalog to Excel?", "style": "familiar" },
  { "query": "What's the way to export all product information to Excel in VTEX?", "style": "expert" }
]
```
