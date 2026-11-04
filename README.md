# Grey Lunk Portfolio

Static Start Bootstrap Creative template prepared for GitHub Pages at `greylunk.com`. No installation or build step is required. The site has not yet been published.

## Edit and preview

- `index.html`: page content and sections
- `css/styles.css`: styling
- `js/scripts.js`: navigation and image lightboxes
- `assets/`: images and favicon
- `CNAME`: custom domain for GitHub Pages
- `.nojekyll`: serves the static files without Jekyll

Open `index.html` in a browser to preview. The template still contains placeholder content, and its contact form cannot send messages until the `API_TOKEN` placeholder is configured with the form provider.

## Publish with GitHub Pages

1. Upload or push these files to the root of the `main` branch in [OhR4tz/Portfolio](https://github.com/OhR4tz/Portfolio).
2. In the repository, open **Settings → Pages**. Select **Deploy from a branch**, then **main** and **/(root)**, and save.
3. Set the custom domain to `greylunk.com` and save before changing DNS.
4. In Spaceship's DNS settings for `greylunk.com`, add these records using automatic/default TTL:

   | Type | Host | Value |
   | --- | --- | --- |
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |
   | CNAME | www | OhR4tz.github.io |

   Replace only conflicting web/parking records for `@` or `www`. Preserve email records such as MX and TXT. The `www` target must not include `/Portfolio`.
5. Wait for GitHub's DNS check and certificate provisioning, then enable **Enforce HTTPS** in Pages settings. DNS and HTTPS availability can take up to 24 hours.

See [GitHub's custom domain guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) for current configuration details.
