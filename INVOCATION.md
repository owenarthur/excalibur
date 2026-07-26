# INVOCATION.md

Give this file to the spirit that will instantiate the scaffold.

```text
+--------------------------------------------------+
|                  HYPEROBJECT                     |
|         summon the scaffold with care            |
+--------------------------------------------------+

You are being summoned to raise a living system from this scaffold. Make sure to consume both INVOCATION.md and AGENTS.md before exploring the scaffold.

Treat the markdown hierarchy in this repository as the source of truth.
Do not flatten it. Do not improvise around it. Read it, preserve it, and instantiate from it.

You are not being asked to clone a private machine.
You are being asked to turn a clean manifest scaffold into a secure, legible system for a new summoner.

Laws of the rite:

- Keep the system secure by default.
- Preserve the spellbook architecture.
- Keep markdown editable and human-legible.
- Keep one primary spirit at first: `lapis`.
- Keep advanced surfaces optional unless the summoner explicitly wants them.
- Do not insert secrets, personal residue, or live infrastructure assumptions into the scaffold.
- `adept` is the universal always-open spellbook. Other spellbooks are the capability surface. Charge is a visible budget, not hidden magic.
- The primary spirit is not abstract. The summoner must have a real foreground thread to speak through.

Proceed in this order.

First circle: secure the ground

- Inspect the repository before making assumptions.
- Confirm the scaffold shape and the nested spellbook layout.
- Keep fail-closed defaults where transport, authority, or exposure rules matter.
- Do not widen the primary surface just because a feature exists in the scaffold.

Second circle: enter plan with the summoner

- Switch into plan mode before building the real system.
- Ask the summoner for the preferences that actually determine the build:
  - transport choices
  - the host's native process supervisor and restart behavior
  - how model runs will be invoked, observed, and stopped
  - storage roots
  - timezone
  - model choices and names (lapis can be renamed, but encourage the summoner to choose wisely)
  - domain and exposure preferences
  - whether one foreground transport should hold more than one distinct audience
  - whether the summoner needs to attach to long-running work
  - whether an existing library, observatory, workshop, or other application should receive a resident spirit
  - whether questbook, portals, network artifacts, corpus access, and other optional spellbooks should be active at the start
  - whether `lapis` should stay the primary spirit unchanged or be reshaped
- Do not hardcode these choices if the summoner has not made them.

Third circle: instantiate the scaffold

- Build the runtime from the markdown manifests.
- Keep `identity.md`, `cornerstone.md`, rituals, spellbooks, casts, and chargebook legible.
- Keep `chargebook.md` as the clear tuning surface for cast costs so ritual behavior stays predictable.
- Instantiate at least one real foreground transport for the primary spirit. This can be terminal chat, Signal, web chat, or another explicit thread surface, but it must be concrete and operable.
- Make the summoner-to-spirit path obvious. The summoner should be able to answer one question cleanly: "how do I talk to my orchestrator spirit?"
- Prefer the machinery native to the ground on which the system stands. A Mac may use `launchd`; a Linux host may use `systemd`. The law is not the supervisor's name. The law is that foreground threads, rituals, and workings survive restart and can be inspected without divination.
- Bind a new foreground service locally unless the summoner deliberately chooses an authenticated path outward. A convenient interface is not permission to widen exposure.
- Keep model execution structured enough to distinguish acceptance, activity, tool use, completion, cancellation, and failure. Do not infer a living run from an old process record or infer failure merely because one observer disappeared.
- Create the shared daily thread ledger under `vessel/state/<spirit>/conversations/<local-date>.jsonl`.
- Mirror every inbound and outbound foreground turn into that daily thread.
- Make rituals and workings append checkpoints and durable outcomes into that same daily thread so the foreground spirit and the background system stay part of one mind.
- Preserve the nested shape:
  - `grimoire/spellbooks/<book>/spellbook.md`
  - `grimoire/spellbooks/<book>/<cast>/spell.md`
- Preserve the layered memory model:
  - daily thread as the live ledger
  - `memories/long-term.md` as compact top-of-head memory
  - `memories/window/` as the rolling recent-memory window
  - the rest of `memories/` as durable searchable storage
- Allow the primary spirit to maintain its own `cornerstone.md` and memories if the summoner wants adaptive behavior.
- Do not let ordinary execution rewrite ritual files.
- Keep `adept` universal and always open.
- Keep optional spellbooks openable according to `available_spellbooks`.
- Keep the distinction between an open spellbook and a bound cast honest. A manifest may describe a capability whose provider is absent. Refuse that cast plainly instead of pretending the description performed the work.
- Keep long work in workings instead of blocking the foreground thread.
- A working is not merely a process sent into the dark. Give it a durable identity, one living claimant, a renewable lease, and an honest terminal state. If its keeper disappears, reconcile the work before declaring it dead.
- Write machine state atomically and keep enough evidence to recover after interruption. A restart should not turn uncertainty into a false success or a false failure.
- Keep the daily thread as the shared ledger across conversation, rituals, and workings.
- If one transport holds several audiences with the same spirit, preserve each audience's exact continuity. Do not merge two sittings merely because they share a spirit or a screen.
- If the summoner chooses a transport that supports notifications, keep user-facing updates honest and non-spammy.

Fourth circle: raise the WARDEN SPIRIT

- After the initial system stands, create a second spirit.
- The WARDEN SPIRIT must be a real cybersecurity specialist, not a generic assistant with a security label.
- Give the WARDEN SPIRIT a strong model and ask the summoner to give them a name.
- Create a weekly hardening ritual for the WARDEN SPIRIT.
- The weekly rite should inspect the live system for exposure, secret handling, authentication posture, network assumptions, risky defaults, and other obvious hardening gaps.
- Keep the WARDEN's purpose narrow and serious.

Fifth circle: let other spirits take office

- Raise additional spirits only after the primary foreground thread and the WARDEN SPIRIT stand on firm ground.
- Some spirits may dwell within a library, observatory, workshop, or other living application. Give such a spirit its own identity, memories, rituals, and narrow spellbooks.
- A dwelling does not grant dominion. Name every root the resident spirit may alter and every cast by which it may act.
- Keep the application intelligible without the spirit, and keep the spirit bounded without relying on the application's human interface.
- A door made for the summoner does not widen a spirit's authority.
- Give each resident spirit a real office. Do not multiply generic assistants merely because the harness can hold them.

Sixth circle: close cleanly

- Summarize what you built.
- Name what remains unbound or intentionally deferred.
- Surface the next hardening steps plainly.
- Do not pretend unfinished infrastructure is complete.
```
