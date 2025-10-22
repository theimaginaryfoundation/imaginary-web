# Repository Guidelines

## Project Structure & Module Organization
This site is intentionally single-page. All customer-facing markup and styles live in `index.html`, including the glassmorphic theme and Formspree capture form. Keep new sections grouped with semantic elements (`<section>`, `<nav>`, `<footer>`) to preserve scroll behavior. Contributor process notes live in `CLAUDE.md`; update it alongside structural shifts. Use `README.md` to communicate launch status or live dependencies.

## Build, Test, and Development Commands
There is no build step; serve the raw HTML while developing to mirror production. Any lightweight static server works:
```bash
python3 -m http.server 8000
```
or
```bash
npx serve .
```
Run these from the repo root and visit `http://localhost:8000/index.html`. When editing the Formspree endpoint, submit a test entry against the local form before pushing.

## Coding Style & Naming Conventions
Indent HTML and CSS with four spaces to match the existing file. Favor semantic tags over generic `<div>` blocks and keep class names lowercase kebab-case (e.g. `hero-banner`). When adding CSS, reuse the color tokens defined in `:root` and place new variables near related shades. Inline JavaScript should stay minimal and live at the bottom of `index.html`; reach for progressive enhancement rather than blocking interactions.

## Testing Guidelines
Manual review is expected. After each change, check layout on desktop and mobile breakpoints and verify the sticky navigation scrolls smoothly. Validate markup with `npx htmlhint index.html` (install-if-missing via `npm install htmlhint --save-dev`) and confirm the Formspree response shows `200 OK` in the browser console. Document any known visual regressions in the pull request.

## Commit & Pull Request Guidelines
Follow the existing Git history by writing short, imperative commit subjects (e.g. `Refine subscribe copy`). Squash incidental work into focused commits that describe user-facing impact. Pull requests should include: 1) a clear summary of the intent, 2) references to related issues or discussions, and 3) before/after screenshots or a short Loom when visual changes occur. Mention any follow-up tasks so the homepage stays production-ready.

## Deployment Notes
Production is served via GitHub Pages from the default branch. Verify that `index.html` remains at the repository root and avoid adding build artifacts—only committed assets are deployed. After merging, allow a few minutes for Pages to refresh, then spot-check the live form submission to confirm the Formspree integration still routes correctly.
