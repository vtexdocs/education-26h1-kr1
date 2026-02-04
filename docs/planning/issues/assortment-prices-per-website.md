# Issue: Sell different product assortment/prices depending on the website

| Field | Value |
|-------|--------|
| **issue_id** | assortment-prices-website-01 |
| **persona** | Store operator |
| **product** | Catalog / Multi-store |
| **user_intent** | Sell different product assortment/prices depending on the website |
| **expected_doc_url** | https://help.vtex.com/en/guides/catalog-and-prices-per-sales-channel *(confirm exact URL)* |
| **source** | Command input |

---

## Queries by path

### A — Google Search

| style | query |
|-------|--------|
| naive | show different products and prices on each of my store sites |
| familiar | VTEX different catalog prices per website sales channel |
| expert | VTEX catalog and prices per sales channel configuration |

**Array (query_google):**
```json
[
  { "query": "show different products and prices on each of my store sites", "style": "naive" },
  { "query": "VTEX different catalog prices per website sales channel", "style": "familiar" },
  { "query": "VTEX catalog and prices per sales channel configuration", "style": "expert" }
]
```

### B — Portal search

| style | query |
|-------|--------|
| naive | different products prices per site |
| familiar | catalog prices sales channel website |
| expert | catalog prices per sales channel |

**Array (query_portal):**
```json
[
  { "query": "different products prices per site", "style": "naive" },
  { "query": "catalog prices sales channel website", "style": "familiar" },
  { "query": "catalog prices per sales channel", "style": "expert" }
]
```

### C — Proprietary search API

| style | query |
|-------|--------|
| naive | assortment prices per website |
| familiar | catalog price table sales channel |
| expert | catalog prices per sales channel VTEX |

**Array (query_api):**
```json
[
  { "query": "assortment prices per website", "style": "naive" },
  { "query": "catalog price table sales channel", "style": "familiar" },
  { "query": "catalog prices per sales channel VTEX", "style": "expert" }
]
```

### D — MCP / E — External LLMs (query_mcp_llm)

| style | query |
|-------|--------|
| naive | I have several store websites and want each to show different products and prices. How do I do that? |
| familiar | How do I configure different product assortment and prices per website in VTEX? |
| expert | How do I set up catalog and prices per sales channel so each website has its own assortment and pricing? |

**Array (query_mcp_llm):**
```json
[
  { "query": "I have several store websites and want each to show different products and prices. How do I do that?", "style": "naive" },
  { "query": "How do I configure different product assortment and prices per website in VTEX?", "style": "familiar" },
  { "query": "How do I set up catalog and prices per sales channel so each website has its own assortment and pricing?", "style": "expert" }
]
```
