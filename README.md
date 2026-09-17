# Dr. Jane Doe — Clinical Psychology Practice Website

A simple, static one-page website: info/about, client success stories, booking (via Calendly), and contact.

## Structure

```
/
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── main.js
├── assets/
│   └── images/     # add headshot.jpg, favicon.png, etc. here
└── README.md
```

No build step is required — this is plain HTML/CSS/JS and can be opened directly
(`index.html` in a browser) or deployed as-is to any static host.

## Before going live — replace these placeholders

1. **Practice / doctor name** — search `index.html` for "Dr. Jane Doe" and replace
   with your real name/title everywhere (title tag, header brand, hero, footer).
2. **Bio & specialties** — edit the hero text in the `#about` section.
3. **Client success stories** — edit the quotes/attributions inside the `#success`
   section (`success-card` blocks). Only use real testimonials with permission,
   and anonymize where appropriate.
4. **Calendly booking widget** — in the `#booking` section, replace
   `https://calendly.com/YOUR-CALENDLY-LINK` with your real Calendly scheduling
   link:
   1. Create a free account at https://calendly.com
   2. Create an event type (e.g. "Consultation — 30 min") and set your availability.
   3. On that event: Share → Add to Website → Inline Embed → copy the link.
   4. Paste it into the `data-url` attribute of the `.calendly-inline-widget` div.
5. **Contact details** — update the email (`mailto:`) and phone (`tel:`) links in
   the `#contact` section.
6. **Images** — add `assets/images/headshot.jpg` and `assets/images/favicon.png`.
   If they're missing, the headshot simply won't render (no broken-image icon).

## Local preview

Just open `index.html` in a browser, or serve it locally, e.g.:

```bash
npx serve .
```

## Deployment (Cloudflare Pages, free)

1. Push this repo to GitHub.
2. In the Cloudflare dashboard: **Pages → Create a project → Connect to Git**,
   select this repo. No build command is needed — leave the output directory
   as the repo root (`/`).
3. Deploy. Cloudflare gives you a free `*.pages.dev` URL immediately.

## Connect your GoDaddy domain

1. In Cloudflare, add your domain as a new site (free plan) — this gives you
   two nameservers.
2. In GoDaddy: **My Domains → DNS → Nameservers** → change from GoDaddy's
   default nameservers to the two Cloudflare nameservers.
3. Wait for propagation (usually a few hours, sometimes up to 24–48h).
4. Back in your Cloudflare Pages project: **Custom domains → Add a domain**,
   enter your domain (and `www` if desired). Cloudflare will provision DNS
   records and a free SSL certificate automatically.
5. Visit your domain over HTTPS to confirm everything (including the Calendly
   widget) works end-to-end.
