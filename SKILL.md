---
name: brand-guide-beaumont-hotel
description: "Official Beaumont Hotel visual brand standards. MUST use for any Beaumont Hotel design, visual explanation, HTML report, document, presentation, webpage, email design, social graphic, video graphic, PDF, or other branded artifact."
license: Proprietary Beaumont Hotel brand standards and assets; bundled theme code retains its stated license
compatibility: Works with Pi, Claude Code, Codex, and other Agent Skills-compatible harnesses.
metadata:
  brand: Beaumont Hotel
  version: "1.0"
  repository: https://github.com/Xammis/brand-guide-beaumont-hotel
---

# Beaumont Hotel Brand Guide v1.0

Use these standards for Beaumont Hotel, Beaumont Hotel • Spa • Events, Roosevelt's Tavern, 1886 Coffee, Spa at the Beaumont, and Events at the Beaumont artifacts.

## Source Priority

1. The April 2024 Beaumont brand book and official bundled assets govern identity, logo use, core colors, and typography.
2. The Beaumont WordPress child theme and deployed public frontend govern digital details that the book does not specify, including sizes, spacing, buttons, links, and responsive patterns.
3. When the checked-in child theme and deployed runtime differ, follow the official brand-book value for identity work and the deployed runtime for interactive behavior. The exceptions are called out below.

## Logos

Use only the official files in [`logos/`](logos/). Never redraw, trace, typeset, recolor, distort, crop, rotate, round, add effects to, or rearrange a logo. Preserve transparency and aspect ratio.

- **Primary general-use logo:** [`logos/digital/beaumont-hotel-spa-events/beaumont-hotel-spa-events-main-logo-digital-full-color-for-light-background-vert.png`](logos/digital/beaumont-hotel-spa-events/beaumont-hotel-spa-events-main-logo-digital-full-color-for-light-background-vert.png)
- **Horizontal web/header logo:** [`logos/digital/beaumont-hotel-spa-events/beaumont-hotel-spa-events-main-logo-digital-full-color-for-light-background-horiz.png`](logos/digital/beaumont-hotel-spa-events/beaumont-hotel-spa-events-main-logo-digital-full-color-for-light-background-horiz.png)
- **Beaumont Hotel-only logo:** [`logos/digital/beaumont-hotel/`](logos/digital/beaumont-hotel/)
- **Beaumont symbol:** [`logos/digital/beaumont-symbol/`](logos/digital/beaumont-symbol/)
- **Roosevelt's Tavern:** [`logos/digital/roosevelts-tavern/`](logos/digital/roosevelts-tavern/)
- **1886 Coffee:** [`logos/digital/1886-coffee/`](logos/digital/1886-coffee/)
- **Spa and Events sub-brands:** [`logos/digital/spa-and-events/`](logos/digital/spa-and-events/)
- **Print-ready PDF assets:** [`logos/print/`](logos/print/)
- **Complete provenance and checksums:** [`logos/manifest.json`](logos/manifest.json)

PNG is the recommended digital format. PDF is the recommended bundled print format.

### Logo Format and Clear Space

- The preferred Beaumont layout is vertical, full color, on Beaumont Tan (`#FCE5C8`).
- Use the horizontal format only when the vertical layout is impractical, such as a constrained website header.
- Maintain clear space equal to the height and width of the letter **B** in the Beaumont symbol.
- Maintain Roosevelt's Tavern clear space equal to the width of the letter **S** in its logo.
- Maintain 1886 Coffee clear space equal to the width of the coffee cup in its logo.
- Do not place a logo over a busy image or a background with insufficient contrast.
- Light and tan backgrounds are preferred. Use brown backgrounds sparingly.
- Dark backgrounds are exceptions. If unavoidable, use the supplied `for-dark-background` logo, never an improvised recolor.
- Never remove or reorder the Beaumont wordmark, symbol, tagline, or ornamentation.
- In the standard full-color mark, keep black ornamentation in Beaumont Black.

## Core Color Palette

The official brand palette is rustic, historic, and elevated.

### Primary colors

- Beaumont Red: `#B31F26`, RGB `179 31 38`, CMYK `21 100 97 12`
- Beaumont Tan: `#FCE5C8`, RGB `252 229 200`, CMYK `1 10 22 0`
- Beaumont Brown: `#7F5538`, RGB `127 85 56`, CMYK `38 62 80 29`
- Beaumont Black: `#000009`, RGB `0 0 9`, CMYK `7 70 63 86`

