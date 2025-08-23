# brand-assets

**Logos, wordmarks, color palettes, typography, and press-kit for CopperlineOS.**  
This repo is the single source of truth for visual identity. It includes ready-to-use PNG/SVG assets, social banners, app icons, and templates—plus clear usage guidelines.

> TL;DR: use the SVGs whenever possible, keep clear space, don’t stretch or recolor the logo, and prefer the **copper + graphite** palette for product UI.

---

## What’s inside

```
brand-assets/
├─ logos/
│  ├─ copperline-logomark.svg
│  ├─ copperline-wordmark.svg
│  ├─ copperline-lockup-horizontal.svg
│  ├─ copperline-lockup-stacked.svg
│  ├─ light/ ...png              # for dark backgrounds
│  └─ dark/  ...png              # for light backgrounds
├─ icons/
│  ├─ app-icons/                 # iOS/Android/maskable web icons
│  └─ favicons/                  # favicon.ico + webmanifest set
├─ social/
│  ├─ og-image.png               # 1200×630 (Open Graph)
│  ├─ twitter-card.png           # 1600×900
│  └─ header-banner.png          # 1500×500
├─ screenshots/                  # product screenshots (curated)
├─ templates/
│  ├─ slides/                    # PPTX/KEY/Google Slides link
│  ├─ letterhead/                # docs & invoice
│  └─ readme-cards/              # shields/OG images per repo
├─ source/                       # editable sources (Figma/Sketch/SVG parts)
├─ fonts/                        # optional: Inter (OFL) + JetBrains Mono (OFL)
├─ tools/
│  ├─ svgo.config.js
│  └─ build.sh                   # optimize & export PNGs
└─ README.md
```

> If a folder is empty in the initial commit, it’s a placeholder for upcoming assets.

---

## Quick links

- **Primary lockup (SVG):** `logos/copperline-lockup-horizontal.svg`  
- **Logomark only (SVG):** `logos/copperline-logomark.svg`  
- **Wordmark only (SVG):** `logos/copperline-wordmark.svg`  
- **Press kit (ZIP):** `press-kit/copperlineos-press-kit.zip` *(to be added)*

---

## Logo usage

### Clear space
Keep at least **1× the logomark’s width** as clear space around the logo.

### Minimum size
- **Logomark**: ≥ **16 px**.  
- **Lockup**: ≥ **120 px** width on screen, **25 mm** in print.

### Backgrounds
- Use **dark** logo on **light** backgrounds.  
- Use **light** logo on **dark** backgrounds (or on copper).  
- For photos, place on a low-contrast area or add a subtle shadow.

### Do / Don’t

**Do**
- Use the provided SVGs and export at target size.  
- Keep aspect ratio; align to pixel boundaries for small sizes.  
- Prefer **horizontal lockup** for headers/toolbars.

**Don’t**
- Recolor the wordmark/logomark outside the approved palette.  
- Skew, stretch, add glow/drop-shadows (unless part of a mock).  
- Combine with other logos without clear separation.  
- Put the logo on low-contrast busy backgrounds.

---

## Color palette

| Role | Name | Hex | Notes |
|---|---|---|---|
| **Primary** | Copper | `#B87333` | Brand accent; use sparingly for highlights, selections. |
| **Primary** | Graphite | `#131418` | Main text on light; backgrounds in dark UI. |
| **Neutral** | Slate | `#2A2E34` | Surfaces, cards, dark UI. |
| **Neutral** | Mist | `#F5F7FA` | Light backgrounds. |
| **Accent** | Teal | `#00C2B2` | Interactive accents, links, success. |
| **Accent** | Peach | `#FFB26B` | Secondary accent for charts/infographics. |
| **Signal** | Red | `#E8515D` | Errors/danger. |

### Accessible pairings (WCAG AA/AAA)

- `Graphite (#131418)` on `Mist (#F5F7FA)` → **AAA** for body text.  
- `Mist (#F5F7FA)` on `Graphite (#131418)` → **AAA**.  
- `Copper (#B87333)` on `Graphite (#131418)` → **AA** for large text/icons ≥ 18 px.  
- `Teal (#00C2B2)` on `Graphite` → **AA** for large text; use for buttons/badges.

