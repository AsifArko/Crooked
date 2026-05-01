# Security policy

This document describes how to report security issues for this repository and
what you can expect in response. The project is a **Next.js** application with
**API routes**, **Sanity CMS** integration, **Stripe** payments, **cron**
endpoints, optional **GitHub** integration, and third-party job/data APIs—see
[`docs/api-spec.md`](docs/api-spec.md) and
[`docs/environment-and-deployment.md`](docs/environment-and-deployment.md) for
surface area and deployment notes.

## Supported versions

Security reports are accepted for the **default branch** of this repository and
for deployments you operate from an up-to-date checkout. Older forks or pinned
commits may not receive fixes; upgrade and retest before reporting when possible.

## Reporting a vulnerability

**Please do not** open a public GitHub issue for undisclosed security
vulnerabilities (that can put users at risk).

Instead, email **asif.imch@gmail.com** with:

- A short description of the issue and its impact
- Steps to reproduce (or a proof-of-concept) if you can share them safely
- Affected components (e.g. specific API route, admin flow, dependency)
- Whether you believe the issue is already exploited or publicly known

You may encrypt your message with PGP if you publish a key for this address;
otherwise we rely on standard email confidentiality.

## What to expect

- We aim to acknowledge receipt within a **few business days**
- We may ask follow-up questions to reproduce or scope the issue
- We will coordinate a fix and disclosure timeline when appropriate
- Credit in release notes or advisories can be discussed if you want it

## Scope

**In scope** (examples):

- Authentication or authorization flaws in this codebase (including Studio gate,
  cron secrets, admin APIs)
- Injection, SSRF, or similar issues in application code we maintain
- Mishandling of secrets or tokens when attributable to this repo’s patterns

**Out of scope** (examples):

- Social engineering or physical attacks
- Denial-of-service against infrastructure without a clear defect in our code
- Issues in third-party services (report to the vendor; we may still harden
  integration if needed)
- **Dependency alerts**: please report critical issues with enough detail to
  reproduce; routine `npm audit` findings may be handled through normal updates.

## Secure development reminders

Operators should follow [`docs/environment-and-deployment.md`](docs/environment-and-deployment.md)
for secrets, `CRON_SECRET`, Studio access, and production hardening. Do not
commit real API keys, tokens, or `.env` files.

## Contact

**Asif Imtiyaz Chowdhury** — asif.imch@gmail.com
