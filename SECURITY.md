# Security Policy

## Supported versions

CoreCare is currently in beta. Security fixes are provided for the newest published beta release. Users should update to the latest available version before reporting an issue that may already be fixed.

## Reporting a vulnerability

Do not publish credentials, personal files, driver backups, browser databases, exploit code, or detailed vulnerability information in a public issue.

For a security-sensitive report:

1. Contact the repository owner through the GitHub profile at [jkaczmarczyk96-code](https://github.com/jkaczmarczyk96-code).
2. Include the affected CoreCare version, Windows version, impact, and minimal reproduction steps.
3. Remove personal paths, tokens, cookies, and other sensitive data from screenshots and logs.

For non-sensitive bugs, use the public [issue tracker](https://github.com/jkaczmarczyk96-code/core-care-releases/issues).

## Release integrity

The public repository contains official CoreCare release assets. Starting with beta.81, the release workflow is configured to require Authenticode signing and verify the signature before publication. Users should download CoreCare only from this repository's Releases page.
