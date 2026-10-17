# Chekhov's Gun Book Discovery App — Project Context

_Last updated: 2026-10-17_

## Current status

The project is now at **Phase 1.1**.

### What Phase 1.1 added
- Integrated the store logo into the prototype UI in a subtle/elegant way.
- Loaded a default catalog derived from the provided Clover export workbook `inventory-export-v2-16.xlsx`.
- Imported **555 book-like records** after filtering out obvious non-book inventory categories.
- Added a Clover staging workbook/CSV to support metadata enrichment.
- Added a metadata-source strategy document.

## Inventory import notes

### Source workbook
- File: `inventory-export-v2-16.xlsx`
- Primary sheet used: `Items`

### Import logic
The current import excluded obvious non-book categories:
- Apparel
- 3D Prints
- Bookmark
- Accessories
- Tea
- Stickers and Pins
- Totes
- Hangover Cures
- DCC merch
- Blind Date placeholder products

Rows were treated as book-like if they had a likely ISBN/SKU or belonged to a book-oriented category.

### Result
- Imported records: **555**
- Records with blank/uncertain Clover category: **107**
- Records with inferred ISBN: **555**

## Data ownership model

- **Clover / future Clover API**: item ID, stock, price, active/hidden state.
- **Chekhov's Gun discovery metadata**: genre fit, tropes, spice, door level, darkness, trigger warnings, pairing, POV, editorial notes, discovery weight.
- **External enrichment sources**: author, description, covers, edition details, and suggested trope/warning clues.

## Why Clover API is still not the next step

Clover API work should remain a later phase because the recommendation quality still depends far more on metadata enrichment than on live OAuth sync. The current prototype already preserves Clover IDs so Phase 3 can plug into the same schema.

## Recommended next phase

### Phase 2 — Metadata enrichment + bookseller workflow
1. Auto-fill author/title metadata by ISBN.
2. Build a review queue for missing spice, darkness, warnings, and tropes.
3. Add a bookseller/admin mode with editing tools.
4. Package the app as a PWA once the customer and admin flows are approved.

### Phase 3 — Clover API read-only sync
- OAuth
- read inventory items
- read stock
- optional price sync
- item mapping verification

## Important UX guidance

When metadata is incomplete, the app should continue to show books but clearly indicate that the title is still being enriched. Missing trigger-warning data must not be mistaken for "safe" or "warning-free."

## Handoff prompt for the next chat

If a future chat needs to continue this project, start with:

> Continue the Chekhov's Gun Book Discovery App project from the attached PROJECT_CONTEXT.md and the current staging catalog. We are at Phase 1.1: logo integrated, Clover-derived inventory loaded, and the next step is metadata enrichment plus an admin workflow. Preserve the existing schema unless there is a strong reason to change it.
