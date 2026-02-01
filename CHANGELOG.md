# Changelog

All notable changes to this project will be documented in this file.

## 2026-02-01
- Fixed structure: moved the v1 template into `v1-default/index.html` and corrected manifest path.
- Added root landing page `index.html` linking all four templates.
- Implemented glass theme toggle with persistent selection in `v2-glass/index.html`.
- Standardized JSON parsing to preserve `expires` where provided.
- Standardized Netscape export to use real expiry epoch values.
- Improved session detection/labels in `v2-glass`, `v3-terminal`, and `v4-minimal`.
- Added format indicators in output (v2/v3/v4) and expired badges (v2/v3/v4).
- Improved parsing robustness (comment line handling, expires from table in v4).
- Added accessibility improvements (aria-live toasts, focus-visible styles).
- Hardened copy/export flows (clipboard fallback + revokeObjectURL).
- Added a shared SVG favicon and linked it across templates to avoid favicon 404s on GitHub Pages.
- Added a Chinese README describing features, usage, and templates.
- Added per-template SVG favicons to match each UI variant.
- Added missing manifest links in v2/v3/v4 templates.
- Removed external Google Fonts imports to comply with the no-network rule.
- Added `.gitignore` to exclude IDE metadata (e.g., `.idea/`).

Files touched:
- `AGENTS.md`
- `CHANGELOG.md`
- `index.html`
- `favicon.svg`
- `favicon-v1.svg`
- `favicon-v2.svg`
- `favicon-v3.svg`
- `favicon-v4.svg`
- `README.md`
- `v1-default/index.html`
- `v2-glass/index.html`
- `v3-terminal/index.html`
- `v4-minimal/index.html`
