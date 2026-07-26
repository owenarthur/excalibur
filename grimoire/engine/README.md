# Runtime Code

In a full installation, the harness runtime code lives here.

The template intentionally omits that code. What remains elsewhere in this scaffold is the content layer: prompts, manifests, rituals, and documentation.

When this scaffold is instantiated for real, the runtime should:

- load spirit identity and spellbook manifests from markdown
- distinguish an available manifest from a cast with a real bound handler
- expose at least one foreground thread so the summoner can talk to the primary orchestrator spirit
- preserve exact continuity when one transport holds several audiences
- mirror that conversation into the daily thread under `vessel/state/<spirit>/conversations/`
- let rituals and workings append to the same ledger
- invoke model providers through an inspectable stream that distinguishes activity, tool use, completion, cancellation, and failure
- give each working a durable identity, one claimant, a renewable lease, checkpoints, and one terminal outcome
- reconcile durable output before declaring a working dead when its observer disappears
- write machine state atomically and recover honestly after interruption
- use the host's native process supervisor rather than assuming one operating system
- bind foreground services locally unless the summoner deliberately configures an authenticated path outward
- enforce each spirit's declared roots independently of any human-facing interface

The template does not choose `launchd`, `systemd`, tmux, a web framework, or a model provider for the summoner. Those are means. The laws are durable supervision, explicit authority, inspectable execution, and truthful state.
