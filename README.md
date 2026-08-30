# Tech Blog

Personal tech blog built with **Hugo Extended** and the **Google Docsy Theme**, published at [https://chornthorn.github.io/tech/](https://chornthorn.github.io/tech/).

## Prerequisites

- **Hugo Extended** (`v0.160+`):
  ```bash
  brew install hugo
  ```
- **Node.js** (`v18+`) & **npm**

## Local Setup

```bash
npm install
npm run serve
# or directly:
hugo server --disableFastRender
```

Navigate to `http://localhost:1313/tech/` in your browser. Live reloading is enabled by default.

## Build Static HTML

```bash
npm run build
# or:
hugo --minify
```

The compiled static site is output to `public/`.

## Content

This site contains **blog posts only** — write new posts under `content/blog/<year>/`:

```
content/
└── blog/
    ├── _index.md             # Blog landing page (year-grouped post list, RSS)
    └── 2026/                 # Posts grouped by year in the URL (e.g. /blog/2026/<post>/)
        ├── _index.md
        └── <post>.md
```

The home page (`layouts/home.html`) shows the three latest posts and renders
the About section from `content/_index.md`.

## Environment Variables

None.

## Deployment (GitHub Pages)

The site is a GitHub Pages **project site** for the `chornthorn/tech` repository, so `baseURL` is `https://chornthorn.github.io/tech/`.

Build with `hugo --minify` and publish the `public/` directory — e.g. via a GitHub Actions workflow or by pushing `public/` to the `gh-pages` branch.
