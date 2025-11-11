<!-- Auto-generated guidance for AI coding assistants working on this repository -->
# Copilot instructions for csehy-fundraising

Short, actionable notes to help an AI editing or generating code/content in this repo.

- Project type: Jekyll static site (GitHub Pages). See `_config.yml` for site metadata and collection settings.
- Base URL: `baseurl: "/csehy-fundraising"` — layouts use `| relative_url` throughout to build correct URLs for project pages.

Key files and what they mean
- `_config.yml` — site-wide config. Important: the `performers` collection is enabled and outputs pages with `permalink: /performers/:name/`.
- `index.md` — home page; uses `site.data.performers` to render the preview list of performers.
- `_data/performers.yml` — YAML array used by the home page preview. Keep this in sync with the performers you want highlighted on the home page.
- `_performers/*.yml` — collection items that render individual performer pages. These are full pages (layout: `performer`) and are available under `/performers/`.
- `_layouts/performer.html` and `_layouts/default.html` — templates. Use `{{ '/assets/images/' | append: page.photo | relative_url }}` for images to respect `baseurl`.
- `performers/index.md` — list page that iterates `site.performers` (the collection) and links to each performer's generated page.
- `assets/images/` — place performer photos here (refer to them by filename in `photo:` front matter).

Project-specific conventions and gotchas
- Two sources of truth for performers:
  - `_data/performers.yml` — used by the home page preview (index.md loops `site.data.performers`).
  - `_performers/` collection — full performer pages; `performers/index.md` loops `site.performers`.
  When adding a new performer you often need to update both places if you want them to appear on the home preview and have a full page.
- Performer front matter keys (used in layouts): `layout: performer`, `title`, `name`, `instrument`, `photo`, `bio`, `media_url`.
  - Example front matter (YAML):
    ---
    layout: performer
    name: "Jane Doe"
    instrument: "Piano"
    photo: "jane.jpg"
    bio: >
      Short multiline bio here.
    media_url: ""
    ---
- URL/permalink behavior: `_config.yml` sets `permalink: /performers/:name/`. The `:name` value comes from the page's `name` front matter and will be slugified by Jekyll — ensure `name` values are unique.
- Use `relative_url` filter in templates (already present) so generated links work both on GitHub Pages (with `baseurl`) and locally.

Local dev & deployment notes (discoverable behavior)
- This repository is intended for GitHub Pages. To preview locally you can use Jekyll (if you have Ruby and Bundler):

  # if you have Ruby/Bundler set up
  bundle exec jekyll serve

  The repository does not include a Gemfile; if you need reproducible local builds, add one with the `jekyll` and theme gems you prefer.
- To publish: use GitHub repository Settings → Pages and point to `main` branch / root (README documents this).
- If you want a custom domain, rename `_CNAME.disabled` to `CNAME` and add your domain (also set DNS). The README documents this workflow.

When making edits or PRs
- Content edits: prefer updating the existing YAML files and markdown pages (`index.md`, files under `_performers/`, `_data/performers.yml`).
- Styling: small CSS changes live in `assets/css/style.css`.
- Media: add images under `assets/images/` and reference only the filename in front matter.

Examples of small tasks an AI may be asked to do
- Add a new performer: create `_performers/new-performer.yml` with the front matter above and add a corresponding entry in `_data/performers.yml` if you want them on the home preview.
- Change donate link: update `index.md` where the donate button `href` is set.
- Improve performer card markup: edit `_layouts/default.html` or `performers/index.md`; remember to use `relative_url` when referencing assets.

If anything here is unclear or you'd like extra detail (example PRs, a local Gemfile, or tests), tell me what to add and I will update this file.
