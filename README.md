# auskf-jrnationals.github.io

The official website for the AUSKF Jr. Open National Kendo Championships, powered by GitHub Pages and Jekyll. Please visit [www.auskf-jrnationals.com][1] for more information on this event.

Design adapted from Twenty by [HTML5 UP][2], free for personal and commercial use under the [CCA 3.0 license][3].

## Running locally with Jekyll

```bash
bundle install
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`. Jekyll will watch for changes and rebuild automatically.

## Year-to-year updates

Almost all tournament-specific content (dates, venue, fees, deadlines) is centralized in `_config.yml`. Update the variables there and the changes propagate across the site automatically.

## Updating page content

| Page | File |
|------|------|
| Home | `index.md` |
| Info | `info.md` |
| Past Results | `past.md` |

## Showing/hiding nav links

Navigation is hardcoded in `_includes/header.html`. Links for Register, Schedule, Brackets, and Results are commented out by default and should be uncommented as the tournament progresses through its lifecycle.

[1]: https://www.auskf-jrnationals.com
[2]: https://html5up.net
[3]: https://html5up.net/license
