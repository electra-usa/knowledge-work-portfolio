# Knowledge Work & Slides Portfolio

Live site: https://electra-usa.github.io/knowledge-work-portfolio/

A curated showcase of decks, frameworks, and written deliverables — kept separate from
unrelated repos so visitors only see this type of work.

## Structure

- `index.html` — the whole site: typing header + badge row, personal intro, a shared
  Claude-activity heatmap, and two accordions — **See my work** (the categorized project
  grid: Slide Decks, Frameworks & Playbooks, Case Studies, Consulting Deliverables) and
  **Additional projects I'm working on** (non-repo work in progress, shown as dark status
  cards).
- `assets/` — cover images and thumbnails referenced from `index.html`.

## Things to fill in

Search `index.html` for `[EDIT ME` to find every placeholder: your name/bio/pronouns,
contact links, badge URLs, and the two typing-animation lines.

## Shared pieces

The typing header, badge row, and heatmap follow the same pattern as
[automations-portfolio](https://github.com/electra-usa/automations-portfolio). The heatmap
is intentionally **not** duplicated — it loads `heatmap.js` and `claude-usage.json` from
[portfolio-shared](https://github.com/electra-usa/portfolio-shared), so updating that one
repo updates both sites at once.

## Adding a project

1. Duplicate a `<a class="card">` block inside the relevant `<section class="category">`.
2. Set `href` to wherever the work lives:
   - Slides: a Google Slides "Publish to web" link, a Canva share link, or a PDF committed
     to this repo (link directly to the file, e.g. `assets/deck-name.pdf`).
   - Case studies / deliverables: a PDF in `assets/`, a Notion public page, or a written
     page you add to this repo.
3. Drop a cover image into `assets/` and reference it in the `.thumb` div, e.g.:
   `<div class="thumb"><img src="assets/your-image.png" alt="..."></div>`
4. Commit and push to `main` — GitHub Pages redeploys automatically within a minute or two.

## Notes

- This repo is intentionally public and separate from private/forked repos — it is meant
  to be linked directly as a portfolio, not browsed via the main GitHub profile.
- `.nojekyll` disables Jekyll processing since this is a plain static site.
