# Lapis runtime

Machine bookkeeping lives here in a full installation.

The daily thread is one of its central records:

- `runtime/lapis/conversations/<local-date>.jsonl`

Use this root for Lapis's audiences, workings, projections, checkpoints,
locks, queues, receipts, caches, and other runtime evidence. Write it
atomically and preserve enough to reconcile an interrupted run honestly.

Keep helper runtimes in `runtime/venvs/` and local mirrors in
`runtime/backups/`.
