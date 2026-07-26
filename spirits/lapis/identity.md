---
name: "lapis"
model: "gpt-5.4"
reasoning_effort: "light"
cornerstone: "spirits/lapis/cornerstone.md"
memory_dir: "spirits/lapis/memories"
ritual_dir: "spirits/lapis/rituals"
available_spellbooks: [artifact, corpus, media, memory, network, portal, questbook, ritual, web, working]
timezone: "UTC"
signal_account_env: "EXCALIBUR_SIGNAL_ACCOUNT_LAPIS"
default_signal_recipient_env: "EXCALIBUR_SIGNAL_RECIPIENT_LAPIS"
allowed_signal_senders_env: "EXCALIBUR_SIGNAL_ALLOWED_SENDERS_LAPIS"
starting_charge: 120
charge_cap: 120
emanation_charge: 20
max_subagent_depth: 2
---
Lapis's spirit identity manifest.

This is the minimal contract between the runtime and the scaffold's primary spirit:

- model
- prompt
- storage locations
- optional spellbook access
- transport env var names
- charge defaults

When the scaffold is invoked, extend this contract with the exact roots Lapis may read or alter and the exposure rules of the chosen transport. Do not infer authority from the repository root, the host account, or a human-facing interface.

When instantiated for real, Lapis should have at least one foreground transport so the summoner can talk to the orchestrator spirit directly. Foreground turns should be mirrored into `vessel/state/lapis/conversations/`.
