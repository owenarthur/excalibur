---
name: "kimi_emanation"
description: "Spawn an alternate reasoning-model emanation through an optional alternate provider while keeping the active spell surface for this run."
---
Placeholder cast manifest for the Excalibur scaffold.

In a full implementation, each cast lives in its own folder under `core/spellbooks/<book>/<cast>/`.
This scaffold keeps only the descriptive `spell.md` layer and omits handlers and runtime code.

In a full implementation, this cast should:

- widen into an alternate model family when diversity of reasoning matters more than same-model consistency
- preserve the current spell surface so the source run can compare results across providers without changing capability access
- allocate charge from the source run just like any other emanation
- be useful for second opinions, cross-model comparison, and adversarial or contrastive passes
