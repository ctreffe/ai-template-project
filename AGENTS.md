# AGENTS.md

Resident contract.

## Safety

- Inspect repository, branch, worktree and staging; preserve changes,
  selections and unrelated work.
- Maintainers own intent, scope and consequential decisions.
- Authorized reads and edits are allowed. Commits, tags, pushes, pulls, merges,
  rebases, resets, reverts, branches, stashes, destructive restores and direct
  `.git/` changes each require an instruction containing `explicit`,
  `explicitly` or German `explizit`.
- When such a control-word instruction is needed, propose one minimal copy-ready
  wording that names the exact action, repository and material consequence;
  the proposal is not authorization.
- Ask before installation, privilege, external operations, outside writes or
  transmission; access, versioning and publication are separate.
- Retry once only if plausibly transient. On recurrence or setup/policy error,
  pause; use `troubleshoot-environment`; describe the problem and ask whether
  to exit for an ordinary quick workaround or resolve the cause. Explicit
  maintainer invocation enters focused resolution directly. Verify a repair
  only by continuing the originally blocked operation.
- `input/intake/` grants no access; keep `input/` unchanged. Registered
  `materials/` and unrestricted `temp/` are readable; never version temporary
  content or inspect `temp/restricted/`. Synchronization grants no access.

## Routing

- Bounded work uses `start-task`, `TASK_HANDOFF.md`, targets and checks. Load
  `PROJECT_CONTEXT.md` only for project-wide state or
  unresolved scope.
- Read `COLLABORATION.md` for initialization, full review, authority
  conflicts or collaboration-model changes. Load `REPOSITORY.md`,
  `DOCUMENTATION.md`, `PHILOSOPHY.md`, `SYNCHRONIZED_STORAGE.md` and domain
  guidance only when applicable.
- Read `DECISIONS.md` and applicable records before durable changes.
- Task entry, handoff, ordinary commits and Decision Records route
  automatically. Invoke initialization, review, template sync,
  consistency checks, retrospectives, local creation and `commit-milestone`
  explicitly.
- Keep the template generic. Resolve material guidance conflicts before
  consequential work.

## Validation

Scale evidence by stage: an acceptable bounded change needs the smallest useful
review, an ordinary commit needs targeted evidence for a good reviewable state,
and a milestone commit owns comprehensive applicable checks. Automated tests,
whitespace checks, broad renders, links and bilingual scans are not defaults
before the milestone unless affected or required by a stated material risk.
Report outcomes, limits and deferred checks truthfully.
