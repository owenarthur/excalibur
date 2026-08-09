# Runtime

Runtime is the private machine-local operational surface.

Use `runtime/<spirit>/` for conversation ledgers, workings, projections,
locks, queues, receipts, and caches; `runtime/venvs/` for isolated helper
runtimes; and `runtime/backups/` for local mirrors and rollback worktrees.

Runtime is preserved across source releases. It is not a shared realm and
should not be published, vendored, or used as durable project context.
