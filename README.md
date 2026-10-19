# franziska-faust-keramik.de · coming soon

The placeholder page `franziska-faust-keramik.de` serves until the Shopify store
launches. Plain static HTML on GitHub Pages: no build, no JavaScript, no cookies, no
third-party requests. The real site lives in `../franziska_faust_keramik`; its brand
tokens, display font, logo and photo are copied from there.

| File                                 | What it is                                                                         |
| ------------------------------------ | ---------------------------------------------------------------------------------- |
| `index.html`                         | The page. Its copy reuses the real site's hero strings.                            |
| `impressum.html`, `datenschutz.html` | The legal minimum for a business page hosted on GitHub.                            |
| `style.css`                          | One stylesheet for all three.                                                      |
| `CNAME`                              | Tells GitHub Pages which domain to serve.                                          |
| `.nojekyll`                          | Skips Jekyll, so files are served exactly as they are.                             |
| `fonts/fraunces-variable.woff2`      | Fraunces, SIL Open Font License 1.1 (<https://github.com/undercasetype/Fraunces>). |

## Preview locally

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.
