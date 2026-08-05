# GVPN August 2026 Convening — landing page promo

Promo material for the Global Violence Prevention Network virtual convening,
requested by Paty (NICJR) on 5 August 2026, for
[gvpn.howpreventionworks.com](https://gvpn.howpreventionworks.com/).

## Event details

- **What:** GVPN Virtual Convening
- **When:** Tuesday 25 August 2026, 8:30–10:00 am PDT / 4:30–6:00 pm BST
- **Registration:** <https://us06web.zoom.us/meeting/register/Xfp4JKCpSgmHtR26g8JlTg#/registration>
- **Partners:** NICJR · GLEPHA · Salzburg Global Seminar

## Contents

| File | Purpose |
| --- | --- |
| `announcement-section.html` | Two drop-in blocks: a slim top-of-page banner and a full announcement section with the flyer and registration button. Styles are scoped (`.gvpn-ac-` prefixes) so they will not clash with the site's existing CSS. |
| `assets/gvpn-flyer-aug-2026.png` | The convening flyer at full resolution (linked as the download). |
| `assets/gvpn-flyer-aug-2026-web.jpeg` | Web-optimised copy shown inline on the page. |

## How to publish

1. Open the landing page source (the Cloudflare Pages deployment behind
   `gvpn.howpreventionworks.com`).
2. Upload both flyer files alongside the page (keep the `assets/` path,
   or adjust the references in the snippet).
3. Paste **Block 1** from `announcement-section.html` immediately inside
   `<body>` so the registration call sits at the very top of the page.
4. Paste **Block 2** directly above the `#why` section (or wherever the
   announcement should sit). It carries the id `#convening`, so it can be
   linked from the nav as `<a href="#convening">August convening</a>`.
5. Redeploy.

The flyer is the original **"GVPN Flyer - 4.png"** from Paty's email of
5 August 2026, with a web-optimised JPEG derived from it for inline display.
