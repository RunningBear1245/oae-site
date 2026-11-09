# Orlando Artisan Events Site

Static MVP site for the Orlando Artisan Events ecosystem.

## Cloudflare Pages

- Framework preset: `None`
- Build command: leave blank for Pages, or `npx wrangler deploy` for Workers static assets
- Build output directory: `public`
- Production branch: `main`
- Pages project: `orlando-artisan-events`
- Intended production alias: `https://orlando-artisan-events.pages.dev`

Manual Pages deployment:

```bash
npx wrangler@4.125.0 pages deploy public \
  --project-name orlando-artisan-events \
  --branch main
```

As of 2026-11-09, Cloudflare records the Pages deployment as successful but both
the production alias and immutable deployment hostname return Cloudflare 522. The
legacy Worker remains online at
`https://billowing-shadow-bc81.tannis07.workers.dev` while this account-level
Pages routing fault is unresolved.

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
