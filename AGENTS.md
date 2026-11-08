# AGENTS.md

## Project overview

This repository is a small static wedding invitation site built with plain HTML, CSS, and JavaScript. The app is intentionally dependency-free and designed for a polished single-page experience with a language switch between English and Telugu.

## Key files

- [index.html](index.html): page structure, invitation sections, language gate, and dynamic `data-i18n` hooks.
- [styles.css](styles.css): all visual styling, motion, responsive behavior, and layout.
- [script.js](script.js): translation dictionary, countdown logic, scene behavior, and language switching.
- [ganesh.png](ganesh.png): decorative asset used throughout the invitation.

## Working conventions

- Keep the project lightweight: prefer direct HTML/CSS/JS edits over introducing build tooling or frameworks.
- Preserve the existing structure of the invitation and the `data-i18n` attributes when changing text.
- If you add new copy, update both English and Telugu translations in `translations` in [script.js](script.js) to keep the language switch synchronized.
- Maintain accessibility: keep button labels, alt text, and semantic structure intact, especially around the language selection experience.
- Respect the current design system: warm maroon/gold palette, serif typography, and soft animated transitions.

## Local preview

There is no build step. To preview the site locally, run one of these from the project root:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000` in a browser.

## Decision notes for future agents

- This is a presentation/static marketing page, not an app with a backend.
- Prefer small, targeted edits: update copy in the existing translation map and styling in [styles.css](styles.css) rather than reworking the whole page.
- Any changes to sections or interaction flow should remain compatible with the existing scroll-driven cinematic behavior and language gate.
- If introducing new content blocks, keep them consistent with the current `scene`/`section` structure and responsive CSS patterns.
