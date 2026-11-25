# Architecture — Adinkra Creative Studios Website

## Overview

A **static website** for Adinkra Creative Studios. No build tooling, no
backend, no database — just HTML + CSS + a favicon, deployed as static assets.
This is the simplest architecture that meets the requirements: a marketing
presence for a small creative studio.

## Technology

- HTML5 + semantic markup.
- CSS with custom properties (design tokens from the brand assets).
- Poppins via Google Fonts (display-fallback).
- `favicon.ico` generated from `images/Bese_Saka_Emblem_Transparent.png` using Pillow.

## Data / Content Sources

All user-facing text derives from the studio's brand assets in `images/`
(extracted via OCR analysis):

- Site name: "Adinkra Creative Studios"
- Tagline: "Local Roots. Global Reach."
- About text: "We help small businesses stand out with professional social media designs, promotional flyers, and engaging content."
- Services: Social Media Starter Pack, Promotional Designs, Design Content Copy Marketing Strategy, Captions for Facebook or Instagram, WhatsApp Status Designs / Month, Monthly Content Calendar, Promotional Flyers, Professional (Headlines) Social Media Design.
- Brand details: Gold #DAAF37, Black #000000, White #FFFFFF, Emerald #0B3D2E, Poppins Bold typography, "Culturally Rooted" personality.
- Emblems/logos: `images/Adinkra Creative Studios Logo.png` (header logo),
  `images/Bese_Saka_Emblem_Transparent.png` (site icon / hero emblem).
- Low-confidence OCR strings (phone "0204975083", an email beginning "hello@adi…") were not committed to the site; they are flagged in the report.

## Site Icon

`Bese_Saka_Emblem_Transparent.png` is used both as the site icon (`favicon.ico`,
generated at 16–512px via Pillow) and as the hero emblem on `index.html`.

## Responsibilities

- `index.html` — full page structure and content (presentation layer only).
- `styles/style.css` — all styling, design tokens, responsive rules, focus styles.
- `favicon.ico` — site icon asset.
- `README.md`, `ARCHITECTURE.md` — documentation (Part 16 of masteragent.md).

## Future Extensibility

If the studio later requires more (e.g., a contact form backed by a mail API,
a CMS), this static structure is easy to extend without breaking changes.

## Verification Approach

- `tools/validate_site.py` (temporary, removed after use): parses `index.html`
  with `html.parser`, checks all referenced assets exist, and serves the site
  via a local HTTP server, fetching each asset URL to verify 200 responses.
