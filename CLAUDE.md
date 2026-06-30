# CLAUDE.md

## Project Overview

Personal portfolio site — a "museum" of physics/engineering simulations presented as art.
Built with vanilla HTML/CSS/JavaScript, no build tools. Deployed via GitHub Pages (main branch).

## Site Structure

The site operates as a **profile hub** with the museum gallery linked back in.
The top page is the owner's profile with links to external activity (X, YouTube,
note, GitHub, AtCoder, Kaggle) plus a Gallery nav link. The gallery and works
001–003 are public again; **`concept.html` stays unlisted** (no inbound links from
public pages; reachable by direct URL) pending a future reorganization.

- `index.html` — Profile hub (hero + responsibilities + background + external links + Gallery nav link)
- `concept.html` — Bilingual (EN/JA) concept statement (**unlisted**)
- `gallery.html` — Museum gallery index (linked from hub nav)
- `001.html` — Flow around a Guitar (LBM fluid simulation, linked from gallery)
- `002.html` — From the Radiant to the Reserved (heat equation, linked from gallery)
- `003.html` — The Unseen Filter (Galton Board, linked from gallery)
- `about.html` — Redirect to `/` (kept so old links don't break)
- `404.html` — Not-found page styled as an empty museum wall (absolute paths — served at any depth)
- `images/` — Screenshots, source images, background texture
- `fonts/` — Self-hosted woff2 fonts + `fonts.css` (generated from Google Fonts, do not edit by hand)

## Design Rules

- **Aesthetic**: Tadao Ando-inspired concrete modernism. Concrete wall background, minimal UI.
- **Layout**: Each work is displayed as "artwork on a concrete wall" — 60% width framed canvas with white caption card below.
- **Fonts**: Outfit (headings), IBM Plex Mono (labels/technical), Noto Sans JP (Japanese). Self-hosted via `fonts/fonts.css` — no Google Fonts requests.
- **Nav/Footer**: Shared across all pages — frosted glass nav bar. The hub nav shows a Gallery link; inner public pages (gallery, works, 404) link Gallery / About. The unlisted concept page keeps Gallery / Concept / About and is reachable only by direct URL.
- **Caption card**: White background, title + technique + EN statement + JA statement.
- **Colors**: Dark canvas (#0a0a0a), concrete background, muted UI elements.

## Coding Conventions

- Single HTML file per work (inline CSS + JS, no external dependencies; fonts self-hosted in `fonts/`).
- Every page carries OGP + Twitter Card metadata (work pages use their screenshot as a large-image card).
- Canvas-based simulations with `devicePixelRatio` scaling.
- `simScale` variable to control simulation resolution.
- Loading overlay with progress bar for heavy computations (chunked setTimeout to avoid blocking UI).
- Controls as sliders below the caption card.

## Branch Strategy

- `main` — production (GitHub Pages source)
- `develop` — working branch
- Fast-forward merge from develop to main, push both.

## Work Naming

- Format: `00N — Title` (e.g., "001 — Flow around a Guitar")
- File: `00N.html`
- Screenshot: `images/00N.png`
