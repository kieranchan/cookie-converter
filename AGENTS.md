# Project Instructions (Codex)

This file defines project-level instructions for Codex/CLI agents.
All changes must follow these rules.

## Project Overview
- Purpose: Convert browser cookies between formats (DevTools table, JSON, Netscape cookies.txt) and present outputs as string/table/domain views.
- Templates: Four UI variants live in separate folders. Each variant should provide the same core functionality unless explicitly noted.

## Directory Structure
- `index.html`
  - Landing page that links to the four templates.
  - Must remain lightweight and load without build steps.
- `manifest.json`
  - PWA manifest shared by templates.
  - If templates are in subfolders, references should use relative paths (e.g. `../manifest.json`).
- `v1-default/index.html`
  - Full-featured default UI.
  - Includes history, theme toggle, search/filter, and optional drag/drop.
- `v2-glass/index.html`
  - Glassmorphism variant.
  - Same core features; can use different visual language.
- `v3-terminal/index.html`
  - Terminal/CRT themed variant.
  - Emphasizes logs and command-line style but must keep core features.
- `v4-minimal/index.html`
  - Minimal UI variant.
  - Keep functionality parity; visuals should remain minimal.

## Functional Parity (Must-Have)
Each template must support:
- Input parsing:
  - DevTools table-like paste
  - JSON array/object
  - Netscape cookies.txt
- Outputs:
  - Cookie string (name=value; ...)
  - Table view
  - Domain-grouped view
- Utilities:
  - URL decode toggle
  - Copy to clipboard
  - Export: JSON, Netscape, cURL
- Flags/Badges:
  - Secure, HttpOnly, SameSite, Session/Expires (as appropriate)
  - Sensitive cookie detection (token/auth/secret/etc.)

## Export/Parsing Rules
- JSON:
  - Read `expirationDate` (seconds) when present.
  - If `expires` exists in JSON, preserve it.
- Netscape:
  - Convert ISO date to epoch seconds.
  - Use `0` for session cookies or invalid dates.
- Session detection:
  - Treat empty expires or `Session` as session cookies.

## UI/UX Rules
- Maintain responsiveness for mobile (max-width <= 900px).
- Avoid breaking keyboard shortcuts (Ctrl+Enter to convert where present).
- Keep toasts and warnings consistent with each template's style.
- Do not introduce a build step; stay in single-file HTML per template.

## Change Tracking (Required)
- Update `CHANGELOG.md` for every change.
- Include:
  - Date (YYYY-MM-DD)
  - Summary of changes
  - Files touched

## Safety Notes
- No external network calls.
- Avoid adding new dependencies unless strictly necessary.
- Keep changes minimal and avoid regressions.
