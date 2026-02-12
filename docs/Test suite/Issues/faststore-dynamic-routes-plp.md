# Issue: FastStore Dynamic Routes for PLPs

## Issue Details

| Field | Value |
|-------|-------|
| **Issue ID** | faststore-dynamic-routes-plp-01 |
| **Persona** | Developer |
| **Product** | FastStore |
| **User Intent** | How to use dynamic routes for PLPs (Product Listing Pages) in a FastStore website |
| **Expected Doc URL** | _To be determined based on VTEX FastStore documentation_ |
| **Source** | User query |

---

## Generated Queries

### A. External Search (Google)

Natural-language queries for organic web search:

| Style | Query |
|-------|-------|
| **Naive** | how to make product category pages load different URLs in VTEX FastStore |
| **Familiar** | FastStore product listing page routing configuration |
| **Expert** | how to implement dynamic routes for PLPs in FastStore |

**JSON format:**
```json
[
  {"query":"how to make product category pages load different URLs in VTEX FastStore","style":"naive"},
  {"query":"FastStore product listing page routing configuration","style":"familiar"},
  {"query":"how to implement dynamic routes for PLPs in FastStore","style":"expert"}
]
```

---

### B. Internal Search (Algolia/Proprietary API)

Keyword-style queries for portal and API search:

| Style | Query |
|-------|-------|
| **Naive** | FastStore category page URL structure |
| **Familiar** | FastStore PLP routing |
| **Expert** | FastStore dynamic routes product listing pages |

**JSON format:**
```json
[
  {"query":"FastStore category page URL structure","style":"naive"},
  {"query":"FastStore PLP routing","style":"familiar"},
  {"query":"FastStore dynamic routes product listing pages","style":"expert"}
]
```

---

### C. MCP (Proprietary Docs)

MCP-appropriate phrasing for agent invocation:

| Style | Query |
|-------|-------|
| **Naive** | How do I set up different URLs for product category pages in FastStore? |
| **Familiar** | Configure routing for product listing pages in FastStore |
| **Expert** | Implement dynamic routes for PLPs in FastStore project |

**JSON format:**
```json
[
  {"query":"How do I set up different URLs for product category pages in FastStore?","style":"naive"},
  {"query":"Configure routing for product listing pages in FastStore","style":"familiar"},
  {"query":"Implement dynamic routes for PLPs in FastStore project","style":"expert"}
]
```

---

### D. External LLMs

User-style questions for ChatGPT, Claude, etc.:

| Style | Query |
|-------|-------|
| **Naive** | I'm using FastStore and need to create custom URLs for my product category pages. How do I do this? |
| **Familiar** | What's the best way to set up dynamic routing for product listing pages in a VTEX FastStore project? |
| **Expert** | How can I implement dynamic routes for PLPs in FastStore following VTEX best practices? |

**JSON format:**
```json
[
  {"query":"I'm using FastStore and need to create custom URLs for my product category pages. How do I do this?","style":"naive"},
  {"query":"What's the best way to set up dynamic routing for product listing pages in a VTEX FastStore project?","style":"familiar"},
  {"query":"How can I implement dynamic routes for PLPs in FastStore following VTEX best practices?","style":"expert"}
]
```

---

## Notes

- All four query types (A, B, C, D) have been generated with exactly 3 queries each (naive, familiar, expert)
- Query wording varies by type per §2 of Planning phase 1 (tests).md
- Expected doc URL needs to be identified from VTEX FastStore documentation
- Ready to be added to test suite spreadsheet
