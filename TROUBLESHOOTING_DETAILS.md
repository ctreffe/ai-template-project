# Environment Troubleshooting

This repository-local registry supports `reuse-fixes`: look up confirmed
corrections before repeating a failed approach and retain concise prevention
after verified recovery. Known cases need no mandatory route-choice menu.
A useful verified task-local adaptation may be retained with its limits; do not
claim permanent environment repair without evidence.

Reuse an entry only when its stable signature and current applicability match.
Use a safe diagnostic when needed. A recorded fix grants no access, privilege,
installation, global configuration, Git, transmission or publication authority.
Historical evidence does not establish readiness on a new clone or device.

Use only the current repository's records; do not inspect or transfer another
repository's failure history or maintain global memory. Host-specific facts
belong in ignored `TROUBLESHOOTING.local.md`.
Never store secrets or sensitive source content.

## Entry Schema

New or substantively updated entries record the fields below. Preserve existing
historical evidence; add prevention when an entry is next usefully updated.
Keep records compact and reusable rather than logging every recurrence.

- **Stable signature:** The failure and execution stage that identify the case.
- **Applicability:** Relevant platforms, repositories and prerequisites.
- **Cause:** A confirmed cause, not a guess presented as fact.
- **Safe diagnostic:** Bounded evidence needed to confirm or reject applicability.
- **Durable repair:** The confirmed correction, including limits of a local adaptation.
- **Authorization needs:** Required action and platform approvals.
- **Prevention:** The smallest rule that changes the next attempt before failure.
- **Verification:** The original normal operation that demonstrated recovery.
- **Last confirmed:** ISO date and sanitized evidence scope.
- **Unresolved marker:** Only for a useful open case; retain its smallest next step.

## KI-0001: Windows sandbox Git ownership check blocks a repository

- **Stable signature:** A normal Git operation in an authorized repository
  stops with `fatal: detected dubious ownership in repository` when the process
  runs under a Windows sandbox identity different from the repository owner.
- **Applicability:** Native Windows Codex tasks whose filesystem policy already
  permits the intended repository access and whose Git process uses the
  maintainer's global Git configuration. Filesystem setup failure is separate.
- **Cause:** Git independently protects repositories owned by another identity.
  Command-scoped trust for an active workspace does not automatically cover an
  authorized sibling repository.
- **Safe diagnostic:** Inspect `git config --show-origin --show-scope --get-all
  safe.directory`. For an exact already-authorized repository, retry only the
  failed read-only query with `git -c safe.directory=<absolute-repository>
  status`. Success confirms missing Git ownership trust; it is not a repair.
- **Durable repair:** With explicit approval for persistent user-level Git
  trust, add only each intended absolute path with `git config --global --add
  safe.directory <absolute-repository>`. A coordinating repository may generate
  an exact set from its authoritative registry. Never substitute
  `safe.directory=*`, system-level trust or automatic derived-project inclusion.
- **Authorization needs:** Persistent Git configuration is a security
  relaxation and needs approval. It grants no filesystem access, input access,
  write, Git-action, external-write, transmission or publication authority.
- **Verification:** Run normal `git status` in every intended repository without
  `-c safe.directory`. Verify writes only at an independently authorized write
  checkpoint.
- **Last confirmed:** 2026-09-07, sanitized native-Windows family evidence;
  seven exact current-user entries allowed normal sandboxed status checks in
  Governance and all six source templates without a trust override.

## KI-0002: Skill validator lacks its YAML dependency

- **Stable signature:** The Skill Creator's `quick_validate.py` stops with
  `ModuleNotFoundError: No module named 'yaml'` before validating a skill.
- **Applicability:** Skill-editing tasks in this clone whose selected Python
  interpreter lacks PyYAML. Ignored environments do not transfer through Git.
- **Cause:** The validator imports `yaml`, but that interpreter has no PyYAML.
- **Safe diagnostic:** Print `sys.executable` and query
  `importlib.util.find_spec('yaml')` without installing anything.
- **Durable repair:** At first validation use, reuse the project's established
  managed environment or create its ignored `.venv`, then install the pin from
  `requirements-tools.txt` under separate authority. Run
  `scripts/Test-CodexSkill.ps1` with an exact `-PythonPath` for a managed
  environment; the wrapper never installs or selects arbitrary Python.
- **Authorization needs:** Ask before environment creation, download or package
  installation. Do not change global Python or `pip`.
- **Verification:** Import `yaml` with the selected interpreter and rerun the
  original validator operation through the wrapper.
- **Last confirmed:** 2026-09-09, portable Templateverse contract and structural
  validation only; this clone must prove runtime readiness on first use.

## KI-0004: Context-sensitive patch application rejects a coordinated edit

- **Stable signature:** `apply_patch` rejects an edit with
  `verification failed: Failed to find expected lines` before reporting any
  changed file. A retry using freshly read exact context and smaller independent
  hunks succeeds.
