# franziska-faust-keramik.de · coming soon

The placeholder page `franziska-faust-keramik.de` serves until the Shopify store
launches. Plain static HTML on GitHub Pages: no build, no JavaScript, no cookies, no
third-party requests. The real site lives in `../franziska_faust_keramik`; its brand
tokens, display font, logo and photo are copied from there.

| File | What it is |
|---|---|
| `index.html` | The page. Its copy reuses the real site's hero strings. |
| `impressum.html`, `datenschutz.html` | The legal minimum for a business page hosted on GitHub. |
| `style.css` | One stylesheet for all three. |
| `CNAME` | Tells GitHub Pages which domain to serve. |
| `.nojekyll` | Skips Jekyll, so files are served exactly as they are. |
| `fonts/fraunces-variable.woff2` | Fraunces, SIL Open Font License 1.1 (<https://github.com/undercasetype/Fraunces>). |

## Preview locally

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploy

1. Create a **public** GitHub repo, push this folder to `main`.
2. Repo → *Settings* → *Pages* → *Deploy from a branch* → `main` / `(root)`. The custom
   domain fills itself in from `CNAME`.
3. INWX → *Nameserver / DNS* for `franziska-faust-keramik.de`. Remove any parking `A`/`AAAA`
   records on `@` and `www` first, then add:

   | Name | Type | Value |
   |---|---|---|
   | *(empty)* | A | `185.199.108.153` |
   | *(empty)* | A | `185.199.109.153` |
   | *(empty)* | A | `185.199.110.153` |
   | *(empty)* | A | `185.199.111.153` |
   | *(empty)* | AAAA | `2606:50c0:8000::153` |
   | *(empty)* | AAAA | `2606:50c0:8001::153` |
   | *(empty)* | AAAA | `2606:50c0:8002::153` |
   | *(empty)* | AAAA | `2606:50c0:8003::153` |
   | `www` | CNAME | `<github-user>.github.io` |

4. Back in *Settings* → *Pages*, tick **Enforce HTTPS** once GitHub has issued the
   certificate (minutes to an hour after DNS resolves).
5. GitHub → your account *Settings* → *Pages* → **Add a verified domain** and add the
   `TXT` record it shows at INWX. This stops any other repo from claiming the domain.

## At launch

Replace the records above with Shopify's (the real repo's `docs/phase-2.md` D1), then
remove the custom domain from this repo's Pages settings and archive the repo.
