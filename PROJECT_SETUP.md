# PROJECT_SETUP.md

# Project Setup Guide

This document describes how to initialize a new project from the AI Project Template.

It is primarily used during project creation and should normally remain in a
derived repository as a record of its initialization method. Record lifecycle
status and template lineage in `PROJECT_CONTEXT.md` instead of rewriting this
guide after setup.

## Lean initialization contract

Before the normal questionnaire, `$start-project` asks one concise,
unnumbered routing choice: use the normal lean path or explicitly select
`$grill-me` for detailed initialization and planning. The routing choice is
not one of the six project questions. The skill is never invoked from a
suggestion; a suggestion is not consent. The maintainer may decline or stop
grilling and return to the lean path, and neither path changes any access,
versioning, transmission, publication or protected-action authority.

`$start-project` begins with no more than six fundamental maintainer
questions. Each numbered item is one coherent decision, not a container for a
hidden questionnaire:

1. What is the project's identity and purpose?
2. Who is it for, and how should they use its result?
3. What is the first useful outcome, and what minimum evidence will show that
   it is useful?
4. What is currently in scope, and what are the explicit non-goals?
5. Which source, material or data classes may the assistant access now, and
   which sensitivity boundary applies?
6. Which operating constraint must be fixed before work begins?

Use existing repository evidence for answers already established. The last
question includes only a constraint that is actually consequential now; do not
turn storage, versioning, publication, tooling and collaboration preferences
into a bundled survey. Keep safe template defaults for nonessential choices or
mark them explicitly undecided. Clarify document structure, detailed roadmap,
links, feedback, rendering, validation depth and publication only when the
first concrete task needs them. Later safety or protected-action questions may
still be required by evidence; this limit does not weaken those gates.

---

# 1. Establish Project Intent

Before filling the repository with structure, clarify the maintainer-owned project intent.

At minimum, define:

- problem space or operating context
- intended audience or users
- desired end state
- boundaries and non-goals
- success criteria
- whether the project may become development-oriented later

Record this in `PROJECT_CONTEXT.md`.

---

# 2. Establish the Baseline

Identify the starting point for the project:

- local repository working tree
- uploaded materials
- existing documents
- external references
- accepted output files or results

The baseline should be explicit enough that a future session can continue from the repository. When using AI assistance, invoke `$start-project` for the one-time initialization.

Before asking an assistant to inspect input files, classify potential sensitivity. For private, unpublished, confidential, licensed or personal material, start with a source inventory rather than raw content inspection. Decide whether the project needs anonymized or reviewed derivatives before raw inputs are read. Record assistant-access approval, Git-versioning approval and publication or sharing approval separately; none implies another. Treat automated checker results as warnings rather than proof that a file is safe.

Document external files and sources in `input/CATALOG.md`. Store sensitive
local catalog details only in ignored `input/CATALOG.local.md`, and reflect
durable handling rules in `PROJECT_CONTEXT.md` or a Decision Record when useful.

---

# 3. Review Core Documents

Review and adapt:

- `README.md`
- `PROJECT_CONTEXT.md`
- `AGENTS.md`
- `COLLABORATION.md`
- `DECISIONS.md`
- `PHILOSOPHY.md`
- `DOCUMENTATION.md`
- `REPOSITORY.md`
- `CHANGELOG.md`
- `VERSION`
- `LICENSE`

## Required AI Collaboration Note

Every derived project README should include an AI Collaboration Note near the top of the file, directly below the title and badges or language link area.

The note is a visible disclosure and orientation element. It should preserve the purpose, position and level of visibility of the template note while adapting the wording to the derived project.

The derived note should state:

- that the project is developed or maintained through collaboration between the repository maintainer and an AI assistant
- what the collaboration model documents in that project, such as practices, workflows, handoff rules, decision records or repository conventions
- that the collaboration contract is maintained in `COLLABORATION.md`

If `README.de.md` is kept, it should contain a structurally aligned German note.

## README Badge Policy

Place the badge block directly below the README title and before the AI
Collaboration Note. Use this semantic order when the corresponding information
applies:

1. status
2. version
3. license
4. real build, test or documentation automation

Derived projects must adapt the template badges to their own documented state.
Do not retain the source-template version as the project version. A status
badge needs a defined project meaning, the license badge must match the actual
license and a release badge is appropriate only when the project maintains
tags or releases. Add automation badges only for workflows that actually exist
and avoid a last-commit badge by default because activity is not a quality or
readiness signal.

Keep English and German badge blocks identical when both READMEs are present.
Record source-template version and lineage in `PROJECT_CONTEXT.md`, not in the
derived project's badge block.

Keep only what is useful for the project.

---

# 4. Review Working Folders

The template provides:

- `input/`
- `input/intake/`
- `input/restricted/`
- `input/local/`
- `input/versioned/`
- `input/CATALOG.md`
- `input/PATHS.local.example.md`
- `temp/`
- `temp/restricted/`
- `materials/`
- `materials/local/`
- `materials/versioned/`
- `materials/CATALOG.md`
- `materials/PATHS.local.example.md`
- `output/`

Keep the standard `input/` zones and their content unchanged. Establish the
standard `materials/` workflow for retained created or transformed files:
registered materials are assistant-readable, while local, versioned or external
storage and sharing remain separate decisions. Add further project-specific
structures only when they serve a clear purpose.

Use ignored `temp/` only for disposable, never-versioned intermediates. All
contents outside `temp/restricted/` are assistant-readable; that directory is
unavailable to assistants. Promote anything worth retaining to `materials/`
and catalog it.

Do not store private, confidential or unlicensed material in versioned folders unless the project intentionally tracks it.

