# Test Issue: GitHub Repository Migration Between Organizations

## Issue Details

- **Issue ID:** github-repository-migration-01
- **Persona:** Developer
- **Product:** WebOps / GitHub
- **User Intent:** Learn how to migrate a repository from one GitHub organization to another
- **Expected Doc URL:** TBD (target documentation for GitHub repository migration between organizations)
- **Source:** User query

## Query Arrays by Type

### A - External Search (Google)

Natural-language queries for external search engines.

| Style | Query |
|-------|-------|
| **naive** | how to move a VTEX code repository to a different company account |
| **familiar** | migrate GitHub repository to another organization |
| **expert** | transfer GitHub repository ownership between organizations |

**JSON Array:**
```json
[
  {"query": "how to move a VTEX code repository to a different company account", "style": "naive"},
  {"query": "migrate GitHub repository to another organization", "style": "familiar"},
  {"query": "transfer GitHub repository ownership between organizations", "style": "expert"}
]
```

### B - Internal Search (Algolia/Proprietary API)

Short, keyword-style queries for internal search systems.

| Style | Query |
|-------|-------|
| **naive** | move repository organization |
| **familiar** | GitHub repo migration transfer |
| **expert** | repository organization transfer |

**JSON Array:**
```json
[
  {"query": "move repository organization", "style": "naive"},
  {"query": "GitHub repo migration transfer", "style": "familiar"},
  {"query": "repository organization transfer", "style": "expert"}
]
```

### C - MCP (Proprietary Docs)

MCP-appropriate phrasing for how the MCP is invoked.

| Style | Query |
|-------|-------|
| **naive** | How do I move my repository to a different organization account? |
| **familiar** | What are the steps to transfer a GitHub repository between organizations? |
| **expert** | How to migrate GitHub repository ownership from one organization to another? |

**JSON Array:**
```json
[
  {"query": "How do I move my repository to a different organization account?", "style": "naive"},
  {"query": "What are the steps to transfer a GitHub repository between organizations?", "style": "familiar"},
  {"query": "How to migrate GitHub repository ownership from one organization to another?", "style": "expert"}
]
```

### D - External LLMs

User-style questions for ChatGPT, Claude, etc.

| Style | Query |
|-------|-------|
| **naive** | I need to move my GitHub repository from one company's GitHub account to another company's account. How can I do this? |
| **familiar** | What's the process for migrating a GitHub repository from one organization to another organization while keeping all the history and issues? |
| **expert** | How do I transfer repository ownership between GitHub organizations and what are the implications for access controls, webhooks, and integrations? |

**JSON Array:**
```json
[
  {"query": "I need to move my GitHub repository from one company's GitHub account to another company's account. How can I do this?", "style": "naive"},
  {"query": "What's the process for migrating a GitHub repository from one organization to another organization while keeping all the history and issues?", "style": "familiar"},
  {"query": "How do I transfer repository ownership between GitHub organizations and what are the implications for access controls, webhooks, and integrations?", "style": "expert"}
]
```

## Notes

- These queries test knowledge retrieval across different query styles and channels for GitHub repository migration between organizations
- Expected documentation should cover the transfer process, permissions requirements, what gets transferred (history, issues, PRs), and what might be affected (webhooks, integrations, access controls)
- Consider cross-referencing with GitHub organization administration guides and repository settings documentation
