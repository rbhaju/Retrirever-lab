# Retriever Lab — Website

Two static pages, ready to publish on GitHub Pages (free):

- **`index.html`** — the Retriever Lab studio homepage
- **`kepto.html`** — the Kepto product page

They link to each other already (the studio's "Learn more" → Kepto; Kepto's footer → studio).

---

## How to publish on GitHub Pages

1. Create a GitHub account (github.com) if you don't have one.
2. Create a new **public** repository. Name it `yourusername.github.io` for a root URL, or any name (e.g. `retriever-lab`) for a sub-path URL.
3. **Upload these files** (`index.html` and `kepto.html`) into the repo — keep the names exactly as they are. (`Add file → Upload files → drag both in → Commit`.)
4. Go to **Settings → Pages**. Under "Source," choose **Deploy from a branch**, branch **main**, folder **/(root)**. Save.
5. Wait ~1 minute, refresh, and your live URL appears at the top of that Pages screen.

## Connect your domain (retrieverlab.com)

1. In **Settings → Pages → Custom domain**, enter your domain and Save. This creates a `CNAME` file in the repo.
2. At your domain registrar, add DNS records (current values are on GitHub's "Managing a custom domain" docs page):
   - **A records** for the apex domain → GitHub Pages IPs:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - **CNAME record** for `www` → `yourusername.github.io`
3. Back in Settings → Pages, tick **Enforce HTTPS** once available.
4. DNS can take a few minutes to a few hours to propagate.

---

## Before you go live — replace the placeholders

In **both** files, search for and update:

- **`hello@retrieverlab.com`** → your real contact email (appears on both pages)
- **App Store buttons** (`href="#"`) → your real App Store link once Kepto is published
- On **kepto.html**: the "Coming soon" / "iOS 17" text → adjust to reality at launch
- Confirm the spelling **"Retriever"** matches your actual domain. (If your domain is literally "retriver" without the second e, change every "Retriever" to match — the site name and domain must agree.)

---

*Note: this is the marketing website only. The Kepto iOS app itself is published separately, through Xcode to the App Store — not via GitHub Pages.*
