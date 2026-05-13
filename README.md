# EACAN Website

**East Anglian Children's Anaesthesia Network**  
[www.eacan.org.uk](https://www.eacan.org.uk)

A static website for EACAN — connecting paediatric anaesthetists across the East of England NHS region.

## Structure

This is a single-page static HTML site, hosted on GitHub Pages with a custom domain.

```
index.html          — Main website
CNAME               — Custom domain (www.eacan.org.uk)
.github/
  workflows/
    deploy.yml      — GitHub Actions auto-deploy on push to main
```

## Hosting setup

### GitHub Pages
1. Go to **Settings → Pages** in this repository
2. Set **Source** to `GitHub Actions`
3. Push to `main` — the site deploys automatically

### Custom domain (www.eacan.org.uk)
Add these DNS records with your domain registrar:

| Type  | Name | Value                   |
|-------|------|-------------------------|
| CNAME | www  | `<your-github-username>.github.io` |

Or, to redirect the apex domain (`eacan.org.uk`) to `www`:

| Type | Name | Value             |
|------|------|-------------------|
| A    | @    | 185.199.108.153   |
| A    | @    | 185.199.109.153   |
| A    | @    | 185.199.110.153   |
| A    | @    | 185.199.111.153   |

Then in **Settings → Pages**, set the custom domain to `www.eacan.org.uk` and enable **Enforce HTTPS**.

## Editing the site

All content is in `index.html`. Key sections to update:

- **Hero stats** — update hospital/member counts as needed
- **Hospitals table** — add lead names, actual emails
- **Committee cards** — add committee member names and contact details
- **Annual Meeting banner** — update date and details each year
- **WhatsApp** — update join link if a formal invite link exists

## Contact

Network email: eacan@nhs.net
