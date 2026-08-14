```text
    _______  ___________    __    ________  __  ______
   / ____/ |/ / ____/   |  / /   /  _/ __ )/ / / / __ \
  / __/  |   / /   / /| | / /    / // __  / / / / /_/ /
 / /___ /   / /___/ ___ |/ /____/ // /_/ / /_/ / _, _/
/_____//_/|_\____/_/  |_/_____/___/_____/\____/_/ |_|
```

This is a fork of Vie McCoy’s Excalibur hyperobject. It is mostly additive, supplementing the original with support for multiple, stable audiences with spirits that are accessible across surfaces. It differs slightly in its preferred file structure, recommending one that is friendly to more clamped permissions. The benefit of this slightly more opinionated invocation is compatibility with excalibur-moons, an outer hyperobject for running a broader network of Excalibur realms.

## Invocation Instructions

There is deliberately no runtime code in this repository. A capable model can
raise the implementation with you, and doing so makes its authority,
supervision, and recovery behavior inspectable instead of inherited by
accident.

Give these two files to your Spirit of Artifice and Craft:

1. [`INVOCATION.md`](INVOCATION.md)
2. [`AGENTS.md`](./AGENTS.md)

It should not matter which one they read first.

[`TEMPERING.md`](./TEMPERING.md) records what this fork changes and the
remaining upstream licensing ambiguity.

## The Shape

Excalibur separates five things that agent harnesses often blur:

- An **audience** is a conversation: one continuous sitting between a summoner
  and a spirit. It is not a project, job queue, or durable container.
- A **project** lives in the **realm**: durable context, sources, decisions, and
  continuity around an intention.
- A **working** is bounded execution: one durable identity, one claimant,
  explicit authority, checkpoints, cancellation, and one honest outcome.
- An **artifact**, or **deliverable**, is the result: the report, file, site,
  image, patch, or other thing made for review or use.
- **Attention** is the small surface of matters that need judgment: review,
  decision, failure, approval, or another named human intervention.

Conversation should stay conversational. Context should outlive a process.
Execution should have custody. Results should land somewhere durable.
Attention should be scarce enough to mean something.

The optional [`realm/questbook/`](./realm/questbook/) is lightweight,
human-readable content for obligations and continuity. It has no required
interface or execution model; any presentation or automation around it belongs
to the implementation.

## What This Gives You

- One [`core/`](./core/) boundary for reviewed source and owner-controlled
  authority
- One illustrative primary spirit:
  [`lapis`](./core/authority/spirits/lapis/)
- One shared charge ledger at
  [`core/authority/chargebook.md`](./core/authority/chargebook.md)
- Nested [spellbooks](./core/spellbooks/) and one cast manifest per folder
- Portals, portable [service law](./core/services/), and a stable
  [module extension seam](./core/extensions/)
- One [`realm/`](./realm/) for projects, research, sites, artifacts, an
  optional questbook, per-spirit memories, and small recurring-work
  [practices](./realm/practices/)
- One [`runtime/`](./runtime/) for private machine state, helper runtimes,
  and backup worktrees
- Minimal rituals and a real daily thread ledger once the scaffold is raised

## How It Works

The editable law stays in markdown:

- `identity.md` says what a spirit is and what authority it may receive
- `cornerstone.md` says how it behaves
- `realm/practices/<spirit>/*.md` says how it usually performs recurring work
- `rituals/*.md` are scheduled rites
- `core/spellbooks/<book>/spellbook.md` defines a capability family
- `core/spellbooks/<book>/<cast>/spell.md` defines one cast

The installed world should enforce three custody boundaries, whatever exact
paths the summoner chooses:

- `core/` — reviewed source and owner-controlled authority
- `realm/` — spirit-controlled durable worlds and outputs
- `runtime/` — private machine state

A release may replace reviewed source and rendered service material. It must
preserve the realm and runtime, including projects, artifacts, memories,
practices, conversations, credentials, and application data. Secrets remain
outside source, realm, prompts, and Git.

