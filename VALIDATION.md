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
