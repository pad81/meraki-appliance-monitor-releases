# Meraki Appliance Monitor – binary releases

This repository contains **only installers and update packages** of Meraki Appliance Monitor, a
small read-only desktop tool for looking up the status of Cisco Meraki appliances via the public
Meraki Dashboard API.

* **No source code is published here.** This repository exists so that installed copies of the
  application can check for and download updates from public GitHub Releases without any login.
* **Not an official Cisco or Meraki product.** Cisco and Meraki are trademarks of their respective owners.

## Platforms

| Platform | Installer | Portable |
|---|---|---|
| Windows 10/11 x64 | `MerakiApplianceMonitor-win-x64-stable-Setup.exe` | `MerakiApplianceMonitor-win-x64-stable-Portable.zip` |
| macOS 12+ Apple Silicon (arm64) | `MerakiApplianceMonitor-osx-arm64-stable-Setup.pkg` | `MerakiApplianceMonitor-osx-arm64-stable-Portable.zip` |

Pre-releases (beta / release candidates) use `-beta-` instead of `-stable-` in the file names and are
marked as *Pre-release*.

## Installation

Download the installer for your platform from the latest release and verify it against
`SHA256SUMS.txt`. The packages are currently **not code-signed**:

* **Windows:** SmartScreen may show “Windows protected your PC” → *More info* → *Run anyway*.
  The application installs per user (no administrator rights).
* **macOS:** Gatekeeper may block the unsigned package. Right-click the `.pkg` → *Open* → *Open*,
  or allow it under *System Settings → Privacy & Security*.

## Updates

The application checks this repository's public releases in the background after start-up and
offers new versions. Nothing is installed or restarted without the user's confirmation. The
*Stable* channel only uses regular releases; the optional *Beta* channel also uses pre-releases.
The update check transfers no user data, credentials or tenant information.
