# CLAUDE.md

Context for Claude (or any AI coding assistant) working on this project.

## Project

One-page marketing website for **Fern & Ember Coffee**, a specialty coffee shop.
Audience: students and young professionals looking for a place to study, work or grab coffee.

## Architecture

- **Single file:** everything is in `index.html` — HTML, a `<style>` block in `<head>`, and a `<script>` block before `</body>`.
- **No build step, no frameworks, no dependencies.** Keep it that way unless explicitly asked.
- Only external resource: Google Fonts (Manrope for headings, Inter for body text).
- Hosted as a static site (Netlify). The publish directory is the repo root.

## Page sections (in order)

| Section | Selector / id | Notes |
|---|---|---|
| Header + nav | `header`, `.nav-links` | Sticky; hamburger menu below 720px |
| Hero | `.hero` | Headline, "Visit Us" button, perks, café picture |
| Menu | `#menu` | 6 `.menu-item` cards with picture, name, price, description |
| About | `#about` | Story text, picture, 4 `.value` tiles |
| Hours + Location | `#visit` | Dark green section; hours list + map card |
| Contact | `#contact` | Contact list + form |
| Footer | `footer` | Copyright and links |

## Design system

Colors are CSS variables in `:root`. Always use the variables rather than new hex values:

- `--green` `#1f3d2f` — primary (buttons, headings)
- `--green-soft` `#2f5a45` — hover states, accents
- `--beige` `#f3ece0` — alternate section background
- `--beige-dark` `#e6dac6` — picture backgrounds
- `--cream` `#fbf8f3` — page background
- `--text` `#22261f`, `--muted` `#6b6a62`, `--line` `#e3dccf`
- Accent brown `#b07d4f` (logo ampersand, small details)

Style: minimal, warm, lots of white space, rounded corners (`--radius: 14px`, larger images at 24px), pill-shaped buttons.

## Pictures

Each image sits in a `.pic` wrapper containing:
1. An inline `<svg>` illustration (always visible fallback), and
2. An Unsplash `<img>` on top with `onerror="this.remove()"`, so the illustration shows if the photo can't load.

When adding a new picture, follow this same pattern. Keep illustrations flat and in the palette above.

## Responsive breakpoints

- `900px`: two-column grids collapse to one column; menu grid becomes 2 columns
- `720px`: hamburger menu, reduced section padding
- `560px`: menu grid and value tiles become 1 column

Always check changes at phone width (~390px) with no horizontal scrolling.

## JavaScript

Vanilla JS only, kept minimal:
- Mobile menu toggle (`.menu-toggle` / `.nav-links.open`)
- Highlights today's row in `#hours` using `data-day` (0 = Sunday)
- Demo contact form handler (shows a thank-you message; not yet connected to a backend)

## Content rules

- Realistic copy, never lorem ipsum.
- Friendly, concise tone aimed at students and young professionals.
- Prices in USD with two decimals (e.g. `$4.50`).

## Known placeholders / to do

- Sample business details (address, phone, email, Instagram) need replacing with real ones
- `.map-placeholder` should become a Google Maps embed iframe
- Contact form needs a backend (Netlify Forms: add `data-netlify="true"` and remove the `preventDefault` demo handler)

## Working agreements

- Make focused edits; don't rewrite the whole file for small changes.
- Preserve accessibility: `alt` text on images, `aria-label` on illustrations and the menu button, semantic sections.
- Test in a browser after changes, on both desktop and mobile widths.
