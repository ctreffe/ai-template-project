# REPOSITORY.md

# Repository Standards

This document describes repository-level standards for projects created from the AI Project Template.

---

# Repository as Project Memory

The repository should contain enough context to continue the project without relying on private chat history.

Important project state, decisions, references and outputs should be captured in repository documents when practical.

---

# Suggested Structure

```text
README.md
AGENTS.md
COLLABORATION.md
PROJECT_CONTEXT.md
PROJECT_SETUP.md
TASK_HANDOFF.md
.agents/skills/
DOCUMENTATION.md
REPOSITORY.md
PHILOSOPHY.md
CHANGELOG.md
VERSION
LICENSE
.gitignore
DECISIONS.md
input/
  intake/
  restricted/
  local/
  versioned/
  CATALOG.md
output/
```

Projects may adapt this structure. When a folder gains project-specific meaning, add a short README that explains its role, expected contents and privacy or file-handling rules.

---

# README Badge Policy

Template repositories use a compact badge block directly below the README
title and before the AI Collaboration Note. The standard semantic order is
status, version and license, followed only by badges for real build, test or
documentation automation.

Status links to `VERSION`, version links to `CHANGELOG.md` and license links to
`LICENSE`. Public repositories may use dynamic GitHub metadata; private or
proprietary repositories may use static badges updated with milestone metadata.
Avoid a last-commit badge because activity does not establish quality or
readiness.

Derived projects adapt the block to their actual status, versioning model,
license and automation. They must not present the source-template version as
their project version or advertise a workflow that does not exist. English and
German badge blocks remain identical when both languages are maintained.

---

# External Files and Sources

`input/` stores external files and source references under four explicit
handling classes:

- `intake/` for unclassified incoming files;
- `restricted/` for ignored files unavailable to assistants;
- `local/` for ignored files approved for assistant access;
- `versioned/` for files deliberately approved for Git and assistant access.

Use `input/CATALOG.md` for safe, versioned metadata and the ignored
`input/CATALOG.local.md` for sensitive filenames, paths or source details.
Assistants do not enumerate or read `intake/` or `restricted/` by default.
Moving a file does not itself authorize content access, Git actions or external
sharing.

`output/` stores deliverables and generated results.

`DECISIONS.md` explains Decision Records.

Use `decisions/` when the project has real decision records to store.

Do not store private, confidential or unlicensed material in versioned folders unless that is an intentional project decision.

---

# Temporary Working Files

`temp/` is fully ignored and never versioned. All contents outside
`temp/restricted/` are assistant-readable disposable intermediates; assistants must not enumerate or
read `temp/restricted/`. Promote retained files to `materials/` and catalog
them rather than keeping durable work in `temp/`.

# Project Materials

Content under `input/` remains unchanged. Retain created or transformed working
files in `materials/`, register them in `materials/CATALOG.md` and record their
provenance through `Based on`. Every registered material is assistant-readable;
choose `local`, `versioned` or `external` storage independently of access.
Machine-specific external-path mappings belong only in ignored
`materials/PATHS.local.md`. Caches, disposable files and final outputs are not
project materials.

# Raw Inputs, Reviewed Derivatives and Generated Outputs

Projects should distinguish raw inputs, reviewed derivatives and generated outputs when that distinction matters.

Raw inputs are maintainer-provided or external materials in their original form. They may be private, confidential, licensed, unpublished or personal. Assistants should not inspect such raw materials by default. First document a source inventory and decide whether inspection is appropriate.

Reviewed derivatives are project-specific representations that have been checked for the intended use, such as anonymized tables, extracted observations, redacted excerpts, normalized CSV files, summaries or review workbooks. They are often safer and more useful to version than raw inputs.

Generated outputs are produced from sources, derivatives or scripts. The repository should make clear whether generated outputs are versioned review files or regenerated locally. Review their visible content, embedded resources and file metadata for disclosure risk before versioning or sharing them.

