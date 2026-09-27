# Image Proof

Find and fix product image problems in your Shopify store with Claude: products without images, variants showing the wrong colour, broken images left in descriptions after data imports, missing or useless alt text, and low-resolution photos.

Built by [Andrew Romanchenko](https://github.com/mssdef).

## What it does

- **image-audit** (read-only): scans your catalog and reports issues by severity, with a suggested fix for each and a full CSV of findings.
- **image-fix**: fixes alt text, assigns the right image to each variant, and helps move description images hosted outside Shopify into Shopify. Always shows a dry run first, works in small batches, never deletes anything, and gives you a rollback file.

## Get started

1. Add the Shopify connector from the Claude directory and connect your store.
2. Let Claude see your product photos: open **Settings → Capabilities**, and under **Code execution and file creation** add `cdn.shopify.com` to **Additional allowed domains**. Without this step the audit still works, but Claude can't look at the photos, so alt text is based on product titles only.
3. Start a new chat and ask, for example:

- "Audit the product images in my store."
- "Which variants show the wrong colour?"
- "Find broken images in my product descriptions."
- "Write alt text for all products that are missing it: show me first."
- "Check whether my product photos match their titles and variants."

## Checks

Missing images, broken image URLs, description images hosted outside Shopify or on `http://`, colour variants sharing one image, variants without an image, low resolution, inconsistent aspect ratio, single-image products, missing or filename-like alt text, and the same image reused across different products.

With `cdn.shopify.com` allowed, Claude also looks at the photos themselves: it flags photos that don't match the product title or variant, alt text that contradicts the photo, and writes alt text that describes what the photo actually shows.

## Data and privacy

- The plugin has no server and stores nothing. It sends no data to the author or anyone else.
- It reads and, only after you confirm, updates your store through the Shopify connector you connected.
- To view photos or check links, Claude downloads your product images from Shopify's CDN (`cdn.shopify.com`) inside Claude's own sandbox. Nothing is uploaded anywhere.

## Support

Issues and ideas: open an issue at [github.com/mssdef/image-proof](https://github.com/mssdef/image-proof/issues).

## License

MIT
