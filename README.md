# CSEHY Fundraising - GitHub Pages site

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