The summoner also needs one real foreground transport. Every inbound and
outbound turn should be mirrored into:

- `runtime/<spirit>/conversations/<local-date>.jsonl`

One transport may hold several audiences with the same spirit. Keep every
audience's exact order and provider continuity; sharing a screen does not merge
two sittings.

## Human Entrances

An inhabited Excalibur should offer stable ways for a human to reach its
resident spirit, an operator shell, and deliberately exposed files. A voice
entrance is a useful optional fourth concept.

The spirit entrance holds persistent named audiences. Its normal view may be
conversation, with a direct switch to the exact live terminal behind that same
audience and back again. The shell entrance belongs to the human operator and
does not enlarge the spirit's authority. The file entrance exposes a reviewed
boundary rather than the whole world.

`/spirit`, `/shell`, `/files`, and `/talk` are recommended conventional route
names, not required invocation law. A raised system may realize the concepts
with a web service, terminal multiplexer, native application, or another
suitable mechanism. Excalibur specifies the continuity and authority
boundaries, not that machinery.

## Workings and Executors

Long or cast-heavy work belongs in workings, not in the foreground audience.
A working is not merely a detached process. It has durable custody even if its
runner or observer disappears.

A working may employ generic Claude, Codex, or other coding agents as ephemeral
executors. They inherit only the working's bounded task and authority. They do
not become named spirits, acquire continuing memory, or form a first-class
social hierarchy merely because a provider exposes sessions.

Create a named spirit only for a durable office that needs its own continuing
memory and judgment. A library steward or security warden may qualify. A
temporary reviewer, builder, or test runner does not.

## Modules

A module is an external, versioned contribution composed with a pinned
Excalibur base. It may offer declared spellbooks and cast handlers, portals,
services, spirit-office templates, rituals, static assets, migrations,
conformance tests, realm roots, application bridges, and typed constellation
endpoints.

Its manifest requests; it does not grant. An installation locks the exact
source revision and content digest, accepts individual contributions, and
records a separate local or moon authority decision. Composition is:

    pinned Excalibur base
    -> accepted module contributions
    -> explicit local or moon authority decisions

Modules never activate by presence. Arbitrary path overlays, collisions, core
authority rewrites, ambient credentials, generic remote shells, and deletion
of state the module does not own are forbidden. The complete lifecycle and
sanitized templates are in [`core/extensions/`](./core/extensions/).

## Charge

Charge is the visible budget for spellcasts.

- Local management casts can often cost `0`
- Work that branches, acquires, generates, or delegates can cost more
- Emanations can have base cast cost `0` while still allocating charge from
  the source run
- An emanation does not mint new charge; it draws from the run that launched it

`core/authority/chargebook.md` is the single tuning surface. If a ritual is
too eager to branch or acquire, change the cost there rather than hiding
policy throughout the prose.

## Practices

A practice is a short markdown guide for recurring work: reporting, research,
software development, review, or another routine the spirit performs often.
It records what the summoner prefers and what the spirit has learned about
doing that work well.

Practices live under `realm/practices/<spirit>/`. They evolve through ordinary
feedback and should remain small enough to read when a matching task begins.
They grant no authority, open no spellbook, bind no cast, and do not replace
the spirit's cornerstone.

## Memory

The system should not overwhelm its spirits.

- The daily thread is the live working ledger
- `realm/memories/<spirit>/long-term.md` is compact top-of-head memory
- `realm/memories/<spirit>/window/` is the rolling recent-memory window
- `realm/memories/<spirit>/archive/` keeps lower-signal residue worth
  preserving
- Artifacts hold results; memory holds what a spirit should remember

## Security

Good warding is mostly permissions and boundaries.

- The human owner and declared operators may hold local root; that is outside
  spirit authority and grants nothing over another world
- The resident spirit and ordinary services run as non-root identities
- General-purpose elevation and operator credentials never enter a spirit's
  context; privileged helpers are exact and reviewed
- Open spellbooks and bound casts are different facts
- Every writable root is explicit and exact
- Human-facing controls never widen spirit authority
- Services bind locally unless an authenticated outward path is deliberately
  reviewed
