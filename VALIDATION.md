# Validation

## Codex skill validation: first use

Only prepare this Python tool environment when a task edits a Codex skill and
needs the bundled Skill Creator validator. Python is not a generic project
prerequisite. Reuse an established project manager and its isolated environment
when available; otherwise, after approval for environment creation and package
download, prepare this clone's ignored `.venv`:

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements-tools.txt
```

Run the fixed wrapper rather than `quick_validate.py` through arbitrary Python:

```powershell
.\scripts\Test-CodexSkill.ps1 -SkillPath .\.agents\skills\start-task
```

For an existing managed environment, supply its exact interpreter path with
`-PythonPath`. Use `-ValidatorPath` only when the installed Skill Creator moved.
The wrapper checks `import yaml` and runs validation; it does not install
packages, alter global Python or grant access, Git or publication authority.
PyYAML is pinned in `requirements-tools.txt`; upgrades are deliberate changes.

## Optional external-storage helper development

When this helper changes, use its invented-only behavior check as needed:

```powershell
./scripts/Test-ExternalStorageHelper.ps1
# Windows PowerShell 5.1, with a process-only option when needed:
powershell.exe -NoProfile -ExecutionPolicy Bypass -File ./scripts/Test-ExternalStorageHelper.ps1
```

It creates only a unique temporary fixture with checked cleanup, including
Windows offline and junction cases. If the platform blocks junction creation,
request narrow execution escalation for this exact synthetic check; do not
change host policy or silently omit the case. This development check is not
part of ordinary tasks, initialization or handoff and accesses no cloud files.
