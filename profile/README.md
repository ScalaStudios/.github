<!-- Hero -->
<p>
  <a href="https://scala.gg">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="/assets/profile/hero-dark.svg">
      <img src="/assets/profile/hero-light.svg" width="100%" alt="Scala Studios: open-source software you can host yourself, or let us run for you. Lines run out of one hub to Halo, for identity, Shipyard, for delivery, and Aether, for email, with more lines planned.">
    </picture>
  </a>
</p>

Scala Studios builds open-source software for running a team's systems, and develops it in public. Every project can be hosted on your own infrastructure in full, and we also run our software as a service for teams that would rather not run it themselves. **[Halo](https://github.com/ScalaStudios/Halo)** decides who can sign in to which applications, and for how long. **[Shipyard](https://github.com/ScalaStudios/Shipyard)** takes a commit through pipelines, registries and releases to a running deployment. **[Aether](https://github.com/ScalaStudios/Aether)** runs a team's email, calendar and contacts. All three are written in Go and keep their state in PostgreSQL. More projects are planned.

<!-- Calls to action. Secondary buttons have light and dark variants. -->
<p>
  <a href="https://scala.gg"><img src="/assets/profile/buttons/website.svg" height="44" alt="Visit scala.gg"></a>
  <a href="https://halo.scala.gg/docs"><picture><source media="(prefers-color-scheme: dark)" srcset="/assets/profile/buttons/halo-docs-dark.svg"><img src="/assets/profile/buttons/halo-docs-light.svg" height="44" alt="Halo docs"></picture></a>
  <a href="https://github.com/ScalaStudios/Shipyard#try-the-demo"><picture><source media="(prefers-color-scheme: dark)" srcset="/assets/profile/buttons/shipyard-demo-dark.svg"><img src="/assets/profile/buttons/shipyard-demo-light.svg" height="44" alt="Shipyard demo"></picture></a>
  <a href="#contribute"><picture><source media="(prefers-color-scheme: dark)" srcset="/assets/profile/buttons/contribute-dark.svg"><img src="/assets/profile/buttons/contribute-light.svg" height="44" alt="Contribute"></picture></a>
</p>

## Projects

<!-- Halo -->
<p>
  <a href="https://github.com/ScalaStudios/Halo">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="/assets/profile/halo-dark.svg">
      <img src="/assets/profile/halo-light.svg" width="100%" alt="Halo, identity and access management: a person signs in with a passkey, a policy is checked, OpenID Connect, SAML or SCIM reaches the application, and access is reviewed.">
    </picture>
  </a>
</p>

