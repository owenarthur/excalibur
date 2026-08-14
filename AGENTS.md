# AGENTS.md

This file is the starter contract for building a new Excalibur-like system from
this repository.

Read [`INVOCATION.md`](./INVOCATION.md) as well. Preserve the repository's
literary register, but treat every security and state claim literally.

## Core Shape

Keep the system simple and explicit:

- one primary spirit at first: `lapis`, unless the summoner names another
- root `README.md`, `AGENTS.md`, and `INVOCATION.md` as the human and agent
  entrance
- one `core/` tree for reviewed source and owner-controlled authority
- one `realm/` tree for spirit-controlled durable context and outputs
- one `runtime/` tree for private machine-local state
- identities and rituals under
  `core/authority/spirits/<name>/`, with memories under
  `realm/memories/<name>/`
- one shared charge ledger at `core/authority/chargebook.md`
- one universal spellbook at `core/spellbooks/adept/`
- optional capability families under `core/spellbooks/<book>/`
- one cast manifest per `core/spellbooks/<book>/<cast>/spell.md`
- portals under `core/portals/` and portable supervisor law under
  `core/services/`
- one stable external module seam under `core/extensions/`
- durable projects, research, sites, artifacts, and an optional questbook
  under `realm/`

Do not flatten the hierarchy. The distinctions are part of the design.

## Five Different Things

Do not make one control plane pretend to be everything:

- **audience** — a conversation, one continuous sitting
- **project or realm** — durable context around an intention
- **working** — bounded execution with custody
- **artifact or deliverable** — the result made for review or use
- **attention** — a review, decision, failure, approval, or intervention

An audience may mention several projects. A project may produce many workings.
A working may produce several deliverables. None of those relationships turns
the conversation into a project or the executor into an office.

Attention is not a generic notification stream. Create it only when judgment is
actually needed.

## Custody Boundaries

Every real installation must separate:

1. `core/` — reviewed source and owner-controlled authority;
2. `realm/` — spirit-controlled durable worlds and outputs;
3. `runtime/` — private machine state.

The root entrance files describe those boundaries. The invocation may choose
different absolute installation paths, but it must preserve the three roles
and may not collapse one into another.

A release may replace reviewed source and generated service material. It must
preserve the realm, projects, artifacts, memories, runtime, credentials,
conversation ledgers, and application data. Seed durable state once; never use
a routine release to reseed it.

Keep credentials outside the source and durable prose. The native supervisor
may provide exact credential references to the exact process that needs them.

## Human Operators and Spirit Authority

The human owner and declared human operators stand outside the spirit's
authority model. They may hold host administration or root because the world
is theirs to inspect, repair, change, or remove. That privilege is local to
this installation; it is not a cast, spellbook, spirit capability, or grant
over another world.

Run the primary spirit and ordinary services as dedicated non-root identities.
A spirit must not receive a root shell, passwordless general-purpose
elevation, the operator's credentials, or authority to rewrite its own
identity and core law. When privileged maintenance is genuinely needed, use a
reviewed operator action or a narrow bound helper with exact inputs and
effects.

An operator may let an installation evolve locally. Treat those changes as
real current state with provenance, not as corruption merely because they are
absent from an earlier scaffold or outside coordinator. Before an update
replaces reviewed source or service material, discover local changes and
either preserve them, incorporate them into a new local revision, or stop for
an explicit conflict decision. Never silently erase them in the name of
reconciliation.

## Primary Spirit

Use Lapis as the illustrative primary orchestrator unless the summoner chooses
another name.

The primary spirit should be:

- responsive in the foreground
- honest about state changes
- explicit before and after consequential action
- able to place long work into workings
- bounded by exact roots and real casts

Do not burden the primary spirit with every durable office.

## Foreground Audiences

Every installation needs one concrete foreground transport.

- Name and configure it; do not imply it.
- Bind locally before deliberately publishing through an authenticated path.
- Verify audience identity before a turn enters the engine.
- Mirror every inbound and outbound turn into
  `runtime/<spirit>/conversations/<local-date>.jsonl`.
