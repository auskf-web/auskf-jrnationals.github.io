# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve

# Build site (output to _site/)
bundle exec jekyll build
```

The site runs at `http://localhost:4000` by default.

## Architecture

This is a static Jekyll site for the AUSKF Jr. Open National Kendo Championships, deployed via GitHub Pages.

**Tournament configuration** is centralized in `_config.yml`. Almost all year-to-year updates (dates, venue, fees, deadlines) happen there via Liquid variables like `{{ site.tournament_year }}`, `{{ site.tournament_date }}`, `{{ site.venue_address_1 }}`, etc. Pages reference these variables throughout.

**Layouts:**
- `landing-page` — used by `index.html`; includes the hero banner.
- `post` — secondary layout.
- `default` — base layout; no structural wrappers beyond standard page structure.

**Navigation** is hardcoded in `_includes/header.html`. Many nav items are commented out and toggled on/off depending on the stage of the tournament (e.g., Register, Schedule, Brackets, Results, Sponsor are hidden until relevant).

**Page lifecycle pattern:** Pages like `register.html`, `schedule.html`, `brackets.html`, `sponsor.html`, and `travel.html` exist but are linked/unlinked from the nav by commenting/uncommenting entries in `header.html`.

**Assets:** `assets/banner.jpg` is the hero image. PDFs (brackets, results, welcome letters) are stored in `assets/` named by year (e.g., `2026-Results.pdf`).

## HTML pages

Content pages use `.html` (not `.md`) with inline Liquid templating. Key patterns:

**Config flags:**
- `site.venue_determined` — controls whether full venue address is shown or just city/state.
- `site.show_save_the_date` — controls whether a link to `assets/{{ site.tournament_year }}-welcome.pdf` is shown.

**Navigation toggling:** Comment/uncomment `<li>` entries in `_includes/header.html` to show/hide nav links as the tournament progresses through its lifecycle (registration open → schedule posted → brackets live → results posted).
