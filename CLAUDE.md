# Seeds of Alternative — CLAUDE.md

## Project overview

Personal blog at [seedsofalternative.com](https://seedsofalternative.com) covering Buddhism, Psychology, spirituality, sustainability, and conscious living. Single author (pierre), ~18 posts, ~28 pages. Deployed automatically via GitHub Pages on push to `main`.

## Tech stack

- **Jekyll** (latest) + **GitHub Pages**
- **Theme**: Mediumish Bootstrap Jekyll — base templates in `_layouts/`, components in `_includes/`
- **Markdown**: kramdown with GFM input; syntax highlighting via Rouge
- **Plugins**: `jekyll-paginate` (6/page), `jekyll-sitemap`, `jekyll-feed`, `jekyll-seo-tag`, `jekyll-archives`
- **Search**: Lunr.js — `assets/js/lunr.js`, `_includes/search-lunr.html`
- **Comments**: Disqus — `_includes/disqus.html`
- **Analytics**: Umami — injected in `_layouts/default.html`
- **Feature flags**: `site.lazyimages`, `site.adsense` in `_config.yml`

## Key directories

| Path | Purpose |
|------|---------|
| `_posts/` | Blog posts, named `YYYY-MM-DD-title.md` |
| `_pages/` | Static pages: about, category indexes, location pages |
| `_layouts/` | Page templates: `default`, `post`, `page`, `archive`, `categories`, `tags` |
| `_includes/` | Reusable Liquid components (postbox, toc, share, star_rating, disqus, …) |
| `_sass/` | SCSS overrides layered on top of theme; `assets/css/main.scss` is the entry point |
| `assets/` | CSS, JS, fonts, images (images organised by topic under `assets/images/`) |
| `_config.yml` | Site config, author data, plugin settings, feature flags |

## Build / run

```bash
# Bundler
bundle exec jekyll serve --watch

# Docker
docker-compose up
```

Site served at `http://localhost:4000`.

## Adding a post

Create `_posts/YYYY-MM-DD-slug.md`. Required front matter fields: `layout`, `title`, `author`, `categories`, `image`. See `.claude/docs/architectural_patterns.md` for the full front matter schema and optional fields.

## Additional documentation

| File | When to check |
|------|--------------|
| `.claude/docs/architectural_patterns.md` | Before editing includes, layouts, or adding posts — covers include conventions, image handling, front matter schema, comments opt-out, author resolution, and category page boilerplate |
