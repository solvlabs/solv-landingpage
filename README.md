
# SOLV Minimal Landing — GitHub/Vercel bundle

This folder is ready to commit at your repo root and deploy with Vercel (static site).

Files:
- `index.html` — uses CDN ESM imports (no build step)
- `Transparent Logo.svg` — logo source for the 3D neon tubes
- `vercel.json` — cache headers (HTML not cached, assets long-cached)

## Deploy via GitHub
1. Replace the files in your repo root with these.
2. Commit to a new branch and open a PR (or push to `main` if you prefer).
3. Vercel will auto-deploy the Preview; verify the hero (black→reveal, animated logo, modal video).
4. Merge to `main` → Production deploy.
5. Project Settings → Domains: ensure `solvrisk.xyz` is attached to THIS project; remove it from any old project.
