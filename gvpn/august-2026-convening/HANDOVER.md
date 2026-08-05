# Handover: Deploy August 2026 Convening Promo to the Live GVPN Site

**For**: a Claude session with Cloudflare access
**From**: session that prepared the promo assets (August 2026)
**Goal**: add the convening flyer and Zoom registration link to the live GVPN landing
page at https://gvpn.howpreventionworks.com

## Context

Paty Garcia Iruegas (paty@nicjr.org, NICJR) asked Stan to add the flyer and
registration link for the GVPN virtual convening to the landing page:

- **Event**: Global Violence Prevention Network Virtual Convening
- **When**: Tuesday 25 August 2026, 8:30–10:00 am PDT / 4:30–6:00 pm BST
- **Registration**: https://us06web.zoom.us/meeting/register/Xfp4JKCpSgmHtR26g8JlTg#/registration
- **Convened by**: NICJR with GLEPHA and Salzburg Global

All promo assets are finished, reviewed in a rendered preview, and sit in this folder
(`gvpn/august-2026-convening/` on branch `claude/gvpn-august-convening-promo-9fy1yz`
of SGilr/SGilr). See `README.md` here for the file-by-file breakdown.

## Hosting facts (verified)

- `gvpn.howpreventionworks.com` is served by **Cloudflare Pages** (Cloudflare-proxied;
  the sibling site `prism-r.howpreventionworks.com` is a CNAME to `prism-r.pages.dev`,
  so the Pages project for this site is most likely named **`gvpn`** → `gvpn.pages.dev`).
- The domain `howpreventionworks.com` is registered at IONOS; DNS is on Cloudflare.
- The landing page was authored by Stan as a single HTML page (shared with the GVPN
  group on 3 July 2026). It has at least a "Why" section (`#why` anchor exists).
- The originating session could NOT fetch the live page or reach Cloudflare, which is
  why deployment is handed over.

## What to do

1. Fetch the currently deployed landing page HTML (Cloudflare Pages project, likely
   `gvpn`; confirm via the account's Pages project list). Do not rebuild the page from
   scratch — edit what is deployed.
2. Insert the promo:
   - Contents of `promo.css` → into the page's `<style>` block (classes are all
     prefixed `gvpn-ac-`, no collisions expected).
   - `banner.html` → immediately after the opening `<body>` tag.
   - `convening-section.html` → after the hero or "Why" section, wherever it reads
     best against the existing flow. Upload `gvpn-convening-flyer.jpg` alongside the
     page. If the deployment is a single HTML file with no separate assets, use
     `convening-section-embedded.html` (flyer as data URI) and skip the image upload.
3. Deploy to the same Pages project so the URL stays gvpn.howpreventionworks.com.
4. Verify on the live URL: banner at top, section renders with flyer, both
   "Register" links resolve to the Zoom registration page, mobile layout wraps
   correctly (the section flexbox wraps below ~34rem width).
5. Report back with the live URL and a screenshot.

## Reference

- Rendered preview of the intended result:
  https://claude.ai/code/artifact/0b4569b8-eee9-4926-b72d-85465ce8aadc
- `preview.html` in this folder is the same thing, viewable locally.
- The flyer here is a web-optimised JPEG of Paty's original "GVPN Flyer - 4.png"
  (emailed 5 August 2026, thread "GVPN July 2nd Meeting Follow-Up"). If the full-res
  original is wanted, it is attached to that email.

## After the event (for whoever maintains the page)

Remove the banner; keep or reword the section as a news item with the recording link.
