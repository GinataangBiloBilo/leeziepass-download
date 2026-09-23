# Security Policy

## Supported versions

Only the [latest release](../../releases/latest) receives fixes. Please check
that you are on it before reporting.

## Reporting a vulnerability

**Please do not open a public issue for security problems.**

Report privately via GitHub's
[private vulnerability reporting](../../security/advisories/new)
(Security tab → "Report a vulnerability").

Relevant reports include, for example:

- weaknesses in how passwords are generated (predictable randomness, biased
  word/number/symbol selection, reduced effective entropy)
- the application leaking generated passwords (to disk, logs, the network,
  or beyond the clipboard copy you requested)
- a release binary whose SHA-256 does not match `SHA256SUMS.txt`
- crashes or unexpected behaviour when loading a crafted custom wordlist

Please include the LeeziePass version (see **About LeeziePass** in the system
menu), your Windows version and steps to reproduce.

This is a hobby project maintained in spare time: expect an acknowledgement
within about a week. Confirmed issues will be fixed in a new release and
credited in the release notes unless you prefer otherwise.
