# SOLV Minimal Landing (stable)

Static, zero-build landing page.

- Fade-in from black
- Electric border (animated) around the hero card
- Centered SOLV logo (uses `Transparent Logo.svg` from the repo root)
- Tagline + CTAs (mailto + modal YouTube)
- LinkedIn + X social links
- `vercel.json` sets **no-store** for `index.html` and long caching for assets

## Deploy (GitHub → Vercel)

1. Commit these files to your repo **root**:
   - `index.html`
   - `vercel.json`
   - `README.md`
   - (and keep your `Transparent Logo.svg` next to them)

2. Vercel auto-deploys.

3. If you previously used “Use existing Build Cache”, hit **Redeploy** once with it **unchecked** to ensure fresh HTML.

4. Point your domain to this project (remove it from any old project).

### Swapping the logo

Replace `Transparent Logo.svg` with your final asset **keeping the same filename**.
