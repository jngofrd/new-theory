# New Theory — landing page

Single-page static site, deployed via GitHub Pages to `newtheory.world` (Porkbun domain).

## Before launch — replace placeholders

- `index.html`: swap `VIDEO_ID_HERE` in the YouTube `<iframe src>` for the real video ID.
- `index.html`: swap `hello@newtheory.world` in the Contact button's `mailto:` link for the real address.
- `assets/logo.png` is the placeholder wordmark — swap in the final logo file (keep the filename or update the `<img src>` in `index.html`).

## Local preview

Just open `index.html` in a browser, or serve the folder locally, e.g.:

```
npx serve .
```

## Deploy

Push to the `main` branch of the GitHub repo with Pages enabled (Settings → Pages → Source: `main` / root). The `CNAME` file tells GitHub Pages to serve this repo at `newtheory.world`.

DNS at Porkbun needs to point the domain at GitHub Pages:

- **Apex (`newtheory.world`)** — four `A` records pointing to:
  - 185.199.108.153
  - 185.199.109.153
  - 185.199.110.153
  - 185.199.111.153
- **`www`** (optional) — `CNAME` record pointing to `<github-username>.github.io`

Once DNS propagates, enable "Enforce HTTPS" in the repo's Pages settings.
