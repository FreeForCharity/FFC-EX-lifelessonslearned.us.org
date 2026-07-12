# FFC-EX-lifelessonslearned.us.org

Life Lessons Learned, Inc. — FFC-supported charity website (static, GitHub Pages).

This repository holds a fully localized static capture of the site at
`lifelessonslearned.us.org` (previously WordPress on Hostinger), migrated as part of
the FFC Wave-1 WordPress-to-Pages program
([FFC-Cloudflare-Automation#702](https://github.com/FreeForCharity/FFC-Cloudflare-Automation/issues/702)).

## Important: source site was in maintenance mode

At capture time (2026-07-12) the WordPress site served its
"SOMETHING NEW IS COMING SOON!" maintenance page (CMP Coming Soon plugin) on
**every** route — the 18 URLs in its sitemap all returned the identical
coming-soon page. This repository therefore faithfully reproduces the single
public page that visitors actually saw, including its background video. The
underlying WordPress page content was never publicly reachable and could not be
captured. See the migration tracking issue for follow-up options.

## Hosting

- Deployed to GitHub Pages on the default URL:
  <https://freeforcharity.github.io/FFC-EX-lifelessonslearned.us.org/>
- Deployment runs from `.github/workflows/static.yml` on every push to `main`.
- No custom domain and no DNS changes are configured at this stage.

## Structure

Plain static HTML — no build step. A single page (`/`) with:

- Background video (`wp-content/uploads/2023/03/lllt1.mp4`, served locally)
- Localized Google Fonts (`wp-content/ffc-local-fonts/`)
- Coming-soon theme CSS/JS served from this repository

External font, CDN, and analytics hosts were localized or stripped during
migration. The dead subscribe form script (posted to the removed WordPress
backend) and an unused Font Awesome CDN stylesheet were removed.

## Maintenance

- Edit the HTML in place; every push to `main` redeploys.
- `linkcheck.yml` runs lychee weekly and on pushes/PRs to catch link rot.

---

Supported by [Free For Charity](https://freeforcharity.org).
