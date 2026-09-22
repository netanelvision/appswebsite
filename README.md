# NetanelVision apps website

Static HTML and CSS. No JavaScript, package dependencies, analytics, or tracking cookies.

## Edit and preview

Edit page content in `scripts/build.py`, styling in `dist/assets/style.css`.
Run `python3 scripts/build.py`, then `python3 -m http.server 4173 --directory dist`.
Open http://localhost:4173.

Routes: `/`, `/anywarranty/`, `/anywarranty/privacy/`, `/anywarranty/terms/`.
Relative links support both a domain root and the GitHub project prefix.
To add an app, add a `page(...)` call and a homepage entry.

## GitHub Pages

Repository Settings → Pages → Build and deployment → Source: GitHub Actions.
Push to main or manually run the Deploy website workflow.
Default website: https://netanelvision.github.io/appswebsite/
Any.Warranty: https://netanelvision.github.io/appswebsite/anywarranty/
Privacy: https://netanelvision.github.io/appswebsite/anywarranty/privacy/
Terms: https://netanelvision.github.io/appswebsite/anywarranty/terms/

For exact domain-root URLs, use a custom domain in Pages settings or the account repository `netanelvision.github.io`. With a custom domain, update the 404 base path in the build script from `/appswebsite/` to `/` and add `dist/CNAME` containing the domain.

## Google OAuth

Once the site is public, use the Any.Warranty page as the application homepage and the privacy and terms URLs above in Google Auth Platform → Branding. This site hosts information only; it is not an OAuth callback or a replacement for the iOS OAuth client.
Google can require domain ownership verification for branding. Prefer a custom domain you own and can verify in Search Console. A public GitHub Pages URL alone does not guarantee verification approval.
Official guidance: https://developers.google.com/identity/protocols/oauth2/production-readiness/policy-compliance

The policy describes the inspected app's local records, Google Drive app-data backup, Dropbox, iCloud/device backups, and support contact. Keep it updated when app behavior or data practices change. Real app screenshots and a verified App Store listing link can be added later; none are fabricated here.