Use `decisions/` when the project has real decision records to store. PDRs are the default for generic project decisions, while ADRs or DDRs may be added when the decision subject is technical or documentation-specific.

For data- or file-oriented projects, decide whether the project should distinguish raw inputs, reviewed derivatives and generated outputs. A project may remain based on the generic template while adopting selected development practices for scripts, validation and reproducible rebuild commands.

When a folder such as `input/` or `output/` gets a project-specific role, add or update a short README in that folder without weakening the input classifications.

---

# 5. Create the Initial Roadmap

Derive the roadmap from project intent and desired end state.

The initial roadmap should identify:

- the first useful milestone
- the next few planned steps
- what each step should produce
- what decisions or uncertainties each step addresses
- what remains intentionally out of scope

Record the roadmap in `PROJECT_CONTEXT.md` or a dedicated roadmap document.

---

# 6. Decide Whether Decision Records Are Needed

Use Decision Records for important decisions.

Good first PDR candidates include:

- project direction
- template structure
- documentation model
- source handling
- privacy boundaries
- transition toward the AI Dev Template

The Decision Record concept is documented in `DECISIONS.md`.

---

# 7. Review Repository Metadata

Update repository metadata:

- repository name
- repository description
- topics
- visibility
- license

Use precise language.

---

# 8. Initialize Versioning

Set the initial project version or state.

For template repositories, Semantic Versioning is recommended.

For derived non-software projects, another consistent scheme may be appropriate, such as:

- milestone names
- date-based versions
- document revisions
- named project states

The chosen scheme should be documented.

---

# 9. Record Initialization Provenance

Keep the two initialization files under their original names:

- `PROJECT_SETUP.md`

In `PROJECT_CONTEXT.md`, record their lifecycle status, initialization date,
source template version and commit, later harmonization baseline and intentional
template deviations. Remove an initialization file only as a deliberate,
documented maintainer exception.

After successful initialization, replace the inherited source-template
maintenance history in `CHANGELOG.md` with a project-owned changelog beginning
at `Unreleased`. Replace `TASK_HANDOFF.md` with a project-owned initialization
handoff containing only current project state, decisions, checks and the next
step. Preserve template lineage in `PROJECT_CONTEXT.md`, not in either active
project-history file. If initialization is incomplete, leave both resets
pending and identify the inherited content as non-authoritative.

Adapt `DOCUMENTATION.md` and `REPOSITORY.md` as ongoing project rules and keep
them current throughout the project lifecycle.

---

# 10. Prepare the First Commit

The first project-specific commit should describe the initialization.

Regular working commits use an exact direct prefix such as `feat:`, `fix:`,
`docs:`, `refactor:`, `test:` or `chore:` and a meaningful body. Scoped forms
such as `feat(scope):` are not used. Milestone commits are the exception: they
are human-readable, omit the prefix and include the completed version number.

Example summary:

```text
chore: initialize project from AI template
```

Example description:

```text
Initialize the project from the AI Project Template.

Adapt the project context, README, repository metadata and working folders for
the new project. Establish the initial project intent and roadmap.
```

Initialization is complete when the six fundamentals are answered or already
evidenced, the first useful next step and current access boundary are recorded,
safe defaults are explicit and the retained template state is internally
consistent. Nonessential setup fields may remain explicitly undecided. An
unresolved safety or authority choice blocks only the work it governs; do not
begin that work while the required decision remains a placeholder.

The initialization commit is normally a regular `chore:` commit. Use an
unprefixed milestone commit only when initialization also completes a genuinely
defined and reviewed versioned milestone.

---

# 11. Continue the Project

Begin each bounded new task through the automatically discoverable `start-task`
skill and use `TASK_HANDOFF.md` for a versioned checkpoint. Load
`COLLABORATION.md` only when initialization, comprehensive review, authority or
the collaboration model is in scope.

Keep `PROJECT_CONTEXT.md` current when:

- a milestone completes, including after a commit or tag has been created
- the roadmap changes
- important decisions are made
- new external files or sources become important
- the project is paused
- a new session needs to resume work

The repository skills should remain available after initialization. Invoke
`$review-project`, `$sync-template`, `$check-consistency` and
`$perform-retrospective` explicitly only when their specialized outcome is
needed. Remove the project copy of `$create-local-project` after successful
initialization because it belongs only in the source template.

# 12. Configure Synchronized External Storage When Needed

If large non-Git files must be available on several devices, apply
`SYNCHRONIZED_STORAGE.md`. Decide provider transmission, stable project ID,
input and material scope, optional external outputs, availability checks,
conflict handling and backup separately. Create ignored `sync:` mappings on
each device and record the durable decision in `PROJECT_CONTEXT.md` or a PDR.
Do not synchronize `temp/`.

## Required local runtime setup

During initialization, check only what the first concrete outcome needs.
Reuse established answers; defer later tooling and do not add a mandatory
questionnaire. General optimization has no dedicated skill; concrete recurring
environment problems route through `reuse-fixes`.

Check the runtime needed for the selected outcome and the actual interpreter
used by its commands. A new clone/device does not inherit ignored environments;
missing local setup is not evidence of damage. Reuse the project's established
manager and isolation model. When Python is required and no suitable managed
environment exists, prepare a clone-local ignored .venv; do not create one for
a project without Python needs or copy one from another clone.

Track dependencies and lockfiles using existing project conventions (for
example requirements-tools.txt for Python helpers). Document reproducible setup
and explicit interpreter or manager commands. Prepare only needed local setup,
reuse existing approval and obtain any missing installation/download authority
before applying it. Verify the interpreter and a minimal relevant import or
original command; defer optional tools without blocking unrelated work.

Keep the generic project free of Python setup when its tasks do not need it.