### Secondary fallback colors

Use these only when a primary color conflicts with a background or a medium neutral is genuinely needed.

- Lighter Red: `#D63444`, RGB `214 52 68`, CMYK `10 94 74 1`
- Medium Grey: `#6D6564`, RGB `109 101 100`, CMYK `56 53 51 20`
- Dark Brown: `#5B3B24`, RGB `91 59 36`, CMYK `44 67 83 50`
- Darker Tan: `#E8C7A7`, RGB `232 199 167`, CMYK `8 22 34 0`

### Digital implementation colors

- Primary background/Base: Beaumont Tan (`#FCE5C8`)
- Alternate background/Base Two: Darker Tan (`#E8C7A7`)
- Page/light texture base: White (`#FFFFFF`)
- Text/Contrast: Beaumont Black (`#000009`)
- Body text/Contrast Two: `#404040`
- Caption/Contrast Three: `#A4A4A4`
- Accent: Beaumont Red (`#B31F26`)
- Accent Three: Beaumont Brown (`#7F5538`)
- Accent Four: Dark Brown (`#5B3B24`)
- Light neutral utility: `#F0F0F0`
- Deep brown utility: `#371600`

**Accent Two discrepancy:** the brand book and checked-in child theme define Accent Two as `#D63444`. The deployed frontend currently compiles Accent Two and the solid-button hover as `#9A1B21`. Keep `#D63444` as the official secondary palette color. Use `#9A1B21` only as the established digital hover/dark-red interaction color.

Do not use unrelated default WordPress preset colors merely because WordPress exposes them.

## Typography

- Heading typeface: Libre Franklin Bold, `700`.
- Body typeface: Libre Franklin Regular, `400`.
- Button and strong interface type: Libre Franklin SemiBold, `600`.
- Headings may be uppercase when possible; this is the preferred brand-book treatment.
- Tertiary serif: Noto Serif Regular, used very sparingly. It is not bundled because neither the supplied font package nor the public site supplied a font file.
- 1886 Coffee display fonts: bundled Bebas Regular and Matchbook Regular. Restrict them to 1886 Coffee sub-brand work; do not replace Beaumont Hotel typography with them.
- Bundled web fonts: [`fonts/libre-franklin/`](fonts/libre-franklin/)
- Bundled coffee fonts: [`fonts/1886-coffee/`](fonts/1886-coffee/)

### Digital font sizes and line heights

These are the deployed WordPress scale:

- H1: `clamp(2.5rem, 2.5rem + ((1vw - .2rem) * 1.283), 3.27rem)`, line height `1.15`
- H2: `clamp(1.85rem, 1.85rem + ((1vw - .2rem) * 1.083), 2.5rem)`, line height `1.2`
- H3: `clamp(1.125rem, 1.125rem + ((1vw - .2rem) * .625), 1.5rem)`, line height `1.2`
- H4: `clamp(1.1rem, 1.1rem + ((1vw - .2rem) * .767), 1.5rem)`, line height `1.2`
- H5: `1.05rem`, line height `1.2`
- H6: `.9rem`, line height `1.2`
- Body: `1.05rem`, line height `1.55`
- Small text: `.9rem`
- Captions: `.8rem`
- Eyebrow/card title pattern: `clamp(1.125rem, 1.125rem + ((1vw - .2rem) * .208), 1.25rem)`, uppercase, approximately `2px` letter spacing

Reserve the oversized display clamps observed on campaign pages for genuine hero numerals or short feature statements. Do not use them for ordinary headings.

## Links

- Standard deployed link: Beaumont Red (`#B31F26`), no underline.
- Standard hover: Dark Red (`#9A1B21`), no underline.
- Navigation links: no underline at rest; underline on hover.
- Links placed on colored covers may inherit a verified high-contrast foreground.
- Always provide visible keyboard focus and never rely on color alone for a critical action.

## Buttons

### Solid button

- Background: Beaumont Red (`#B31F26`)
- Text: White (`#FFFFFF`)
- Font: Libre Franklin `600`, `1.05rem`
- Text: uppercase with `1px` letter spacing
- Radius: `.33rem`
- Base padding: `.6rem 1rem`
- Standard content-button horizontal padding: `40px`
- Hover: Dark Red (`#9A1B21`)
- Focus: Contrast Two (`#404040`) with Beaumont Tan text, Beaumont Black outline, and `2px` outline offset
- Active: Beaumont Black with Beaumont Tan text