- **Applicability:** Context-based repository patches, especially coordinated
  multi-file edits and line-wrapped Markdown where a generated hunk reconstructs
  or approximates surrounding text instead of copying the current target span.
  The same signature may follow a concurrent edit, different indentation or
  line wrapping; it is not by itself evidence of whitespace or line-ending
  damage.
  Dynamically assembled patch text can produce the same rejection when inserted
  lines lose their line-level operation markers.
- **Cause:** `apply_patch` verifies each hunk against exact current context. In
  the confirmed Governance incident, the failed hunk expected a shortened
  phrase at a line boundary that did not match the actual sentence. Because the
  combined patch was rejected as one operation, none of its otherwise valid
  hunks changed a file. The mismatch was generated patch context, not verified
  repository whitespace corruption.
  During the family rollout, one dynamically assembled insertion likewise lost
  its add-operation markers and was rejected atomically before changing a file.
- **Safe diagnostic:** Do not retry the same patch. Read only the bounded target
  span named in the failure, compare its exact wording and indentation with the
  rejected hunk, and inspect the affected repositories read-only to confirm
  whether any partial edit occurred. Distinguish stale or approximated context
  from malformed line-level operation markers and actual line-ending or
  whitespace evidence before selecting a repair.
- **Durable repair:** Before the first complex patch, read the exact target
  spans and build hunks around the smallest stable semantic anchors. Separate
  independent files or uncertain hunks so one context mismatch does not reject
  a broad coordinated edit. When assembling patch text dynamically, preserve an
  explicit operation marker on every hunk line. For repeated family changes,
  prove the hunk on one representative file, then apply the same verified shape
  to matching copies.
  After any rejection, verify atomicity and correct only the mismatched hunk;
  do not broaden the context or attribute the failure to whitespace by default.
- **Authorization needs:** Read-only context and state inspection need no new
  authority inside the active repository scope. Resulting edits retain all
  input, material, external-write, publication and Git boundaries.
- **Verification:** On a natural coordinated multi-file edit, read the exact
  spans before constructing the first patch, apply the bounded hunks through
  the normal `apply_patch` path and inspect the resulting diff. Success
  requires first-attempt application with only the intended files changed; do
  not create a fix-specific fixture or substitute patch test.
- **Last confirmed:** 2026-09-06, coordinated Governance and six-source-template
  rollout. One normal multi-repository patch updated all seven freshly read
  `start-task` targets on its first attempt, and focused diffs showed only the
  intended skill changes. After the malformed generated insertion was diagnosed
  and rejected atomically, a later dynamically assembled seven-file handoff
  patch with explicit line markers also succeeded on its first attempt.

## KI-0005: Default sandbox blocks an authorized Git metadata write

- **Stable signature:** An authorized `git add -- <exact paths>` or `git commit`
  starts in the default `workspace-write` sandbox and fails because Git cannot
  create `.git/index.lock`. Read-only Git inspection succeeds, no partial
  index state is observed, and the same exact write succeeds when separately
  approved to run outside the sandbox.
- **Applicability:** Codex local command execution with a writable repository
  root under the default `workspace-write` policy. The protection also applies
  when `.git` is a pointer file and Git resolves metadata elsewhere.
- **Cause:** Codex deliberately protects every writable root's `.git` path
  recursively as read-only. Creating `index.lock` is the normal first step for
  an index write, so this denial is an expected sandbox boundary, not evidence
  of a stale lock, repository ACL defect or transient Git failure.
- **Safe diagnostic:** Do not repeat the write in the sandbox. Preserve the
  current selection, inspect status and staged paths read-only, distinguish
  failure to create `index.lock` from an already-existing lock, and confirm
  that no partial index change occurred. Investigate an existing lock or a
  failure outside the sandbox as a different incident.
- **Durable repair:** Once exact staging is requested or the corresponding
  commit is authorized, request each exact Git command that writes `.git`
  through the platform's narrow sandbox escalation on its first attempt. Keep
  read-only Git inspection sandboxed. Do not add `.git` to writable roots,
  change ACLs or ownership, delete a lock, enable full access, or install a
  persistent allow rule. Escalation changes only the execution boundary and
  grants no additional repository, input, external-write, publication,
  path-selection, push or standing authority.
- **Authorization needs:** Staging requires its normal concrete request or the
  authorization of the corresponding commit. Commits and other protected Git
  actions retain every repository-specific control-word requirement. The
  platform's narrowly scoped sandbox approval is separate from both.
- **Verification:** At the next natural authorized staging or commit, run the
  exact metadata-writing command outside the sandbox on its first attempt, then
  verify the intended staged paths, index state and absence of a residual lock
  through the normal workflow. Do not create a fix-specific repository or
  substitute index test.
- **Last confirmed:** 2026-09-07, natural seven-repository runtime acceptance.
  Exact authorized `git add` and `git commit` operations succeeded on their
  first attempt through narrow sandbox escalation in Governance and all six
  source templates, with exact selections and no residual `index.lock`.
