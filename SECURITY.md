# Security policy

## Reporting a vulnerability

**Do not open a public issue for a security vulnerability.**

Our Atlassian apps handle permission data, content metadata, and scheduled
automation inside customer Jira and Confluence sites. A publicly posted
vulnerability report is actionable by anyone who reads it before we have
shipped a fix.

Report it privately by email to
<support@keelapps.atlassian.net>.

Please include what you found, how to reproduce it, and what an attacker could
do with it. If you have a proof of concept, keep it to the minimum needed to
demonstrate the issue.

## What happens next

- We acknowledge within **3 working days**.
- We confirm or dispute the finding, with reasoning, within **10 working days**.
- Confirmed vulnerabilities are fixed and released as a priority. The apps run
  on Forge, so a fix reaches every installation without customer action.
- We will tell you when the fix is live, and we are happy to credit you by name
  unless you prefer otherwise.

## Scope

In scope: the Atlassian apps listed in [README.md](README.md), and the
[keelapps.app](https://keelapps.app/) website.

Out of scope, because they are not ours to fix:

- Vulnerabilities in Atlassian Jira, Confluence, or the Forge platform — report
  those to
  [Atlassian](https://www.atlassian.com/trust/security/report-vulnerability).
- Findings that require an already-compromised administrator account.

## Good faith

We will not pursue legal action against anyone who reports a vulnerability in
good faith, stays within the scope above, and gives us reasonable time to fix
it before disclosing publicly. We do not currently run a paid bounty programme.
