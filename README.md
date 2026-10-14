# Kotlin Guide — Static Site for Cloudflare Pages

A beautiful, kotlinlang.org-inspired multi-page static website that explains Kotlin, getting started, installation, coding, and documentation resources.

## Pages (endpoints)

| Path | Description |
|------|-------------|
| `/` or `/index.html` | Home — overview, why Kotlin, hello world |
| `/getting-started.html` | Getting started guide |
| `/install.html` | Installation (IDE, CLI, SDKMAN, Android Studio) |
| `/learn.html` | **Full step-by-step tutorial** (learnpython.org style) — 36 lessons covering basics through generics, sealed types, delegation, sequences, coroutines & Flows |
| `/coding.html` | Language features & coding examples |
| `/docs.html` | Docs map & official resources |

## Features

- Dark purple/teal theme inspired by kotlinlang.org
- Fully responsive
- Inline SVG icons throughout
- Syntax-highlighted code blocks with copy buttons
- Tabbed install instructions
- Mobile navigation
- Zero build step — pure HTML/CSS/JS

## Deploy to Cloudflare Pages

1. Unzip this archive.
2. In the Cloudflare dashboard: **Workers & Pages** → **Create** → **Pages** → **Upload assets**.
3. Upload the contents of this folder (or connect a Git repo that contains these files).
4. Set the build command to empty / none and the output directory to `/` (root).
5. Deploy.

Alternatively with Wrangler:

```bash
npx wrangler pages deploy . --project-name=kotlin-guide
```

## Local preview

Open `index.html` in a browser, or serve with any static server:

```bash
npx serve .
# or
python -m http.server 8080
```

## Structure

```
├── index.html
├── getting-started.html
├── install.html
├── coding.html
├── docs.html
├── css/styles.css
├── js/main.js
├── assets/favicon.svg
└── README.md
```