Assistant access, Git versioning and publication or other sharing are separate
approval decisions. A reviewed derivative may be suitable for one of these
purposes without being suitable for the others.

`.gitignore` rules and source documentation should be updated together when private local inputs are required.

Sensitive raw inputs should remain outside Git by default. Establish ignore
rules and a source inventory before copying them into a repository working
tree. Before a commit is prepared, review new and untracked files for secrets,
personal data, confidential material, licensing restrictions and accidental
raw-source inclusion. Prefer reviewed derivatives whenever they satisfy the
project need.

Automated privacy, secret or content checks may identify risks, but a clean
result does not authorize access, versioning or publication.

---

# Git Workflow

GitHub Desktop is a suitable Git client for the repository maintainer.

The repository maintainer controls Git history.

AI assistants may inspect Git status, diffs and logs when useful. They may
prepare changes, propose commit boundaries and suggest commit summaries and
descriptions.

Staging and unstaging are index operations rather than history actions. They do
not require a control word, but the assistant may perform them only when the
maintainer specifically requests the index action or authorizes the
corresponding commit. Preserve existing staged selections and unrelated
changes.

AI assistants must not create commits, amend commits, rebase, reset, revert,
create or delete branches, create or delete tags, push, pull, merge, manipulate
stashes or perform another protected Git action unless the maintainer instructs the
assistant to perform that specific action and uses a recognized control word:
`explicit` or `explicitly` in English, or the German word family `explizit`,
including `explizite`, `expliziten`, `expliziter` and `explizites`.

Within `commit-changes` or `commit-milestone`, repository-specific explicit
commit authorization includes the commit and its normal push to the verified
existing upstream unless the maintainer excludes push. Skill invocation alone
grants no Git authority. Force-push, other refs, remote changes, tags and release
publication remain outside this bundle; other protected actions still need
separate authority. This changes neither content-access nor publication rules.

Approval for file edits is not approval for protected Git actions. Approval for
other independent protected actions still require their own authority,
with the bounded commit-and-push workflow below as the specific exception. Requests such as "commit this",
"create the commit", "tag this" or "push this" do not authorize the assistant to
run protected Git commands unless they contain a recognized control word.

Commits should be small enough to review and should represent one logical
project step. A roadmap milestone should normally be built through multiple
regular working commits when its work can be separated meaningfully.

Regular working commits must use exact direct prefixes such as:

```text
feat:
fix:
docs:
refactor:
test:
chore:
```

Do not insert an optional scope between the type and colon; `feat(scope):` is
not part of this repository-family convention. Use real line breaks in the
meaningful description and never literal `\n` escape text.

Milestone commits are the exception. A milestone commit should not use a
Conventional Commit prefix. It should use a human-readable summary that
includes the completed version number, for example:

```text
Finalize project discovery milestone (v0.3.0)
```

A milestone commit should primarily close and harmonize work already recorded
in regular commits. It must not hide a large set of unrelated or unreviewed
changes. A genuinely small milestone may need only one preceding working
commit, but the commit boundary should follow the logical work rather than the
version boundary.

Every commit should include:

- a concise summary
- a meaningful description

Commit summaries should describe the primary purpose of the change. Commit
descriptions should describe the actual diff and, when useful, its reason or
validation. They should not repeat unrelated history or claim future work as
completed.

---

# Review and Harmonization Commits

Harmonization commits are appropriate when a project-wide rule, roadmap, decision or documentation model changes.

A harmonization commit should update affected documents together so the repository reads as one coherent state.

---

# Versioning

Templates should use Semantic Versioning.

Derived projects may use the versioning scheme that fits the work:

- Semantic Versioning
- date-based versions
- milestone names
- document revisions
- named project states

Whatever scheme is chosen should be documented and used consistently.

---

# Transition to AI Dev Template

If a project becomes development-oriented, consider adopting or migrating toward the AI Dev Template.

This is useful when the project becomes centered on:

- code
- scripts
- automation
- tests
- releases
- technical architecture
- implementation lifecycle

The transition should be documented with a PDR.
