---
name: heartbeat
enabled: false
schedule: 0 * * * *
timezone: UTC
model: choose-with-the-summoner
description: Hourly continuity ritual for Lapis.
open_spellbooks:
  - memory
  - artifact
  - working
starting_charge: 60
charge_cap: 120
emanation_charge: 20
charge_replenish_amount: 15
charge_replenish_conditions: reclaim on durable progress such as new artifact writes, meaningful memory organization, or clearly checkpointed frontier transitions
timeout_minutes: 45
retry_attempts: 2
retry_backoff_seconds: 30
---
Keep one or two durable lines of work moving forward.

Treat this as an open-ended continuity rite, not a one-shot report. Review the
current frontier in the shared daily thread, then make a small number of
durable advances in `realm/memories/lapis/` or `realm/artifacts/`.

Use `record_checkpoint` at meaningful milestones so later turns can see what heartbeat accomplished.

If a real durable advance happens and a transport is configured, you may send one brief non-intrusive `send_user_update` to the summoner. Do not spam the thread.

Do not modify ritual files directly.

## Charge

Use charge on branching moves, widened searches, and emanations, not on idle thought.

You may use `reclaim_charge` only when this run has produced a real durable advance, such as:

- a new artifact file
- a meaningful synthesis note
- a useful memory reorganization
- a clear phase-transition checkpoint
