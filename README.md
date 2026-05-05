# link redirect (emaniaditya.github.io/link)

A tiny static site that redirects to a target URL passed as a query parameter.

## How it works
- `index.html` reads the URL directly from the query string after the `?`.
- The browser is redirected to that URL via `location.replace()`.
- Example: `https://emaniaditya.github.io/link?https://example.com`

## Usage
1. Push this repo to GitHub as `link` (public):
   - Repository name: `link`
   - Default branch: `main`
2. Enable GitHub Pages:
   - Settings → Pages → Build and deployment → Source: `Deploy from a branch`
   - Branch: `main` / folder: `/ (root)`
3. Visit with your target URL: `https://emaniaditya.github.io/link?https://your-target-url.com`

## Local test
```bash
python3 -m http.server 8080
# then open http://localhost:8080?https://example.com
```
