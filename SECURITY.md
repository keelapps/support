# Security policy

## Reporting a vulnerability

**Do not open a public issue for a security vulnerability.**

Our apps handle permission data, content metadata, and scheduled automation
inside customer Jira and Confluence sites. A publicly posted vulnerability
report is actionable by anyone who reads it before we have shipped a fix.

Report it privately through GitHub's
[private vulnerability reporting](https://github.com/keelapps/support/security/advisories/new).

Please include what you found, how to reproduce it, and what an attacker could
do with it. If you have a proof of concept, keep it to the minimum needed to
demonstrate the issue.

## What happens next

- We acknowledge within **3 working days**.
- We confirm or dispute the finding, with reasoning, within **10 working days**.
- Confirmed vulnerabilities are fixed and deployed as a priority. Because our
  apps run on Atlassian Forge, fixes reach all installations without customer
  action.
- We will tell you when the fix is live, and we are happy to credit you by name
  unless you prefer otherwise.

## Scope

In scope: the keelapps apps listed in [README.md](README.md), and this
organisation's public repositories.

Out of scope: vulnerabilities in Atlassian Jira, Confluence, or the Forge
platform itself — report those to
[Atlassian](https://www.atlassian.com/trust/security/report-vulnerability).
Findings that require an already-compromised administrator account are also out
of scope.

## Good faith

We will not pursue legal action against anyone who reports a vulnerability in
good faith, stays within the scope above, and gives us reasonable time to fix
it before disclosing publicly. We do not currently run a paid bounty programme.
