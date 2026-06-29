# Whistle Static Demo Pages

Open the hosted demo site here:

https://glitch-ops-dump.github.io/whistle-demo-pages/

Use the hosted GitHub Pages URLs above, not the GitHub repository file viewer. GitHub's code viewer does not execute these `.demo.html` files, and some generated app files are large enough that GitHub shows "we can't show files that are this big right now."

These pages are generated browser-local demonstrations for the MVP1 app surfaces:

- `index.html`
- `citizen.demo.html`
- `verification.demo.html`
- `mla.demo.html`
- `ministry.demo.html`
- `cm-cell.demo.html`
- `admin.demo.html`

Each `.demo.html` page is generated from the real standalone app export under `exports/standalone/` and then watermarked with `SAMPLE DATA - DEMO ONLY`. The demo files should look like the actual app surfaces; the watermark is the only intentional visual addition.

The demo pack is intended for GitHub Pages-style static hosting only. It must stay sample-data-only, noindex, unaffiliated with any government or official service, and disconnected from production, staging, uploads, OTP providers, analytics, and live APIs.

Direct hosted links:

- Citizen Mobile PWA: https://glitch-ops-dump.github.io/whistle-demo-pages/citizen.demo.html
- Verification Console: https://glitch-ops-dump.github.io/whistle-demo-pages/verification.demo.html
- MLA Dashboard: https://glitch-ops-dump.github.io/whistle-demo-pages/mla.demo.html
- Minister Dashboard: https://glitch-ops-dump.github.io/whistle-demo-pages/ministry.demo.html
- CM Cell Dashboard: https://glitch-ops-dump.github.io/whistle-demo-pages/cm-cell.demo.html
- Admin Console: https://glitch-ops-dump.github.io/whistle-demo-pages/admin.demo.html

Regenerate after changing app UI:

```bash
npm run build
npm run export:all
npm run export:demo-pages
```

Run the guardrail check after regenerating:

```bash
npm run smoke:demo-pages
```