When in doubt, check contrast at 4.5:1 for normal text and 3:1 for large text/icons.

---

## Typography

- **Primary UI:** **Inter** (SIL Open Font License).  
- **Monospace/code:** **JetBrains Mono** (SIL Open Font License).

Fonts may be included under `fonts/` with their respective `OFL.txt` files, or consumed from system packages. Suggested styles:

- Headings: `Inter SemiBold`  
- Body: `Inter Regular`  
- Code: `JetBrains Mono Regular`

---

## Iconography & favicons

### Web/app icons
- Provide **maskable** `512×512` PNG at `icons/app-icons/`.  
- Include `192×192`, `512×512`, and `1024×1024` marketing icon PNGs.

### Favicon set
Place in `icons/favicons/`:
- `favicon.ico` (16, 32, 48)  
- `favicon-32x32.png`, `favicon-16x16.png`  
- `apple-touch-icon.png` (180×180)  
- `site.webmanifest` with theme/background colors

Use the **copper** logomark on a **graphite** or **mist** background for favicons.

---

## Social / Open Graph

- **OG image:** `1200×630` (`social/og-image.png`)  
- **Twitter/Mastodon header:** `1500×500` (`social/header-banner.png`)  
- **YouTube banner:** `2560×1440` safe area centered

Include concise headlines, avoid fine detail near edges, keep contrast high.

---

## Screenshots

Curate in `screenshots/` with descriptive filenames:
```
screenshots/
  2025-08-23_copperd_timeline.png
  2025-08-23_compositor_layers.png
```

Guidelines:
- Use **native resolution**; don’t upscale.  
- Hide personal info; use demo assets.  
- Prefer light or dark mode consistently within a set.  
- Add simple captions in README.md when embedding.

---

## Templates

- **Slides**: base deck in PPTX + KEY.  
- **Docs**: letterhead and simple one-pager.  
- **README cards**: prebuilt OG images per repo (`templates/readme-cards/`).

Please export an **SVG** source in `source/` and optimized PNGs via `tools/build.sh`.

---

## Contributing new assets

1. **Source format**: SVG or Figma/Sketch exports. Avoid embedding text as outlines unless unavoidable.  
2. **Optimization**: run `tools/build.sh` (uses `svgo`) before committing PNGs.  
3. **Sizes**: for raster exports provide `1x`, `2x`, and `3x` where relevant.  
4. **Filenames**: `copperline-logo-dark@2x.png` etc.  
5. **Accessibility**: ensure OG images/banners meet contrast guidelines.

---

## License & trademark

- **Artwork (except logo/wordmark):** Creative Commons **BY 4.0**.  
- **Logo & wordmark:** © CopperlineOS Project. **Permitted use**: unmodified, to reference or link to the project, per these guidelines. **Not permitted**: implying endorsement, using in a product name, or altering the mark.  
- **Name “CopperlineOS”** and the logomark/wordmark are **trademarks** of the CopperlineOS maintainers.

For permissions, clarifications, or press inquiries: **brand@copperline.os** *(placeholder)*.

---

## Versioning

Every update to this repo should bump `brand.json` (to be added) with:
```json
{ "version": "0.1.0", "updated": "2025-08-23" }
```

Consumers (website/docs) can read this to invalidate caches.

---

## FAQ

**Can I recolor the logo to match my app?**  
No—stick to the approved palette. Use the logomark mono versions if color clashes.

**Can I combine CopperlineOS with my logo?**  
Yes, in comparison charts or “works with” sections—but separate clearly and don’t create a new lockup unless we approve it.

**Can I distribute the fonts?**  
Inter and JetBrains Mono are OFL; include the `OFL.txt` and follow their licenses.

---

## See also

- [`website`](https://github.com/CopperlineOS/website) — public site that consumes these assets  
- [`docs`](https://github.com/CopperlineOS/docs) — specs with embedded diagrams/screenshots
