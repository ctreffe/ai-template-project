# Changelog

All notable changes to this project will be documented in this file.

This project follows Semantic Versioning.

## [Unreleased]

- Make local runtime setup demand-driven, reproducible per clone and explicit
  about interpreter selection; preserve existing environment managers.

- Rebuild `troubleshoot-environment` around an undocumented quick exit or
  focused cause removal, direct explicit invocation, and acceptance at the
  original checkpoint or a pre-agreed standalone test. Remove the unspecific
  `optimize-codex` skill while preserving demand-driven setup.

## [0.5.0] - 2026-09-02

### Added

- Add the pinned MIT-licensed `grill-me` and `grilling` skills to the
  template and new derived projects, with explicit-only invocation and an
  opt-in detailed path before the normal six-question initialization.

- Add the bounded TVDR-0026 source-template pilot with an implicitly
  discoverable environment-troubleshooting skill plus portable and ignored
  host-local known-issue records.
- Add a source-template `IDEAS.md` backlog for sanitized reusable
  retrospective candidates.
- Add a provider-neutral, conditionally loaded `COLLABORATION.md` contract.
- Add repository-scoped collaboration skills and a tracked compact
  `TASK_HANDOFF.md` for task lifecycle, project review, synchronization,
  consistency checks, retrospectives, decisions and commit preparation.
- Add provider-neutral synchronized external project storage for large non-Git
  input and materials that must remain available across devices.

### Changed

- Adopt TVDR-0030 so control-word requests include minimal copy-ready wording
  while keeping access, Git, sharing and publication actions separate.

- Adopt TVDR-0028's acceptable-change, good-commit and comprehensive-milestone
  validation stages with bounded evidence and no default whitespace or full
  suite before milestone closure.

- Make project initialization progressive: ask no more than six coherent
  fundamental questions, reuse established answers and defer nonessential
  setup details until a concrete task needs them.
- Route recurring, setup, policy and permission failures from the resident
  trigger to signature-matched, authorized and verified recovery.
- Interrupt recurring tool or environment failures for durable authorized
  diagnosis and verified recovery before resuming work.
- Require successful project initialization to replace inherited template
  maintenance history in `CHANGELOG.md` and `TASK_HANDOFF.md` with project-owned
  state, and reinduce exact direct-prefix commit messages with meaningful bodies.
- Assign targeted checks to implementation and the complete applicable
  repository gate to commit preparation, while reporting deferred gates
  truthfully in handoffs.
- Route retrospective findings explicitly to project, source-template or
  governance destinations with a Pending Idea Transfer fallback, and remove
  the template backlog during successful normal-project initialization.
- Make `AGENTS.md` the sole resident safety kernel, retire provider-specific
  collaboration files and require explicit `$commit-milestone` invocation.
- Replace the root initialization, continuation, harmonization, retrospective
  and local-project creation prompts with `$start-project` and scoped skills;
  retain `PROJECT_SETUP.md` as initialization method and provenance.
- Remove the project copy of `CREATE_LOCAL_PROJECT_PROMPT.md` and its
  template-only references after successful initialization.
- Clarify that a generated file's project role, rather than its generation
  method, distinguishes retained materials from final outputs.

## [0.4.0] - 2026-07-26

### Added

- Replace the input inventory files with an external-file and source catalog,
  portable local path mapping and support for unchanged external sources.
- Add a shared, never-versioned `temp/` area with a restricted access boundary.
- Add a cataloged project-material workflow with local, versioned and external
  storage states for retained assistant-readable working files.
- Add `CREATE_LOCAL_PROJECT_PROMPT.md` for independent local-only projects.
- Add a common catalog-based workflow for external files and sources with
  `intake`, `restricted`, `local` and `versioned` input zones.
- Add `AGENTS.md` as the concise, automatically loaded entry point that routes
  AI agents to the complete repository rules and validation guidance.

### Changed

- Upgrade the AGIT Generic Collaboration Model to v0.4.0.
- Align the project-context template with input catalogs, temporary files and
  retained project-material storage states.
- Require external input content to remain unchanged and preserve provenance
  when project work creates or transforms files.
- Clarify user-facing terminology for files, sources, records and outputs and
  remove the unused `notes/` and `references/` defaults.
