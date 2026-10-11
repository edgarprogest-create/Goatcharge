# Goat Spaces — Deploy folder

Drop this entire folder onto **Cloudflare Pages** (or any static host).
Tested for: Cloudflare Pages, Netlify, Vercel.

## What's inside

- `index.html` — the whole webapp, fully self-contained (no external requests at runtime)
- `_redirects` — tells the host to serve `index.html` for `/s/<qrcode>` URLs
- `_headers` — basic security hardening + cache-control

## Deploy via Cloudflare Pages (2 minutes)

1. Go to **dash.cloudflare.com → Workers & Pages → Create**
2. Choose **Pages → Upload assets**
3. Project name: `goatcharge` (or any name)
4. Drag this whole `deploy/` folder into the upload box
5. Click **Deploy site**

Cloudflare gives you a `*.pages.dev` URL immediately. The site works.

## Connect `goatcharge.com`

1. In the Pages project → **Custom domains** → **Set up a custom domain**
2. Enter `goatcharge.com` and `www.goatcharge.com`
3. Cloudflare auto-configures DNS (because the domain is in the same Cloudflare account)
4. SSL/TLS activates in ~30 seconds

That's it. The QR stickers can now point at `goatcharge.com/s/1644825217` etc.
