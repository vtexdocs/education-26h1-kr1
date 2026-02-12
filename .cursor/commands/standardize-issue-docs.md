# Standardize Issue Documentation

## Overview

Review and standardize all issue documentation files in `docs/Test suite/Issues/` to ensure consistency with the specification defined in `.cursor/commands/generate-knowledge-queries.md`.

## Tasks

### 1. Standardize Persona Values

- **Requirement:** The `persona` field must be exactly one of these three values (case-sensitive):
  - `'Developer'`
  - `'Store operator'` (lowercase 'o')
  - `'Decision maker'`

- **Actions:**
  - Review each issue document's `persona` field
  - If the value doesn't match exactly, map it to the correct value:
    - `'Store Operator'` → `'Store operator'`
    - `'Store Admin'` → `'Store operator'`
    - `'Technical Lead'`, `'Technical Lead / Store Owner'`, or similar → `'Developer'` (if technical/development focused) or `'Decision maker'` (if strategic/business focused)
    - Any other variations → determine the correct persona based on the user_intent and product fields
  - Update the persona field in the document

- **Persona determination criteria (from spec):**
  - **`'Store operator'`** — Admin panel tasks, catalog management, payment method setup, inventory management, order management, configuration tasks in the VTEX admin interface
  - **`'Developer'`** — Storefront customization, Backoffice integration, APIs, development tasks, code integration, technical implementation
  - **`'Decision maker'`** — Checking platform capabilities, security, compliance, business features, strategic evaluation, platform comparison

### 2. Ensure Unique Issue IDs

- **Requirement:** Every issue document must have a unique `issue_id` field

- **Actions:**
  - Scan all issue documents to collect existing `issue_id` values
  - For documents missing an `issue_id` or with `issue_id: TBD`:
    - Generate a new unique ID following the existing pattern
    - Pattern format: `{topic}-{category}-{number}` or `{topic}-{descriptor}-{number}`
    - Examples from existing issues:
      - `bitcoin-payment-01`
      - `payment-provider-01`
      - `product-not-visible-01`
    - Make IDs mnemonic (descriptive and easy to remember) based on the issue content
    - Ensure uniqueness across all documents
    - Use sequential numbering (01, 02, 03...) for similar topics
  - Update the `issue_id` field in each document

### 3. Ensure VTEX Mention in External Search Queries

- **Requirement:** All queries of type A (External search / Google) must explicitly mention 'VTEX' in the query text, including the naive style query.

- **Actions:**
  - For each issue document, review the "A — External search (Google)" section
  - Check all three queries (naive, familiar, expert) in the query_external array
  - If any query (especially naive) doesn't include 'VTEX' or 'vtex':
    - Add 'VTEX' to the query in a natural way
    - Examples:
      - ❌ "my products are not showing on my online store" → ✅ "my products are not showing on my VTEX online store" or "VTEX products not showing on website"
      - ❌ "How to migrate my online store without breaking it" → ✅ "How to migrate my VTEX online store without breaking it" or "VTEX store migration without breaking"
  - Update both the table and the JSON array to reflect the changes

## Output

For each issue document:

1. **Report changes made:**
   - List any persona corrections
   - List any issue_id additions/modifications
   - List any external search queries that were updated to include VTEX

2. **Update the document:**
   - Modify the markdown file with all corrections
   - Ensure the table format and JSON arrays are consistent
   - Preserve all other content and formatting

## Validation Checklist

After processing all documents, verify:

- [ ] All persona values are exactly one of: `'Developer'`, `'Store operator'`, `'Decision maker'`
- [ ] All documents have a unique `issue_id` field
- [ ] All issue_ids follow a consistent pattern and are mnemonic
- [ ] All type A (external search) queries include 'VTEX' or 'vtex' explicitly
- [ ] All JSON arrays match the table content
- [ ] No duplicate issue_ids exist across documents

## Files to Process

Process all `.md` files in `docs/Test suite/Issues/` directory.
