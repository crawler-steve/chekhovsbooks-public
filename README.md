# Chekhov's Gun Book Discovery — Phase 1.1 Prototype

This update adds your logo, loads a Clover-derived default book catalog, and prepares the project for metadata enrichment.

## What changed

- Added your logo (`logo.png`) to the interface in a subtle dark-elegant treatment.
- Imported **555 book-like inventory records** from `inventory-export-v2-16.xlsx`.
- Filtered out obvious non-book inventory categories such as apparel, 3D prints, bookmarks, tea, totes, stickers/pins, DCC merch, and blind-date placeholder items.
- Mapped Clover categories into starter app genres where possible.
- Preserved Clover item IDs, SKU/ISBN candidates, price, and stock quantity.
- Generated a staging catalog for enrichment:
  - `Chekhovs_Gun_Clover_Book_Inventory_Staging.xlsx`
  - `Chekhovs_Gun_Clover_Book_Inventory_Staging.csv`
- Added `METADATA_SOURCES.md` to guide the next enrichment phase.

## Current limitations

Most imported titles still need enrichment for:
- author names
- spice / door level / darkness
- detailed tropes
- content warnings / trigger notes
- ending / POV / pairings where useful

The prototype handles missing metadata gracefully and marks those titles as still being enriched.

## Files in this package

- `index.html` — updated prototype with your logo and Clover-derived default catalog.
- `logo.png` — your uploaded logo.
- `Chekhovs_Gun_Clover_Book_Inventory_Staging.xlsx` — working enrichment workbook.
- `Chekhovs_Gun_Clover_Book_Inventory_Staging.csv` — import-ready version of the current staging catalog.
- `Chekhovs_Gun_Book_Catalog_Template.xlsx` — original empty-ish working template.
- `Chekhovs_Gun_Book_Catalog_Template.csv` — original template CSV.
- `PROJECT_CONTEXT.md` — durable handoff context.
- `METADATA_SOURCES.md` — external-source strategy for enrichment.

## Recommended next phase

Phase 2 should focus on metadata enrichment and a bookseller/admin workflow before Clover API OAuth work.


## Added in this update
- `WEB_SOURCING_GUIDE.md` — notes on the web-sourced trope language, spice scale, darkness scale, and content warning wording used in the refined prototype.
- `logo-small.png` — smaller version of the provided logo asset for subtler UI use.
- `store-hero.jpg`, `store-ambience.jpg`, `store-detail.jpg`, `store-exterior.jpg` — local visual assets used to push the prototype toward a darker, more luxurious brand feel.
