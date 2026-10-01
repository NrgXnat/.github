# Security Policy

This policy applies to all repositories in the [NrgXnat](https://github.com/NrgXnat)
organization, including XNAT core, XNAT plugins, and related tools, unless a
repository provides its own `SECURITY.md`.

## Supported Versions

### XNAT core

| Version  | Supported                   |
| -------- | --------------------------- |
| 1.10.x   | :white_check_mark:          |
| 1.9.3.x  | :warning:					 |
| < 1.9.3  | :x:                         |

Fixes for 1.9.3.x are provided at the XNAT team's discretion, typically for
critical or high-severity issues. For the latest features and fixes, we 
recommend upgrading to the latest release.

### XNAT plugins

For each plugin, only the **latest release** is supported. Security fixes are
delivered in a new plugin release rather than backported to older plugin
versions. To receive a fix, upgrade to the latest release of the plugin that
is compatible with a supported XNAT version.

## Reporting a Vulnerability

Please **do not** report security vulnerabilities through public GitHub
issues, discussions, or pull requests.

### Private vulnerability reporting (preferred)

Report the issue privately in the repository where the vulnerability exists:

1. Go to the affected repository (for example, `NrgXnat/xnat` for XNAT core,
   or the repository for the affected plugin).
2. Open the **Security** tab.
3. Click **Report a vulnerability**.

If you're not sure which repository is affected, report it in
[NrgXnat/xnat](https://github.com/NrgXnat/xnat/security/advisories/new).

### Email

Prefer email? Write to
[security@xnat.org](mailto:security@xnat.org?subject=XNAT%20Security%20Report&body=Affected%20repository%2Fplugin%3A%0AXNAT%20version%3A%0APlugin%20versions%3A%0ATomcat%20version%3A%0APostgres%20version%3A%0AOS%20version%3A%0ABrowser%20version%3A%0A%0ADescription%20and%20steps%20to%20reproduce%3A%0A%0APotential%20impact%3A%0A)
instead. Use email if you need to attach logs, screenshots, or other files,
or if the affected repository is archived or doesn't offer the
**Report a vulnerability** button.

## What to Include

Please include a detailed description of the issue, steps to reproduce it,
its potential impact, and your environment:

- Affected repository or plugin
- XNAT version
- Plugin versions
- Tomcat version
- Postgres version
- OS version
- Browser version


**Do not include protected health information (PHI) or real subject data**
in your report, logs, or screenshots. Please redact or de-identify them first.

Thanks for helping us keep XNAT secure!
