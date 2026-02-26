# Process Documentation — Uncle Roger's Comic Shop

## Project Overview

A multi-page website for Uncle Roger's Comic Shop, a fictional local comic book store. The site includes four pages: Home, About, Catalog, and Contact, all built with semantic HTML, custom CSS, and vanilla JavaScript.

## Development Process

### 1. Site Structure & Layout

Started by establishing the core HTML structure across four pages (`index.html`, `about.html`, `menu.html`, `contact.html`) with a shared navigation bar, hero sections, content areas, and a consistent footer. Each page uses the same `styles.css` stylesheet for a unified look and feel.

### 2. Visual Design & Styling

Designed a bold, comic-book-inspired aesthetic using CSS custom properties for theming. Key design decisions:

- Comic-style color palette with strong yellows, reds, and dark backgrounds
- Card-based layouts for features, catalog items, and weekly events
- Responsive grid layouts that stack on smaller screens
- Fade-in animations for visual polish

### 3. Hero Sections & Imagery

Each page features a hero section with a side-by-side layout — page title and description on the left, a banner image on the right. On mobile, these stack vertically. Images are styled with rounded corners and shadow effects.

### 4. Dark/Light Mode Implementation

Followed a structured build plan (see `docs/BUILD-PLAN.md`):

1. **CSS Variables & Themes** — Defined color palettes as custom properties on `:root` (light) and `[data-theme="dark"]` (dark)
2. **Toggle Button & JS** — Added a sun/moon toggle button in the navbar that switches the `data-theme` attribute on `<html>`
3. **Persist Preference** — Saved the chosen theme to `localStorage` so it persists across page loads
4. **System Preference** — Used `prefers-color-scheme` media query as a fallback and added a `matchMedia` listener for live OS theme changes
5. **Flash Prevention** — Placed theme-detection script in `<head>` (before render) to avoid a flash of the wrong theme on load

### 5. Navigation & Interactivity

- Responsive hamburger menu toggle for mobile viewports
- Active page highlighting in the nav links
- Smooth theme transitions (disabled on initial load to prevent flash)

## Tools & Technologies

- **HTML5** — Semantic markup
- **CSS3** — Custom properties, Flexbox, Grid, animations, media queries
- **JavaScript** — DOM manipulation, localStorage, matchMedia API
- **Claude Code** — AI-assisted development for implementation and iteration

## File Structure

```
week5/
├── index.html          # Home page
├── about.html          # About page
├── menu.html           # Catalog page
├── contact.html        # Contact page
├── styles.css          # Shared stylesheet
├── PROCESS.md          # This file
├── CLAUDE-TRANSCRIPT.txt
├── docs/
│   └── BUILD-PLAN.md   # Dark mode implementation plan
├── images/
│   └── uncle.webp
└── public/
    └── images/
        └── hero.jpg
```
