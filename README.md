# SOLV Minimal Landing — Clean bundle

This folder is ready to commit to **GitHub** and deploy on **Vercel** (static site, no build step).

## Files
- `index.html` — CDN ESM imports (no build). Contains the neon 3D logo hero and modal video.
- `Transparent Logo.svg` — your logo used to draw the neon tubes.
- `vercel.json` — HTTP headers to avoid `index.html` being cached while caching assets long-term.

## Deploy (GitHub + Vercel)
1. Create a new empty repo **or** delete existing files in the current repo.
2. Upload the three files in this folder to the repo root (not inside a subfolder).
3. In Vercel Project Settings → **Build & Output Settings**:
   - Framework Preset: **Other**
   - Build Command: _empty_
   - Output Directory: `.`
   - Root Directory: _empty_ (repo root)
4. Redeploy and **uncheck “Use existing Build Cache.”**

## Verify
- View Source and ensure the first line includes `<!-- BUILD: neon-hero`.
- Check that `/Transparent%20Logo.svg` loads directly.
