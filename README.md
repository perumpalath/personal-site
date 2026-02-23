# perumpalath.com

Personal website and resume for Avinash Perumpalath, live at [perumpalath.com](https://perumpalath.com).

## What's here

- `index.html` — the entire site, a single self-contained HTML file with embedded CSS. No framework, no build step.
- `headshot.jpg` — profile photo used in the sidebar and OG card.
- `og-image.png` — Open Graph preview image shown when the site is shared on LinkedIn, iMessage, Slack, etc.
- `og-card.html` — source template used to generate `og-image.png` via headless browser screenshot.
- `CNAME` — points the GitHub Pages deployment to the custom domain.

## Running locally

Open `index.html` directly in a browser. No server required.

## Regenerating the OG image

If you update `og-card.html`, regenerate the preview image with:

```bash
/Applications/Brave\ Browser.app/Contents/MacOS/Brave\ Browser \
  --headless=new \
  --screenshot="og-image.png" \
  --window-size=1200,630 \
  --hide-scrollbars \
  --force-device-scale-factor=1 \
  "file://$(pwd)/og-card.html"
```
