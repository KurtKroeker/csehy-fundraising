# Csehy Fundraising - GitHub Pages site

This repository contains a minimal Jekyll scaffold for a mostly-static website to promote a benefit concert raising funds for four young musicians. The site is designed for GitHub Pages hosting.

## What is included

- Basic Jekyll config (`_config.yml`)
- Home page (`index.md`) that pulls performer data from `_data/performers.yml`
- Simple layout (`_layouts/default.html`) and responsive CSS (`assets/css/style.css`)
- Sample performer data in `_data/performers.yml`

## How non-developers can edit content

Edit content directly in the GitHub web UI. Files to edit:

- `index.md` — for hero text, event date/venue, donate link
- `_data/performers.yml` — to update performer names, bios, and photo filenames
- `assets/images/` — upload performer photos via the web UI (use the same filenames referenced in `_data/performers.yml`)
- `assets/css/style.css` — basic styling (developer help recommended)

### Quick editing steps in GitHub web UI

1. Open the repository on GitHub.
2. Navigate to the file you want to edit (for example `_data/performers.yml`).
3. Click the pencil icon to edit the file.
4. Commit changes directly to the `main` branch or create a PR if you want review.

## GitHub Pages setup

1. In the repository Settings > Pages, set the source branch to `main` and the folder to `/ (root)`.
2. If you want a custom domain, add a `CNAME` file at the repository root with your domain (example: `concert.example.com`) and follow your DNS provider instructions to point the domain to GitHub Pages.
3. Wait a few minutes for GitHub to build the site. Your site will be available at:
   - https://KurtKroeker.github.io/csehy-fundraising (project page) or
   - https://yourcustomdomain (if using CNAME and DNS configured)

## Local preview (Windows)

This repository includes a minimal `Gemfile` to make local Jekyll builds reproducible. Two simple ways to preview the site locally on Windows are shown below.

Native Ruby + Bundler (PowerShell)

1. Install Ruby for Windows (RubyInstaller) and the MSYS2 toolchain when prompted.
2. From the project root open PowerShell and run:

```powershell
gem install bundler
bundle install
```

3. Serve the site. Because `_config.yml` sets `baseurl: "/csehy-fundraising"` you can either serve with that baseurl (the site will be available at http://127.0.0.1:4000/csehy-fundraising/) or override it locally to preview at root:

```powershell
# serve with baseurl (final path includes /csehy-fundraising/)
bundle exec jekyll serve --livereload

# or serve at root for easier local preview (no suffix)
bundle exec jekyll serve --livereload --baseurl ""
```

Docker (no Ruby install)

If you have Docker Desktop, run this from the project root in PowerShell:

```powershell
docker run --rm -it -v ${PWD}:/srv/jekyll -p 4000:4000 jekyll/jekyll:4 jekyll serve --watch --baseurl ""
```

Open http://127.0.0.1:4000 in your browser (append `/csehy-fundraising/` if you served with the baseurl).

Notes
- The `Gemfile` in the repository pins `jekyll` and `webrick` for local development.
- Ensure images referenced in `_data/performers.yml` and `_performers/*.yml` exist in `assets/images/`.

## Content checklist before launch

- Hero image and/or logo (place in `assets/images/`)
- Flyer PDF (optional)
- Event date/time and venue details
- Contact email for RSVPs
- Four performer photos and short bios
- Donation page URL (replace the placeholder in `index.md`)

## Next improvements I can generate for you

- Add individual performer pages (collection) and a performers listing page
- Add an RSVP form (Google Forms, Formspree) and an embeddable or linked RSVP
- Add social meta tags / structured data (Event Schema) & analytics
- Create an editor guide or short walkthrough video