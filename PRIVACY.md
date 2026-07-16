# CoreCare Privacy Information

Last updated: 16 July 2026

## Local processing

CoreCare is designed to perform storage scanning, cleanup classification, disk-health checks, startup analysis, browser-cookie review, performance measurement, and maintenance-result processing locally on the user's computer.

CoreCare does not currently require a user account and does not include advertising, behavioral analytics, or a telemetry SDK.

## Data handled by CoreCare

Depending on the tools the user runs, CoreCare may locally inspect:

- File and folder paths, sizes, timestamps, and classifications.
- Fixed-drive capacity and file-system information.
- Installed startup entries and current process resource use.
- Windows Update history and available driver-update metadata.
- Browser cookie domains, last-access timestamps, and cookie counts.

This information is displayed in the application and is not uploaded by CoreCare to a CoreCare-operated server.

## Backups

Before supported maintenance actions, CoreCare may create local backups:

- Driver backups are stored under the current user's local CoreCare application-data folder.
- Browser cookie database backups are stored under the current user's local CoreCare application-data folder.

These backups remain on the computer until the user removes them.

## Network connections

CoreCare may connect to third-party services only for requested product functions:

- GitHub is used to check and download CoreCare application releases.
- Windows Update is used to find and install system and driver updates.

Those services operate under their own privacy terms and network policies.

## Browser data

Smart Cookie Cleanup is opt-in. CoreCare scans copies of supported browser cookie databases, presents old domains for review, and removes only domains explicitly selected by the user. The user should close affected browsers before removal.

## Future changes

If accounts, payments, cloud synchronization, crash reporting, or telemetry are added later, this document must be updated before those features are released.
