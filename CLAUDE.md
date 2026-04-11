# CLAUDE.md

## Project Overview

Personal portfolio site — a "museum" of physics/engineering simulations presented as art.
Built with vanilla HTML/CSS/JavaScript, no build tools. Deployed via GitHub Pages (main branch).

## Site Structure

- `index.html` — Gallery index (thumbnail grid linking to individual works)
- `001.html` — Flow around a Guitar (LBM fluid simulation)
- `002.html` — From the Radiant to the Reserved (heat equation)
- `003.html` — The Unseen Filter (Galton Board)
- `concept.html` — Bilingual (EN/JA) concept statement
- `about.html` — English only profile
- `images/` — Screenshots, source images, background texture

## Design Rules

- **Aesthetic**: Tadao Ando-inspired concrete modernism. Concrete wall background, minimal UI.
- **Layout**: Each work is displayed as "artwork on a concrete wall" — 60% width framed canvas with white caption card below.
- **Fonts**: Outfit (headings), IBM Plex Mono (labels/technical), Noto Sans JP (Japanese).
- **Nav/Footer**: Shared across all pages — Gallery / Concept / About links, frosted glass nav bar.
- **Caption card**: White background, title + technique + EN statement + JA statement.
- **Colors**: Dark canvas (#0a0a0a), concrete background, muted UI elements.

## Coding Conventions

- Single HTML file per work (inline CSS + JS, no external dependencies except Google Fonts).
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
- Screenshot: `images/00N — Title.png`
