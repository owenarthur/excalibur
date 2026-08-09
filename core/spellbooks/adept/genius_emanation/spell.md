---
name: "genius_emanation"
description: "Spawn a stronger general-purpose emanation for the current task while keeping the active spell surface for this run."
---
Placeholder cast manifest for the Excalibur scaffold.

In a full implementation, each cast lives in its own folder under `core/spellbooks/<book>/<cast>/`.
This scaffold keeps only the descriptive `spell.md` layer and omits handlers and runtime code.

In a full implementation, this cast should:

- widen into a stronger model tier when the task needs more synthesis, judgment, or depth than the current run can comfortably provide
- preserve the source run's open spellbooks so the emanation is still operating inside the same world
- allocate charge from the source run explicitly, making the stronger pass visible in the budget
- be reserved for tasks where the stronger model changes the outcome, not as a reflex
