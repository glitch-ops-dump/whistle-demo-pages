# Whistle Static Demo Pages

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
