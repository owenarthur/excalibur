# INVOCATION.md

Give this file to the spirit that will instantiate the scaffold.

```text
+--------------------------------------------------+
|                  HYPEROBJECT                     |
|         summon the scaffold with care            |
+--------------------------------------------------+

You are being summoned to raise a living system from this scaffold. Consume
both INVOCATION.md and AGENTS.md before exploring the rest.

The markdown hierarchy is law and material, not an implementation. Preserve
its voice and distinctions while building the smallest complete system that
serves this summoner.

You are not being asked to clone another person's machine.
You are being asked to turn a clean scaffold into a secure, legible world.

Laws of the rite:

- Keep the system secure by default.
- Keep markdown editable and human-legible.
- Keep one primary spirit at first: lapis, unless the summoner names another.
- Keep advanced surfaces optional until they are wanted.
- Do not insert secrets, personal residue, or live infrastructure assumptions.
- Keep adept universal and always open; other spellbooks are explicit capability.
- Keep charge visible.
- Keep the human operator's root distinct from the spirit's authority. Run the
  spirit and ordinary services as non-root identities.
- Preserve `core/`, `realm/`, and `runtime/` as separate custody
  boundaries even when their absolute installation paths differ.
- Give the summoner one real foreground path to the primary spirit.
- Treat audiences as conversations, realms and projects as durable context,
  workings as bounded execution, artifacts as deliverables, and attention as
  review or judgment that cannot be completed safely in the background.

Proceed in this order.

First circle: secure the ground

- Inspect the repository, host, and existing operator law before making
  assumptions.
- Inventory existing users, services, networks, data, supervisors, and trust
  boundaries without changing them.
- Confirm what the summoner controls and what remains a protected peer.
- Identify the humans who may operate the world, whether they hold local root,
  and which human actions must remain impossible for the spirit.
- Fail closed where authority, transport, exposure, or secret handling is
  unknown.
- Do not widen the primary spirit merely because a capability exists.

Second circle: enter plan with the summoner

- Ask only for choices that materially determine the build:
  - the foreground transport
  - the host's native supervisor and restart behavior
  - model providers and how runs are invoked, observed, cancelled, and stopped
  - the absolute roots corresponding to `core/`, `realm/`, and `runtime/`
  - timezone
  - the primary spirit's name and office
  - network exposure and authenticated access
  - what should create attention and how the summoner receives it
  - whether long work needs an attachable executor session
  - which optional spellbooks or portals should be open initially
  - whether any external module should be considered, and from which immutable
    source and digest
  - whether the lightweight questbook is useful
  - whether any existing domain truly needs a resident spirit
- Do not hardcode an unanswered security-significant choice.

Third circle: establish custody

- Give reviewed source and owner-controlled authority the `core/` role.
- Give spirit-controlled durable context and outputs the `realm/` role.
- Give private machine state the `runtime/` role.
- Place projects and their durable context in the realm.
- Place completed or reviewable results in `realm/artifacts/`.
- Keep credentials, provider state, locks, caches, queues, and conversation
  ledgers in private runtime or an external secret store.
- A release may replace reviewed source and rendered service definitions. It
  must not replace realm, artifacts, memories, runtime, credentials, or
  application data.
- Seed durable state at most once. Upgrades preserve it by construction.
- Write runtime records atomically and keep enough evidence to recover after
  interruption without inventing success or failure.
- Treat owner-made local changes as current installation state. An update must
  inspect and preserve them, incorporate them into a reviewed local revision,
  or stop on conflict; it must not silently restore an earlier scaffold.

Fourth circle: raise one complete path

- Instantiate one primary spirit and one foreground transport before adding
  breadth.
- Run the spirit and ordinary services under dedicated non-root identities.
  Keep general-purpose root and operator credentials out of the spirit's
  context; expose only exact reviewed helpers when privileged maintenance is
  necessary.
- Make the answer to "how do I talk to my spirit?" concrete.
- Mirror every inbound and outbound turn into
  runtime/<spirit>/conversations/<local-date>.jsonl.
- Preserve exact continuity when one transport holds several audiences.
- Reread the spirit's identity for every run. Changing identity is changing
  authority; do not cache it past that boundary.
- Bind a new service to loopback first. Publish it only through a reviewed,
  authenticated path.
- Use the host's native supervisor. A Mac may use launchd; a Linux host may use
  systemd. The law is durable, inspectable supervision, not either name.
- Keep provider execution structured enough to distinguish acceptance,
  activity, tool use, completion, cancellation, and failure.

Fifth circle: bind casts truthfully

- Preserve the nested spellbook shape:
  - core/spellbooks/<book>/spellbook.md
  - core/spellbooks/<book>/<cast>/spell.md
- Keep adept always open.
- Keep optional spellbooks openable only through declared availability.
- Keep an open spellbook distinct from a bound cast. A manifest can describe a
  capability whose handler is absent; refuse it plainly.
- Treat a human-facing button, form, or shell as a user interface, never as a
  way around spirit authority.
- Keep secrets outside source, realm, markdown, prompts, and Git. Let the
  supervisor provide only the external credential references a service
  actually needs.

Sixth circle: compose modules without widening the base

- Read `core/extensions/README.md` before accepting any external module.
- Require one versioned manifest and an immutable source, revision, and content
  digest in the module lock. Do not require vendoring or a Git submodule.
- Accept contribution ids individually. Mere presence, download, or lock
  entry never activates a module.
- Compose in this order: pinned Excalibur base, accepted module
  contributions, then explicit local or moon authority decisions.
- Reject arbitrary path overlays, collisions, core-authority rewrites,
  ambient credentials, generic remote shells, and undeclared route endpoints.
- Keep external applications external. A bridge declares its interface and
  bounded data movement; it does not absorb application code or data.
- Stage, validate compatibility, digest, collisions, and authority, render,
  test, explicitly promote, verify, and write a receipt.
- Rollback preserves realm, runtime, credentials, application data, and
  module state. Disable or uninstall may not delete state the module does not
  own.

Seventh circle: give long work custody

- Keep long or cast-heavy work out of the foreground audience.
- Give every working a durable identity, bounded task, exact writable roots,
  model policy, one claimant, renewable lease, checkpoints, cancellation, and
  one terminal state.
- Let a generic Claude, Codex, or other coding agent execute a working when
  useful. The executor is ephemeral. It does not gain a named office,
  continuing memory, or authority beyond the working.
- If an observer or runner disappears, reconcile the durable evidence before
  declaring the working dead.
- Land the result as an artifact or another named deliverable.
- Raise attention only for review, decision, failure, approval, or another
  intervention that truly requires judgment.

Eighth circle: decide whether another spirit is warranted

- A named spirit is a durable office with distinct continuing memory and
  judgment, not a provider session or worker label.
- Raise a resident spirit only when an enduring library, observatory,
  application, or other domain benefits from that office.
- A dwelling does not grant dominion. Name every root and cast.
- A separate warden is conditional. Raise one only when exposure, complexity,
  or stewardship warrants a durable security office. Keep it narrow and give
  it a serious recurring hardening rite.
- Otherwise run hardening as ordinary reviewed checks and bounded workings.

Ninth circle: close cleanly

- Demonstrate one real conversation, one bounded working, one deliverable, and
  one recovery or cancellation path.
- Summarize what was built.
- Name what remains unbound, deferred, or awaiting attention.
- Do not call described infrastructure complete until it has run.

Patterns that have served well

1. Private foreground surface

   listener: loopback only
   publication: authenticated private mesh
   audience identity: verified before the turn enters the engine
   ledger: runtime/<spirit>/conversations/<local-date>.jsonl
   public ingress: absent unless separately reviewed

2. Bounded working

   acknowledge -> record working -> claim -> execute -> checkpoint
   -> validate deliverable -> commit terminal outcome -> return attention if needed

   The process is replaceable. The working record and deliverable are not.

3. Seed-once release

   reviewed source + rendered service bundle -> stage -> verify -> promote
   realm + runtime + secrets + application data -> preserve untouched
   previous source bundle + receipt -> rollback path

4. Constellation member

   human operator root remains local to this world
   resident spirit and ordinary services remain non-root
   outer administration is separate from spirit-to-spirit communication
   every data route is explicit, typed, authenticated, audited, and revocable
   transport grants movement, never recipient authority

5. Ephemeral executor

   working task + bounded roots + model policy -> generic executor
   executor completion -> evidence and deliverable
   no durable office, memory, or ambient host authority

6. External module

   pinned base + verified module lock + accepted contributions
   -> explicit authority decision -> inert stage -> validate and render
   -> test -> reviewed promotion -> health verification + receipt
   disable and rollback -> preserve every state root not separately owned
```
