# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static personal website for Kuba Jądrzak, hosted at https://www.kubajadrzak.com. No build tools, package managers, or frameworks — just plain HTML and CSS.

## Development

Open `index.html` directly in a browser to preview. To serve locally:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

## Architecture

Everything lives in two places:

- **[index.html](index.html)** — All HTML structure and CSS styles in a single file (~260 lines). No external stylesheets, no JavaScript.
- **[images/](images/)** — Static assets: profile picture, project logos, social media icons (PNG/SVG).

CSS uses media queries at `900px` and `1400px` breakpoints for responsive layout. Hover effects are done with CSS transitions (`transform`, `box-shadow`).

## Content Structure

The page has two sections:
1. **My Projects** — project cards with logo, title, description, and links
2. **Connect with Me** — social/contact links (GitHub, LinkedIn, email)

To add a project: add a new `<div class="project">` block in the projects section and place the logo image in `images/`.
