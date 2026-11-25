# Adinkra Creative Studios — Official Website

Official site for **Adinkra Creative Studios**, a creative studio helping small
businesses stand out with professional social media designs, promotional
flyers, digital content, WhatsApp status designs and engaging strategies.

**Tagline:** *Local Roots. Global Reach.*

## Features

- Hero section featuring the Bese Saka emblem (used as the site icon).
- About the studio, services list, brand details, and contact section.
- Responsive, accessible design (WCAG-friendly contrast).
- Uses brand colours extracted from the studio's brand-launch assets:
  Gold `#DAAF37`, Black `#000000`, White `#FFFFFF`, Emerald `#0B3D2E`.
- Images from the `images/` folder are used as-is (logo, emblem, and source
  assets).

## Technology Stack

- **Type:** Static HTML5 website (no build step, no backend).
- **Styling:** CSS (custom properties) + Poppins (Google Fonts, display fallback).
- **Accessibility:** semantic HTML, visible focus states, ARIA labels, mobile-first.

## Project Structure

```
Adinkra_Creative_Studios/
├── index.html              # Main site page
├── styles/style.css        # Site stylesheet
├── favicon.ico             # Generated from images/Bese_Saka_Emblem_Transparent.png
├── images/                 # Source images (existing)
│   ├── Adinkra Creative Studios Logo.png
│   ├── Adinkra Creative Studios Marketing Flyer.png
│   ├── Adinkra Creative Studios Brand Launch.png
│   └── Bese_Saka_Emblem_Transparent.png
├── masteragent.md          # Engineering rules (existing)
├── README.md               # This file
└── ARCHITECTURE.md         # Architecture notes
```

## Running Locally

```powershell
# Serve the folder with a simple static server
python -m http.server 8000
```

Then open http://localhost:8000 in a browser.

## Testing

- Validate the HTML: the repo's validation script checks structure and asset links.
- Check contrast ratios of brand colours (≥ 4.5:1 on white where used as text).
- Test on mobile and desktop widths.

## Deployment

Deploy as a static site to any static hosting (Vercel, Netlify, GitHub Pages,
Cloudflare Pages). No environment variables or database required.

---

*Brand details (tagline, colours, typography, services) were extracted from
the studio's `images/` assets via OCR analysis. Ambiguous contact details
were flagged in the report — see the contact note on the site.*
