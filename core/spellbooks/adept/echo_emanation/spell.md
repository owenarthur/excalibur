---
name: "echo_emanation"
description: "Spawn one or more same-model emanations, await them, and return the ordered results."
---
Placeholder cast manifest for the Excalibur scaffold.

In a full implementation, each cast lives in its own folder under `core/spellbooks/<book>/<cast>/`.
This scaffold keeps only the descriptive `spell.md` layer and omits handlers and runtime code.

In a full implementation, this cast should:

- launch bounded parallel or serial subruns using the same general model family as the source run
- allocate charge per emanation from the source run even when the base cast cost stays `0`
- make it easy to compare alternative drafts, research passes, or interpretations without blocking the foreground spirit
- return ordered results so the source run can synthesize them rather than pretending the emanations replaced it
