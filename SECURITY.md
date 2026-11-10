# Security Policy

## Status of this repository

This repository is a **frozen demonstration** (proof of concept) of Q-Ready, a
post-quantum cryptography migration assistant. It is published to show what the
project does, not to be run in production.

- **No maintenance is promised.** Reports are read, but a fix is not guaranteed.
- **Do not deploy it on a production system or an exposed network.** The API has
  no authentication and only allows requests from a local development origin.
  Run it on your own machine, for evaluation only.
- **Do not point the scanner at systems you do not own or administer.**

## Reporting a vulnerability

Please report security issues **privately**, using GitHub's private vulnerability
reporting:

1. Open the [**Security** tab](https://github.com/Q-Ready/Q-Ready-Public/security)
   of this repository.
2. Click **Report a vulnerability** (direct link:
   [new advisory](https://github.com/Q-Ready/Q-Ready-Public/security/advisories/new)).

Please **do not open a public issue or pull request** for a vulnerability, and do
not disclose it publicly before we have acknowledged your report.

A useful report includes:

- what is affected (file, endpoint or component) and the impact you see;
- steps to reproduce, or a minimal proof of concept;
- any suggested fix.

Do not include real secrets, private keys or personal data in a report.

## What to expect

- We acknowledge a report **within 14 days**.
- We then tell you whether we consider it in scope and whether we plan to act on
  it. Because this repository is a frozen demonstration, a code fix is not
  guaranteed.
- There is no bug bounty programme.

## Scope

In scope: the code in this repository (scanning agent, backend API, frontend and
scoring library), for example a flaw that lets a crafted certificate, key or
configuration file crash the parser, read files outside the intended scope, or
execute code.

Out of scope:

- The test certificates, keys and password-protected files under
  `agent/tests/import/`. They are test fixtures, they are public on purpose, and
  they protect nothing.
- The absence of authentication on the demonstration API, and any issue that
  requires exposing it beyond localhost.
- Vulnerabilities in third-party dependencies that are not exploitable through
  this code.