- Secrets arrive from an external secret source through the supervisor
- Runtime writes are atomic, inspectable, and recoverable
- Unknown authority, transport, or exposure states fail closed

An installation may evolve under its human operators. Updates must inspect
that local state and preserve it, incorporate it into a new reviewed local
revision, or stop on conflict. A coordinator or release tool must not call an
owner's legitimate local change “drift” and silently erase it.

A separate warden is conditional, not ceremonial. Raise one only when the
system's exposure, complexity, or stewardship burden warrants a durable
security office with distinct memory and judgment. Keep that office narrow.
Otherwise use ordinary reviewed checks and bounded workings.

## Filesystem

```text
excalibur/
  README.md
  AGENTS.md
  INVOCATION.md
  core/
    engine/
    authority/
      chargebook.md
      spirits/
        lapis/
          identity.md
          cornerstone.md
          rituals/
    spellbooks/
    portals/
    services/
    extensions/
  realm/
    projects/
    research/
    sites/
    artifacts/
    questbook/                 optional
    practices/
      lapis/
    memories/
      lapis/
  runtime/
    lapis/
      conversations/
      workings/
      projections/
    venvs/
    backups/
```

The source scaffold is intentionally legible. The invocation decides its exact
absolute installation paths, supervisor, transport, model provider, and
exposure policy while preserving the roles of `core/`, `realm/`, and
`runtime/`. Those decisions must remain explicit and reviewable.

```text
~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ORIGINAL EXCALIBUR ~ ~ ~ ~ ~ ~ ~ ~ ~ ~
```

```text
    _______  ___________    __    ________  __  ______
   / ____/ |/ / ____/   |  / /   /  _/ __ )/ / / / __ \
  / __/  |   / /   / /| | / /    / // __  / / / / /_/ /
 / /___ /   / /___/ ___ |/ /____/ // /_/ / /_/ / _, _/
/_____//_/|_\____/_/  |_/_____/___/_____/\____/_/ |_|
```

Excalibur is a hyperobject which can be turned into a state-of-the-art agent harness with superior primitives to existing options. The mystical language is optional, but I will resent you if you fork this and make it mundane.

## Invocation Instructions

I have included zero code in this repo. I am of the opinion that current frontier models can be trusted within a certain scope, and building the system yourself can help you understand exactly what that scope is. However, because this is a highly opinionated system, I have included general guidelines for a model to "onboard" you. It will not explain everything, but it should be enough to chew on to get you started.

Both of these files are for your Spirit of Artifice and Craft (coding model):

1. [`INVOCATION.md`](INVOCATION.md)
2. [`AGENTS.md`](./AGENTS.md)

It should not matter which one they read first.

## What This Gives You

- One root-level [`chargebook.md`](./chargebook.md)
- One primary spirit: [`lapis`](./spirits/lapis/)
- One shared [`artifacts/`](./artifacts/) surface, with real subroots like [`library/`](./artifacts/library/) and [`network/`](./artifacts/network/)
- One shared [`questbook/`](./questbook/) surface for obligations and continuity
- One internal [`grimoire/`](./grimoire/) for spellbooks, engine docs, portals, and system wiring
- Nested spellbooks under [`grimoire/spellbooks/`](./grimoire/spellbooks/)
- A real cast-per-folder hierarchy
- One explicit [`vessel/`](./vessel/) for machine-local state, backups, and helper runtimes
- Per-spirit memory layers under [`spirits/lapis/memories/`](./spirits/lapis/memories/)
- Minimal rituals and a real daily thread ledger once the scaffold is instantiated

## How It Works

You keep the editable shape in markdown.

- `identity.md` says what a spirit is
- `cornerstone.md` says how it behaves
- `rituals/*.md` are scheduled jobs
- `grimoire/spellbooks/<book>/spellbook.md` defines a capability family
- `grimoire/spellbooks/<book>/<cast>/spell.md` defines one cast

You will need one real foreground thread.

