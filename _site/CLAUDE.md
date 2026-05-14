# CLAUDE.md

## Project Overview

**Intergalactic Bounce** — Jekyll static site for a bouncy castle hire business in Palnackie and Dalbeattie, Dumfries and Galloway, Scotland.

**Business:**
- One bouncy castle (may expand)
- £40/hour hire rate
- Serves Palnackie and Dalbeattie only
- Owner: Chris (chris@nashintergalactic.com)

**Booking flow:**
1. Customer visits `pages/book.html` and clicks the WhatsApp link
2. WhatsApp opens with a pre-filled message to 07827910339
3. Owner handles booking manually via WhatsApp

## Development Commands

```bash
bundle install
bundle exec jekyll serve --livereload   # http://localhost:4000
bundle exec jekyll build
```

## Architecture

- `_layouts/default.html` — base shell (nav, footer, all CSS inline as `<style>`)
- `_layouts/home.html`, `_layouts/page.html` — extend default
- `index.html` — homepage
- `pages/book.html` — WhatsApp CTA page (no JS, no form)
- `pages/faq.html` — FAQ

No JavaScript on any page.

## Deployment

GitHub Pages — push to `main`, site rebuilds automatically.
