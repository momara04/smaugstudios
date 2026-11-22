# Smaug Studios website

This is a static site for **Smaug Studios Publisher**. It has the homepage, Privacy Policy, Terms of Service and Data Deletion pages that TikTok, Google Cloud (YouTube) and Meta (Instagram) require for API app review.

| Page | Use it for |
|---|---|
| `/` (index.html) | App homepage / website URL |
| `/privacy.html` | Privacy Policy URL |
| `/terms.html` | Terms of Service URL |
| `/data-deletion.html` | Meta "User data deletion" → Data deletion instructions URL |

## Before you deploy

1. **Contact email:** the pages use `smaugstudios.official@gmail.com`. Reviewers may write to it, so keep an eye on that inbox.
2. **Platforms:** the pages name TikTok, YouTube and Instagram. If your third platform is different, edit the platform sections in `privacy.html`, `terms.html`, `data-deletion.html` and `index.html`.
3. **App name:** use **Smaug Studios Publisher** as the app name everywhere (the TikTok app, the Google OAuth consent screen and the Meta app). Reviewers compare the names.

## Deploy (GitHub Pages)

1. Push this repo to GitHub.
2. Go to **Settings → Pages → Deploy from branch → `main` / root**.
3. Recommended: add a custom domain (for example `smaugstudios.com`) under **Settings → Pages → Custom domain**, then enable **Enforce HTTPS**.

Netlify, Vercel and Cloudflare Pages also work. Point them at the repo root; there is no build step.

## Verify domain ownership

- **Google:** verify the domain in [Search Console](https://search.google.com/search-console). Then add it under **OAuth consent screen → Branding → Authorized domains**, and set the homepage, privacy and terms links to the URLs above.
- **TikTok:** in the developer portal, choose **URL properties → Verify** and use the URL-prefix method. Download the `tiktok*.txt` signature file, put it in the repo root, push, and click Verify.
- **Meta:** in **App settings → Basic**, set the Privacy Policy URL, Terms of Service URL and User data deletion URL (`/data-deletion.html`).
