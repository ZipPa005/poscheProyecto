# Repository Guidelines

## Project Structure & Module Organization
- Root-level HTML lives in the top directory (`index.html`, `product.html`, `about.html`, `contact.html`, `client.html`), with styling and behavior broken out into `css/` and `js/`.
- `images/` and `fonts/` store the media assets referenced by the templates; `porscheImagenes/` contains brand imagery not part of the generic asset folders.
- Assets that depend on third-party tooling (Bootstrap, Owl Carousel) are already referenced via CDN links in the HTML head, so coverage is mostly static files.

## Build, Test, and Development Commands
- There are no build or test scripts in this static site; open `index.html` in a browser to preview, or serve the directory locally (for example, `npx http-server .` or `python -m http.server 8000`) to exercise JS-driven components.
- Use the browser developer console to verify responsive breakpoints or interactive features after editing the static files.

## Coding Style & Naming Conventions
- HTML uses two-space indentation and keeps attributes one per line when helpers (Bootstrap classes, data attributes) grow long; keep this pattern when modifying the markup.
- CSS resides in `css/style.css` and `css/responsive.css` and should follow the existing selector ordering (framework imports first, then custom overrides); keep media queries grouped at the bottom of the file.
- File names are lowercase with hyphen separators for multi-word identifiers (e.g., `custom_nav-container` in HTML, `responsive.css`), matching the current assets.

## Testing Guidelines
- No automated tests are defined; rely on manual preview in-browser across Chrome/Edge and desktop/mobile viewports.
- Double-check interactive elements (nav toggles, carousels) after any JavaScript change by triggering their behaviors in a local host environment.

## Commit & Pull Request Guidelines
- This repository currently lacks a Git history, but we recommend using Conventional Commits (`feat:`, `fix:`, `docs:`) once version control is enabled to keep changes clear.
- Pull requests should include a short description of what was changed, reference any related issue numbers (if applicable), and note any visual regressions that reviewers should look for during manual QA.

## Security & Configuration Tips
- Sensitive configuration or assets (e.g., API keys or private imagery) should never be committed; keep this repo limited to the static showcase files already present.
