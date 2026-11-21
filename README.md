# reso.family

The website for Reso, a private home app for your household.

It's plain HTML and CSS with no build step, served by Cloudflare Pages. Every
push to `main` publishes.

| File | What it is |
|---|---|
| `index.html` | The holding page |
| `404.html` | The not-found page |
| `style.css` | Styles, using Reso's Grape color pack |
| `favicon.svg` | Res, used as the icon and on the pages |
| `.well-known/security.txt` | Where to report security issues ([RFC 9116](https://www.rfc-editor.org/rfc/rfc9116)) |
| `_headers` | Security headers for Cloudflare Pages |
| `fonts/` | Baloo 2 for headings, served from this site, with its license |
| `THIRD-PARTY-NOTICES.md` | Licenses for the Tabler icons and Baloo 2 |

**The site loads nothing from anywhere else**: no scripts, outside fonts,
analytics, cookies or embeds. `_headers` enforces that with a strict
Content-Security-Policy, so adding any of them means changing it on purpose.

**`security.txt` expires on 2027-11-20.** Renew it before then. A weekly
GitHub Action fails once it's within 60 days of expiring. GitHub turns off
scheduled workflows in a repo with no activity for 60 days, so keep a calendar
reminder too.

To preview it, open `index.html` in a browser, or run any static server here
(for example `python -m http.server`).

## Rights

All content, including the text, the name Reso and the art of Res, is
copyright Hats & Tatts, all rights reserved. Reso's app code is in a separate
repository under its own license.
