# GVPN August 2026 Convening — Landing Page Promo

Promo blocks for the Global Violence Prevention Network landing page
([gvpn.howpreventionworks.com](https://gvpn.howpreventionworks.com)), announcing the
virtual convening on **Tuesday 25 August 2026, 8:30–10:00 am PDT / 4:30–6:00 pm BST**.

Registration (free, via Zoom):
<https://us06web.zoom.us/meeting/register/Xfp4JKCpSgmHtR26g8JlTg#/registration>

## What is in this folder

| File | Purpose |
|---|---|
| `banner.html` | Slim announcement banner for the very top of the page, directly after `<body>` |
| `convening-section.html` | Full announcement section with the flyer and Zoom registration button (`id="convening"`, so `#convening` links work). References the flyer as a separate image file |
| `convening-section-embedded.html` | Same section with the flyer embedded as a data URI, for a single self-contained HTML file with no separate assets |
| `gvpn-convening-flyer.jpg` | Web-optimised copy of Paty's "GVPN Flyer - 4.png" (127 KB) |
| `promo.css` | Styles for both blocks. All classes are prefixed `gvpn-ac-` so nothing collides with existing page styles |
| `preview.html` | Standalone preview showing both blocks in position around a placeholder for the existing content — open in a browser to check before deploying |

## How to add to the landing page

1. Paste the contents of `promo.css` inside the page's existing `<style>` block
   (or link it as a stylesheet).
2. Paste `banner.html` immediately after the opening `<body>` tag, above the header.
3. Paste `convening-section.html` where the announcement should sit — suggested placement
   is directly after the hero or the "Why" section. If the landing page is deployed as a
   single HTML file with no separate assets, use `convening-section-embedded.html` instead
   and skip uploading the image.
4. If using `convening-section.html`, upload `gvpn-convening-flyer.jpg` alongside the page.
5. Redeploy to Cloudflare Pages as usual.

The banner and the section are independent — either can be used on its own.

## After the event

Remove the banner, and either remove the section or reword it as a "latest news" item
with the recording link once available.
