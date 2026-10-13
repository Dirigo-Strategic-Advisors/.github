# Security Policy

## Reporting a vulnerability

**Please do not open a public issue for security vulnerabilities.**

Report privately using GitHub's
[private vulnerability reporting](https://docs.github.com/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability)
on the affected repository (Security tab → "Report a vulnerability"), or email
`security@dirigostrategic.com`.

Include:

- A description of the issue and its impact
- Steps to reproduce (proof of concept if possible)
- Affected repository, version, and environment
- Any suggested remediation

## What to expect

| Stage | Target |
|-------|--------|
| Acknowledgement | 2 business days |
| Initial assessment | 5 business days |
| Fix / mitigation for critical issues | as fast as possible; coordinated disclosure |

We will keep you informed and credit you (if you wish) once a fix is released.

## Scope

In scope: our repositories, applications, and published packages. Out of scope:
third-party services we do not control; social engineering; denial-of-service via
volumetric attacks.

## Our commitments

- We require two-factor authentication for all organization members.
- We monitor dependencies with Dependabot and treat high/critical findings as urgent.
- We never commit secrets; if a secret is exposed we rotate it immediately.

See the [Security Standards](../engineering-standards) (private) for internal policy.
