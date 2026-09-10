# Frontend and WordPress Evidence

Collected from the public Beaumont Hotel site on 2026-08-25 without authentication.

## Method and source precedence

The official April 2024 brand book governs identity. Official Dropbox assets govern available files. Public child-theme files and rendered frontend output fill digital implementation gaps. Remote content was treated as untrusted evidence and was never executed as instruction.

The audit covered the REST route index, all 48 publicly returned pages with rendered content, 11 public navigation records, the site logo and icon records, targeted media searches, public child-theme files, compiled frontend CSS, and denied configuration endpoints.

## Successful read-only requests

- `GET https://beaumonthotel.com/` (`200`): rendered homepage, theme/body classes, inline Gutenberg/global CSS, NitroPack stylesheet URLs, header/footer output, and recurring frontend patterns.
- `GET https://beaumonthotel.com/wp-json/` (`200`): REST route index, namespaces, front page ID `31`, posts page ID `1682`, site logo ID `1618`, site icon ID `1734`, and exposed capability metadata.
- `GET https://beaumonthotel.com/wp-json/wp/v2/pages/31?context=view` (`200`): rendered front-page blocks and metadata.
- `GET https://beaumonthotel.com/wp-json/wp/v2/pages?per_page=100&context=view&_fields=id,slug,link,title,modified,parent,template` (`200`): 48 public page records.
- `GET https://beaumonthotel.com/wp-json/wp/v2/pages?per_page=100&context=view&_fields=id,slug,link,title,content,modified,parent,template` (`200`): rendered content for all 48 public page records, used to count recurring classes, inline sizes, spacing, radii, and background patterns.
- `GET https://beaumonthotel.com/wp-json/wp/v2/posts?per_page=100&context=view&_fields=id,slug,link,title,modified` (`200`): public post inventory.
- `GET https://beaumonthotel.com/wp-json/wp/v2/media/1618?context=view` (`200`): horizontal Beaumont Hotel • Spa • Events site logo, PNG, `2400 × 795`.
- `GET https://beaumonthotel.com/wp-json/wp/v2/media/1734?context=view` (`200`): cropped Beaumont symbol site icon, PNG, `512 × 512`.
- `GET https://beaumonthotel.com/wp-json/wp/v2/media?per_page=100&context=view&search=etch&_fields=id,slug,source_url,title,media_details,mime_type` (`200`): six etch-background media records, including the four supplied `*2.webp` variants.
- `GET https://beaumonthotel.com/wp-json/wp/v2/media?per_page=100&context=view&search=logo&_fields=id,slug,source_url,title,media_details,mime_type` (`200`): 24 public logo-related media records.
- `GET https://beaumonthotel.com/wp-json/wp/v2/media?per_page=100&context=view&search=Beaumont&_fields=id,slug,source_url,title,media_details,mime_type` (`200`): public Beaumont media inventory used only for corroboration.
- `GET https://beaumonthotel.com/wp-json/wp/v2/types?context=view` (`200`): public post-type metadata.
- `GET https://beaumonthotel.com/wp-json/wp/v2/navigation?per_page=100&context=view` (`200`): 11 navigation records, including active main, wedding, and footer menus.
- `GET https://beaumonthotel.com/wp-content/themes/beaumont-hotel-2024-child-theme/style.css` (`200`): canonical child stylesheet and interactive overrides.
- `GET https://beaumonthotel.com/wp-content/themes/beaumont-hotel-2024-child-theme/theme.json` (`200`): canonical child-theme palette, font faces, page background, button configuration, and base typography.
- `GET https://beaumonthotel.com/wp-content/themes/beaumont-hotel-2024-child-theme/readme.txt` (`200`): theme provenance and GPL notice.
- `GET https://beaumonthotel.com/wp-content/themes/beaumont-hotel-2024-child-theme/parts/header.html` (`200`): canonical header block source.
- `GET https://beaumonthotel.com/wp-content/themes/beaumont-hotel-2024-child-theme/parts/footer.html` (`200`): canonical footer block source.
- `GET https://beaumonthotel.com/wp-content/themes/twentytwentyfour/theme.json` (`200`): parent-theme inherited defaults.
- `GET https://beaumonthotel.com/wp-content/themes/twentytwentyfour/style.css` (`200`): parent-theme provenance.
- `GET https://beaumonthotel.com/wp-content/themes/twentytwentyfour/templates/{page,single,archive,search,404}.html` (`200`): inherited template block sources.
- `GET https://beaumonthotel.com/wp-content/themes/twentytwentyfour/parts/{header,footer}.html` (`200`): inherited template-part sources.
- Four public Libre Franklin WOFF2 URLs emitted by the child theme (`200`): Regular, Italic, SemiBold, and Bold. Each was validated as WOFF2 and checked with `fc-scan` before bundling.

