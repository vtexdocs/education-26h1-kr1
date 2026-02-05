# Issue: Webstore (OAuth 2.0) — Custom login integration

| Field | Value |
|-------|--------|
| **issue_id** | webstore-oauth2-01 |
| **persona** | Developer |
| **product** | Login / Authentication / Webstore |
| **user_intent** | How to set up or integrate a custom OAuth identity provider for webstore login so customers can log in with an external IdP (e.g. company SSO, loyalty club). |
| **expected_doc_url** | https://developers.vtex.com/docs/guides/login-integration-guide-webstore-oauth2 |
| **source** | Target document (command input) |

---

## Queries by path

### A — External search (Google)

| style | query |
|-------|--------|
| naive | let customers log in with our company login instead of creating a new account |
| familiar | custom OAuth login for webstore VTEX identity provider |
| expert | VTEX webstore custom OAuth 2.0 integration guide |

**Array (query_external):**
```json
[
  { "query": "let customers log in with our company login instead of creating a new account", "style": "naive" },
  { "query": "custom OAuth login for webstore VTEX identity provider", "style": "familiar" },
  { "query": "VTEX webstore custom OAuth 2.0 integration guide", "style": "expert" }
]
```

### B — Internal search (Algolia/Proprietary API)

| style | query |
|-------|--------|
| naive | custom login external identity |
| familiar | OAuth webstore identity provider configure |
| expert | login integration guide webstore OAuth2 |

**Array (query_internal):**
```json
[
  { "query": "custom login external identity", "style": "naive" },
  { "query": "OAuth webstore identity provider configure", "style": "familiar" },
  { "query": "login integration guide webstore OAuth2", "style": "expert" }
]
```

### C — MCP (proprietary docs)

| style | query |
|-------|--------|
| naive | how can customers log in with our own login system |
| familiar | custom OAuth identity provider webstore setup |
| expert | webstore OAuth 2.0 login integration guide |

**Array (query_mcp):**
```json
[
  { "query": "how can customers log in with our own login system", "style": "naive" },
  { "query": "custom OAuth identity provider webstore setup", "style": "familiar" },
  { "query": "webstore OAuth 2.0 login integration guide", "style": "expert" }
]
```

### D — External LLMs

| style | query |
|-------|--------|
| naive | How do I let my store customers sign in with our existing user database? |
| familiar | How do I configure a custom OAuth provider for VTEX webstore login? |
| expert | How do I set up My Custom OAuth for the VTEX webstore following the OAuth2 flow? |

**Array (query_llm):**
```json
[
  { "query": "How do I let my store customers sign in with our existing user database?", "style": "naive" },
  { "query": "How do I configure a custom OAuth provider for VTEX webstore login?", "style": "familiar" },
  { "query": "How do I set up My Custom OAuth for the VTEX webstore following the OAuth2 flow?", "style": "expert" }
]
```
