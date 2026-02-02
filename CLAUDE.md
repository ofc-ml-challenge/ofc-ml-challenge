# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the OFC 2026 ML Challenge website, built using the **al-folio** Jekyll theme. It's a static site for an academic machine learning challenge related to optical networking.

## Common Commands

### Local Development with Docker (Recommended)

```bash
# Start the development server
docker compose pull
docker compose up

# Site available at http://localhost:8888
# Uses live reload - changes to files auto-refresh the browser
```

### Local Development without Docker (Legacy)

```bash
bundle install
pip install jupyter
bundle exec jekyll serve
# Site available at http://localhost:4000
```

### Build for Production

```bash
export JEKYLL_ENV=production
bundle exec jekyll build
# Output goes to _site/ directory

# Optional: Remove unused CSS
purgecss -c purgecss.config.js
```

### Code Formatting

```bash
npm install
npx prettier --check .   # Check formatting
npx prettier --write .   # Fix formatting
```

## Architecture

### Jekyll Static Site Structure

- **`_config.yml`** - Main site configuration (title, URL, plugins, features)
- **`_pages/`** - Markdown files for static pages (about, ml-challenge, call-for-submission, etc.)
- **`_layouts/`** - Liquid templates (`.liquid` files) defining page structures
- **`_includes/`** - Reusable HTML/Liquid components
- **`_sass/`** - SCSS stylesheets
- **`_data/`** - YAML data files (cv.yml, repositories.yml, etc.)
- **`assets/`** - Static assets (images, PDFs, JSON, JavaScript)
- **`_bibliography/`** - BibTeX files for publications (papers.bib)

### Content Collections

- **`_news/`** - News/announcement items displayed on homepage
- **`_posts/`** - Blog posts
- **`_projects/`** - Project showcase items

### Key Configuration in `_config.yml`

- `url`: `https://ofc-ml-challenge.github.io`
- `baseurl`: `/ofc-ml-challenge`
- Site uses Jekyll Scholar for academic publications from `_bibliography/papers.bib`
- MathJax enabled for math typesetting
- Google Analytics configured

## Deployment

- **Automatic deployment** via GitHub Actions on push to `main` branch
- Deploys to GitHub Pages using `gh-pages` branch
- Workflow defined in `.github/workflows/deploy.yml`
- Uses Ruby 3.3.5 and Python 3.13 in CI

## Page Front Matter

Pages in `_pages/` use YAML front matter:
```yaml
---
layout: about      # Layout template from _layouts/
title: about       # Page title
permalink: /       # URL path
---
```

## Adding Content

- **New page**: Create `.md` file in `_pages/` with front matter
- **New publication**: Add BibTeX entry to `_bibliography/papers.bib`
- **News item**: Create `.md` file in `_news/`
- **Images**: Place in `assets/img/` and reference in markdown
