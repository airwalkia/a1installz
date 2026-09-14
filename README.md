# A1 Installz website

Static marketing site for **A1 Installz** (`a1installz.com`) — TV wall mounting and home installs serving Los Angeles, the San Gabriel Valley, and Orange County.

> Domain spelling: **a1installz.com** (with a **z**).

## Preview locally

From this directory:

```bash
python3 -m http.server 8080
```

Open http://127.0.0.1:8080/

## GitHub Pages + custom domain

1. Push this repo to GitHub (e.g. `airwalkia` account).
2. In the repo **Settings Pages**, set source to **GitHub Actions**.
3. The workflow `.github/workflows/pages.yml` publishes the static site from `main` using `actions/upload-pages-artifact` and `actions/deploy-pages`.
4. Custom domain: the `CNAME` file contains `a1installz.com`. In Pages settings, set the custom domain to `a1installz.com` and enable HTTPS once DNS propagates.

### DNS notes

Point the apex domain and `www` as follows (GitHub Pages):

**Apex (`a1installz.com`) — A records**

| Type | Host | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

**Optional IPv6 — AAAA records**

| Type | Host | Value |
|------|------|-------|
| AAAA | @ | 2606:50c0:8000::153 |
| AAAA | @ | 2606:50c0:8001::153 |
| AAAA | @ | 2606:50c0:8002::153 |
| AAAA | @ | 2606:50c0:8003::153 |

**www — CNAME**

| Type | Host | Value |
|------|------|-------|
| CNAME | www | airwalkia.github.io |

## Contact (site CTAs)

- Phone: (626) 290-6211
- Email: airwalkia@gmail.com
- Base: San Marino, CA 91108 (appointment service — not a retail storefront)

## Stack

- Static HTML / CSS / small vanilla JS
- No backend, no build step required
- Images under `images/` are web-compressed JPEG/WebP (not full-resolution originals)
