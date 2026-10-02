# 90-day FDE profile plan

Start date: 2 October 2026. Review the public profile on day 90, not the number of repos.

Build two engagements yourself. Leave the third as a stretch only if the first two are runnable, tested, and written up. Three half-finished demos are weaker than two engagements a stranger can clone.

## Outcome on day 90

- Two public repos, each with the seven engagement docs and a test the metric depends on
- GitHub pinned repos: this playbook, Harborline, and the second engagement
- LinkedIn headline and About section use the positioning line
- Four short write-ups, one per artifact type: a discovery constraint, a rejected design, a security rule, a rollout stop condition
- One 8-minute demo recording per engagement, spoken as a customer readout
- A one-page story you can tell in an interview without opening the code

## Days 1-21 — show the motion

**Repo:** [fde-harborline-engagement](https://github.com/iarsingh/fde-harborline-engagement)

Harborline Freight will not send shipment data to an external model. The night desk needs a cited answer, not a chatbot.

Done when:

- `pytest` and `python -m harborline eval` pass
- The readout states the baseline the customer reported and refuses a fake ROI
- You can explain the score for SHP-1042 from memory: SLA, P1, temperature

Practice this week: write the discovery brief before you touch the scorer. If the constraint does not delete a design you wanted, the brief is too soft.

## Days 22-50 — change the industry, keep the muscle

**Repo to create:** `fde-clinic-intake`

A clinic wants after-hours symptom intake summarized for the morning nurse. The constraint is different from Harborline: notes may contain health information, the audit log has a named viewer, and the service must record consent before it stores a summary.

Reuse the seven templates. Do not reuse the freight scorer.

Done when:

- A sample note is rejected when consent is missing
- The audit log names the viewer and does not store the raw note
- The nurse-facing summary cites the source sentence
- The readout is written to a clinic manager, not to an ML audience

This is the repo that stops the profile from looking like one logistics demo.

## Days 51-75 — show you can integrate, not only score

**Repo to create:** `fde-ledger-reconcile`

A finance ops team receives payment webhooks and a settlement CSV that do not share a key. The engagement is idempotent matching, an exception queue, and a reconciliation note a controller can sign.

Done when:

- Replaying the same webhook does not double-count
- An unmatched payment lands in an exception file with the reason
- Tests cover duplicate delivery, a missing field, and a partial settlement
- The design doc says what you refused to auto-resolve

Harborline proves judgment under a security constraint. This one proves you can be trusted with money-shaped data.

## Days 76-90 — make it findable

- Pin the playbook, Harborline, and whichever of the two later repos is stronger
- Rewrite the LinkedIn About section from [positioning](positioning.md). Lead with the customer workflow, then the stack.
- Publish four posts, each one artifact:
  1. The Harborline constraint that killed the model API
  2. The score table, and why a ranker lost
  3. What the clinic audit log is forbidden to store
  4. A rollout stop condition from one of the engagements
- Record two 8-minute walkthroughs. Script them from the customer readout, then show one test failing and the rule that makes it pass.
- Do two mock discovery calls. The other person plays IT and tries to ban your design. Write down the sentence where you changed scope.

## Weekly cadence

| Day | Hour | Output |
| --- | --- | --- |
| Monday | 1 | Pick the constraint for the week and write it in the discovery brief |
| Wednesday | 2 | Code and tests for that constraint only |
| Friday | 1 | Update the readout so the numbers match the tests |
| Sunday | 1 | One public paragraph. If you cannot explain the decision, the design is not done |

## What not to build

- Another Kubernetes tutorial. The GCP and GKE repos already cover that.
- A wrapper around a hosted chat API with no customer, no eval, and no security rule.
- A fifth portfolio website. Point the existing one at these repos.
- Empty repo shells for clinic and ledger. Create each one when the previous engagement runs.

## Interview story, one page

1. Customer and the hour of the day the pain shows up.
2. The constraint, in their words.
3. The design you wanted and why you dropped it.
4. The artifact they kept: policy, eval file, audit log, or exception queue.
5. How they roll back without you.
6. The metric you agreed before the build, and the metric you refused to claim.
