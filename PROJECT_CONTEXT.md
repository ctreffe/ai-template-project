# PROJECT_CONTEXT.md

# Project Context Template

This document captures the current state of a project created from the AI Project Template.

It is the primary handoff document for resuming work after a pause, continuing on another computer or starting a new AI-assisted session.

Replace the placeholders during project setup.

---

# Template Lineage and Initialization

Repository role:

```text
<derived project>
```

Source template:

```text
AI Project Template
```

Initial template baseline:

```text
<template version and commit hash>
```

Initialization status:

```text
<not started | in progress | completed>
```

Initialization date:

```text
<YYYY-MM-DD | not yet completed>
```

Last template harmonization:

```text
<not yet performed | template version, commit hash and date>
```

Last collaboration retrospective:

```text
<not yet performed | reviewed period or milestone, date and relevant record>
```

Intentional template deviations and relevant Decision Records:

```text
<none | concise list>
```

Keep `PROJECT_SETUP.md` as initialization provenance. It describes the
project's methodological roots; this section records its
lifecycle status and the baselines used over time.

During initialization, replace only the placeholders needed to record the six
fundamental answers, the first useful outcome and its current safety boundary.
Keep nonessential later detail explicitly undecided until a concrete task needs
it; do not invent precision merely to fill this template.

---

# Project

Project name:

```text
<project name>
```

Repository:

```text
<repository URL or local path>
```

Short description:

```text
<one or two sentences describing the project>
```

Project type:

```text
<general | research | documentation | process | planning | mixed | development-oriented>
```

Potential transition:

```text
<whether this project may later adopt the AI Dev Template>
```

---

# Maintainer Project Intent

Maintainer-owned initial context:

```text
<problem space, operating context, audience or environment>
```

Desired end state:

```text
<what the project should enable, produce or make easier when successful>
```

Boundaries and non-goals:

```text
<what the project should avoid, postpone or deliberately not cover>
```

Success criteria:

```text
<how the maintainer will know the project has succeeded>
```

---

# Current Status

Current project version or state:

```text
<version, date, milestone or named state>
```

Current phase or milestone:

```text
<current milestone name>
```

Current focus:

```text
<what the project is currently working on>
```

Status:

```text
<planned | in progress | review | waiting for input | validated | completed | paused | archived>
```

---

# Working Baseline

Current baseline:

```text
<local working tree | supplied files | public repository | accepted output>
```

Baseline notes:

```text
<notes about which repository state, files or materials are authoritative>
```

---

# Roadmap

- `<next step>` - `<purpose or expected result>`
- `<later step>` - `<purpose or expected result>`

Roadmap entries should be small enough to review and validate.

---

# External Inputs and Project Materials

Important unchanged external files and sources:

- `<input file or source>`

Input catalog and location mapping:

```text
<input/CATALOG.md entries and any required input/PATHS.local.md mappings>
```

Synchronized external storage:

```text
<not used | project ID, sync: roots, mapped input/material scope, availability, conflict and backup notes>
```

Source handling notes:

```text
<privacy, licensing, verification or data-disclosure notes>
```

Source sensitivity and handling:

```text
<which raw inputs are private, confidential, licensed, unpublished or personal; what should be represented through reviewed derivatives>
```

Assistant-access approval for classified input:

```text
<exact sources or reviewed derivatives, permitted task and limitations>
```

Git-versioning approval:

```text
<exact reviewed files approved for Git, or none>
```

Publication or sharing approval:

```text
<exact files or outputs and audience, or none>
```

Retained project materials:

- `<material>` - `<source relationship, purpose and materials/local | versioned | external storage state>`

Materials catalog and external location mapping:

```text
<materials/CATALOG.md entries and any required materials/PATHS.local.md mappings>
```

Temporary-file state:

```text
<relevant temp/ work in progress; do not record sensitive details from temp/restricted/>
```

---

# Outputs

Current or expected deliverables:

- `<deliverable>`

Output location:

```text
<output/ path, document path or external location>
```

Generated output status:

```text
<which outputs are generated, which source files produce them and whether they are versioned or regenerated locally>
```

---

# Open Questions

- `<open question>`

If there are no open questions, state that explicitly.

---

# Important Decisions

Important decisions already made:

- `<decision>`

Relevant decision records:

- `<decision record file, if any>`

---

# Relevant Documents

- `README.md` - project overview
- `PROJECT_SETUP.md` - retained initialization method and provenance
- `CHANGELOG.md` - version or project-state history
- `COLLABORATION.md` - provider-neutral collaboration contract, loaded when relevant
- `TASK_HANDOFF.md` - compact versioned checkpoint for task continuation
- `.agents/skills/` - task lifecycle and explicit specialized workflows
- `TROUBLESHOOTING.md` - conditionally loaded portable environment recovery patterns
- `SYNCHRONIZED_STORAGE.md` - provider-neutral external storage and per-device mapping workflow
- `$sync-template` - source-template comparison and selected adoption
- `$check-consistency` - internal consistency diagnosis and solution options
- `$perform-retrospective` - structured Maintainer-Agent collaboration review
- `DECISIONS.md` - Decision Record guidance
- `decisions/` - Decision Record templates or project decisions, if used
- `PHILOSOPHY.md` - project philosophy
- `DOCUMENTATION.md` - documentation standards
- `REPOSITORY.md` - repository standards
- `input/` - classified external files and sources
- `temp/` - never-versioned intermediate files
- `materials/` - retained assistant-readable project files and catalog
- `output/` - deliverables

Remove or adapt entries that do not apply.

- `PROJECT_SETUP.md` remains as initialization provenance unless the maintainer documents a deliberate exception.
- Active roadmap milestones should progress through small regular commits when
  meaningful project steps can be reviewed separately.
- Maintainer decisions and clarification questions should be presented as
  concise numbered lists when practical.
- After milestone commits or tags, update this document to reflect the completed state rather than leaving pre-commit review instructions as the current focus.
- Staging and unstaging require a specific maintainer request or authorization
  of the corresponding commit, but no control word. Protected Git actions
  require a specific instruction containing `explicit`, `explicitly` or the
  German word family `explizit`.

---

# Notes for the Next Session

Use this section to make restarting work easy.

```text
<what to do next, what not to change yet, what needs review, what is blocked>
```
