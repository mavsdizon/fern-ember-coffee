# Fern & Ember Coffee — Website

A clean, mobile-friendly one-page website for **Fern & Ember Coffee**, a neighborhood specialty coffee shop for students and young professionals.

**Live site:** _add your Netlify or custom domain link here_

## Features

- **Hero** with headline, "Visit Us" call to action and quick perks
- **Menu** with 6 items, prices and pictures
- **About** section with the shop's story and values
- **Opening hours** with today's row highlighted automatically
- **Location** card with map placeholder and "Get Directions" link
- **Contact** details and a contact form
- Responsive layout with a mobile hamburger menu
- Pictures that always display: built-in illustrations, with Unsplash photos layered on top when available

## Tech stack

- HTML5
- CSS3 (custom properties, Grid, Flexbox — no frameworks)
- Vanilla JavaScript (mobile menu, hours highlight, form message)
- Google Fonts: Manrope and Inter

Everything lives in a single `index.html` file. There is no build step and nothing to install.

## Project structure

```
fern-ember-coffee/
├── index.html   # The whole website: markup, styles and scripts
├── README.md    # Project overview (this file)
├── CLAUDE.md    # Project context for Claude / AI assistants
└── .gitignore   # Files Git should ignore
```

## Run locally

Open `index.html` in any web browser. That's it.

Optional, to preview with a local server:

```bash
npx serve .
```

## Deployment

The site is a static page, so it can be hosted anywhere that serves HTML.

**Netlify (drag and drop):** go to app.netlify.com/drop and drag the project folder onto the page.

**Netlify (from GitHub):** in Netlify choose **Add new site → Import an existing project**, pick this repository, leave the build command empty and set the publish directory to `/`. Every push to `main` then redeploys automatically.

## Customizing

| What to change | Where in `index.html` |
|---|---|
| Colors | CSS variables in `:root` at the top of the `<style>` block |
| Business name, text, prices | Directly in the HTML sections |
| Photos | `src` of each `<img>` inside a `.pic` block |
| Map | Replace the `.map-placeholder` block with a Google Maps embed |
| Contact form | Connect to Netlify Forms or Formspree |

## To do

- [ ] Replace sample name, address, phone and email with real details
- [ ] Add a real Google Maps embed
- [ ] Connect the contact form so messages are delivered
- [ ] Connect a custom domain

## Author

**Maverick D** — [GitHub](https://github.com/your-username)

## License

© 2026 Maverick D. All rights reserved.
