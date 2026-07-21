# enveloop.io

Marketing site for Enveloop — a Google Workspace add-on that mail merges Google Sheets data into ready-to-print labels. Plain HTML/CSS/JS, no build step, no backend.

Pages: `index.html` (home), `pricing.html`, `support.html`, `privacy-policy.html`, `terms-of-service.html`.

## Before publishing

- **Payment processor** — `privacy-policy.html` and `terms-of-service.html` currently name Stripe as the payment provider and a 30-day refund window. Update both if you end up using a different provider or policy.
- **Install link** — all "Get notified at launch" CTAs currently point to a `mailto:` placeholder. Once Enveloop has a live install listing, swap these for the real install URL and update the button copy (e.g. "Install Enveloop").

Also review `privacy-policy.html`'s Google API Services User Data Policy section once the add-on's actual OAuth scopes are finalized — the current text is a reasonable starting template but should get a lawyer/compliance pass before the add-on goes live, since it governs real user data collected through Google APIs.

Update the "Effective date" line in both legal files whenever you materially change the policy/terms text.

## Deploy

Any static host works (Netlify, Vercel, GitHub Pages, S3, or your own web server) — just upload the folder as-is. To preview locally:

```
python3 -m http.server 8000
```

Then open http://localhost:8000
