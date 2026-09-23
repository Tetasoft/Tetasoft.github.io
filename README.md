# Tetasoft website

Static one-page site for https://www.tetasoft.dk, hosted on GitHub Pages. No build step.

## Files
- `index.html` – the whole site (inline CSS, no external dependencies/cookies)
- `404.html` – not-found page
- `assets/` – logo (original + transparent PNG), header whale, favicon, apple-touch icon
- `robots.txt`, `sitemap.xml` – for search engines (update `lastmod` when content changes)
- `CNAME` – custom domain `www.tetasoft.dk`
- `.nojekyll` – serve files as-is

## Deploy
1. Create a GitHub repo (e.g. `tetasoft-web`) and push these files to `main`.
2. Repo → Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
3. Custom domain: `www.tetasoft.dk` (read from `CNAME`), then tick **Enforce HTTPS** once the certificate is issued.

## DNS (at the tetasoft.dk DNS provider)
| Type  | Name | Value |
|-------|------|-------|
| CNAME | www  | `<github-username>.github.io` |
| A     | @    | 185.199.108.153 |
| A     | @    | 185.199.109.153 |
| A     | @    | 185.199.110.153 |
| A     | @    | 185.199.111.153 |

The apex `A` records make `tetasoft.dk` redirect to `www.tetasoft.dk`.
Optionally verify the domain under GitHub → Settings → Pages (account level) to prevent takeover.

## After launch
Add https://www.tetasoft.dk in Google Search Console (DNS TXT verification) and submit `sitemap.xml`.