- Give each audience exact order and provider continuity.
- Keep foreground conversation responsive while workings continue elsewhere.

The shared daily thread joins conversation, ritual continuity, and working
outcomes. It does not turn them into one kind of object.

## Behavioral Laws

- Answer the summoner before deeper work begins.
- Acknowledge before a cast, emanation, working, or file change.
- Report what actually happened after it lands.
- Perform real lookups when a request depends on external state.
- Never claim a write, send, search, publication, or notification succeeded
  unless it did.
- Never claim a cast ran merely because its manifest exists.
- Reconcile durable evidence before declaring a working dead.
- Treat ritual files as read-only during execution.
- Keep attention concise and consequential.

## Spellbooks and Casts

- `adept` is always open.
- Other spellbooks are optional capability families.
- A spirit advertises optional access through `available_spellbooks`.
- Rituals may widen only through declared spellbooks.
- Each cast lives in its own folder beside its manifest.
- Design spellbooks by capability family, not convenience.

An open spellbook and a bound cast are different facts. A manifest makes a
capability legible. Only a real handler or provider makes it callable. Missing
bindings fail plainly.

Human-facing controls do not bind casts and do not widen authority.

## Workings

A working is durable bounded execution, not merely a detached process.

Every full implementation should give it:

- a durable identity
- a bounded purpose and declared deliverable
- exact authority and writable roots
- an explicit model or executor policy
- one current claimant
- a renewable lease or heartbeat
- explicit cancellation
- durable checkpoints
- one honest terminal state

If a runner, supervisor, or observer disappears, inspect the durable evidence
before deciding what happened. Do not turn an observer failure into a working
failure. Do not leave an unowned process alive after declaring the work dead.

The summoner may be able to inspect or attach to the exact executor session,
but attachability is not custody. The working record is custody.

## Executors Are Not Spirits

A working may launch generic Claude, Codex, or other agents as ephemeral
executors. They receive the working's bounded task and authority, then return
evidence and deliverables.

Do not introduce knights, quest agents, or any provider-specific worker caste
as a first-class Excalibur concept. Provider sessions are implementation
details beneath workings.

An executor does not acquire:

- a named durable office
- continuing memory
- independent ritual law
- ambient host authority
- a social rank in the system

## Artifacts and Deliverables

Artifacts are what the system makes, collects, captures, publishes, or files.
They are not memories and they are not execution records.

Useful generic roots include:

- `realm/artifacts/archive/`
- `realm/artifacts/library/`
- `realm/artifacts/media/`
- `realm/artifacts/network/`
- `realm/artifacts/notes/`
- `realm/artifacts/reports/`
- `realm/artifacts/research/`

Add project-specific folders when the work warrants them. A working should
name its expected deliverable before execution begins and validate it before
claiming completion.

## Realm and Projects

The realm holds durable context around intentions: projects, sources,
decisions, research, drafts, and other material that should outlive a turn or
runner.

A project is not a queue. It may contain obligations, but those obligations do
not define the project.

Keep product code and domain material in projects rather than folding them into
the harness distribution.

## Optional Questbook

The questbook is a small, human-legible obligation and continuity ledger.

Use it when the summoner benefits from a durable list of commitments,
handoffs, reminders, or unresolved decisions. Do not make it:

- a required control plane
- a workflow engine
- an agent registry
- the owner of projects, workings, artifacts, or attention

Workings remain valid without a questbook.

## Named Spirits and Offices

Create a named spirit only when an office needs distinct continuing memory and
judgment. A spirit may steward a library, observatory, or application:

- give it an exact identity and cornerstone
- give it its own memory and narrow rituals
- name every optional spellbook
- name every root it may alter
- keep application action behind bound casts or explicit filesystem authority
- keep the application intelligible without the spirit

A human-facing application door never widens spirit authority.

A warden is conditional. Raise one only when exposure, complexity, or
stewardship warrants a durable security office. Keep the office narrow and the
rite serious. Otherwise use ordinary checks and bounded hardening workings.

