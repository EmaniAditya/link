# link redirect (emaniaditya.github.io/link)

A tiny static site that redirects to a target URL specified in `.env.example`.

## How it works
- `index.html` fetches `.env.example` (or `.env` if present) and reads the line `URL=...`.
- The browser is redirected to that URL via `location.replace()`.
- `.nojekyll` ensures GitHub Pages serves dotfiles like `.env.example`.

## Usage
1. Edit `.env.example` and set your destination:
   ```env
   URL=https://your-destination.example.com
   ```
2. Push this repo to GitHub as `link` (public):
   - Repository name: `link`
   - Default branch: `main`
3. Enable GitHub Pages:
   - Settings → Pages → Build and deployment → Source: `Deploy from a branch`
   - Branch: `main` / folder: `/ (root)`
4. Visit: https://emaniaditya.github.io/link

## Local test
```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## Notes
- You can temporarily override with a query param: `?u=https://temp.example.com`.
- Mirrors the simplicity of the `resume` project (static Pages + instant redirect), but keeps the target configurable via `.env.example`.