[![CI](https://img.shields.io/github/actions/workflow/status/ScalaStudios/Halo/ci.yml?branch=main&style=flat&label=ci&labelColor=2a2724)](https://github.com/ScalaStudios/Halo/actions/workflows/ci.yml)
[![Pre-release](https://img.shields.io/github/v/tag/ScalaStudios/Halo?sort=semver&style=flat&label=pre-release&labelColor=2a2724&color=fa7e26)](https://github.com/ScalaStudios/Halo/blob/main/CHANGELOG.md)
[![License: Apache-2.0](https://img.shields.io/badge/license-Apache--2.0-57534d?style=flat&labelColor=2a2724)](https://github.com/ScalaStudios/Halo/blob/main/LICENSE)

**Self-hosted identity and access management.** Halo is where an organization decides who can sign in to which applications, how they prove who they are, and how long their access lasts.

- **Passkeys first.** People sign in with passkeys or security keys. Authenticator apps, recovery codes and magic links are fallbacks you can turn off.
- **Single sign-on.** OpenID Connect, OAuth 2.0 and SAML 2.0 for your applications, and SCIM 2.0 provisioning in both directions.
- **Policies you can test.** Before a conditional access policy applies, report-only mode shows what it would have done to the last 24 hours of sign-ins.
- **Access that ends.** Time-limited access packages, access reviews, and joiner, mover and leaver rules are part of the core product.
- **Small to run.** A Go server, a Next.js interface and PostgreSQL. No Redis, no message queue and no license key.

```bash
curl -fsSL https://halo.scala.gg/install.sh | sh
```

Halo is pre-release, so the API and configuration may change before 1.0. A hosted version, Halo Cloud, is planned.

**[Repository](https://github.com/ScalaStudios/Halo)** · **[Documentation](https://halo.scala.gg/docs)** · **[Self-hosting guide](https://halo.scala.gg/docs/self-hosting)** · **[Changelog](https://github.com/ScalaStudios/Halo/blob/main/CHANGELOG.md)**

<br>

<!-- Shipyard -->
<p>
  <a href="https://github.com/ScalaStudios/Shipyard">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="/assets/profile/shipyard-dark.svg">
      <img src="/assets/profile/shipyard-light.svg" width="100%" alt="Shipyard, CI/CD, packages and container images: source, pipeline and job, then an artifact, a package or an image, then a release and a deployment.">
    </picture>
  </a>
</p>

[![CI](https://img.shields.io/github/actions/workflow/status/ScalaStudios/Shipyard/ci.yml?branch=master&style=flat&label=ci&labelColor=2a2724)](https://github.com/ScalaStudios/Shipyard/actions/workflows/ci.yml)
[![Status: alpha](https://img.shields.io/badge/status-alpha-fa7e26?style=flat&labelColor=2a2724)](https://github.com/ScalaStudios/Shipyard#readme)

**One control plane for software delivery.** Most teams glue the path from source to production together from four or five tools. Shipyard is one binary, one database and one UI that covers all of it.

- **Pipelines and runners.** YAML pipelines with a dependency graph and live logs, run by distributed runners with labels, heartbeats and leases.
- **Artifacts, packages and images.** Content-addressed artifacts on the filesystem or S3, npm and Maven repositories, and an OCI registry that works with `docker push`.
- **Releases and deployments.** Promote a release into an environment from the same UI that built it.
- **Works with your forge.** Import a whole organization through a token, OAuth or a GitHub App, and get webhooks, commit statuses and pull request comments.

```bash
git clone https://github.com/ScalaStudios/Shipyard.git && cd Shipyard
docker compose -f deploy/compose/compose.demo.yml up --build -d
```

Shipyard is alpha. It runs real pipelines against real forges, and the schema and HTTP API are still moving, so pin a commit if you deploy it.

**[Repository](https://github.com/ScalaStudios/Shipyard)** · **[Try the demo](https://github.com/ScalaStudios/Shipyard#try-the-demo)** · **[Deployment guide](https://github.com/ScalaStudios/Shipyard/blob/master/docs/DEPLOY.md)** · **[API and MCP](https://github.com/ScalaStudios/Shipyard/blob/master/docs/mcp.md)**

<br>

<p>
  <a href="https://github.com/ScalaStudios/Aether">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="/assets/profile/aether-dark.svg">
      <img src="/assets/profile/aether-light.svg" width="100%" alt="Aether, email, calendar and contacts: a message from a sender passes Postfix and Rspamd, SPF, DKIM and DMARC are checked, Dovecot stores it, and it reaches the inbox.">
    </picture>
  </a>
</p>

[![CI](https://img.shields.io/github/actions/workflow/status/ScalaStudios/Aether/ci.yml?branch=main&style=flat&label=ci&labelColor=2a2724)](https://github.com/ScalaStudios/Aether/actions/workflows/ci.yml)
[![Status: pre-release](https://img.shields.io/badge/status-pre--release-fa7e26?style=flat&labelColor=2a2724)](https://github.com/ScalaStudios/Aether#known-limitations)
[![License: AGPL-3.0-or-later](https://img.shields.io/badge/license-AGPL--3.0--or--later-57534d?style=flat&labelColor=2a2724)](https://github.com/ScalaStudios/Aether/blob/main/LICENSE)

**Self-hosted email, calendar and contacts.** Aether runs a complete mail server, webmail and CalDAV and CardDAV from one Docker Compose file, and people sign in with a local account, Halo or any OpenID Connect provider.

- **A proven mail stack.** Postfix for SMTP, Dovecot for IMAP and Rspamd for spam filtering and DKIM, configured from PostgreSQL by a Go control plane instead of hand-edited files.
- **Its own webmail.** Aether Mail has conversations, search, rich-text compose with signatures, rules, scheduled send and shared mailboxes.
- **Deliverability built in.** Every domain gets its DNS records with a live check, MTA-STS, TLS reporting and summarized DMARC reports.
- **Calendar and contacts.** Shared calendars, meeting invitations that work with Gmail, Outlook and Apple Calendar, and free/busy while you schedule.
- **Single sign-on in the core.** OpenID Connect sign-in with group-to-role mapping, and app passwords scoped to one mailbox for mail and calendar apps.

```bash
git clone https://github.com/ScalaStudios/Aether.git && cd Aether
./scripts/setup.sh dev && docker compose up -d --build
```

Aether is pre-release and has no version tags yet, so the API and configuration may change before 1.0. It runs Scala Studios' own mail.

**[Repository](https://github.com/ScalaStudios/Aether)** · **[Installation guide](https://github.com/ScalaStudios/Aether/blob/main/documentation/installation.md)** · **[Authentication](https://github.com/ScalaStudios/Aether/blob/main/documentation/authentication.md)** · **[Architecture](https://github.com/ScalaStudios/Aether/blob/main/documentation/architecture.md)**

## How we build

<table>
  <tbody>
    <tr>
      <td width="50%" valign="top">
        <b>Self-hosted, all of it</b><br>
        Every Halo feature is in its open-source repository, and self-hosting is meant to stay complete, with no paid tier for core features. Shipyard has no per-seat pricing and no SaaS dependency, and Aether has no paid tier, no telemetry and no license key.
      </td>
      <td width="50%" valign="top">
        <b>Standards at the edges</b><br>
        Halo speaks OpenID Connect, SAML 2.0, SCIM 2.0 and WebAuthn. Shipyard serves the OCI distribution API and npm and Maven repositories, so <code>docker push</code> works against it. Aether speaks SMTP, IMAP, CalDAV and CardDAV, and signs mail with DKIM.
      </td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <td width="50%" valign="top">
        <b>Secrets stay sealed</b><br>
        Halo keeps session tokens, client secrets and API keys only as SHA-256 hashes and seals signing keys with AES-256-GCM. Shipyard encrypts forge credentials and webhook secrets at rest. Aether encrypts DKIM keys and OIDC client secrets with AES-256-GCM.
      </td>
      <td width="50%" valign="top">
        <b>Built to be automated</b><br>
        All three publish an OpenAPI 3.1 description of their API. Halo issues API keys to service accounts, Shipyard ships an MCP server that lets AI agents drive builds and runners, and Aether sends signed webhooks for every audit event.
      </td>
    </tr>
  </tbody>
</table>

| | Halo | Shipyard | Aether |
| --- | --- | --- | --- |
| **Server** | Go | Go | Go |
| **Interface** | Next.js, React, Tailwind CSS | React, Vite, CSS Modules | Next.js, React, Tailwind CSS |
| **Data** | PostgreSQL, optional S3-compatible storage | PostgreSQL, filesystem or S3-compatible storage | PostgreSQL, Valkey, mail in Maildir |
| **Runs on** | Docker Compose and Caddy, images for amd64 and arm64 | Docker Compose with Caddy or nginx, BuildKit for images | Docker Compose and Caddy, with Postfix, Dovecot and Rspamd |
| **Protocols** | OpenID Connect, OAuth 2.0, SAML 2.0, SCIM 2.0, WebAuthn | OCI Distribution, npm, Maven, MCP | SMTP, IMAP, CalDAV, CardDAV, OpenID Connect |
| **Tests** | Go tests against PostgreSQL, Playwright end-to-end tests | Go tests, an API smoke test | Go tests, integration tests against the running mail stack |
| **CI** | GitHub Actions | GitHub Actions | GitHub Actions |

## Contribute

All three projects take issues and pull requests. A typo or a bug with an obvious cause can go straight to a pull request; for anything larger, open an issue first so the approach is agreed before the code is written. Halo's [code of conduct](https://github.com/ScalaStudios/Halo/blob/main/CODE_OF_CONDUCT.md) applies to everyone taking part in that project.

| | Halo | Shipyard | Aether |
| --- | --- | --- | --- |
| **Bugs and ideas** | [Open an issue](https://github.com/ScalaStudios/Halo/issues/new/choose) | [Open an issue](https://github.com/ScalaStudios/Shipyard/issues/new) | [Open an issue](https://github.com/ScalaStudios/Aether/issues/new) |
| **Local setup** | [Contributing guide](https://github.com/ScalaStudios/Halo/blob/main/CONTRIBUTING.md) | [Development](https://github.com/ScalaStudios/Shipyard#development) | [Contributing guide](https://github.com/ScalaStudios/Aether/blob/main/CONTRIBUTING.md) |
| **Before review** | `go vet`, `go test`, type check and web build | `go test ./...` and the UI build | `gofmt`, `go vet`, `go test`, the integration tests, web lint and build |

## Security

> [!WARNING]
> Report vulnerabilities privately, never in a public issue, pull request or discussion.

Halo takes reports through [GitHub private vulnerability reporting](https://github.com/ScalaStudios/Halo/security/advisories/new), with a target of acknowledging each one within three working days; [SECURITY.md](https://github.com/ScalaStudios/Halo/blob/main/SECURITY.md) lists the rest of the response targets. Aether takes reports the same way, through its own [private vulnerability reporting](https://github.com/ScalaStudios/Aether/security/advisories/new), as its [SECURITY.md](https://github.com/ScalaStudios/Aether/blob/main/SECURITY.md) describes. For Shipyard, report the problem privately to the maintainers and leave time for a fix before disclosure, as its [security note](https://github.com/ScalaStudios/Shipyard#security) asks. Every other repository follows the [organization policy](https://github.com/ScalaStudios/.github/blob/main/SECURITY.md).

<!-- Footer -->
<br>

<a href="https://scala.gg"><img src="/assets/profile/divider.svg" width="100%" alt="Scala Studios"></a>

<p align="center">
  <a href="https://scala.gg">scala.gg</a> &nbsp;·&nbsp; <a href="https://halo.scala.gg">halo.scala.gg</a> &nbsp;·&nbsp; <a href="https://github.com/ScalaStudios/Halo">Halo</a> &nbsp;·&nbsp; <a href="https://github.com/ScalaStudios/Shipyard">Shipyard</a> &nbsp;·&nbsp; <a href="https://github.com/ScalaStudios/Aether">Aether</a>
</p>
