# CLAUDE.md

Portfolio + blog website for **OWL**, the solo indie game developer persona of the repo owner. It showcases OWL's games, an about section, and a blog. Live at **https://www.owlgame.dev**.

## Scope (read first)

**Work only on the raw HTML and CSS** — i.e. [index.markdown](index.markdown)/[_layouts/home.html](_layouts/home.html), [blog.html](blog.html), [lokis_revenge.html](lokis_revenge.html), and [styles.css](styles.css). **Do not touch or modify the Jekyll/minima theme internals** (the `*.scss` files, `_includes`/layout overrides, theme gems) unless explicitly asked. The Jekyll/minima details below are reference only.

## Stack & Hosting

- **Jekyll** static site using the **minima** theme, deployed via **GitHub Pages** (`github-pages` gem in the Gemfile).
- Custom domain set via [CNAME](CNAME) → `owlgame.dev`.
- Plugin: `jekyll-feed` (generates `/feed.xml`).
- Site-wide config in [_config.yml](_config.yml): title `OWL`, contact `owl@owlgame.dev`, blog permalink pattern `/blog/:title/`.

## Local Development

```bash
bundle install          # first-time setup
bundle exec jekyll serve # build + serve with live reload at http://localhost:4000
```

- [_site/](_site/) is the generated build output — **gitignored, never edit by hand**. Editing it does nothing; change the source files instead.
- `Gemfile.lock`, `.jekyll-cache`, and `.sass-cache` are also gitignored.

## Two Separate Styling Systems (important)

This site does **not** style everything one way. Be careful which one you touch:

1. **Landing page** — [index.markdown](index.markdown) uses `layout: home` → [_layouts/home.html](_layouts/home.html), a fully standalone HTML document that links plain [styles.css](styles.css). It does **not** use the minima theme at all. This is where the games grid, social links, avatar, and newsletter embed live.
2. **Blog & other pages** — [blog.html](blog.html) (`layout: default`) and blog posts (`layout: post`) render through the **minima** theme. Theme variables are overridden in [assets/main.scss](assets/main.scss) and [_sass/minima.scss](_sass/minima.scss) (dark background `#1a1a1a`, white text, etc.).

So: edit `styles.css` for the home page; edit the `*.scss` files for blog/theme pages.

## Blog Posts

- Live in [_posts/](_posts/), named `YYYY-MM-DD-title.md` (Jekyll requires this date-prefixed filename).
- Front matter needs `layout: post`, `title`, and `date`. Example existing posts: `2025-10-10-lokiretro.md`, `2026-01-29-thors-training-timer.md`.
- Posts are long-form Markdown (dev post-mortems, release notes), can embed images from `/images` and inline `<br>`/HTML.
- Published URLs follow `/blog/:title/`. [blog.html](blog.html) auto-lists all posts newest-first with excerpts.

## Images & Assets

- All images live in [images/](images/) and are referenced with absolute root paths, e.g. `/images/owl_avatar.png`.
- Includes game banners, logos, Steam stat screenshots, and social icons (itch.io, YouTube, Bluesky).

## Games Featured

The landing page links out to OWL's games and storefronts:
- **Loki's Revenge** — Norse survivors-like roguelite (Steam app `2936750`, also free on itch.io).
- **Thor's Training Timer** — pomodoro timer idle toy (itch.io).
- Social/store presence: itch.io (`owlmakesgames`), YouTube (`@OwlGameDev`), Bluesky (`owlgamedev.bsky.social`).

## Conventions & Notes

- Voice is first-person as OWL. Blog writing is candid and personal — match that tone when drafting or editing post content.
- New games are added as `<a>`/`<img>` entries inside the `.game-grid` in [_layouts/home.html](_layouts/home.html).
- To add a blog post: create a properly dated file in `_posts/` with the `post` layout — no other wiring needed; it appears in the blog index automatically.
