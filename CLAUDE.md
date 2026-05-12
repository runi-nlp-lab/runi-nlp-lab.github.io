# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
bundle install                  # install Ruby gem dependencies
bundle exec jekyll serve        # local dev server at http://localhost:4000
bundle exec jekyll build        # build to _site/
```

The `_site/` directory is the generated output — never edit files there directly.

## Architecture

This is a **Jekyll static site** using the [Alembic](https://github.com/daviddarnes/alembic) remote theme (`daviddarnes/alembic@main`). There are no custom layouts or `_layouts/` — all layout is inherited from the remote theme.

### Key files

| File | Purpose |
|------|---------|
| `_config.yml` | Site-wide settings: URL, title, nav links, plugins, default layout |
| `_includes/custom_style.html` | CSS overrides for lab brand colors — included on every page |
| `index.md` | Home page with research areas |
| `team.md` | Team members grid (PhD, Master's, Former) |
| `publications.md` | Publication list by year |
| `contact.md` | Contact page |
| `members_pics/` | Member photos (JPEG/JPG) |
| `assets/` | Logos (`logo.png`, `logo_below.png`, `logo_side.png`) and social icons |

### Brand colors

- Primary (dark blue): `#1b258a`
- Accent (lavender): `#abb0e4`

All pages must include `{% include custom_style.html %}` at the top of the body to apply brand colors — without it the Alembic theme defaults apply.

### Navigation

Defined in `_config.yml` under `navigation_header`. Adding a new top-level page requires both creating the `.md` file and adding an entry there.

### Member cards pattern

Team members use a 3-column CSS grid with inline styles. Each card follows:

```html
<div class="member-card">
  <img src="/members_pics/<filename>" alt="Name"
       style="width: 100%; aspect-ratio: 1/1; object-fit: cover; border-radius: 8px;">
  <h4 style="font-size: 1em; margin: 10px 0 5px 0; letter-spacing: -0.01em;">
    <a href="<profile-url>">Name</a>
  </h4>
  <p>Role</p>
</div>
```

Photos go in `members_pics/`. The `onerror` fallback to `/assets/logo.png` is used on the director's photo only.
