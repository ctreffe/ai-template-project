# Decision Records

This directory is the default location for durable decision records in projects derived from the AI Project Template.

Use the record type that matches the decision:

- `PDR` - Project Decision Record for scope, direction, collaboration, privacy, repository structure, roadmap or governance decisions.
- `ADR` - Architecture Decision Record for technical architecture, tooling, data flow, configuration, lifecycle or implementation-structure decisions.
- `DDR` - Documentation Decision Record for documentation structure, audience, terminology, screenshot, link, publication or documentation QA decisions.

The generic template defaults to PDRs, but derived projects may mix record types when the project work crosses domains.

## Naming

Use a stable prefix, number and short kebab-case title:

```text
PDR-0001-project-scope.md
ADR-0001-tooling-model.md
DDR-0001-documentation-structure.md
```

## Template

Use [PDR-0000-template.md](PDR-0000-template.md) as the default starting point for generic project decisions. Derived projects may add more specialized templates when needed.
