# Tisserin Group

Static company website for owner representation, development management, construction oversight, commissioning, and asset operations.

## Project

- `dist/index.html`: website content, styling, and lifecycle interactions.
- `dist/hero.jpg`: architectural photograph.
- `netlify.toml`: Netlify deployment configuration.

No installation or build command is required. The `dist` folder is the finished website and must be committed to GitHub.

## Push to GitHub

Create an empty GitHub repository named `tisserin-group`, without generating a README or .gitignore. Open a terminal in this folder, then run:

```sh
git remote add origin https://github.com/YOUR-USERNAME/tisserin-group.git
git push -u origin main
```

Replace YOUR-USERNAME with your GitHub username. Sign in when prompted. This export is a separate repository; it contains no credentials or previous Sites deployment configuration.

## Deploy with Netlify

1. Sign in at https://app.netlify.com/.
2. Choose Add new project / Import an existing project and connect GitHub.
3. Select the `tisserin-group` repository and the `main` branch.
4. Leave the base directory and build command empty. Publish directory: `dist` (also supplied by netlify.toml).
5. Deploy and review the assigned `*.netlify.app` URL, including mobile layout and all lifecycle tabs.
6. Test the Contact Us form and check that the inquiry reaches the destination inbox. FormSubmit might request confirmation for the new site origin; complete it if prompted.

Future pushes to the connected production branch will trigger Netlify deployments.

## Connect tisseringroup.com

First verify the Netlify deployment. Then add `tisseringroup.com` and `www.tisseringroup.com` in Netlify Domain management. Use the exact DNS instructions shown for this Netlify site.

In GoDaddy, replace the old root A records (`162.159.143.30` and `172.66.3.26`) with the record(s) Netlify specifies. Update `www` to the exact Netlify CNAME target. Keep nameservers, MX records, and unrelated TXT records intact. Old `_openai-site-verification` and `_cf-custom-hostname` TXT records are no longer needed after the migration is confirmed.

Allow DNS to update, then confirm Netlify has issued the HTTPS certificate and that both domain variants load correctly. Keep the existing hosted site available until the switch is verified.

## Contact form

The form uses FormSubmit to deliver inquiries to the previously configured inbox. The email address is not displayed as page text or a mail link, but appears in the public form endpoint in the HTML source. No email credentials are stored in this project. Keep the honeypot and default CAPTCHA enabled. FormSubmit handles submission confirmation; this site does not claim an email was delivered before the provider accepts it.

## Image attribution

Photograph by Vlad Ion on Unsplash:
https://unsplash.com/photos/modern-architectural-buildings-under-construction-and-completed-PC3PdgD82jY
License: https://unsplash.com/license

## References

- Netlify Git deployment: https://docs.netlify.com/deploy/create-deploys/
- Configuration: https://docs.netlify.com/build/configure-builds/file-based-configuration/
- Domains: https://docs.netlify.com/manage/domains/get-started-with-domains/
