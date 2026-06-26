# PurrTrail Release Site

This folder contains generated static pages for the required App Store support, privacy, and marketing URLs.

Do not edit generated HTML, CSS, `404.html`, `robots.txt`, `sitemap.xml`, `CNAME`, or `.nojekyll` manually. Update the source Markdown in `release/app-store/en-US/`, then run:

```sh
scripts/generate_release_site.rb
```

Check that committed generated files match the source drafts with:

```sh
scripts/generate_release_site.rb --check
```

The site is static only. Do not add backend code, analytics, ads, account flows, comments, public maps, or server sync here.

Deployment notes live in `docs/development/static-site-deployment.md`. In the current private-source setup, publish this generated folder to the public static site repository with `scripts/publish_release_site_repo.sh`.

Use `PURRTRAIL_DEVELOPMENT_TEAM=TEAMID scripts/release_preflight.sh --full --screenshots --live --signing` before final App Store submission to verify the generated site, App Store screenshot set, public Pages configuration, exact GitHub Pages DNS, live URLs, support mail, and local signing readiness together.
