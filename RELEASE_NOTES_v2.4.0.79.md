# Hamachi 2.4.0.79 — Windows MSI + SHA-256

Current LogMeIn Hamachi build for Windows 10 / 11.

**Installer:** `hamachi.msi` — 14,761,984 bytes (14.1 MB)
**Download:** https://secure.logmein.com/hamachi.msi
**Published:** 2026-10-01 (vendor CDN `Last-Modified`)

## SHA-256

```
5c672c9a12b69b75b2cf25710bac8c579b3ef7ed1a907930dc0d7e20eab7584d  hamachi.msi
```

## Verify before running

```powershell
Get-FileHash .\hamachi.msi -Algorithm SHA256
```

## Silent install

```cmd
msiexec /i hamachi.msi /qn
```

## Notes

- The installer is not re-hosted here. Attached: `SHA256SUMS.txt` only, so the binary always comes from the vendor's CDN.
- Version 2.4.0.79 is read from the installer's own `ProductVersion` resource.
- Free tier: up to 5 devices per network; gateway features require a paid plan.
