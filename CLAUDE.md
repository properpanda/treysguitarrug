# Trey's Guitar Rug

Hugo-based static site hosted on GitHub Pages.

## Build Commands

- `hugo server` — local dev server with live reload (http://localhost:1313)
- `hugo server --buildDrafts` — include draft posts
- `hugo` — build site to `public/`
- `hugo --gc --minify` — production build (used in CI)

## Project Structure

```
content/          — markdown content (posts, pages)
  _index.md       — homepage
  about.md        — about page
  posts/          — blog posts (rug articles)
themes/PaperMod/  — PaperMod theme (git submodule)
hugo.toml         — site configuration
static/           — static assets (images, etc.)
.github/workflows/hugo.yml — GitHub Actions deployment
```

## Theme

PaperMod, added as a git submodule. After cloning, run:
```
git submodule update --init --recursive
```

## Deployment

Automated via GitHub Actions on push to `main`. The workflow builds the site and deploys to GitHub Pages.

Site URL: https://treysguitarrug.com/

## Content

Posts use front matter with `tags` and `categories` taxonomies for organizing by tour, year, etc.