- Align the initialization and continuation prompts with `AGENTS.md`: setup is
  an explicit one-time workflow, while continuation only reconstructs state.
- Expand continuous-improvement guidance with the candidate-to-governance
  lifecycle and transparent, unlinked private Templateverse coordination.

## [0.3.0] - 2026-07-20

### Changed

- Clarify `INITIAL_PROMPT.md` as the sole maintainer entry point for agent-led
  initialization, separate language navigation from the collaboration note,
  move README authority guidance into documentation rules and link maintainer
  tools to their official sources.
- Standardize template README badges as status, version and license links and
  document how derived projects adapt badges without inheriting template state
  or advertising nonexistent automation.
- Upgrade the AGIT Generic Collaboration Model to v0.3.0 and classify staging
  and unstaging as specifically requested index operations outside the
  control-word rule while preserving staged and unrelated changes.

## [0.2.0] - 2026-07-19

### Added

- Add `RETROSPECTIVE_PROMPT.md` for evidence-based Maintainer-Agent
  collaboration review and controlled template-learning candidates.
- Add `HARMONIZATION_PROMPT.md` for source-template comparison, internal
  consistency review and roadmap alignment.
- Add `CONTINUATION_PROMPT.md` for reproducible project re-entry in a new
  context window or assistant session.
- Add `INITIAL_PROMPT.md` as a reproducible first-session prompt for derived project initialization.
- Add an AGIT Templateverse section to the English and German READMEs.
- Add `decisions/` as the shared Decision Record location with default PDR guidance and support for ADR, DDR and WDR prefixes when needed.

### Changed

- Retain initialization artifacts as project provenance, record template
  lineage and harmonization baselines in `PROJECT_CONTEXT.md`, and clarify that
  documentation and repository guidance remain active project rules.
- Separate assistant access, Git versioning and publication approval for
  sensitive sources, derivatives and generated outputs.
- Define automated sensitivity checks as warnings rather than safety approval.
- Add a standard checkpoint handoff for reviewable working steps.
- Limit the generic Decision Record vocabulary to PDR, ADR and DDR and remove
  domain-specific record guidance from the generic template.
- Formalize small working commits below roadmap milestones and reserve separate
  milestone commits for reviewed milestone closure.
- Require commit recommendations to contain consistent summaries and meaningful
  descriptions.
- Strengthen safeguards against adding sensitive raw sources to Git.
- Define completion criteria for structured project initialization.
- Prefer concise numbered maintainer decisions and next steps.
- Upgrade the AGIT Generic Collaboration Model to v0.2.0.
- Carry the working-commit rhythm and numbered collaboration convention into
  the derived-project context template.
- Require recognized Git history control words before an assistant may perform Git history actions.
- Clarify the AI Collaboration Note with an explicit AI-assisted collaboration sentence.
- Add setup guidance requiring derived projects to preserve and adapt a visible AI Collaboration Note linked to `ChatGPT.md`.
- Introduce the AGIT Generic Collaboration Model as v0.1.0.
- Add source-sensitivity, reviewed-derivative and generated-output guidance based on access-plan project retrospection.
- Add folder README, review artifact and post-milestone context-refresh guidance.
- Expand PDR candidate guidance for privacy, derivative versioning, output versioning and related-repository scope decisions.
- Clarify that template-only setup files may be removed or retained after initialization depending on project needs.
- Clarify that retained initialization files should keep their original names and may document setup status internally or in `PROJECT_CONTEXT.md`.
- Clarify that regular working commits must use Conventional Commit prefixes while milestone commits should omit prefixes and include the completed version number.

## [0.1.1] - 2026-07-02

### Added

- Add German README documentation.
- Add the AI Collaboration Note to the README files.
- Add explicit maintainer control over Git history actions to the collaboration
  and repository guidance.
- Add `CODEX.md` as the local Codex operating policy for generic AGIT projects.

## [0.1.0] - 2026-07-02

### Added

- Initialize the generic AGIT Project Template.
- Add collaboration, project context, setup, documentation, repository and philosophy guidance.
- Add `DECISIONS.md` as the generic Project Decision Record guidance.
- Add working folders for inputs, references, notes and outputs.
- Add changelog, version metadata and ignore rules.
