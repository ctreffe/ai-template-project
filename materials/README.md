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
materials, normally under ignored `local/research/`. Use the
[report scaffold](../templates/RESEARCH_REPORT.md) for concrete questions,
individual source assessments with evidence/reasons/dates, methods and limits.
Keep prior report/source references when later assessments change. New data
retain schema and record/field provenance; publication remains separate.
