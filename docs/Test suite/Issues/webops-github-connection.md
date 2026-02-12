# Test Issue: WebOps GitHub Connection

## Issue Details

- **Issue ID:** webops-github-connection-01
- **Persona:** Developer
- **Product:** WebOps
- **User Intent:** Learn how to connect WebOps to GitHub for version control and deployment
- **Expected Doc URL:** TBD (target documentation for WebOps GitHub integration)
- **Source:** User query

## Query Arrays by Type

### A - External Search (Google)

Natural-language queries for external search engines.

| Style | Query |
|-------|-------|
| **naive** | how do I link my VTEX website deployment tool to github |
| **familiar** | connect WebOps to GitHub repository |
| **expert** | VTEX WebOps GitHub integration setup guide |

**JSON Array:**
```json
[
  {"query": "how do I link my VTEX website deployment tool to github", "style": "naive"},
  {"query": "connect WebOps to GitHub repository", "style": "familiar"},
  {"query": "VTEX WebOps GitHub integration setup guide", "style": "expert"}
]
```

### B - Internal Search (Algolia/Proprietary API)

Short, keyword-style queries for internal search systems.

| Style | Query |
|-------|-------|
| **naive** | github connect deployment |
| **familiar** | WebOps GitHub integration |
| **expert** | WebOps GitHub repository connection |

**JSON Array:**
```json
[
  {"query": "github connect deployment", "style": "naive"},
  {"query": "WebOps GitHub integration", "style": "familiar"},
  {"query": "WebOps GitHub repository connection", "style": "expert"}
]
```

### C - MCP (Proprietary Docs)

MCP-appropriate phrasing for how the MCP is invoked.

| Style | Query |
|-------|-------|
| **naive** | How do I set up GitHub with my WebOps account? |
| **familiar** | What are the steps to integrate GitHub with WebOps? |
| **expert** | How to configure GitHub repository connection in VTEX WebOps? |

**JSON Array:**
```json
[
  {"query": "How do I set up GitHub with my WebOps account?", "style": "naive"},
  {"query": "What are the steps to integrate GitHub with WebOps?", "style": "familiar"},
  {"query": "How to configure GitHub repository connection in VTEX WebOps?", "style": "expert"}
]
```

### D - External LLMs

User-style questions for ChatGPT, Claude, etc.

| Style | Query |
|-------|-------|
| **naive** | I'm using WebOps for my website and want to connect it to GitHub so I can manage my code there. How do I do that? |
| **familiar** | What's the process for connecting a WebOps project to a GitHub repository for version control? |
| **expert** | How do I configure GitHub integration in VTEX WebOps to enable repository-based deployments? |

**JSON Array:**
```json
[
  {"query": "I'm using WebOps for my website and want to connect it to GitHub so I can manage my code there. How do I do that?", "style": "naive"},
  {"query": "What's the process for connecting a WebOps project to a GitHub repository for version control?", "style": "familiar"},
  {"query": "How do I configure GitHub integration in VTEX WebOps to enable repository-based deployments?", "style": "expert"}
]
```

## Notes

- These queries test knowledge retrieval across different query styles and channels for WebOps-GitHub integration
- Expected documentation should cover authentication setup, repository linking, deployment configuration, and permissions
- Consider cross-referencing with WebOps CLI documentation and GitHub app installation guides
