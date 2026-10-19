# External Files and Sources

For approved external originals in the simple synchronized input root,
follow [SYNCHRONIZED_STORAGE.md](../SYNCHRONIZED_STORAGE.md). Mapping a root
does not authorize its contents or unrelated synchronized folders.

Use `input/` for files supplied by the maintainer or obtained from external
sources. This includes documents, datasets, screenshots, exports, forms and
other files that enter the project from outside its maintained project files.

Keep their content unchanged. Any conversion, redaction, annotation or other
content change creates a new file governed through `materials/`.

New or uncertain files start in `intake/`. Files whose handling is already
clear may be placed directly in the appropriate folder:

- `intake/` contains files that have not yet been classified;
- `restricted/` contains local files whose contents an assistant must not
  inspect;
- `local/` contains local files approved for assistant access but not for Git;
- `versioned/` contains files deliberately approved for Git versioning and
  assistant access.

Record safe source and handling information in `CATALOG.md`. Include unchanged
external services, datasets and URLs even when their content remains outside
the repository. If filenames,
paths or other details are themselves sensitive, keep them in the ignored
`CATALOG.local.md` instead. Resolve logical external locations per device in
ignored `PATHS.local.md`, copied from `PATHS.local.example.md`.

Assistant access, Git versioning and publication or external sharing are
separate maintainer decisions. Moving a file does not authorize reading,
staging, committing, pushing or sharing it. Files that become maintained
project content may move to a more specific project folder after their origin
and handling have been recorded.
