# QA Engineer Portfolio

Personal portfolio website for **Firman Fajar Kurniawan** — Quality Assurance Engineer with 8+ years of experience in E-commerce and payment systems.

## Design

Single-page Linear-inspired dark technical layout with a QA "pass signal" accent (`#00E5A0`).

- **Space Grotesk** — display headings
- **Inter** — body
- **JetBrains Mono** — labels, tags, stats
- **Vanilla CSS + JS** — no build step, no Tailwind

## Sections

| Anchor | Content |
|--------|---------|
| `#about` | What I do, domains, beyond testing |
| `#skills` | Automation, methodology, performance, API, data, CI/CD |
| `#projects` | Appium/Playwright demos + GitHub projects |
| `#experience` | Bluesky Tech → Catalyst → Tiket.com → Elevenia + education |
| `#contact` | LinkedIn, GitHub, Email, CV download |

Old multipage URLs (`experience.html`, `projects.html`, `skills.html`, `contact.html`) redirect to the matching anchors on `index.html`.

## Video demos

Google Drive embeds use the **file preview** endpoint:

```
https://drive.google.com/file/d/{FILE_ID}/preview
```

> **Why videos failed before:** `docs.google.com/videos/d/{id}/preview` returns **404** for Drive-hosted files. Drive file videos must be embedded via `drive.google.com/file/d/{id}/preview`.
>
> Sharing must also be set to **Anyone with the link**. Each demo card includes an "Open demo on Drive" fallback link.

## Running Locally

```bash
python3 -m http.server 8080
# or
npx serve .
```

Then open http://localhost:8080

## Deployment

Static site — deploys as-is to **GitHub Pages**, Netlify, or Vercel.

## Project Structure

```
.
├── index.html          # Single-page portfolio
├── experience.html     # Redirect → index.html#experience
├── projects.html       # Redirect → index.html#projects
├── skills.html         # Redirect → index.html#skills
├── contact.html        # Redirect → index.html#contact
├── assets/
│   ├── favicon.ico
│   └── Firman-Fajar-Kurniawan-QA-CV.pdf
├── css/style.css       # Design system
├── js/main.js          # Nav + scroll reveal
└── images/
```
