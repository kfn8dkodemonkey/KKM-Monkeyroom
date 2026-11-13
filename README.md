# KKM Admin

A Jekyll + Bootstrap launch dashboard for Heather’s independent tools and projects.

## Local use

```sh
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000. This checkout starts from an empty GitHub repository; merge into an existing local Jekyll installation only after reviewing its files.

## Edit links

- `_data/tools.json`: tool name, group, initials, description, and URL.
- `_data/projects.json`: project name, description, and an array of labeled links.
- Add a repository or project board as another entry in a project’s `links` array.
- ClubHub has no confirmed URL yet, so its card displays text rather than a dead link.
- Links open in the same tab; browser controls can open a new tab when desired.
- WEAR-TTProcess uses the HTTP URL supplied by the owner.

## Publish on GitHub Pages

1. Push these files to the `main` branch of `kfn8dkodemonkey/KKM-Admin`.
2. In repository Settings → Pages, choose **Deploy from a branch**, **main**, **/(root)**, then Save.
3. Set Custom domain to `admin.caffeinatedcodemonkey.com` and save.
4. At the DNS provider for **caffeinatedcodemonkey.com**, set CNAME host `admin` to `kfn8dkodemonkey.github.io` (no protocol or repository name). Remove conflicting A/AAAA records for this exact host only; do not change main-site records.
5. When GitHub’s DNS check and certificate provisioning finish, enable **Enforce HTTPS**.
6. Check all dashboard links, keyboard focus, and mobile layout after deployment.

The admin domain is intentionally spelled caffeinatedcodemonkey.com, while some supplied tool URLs use kaffeinatedkodemonkey.com. Preserve those distinct domains.

## Access and indexing

No authentication is included. The dashboard and repository contents can be publicly accessible. Do not store secrets or confidential project details here. Every page using the default layout includes `noindex, nofollow, noarchive`; robots.txt requests no crawling. These are voluntary crawler instructions, not access control or a guarantee of exclusion. A blocked crawler may never see noindex. No sitemap, analytics, or service worker is included.

Stytch access control is deferred to a separate phase; client-only hiding would not protect static files.

## Validation

Run `bundle exec jekyll build` before publishing. The creation environment lacked Ruby/Bundler, so a real Jekyll build must be verified locally or by the GitHub Pages build.
# KKM-Admin
# KKM-Admin
