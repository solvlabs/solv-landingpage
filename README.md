# SOLV Landing Page (v3)

Static, zero-build landing page for **Solv** — *“Make autonomous AI insurable — with runtime evidence.”*  
Deployed on **Vercel** from this GitHub repo.

**Production:** `https://www.solvrisk.xyz` (and `https://solvrisk.xyz` if configured to redirect)  
**Tech:** Pure HTML/CSS/JS (no framework). Google Fonts (Plus Jakarta Sans). YouTube modal.

---

## Repo structure

```
/
├─ index.html                # The entire page
├─ Transparent Logo.svg      # Lion + SOLV wordmark (replace with same filename to swap)
├─ vercel.json               # Caching / headers for static hosting
└─ README.md                 # You are here
```

> ⚠️ This is a static site—**no build step**. If `index.html` is at the repo root, Vercel deploys it.

---

## Edit & preview

### Quick edits (GitHub UI)
1. Open `index.html` → **✏️ Edit** (or **Add file → Create new file**).
2. Choose **Create a new branch** (e.g., `lp-v4`) → **Propose changes** → **Create pull request**.
3. Vercel will attach a **Preview URL** to the PR. Review there before merging.

> Tip: Press **.** on GitHub to open the web VS Code editor (`github.dev`).

### Local preview (optional)
Just open `index.html` in your browser. No dev server required.

---

## Deploying to Production

- **Automatic:** Merging to `main` triggers a Production deployment on Vercel.
- **Promote / Roll back:** In Vercel → **Deployments**, use the **···** menu:
  - **Promote to Production** (promote any preview)
  - **Rollback** (promote an older production build)

> If an asset looks stale, **Redeploy** and **uncheck** “Use existing Build Cache” once.

---

## What to change (content quick guide)

All copy lives in `index.html`.

### Title & SEO
```html
<title>Solv | Insuring Autonomous AI</title>
<meta name="description" content="SOLV provides runtime observability, policy enforcement, and claims-grade evidence so insurers can price autonomous AI. Real-time, inference-speed proofs for safety and accountability.">
```

### Headline & subhead
```html
<h1>Make autonomous AI insurable — with runtime evidence.</h1>
<p class="subhead">Continuous observability, policy checks, and claims-grade logs — generated at inference time.</p>
```

### CTAs
```html
<a class="btn primary" href="mailto:patrick@solvrisk.xyz?...">Talk to Solv</a>
<a class="btn primary" id="learnMoreBtn" href="#">Why Solv?</a>
```
- Primary CTA is a **mailto**; edit address/subject/body as needed.
- “Why Solv?” opens the video modal.

### Video modal (YouTube)
```js
const YT_URL = "https://www.youtube.com/embed/-nls6846TPs?autoplay=1&rel=0&modestbranding=1&playsinline=1&vq=hd720";
```
- Replace the ID to change videos.
- `vq=hd720` hints 720p; YouTube/client may adjust based on bandwidth.

### Social links
Update the `href` values for LinkedIn/X in the `<footer>`.

### Logo swap
Replace **`Transparent Logo.svg`** with your final asset **using the same filename** (keeps code and caching simple).

---

## Visual controls (CSS variables)

Inside `<style>`:

```css
:root{
  /* Colors */
  --bg: #0e0f10;        /* page background */
  --copy: #e9edf0;      /* body text */
  --accent:  #c38d53;   /* bronze */
  --accent-2:#e0a357;   /* gold */

  /* Tunnel (3D frame) */
  --tunnel-frames: 24;  /* number of frames */
  --depth-step: 38px;   /* Z-depth per frame */
  --max-rotation: 18deg;/* mouse-tilt sensitivity */

  /* Warm hue sweep (oklch hue angles) */
  --hBase: 56;          /* yellow-gold start */
  --hStep: -1.15;       /* shifts toward copper/bronze per frame */
}
```
- Make the tunnel subtler by lowering `--tunnel-frames` or reducing glow in `.tunnel-frame`.
- Users with **Reduce Motion** are respected via `@media (prefers-reduced-motion: reduce)`.

---

## Accessibility & UX

- Video modal: **ESC** or **click outside** closes it; focus returns to the trigger.
- Keyboard focusable CTAs and social links.
- Reduced motion disables tilt/animation.

---

## Domains

- Primary: `www.solvrisk.xyz`.
- Configure apex `solvrisk.xyz` to **redirect** to `www` (or point directly) in Vercel → **Project → Settings → Domains**.

---

## Troubleshooting

- **Can’t see updates?** Hard refresh (⌘/Ctrl-Shift-R) or Incognito.
- **Autoplay blocked?** Some browsers block autoplay with sound; interaction typically resolves it.
- **Tunnel perf issues?** Reduce `--tunnel-frames` and `--max-rotation`; aim for ≤ ~60 total layers.

---

## Workflow hygiene

- Prefer **branch → PR → Preview** for all edits.
- Keep hero headline **10–14 words**. Subhead: one short sentence.
- Avoid heavy libs; keep the page instant.

---

## Credits

- Interactive tunnel inspired by modern CSS 3D frame techniques from @utilityblend on Codepen.io.  
- © **Solv**. All rights reserved. 2025.
