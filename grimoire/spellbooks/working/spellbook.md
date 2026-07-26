---
name: "working"
description: "Background working orchestration, status, cancellation, and checkpointing."
---
This optional spellbook governs foreground-to-working handoff.

Use it to queue long or cast-heavy work instead of blocking the foreground thread.

A working is not merely a detached process. A full implementation should give it a durable identity, one living claimant, a renewable lease, durable checkpoints, explicit cancellation, and one honest terminal state.

If the foreground thread or supervisor disappears, reconcile the working from durable evidence before declaring success or failure.

Each concrete cast in this spellbook lives in its own folder beside this manifest.
