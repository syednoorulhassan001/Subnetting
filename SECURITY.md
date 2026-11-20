# Security Policy

## Supported versions

Only the latest release and the current `main` branch receive security fixes.

## Reporting a vulnerability

Please **do not open a public issue** for security problems.

Use GitHub's private reporting instead: go to the repository's **Security** tab and choose
**Report a vulnerability**. Include what you found, how to reproduce it, and the impact you expect.

This is a volunteer-run project. I aim to acknowledge reports within 7 days and will keep you
updated on the fix. Credit is given in the release notes if you would like it.

## Scope

Subnetting is a static, client-side site: no accounts, no server, no stored user data. Relevant
reports include:

- Cross-site scripting or other injection through user input
- Vulnerable or malicious dependencies
- Weaknesses in the build, CI or release pipeline

A wrong subnet calculation is a bug, not a vulnerability. Please file it as a normal bug report.
