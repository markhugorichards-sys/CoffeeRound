# Coffee Round

Staging preview of the Coffee Round storefront: premium ready-to-drink iced coffee.

**Status:** design and UX prototype. Not taking orders. Blocked from search indexing (`robots.txt`, `X-Robots-Tag`, meta robots).

## What's here

| Path | Purpose |
| --- | --- |
| `index.html` | The whole storefront: hash-routed pages, catalogue, basket, build-your-box, checkout form, consent, build-status page (`#/launch`) |
| `img/` | Web images cropped from the brand concept render (not final packaging photography) |
| `vercel.json` | Security, cache and no-index headers |
| `robots.txt` | Staging: disallows all crawlers |
| `docs/BUILD-SPEC.md` | The master build specification |

No build step. Open `index.html` locally or deploy the folder as a static site.

## Production plan: Shopify

This repo is the design reference. The live store will run on Shopify:

1. Port the design into a Shopify theme (Online Store 2.0, sections per homepage block). Colour and type tokens are the `:root` block at the top of `index.html`.
2. Load the six products from the `P` catalogue array. Fields that are `null` (volume, ingredients, allergens, nutrition, caffeine, GTIN) become product metafields and must be filled from the approved specification before any product goes active.
3. Shopify handles checkout, payments, VAT, shipping, order emails, accounts and the Google Merchant Center feed.
4. Real server-rendered URLs (`/products/vanilla-iced-latte`) replace the hash routes here, giving proper SEO and structured data.

## Removed from the mockup pending evidence

"Real ingredients", "No artificial flavours", "Natural energy", "Plant-based options", "Fully recyclable", "A greener choice", and all star ratings and review counts.
