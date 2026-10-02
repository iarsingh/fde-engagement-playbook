# Example — Harborline Freight

Filled engagement: [fde-harborline-engagement](https://github.com/iarsingh/fde-harborline-engagement)

| Template | Where it went |
| --- | --- |
| Discovery brief | `docs/01-discovery-brief.md` |
| Success metrics | `docs/02-success-metrics.md` |
| Solution design | `docs/03-solution-design.md` |
| Security review | `docs/04-security-and-data.md` |
| Rollout and rollback | `docs/05-rollout-plan.md` |
| Weekly readout | `docs/06-customer-readout.md` |
| Retro | Below |

## Retro

**What the customer kept:** the score table and the eval file. The night lead can add a shipment without understanding the HTTP layer.

**What to refuse earlier next time:** a model API. IT said no on day one. Sketching a hosted model would have wasted the first design pass.

**Copied next time:** seven docs, an eval file that CI runs, an audit log that stores the decision and not the raw record.

**Left behind:** freight-specific points for SLA, P1, and reefer temperature. The clinic engagement needs consent and a viewer, not a checkpoint SLA.

**Interview sentence:** Harborline's night desk was spending half an hour on late reefers, IT banned external models, so the pilot is a cited scoring policy with an eval gate, and it does not claim fewer missed deliveries yet.
