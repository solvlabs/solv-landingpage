# SOLV Minimal Landing

Static, zero-build landing page.

- Black → reveal animation
- Three.js neon glass logo extruded from `Transparent Logo.svg`
- Tagline + CTAs (“Get in touch”, “Learn More” with inline YouTube modal)
- LinkedIn + X social links
- `vercel.json` sets `no-store` on HTML, and long caching for assets

## Local preview

Just open `index.html` directly. (No build step.)

## Deploy (GitHub → Vercel)

1. Commit these four files to the repo root:
   - `index.html`
   - `Transparent Logo.svg`
   - `vercel.json`
   - `README.md`
2. Vercel auto-deploys.
3. In the new deployment, click **Redeploy** and **uncheck** “Use existing Build Cache” once to ensure no stale HTML remains.
4. Make sure your domain (`solvrisk.xyz`) points to this project (and not the old one).

> To swap the logo, replace `Transparent Logo.svg` with your final asset while keeping the same filename.
