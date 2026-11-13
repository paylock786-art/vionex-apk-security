# Vionex APK Security & Download Portal

Official Vionex CRM Android download landing page.

- Website source: `index.html`
- Security instructions: [SECURITY.md](SECURITY.md)
- Official APK releases: https://github.com/paylock786-art/vionex-crm-releases/releases

## GitHub Pages
This repository includes a Pages deployment workflow. Open **Settings → Pages** and select **GitHub Actions** as the build/deployment source if prompted. The site URL will be shown there after the first successful deployment.

## Automatic VirusTotal APK audit

A scheduled/manual GitHub Actions workflow (`.github/workflows/security-audit.yml`) downloads the latest APK from the official releases repository, submits it to VirusTotal, waits for analysis, records SHA-256 + detection statistics, and uploads `security-report.json` as a workflow artifact.

### Required repository secret (one-time)
1. Open **Settings → Secrets and variables → Actions → New repository secret**.
2. Name: `VIRUSTOTAL_API_KEY`
3. Value: paste your VirusTotal API key privately (never commit it to files or chat).
4. Save. Then open **Actions → Vionex APK Security Audit → Run workflow**.

Audit workflow runs every 6 hours as well. Reports are available under the completed run's **Artifacts** and Summary. VirusTotal detections are signals, not a guarantee of safety or WhatsApp/Play Protect approval.
