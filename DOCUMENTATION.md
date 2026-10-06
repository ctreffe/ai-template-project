# DOCUMENTATION.md

# Documentation Standards

Documentation is part of the project.

It should make the project understandable without relying on private chat history.

---

# Document Roles

## README.md

The public entry point. It explains what the project is, who it is for and where to find more information.

## README Language Policy

In source-template checkouts, `README.md` is the English source text and
`README.de.md` is its close structural and semantic German translation. In
initialized projects this applies independently to the project pair and the
retained guide pair. Both pairs are required; the project introduction and
the guide have different roles and are not translations of one another.

## Project and guide README roles

After initialization, `README.md` and `README.de.md` introduce the actual project
and link early to its workflows and skills. `TEMPLATE_README.md` and
`TEMPLATE_README.de.md` retain adapted inherited operating guidance. Both pairs
are required, have reciprocal language links within the pair and link between
project introduction and guide in the same language. Follow `PROJECT_SETUP.md`
for safe renaming, interrupted setup and final inventory review. Local resident
and domain rules and accepted decisions remain authoritative. Keep guide links,
identity and license wording accurate and omit inherited guide badges. Badge
policy applies to source-template or project introductions, not guides.
Selected upstream README updates map to the guides through `sync-template`,
without replacing the project introductions. Source checkouts retain their
original pair; existing projects are not automatically migrated.

## README Badge Block

Place badges directly below the title and before the AI Collaboration Note.
Use status, version and license in that order, followed only by badges backed
by real build, test or documentation automation. Each badge should communicate
maintained project information and link to its durable source where practical:
`VERSION`, `CHANGELOG.md`, `LICENSE` or the corresponding workflow.

Do not use badges as decoration or retain source-template badges unchanged in
a derived project. A last-commit badge is discouraged because activity is not
a quality or readiness measure. Keep English and German badge blocks identical,
and update static badges together with the project metadata they represent.

## PROJECT_CONTEXT.md

The current-state handoff document. It describes where the project stands now.

## Repository Skills

`.agents/skills/` contains lean automatic task entry, handoff and commit
preparation plus explicit initialization, neutral review, source-template
synchronization, internal consistency and retrospective workflows.

`TASK_HANDOFF.md` is the compact versioned handoff between bounded tasks and
devices. It does not duplicate project history or full session output.

## CHANGELOG.md

The history of completed project states or template versions.

## COLLABORATION.md

The provider-neutral collaboration contract. It is conditional context for
initialization, comprehensive review, authority conflicts and collaboration-
model changes.

## AGENTS.md

The concise, automatically resident safety kernel and context router. It keeps
protected-action, access, working-tree and minimum validation rules available
without loading the full collaboration contract for every task.

## PHILOSOPHY.md

The project values and reasoning style.

## REPOSITORY.md

Repository organization and version-control guidance.

## DECISIONS.md

Decision Record guidance.

It explains when to create decision records, where to store them and which structure to use.

## input/

External files and sources classified as intake, restricted, local or
versioned. `input/CATALOG.md` contains only source metadata suitable for Git;
sensitive local catalog details belong in ignored
`input/CATALOG.local.md`.

## output/

Deliverables and final outputs.

---

# Current State vs. History

Keep current state and history separate.

- Current state belongs in `PROJECT_CONTEXT.md`.
- History belongs in `CHANGELOG.md`.
- Durable decisions belong in decision records when the project creates them.
- Deliverables belong in `output/`.

---

# Source and Evidence Notes

When a project uses external sources, document enough context to understand how they were used.

Where relevant, distinguish:

- direct source material
- summaries
- assumptions
- maintainer-provided context
- AI interpretation
- information that still needs verification

---

# Source Sensitivity and Reviewed Derivatives

Before an assistant inspects private, unpublished, confidential, licensed or personal raw material, document the source inventory and sensitivity first. Start with file names, file types, maintainer descriptions and intended handling rather than reading raw contents by default.

When raw material is sensitive, prefer reviewed derivatives that expose only the information needed for the project. Examples include anonymized tables, extracted observations, source summaries, redacted excerpts, derived CSV files or generated review files.

Source documentation should make clear:

- which raw materials exist locally
- which materials are ignored or not versioned
- which reviewed derivatives may be versioned
- what still requires maintainer approval before assistant inspection or external sharing

---

# Folder README Files

When a working folder gains project-specific meaning, add or update a short README in that folder. The README should explain the folder role, expected contents, privacy or licensing constraints, and whether files are sources, reviewed derivatives, working notes or generated outputs.

---

# Review Files and Records

For complex milestones, create a concise review or harmonization record when it helps future continuation. It may capture technical checks, content checks, source assumptions, validation results, unresolved risks and maintainer review points.

Review files belong in the location that fits the project, such as `docs/`,
`reports/` or a project-specific review folder.

---

# Harmonization

Invoke `$sync-template` for a deliberate source-template comparison and
`$check-consistency` for internal consistency and roadmap diagnosis. When a
change affects multiple documents, update them together.

Avoid adding isolated notes when existing sections should be revised.

Harmonization is especially important after:

- roadmap changes
- important decisions
- scope changes
- completion of a milestone
- retrospectives
- transition toward a development-oriented project

---

# Language and Tone

Use precise, plain language.

Avoid promotional wording.

Prefer clarity over persuasion.

State limitations, uncertainty and open questions directly.
