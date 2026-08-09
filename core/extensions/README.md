# Module extension seam

A module is an optional, versioned contribution to an Excalibur installation.
It can add a capability without editing the pinned Excalibur base. A module is
not a project, external application, spellbook, service, or spirit:

- a project is durable context in the realm
- an external application keeps its own source, data, and lifecycle
- a spellbook is a family of named casts; a cast is callable only when a real
  handler is bound
- a service is one process under the host's native supervisor
- a spirit is a durable office with distinct identity, memory, and judgment
- a module may contribute declared pieces of those things, subject to a
  separate acceptance decision

The base repository remains a zero-code hyperobject. An implementation raised
from it must enforce this contract before it can claim module support.

## Manifest and lock

Every module has one versioned manifest. The installation has a separate lock
that records:

- module id and semantic version
- immutable source reference and exact revision
- content digest over the acquired module bundle
- compatible Excalibur base interface and revisions
- accepted contribution ids
- the exact local or moon authority decision

The source may be an archive, package, or repository reference. Excalibur does
not require vendoring or a Git submodule. Presence in a directory, a lock
entry, or a successful download never activates a module.

The manifest declares:

- inputs and external requirements
- outputs and expected deliverables
- every contribution and its module-relative source
- requested realm roots and other authority
- authority it must never receive
- state it owns, state it may only read, and state it must preserve
- secrets by external reference and the exact consumer of each reference
- health and conformance checks
- staging, migration, promotion, verification, rollback, disable, and removal
  behavior

The sanitized templates beside this file show the minimum shape. They are
examples, not active modules or locks.

## Supported contributions

A module may offer only these contribution classes:

- spellbook manifests and their separately identified cast handlers
- portals
- native-supervisor service material
- optional spirit-office templates
- rituals attached to a spirit office the summoner has already accepted
- static assets
- ordered, reversible migrations
- conformance tests
- requested realm roots
- bridges to external applications
- typed route endpoints when a constellation contract exists

Each contribution has a stable id. Source paths are relative to the verified
module bundle. The implementation maps accepted contributions into rendered
destinations; a module may not supply an arbitrary filesystem overlay.

A bridge does not absorb an external application's code or data into
Excalibur. It names the application interface, the direction of access, the
bounded data classes, and the authority needed to cross that boundary.

A spirit-office template does not create a spirit by itself. Acceptance names
the office, its identity, memory root, rituals, spellbooks, writable roots,
provider and spending policy, service, and audience path. Provider sessions
remain ephemeral executors beneath workings.

Route endpoints are inert unless a constellation separately selects the
module and both endpoint worlds accept an identical typed route contract.
Transport grants movement, never recipient authority.

## Composition and authority

Composition order is fixed:

1. pinned Excalibur base
2. accepted module contributions
3. explicit local or moon authority decisions

Later layers may narrow an earlier layer. They may not silently widen it.
Requested authority is not granted authority.

Validation must fail closed on:

- an unknown manifest or interface version
- a source or content-digest mismatch
- an undeclared contribution
- duplicate ids or destination collisions
- an arbitrary path overlay
- an attempt to replace base files or rewrite core authority
- a ritual attached to an unaccepted spirit
- a cast handler without its manifest, or a manifest that is claimed bound
  without a real handler
- a service or migration outside its accepted roots
- an undeclared secret, ambient credential inheritance, or secret value in
  source, realm, prompts, logs, receipts, or the lock
- a generic remote shell
- an undeclared route endpoint or message class

If two accepted contributions target the same rendered destination, the
composition is invalid. Local authority may reject either contribution; it
may not resolve the collision through order-dependent overwrite.

## Lifecycle

The only valid promotion sequence is:

    acquire -> stage -> validate compatibility, digest, collisions, and authority
    -> render -> test -> explicit promote -> verify -> receipt

Acquisition and staging are inert. Promotion requires a distinct reviewed
decision. A receipt records the pinned base, module lock, authority decision,
rendered digest, migrations, checks, preserved roots, and previous release.

Migrations declare exact inputs, outputs, owned state, preconditions,
postconditions, backup point, reversal, and failure behavior. They run only
during an explicit promotion and never infer state ownership from a writable
parent directory.

Rollback restores the previous reviewed source and rendered service material.
It preserves realm, runtime, memories, credentials, conversation ledgers,
application data, databases, and module-owned state unless a separately
reviewed state migration explicitly says otherwise.

Disable stops module entrypoints and removes their rendered bindings while
retaining state. Uninstall may remove source and replaceable rendered
material. It may delete durable state only when the contract names that exact
state as module-owned and the summoner separately approves the deletion.
Neither operation may delete borrowed, shared, external-application, realm, or
runtime state it does not own.

## Implementation standard

An implementation that supports modules must:

- parse and validate the manifest and lock before rendering
- verify immutable references and digests before reading contributions
- allow only the contribution classes above
- compute collisions before any promotion
- compare requested authority with an explicit acceptance record
- keep secret values external and deliver references only to named consumers
- run negative conformance tests for authority and collision refusal
- stage and render outside live roots
- promote atomically through the host's native supervisor
- verify health after promotion and exercise rollback
- emit an inspectable receipt

If those checks are descriptive rather than enforced, the module is not bound.
