# Queenly Beauty E-Commerce Platform

A luxury beauty e-commerce frontend built with **SvelteKit** and **Tailwind CSS v4**.

Design sourced from [Google Stitch](https://stitch.googleapis.com) project.

## Tech Stack

- **SvelteKit** — Full-stack web framework
- **Tailwind CSS v4** — Utility-first CSS with custom design tokens
- **TypeScript** — Type safety
- **Playfair Display + Montserrat** — Typography pairing

## Getting Started

```bash
npm install
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

## Build

```bash
npm run build
npm run preview
```

## Project Structure

```
src/
├── lib/
│   └── components/
│       ├── Navbar.svelte
│       ├── Hero.svelte
│       ├── Categories.svelte
│       ├── QueensPicks.svelte
│       ├── Newsletter.svelte
│       └── Footer.svelte
└── routes/
    ├── +layout.svelte
    ├── +page.svelte
    └── layout.css          # Tailwind theme tokens
```

## Design Tokens

Custom Material 3 color system with:
- Deep forest greens (primary)
- Gold accents (secondary)
- Warm neutrals (surface/background)

Typography: Playfair Display for headlines, Montserrat for body text.
