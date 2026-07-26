---
name: "inspect_working"
description: "Inspect one background working by name or id."
---
Inspect one working by its durable name or id.

Return its actual state, current claimant, recent heartbeat, checkpoints, cancellation state, and terminal outcome. An absent observer is not itself proof that the working failed.

This scaffold keeps only the descriptive `spell.md` layer and omits the handler and runtime code.
