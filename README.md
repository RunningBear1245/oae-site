# Orlando Artisan Events Site

Static MVP site for the Orlando Artisan Events ecosystem.

## Cloudflare Pages

- Framework preset: `None`
- Build command: leave blank for Pages, or `npx wrangler deploy` for Workers static assets
- Build output directory: `public`
- Production branch: `main`

This repo includes `wrangler.jsonc` so Cloudflare Workers static asset deployments
serve only the `public/` directory. The production Worker is
`billowing-shadow-bc81`; do not rename it without also migrating its route. Do not
deploy from the repository root.

## Routes

- `/` - Orlando Artisan Events
- `/request/` - customer quote request form
- `/vendors/` - vendor interest form
- `/artists/` - approved artisan roster and founding feature slots
- `/parkday/` - Parkday Provisions
- `/chefs-table/` - Orlando Chefs Table
