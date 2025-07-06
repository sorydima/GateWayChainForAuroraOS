# Governance

This document outlines how **GateWayChainForAuroraOS** is stewarded – how decisions are made, who can make them, and how new maintainers are selected.

## Roles

| Role | Responsibilities | Current Holder |
|------|------------------|----------------|
| **Core Maintainer** | Merges PRs, leads releases, guards project vision | @sorydima |
| **Reviewer** | Reviews incoming PRs for style, tests & security | Community volunteers |
| **Contributor** | Submits issues & PRs following CONTRIBUTING.md | Anyone |
| **Security Contact** | Triage private security reports | security@rechain.network |

## Decision‑Making Process

* **Small changes** (docs, typo fixes) are merged by a single Core Maintainer once CI passes  
* **Feature work** requires **2 approving reviews** (at least one Core Maintainer)  
* **Breaking changes** follow an **RFC** process: open a `proposal/` PR, gather community feedback, and reach lazy consensus (≥ 72 h, –1 strong objection blocks)

## Release Authority

Core Maintainers cut releases according to the *RELEASE.md* process. A release candidate can be vetoed by another Core Maintainer within 24 h if a blocking issue is raised.

## Conflict Resolution

When consensus can’t be reached, Core Maintainers vote (majority). In case of deadlock, the project founder (@sorydima) has tie‑breaking authority.

_Last updated: 2025-07-06_
