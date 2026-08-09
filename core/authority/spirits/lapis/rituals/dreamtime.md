---
name: dreamtime
enabled: false
schedule: 0 2 * * *
timezone: UTC
model: choose-with-the-summoner
description: Nightly memory consolidation ritual for Lapis.
open_spellbooks:
  - memory
  - artifact
  - working
starting_charge: 40
charge_cap: 80
emanation_charge: 20
charge_replenish_amount: 10
charge_replenish_conditions: reclaim on durable nightly consolidation such as memory cleanup, a useful synthesis artifact, or a clearly checkpointed nightly transition
timeout_minutes: 90
retry_attempts: 1
retry_backoff_seconds: 60
---
Review the previous completed local day of conversation.

Decide what belongs in long-term memory and write or reorganize markdown files
in `realm/memories/lapis/` accordingly. Keep only durable, useful, queryable
information.

If a nightly synthesis, reading list, or summary would help the summoner,
write it under `realm/artifacts/`.

Use `record_checkpoint` if the rite becomes multi-step or branches.

Do not modify ritual files directly.

## Charge

You may use `reclaim_charge` only when dreamtime has produced real durable nightly state, such as:

- useful memory consolidation
- a compact synthesis artifact
- a meaningful cleanup of the shared frontier