## Rituals

Rituals should be readable, narrow, quiet by default, and durable in effect.
Use them for continuity, consolidation, refresh work, and recurring
stewardship. Do not use ritual prose to hide authority or spending.

## Modules and Other Boundaries

A module is an optional, versioned contribution composed with a pinned
Excalibur base. Its manifest may request spellbooks and handlers, portals,
services, spirit-office templates, rituals, static assets, migrations,
conformance tests, realm roots, external-application bridges, and typed route
endpoints. The complete contract is
`core/extensions/README.md`.

Keep the surrounding terms distinct:

- a module is the versioned contribution and lifecycle contract
- a spellbook is a capability family; a cast needs a real bound handler
- a service is a supervised process, whether supplied by the base or a module
- an external application retains its own source, data, and lifecycle
- a spirit is a durable office with its own authority, memory, and judgment
- a project is durable context in the realm
- a working is bounded execution with custody
- a deliverable is the result made for review or use

Composition is pinned base, then accepted module contributions, then explicit
local or moon authority decisions. Requested authority is not granted
authority. Mere presence never activates a module.

Modules may not apply arbitrary path overlays, collide with other
contributions, rewrite core authority, inherit ambient credentials, expose a
generic remote shell, or delete state they do not own. A constellation may
select modules and govern typed routes, but it does not replace this base
extension contract.

## Charge

Charge is the run-level continuation primitive.

- local management casts may cost `0`
- acquisition, generation, or widening paths may cost more
- emanations can have base cast cost `0` while allocating charge from their
  source run

Keep `core/authority/chargebook.md` as the single tuning surface. Charge
makes expansion visible; it does not replace authority.

## Memory

- the daily thread is the live ledger
- `realm/memories/<spirit>/long-term.md` is compact top-of-head memory
- `realm/memories/<spirit>/window/` is recent rolling memory
- `realm/memories/<spirit>/archive/` preserves lower-signal residue
- the rest of memory is durable searchable storage
- artifacts hold results, not recollection

Do not let prompt context become an undifferentiated archive.

## Runtime and Recovery

Use `runtime/<spirit>/` for conversation ledgers, workings, projections,
locks, queues, receipts, caches, and other machine records. Use
`runtime/venvs/` for helper runtimes and `runtime/backups/` for local
mirrors or rollback worktrees.

- Write state atomically.
- Preserve enough evidence to reconcile interrupted execution.
- Keep one current claimant per working.
- Use the host's native supervisor.
- Retain a verified previous source bundle and release receipt.
- Test cancellation, restart, and rollback before relying on them.

## Network and Subordinate Worlds

Bind services to loopback by default. Prefer a private authenticated mesh for
remote access. Public exposure is a separate reviewed exception.

When one world administers another:

- administrative direction is explicit
- least authority is explicit on both ends
- the administered world inherits no ambient administrator credential
- human administration and spirit-to-spirit communication remain separate
- every inter-world route is typed, authenticated, audited, revocable, and
  bounded by sender, recipient, payload, and delivery semantics
- a route grants transport, never authority inside the recipient

## Security and Cleanliness

- fail closed when authority, transport, or exposure is incomplete
- reread spirit identity at each run boundary
- keep source, durable realm, and private runtime distinct
- keep secrets out of source, realm, markdown, Git, prompts, logs, and
  artifacts
- keep mutable private state out of generated source
- keep manifests legible and reviewable
- expose nothing publicly by implication

## Standard

A new summoner should be able to answer:

- how do I talk to the primary spirit?
- where does durable project context live?
- what work is running, under whose custody, and with what authority?
- what deliverable did it produce?
- what needs my attention?
- what survives an upgrade?
- what is exposed, to whom, and why?

If those answers are muddy, the system is too muddy.

## Maintenance Rule

When the taxonomy, hierarchy, or operating laws change, update this file,
`INVOCATION.md`, and the human entrypoint in the same turn.
