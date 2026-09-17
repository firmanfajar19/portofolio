# AGENTS.md

Static personal portfolio for Firman Fajar Kurniawan (QA Engineer). No package.json, no build, no tests, no CI.

## What this repo is

- **Single-page site.** Real content lives only in `index.html` (anchors: `#about`, `#skills`, `#projects`, `#experience`, `#contact`).
- **Redirect stubs.** `experience.html`, `projects.html`, `skills.html`, `contact.html` are meta-refresh + `location.replace` shims to `index.html#…`. Do not put real content in them.
- **Stack.** Vanilla HTML + CSS + JS. No Tailwind, no bundler, no framework. Fonts load from Google Fonts CDN (Space Grotesk / Inter / JetBrains Mono).
- **Deploy.** Push to `main` → GitHub Pages (`https://firmanfajar19.github.io/portofolio/`). No workflow file; Pages is configured on the repo.

## Local preview

```bash
python3 -m http.server 8080
# or: npx serve .
```

Open http://localhost:8080. Relative assets need a server (file:// is unreliable for iframes/fonts).

## Design system (do not drift)

Tokens live in `css/style.css` `:root`. Match them; do not invent a second palette or reintroduce Tailwind CDN.

- Accent / “pass signal”: `--accent: #00e5a0` on dark bg `#070b0f`
- Fonts: `--font-display` (Space Grotesk), `--font-body` (Inter), `--font-mono` (JetBrains Mono)
- Scroll-reveal classes are **`.reveal` → `.is-visible`** (wired in `js/main.js`). Using `.visible` alone will leave content invisible.
- Hero visual is a **QA console panel**, not a photo. `images/profile.jpg` still exists on disk but is intentionally unused — do not re-add a portrait without asking.

## Google Drive video embeds (easy to break)

Demo videos must use the **file preview** URL:

```
https://drive.google.com/file/d/{FILE_ID}/preview
```

- `https://docs.google.com/videos/d/{ID}/preview` and the share “play” link return **404** in an iframe.
- Sharing on Drive must be **Anyone with the link**, or the embed shows a permission wall.
- Keep an “Open demo on Drive” fallback link (`…/file/d/{ID}/view`) under each iframe.

Current file IDs are in `index.html` (`#projects`). Verify with curl (`-w '%{http_code}'`) if embeds regress.

## Content sources

- **LinkedIn** (`https://www.linkedin.com/in/loncing`) is login-walled from most agents. Prefer `assets/Firman-Fajar-Kurniawan-QA-CV.pdf` for roles, skills, dates, and education.
- Current timeline: Bluesky Tech (Present) → Catalyst → Tiket.com → Elevenia; education Universitas Gunadarma.
- Owner contacts: LinkedIn `/in/loncing`, GitHub `/firmanfajar19`, email `firmanfajar19@gmail.com`.

## When editing

- Keep section copy and chips aligned with the CV; do not invent employers or metrics.
- Footer year is set in JS (`#year`); leave a hardcoded fallback in HTML.
- After HTML/CSS/JS edits, smoke-check: pages return 200, no leftover `docs.google.com/videos` embeds, no unexpected `profile.jpg` references.
- Commit/push only when the user asks. Work happens on `main` (no feature-branch convention observed).
