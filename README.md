# Kepto Site

Clean, organized static site for Retriever Labs and its product, Kepto.

## Structure

```
kepto-site/
├── index.html          Studio homepage
├── kepto.html          Kepto product page
├── css/
│   ├── base.css        Shared: design tokens, reset, fonts, top bar, background, reveal
│   ├── studio.css      Studio-page styles
│   └── kepto.css       Kepto-page styles
├── js/
│   └── reveal.js       Shared scroll-reveal behaviour
├── img/
│   ├── logo.png        Primary logo (black shield, gold dog) — used site-wide
│   ├── logo-gold-full.png   Alternate: gold logo + text on transparent
│   └── logo-badge.png       Alternate: gold logo + text on black badge
└── README.md
```

### Why it's split this way
- **Design tokens** (colours, fonts, spacing) live once in `css/base.css` under `:root`. Change a brand colour there and it updates everywhere.
- **Shared UI** (top bar, background, scroll-reveal) is in `base.css`, so both pages stay consistent automatically.
- **Page-specific styles** are isolated in `studio.css` / `kepto.css`.
- **Logo** is one file in `img/`. Swap `img/logo.png` to change the logo across the whole site.

## Editing tips
- Change brand colour: edit `--amber` (and friends) in `css/base.css`.
- Change the logo everywhere: replace `img/logo.png` (keep the filename).
- Add a new page: copy an HTML file, link `css/base.css` + a new page CSS, include `js/reveal.js`.

## Publish on GitHub Pages
1. Upload the **entire `kepto-site` folder contents** to your repo, keeping the folder structure (css/, js/, img/ must stay as subfolders).
2. Settings → Pages → Deploy from a branch → main → /(root) → Save.
3. Wait ~1 minute for the live URL.

## Custom domain (retrieverlab.online)
1. Settings → Pages → Custom domain → `retrieverlab.online` → Save.
2. At your registrar, add four A records (`@`) → 185.199.108.153, .109, .110, .111, and a CNAME (`www`) → `rbhaju.github.io`.
3. Tick **Enforce HTTPS** once the certificate is issued.

## Before launch — replace placeholders
- App Store button links (`href="#"`) → real App Store URL.
- "Coming soon" / "iOS 17 or later" → adjust at launch.
- Email is `hello@retrieverlab.online` — confirm it's a real, monitored address.

---
*The Kepto iOS app is published separately via Xcode to the App Store — not through this site.*