### Outline button

- Border: `2px solid currentColor`
- Padding: `.45rem calc(1rem - 1px)`
- Established hover fill: Beaumont Brown (`#7F5538`)

At viewport widths of `430px` and below, button blocks and links become full width.

## Navigation

- Primary nav type: Libre Franklin `700`, `.9rem`, uppercase, `1px` letter spacing.
- Primary item gap: spacing preset 20, `min(1.5rem, 2vw)`.
- Main header surface: Tan etch background at `720px`, with a `5px` Beaumont Red bottom border and `25px` vertical padding.
- Desktop utility bar: Contrast Two background, small high-contrast text.
- Mobile menu: Beaumont Red overlay with White text.
- Footer nav: small text, normal `400` weight, vertical spacing preset 10 (`1rem`).

## Backgrounds and Surface Use

Use the official files in [`backgrounds/`](backgrounds/).

- Default page texture: [`etch-bg-white2.webp`](backgrounds/etch-bg-white2.webp), repeated at approximately `720px` tiles over White.
- Primary branded surface: [`etch-bg-tan2.webp`](backgrounds/etch-bg-tan2.webp), repeated at approximately `720px` tiles.
- Strong accent surface: [`etch-bg-red2.webp`](backgrounds/etch-bg-red2.webp).
- Dark exception surface: [`etch-bg-brown2.webp`](backgrounds/etch-bg-brown2.webp), used sparingly.
- Light and tan surfaces should dominate. Do not default to dark mode.
- Ensure all text and controls meet practical contrast requirements.
- Do not place a full-color light-background logo on a dark texture. Use its approved dark-background alternate.

## Layout, Spacing, and Padding

- Content width: `620px`
- Wide width: `1280px`
- Default block gap: `1.2rem`
- Spacing 10: `1rem`
- Spacing 20: `min(1.5rem, 2vw)`
- Spacing 30: `min(2.5rem, 3vw)`
- Spacing 40: `min(4rem, 5vw)`
- Spacing 50: `min(6.5rem, 8vw)`
- Spacing 60: `min(10.5rem, 13vw)`
- Spacing 70: `3.38rem`
- Spacing 80: `5.06rem`
- Root horizontal padding: spacing 50.
- Standard section padding pattern: generous spacing 40 or 50; `80px` top/bottom sections and `40px` internal separations recur on the public site.
- Standard card/image radius: approximately `1.25rem`; use `1rem` for secondary compact surfaces.
- Button radius remains smaller at `.33rem`.
- Use spacing and textured/color contrast before adding shadows. Avoid diffuse decorative shadows.
- Keep layouts responsive and free of horizontal overflow.

## Recurring Frontend Patterns

- Full-width textured sections contain a constrained or wide inner wrapper.
- White etch is the page canvas; tan etch anchors headers, footers, and warm content sections.
- Red sections are high-emphasis moments, not the dominant page background.
- Photo-led layouts use wide images, covers, two-column media/text blocks, and modest rounded corners.
- Section eyebrows and compact headings are uppercase with noticeable tracking.
- Alternating White, Tan, and occasional Red/Brown sections create hierarchy.
- Footer patterns use Tan texture, a `10px` Base Two top border, a vertical full-color logo, small navigation columns, and red social icons.

## Icons

Use the official arrow, phone, and location PNGs in [`icons/`](icons/). Variants are bundled in Red, Burgundy, White, Tan, and Black. The Burgundy icon files use their supplied `#77070C`; treat this as an asset-specific color, not an extension of the general palette. Do not recolor an icon when an approved variant exists.

## Visual Explainers and Generated Reports

- Read this guide fresh before every Beaumont visual pass.
- Read source content separately from any prior rendered report.
- Build each artifact from the Beaumont information architecture and these standards, not from a generic template.
- Preserve all facts, caveats, and meaning.
- Keep pages semantic, responsive, spacious, readable, and free of horizontal overflow.
- Use only bundled official logo assets.
- Verify contrast and focus states.
- Publish user-viewable HTML reports through the required verified Live Reports workflow.

## Detailed References

- [Frontend and WordPress evidence](references/frontend-and-wordpress.md)
- [CSS tokens and font-face starter](references/css-tokens.css)
- [Canonical public child-theme JSON](references/wordpress-child-theme.json)
- [Canonical public child-theme stylesheet](references/wordpress-child-style.css)
