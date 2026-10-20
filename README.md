# WorkAtlas Consult website

Static website for WorkAtlas Consult Limited. Built as a single-page, multi-section HTML/CSS/JavaScript site and suitable for version control in GitHub.

## Run locally

Open `index.html` in a modern browser, or run a local static server from this directory, for example:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish with GitHub Pages

1. Create a GitHub repository for the website.
2. Upload `index.html`, `README.md`, and `.nojekyll` to the repository root.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**, choose `main` and `/ (root)`, then save.
5. Wait for GitHub Pages to publish the site and test the published URL on desktop and mobile.
6. For a custom domain, configure the domain in Pages and set the DNS records required by GitHub. Enable HTTPS after DNS verification.

## Production launch checklist

This repository contains the public-facing static website. GitHub Pages serves static files; it does not provide a secure application server or database.

Before treating all features as production-ready:

- **Contact and career forms:** currently open the visitor's email application using `mailto:`. They do not submit directly to a server, reliably store submissions, or upload CVs. Connect them to a trusted form service or secured backend and test spam protection, validation, delivery, retention and access controls.
- **Employee login:** currently a presentation-only sign-in screen. No authentication is performed and no credentials are sent or stored. Do not enter real credentials. Connect a real identity provider or secure backend before offering employee access. Never put passwords, API secrets, or privileged credentials in this repository or client-side JavaScript.
- **Sample team and testimonials:** replace illustrative names, biographies, avatars, testimonials and any sample client marks with verified, approved content before public launch. Do not present invented endorsements as genuine.
- **Privacy and cookies:** verify that the site's actual cookie behaviour matches its notice and preferences. Have the responsible privacy/legal reviewer approve the final notice and retention practices.
- **Quality checks:** test all navigation, links, forms, keyboard access, mobile layouts, reduced-motion settings, page performance and browser console errors. Confirm contact details and brand assets are approved.
- **Operations:** enable HTTPS, choose an owner for updates, review dependencies (if added), and establish a backup/release process.

## Updating the site

Edit `index.html`, commit the change, and push to the configured branch. GitHub Pages will publish the new static files after its build completes. Keep changes in small commits so previous versions can be restored.
