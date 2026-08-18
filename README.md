<picture>
  <source media="(prefers-color-scheme: dark)"
          srcset="https://raw.githubusercontent.com/keelapps/.github/main/brand/wordmark-transparent-cream.png">
  <img alt="keelapps"
       src="https://raw.githubusercontent.com/keelapps/.github/main/brand/wordmark-transparent.png"
       width="300">
</picture>

# Support

This is where bugs, feature requests, and questions about keelapps products are
tracked. The products themselves are closed-source; this repository is the
public record of what has been reported, what is being worked on, and what has
been fixed.

## Products

**Atlassian Cloud** — apps built on Atlassian Forge, sold through the Atlassian
Marketplace.

| App | Product | Status |
| --- | --- | --- |
| **AccessLens** | Permission audit for Jira | In development |
| **Digest** | Scheduled reporting for Jira | In development |
| **Evergreen** | Content freshness for Confluence | In development |
| **Mail Templates** | Notification templates for Jira | In development |
| **Recur** | Recurring tasks for Jira | In development |

**macOS** — sold directly.

| App | Product | Status |
| --- | --- | --- |
| **Keelhaven** | Backup for macOS — [keelhaven.app](https://keelhaven.app) | Pre-release |

Nothing has shipped yet. This tracker is open ahead of the first release so that
early questions have somewhere to go.

## Reporting something

[Open an issue](https://github.com/keelapps/support/issues/new/choose) and pick
the template that fits:

- **Bug report (Atlassian apps)** — something in a Forge app does not work as
  it should
- **Bug report (Keelhaven)** — something in the Mac app does not work as it
  should
- **Feature request** — something a product should be able to do
- **Question** — how something works, or whether a product can do what you need,
  including before you install it

Bug reports are split by platform, because the details that identify a problem
in a Forge app and a problem in a Mac app have nothing in common. The other
templates ask which product you mean — please answer it; it is what routes the
issue.

## What does not belong here

This tracker is public and permanent. Two things should go elsewhere:

- **Security vulnerabilities** — report them privately. See [SECURITY.md](SECURITY.md).
- **Billing, licensing, refunds, and evaluation periods for the Atlassian apps**
  — handled by Atlassian, not by us. Contact
  [Atlassian Marketplace support](https://support.atlassian.com/contact/).
  Keelhaven is sold directly, so once it is on sale those questions come to us
  at <support@keelhaven.app> instead.

## What to expect

We read everything. Issues are triaged within a few working days, and we would
rather tell you plainly that something is out of scope than leave it open
indefinitely. Issues closed without a fix will say why.

## Legal

**Atlassian apps.** All five adopt the Atlassian standard end-user agreement
(Bonterms v1.0) and publish a per-app privacy policy. They are zero-egress: they
run on Atlassian Forge, store data in the customer's own Atlassian tenant, and
the vendor never touches customer data — so we are not a data processor under
GDPR and do not sign separate DPAs.

**Keelhaven.** Sold directly rather than through a marketplace, so none of the
above carries over. It has no account system and no server of ours: backups go
from the user's Mac to storage they own, encrypted before they leave the
machine, and nothing reaches us. Its privacy policy is published at
[keelhaven.app/privacy](https://keelhaven.app/privacy); its end-user agreement
is not written yet and will be before the app goes on sale.

[LEGAL.md](LEGAL.md) records the reasoning behind both, and the per-product
status.

---

<sub>keelapps builds administration and compliance apps for Atlassian Cloud, and
Keelhaven for macOS. See the
<a href="https://github.com/keelapps">organisation profile</a>.</sub>
