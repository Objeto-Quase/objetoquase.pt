# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Jekyll-based website for the band "Objeto Quase", hosted on GitHub Pages at objetoquase.pt. All content is in European Portuguese.

## Development Commands

```bash
# Install dependencies
bundle install

# Run local server (http://localhost:4000)
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

## Architecture

Single-page website with anchor navigation. All sections are included in `index.md`.

### Directory Structure
- `_layouts/` - HTML templates (`default.html` is the base)
- `_includes/` - Reusable components (header, footer)
- `_includes/sections/` - Page sections (hero, musica, concertos, merch, sobre)
- `_data/` - YAML data files for content
- `assets/css/` - SCSS stylesheets
- `assets/images/` - Band photos and logos
  - `band/` - Band photos
  - `releases/` - Album covers
  - `merch/` - Merchandise images

### Content Management

Content is managed through YAML files in `_data/`:
- `musica.yml` - Albums and releases
- `concertos.yml` - Concert dates
- `merch.yml` - Merchandise items
- `social.yml` - Social media links

Each file contains commented examples showing the expected format.

### Styling

Dark theme with SCSS variables defined at the top of `assets/css/main.scss`:
- `$accent-color` - Gold (#c9a227), configurable in `_config.yml`
- Mobile-first responsive design with breakpoint at 768px
