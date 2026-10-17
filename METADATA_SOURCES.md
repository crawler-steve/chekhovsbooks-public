# Metadata enrichment sources — Chekhov's Gun Discovery App

_Last updated: 2026-10-17_

## Recommended source priority

1. **Chekhov's Gun store curation (authoritative final layer)**  
   Final decisions about genre fit, tropes, darkness, spice, and customer-facing trigger language should live here. Community sites can suggest tags, but your store should be the final authority.

2. **Clover export / Clover API**  
   Best source for operational data: title as sold, price, current stock, item IDs, hidden/active state, and internal inventory mapping.

3. **ISBN-based metadata sources**  
   Best for filling in bibliographic basics like author name, publisher, pub date, cover image, and description. Good candidates for the next enrichment phase:
   - Google Books API
   - Open Library
   - Publisher APIs / feeds when available

4. **Publisher and distributor product pages**  
   Useful for official descriptions, series information, edition type, and cover images. This includes your Ingram workflow and publisher pages such as Penguin Random House where applicable.

5. **Romance / reader community reference sites (manual review recommended)**  
   Helpful for tropes, pairings, and steam-level context, but should not be treated as automatically authoritative without review.
   - Romance.io
   - The StoryGraph
   - Goodreads (manual reference only; not recommended as the core structured source)

6. **Content-warning specific sources (manual verification recommended)**  
   Helpful when building informed-consent metadata for customers.
   - Author content warning pages
   - Publisher/author front-matter or websites
   - Book Trigger Warnings–style community resources
   - Does the Dog Die–style structured warning sites where relevant

## Recommended data ownership model

- **Clover owns:** item identity in your POS, live stock, price, sellable state.
- **External metadata services own:** bibliographic fill-in such as author, description, cover, edition facts.
- **Chekhov's Gun owns:** genre fit, trope taxonomy, spice scale, darkness scale, trigger warning language, discovery weight, shelf notes, and any adjustments made for your audience.

## Best next move for enrichment

For the next phase, I recommend a semi-automated enrichment workflow:

1. Match each title by ISBN where available.
2. Auto-fill author, cover, publisher, and description.
3. Use Clover category to seed a starting genre/subgenre.
4. Create a review queue for titles missing spice, darkness, tropes, or content warnings.
5. Manually verify trigger warnings and any sensitive metadata before showing them to customers.

## Important caution

Trigger-warning data should never be presented as guaranteed complete. The app should use language such as:

> "Catalog warnings are provided to help customers browse more confidently, but they may not be exhaustive."
