# fde-engagement-playbook — project architecture

[README](README.md) · [Interview questions and answers](INTERVIEW_QA.md)

## Purpose and scope

How Akhilesh Ranjan Singh runs a forward deployed engagement, and the 90-day plan for making that the public profile.

This document describes files and symbols in this checkout. Deployment templates and statements in the original overview are distinguished from a verified running environment.

## Component diagram

```mermaid
flowchart LR
    R["Repository"]
    R -. contains .-> C0["README.md"]
    R -. contains .-> C1["examples"]
    R -. contains .-> C2["plan"]
```

For Python repositories, arrows show resolved local imports, not network calls or deployment order. Otherwise the diagram is a repository component map; containment arrows do not assert runtime integration.

## Components and responsibilities

| Component | Responsibility |
| --- | --- |
| [`README.md`](README.md) | Project explanations or operating notes |
| [`examples/harborline.md`](examples/harborline.md) | Project explanations or operating notes |
| [`plan/90-day-fde-profile.md`](plan/90-day-fde-profile.md) | Project explanations or operating notes |

## Existing design and operating guides

These checked-in guides provide the project’s detailed design, operational context, or deployment view:

- [`templates/01-discovery-brief.md`](templates/01-discovery-brief.md).
- [`templates/03-solution-design.md`](templates/03-solution-design.md).
- [`templates/04-security-review.md`](templates/04-security-review.md).
- [`templates/05-rollout-and-rollback.md`](templates/05-rollout-and-rollback.md).

## Documentation workflow

Read the overview, choose the relevant topic or engagement template, and follow its linked examples. This repository is a learning/reference collection rather than a single deployable service.

## Setup and verification

Follow the existing README and the component-specific instructions linked above. No new application start command is asserted for this repository.

No dedicated test files were found in the inspected first-party file inventory. A future implementation should add executable acceptance checks.

## Operating boundaries and design review

Before turning this checkout into a customer deployment, establish the input contract, data ownership, access controls, failure response, evaluation criteria, and rollback owner. Repository fixtures and unit tests demonstrate local behavior; they do not establish throughput, uptime, compliance, or business impact.

A useful architecture review starts with the linked implementation: identify where input enters, where a decision is made, which state can change, and which external dependency can fail. Add a deployment view only for infrastructure that is actually configured and exercised.
