# Issue: Product not visible on website

| Field | Value |
|-------|--------|
| **issue_id** | product-not-visible-01 |
| **persona** | Store operator |
| **product** | Catalog / Products |
| **user_intent** | Why is the product not visible on the website / troubleshoot product visibility |
| **expected_doc_url** | https://help.vtex.com/faq/why-is-the-product-not-visible-on-the-website |
| **source** | Command input (target document URL) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | my products are not showing on my VTEX online store |
| familiar | VTEX product not visible on website |
| expert | why is the product not visible on the website VTEX |

**Array (query_external):**
```json
[
  { "query": "my products are not showing on my VTEX online store", "style": "naive" },
  { "query": "VTEX product not visible on website", "style": "familiar" },
  { "query": "why is the product not visible on the website VTEX", "style": "expert" }
]
```

### B — Internal search (Algolia/Proprietary API)

| style | query |
|-------|--------|
| naive | products not showing |
| familiar | product not visible website |
| expert | product not visible site FAQ |

**Array (query_internal):**
```json
[
  { "query": "products not showing", "style": "naive" },
  { "query": "product not visible website", "style": "familiar" },
  { "query": "product not visible site FAQ", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | why can't customers see my products |
| familiar | troubleshoot product not showing on storefront |
| expert | why is the product not visible on the website |

**Array (query_mcp):**
```json
[
  { "query": "why can't customers see my products", "style": "naive" },
  { "query": "troubleshoot product not showing on storefront", "style": "familiar" },
  { "query": "why is the product not visible on the website", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | Why can't my customers see the products I added to my store? |
| familiar | Why is my VTEX product not showing on the website? |
| expert | Why is the product not visible on the website in VTEX? |

**Array (query_llm):**
```json
[
  { "query": "Why can't my customers see the products I added to my store?", "style": "naive" },
  { "query": "Why is my VTEX product not showing on the website?", "style": "familiar" },
  { "query": "Why is the product not visible on the website in VTEX?", "style": "expert" }
]
```
