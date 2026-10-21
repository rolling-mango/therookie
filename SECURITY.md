# Security

## Reporting a vulnerability

Please don't report security issues in public GitHub issues.

Email **info@rollingmango.co.kr** with:

- What you found and where (CLI version, command, or page)
- Steps to reproduce
- What an attacker could do with it

Don't include real tokens, passwords, or other people's data. If a proof needs a credential, describe it instead of pasting it.

## What to expect

- We aim to confirm we received your report within 3 business days.
- After we've looked into it, we'll tell you whether we can reproduce it and what we plan to do.
- When a fix ships, it will be listed in [CHANGELOG.md](CHANGELOG.md). We'll credit you there if you'd like.

Please give us reasonable time to fix the issue before you disclose it publicly.

## If your connection was exposed

If a Rookie connection token was shown or shared somewhere it shouldn't be, run `rookie login` on that machine to connect again, then check your dashboard for connections you don't recognize.
