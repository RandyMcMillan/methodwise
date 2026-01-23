# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 0.1.x   | :white_check_mark: |
| < 0.1   | :x:                |

## Reporting a Vulnerability

We take the security of Methodwise seriously. If you have found a security vulnerability, please do not report it in the public issue tracker.

### How to Report

Please email the maintainers directly at **security@methodwise.com** (or your personal email).
We will acknowledge your report within 48 hours and provide an estimated timeline for a fix.

### What to Include

*   Description of the vulnerability.
*   Steps to reproduce the issue.
*   Potential impact.

## Security Features

Methodwise is designed with security in mind:

1.  **Rust Memory Safety**: Built with Rust to prevent common memory vulnerabilities like buffer overflows.
2.  **No JavaScript**: By design, Methodwise does not execute JavaScript, eliminating an entire class of XSS and browser-based attacks.
3.  **Minimal Parsing**: We use `html2text` for rendering, which reduces the attack surface compared to full web engines.
4.  **Local Only**: History and bookmarks are stored locally with no cloud sync or telemetry.

## Dependency Management

We use `cargo audit` to check for vulnerabilities in our dependency tree.
