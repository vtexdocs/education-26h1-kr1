# Issue: Product not appearing on site

| Field | Value |
|-------|--------|
| **issue_id** | product-visibility-01 |
| **persona** | Store Admin |
| **product** | Catalog / Products |
| **user_intent** | How to show my products on the site / troubleshoot product visibility |
| **expected_doc_url** | https://help.vtex.com/pt/faq/por-que-o-produto-nao-aparece-no-site |
| **source** | Command input (user issue + target document) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | my products are not showing up on my online store |
| familiar | VTEX product not appearing on storefront |
| expert | por que o produto não aparece no site VTEX |

**Array (query_external):**
```json
[
  { "query": "my products are not showing up on my online store", "style": "naive" },
  { "query": "VTEX product not appearing on storefront", "style": "familiar" },
  { "query": "por que o produto não aparece no site VTEX", "style": "expert" }
]
```

### B — Internal search (Algolia/Proprietary API)

| style | query |
|-------|--------|
| naive | products not showing site |
| familiar | product not appearing storefront |
| expert | produto não aparece site |

**Array (query_internal):**
```json
[
  { "query": "products not showing site", "style": "naive" },
  { "query": "product not appearing storefront", "style": "familiar" },
  { "query": "produto não aparece site", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | why can't customers see my products on the website |
| familiar | troubleshoot product visibility VTEX storefront |
| expert | product not appearing on site VTEX catalog |

**Array (query_mcp):**
```json
[
  { "query": "why can't customers see my products on the website", "style": "naive" },
  { "query": "troubleshoot product visibility VTEX storefront", "style": "familiar" },
  { "query": "product not appearing on site VTEX catalog", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | Why aren't my products showing up on my website? |
| familiar | My VTEX products are not appearing on the storefront, how do I fix this? |
| expert | Why is my product not appearing on my VTEX site? |

**Array (query_llm):**
```json
[
  { "query": "Why aren't my products showing up on my website?", "style": "naive" },
  { "query": "My VTEX products are not appearing on the storefront, how do I fix this?", "style": "familiar" },
  { "query": "Why is my product not appearing on my VTEX site?", "style": "expert" }
]
```