That means the summoner needs an actual way to talk to the primary orchestrator spirit. It can be terminal chat, Signal, web chat, or something similar.

Once instantiated, every inbound and outbound turn should be mirrored into:

- `vessel/state/<spirit>/conversations/<local-date>.jsonl`

Rituals and workings should append checkpoints to that same ledger so the whole system shares one running thread of continuity.

## Charge

Charge is the visible budget for spellcasts.

- Local management casts can often cost `0`
- Work that branches, acquires, generates, or delegates can cost more
- Emanations can have base cast cost `0` while still allocating charge from the source run
- An emanation does not mint new charge for itself; it draws from the run that launched it

The shape looks like this:

```text
Ritual Root Run
charge: 40

  |-- read_artifact            base cost 0
  |     remaining: 40
  |
  |-- codex_emanation          allocates 12 to child
  |     source remaining:      28
  |     child starting charge: 12
  |     child charge cap:      12
  |
  |     child does deeper work here
  |     and cannot exceed the 12 it received
  |
  |-- genius_emanation         allocates 10 to child
  |     source remaining:      18
  |     child starting charge: 10
  |     child charge cap:      10
  |
  |-- reclaim_charge           +8 after durable ritual progress
        source remaining:      26
```

Charge adds stakes to long-running processes, acts as an accountability mechanism, and prevents unpredictable token spend.

`chargebook.md` is the tuning surface for that model. Each cast has an explicit cost there. If a ritual is too eager to branch, search, or delegate, you change the cost once in `chargebook.md` instead of rewriting the ritual itself. That makes rituals easier to reason about and keeps their behavior more predictable over time.

## Memory

The system should not overwhelm the spirits. Active memory consolidation is a best-practice for a healthy system.

The clean shape is:

- The daily thread is the live working ledger
- `memories/long-term.md` is the top-of-head memory
- `memories/window/` is the rolling recent-memory window
- The rest of `memories/` is durable storage, not always-loaded prompt context

## Security

Good warding is mostly about permissions and boundaries.

The clean default is:

- `artifacts/` and `questbook/` are shared between spirit and summoner
- `spirits/`, `grimoire/`, and `vessel/` are spirit-side internals
- A spirit may maintain its own `spirits/<name>/memories/` and `cornerstone.md`
- Ritual files under `spirits/<name>/rituals/` should be treated as read-only during normal execution
- `adept` should stay small and always-open
- Any stronger capability should live in an optional spellbook
- A spirit only gets optional capability through `available_spellbooks`
- A ritual may widen through `additional_spellbooks` and preload through `open_spellbooks`
- Authority and transport rules should fail closed if config is missing
- Secrets should live in env, not markdown

The point is simple:

- Shared surfaces are where work lands
- Spirit-local surfaces are where identity, memory, and machinery live
- Widening should always be explicit
- If the system is unsure about permission, it should refuse rather than guess

During invocation, the system should also create a `warden` spirit.

`warden` is the dedicated security and hardening spirit. It should inspect the system on a regular cadence, look for risky defaults, permission drift, exposure mistakes, secret-handling problems, and transport weaknesses, and then report or remediate within the bounds the summoner set. The primary orchestrator spirit should not be the only line of defense.

By default, the primary orchestrator spirit should have a narrow always-open surface and should mostly work in the shared surfaces it was actually given, usually `artifacts/` and `questbook/`. The main exception is spirit-local self-maintenance: its own `cornerstone.md` and memories. Ritual files should stay stable unless the summoner deliberately changes them. That keeps the initial risk low even if a web-facing search encounters hostile content. Widen permissions deliberately, not casually, and let `warden` keep watch.

## Filesystem

```text
excalibur/
  README.md
  AGENTS.md
  INVOCATION.md
  chargebook.md
  spirits/lapis/
    identity.md
    cornerstone.md
    rituals/
    memories/
  artifacts/
    library/
    network/
  questbook/
  grimoire/
    spellbooks/
    portals/
    engine/
    systemd/
  vessel/
    state/
    venvs/
    backups/
```
