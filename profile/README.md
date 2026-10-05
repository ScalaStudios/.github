<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="../assets/profile/hero-dark.svg" />
    <img src="../assets/profile/hero-light.svg" width="880" alt="Halo, for identity, and Shipyard, for delivery, connected along one line. An ember segment marks the path between them." />
  </picture>
</p>

# Scala Studios

Scala Studios builds open-source infrastructure you host yourself: identity and access management, and the systems that build, store, and ship software.

[Halo](https://github.com/ScalaStudios/Halo) is the identity provider. [Shipyard](https://github.com/ScalaStudios/Shipyard) is the delivery control plane. Both are Go, both run on PostgreSQL, and both are developed in public on this organization.

[scala.gg](https://scala.gg) · [Halo](https://github.com/ScalaStudios/Halo) · [Shipyard](https://github.com/ScalaStudios/Shipyard) · [halo.scala.gg](https://halo.scala.gg)

## Open-source projects

### [Halo](https://github.com/ScalaStudios/Halo)

**Identity and access management**

Halo is a self-hosted identity provider for single sign-on. People sign in with passkeys and security keys. Applications integrate with OpenID Connect, OAuth 2.0, and SAML 2.0. SCIM 2.0 provisions users in and out. Conditional access can require a stronger sign-in method, including in report-only mode, and access reviews remove access that should have ended.

It is a Go server, a web console, and PostgreSQL. No Redis, no message queue, and no license key. Halo is pre-release: what is on `main` works, there is no tagged release yet, and the API can still change before 1.0.

Go · [Apache-2.0](https://github.com/ScalaStudios/Halo/blob/main/LICENSE)

[Repository](https://github.com/ScalaStudios/Halo) · [Website](https://halo.scala.gg) · [Security policy](https://github.com/ScalaStudios/Halo/blob/main/SECURITY.md)

### [Shipyard](https://github.com/ScalaStudios/Shipyard)

**CI/CD, packages, and container images**

Shipyard is one control plane for the path from source to a running environment. YAML pipelines, distributed runners, content-addressed artifacts, npm and Maven repositories, an OCI registry, releases, and deployments. One binary, one database, one UI. Forge credentials are encrypted at rest.

It is alpha. Pipelines run against real forges today. The schema and HTTP API are still moving, so pin a commit if you deploy it. There is no hosted service and no public documentation site yet. The demo in the repository README is the place to start.

Go

[Repository](https://github.com/ScalaStudios/Shipyard) · [Contributing](https://github.com/ScalaStudios/Shipyard#contributing) · [Security](https://github.com/ScalaStudios/Shipyard#security)

## What this organization publishes

Two kinds of infrastructure are public here.

**Identity.** Who may sign in, how they prove it, which applications they can open, and when that access ends. Halo covers that as a self-hosted identity provider: OpenID Connect, SAML, OAuth, passkeys, SCIM, conditional access, and access reviews.

**Delivery.** How a change becomes an artifact, a package, or an image, and how that build is promoted into an environment. Shipyard covers that as a self-hosted CI/CD platform: pipelines, runners, an artifact store, package registries, and an OCI registry.

Private repositories on this organization are not part of the public project list.

## Contributing

Issues and pull requests are welcome.

For Halo, read the [contributing guide](https://github.com/ScalaStudios/Halo/blob/main/CONTRIBUTING.md) before a large change. A typo or a bug with an obvious cause can go straight to a pull request. Halo's [code of conduct](https://github.com/ScalaStudios/Halo/blob/main/CODE_OF_CONDUCT.md) applies to participation in that project.

For Shipyard, keep the change focused, add a test for non-trivial logic, and run `go test ./...` plus the UI build. Details are in the [README](https://github.com/ScalaStudios/Shipyard#contributing).

## Security

Do not report a vulnerability in a public issue or pull request.

Halo accepts reports through [GitHub private vulnerability reporting](https://github.com/ScalaStudios/Halo/security/advisories/new). Response targets are in [SECURITY.md](https://github.com/ScalaStudios/Halo/blob/main/SECURITY.md).

For Shipyard, report the problem privately to the maintainers and leave time for a fix before disclosure. See the [security note](https://github.com/ScalaStudios/Shipyard#security) in the repository.
