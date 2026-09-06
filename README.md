# QA Engineer Portfolio

Personal portfolio website for **Firman Fajar Kurniawan** — Quality Assurance Engineer with 8+ years of experience in E-commerce and payment systems.

## Tech Stack

- **HTML5** — semantic, accessible markup
- **Tailwind CSS** (via CDN) — utility-first styling
- **Vanilla JavaScript** — mobile navigation and scroll-reveal animations
- **Inter** — typography via Google Fonts

## Pages

| Page | Description |
|------|-------------|
| `index.html` | Hero, professional summary, and quick stats |
| `projects.html` | QA automation projects with live demo videos |
| `skills.html` | Testing tools & frameworks organized by category |
| `contact.html` | Contact links and CV download |

## Project Structure

```
.
├── index.html          # Home / hero page
├── projects.html       # QA automation projects
├── skills.html         # Skills & tools
├── contact.html        # Contact information
├── assets/
│   ├── favicon.ico
│   └── Firman-Fajar-Kurniawan-QA-CV.pdf
├── css/
│   └── style.css       # Shared styles (animations, nav, cards)
├── js/
│   └── main.js         # Mobile nav + scroll reveal
└── images/
    └── profile.jpg
```

## Running Locally

No build step required — it's a static site. Serve it with any static server:

```bash
# Python
python3 -m http.server 8080

# or Node
npx serve .
```

Then open http://localhost:8080

## Deployment

Deploys as-is to any static host: **GitHub Pages**, Netlify, or Vercel. No build configuration needed.
