<div align="center">
  <img src="assets/corecare-logo.png" width="150" alt="CoreCare logo">
  <h1>CoreCare</h1>
  <p><strong>Understand your computer. Clean it carefully. Keep recovery within reach.</strong></p>
  <p>
    <a href="https://github.com/jkaczmarczyk96-code/core-care-releases/releases"><img alt="Downloads" src="https://img.shields.io/badge/Download-Windows%20%7C%20Linux-087DD1?style=for-the-badge"></a>
    <img alt="Beta" src="https://img.shields.io/badge/status-free%20beta-00AFA5?style=for-the-badge">
    <img alt="Languages" src="https://img.shields.io/badge/UI-English%20%7C%20Czech-49368C?style=for-the-badge">
  </p>
  <p><a href="README.cs.md">Česká verze</a> · English</p>
</div>

CoreCare is a safety-first desktop health application for people who want a
cleaner and healthier computer without trusting a one-click tool to make risky
decisions. It combines guided cleanup, disk diagnostics, startup management,
updates, privacy controls, and performance monitoring in one approachable app.

CoreCare scans and explains first. Nothing is cleaned, repaired, disabled, or
updated until the user reviews and approves the action.

> **Free beta:** CoreCare is under active development. Keep backups of important
> data and review proposed system changes before confirming them.

## Download CoreCare

All official installers and update packages are available on the
**[Releases page](https://github.com/jkaczmarczyk96-code/core-care-releases/releases)**.

| Platform | Recommended download | Current public beta | Notes |
| --- | --- | --- | --- |
| Windows 10/11 x64 | `CoreCare-win-Setup.exe` | `0.1.0-beta.84` | Velopack installer with automatic updates. The current beta is unsigned, so Windows may show a publisher warning. |
| Linux x64 | `CoreCare.AppImage` | `0.1.0-beta.89-linux` | Self-contained AppImage with a dedicated Linux update channel. |

### Run on Linux

After downloading the AppImage, mark it as executable and start it:

```bash
chmod +x CoreCare.AppImage
./CoreCare.AppImage
```

Files ending in `.nupkg`, `RELEASES`, or `releases.*.json` are update metadata
used automatically by CoreCare. Normal users do not need to download or open
them manually.

## Features

### Smart Cleaner

- Scans one drive or all fixed drives.
- Finds large files, old temporary data, archives, disk images, caches, and
  directories containing many small files.
- Evaluates every result by context, location, ownership, age, size, and risk.
- Protects operating-system paths, installed applications, game libraries,
  saves, configuration data, and personal files.
- Automatically selects only conservative low-risk candidates.
- Explains why an item was found and shows the proposed action before cleanup.
- Uses Recycle Bin on Windows and desktop Trash on Linux wherever possible.
- Includes sorting, filtering, individual selection, review, and live progress.

### Disk Health and repair

- Shows used space, free space, file-system type, and capacity pressure.
- Provides guided disk checks with progress and results inside CoreCare.
- Detects common storage and file-system warning signals.
- Offers platform-appropriate repair and storage tools.
- On Linux, supports device details, temperature where available, TRIM
  capability, SMART checks, Btrfs status, and capacity trends.
- On Linux, can verify package-managed system files and repair package
  dependencies using trusted distribution tools.
- Keeps privileged and potentially disruptive actions explicit.

### Startup

- Detects applications configured to run when the user signs in.
- Measures CPU and memory use of startup applications currently running in the
  background.
- Highlights applications that cross conservative resource thresholds.
- Supports reversible enable and disable actions where the platform permits.
- Never disables an application automatically.

### Updates and recovery

**Windows**

- Detects available driver updates through Windows Update.
- Creates a local driver backup before installing selected drivers.
- Shows installation progress, completion, restart state, and update history.

**Linux**

- Discovers system, kernel, firmware, and driver packages through APT, DNF,
  Pacman, or Zypper.
- Creates package restore points before selected updates.
- Requires a verified rollback source for every package before an in-app update
  proceeds.
- Provides compatible rollback actions and package-manager history.

### Privacy

- Smart Cookie Cleanup is opt-in.
- Detects supported Chromium-family and Firefox browser profiles.
- Groups cookies by domain and lets the user choose individual sites.
- Refuses to modify an active browser profile.
- Creates a local browser database backup before removal and supports restore.
- Leaves unselected cookies and browsing history untouched.

### Performance and overview

- Displays live CPU, memory, process, storage, and application health signals.
- Highlights meaningful background resource use instead of listing every
  process as a problem.
- Brings cleaner, storage, startup, update, privacy, and performance status into
  one overview.
- Keeps a local history of cleanup and maintenance actions.
- Includes English and Czech interfaces, an in-app changelog, and update alerts.

## How CoreCare stays careful

1. **Scan locally** without changing the computer.
2. **Explain the finding** and its risk in understandable language.
3. **Ask for review** before cleanup, repair, update, or startup changes.
4. **Block protected locations** belonging to the operating system and apps.
5. **Prefer recovery paths** such as Trash, backups, and package restore points.

CoreCare intentionally avoids registry cleaning, indiscriminate cookie or
history deletion, and one-click system modification.

## Privacy

CoreCare does not currently require an account, subscription, advertising
identifier, or analytics service. File inventories, scan findings, and activity
history stay on the local computer. Online connections are used for update
checks and operating-system update operations requested by the user.

See [PRIVACY.md](PRIVACY.md) for the complete privacy notes.

## Automatic application updates

CoreCare uses [Velopack](https://velopack.io/) and this public repository as its
official update channel. Installed copies can check for a new release, display
release notes, download the correct platform package, and restart into the
update. Windows and Linux use separate update feeds so packages cannot be mixed
between platforms.

## Platform status

| Area | Windows | Linux |
| --- | :---: | :---: |
| Guided cleanup and protected paths | Available | Available |
| Disk capacity and health guidance | Available | Available |
| Startup discovery and resource use | Available | Available |
| Driver or system package updates | Available | Available |
| Local pre-update recovery | Driver backup | Package restore point |
| Smart Cookie Cleanup with backup | Available | Available |
| Czech and English interface | Available | Available |

The Linux beta is validated automatically on Ubuntu 22.04 and 24.04. Support for
other distributions depends on their desktop integration and availability of
APT, DNF, Pacman, or Zypper tools. macOS is planned as a separate native
implementation; mobile platforms are not part of the current desktop beta.

## Support and security

- Report normal bugs and feature requests through
  [GitHub Issues](https://github.com/jkaczmarczyk96-code/core-care-releases/issues).
- For security-sensitive reports, follow [SECURITY.md](SECURITY.md).
- Include the CoreCare version, operating system, affected module, and steps to
  reproduce the problem.
- Never attach credentials, private documents, cookie databases, or personal
  scan results to a public issue.

## About this repository

This is the official public binary and update repository for CoreCare. The
application source repository is private. GitHub may automatically display
source archives for repository tags; those archives contain only the public
release-repository files and are not the private CoreCare application source.

No source-code license is granted by the presence of downloadable binaries in
this repository.

Copyright © CoreCare contributors. All rights reserved.
