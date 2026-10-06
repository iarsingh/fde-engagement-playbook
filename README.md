# FDE engagement playbook

<!-- project-guide:start -->
## Project guide

[Project architecture](PROJECT_ARCHITECTURE.md) · [Interview questions and answers](INTERVIEW_QA.md)

Use the architecture document for the component diagram, implementation boundaries, and verification entry points. The interview guide includes source-backed answers and project walkthroughs.

### Implementation map

| Component | Responsibility |
| --- | --- |
| [`README.md`](README.md) | Project explanations or operating notes |
| [`examples/harborline.md`](examples/harborline.md) | Project explanations or operating notes |
| [`plan/90-day-fde-profile.md`](plan/90-day-fde-profile.md) | Project explanations or operating notes |

Setup and examples are described in the existing project notes below. Consult the component-specific manifests before assuming a single launch command.

<!-- project-guide:end -->

How Akhilesh Ranjan Singh runs a forward deployed engagement, and the 90-day plan for making that the public profile.

The cloud portfolio already shows GCP, Kubernetes, SRE, and MLOps. Forward deployed hiring looks for a different proof: you can sit with a customer, cut a messy operational problem down to something shippable, obey a constraint that deletes your favorite design, and write the note an operator will forward to their boss.

## Start here

| Doc | Use it for |
| --- | --- |
| [Positioning](plan/positioning.md) | The one-line story and who it is for |
| [90-day profile plan](plan/90-day-fde-profile.md) | What to build, in order, and what "done" means |
| [Templates](templates/) | The seven documents every engagement leaves behind |
| [Harborline example](examples/harborline.md) | One filled engagement: [fde-harborline-engagement](https://github.com/iarsingh/fde-harborline-engagement) |

## The seven artifacts

1. [Discovery brief](templates/01-discovery-brief.md) — the job, the room, the constraint
2. [Success metrics](templates/02-success-metrics.md) — baseline, pilot target, what you will not claim
3. [Solution design](templates/03-solution-design.md) — the decision and why the alternative lost
4. [Security review](templates/04-security-review.md) — data, access, audit, egress
5. [Rollout and rollback](templates/05-rollout-and-rollback.md) — shadow, one desk, stop conditions
6. [Weekly readout](templates/06-weekly-customer-readout.md) — one page a sponsor can forward
7. [Retro](templates/07-engagement-retro.md) — what to reuse next time

A repo that only contains a model demo reads as a tutorial. A repo that contains these seven docs plus code that enforces the metric reads as a deployment.

## Documentation checks

Project architecture, interview guides, and local source links are checked automatically on pushes and pull requests. Run the same check locally:

```bash
python3 .github/scripts/validate_project_docs.py
```
