# Grey Lunk Portfolio

Static portfolio for Grey Lunk, developed from the Start Bootstrap Creative template. GitHub Pages is enabled from `main` at the repository root with the custom domain `greylunk.com`; Spaceship DNS is configured, and HTTPS certificate provisioning is pending. The current pages use local assets with no external runtime dependencies or scripts. No installation or build step is required.

## Edit and preview

- `index.html`: portfolio homepage
- `ergo-mk1.html`, `heartline.html`, `pl4y.html`, `deadlink.html`: four project pages
- `css/portfolio.css`: custom portfolio styling; make design changes here rather than in the retained vendor file `css/styles.css`
- `assets/portfolio/`: optimized project images extracted from the supplied portfolio PDF
- `assets/favicon.svg`: portfolio favicon
- `CNAME`: custom domain for GitHub Pages
- `.nojekyll`: serves the static files without Jekyll

Open `index.html` in a browser to preview, then follow its project links. Edit text directly in the HTML files. To change an image, replace its local file or update the relevant `src` and descriptive `alt` text; keep image sizes reasonable for mobile visitors.

The four projects are based on the supplied portfolio PDF. Preserve the PL4Y team credit when editing. No email address was supplied, so the portfolio intentionally has no email link or contact form.

After checking your changes locally, stage only the intended files, commit, and push to `main`. For example, from this repository folder:

```powershell
git add -- index.html ergo-mk1.html heartline.html pl4y.html deadlink.html css/portfolio.css assets/portfolio assets/favicon.svg README.md .gitignore
git commit -m "Update portfolio"
git push origin main
```

Review `git diff --cached` before committing. GitHub Pages deploys changes pushed to `main` automatically. Keep `CNAME` and `.nojekyll` in the repository; add them explicitly if you intentionally change them. `.gitignore` excludes local PDF inspection and image preparation artifacts.

## Publish with GitHub Pages

1. Push the site files to the root of the `main` branch in [OhR4tz/Portfolio](https://github.com/OhR4tz/Portfolio).
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
