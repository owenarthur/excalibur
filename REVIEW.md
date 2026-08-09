# Second Tempering Review

This branch is a review-only proposal. It does not open a pull request, grant a
license, publish a distribution, or authorize a merge or installation.

## Exact review anchors

- Base: `7db9c66f1f6515eefe0f7259fe60596b5a761feb`
  (`origin/master` and `upstream/main` when this review was prepared).
- Substantive source head: `48ab2afafcd9d0211ca130504dd1179333bc9a80`.
- Review range: `7db9c66f1f6515eefe0f7259fe60596b5a761feb...48ab2afafcd9d0211ca130504dd1179333bc9a80`.
- Published comparison, once Owen chooses to inspect it:
  <https://github.com/owenarthur/excalibur/compare/master...second-tempering>

The branch-tip commit refreshes this guide after the substantive source head.
For the exact branch tip, use `git rev-parse second-tempering`; for the complete
proposal, compare `origin/master...second-tempering`.

## Conceptual sequence

1. `c0bca75` gives workings durable custody and recovery law.
2. `e702a8e` tempers invocation around audiences, durable realm, and bounded
   execution.
3. `6d59ea9` distinguishes deliverables, attention, optional questbook
   continuity, named offices, and ephemeral executors.
4. `5aa03ad` establishes the `core/`, `realm/`, and `runtime/` custody boundary
   and adds the versioned module-extension contract.
5. `4bbc9be` adds the initial review guide.
6. `48ab2af` makes each example cast handler an individually accepted
   contribution and explicitly denies deletion of unowned state.
7. The branch-tip commit refreshes only this review guide.

## Review order

1. Read `AGENTS.md`, `INVOCATION.md`, and `README.md` for the operating model.
2. Review `core/extensions/` for module composition, authority, lifecycle,
   rollback, and the sanitized contract examples.
3. Check `core/authority/`, `core/spellbooks/`, `core/portals/`, and
   `core/services/` for agreement with the custody model.
4. Check `realm/` and `runtime/` for preservation boundaries and the absence of
   committed private state.
5. Read `TEMPERING.md` for design rationale, unresolved questions, and the
   publication warning.

The upstream repository contains no license file. Merge, release, and
redistribution therefore remain unresolved decisions for Owen and the upstream
author; this branch makes no claim that those rights are settled.
