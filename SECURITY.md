# Vionex APK Security & Verification

## Official source
Download Vionex CRM only from this portal or the official release repository:
https://github.com/paylock786-art/vionex-crm-releases/releases

## Verify SHA-256 (Windows PowerShell)
After downloading the APK, run:
```powershell
Get-FileHash .\Vionex-CRM.apk -Algorithm SHA256
```
Compare the result with the SHA-256 value published for that exact release.

## Verify Android APK signature
With Android SDK Build Tools installed:
```powershell
apksigner verify --verbose --print-certs .\Vionex-CRM.apk
```
The signer certificate should match the official Vionex release signing certificate.

## Important
- A valid signature proves the APK has not changed since it was signed; it does **not** prove an app is harmless.
- Play Protect may still warn about a new or less-reputed APK. This portal cannot guarantee warning-free installation.
- Never install an APK if Android identifies it as harmful or if its hash/signature does not match.
- VirusTotal reports can be incomplete and are not a guarantee of safety.
- Report suspected security issues privately to the Vionex team rather than publishing exploit details.
