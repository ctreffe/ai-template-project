# DECISIONS.md

# Decision Records

Decision Records document important decisions that future collaborators should understand without relying on chat history.

The AI Project Template defaults to Project Decision Records (PDRs), but derived projects may also use Architecture Decision Records (ADRs) or Documentation Decision Records (DDRs) when the decision subject calls for a more specific record type.

Choose the prefix by decision subject, not by repository type.

---

# When to Use a Decision Record

Use a decision record when a decision affects:

- project direction
- scope or non-goals
- collaboration structure
- documentation structure
- source or evidence handling
- sensitivity classification of raw inputs before assistant inspection
- privacy or data disclosure boundaries
- whether raw inputs, reviewed derivatives or generated outputs are versioned
- scope boundaries between related repositories
- tool or repository choices
- review or approval process
- transition toward a development-oriented project

Do not create a PDR for every small choice. Use one when future collaborators would benefit from understanding why a decision was made.

---

# Recommended Location

When a project needs durable decision records, use the `decisions/` folder.

Example:

```text
decisions/
  PDR-0001-project-direction.md
  PDR-0002-source-handling.md
  ADR-0001-tooling-model.md
  DDR-0001-documentation-structure.md
```

The generic template explains the concept, but derived projects should create their own decision records only when real decisions exist.

---

# Suggested Format

```text
# PDR-0001: Decision Title

## Status

Proposed | Accepted | Superseded

## Context

What situation, problem or uncertainty made the decision necessary?

## Decision

What was decided?

## Rationale

Why was this option chosen?

## Consequences

What follows from the decision?
```

---

# Relationship to Other Documents

- `PROJECT_CONTEXT.md` should summarize important decisions that affect current work.
- Decision records should preserve durable decision reasoning.
- `CHANGELOG.md` records completed changes, not decision rationale.
- `README.md` should link to relevant decisions only when users or contributors need them.
