# Issue: FastStore Variable Renaming

## Issue Details

- **Issue ID:** ISS-004
- **Persona:** Developer
- **Product:** FastStore
- **User Intent:** Learn how to rename variables in a FastStore project
- **Expected Document URL:** (To be determined based on test results)
- **Source:** User query - command execution

---

## Query Arrays by Type

### A. External Search (Google)

| Style | Query |
|-------|-------|
| **Naive** | how do I change variable names in my faststore site |
| **Familiar** | renaming variables faststore project |
| **Expert** | FastStore variable renaming configuration |

**Array format:**
```json
[
  {"query": "how do I change variable names in my faststore site", "style": "naive"},
  {"query": "renaming variables faststore project", "style": "familiar"},
  {"query": "FastStore variable renaming configuration", "style": "expert"}
]
```

---

### B. Internal Search (Algolia/Proprietary API)

| Style | Query |
|-------|-------|
| **Naive** | change variable names |
| **Familiar** | rename variables faststore |
| **Expert** | variable renaming faststore |

**Array format:**
```json
[
  {"query": "change variable names", "style": "naive"},
  {"query": "rename variables faststore", "style": "familiar"},
  {"query": "variable renaming faststore", "style": "expert"}
]
```

---

### C. MCP (Proprietary Docs)

| Style | Query |
|-------|-------|
| **Naive** | How can I change the names of variables in my FastStore project? |
| **Familiar** | What's the process for renaming variables in FastStore? |
| **Expert** | How do I rename FastStore project variables? |

**Array format:**
```json
[
  {"query": "How can I change the names of variables in my FastStore project?", "style": "naive"},
  {"query": "What's the process for renaming variables in FastStore?", "style": "familiar"},
  {"query": "How do I rename FastStore project variables?", "style": "expert"}
]
```

---

### D. External LLMs (ChatGPT, Claude, etc.)

| Style | Query |
|-------|-------|
| **Naive** | I need to change some variable names in my FastStore website, how do I do that? |
| **Familiar** | What's the best way to rename variables in a FastStore project? |
| **Expert** | How do I properly rename variables in FastStore while maintaining functionality? |

**Array format:**
```json
[
  {"query": "I need to change some variable names in my FastStore website, how do I do that?", "style": "naive"},
  {"query": "What's the best way to rename variables in a FastStore project?", "style": "familiar"},
  {"query": "How do I properly rename variables in FastStore while maintaining functionality?", "style": "expert"}
]
```

---

## Notes

- This issue focuses on variable renaming within FastStore projects, which may involve configuration files, component variables, or environment variables.
- Queries are designed to test whether different information retrieval systems can surface relevant documentation about FastStore's variable management and customization.
