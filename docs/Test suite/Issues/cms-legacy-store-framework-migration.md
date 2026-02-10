# Test Issue: CMS Legacy to Store Framework Migration - Production Impacts and Rollback

## Issue Details

- **Issue ID:** TBD
- **Persona:** Technical Lead / Store Owner
- **Product:** VTEX Store Framework / CMS
- **User Intent:** Understand the production environment impacts and rollback possibilities when migrating a store from CMS Legacy to Store Framework
- **Expected Document URL:** TBD (needs to be identified)
- **Source:** User inquiry about migration safety and risk management

## Query Type A: External Search (Google)

Natural-language queries for external search engines.

| Style | Query |
|-------|-------|
| **naive** | How to migrate my online store without breaking it and how to undo if something goes wrong |
| **familiar** | VTEX CMS Legacy to Store Framework migration production impact and rollback |
| **expert** | VTEX Store Framework migration production deployment strategy rollback procedures CMS Legacy |

**JSON Array:**
```json
[
  {"query": "How to migrate my online store without breaking it and how to undo if something goes wrong", "style": "naive"},
  {"query": "VTEX CMS Legacy to Store Framework migration production impact and rollback", "style": "familiar"},
  {"query": "VTEX Store Framework migration production deployment strategy rollback procedures CMS Legacy", "style": "expert"}
]
```

## Query Type B: Internal Search (Algolia/Proprietary API)

Short, keyword-style queries for internal search systems.

| Style | Query |
|-------|-------|
| **naive** | migrate store safely undo changes |
| **familiar** | Store Framework migration production rollback |
| **expert** | CMS Legacy Store Framework migration rollback |

**JSON Array:**
```json
[
  {"query": "migrate store safely undo changes", "style": "naive"},
  {"query": "Store Framework migration production rollback", "style": "familiar"},
  {"query": "CMS Legacy Store Framework migration rollback", "style": "expert"}
]
```

## Query Type C: MCP (Proprietary Docs)

MCP-appropriate phrasing for how the MCP is invoked.

| Style | Query |
|-------|-------|
| **naive** | How do I move my store to the new system without problems and what if I need to go back |
| **familiar** | What are the risks when migrating from CMS Legacy to Store Framework and can I rollback |
| **expert** | What are the production impacts and rollback possibilities when migrating from CMS Legacy to Store Framework |

**JSON Array:**
```json
[
  {"query": "How do I move my store to the new system without problems and what if I need to go back", "style": "naive"},
  {"query": "What are the risks when migrating from CMS Legacy to Store Framework and can I rollback", "style": "familiar"},
  {"query": "What are the production impacts and rollback possibilities when migrating from CMS Legacy to Store Framework", "style": "expert"}
]
```

## Query Type D: External LLMs

User-style questions for ChatGPT, Claude, etc.

| Style | Query |
|-------|-------|
| **naive** | I need to upgrade my VTEX store to a new version. What happens to my live site and can I reverse it if needed? |
| **familiar** | What are the production environment impacts when migrating a VTEX store from CMS Legacy to Store Framework? What are my rollback options? |
| **expert** | What are the production environment impacts and rollback possibilities in the process of migrating a VTEX store from CMS Legacy to Store Framework? |

**JSON Array:**
```json
[
  {"query": "I need to upgrade my VTEX store to a new version. What happens to my live site and can I reverse it if needed?", "style": "naive"},
  {"query": "What are the production environment impacts when migrating a VTEX store from CMS Legacy to Store Framework? What are my rollback options?", "style": "familiar"},
  {"query": "What are the production environment impacts and rollback possibilities in the process of migrating a VTEX store from CMS Legacy to Store Framework?", "style": "expert"}
]
```

## Document Context

This issue addresses critical concerns for store owners and technical teams planning a migration from CMS Legacy to Store Framework. Key topics to be covered in expected documentation:

### Production Impacts:
- Workspace-based development (no downtime during development)
- A/B testing capabilities for gradual rollout
- URL structure changes and SEO considerations
- Performance characteristics differences
- Custom functionality migration requirements
- Third-party integrations reconfiguration
- Analytics and tracking migration

### Rollback Possibilities:
- Pre-production rollback (workspace level - immediate)
- During A/B testing rollback (traffic routing - minutes)
- Post-migration rollback (binding switch - hours/days)
- Best practices for maintaining rollback readiness
- Risk mitigation strategies

### Migration Strategy:
- Isolated workspace development
- Comprehensive QA testing
- Gradual traffic rollout
- Monitoring and alerting setup
- Clear rollback procedures and decision criteria
