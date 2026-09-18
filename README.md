# QA Engineer Portfolio

Personal portfolio for **Firman Fajar Kurniawan** — QA Engineer with 8+ years in E-commerce and payment systems.

**Live:** https://firmanfajar19.github.io/portofolio/

## Stack

- Vanilla **HTML / CSS / JS** — no build step, no framework, no Tailwind
- Google Fonts: Space Grotesk (display), Inter (body), JetBrains Mono (labels)
- Design system tokens in `css/style.css` (`:root`)

## Sections

Single page (`index.html`). Navigation uses anchors:

| Anchor | Content |
|--------|---------|
| `#about` | What I do, domains, beyond testing |
| `#skills` | Automation, methodology, performance, API, data, CI/CD |
| `#projects` | Appium/Playwright demos + GitHub projects |
| `#experience` | Bluesky Tech → Catalyst → Tiket.com → Elevenia + education |
| `#contact` | LinkedIn, GitHub, Email, CV download |

`experience.html`, `projects.html`, `skills.html`, and `contact.html` are redirect stubs to the matching anchors (old multipage URLs).

## Project structure

```
.
├── index.html          # All real content (single page)
├── experience.html     # Redirect → index.html#experience
├── projects.html       # Redirect → index.html#projects
├── skills.html         # Redirect → index.html#skills
├── contact.html        # Redirect → index.html#contact
├── AGENTS.md           # Notes for AI coding agents
├── assets/
│   ├── favicon.ico
│   ├── og-cover.png    # 1200×630 social preview used by og:image / twitter:image
│   └── Firman-Fajar-Kurniawan-QA-CV.pdf
├── css/style.css       # Design tokens + layout
├── js/main.js          # Mobile nav + scroll reveal + footer year
└── images/profile.jpg  # Unused (hero uses a QA console panel, not a photo)
```

## Run locally

```bash
python3 -m http.server 8080
# or: npx serve .
```

Open http://localhost:8080. Use a local server — `file://` breaks fonts and iframes.

Both the page and `assets/og-cover.png` are checked in, so the site has no build step: edit the file, refresh, done.

## Deploy

Static site on **GitHub Pages**. Push to `main`:

```bash
git push origin main
```

No workflow file; Pages is enabled on the GitHub repo.

## Video demos

Google Drive embeds must use the **file preview** URL:

```
https://drive.google.com/file/d/{FILE_ID}/preview
```

`docs.google.com/videos/d/{id}/preview` returns **404** in an iframe. Files must be shared as **Anyone with the link**. Each demo card also has an “Open demo on Drive” fallback.

## Content source of truth

Career details and skills should match `assets/Firman-Fajar-Kurniawan-QA-CV.pdf`. LinkedIn (`/in/loncing`) is often login-walled, so prefer the CV when updating copy.
