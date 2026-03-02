# PostgreSQL images with `pg_crash`

[pg_crash](https://github.com/cybertec-postgresql/pg_crash) is a PostgreSQL
extension designed for **fault injection and chaos engineering**.
It allows users to simulate various failure scenarios—such as backend crashes,
signal handling issues, and memory corruption—to verify how a system handles
unexpected outages.

> [!CAUTION]
> **DO NOT USE THESE IMAGES IN PRODUCTION.**
> These images are specifically designed for fault injection. They include the
> `pg_crash` extension, which is intended to intentionally crash or destabilize
> PostgreSQL processes. Deploying these in a production environment will lead
> to service downtime and potential cluster corruption.

This repository has two major goals:

1. **Build images** of all supported PostgreSQL versions with the
   `pg_crash` extension for Chaos Monkey testing.

2. **Scheduled testing**: Run automated resilience tests for the latest
   container images of each major Postgres version on a cluster built with
   the [CloudNativePG](https://cloudnative-pg.io) operator.

## Trademarks

*[Postgres, PostgreSQL and the Slonik Logo](https://www.postgresql.org/about/policies/trademarks/)
are trademarks or registered trademarks of the PostgreSQL Community Association
of Canada, and used with their permission.*

