# CLAUDE.md

Guidance for Claude Code (and the `impeccable` skill) when working in this repo.

## What this is

Status Green Solutions' marketing site: a single-page Vue app deployed to GitHub Pages (`statusgreensolutions.github.io`). Read `PRODUCT.md` for who it's for and why, and `DESIGN.md` for the visual system (colors, type, components, do's/don'ts). Don't duplicate either here — check them before making product or visual decisions.

## Stack

- Vite + Vue 3 (`<script setup lang="ts">` SFCs) + TypeScript
- Tailwind CSS v4, CSS-first config — theme tokens live in `src/style.css` under `@theme` (`--color-*`, `--font-*`, `--radius-*`), not a `tailwind.config.js`. `DESIGN.md`'s `{colors.*}` / `{rounded.*}` tokens map directly to these.
- Fonts self-hosted via `@fontsource/*` packages, imported in `src/style.css`.

## Commands

- `npm run dev` — Vite dev server (default port 5173; check before starting a second one, it's often already running).
- `npm run build` — type-checks (`vue-tsc -b`) then builds.
- `npm run preview` — serve the production build locally.

No test suite or linter is configured.

## Structure

- `index.html` → `src/main.ts` → `src/App.vue`, which composes the page from `src/components/*.vue` in order: `TheNav`, `TheHero`, `ConsoleModule`, `WhatWeDo`, `TrustBand`, `TheFooter`. One section = one component; add new sections the same way rather than growing `App.vue` or an existing component.
- `src/assets/` — logo SVGs (`sg-logo.svg` dark, `sg-logo-gray.svg` light-on-dark variant) and `terminal_banner.png` (the console-module proof image, see `DESIGN.md`).
- `src/style.css` — Tailwind entry, font imports, `@theme` tokens, and any global keyframes/utility classes (e.g. `.console-line`) that don't fit a single component.

## Conventions

- Style with Tailwind utility classes using the theme tokens above (`bg-primary`, `text-ink`, `font-display`, `rounded-md`, etc.); avoid introducing raw hex values or one-off fonts outside `DESIGN.md`'s palette/type system.
- Keep components single-file and self-contained (data/copy as local `const`s in `<script setup>`, no shared state store — the site doesn't need one).
- This is a real business's public site: don't invent stats, client names, or claims beyond what `PRODUCT.md`'s "Evidence on Hand" records.
