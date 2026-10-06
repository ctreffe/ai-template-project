# AI Project Template

[![Status](https://img.shields.io/badge/status-stable-green)](VERSION)
[![Version](https://img.shields.io/github/v/tag/ctreffe/ai-template-project?label=version)](CHANGELOG.md)
[![License](https://img.shields.io/github/license/ctreffe/ai-template-project)](LICENSE)

> [!NOTE]
> **AI Collaboration**
>
> This repository maintains the generic AI Project Template.
>
> The template documents AI-assisted collaboration practices, context handoff, decision records and repository conventions for structured project work.
>
> The collaboration contract is maintained in [COLLABORATION.md](COLLABORATION.md).

<br>

**[Link zur deutschen README](README.de.md)**

<br>

## Contents

- [Overview](#overview)
- [Core Principle](#core-principle)
- [AI Templateverse](#ai-templateverse)
- [When to Use This Template](#when-to-use-this-template)
- [Project Initialization](#project-initialization)
- [Collaboration Skills](#collaboration-skills)
- [External Files and Sources](#external-files-and-sources)
- [Temporary Working Files](#temporary-working-files)
- [Project Materials](#project-materials)
- [Recommended Workflow](#recommended-workflow)
- [Git Index and Protected Git Actions](#git-index-and-protected-git-actions)
- [Decision Records](#decision-records)
- [Repository Structure](#repository-structure)
- [Template and Derived Project Files](#template-and-derived-project-files)
- [How to Use This Template](#how-to-use-this-template)
- [Maintainer Tool Setup](#maintainer-tool-setup)
- [Continuous Improvement](#continuous-improvement)
- [License](#license)

## Overview

The AI Project Template is a generic starting point for projects that benefit from structured collaboration, explicit context, documented decisions and reliable handoff between work sessions. It is intentionally not limited to software development: it supports research, planning, concept work, process design, operational projects and mixed project types.

The template provides a repository-first collaboration model, local Codex rules, scoped collaboration skills, retained setup guidance, a current-state project context, documentation and repository standards, decision-record guidance and optional working folders. It is a project method and repository foundation, not a domain-specific framework.

## Core Principle

The maintainer owns the project intent and direction. The assistant may help structure information, identify gaps, prepare project files and results, check consistency and preserve project memory, but it must not invent the desired end state, silently resolve consequential decisions or report work as complete when it does not exist.

The repository is the durable project memory. A future maintainer, contributor or assistant should be able to understand the current state and continue the work without relying on private chat history.

## AI Templateverse

The public AI templates form a small templateverse: a family of related templates that share a repository-first, maintainer-led Human-AI collaboration model while specializing it for different project types.

- [AI Project Template](https://github.com/ctreffe/ai-template-project) is the generic starting point for structured project work, research, planning, concept work, process design and mixed projects.
- [AI Dev Template](https://github.com/ctreffe/ai-template-dev) is for development-oriented projects where code, scripts, automation, validation, architecture or release workflows are central.
- [AI Documentation Template](https://github.com/ctreffe/ai-template-docs) is for technical documentation projects such as user guides, admin guides, operating procedures, tutorials, migration guides and documentation sites.

## When to Use This Template

Use the Project Template when the project shape is still open or when several kinds of work need one coherent project memory. It is well suited to discovery, planning, research, coordination, process design and projects that may later become more specialized.

Start from a specialized template when the primary work is already clear:

- choose the Dev Template for implementation, tests, automation and releases;
- choose the Documentation Template for audience-oriented technical documentation and publication;
If a generic project later becomes development-oriented, document the transition and adopt or migrate toward the Dev Template deliberately.

## Project Initialization

After creating the repository, the maintainer invokes `$start-project`. The
skill reads the repository, follows `PROJECT_SETUP.md` and leads the complete
initialization. The maintainer does not need to open or execute the setup files
separately.

The simplest instruction to the agent is:

> `$start-project`

There is no initialization prompt to open or copy into the conversation.
Before the normal questionnaire, the agent offers one concise choice between
the normal lean path and the explicit `$grill-me` path for detailed planning.
Choosing the detailed path does not grant access or action authority.

The agent then:

1. reads the collaboration, setup, documentation, repository and decision rules;
2. inspects the repository baseline without altering Git history;
3. follows the selected initialization path and, on the lean path, asks no more
   than six unanswered fundamentals covering identity and purpose, audience and
   use, the first useful outcome and its evidence, current scope and non-goals,
   source or material access and sensitivity, and only constraints that must be
   fixed before work begins;
4. asks for each consequential decision instead of inventing project direction
   and allows nonessential choices to remain explicitly deferred;
5. adapts the README files, project context, working folders and ongoing project rules after the maintainer answers;
6. records the template baseline and initialization provenance in [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md);
7. applies safe defaults and keeps required placeholders and unresolved setup decisions visible; and
8. hands back the initialized repository state with proportionate validation results, limitations and suggested commit metadata.

`PROJECT_SETUP.md` remains the agent's detailed initialization checklist and
method provenance. `$start-project` is the single executable entry point that
activates that checklist.

For a project that should remain local and have no remote, invoke
`$create-local-project` explicitly in this checked-out template. The skill
verifies the destination, creates an independent local clone without a remote,
then invokes `$start-project`; it is not a second initialization.
After successful initialization, the inherited template history in
`CHANGELOG.md` and `TASK_HANDOFF.md` is replaced with project-owned state. The
template-only `IDEAS.md`, the project's copy of `$create-local-project` and
their references are removed unless the maintainer deliberately establishes a
project-local idea backlog. The initialization files remain as provenance.

## Collaboration Skills

Skills are scoped workflows in [`.agents/skills/`](.agents/skills/). They guide
the agent through a particular task and load the relevant repository guidance.
Invoke a skill in chat with `$skill-name`, for example
`$review-project`. The linked skill files describe each full workflow.

- **Agent or explicit:** The agent may select the skill when the task fits;
  you can also invoke it directly.
- **Explicit:** The skill needs a deliberate invocation or explicit maintainer
  selection. An agent suggestion does not activate it.

Selecting a skill grants no additional permission for protected Git actions,
installation, external transmission or publication. Local access and domain
rules apply to every workflow.

In `commit-changes` and `commit-milestone`, explicit commit authorization for
this repository includes its normal push to the verified existing upstream.
Specify "commit only" or "no push" to exclude it. Other Git actions, tags and
release publication still need their own authorization.

`reuse-fixes` reads and updates only this repository's error knowledge. It does
not collect lessons across repositories or maintain global memory.
Active fixes use 4–8 lines per case in `TROUBLESHOOTING.md`.
[Detailed evidence](TROUBLESHOOTING_DETAILS.md) is preserved separately;
read only a matching detail section when needed.

| Skill | Invocation | Purpose |
| --- | --- | --- |
| [`start-task`](.agents/skills/start-task/SKILL.md) | Agent or explicit | Reconstruct only the context needed for a new bounded task. |
| [`handoff-task`](.agents/skills/handoff-task/SKILL.md) | Agent or explicit | Save the task outcome, evidence and next step in a compact `TASK_HANDOFF.md`. |
| [`commit-changes`](.agents/skills/commit-changes/SKILL.md) | Agent or explicit | Create an ordinary scoped commit and perform its normal upstream push with explicit commit authorization, unless push is excluded. |
| [`record-decision`](.agents/skills/record-decision/SKILL.md) | Agent or explicit | Document a durable decision using the applicable record type; source-template decisions route to Governance. |
| [`reuse-fixes`](.agents/skills/reuse-fixes/SKILL.md) | Agent or explicit | Reuse this repository's confirmed fixes, retain concise prevention and ask only for missing authority or blocking decisions. |
| [`start-project`](.agents/skills/start-project/SKILL.md) | Explicit | Initialize a new, uninitialized derived project from the retained setup guidance. |
| [`review-project`](.agents/skills/review-project/SKILL.md) | Explicit | Produce a comprehensive neutral inventory of project state and evidence gaps. |
| [`sync-template`](.agents/skills/sync-template/SKILL.md) | Explicit | Compare a derived project with its verified source template and adopt selected updates while preserving project adaptations. |
| [`check-consistency`](.agents/skills/check-consistency/SKILL.md) | Explicit | Diagnose internal contradictions between intent, roadmap, decisions, content and documentation; develop bounded options. |
| [`perform-retrospective`](.agents/skills/perform-retrospective/SKILL.md) | Explicit | Review collaboration evidence and distinguish project findings from reusable template or family candidates. |
| [`create-local-project`](.agents/skills/create-local-project/SKILL.md) | Explicit | Create a local derived repository from this source template and hand it over to initialization; removed after successful project setup. |
| [`commit-milestone`](.agents/skills/commit-milestone/SKILL.md) | Explicit | Close a reviewed milestone with metadata, comprehensive applicable checks, a commit and normal upstream push unless excluded. |

### Optional Planning Skills

`grill-me` and `grilling` are adopted MIT-licensed skills by Matt Pocock.
They complement the repository's own skills and are used only after explicit
selection. The normal lean initialization path remains available.

| Skill | Invocation | Purpose |
| --- | --- | --- |
| [`grill-me`](.agents/skills/grill-me/SKILL.md) | Explicit | Start the optional intensive planning interview and route it to `grilling`. |
| [`grilling`](.agents/skills/grilling/SKILL.md) | Explicit | Explore a plan, decision or idea through detailed interview rounds; use only after explicit opt-in. |

## External Files and Sources

Use `input/` for files supplied by the maintainer or obtained from external
sources. New or uncertain files begin in `input/intake/`; files with an already
known classification may go directly to `restricted/`, `local/` or
`versioned/`.

- **`input/intake/`** contains files whose access, Git and sharing rules have
  not yet been decided. Assistants must not enumerate or read them by default.
- **`input/restricted/`** contains ignored local files that remain under
  maintainer-controlled access.
- **`input/local/`** contains ignored local files approved for assistant access
  within a documented scope but not for Git versioning.
- **`input/versioned/`** contains external files deliberately approved for Git
  and assistant access.

Record safe metadata, provenance and handling decisions in
`input/CATALOG.md`. Use the ignored `input/CATALOG.local.md` when filenames,
paths or source details are themselves sensitive. External sources that remain
outside the repository belong in the catalog without copying their contents.
Use stable public URLs directly and resolve logical private or device-specific
locations through ignored `input/PATHS.local.md`.

Assistant access, Git versioning and publication or external sharing remain
separate maintainer decisions. Moving a file does not authorize reading,
staging, committing, pushing or sharing it. A classified file may later move to
a more specific project folder when it becomes maintained project content.

For large non-Git files that must remain available across devices, use the
provider-neutral workflow in [SYNCHRONIZED_STORAGE.md](SYNCHRONIZED_STORAGE.md).
Synchronized files remain external storage; synchronization is not Git
versioning, backup, assistant access or publication approval.

## Temporary Working Files

Use `temp/` for disposable intermediate files. All contents outside
`temp/restricted/` are assistant-readable; that restricted directory must not
be enumerated or read.
All temporary content is ignored and must never be versioned. It is not
cataloged. Promote anything worth retaining to `materials/` and catalog it.

## Project Materials

Keep files in `input/` unchanged: they are original external files and fixed
source references. Any content change—including conversion, OCR, redaction,
cropping, annotation, normalization or combination—creates a new file under
the project-material workflow rather than modifying the input.

`materials/` holds durable working files created in the project or derived
from input. Every registered material is approved for assistant access, while
Git versioning and external sharing remain separate decisions. Record each file
in `materials/CATALOG.md`, including purpose, creation or transformation,
storage state and provenance through `Based on` input or material IDs.

- **`local`** files live in ignored `materials/local/`.
- **`versioned`** files live in `materials/versioned/` and may be committed.
- **`external`** files remain outside the repository at a stable logical
  location in the catalog. Resolve that location per machine in ignored
  `materials/PATHS.local.md`, copied from the versioned example.

Do not use `materials/` for caches, disposable temporary files or final
deliverables; outputs remain in `output/`. Never record credentials, private
share tokens or device-specific absolute paths in versioned files.

Generation method does not determine location. Keep a generated file in
`materials/` when it is a durable working or source file consumed by later
project steps. Place it in `output/` when it is a project result intended for
use, review, handoff, publication or delivery. Disposable generation
intermediates remain in `temp/`; domain-specific authoritative files keep their
maintained locations.

## Recommended Workflow

Projects proceed from maintainer intent through small, reviewable project loops:

```text
Intent -> Roadmap -> Produce -> Review -> Check -> Record -> Continue
```

1. Establish or confirm the repository baseline.
2. Review the maintainer intent, desired end state and current roadmap.
3. Select the smallest useful step that reduces uncertainty or produces a reviewable result.
4. Create or revise the project file, result or other relevant project content.
5. Review or validate the result and make limitations visible.
6. Update affected context, documentation and decision records.
7. Prepare a regular working commit with an appropriate Conventional Commit prefix.
8. Continue until the milestone objective is satisfied.
9. Close the milestone separately by reconciling current state, versioning and history.

Routine new tasks use the lean `start-task` skill. Invoke `$review-project` for
a comprehensive neutral inventory, `$sync-template` for source-template
updates, `$check-consistency` for internal diagnosis and
`$perform-retrospective` for a collaboration review.

## Git Index and Protected Git Actions

The maintainer controls Git history. Assistants may inspect status, diffs and logs and may prepare working-tree changes and commit metadata.

Staging and unstaging are index operations. They do not require a control word, but they may be performed only after a specific maintainer request or authorization of the corresponding commit. Existing staged selections and unrelated changes must be preserved.

Protected actions include commits, amendments, tags, pushes, pulls, merges, rebases, resets, branch changes, stash manipulation and other Git history operations. An assistant may perform a specific protected action only when the instruction for that action contains `explicit` or `explicitly` in English, or the German word family `explizit`. File-edit approval does not authorize Git history changes, and other protected actions remain separately authorized, with the commit-and-push workflow above as the specific exception.

When this rule requires authorization, the assistant proposes one minimum-scope,
copy-ready instruction naming the exact action, repository and material
consequence. The proposal itself is not authorization.

Regular working commits use Conventional Commit prefixes such as `feat:`, `fix:`, `docs:` or `chore:`. Milestone commits omit the prefix, use a human-readable summary containing the completed version and close already reviewed work.

## Decision Records

Decision Records preserve why consequential choices were made. Choose the prefix by decision subject, not merely by repository type:

- **PDR — Project Decision Record:** project direction, scope, roadmap, collaboration, governance, privacy boundaries, review models or repository relationships.
- **ADR — Architecture Decision Record:** technical architecture, tooling, formats, automation or another durable technical structure in a derived project.
- **DDR — Documentation Decision Record:** documentation structure, terminology, audience-facing material, publication rules or documentation QA.

The generic template defaults to PDRs and explains the model in [DECISIONS.md](DECISIONS.md). Use [decisions/](decisions/) only for decisions whose rationale will matter to future collaborators; small routine choices do not need a record.

## Repository Structure

### Entry Points and Project Memory

- **`README.md` and `README.de.md`** introduce the project, explain how to start and link to the deeper rules in English and German.
- **`PROJECT_CONTEXT.md`** is the primary re-entry point. It records current intent, status, roadmap, baseline, validation state, open decisions and the next useful step rather than duplicating the full project history.
- **`CHANGELOG.md` and `VERSION`** describe completed states and version history. They are updated when a versioned milestone is completed, not merely when work begins.

### Collaboration and Operating Rules

- **`AGENTS.md`** is the concise, automatically resident safety kernel and context router for AI agents.
- **`COLLABORATION.md`** defines the provider-neutral Maintainer-Agent collaboration contract, authority boundaries, evidence model and success criteria. It is loaded only when its broader context is relevant.
- **`TROUBLESHOOTING.md`** retains confirmed corrections and concise prevention
  for `reuse-fixes` in this repository. Host facts remain ignored in
  `TROUBLESHOOTING.local.md`. Other repositories are not included.
- **`PHILOSOPHY.md`** records the values behind the project method, including intent before structure, traceability, lightweight process and integrity over appearance.

### Setup, Continuation and Review

- **`PROJECT_SETUP.md`** guides the first initialization and preserves its methodological provenance. `$start-project` is the explicit executable entry point.
- **`.agents/skills/`** contains the workflows and invocation rules described in
  [Collaboration Skills](#collaboration-skills).
- **`TASK_HANDOFF.md`** is the compact versioned checkpoint for a completed,
  paused or blocked task and supports continuation on another computer.
- **`IDEAS.md`** is a source-template backlog for reusable candidates. Normal
  derived projects remove it during successful initialization unless they
  deliberately establish a project-local backlog.

### Repository Guidance and Decisions

- **`DOCUMENTATION.md`** defines documentation roles, current-state versus history boundaries and quality expectations. It remains an ongoing project rule after initialization.
- **`REPOSITORY.md`** defines repository organization, Git conventions, source and output handling, versioning and repository-ready delivery. Derived projects adapt it to their actual workflow rather than treating it as disposable setup material.
- **`DECISIONS.md` and `decisions/`** explain Decision Records and store durable decision rationale. The template provides reusable PDR guidance and subject-specific record templates.

### External Files and Project Outputs

- **`input/`** applies the shared intake, restricted, local and versioned
  classifications to external files and sources. Its inventories preserve safe
  provenance and handling decisions.
- **`materials/`** catalogs retained assistant-readable working files and
  separates local, versioned and external storage from access permission.
- **`temp/`** holds ignored, never-versioned intermediates, with
  `temp/restricted/` as the inaccessible exception.
- **`output/`** holds project deliverables or generated results. Projects define
  whether outputs are versioned milestones, review files or reproducible local
  products and review them before sharing.

## Template and Derived Project Files

The template contains reusable rules and placeholders. In a derived project:

- fill and maintain `PROJECT_CONTEXT.md` as the current project state;
- adapt both README files, `DOCUMENTATION.md` and `REPOSITORY.md` to the concrete project;
- keep and adapt `AGENTS.md`, `COLLABORATION.md` and `PHILOSOPHY.md` unless a documented project need requires a change;
- retain `PROJECT_SETUP.md` as initialization provenance;
- retain the applicable repository skills for repeatable later workflows;
- adapt the input and output folders to the concrete workflow while preserving
  their documented handling rules;
- replace template Decision Records with real records only when consequential decisions exist.

Record the source-template version and commit, initialization status, last harmonization baseline and intentional deviations in `PROJECT_CONTEXT.md`. A derived project is authoritative for its own intent and accepted decisions; template updates are reviewed and adapted rather than copied blindly.

## How to Use This Template

1. Create a repository from the template and invoke `$start-project`.
2. Choose the normal lean path or explicitly opt into `$grill-me`; on the lean
   path, answer no more than six unanswered fundamental questions while the
   agent applies the remaining setup files automatically.
3. Review the initialized repository state, validation results and proposed first commit.
4. Let the agent keep `PROJECT_CONTEXT.md` current as the concise project handoff during later work.
5. Work in small files, results or changes derived from maintainer-owned intent, boundaries and success criteria.
6. Distinguish raw inputs, reviewed derivatives and generated outputs before granting access, versioning or publication.
7. Record consequential decisions in `decisions/` and validate results before presenting them as complete.
8. Begin a bounded new task through `start-task`; invoke `$review-project` only
   when a comprehensive inventory is actually needed.
9. Keep `$sync-template`, `$check-consistency` and `$perform-retrospective` as
   separate explicit workflows with distinct outcomes.
10. Close milestones with coherent context, documentation, changelog and version metadata.

## Maintainer Tool Setup

The generic template has no mandatory domain toolchain. A practical local baseline is:

- [Git](https://git-scm.com/downloads) and a maintainer-controlled client such as [GitHub Desktop](https://desktop.github.com/download/);
- a text or Markdown editor such as [Visual Studio Code](https://code.visualstudio.com/download);
- [PowerShell](https://learn.microsoft.com/powershell/scripting/install/installing-powershell-on-windows) on Windows or an equivalent local shell;
- [ripgrep (`rg`)](https://github.com/BurntSushi/ripgrep/releases) or another fast search tool;
- project-specific tools installed only when the concrete work requires them.

Prefer project-local environments such as `.venv/` or `node_modules/` over global changes. Package installation, external services and network use should have a clear project purpose, and private repository material should remain local by default.

## Continuous Improvement

Use `$sync-template` to compare a concrete project with a verified source-template baseline and adopt selected developments. Use `$check-consistency` separately for internal contradictions, and `$perform-retrospective` for collaboration practices, handoffs, decision-making and work rhythm. Mixed projects may reveal both generic improvements and evidence that a more specialized template would be the better long-term home.

Treat observations from a derived project as candidates rather than automatic template rules. Evaluate whether they recur, remain useful outside their original context and belong in the generic template or a domain specialization. Derived projects and their Decision Records remain authoritative for project-specific choices.

The maintainer coordinates cross-template evolution in a private governance repository named `ai-templateverse`. It records shared conventions, deliberate specializations and evidence from derived projects. The repository is intentionally not linked because template users do not need access to it.

Governance coordination does not create hidden requirements. Every change that affects this template must be represented here through maintained guidance, Decision Records where appropriate, the changelog and release history. Template changes should update affected documents coherently rather than append isolated notes.

## License

This project is licensed under the [MIT License](LICENSE).
