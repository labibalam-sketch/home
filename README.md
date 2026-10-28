# Labib Alam — Static Portfolio Website

Editorial-luxury, warm-white personal brand website for GitHub Pages.

## Included
- `index.html` — single-page portfolio and content structure
- `assets/styles.css` — responsive styling
- `assets/script.js` — mobile navigation and dynamic copyright year
- `assets/favicon.svg` — monogram favicon
- `CNAME` — custom domain `labibalam.co.in`
- `robots.txt` and `sitemap.xml` — basic crawl configuration
- `.nojekyll` — prevents GitHub Pages Jekyll processing

## Before launch: content and rights checklist
This starter uses remote Unsplash images as visual placeholders and a generic portrait placeholder. Replace them with approved project photographs, your own portrait and final book-cover artwork. Confirm you have publication rights for every image and confirm project descriptions, attribution and your role before publishing.

The site includes a few professional details based on the supplied brief and prior conversation context. Review the biography and experience wording before launch. The “25+ years” claim reflects wording previously used in your professional positioning; use it only if it accurately represents your total professional experience.

Book covers are CSS mockups, not the final published covers. Add verified purchase URLs and contact details when available.

## Publish using GitHub Pages

1. Sign in to GitHub and create a new repository, e.g. `labibalam-website`.
2. For the simplest setup, set the repository to **Public**. GitHub Pages availability and limits depend on your account and repository settings.
3. Upload all files and folders in this package to the repository root. Keep `index.html`, `CNAME`, `robots.txt`, `sitemap.xml` and `.nojekyll` at the root.
4. Open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select branch `main` and folder `/(root)`, then save.
7. Wait for the Pages deployment to complete. Test the GitHub-provided URL before connecting the custom domain.

## Connect `labibalam.co.in` safely

Do not change nameservers or delete existing DNS records just to publish the website. First inspect the current DNS zone and record all existing MX, TXT, SPF, DKIM, DMARC, verification and other records. This is especially important if you later configure domain email.

At the domain's current DNS provider, add the following records for the apex/root domain (`@`) when ready:

| Type | Name | Value |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| AAAA | `@` | `2606:50c0:8000::153` |
| AAAA | `@` | `2606:50c0:8001::153` |
| AAAA | `@` | `2606:50c0:8002::153` |
| AAAA | `@` | `2606:50c0:8003::153` |
| CNAME | `www` | `YOUR-GITHUB-USERNAME.github.io` |

Use the exact DNS values recommended by GitHub's current Pages documentation at the time of setup. If your DNS provider does not support AAAA records or if GitHub's documentation differs, follow GitHub's current instructions. Do not create a CNAME at `@` alongside apex A/AAAA records. If `www` already has a record, review it before replacing it.

Then in GitHub: **Repository → Settings → Pages → Custom domain**, enter `labibalam.co.in` and save. Keep the root `CNAME` file in the repository. Once DNS has propagated and GitHub verifies the domain, enable **Enforce HTTPS** when the option becomes available.

### DNS safety notes
- Do not delete MX records; those control incoming email.
- Preserve TXT records for SPF, DKIM, DMARC and domain verification.
- Avoid changing nameservers unless you deliberately intend to migrate the entire DNS zone.
- DNS propagation can take time. Verify with your DNS provider and GitHub Pages status.
- Do not enable HTTPS until GitHub has finished checking the custom domain and certificate.

## Updating content
- Edit text in `index.html`.
- Change colours, spacing and responsive layouts in `assets/styles.css`.
- Update external profile URLs in `index.html` if your profile URLs differ.
- Replace the image URLs in `index.html` with your own image files, for example `assets/projects/project-name.jpg`.
- Add descriptive alt text to all meaningful images.
- Keep project-specific case studies truthful and publication-cleared.

## Functional scope
This is a static website. It does not include a server, CMS, database, login, checkout, or email form backend. For payments, book sales or enquiry forms, connect a reputable external service and test its privacy and payment requirements before launch.
