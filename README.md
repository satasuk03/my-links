# my-links

Personal link-in-bio page for [@thezezelab](https://x.com/thezezelab).

Static site, no build step. Deploys on Cloudflare Pages.

## Files

- `index.html` — the page
- `profile.webp` — 512×512 avatar (also used as OG image / apple-touch-icon)
- `profile-192.webp` — smaller variant
- `_headers` — Cloudflare Pages cache headers

## Local preview

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy on Cloudflare Pages

1. Push this repo to GitHub.
2. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
3. Pick this repo. Build settings:
   - Framework preset: **None**
   - Build command: *(empty)*
   - Build output directory: `/`
4. Deploy. Then add a custom domain in **Custom domains** if needed.

Or via Wrangler CLI:

```sh
npx wrangler pages deploy . --project-name=my-links
```
