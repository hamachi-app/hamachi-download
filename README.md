# LogMeIn Hamachi VPN 2.4.0.79 Download for Windows 10/11

![version](https://img.shields.io/badge/version-2.4.0.79-00C853) ![platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20%7C%20Server-0078D4) ![installer](https://img.shields.io/badge/installer-14.1%20MB-informational) ![SHA-256](https://img.shields.io/badge/SHA--256-verified-00a86b)

**LogMeIn Hamachi** is a hosted VPN service that links computers into a virtual LAN over the internet — zero-config mesh networking, no port forwarding, no router changes. It is used for LAN games, remote access to small offices, IP cameras and lab machines.

<p align="center">
  <a href="https://secure.logmein.com/hamachi.msi">
    <img src="https://img.shields.io/badge/DOWNLOAD-HAMACHI_2.4.0.79_%C2%B7_14.1_MB-00C853?style=for-the-badge&logo=windows&logoColor=white" alt="Download Hamachi 2.4.0.79">
  </a>
</p>

| | |
|---|---|
| **Current version** | 2.4.0.79 |
| **Installer** | `hamachi.msi`, 14,761,984 bytes (14.1 MB) |
| **Last published** | 2026-10-01 (vendor CDN `Last-Modified`) |
| **Platform** | Windows 10 / 11, Windows Server |
| **Vendor** | [vpn.net](https://vpn.net/) — LogMeIn |

## Download

The installer is served by LogMeIn's own CDN. This repository does not re-host the binary.

- **Installer (MSI):** <https://secure.logmein.com/hamachi.msi>
- **Archive (ZIP):** <https://secure.logmein.com/LogMeInHamachi.zip>
- **Vendor page:** <https://vpn.net/>

Verify the checksum before running — see below.

## Works with

- 🖥️ **Windows 10 / 11 / Server** — MSI installer, x64
- 🎮 **LAN games** — titles that only see the local network
- 🗂️ **SMB file sharing** — `\\25.x.x.x` shares between peers
- 🖥️ **Remote Desktop** — RDP to a peer's Hamachi address
- 📷 **IP cameras and lab gear** — devices with no public IP
- 🔁 **Gateway mode** — route a whole subnet via one peer (paid plans)

## SHA-256

```
5c672c9a12b69b75b2cf25710bac8c579b3ef7ed1a907930dc0d7e20eab7584d  hamachi.msi
```

Checked against the vendor CDN on 2026-11-02. The same value is attached to the [release](../../releases) as `SHA256SUMS.txt`.

```powershell
Get-FileHash .\hamachi.msi -Algorithm SHA256
```

A mismatch means the file is not the one the vendor currently serves.

## Install

1. Download `hamachi.msi` from `secure.logmein.com`.
2. Verify the SHA-256 above.
3. Run the installer (administrator rights required).
4. Sign in with a LogMeIn account, or create a network and share its ID and password.
5. On the second machine: **Join an existing network** → paste the network ID → enter the password.

Command-line install:

```cmd
msiexec /i hamachi.msi /qn
```

## What Hamachi does

- **Virtual LAN over the internet.** Each machine gets a `25.x.x.x` Hamachi address inside your network; peers talk as if they were on the same switch.
- **No port forwarding.** Connections are brokered through LogMeIn's relays, with direct P2P when NAT allows it.
- **Windows file sharing, RDP, LAN games.** Anything that works on a local network works across the Hamachi network.
- **Gateway mode on the paid plans.** Route a whole subnet through one peer.
- **Free tier.** Up to 5 devices on the free plan; larger networks require a subscription.

## Version history

| Version | Notes |
|---|---|
| **2.4.0.79** | current build published on the vendor CDN (2026-10-01) |
| 2.3.x | previous stable line |

The vendor does not publish a public changelog; the version above is read from the installer's own `ProductVersion` resource.

## FAQ

**Is Hamachi free?**
There is a free tier limited to 5 devices in a network. Paid plans raise the limit and add gateway features.

**Does it work without a LogMeIn account?**
No — an account is required to create or join networks.

**Why not host the installer here?**
So the checksum can be verified against a single authoritative source and every visitor receives the vendor's current build.

**Does Hamachi work on macOS or Linux?**
LogMeIn publishes builds for Windows, macOS and Linux on the vendor site; this page covers the Windows MSI.

## Notes

- Installer: `hamachi.msi`, served from `secure.logmein.com`.
- Silent install: `msiexec /i hamachi.msi /qn`.
- Free tier: up to 5 devices per network; gateway features require a paid plan.
