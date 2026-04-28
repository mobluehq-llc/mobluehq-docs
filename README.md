# mobluehq-docs

Public documentation for blueForge. Target: `docs.mobluehq.com` (Cloudflare Pages custom domain, attach in dashboard).

## Build

```bash
npm install
npm run build
```

## Deploy

```bash
export CLOUDFLARE_API_TOKEN=...  # or grep from MOBLUEHQ-workspace/.env
npx wrangler pages deploy dist --project-name mobluehq-docs --branch main
```

Create the project once if needed: `npx wrangler pages project create mobluehq-docs --production-branch main`
