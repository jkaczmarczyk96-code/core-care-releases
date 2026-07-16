# CoreCare

**A safety-first Windows health and cleanup application.**

[Čeština](README.cs.md) | English

CoreCare helps people understand what occupies their storage, review low-risk cleanup candidates, maintain Windows, and monitor common health signals without blindly deleting files or changing the system without approval.

> CoreCare is currently a free beta. The Windows version is under active development and should be used with the same care as other system maintenance software.

## Download

Open the [CoreCare Releases](https://github.com/jkaczmarczyk96-code/core-care-releases/releases) page and download:

- **`CoreCare-win-Setup.exe`** - recommended Windows installer with automatic updates.
- **`CoreCare-win-Portable.zip`** - portable build intended mainly for testing.
- **`.nupkg`, `RELEASES`, and `releases.win.json`** - Velopack update files used by CoreCare; users do not need to open them manually.

The current public beta is available from the [beta.80 release](https://github.com/jkaczmarczyk96-code/core-care-releases/releases/tag/v0.1.0-beta.80).

## Current features

### Smart Cleaner

- Scans a selected fixed drive.
- Finds large files, old temporary data, caches, installers, archives, disk images, and folders containing many small files.
- Classifies every result by context and risk.
- Protects Windows locations, installed applications, game installations, saves, and personal data.
- Automatically selects only conservative low-risk candidates.
- Moves approved files to the Recycle Bin instead of permanently deleting them.
- Supports sorting, filtering, individual selection, removal review, and progress reporting.

### Disk Health

- Shows used and available space for fixed drives.
- Provides read-only file-system checks with in-app progress and results.
- Offers guided access to Windows file repair, image repair, drive optimization, and storage settings.
- Keeps administrative actions explicit and user-approved.

### Startup

- Detects applications launched with Windows.
- Measures current CPU and memory use of running startup applications.
- Highlights resource-heavy background applications.
- Supports reversible enable and disable actions where Windows permits them.

### Driver and system updates

- Detects available driver updates through Windows Update.
- Allows users to select driver updates directly in CoreCare.
- Creates a local driver backup before installation.
- Downloads and installs selected drivers through a hidden elevated CoreCare worker.
- Displays update progress, completion status, and restart requirements in the application.
- Shows recent Windows Update history and pending restart status.

### Privacy

- Smart Cookie Cleanup is disabled by default.
- Detects old website cookies in supported Chromium browsers and Firefox.
- Allows per-domain selection instead of deleting all browser data.
- Creates a browser database backup before removal.

### Performance

- Measures current system CPU and memory use.
- Lists applications with meaningful background resource use.
- Links to Task Manager, power settings, and startup controls for informed action.

## Safety principles

CoreCare is designed around a few strict rules:

1. Nothing is removed or repaired without user approval.
2. Windows and application integrity take priority over reclaimed space.
3. Uncertain files are shown for review, not selected automatically.
4. Cleanup uses the Recycle Bin wherever possible.
5. Driver installation starts only after a local backup succeeds.
6. Privacy tools are opt-in and operate on selected domains only.

CoreCare intentionally avoids registry cleaning, one-click system modification, and indiscriminate deletion of browser history or cookies.

## Requirements

- Windows 10 or Windows 11, 64-bit.
- Internet connection for application and driver update checks.
- Administrator approval for driver installation and protected Windows repair operations.

The installer is self-contained; users do not need to install the .NET SDK or runtime separately.

## Updates

Installed builds use [Velopack](https://velopack.io/) to check this public repository for new CoreCare releases. Update packages are downloaded only after the user chooses to update, and installation is handled by the installed CoreCare updater.

Starting with beta.81, official release builds are obfuscated before packaging and the release pipeline requires a valid Windows code signature. Code signing improves authenticity and tamper detection; it does not make reverse engineering impossible.

## Privacy

CoreCare does not currently require an account, subscription, advertising identifier, or analytics service. Scan findings and maintenance results remain on the local computer. Online connections are used for GitHub release checks and Windows Update operations requested by the user.

See [PRIVACY.md](PRIVACY.md) for details.

## Beta limitations

- The current release targets Windows only.
- macOS and Linux versions are planned but require platform-specific storage, update, startup, and repair implementations.
- Mobile operating systems impose stricter sandbox limitations and are not part of the current desktop beta.
- Hardware diagnostics, per-device driver rollback, installed-application uninstall guidance, and game library/save detection will continue to evolve.

## Support and security

- For normal bugs and feature requests, use [GitHub Issues](https://github.com/jkaczmarczyk96-code/core-care-releases/issues).
- For security-sensitive reports, follow [SECURITY.md](SECURITY.md) and do not post credentials, private files, or exploit details in a public issue.
- Include the CoreCare version, Windows version, affected module, and reproduction steps when reporting a problem.

## Source and licensing

This repository is the official public binary release channel. The CoreCare source repository is private. No source-code license is granted by the presence of downloadable binaries in this repository.

Copyright © CoreCare contributors. All rights reserved.
