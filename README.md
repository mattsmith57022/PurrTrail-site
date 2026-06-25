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

Deployment notes live in `docs/development/static-site-deployment.md`. The GitHub Pages workflow deploys this folder only after the generator and metadata validator pass.

Use `scripts/release_preflight.sh --full --live` before final App Store submission to verify the generated site, DNS, live URLs, and support mail readiness together.