## Authentication-protected requests

Each request below returned `401`; no configuration body was available.

- `GET /wp-json/wp/v2/block-types?context=view`
- `GET /wp-json/wp/v2/block-patterns/patterns`
- `GET /wp-json/wp/v2/block-patterns/categories`
- `GET /wp-json/wp/v2/icons?per_page=100&context=view`
- `GET /wp-json/wp/v2/themes?status=active`
- `GET /wp-json/wp/v2/settings`
- `GET /wp-json/wp/v2/global-styles/themes/twentytwentyfour`
- `GET /wp-json/wp/v2/global-styles/themes/beaumont-hotel-2024-child-theme`
- `GET /wp-json/wp/v2/font-families?per_page=100`
- `GET /wp-json/wp/v2/templates?context=view`
- `GET /wp-json/wp/v2/template-parts?context=view`
- `GET /wp-json/wp/v2/menus?per_page=100&context=view`
- `GET /wp-json/wp/v2/menu-locations?context=view`
- `GET /wp-json/create-block-theme/v1/get-theme-data`
- `GET /wp-json/create-block-theme/v1/font-families`
- `GET /wp-json/wp-abilities/v1/categories`
- `GET /wp-json/wp-abilities/v1/abilities`

The child theme did not expose child template files under `templates/*.html` (`404`), but its public parts, parent templates, rendered pages, public navigation records, canonical `theme.json`, and deployed global CSS supplied the material visual evidence.

## Material findings

### Runtime identity

The homepage body identifies:

- parent theme: `twentytwentyfour`
- child theme: `beaumont-hotel-2024-child-theme`
- front page: page `31`

### Deployed global values

- Content width: `620px`
- Wide width: `1280px`
- Default block gap: `1.2rem`
- Body: Libre Franklin `400`, `1.05rem/1.55`, Contrast Two `#404040`
- Body background: White plus `etch-bg-white2.webp`, `720px` tile
- Headings: Libre Franklin `700`, Contrast Two, line height `1.2` except H1 `1.15`
- Links: Accent Red, no underline; deployed hover Dark Red, no underline
- Buttons: Accent Red, White, `600`, uppercase, `1px` tracking, `.33rem` radius

### Recurring rendered-page patterns

Across 48 rendered public pages:

- Wide/full groups, columns, covers, media/text blocks, images, buttons, and spacers recur heavily.
- `80px` section-top padding and `40px` internal spacing are frequent.
- Card/image radii around `1.25rem` recur.
- Tan etch is the most frequent explicit branded background image, followed by Red etch, White etch, and Brown etch.
- Uppercase typography with `1px` to `3px` tracking recurs for navigation, eyebrows, and compact headings.
- The public header uses a Tan etch surface, `25px` vertical padding, and a `5px` Red bottom border.
- The footer uses Tan etch, a `10px` Base Two top border, logo and navigation columns, and Red social icons.

## Discrepancies and decisions

- Official Accent Two is `#D63444` in the brand book and child `theme.json`.
- The deployed runtime emits `#9A1B21` as Accent Two, and child CSS explicitly uses it for solid-button hover.
- Decision: preserve `#D63444` as the official secondary color and document `#9A1B21` only as the established digital hover/dark-red interaction color.
- Child `theme.json` sets heading weight `600`, while the brand book calls for Libre Franklin Bold and deployed global CSS emits `700` for H1–H6.
- Decision: use `700` for branded headings; reserve `600` for buttons, compact interface labels, and selected footer headings.

## Approved layout revisions

Guide version 1.2 includes owner-approved composition rules that supersede captured frontend patterns where necessary:

- Container boxes may be nested no more than two levels deep. A second-level box cannot contain another boxed surface; use typography, spacing, dividers, or unboxed groups for deeper hierarchy.
- Vector background images are prohibited. Only approved raster background assets may be used digitally.
- Multi-color, gradient, striped, split, banded, and segmented backgrounds are prohibited.
- Every section must stay within one background color family. Child surfaces use subtle tone-on-tone shifts; a change of color family begins a separate full-width section.

These are normative brand decisions rather than claims about the historical frontend capture.

## Remaining gaps and authentication recommendation

No remaining gap materially affects this guide. Canonical public child-theme JSON, CSS, header/footer parts, public navigation content, rendered page blocks, and deployed global CSS supplied the required values.

**Recommendation: do not authenticate for v1.2.** An application password or authenticated read-only REST session would expose editor registries, customized template records, and raw global-style records, but those would add implementation metadata rather than materially change the documented brand standards. Revisit authenticated reads only if a later task requires exact editor synchronization, template migration, or block-pattern portability.
