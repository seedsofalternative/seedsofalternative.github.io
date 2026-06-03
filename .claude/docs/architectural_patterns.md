# Architectural Patterns

Patterns observed in 3+ files. Follow these when editing or extending the site.

---

## 1. Implicit loop variable in includes

`_includes/postbox.html` and `_includes/featuredbox.html` receive no parameters — they rely on a `post` variable already set by the caller's `{% for post in ... %}` loop.

Used in: `index.html`, `_layouts/archive.html`, `_layouts/categories.html`, `_layouts/tags.html`.

**Convention**: don't add parameters to these includes. If you need a variant, follow the same implicit-variable approach.

---

## 2. Manual-parameter includes (exceptions to rule 1)

Two includes are called with explicit Liquid parameters from post body content:

- `{% include image.html url="..." description="..." %}` — `_includes/image.html`
- `{% include youtubePlayer.html id=page.youtubeId %}` — `_includes/youtubePlayer.html`

All other includes use implicit context variables, not params.

---

## 3. Author resolution

Every component that displays author info follows the same pattern before rendering:

```liquid
{% assign author = site.authors[post.author] %}
```

Author data (name, gravatar, description) lives in `_config.yml` under `authors:`. Used in `_includes/postbox.html`, `_includes/featuredbox.html`, `_layouts/post.html`.

---

## 4. Lazy image loading toggle

Every image in a layout or include is wrapped in a conditional:

```liquid
{% if site.lazyimages == "enabled" %}
  <img class="lazyimg" data-src="..." ...>
{% else %}
  <img src="..." ...>
{% endif %}
```

Toggle via `lazyimages: "enabled"` in `_config.yml`. Used in `_layouts/post.html`, `_includes/postbox.html`, `_includes/featuredbox.html`.

---

## 5. Absolute vs relative image URL

Image paths in front matter can be either a relative asset path (`assets/images/...`) or an external URL. All three image-rendering locations guard with:

```liquid
{% if post.image contains "://" %}{{ post.image }}{% else %}{{ site.baseurl }}/{{ post.image }}{% endif %}
```

Same files as pattern 4.

---

## 6. Comments opt-out

Disqus is included conditionally in `_layouts/post.html` and `_layouts/page.html`:

```liquid
{% if page.comments != false %}{% include disqus.html %}{% endif %}
```

- Posts: comments **on** by default (omit `comments` front matter key).
- Pages: comments **off** by default (`comments: false` in front matter).

---

## 7. Post front matter schema

All 18 posts follow this schema:

**Required**
```yaml
layout: post
title: "…"
author: pierre
categories: [ psychology ]   # single category array
image: assets/images/topic/cover.jpg
```

**Optional**
```yaml
featured: false          # suppress from featured slot on index
rating: 4                # 1–5 stars; renders via _includes/star_rating.html
toc: true                # auto-generate TOC from headings
beforetoc: "…"           # text rendered above the TOC
youtubeId: "abc123"      # used with {% include youtubePlayer.html id=page.youtubeId %}
last_modified_at: YYYY-MM-DD
```

---

## 8. Category page boilerplate

12+ pages in `_pages/` (e.g., `buddhism.md`, `psychology.md`, `society.md`) are structurally identical. Only `title`, `permalink`, and the category name in the loop differ:

```yaml
---
layout: page
title: Buddhism
permalink: /buddhism
comments: false
---
```

Body: Bootstrap `col-md-8` grid + `{% for post in site.categories.buddhism %}` list.

When adding a new category page, copy an existing one and change those three values.
