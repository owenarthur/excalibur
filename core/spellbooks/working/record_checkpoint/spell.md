---
name: "record_checkpoint"
description: "Write an internal checkpoint into the shared daily thread without sending a user-facing message."
---
Write one bounded checkpoint into the working's durable record and the shared daily thread.

Only the living claimant should advance a working. A checkpoint reports state; it does not grant authority or prove completion.

This scaffold keeps only the descriptive `spell.md` layer and omits the handler and runtime code.
