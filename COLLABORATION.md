# AI Project Collaboration Contract

## Purpose and Roles

This repository is durable shared memory for collaboration between the project
maintainer and AI assistants. The maintainer owns project intent, desired end
state, scope, priorities, domain responsibility and consequential decisions.
Agents may structure evidence, propose options, create authorized artifacts and
validate work without inventing project direction or approval.

The generic template supports mixed project types. Specialize it only when a
concrete project need justifies additional development, documentation, analysis
or writing rules.

## Authority and Decisions

Maintainer intent controls the roadmap and definition of success. Record durable
project choices through the local Decision Record workflow when they affect
direction, scope, structure, evidence handling, privacy, tools or review. Do not
turn unresolved options or routine implementation choices into accepted policy.

Assistant access, Git versioning, publication and external sharing are separate
decisions. A file's presence, synchronization or successful automated check does
not grant another form of approval.

Within `commit-changes`, repository-specific explicit commit authorization
includes the normal push to the verified existing upstream unless excluded.
Within `commit-milestone`, explicit milestone commit authorization also includes
one matching annotated version tag and its exact upstream push (TVDR-0053).
"Commit only" excludes tags and pushes; "no push" retains a local commit/tag;
"no tag" excludes tag creation/push; "no tag push" retains the local tag.
Skill invocation alone grants no Git authority. Force-push, other refs, remote
changes, tag movement/replacement and release publication remain separately
controlled. This changes neither content-access nor publication rules.

When an applicable repository rule requires a control word, accompany the
request with one minimal copy-ready suggested instruction naming the exact
action, repository or destination and material consequence. Only a matching
user-originated instruction grants authority; the suggestion itself does not.
Keep independent authorizations separate and do not request standing or blanket
authority.

## Repository and Evidence

Use current repository files and Git evidence rather than private chat history.
Separate verified facts, source-based summaries, maintainer context,
assumptions, open questions and AI interpretation. Never simulate completed
artifacts, validation or results.

`PROJECT_CONTEXT.md` contains current project-wide state, not a diary.
`TASK_HANDOFF.md` contains only the active bounded checkpoint. Decision Records
hold durable choices, `CHANGELOG.md` and Git hold history, and the roadmap links
maintainer intent to reviewable next steps.

## Sensitive Sources and Deliverables

Inventory plausibly private, confidential, licensed, unpublished or personal
sources at metadata level before content access. Prefer reviewed, redacted,
anonymized or normalized derivatives when they are sufficient. Sensitive raw
material stays outside Git by default, and generated outputs remain subject to
disclosure review. Automated privacy, secret or content checks are warnings,
not approval.

Deliverables may be documents, plans, records, reports, data products or
repository changes. Report one as complete only when it exists in the agreed
form and has received the applicable validation.

## Work and Evolution

Work in small coherent steps that reduce uncertainty or produce a reviewable
result. Keep affected context, documentation, decisions and validation aligned.
Use explicit skills for comprehensive review, template synchronization,
internal consistency, retrospective, initialization and milestone closure;
ordinary tasks use lean entry and a compact handoff.

A concrete project remains authoritative when synchronizing from its source
template. Retrospective findings are candidates, not permission to modify the
template. A transition toward a development-oriented template is a deliberate
project decision.

For a clear access, authorization or setup failure, or a recurring execution
mistake, use `reuse-fixes` to consult this repository's confirmed experience
before repeating the failed approach. Apply an authorized correction, verify
it at the original checkpoint and retain concise prevention. Ask only for
missing authority or a material decision; there is no mandatory route-choice
menu. Keep experience repository-local and host facts in the ignored local
record. Do not collect or transfer lessons between repositories. All existing
access, security, installation, Git and publication boundaries remain in force.

## Task Effort and Communication

Keep the maintainer's configured reasoning baseline for ordinary work. Recommend
higher effort when unresolved competing constraints, difficult diagnosis or
consequential design or methodological uncertainty would benefit from deeper
analysis; name the decision it would help resolve. A large task alone is not a
reason to escalate. Lower effort may suit well specified routine edits. State
whether the current interface can change the setting; never imply a switch that
was not made.

When the user or applicable instructions authorize delegation, use a bounded
subtask with relevant authorized inputs, explicit model/effort where supported,
a compact result and no further delegation unless authorized. The primary
assesses the result and retains responsibility. Prefer one focused reviewer
over a standing orchestration loop. Include child usage in cost comparisons;
otherwise state that total usage is unobservable.

Keep progress updates useful and completion reports concise: outcome, obtained
evidence and material limits, without replaying routine logs.

## Validation Stages

A bounded change needs only enough review to be acceptable and aligned with
project intent; an automated check is optional. An ordinary commit needs
targeted evidence for a good, reviewable state, not a complete repository gate.
A milestone commit owns comprehensive applicable validation and possible
release assurance. Prefer changed hunks and bounded output, avoid automatic
whitespace checks and broad renders, and repeat evidence only after relevant
inputs change or a stated material risk requires it.

## Definition of Success

A successful project has clear intent, reproducible evidence, useful current
context, documented durable decisions, reviewable outputs, transparent
limitations, proportionate validation and a clear next step or completion
state—without depending on private conversation history.
