# Project Materials

Synchronized external materials use provider-neutral `sync:` roots and storage
`external`; see [SYNCHRONIZED_STORAGE.md](../SYNCHRONIZED_STORAGE.md).

`materials/` contains retained working files created within the project or
derived by changing content from one or more external files under `input/`.
Every material is approved for assistant access. Git versioning and external
sharing remain separate decisions.

Files under `input/` remain content-unchanged. Decompression, conversion, OCR,
redaction, cropping, annotation, normalization, combination or any other
content change creates a new material; preserve the original input and record
its ID under `Based on` in `CATALOG.md`.

The catalog records three storage states:

- `local`: the file is stored under `materials/local/`, is ignored by Git and
  remains assistant-readable;
- `versioned`: the file is stored under `materials/versioned/` and is approved
  for Git versioning;
- `external`: the file is stored outside the repository and represented by a
  stable logical location in `CATALOG.md`.

Copy `PATHS.local.example.md` to the ignored `PATHS.local.md` when logical
external locations need device-specific paths. Do not put credentials, private
share tokens or machine-specific absolute paths in the versioned catalog.

Materials are durable working foundations, not caches, disposable temporary
files or final deliverables. Move files into a more specific maintained
project location when that location communicates their lasting role better;
keep their provenance in the catalog.

## Question research

Retain question research reports and optional datasets as separately cataloged
materials, under the storage rule below. Use the
[report scaffold](../templates/RESEARCH_REPORT.md) for concrete questions,
individual source assessments with evidence/reasons/dates, methods and limits.
Keep prior report/source references when later assessments change. New data
retain schema and record/field provenance; publication remains separate.

## Research storage and reuse

New research reports and generated data sources stay outside Git by default.
Prefer `sync:<project-id>/materials/research/` only when that project's mapping,
identity and approved write/provider scope already cover these materials and
the destination is locally available. Use the selected project's existing
catalog and ignored mapping; do not discover cloud folders or set up storage
implicitly. This use of an approved mapping does not invoke a setup skill.

Otherwise save under ignored `materials/local/research/` and catalog the actual
local location and any availability limitation. A missing, mismatched,
placeholder or unsupported external destination is not permission to hydrate,
move or transmit. If an externally stored artifact is required for the task,
report the gap rather than silently claiming successful external delivery.
Do not move earlier artifacts automatically. Separate file-specific approval
is needed to version research content; a cloud location is not Git or publication
approval. Keep reports and generated datasets separately cataloged with stable
IDs, provenance and references to prior assessments.

Before later reuse, resolve the required artifact's ID and location, verify the
relevant availability and access, and reuse still-current evidence from this
task. Record a missing report as an evidence gap; never invent its contents or
assessment. Check only needed artifacts, not every catalog or project. Use
[SYNCHRONIZED_STORAGE.md](../SYNCHRONIZED_STORAGE.md) when setup or a mapping
problem actually needs attention.
