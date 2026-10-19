# Template synchronization state

Use this record only for a deliberately selected synchronization of a derived
project. Initialize provenance from PROJECT_CONTEXT.md on first use; ordinary
task entry and project initialization need no additional questionnaire or scan.
Source-template maintenance checkouts keep this as an unfilled scaffold.

## Comparison and adoption

- Verified source identity: `<source template>`
- Initial project baseline: `<reference to PROJECT_CONTEXT.md>`
- Last compared upstream commit/date: `<none | full commit and date>`
- Latest selected adoption checkpoint: `<none | upstream commit, selected change IDs and actual validation>`
- Fully resolved through: `<none | upstream commit whose changes are all adopted, adapted or deliberately rejected>`

Compared is not adopted. Advance the compared commit only after recording the
reviewed differences; advance the selected adoption checkpoint only for applied
and validated changes. Do not claim a fully resolved baseline while earlier
deferred or conflicting items remain. Deliberate rejection needs its reason and
reconsideration condition; it is not the same as postponement.

## Change outcomes

| Change ID | Source commit/range and affected concept or paths | Outcome | Local adaptation, evidence or reason | Next review condition |
| --- | --- | --- | --- | --- |
| `<SYNC-001>` | `<origin and selected scope>` | `<adopted/adapted/deferred/conflicting/rejected>` | `<actual application/validation or unresolved reason>` | `<trigger or none>` |

At the next sync, review new changes since the last compared commit AND every
deferred/conflicting item from its original baseline. Recheck deliberately
rejected items when their condition applies. Preserve local adaptations and
completed initialization cleanup. Keep resolved rows as compact evidence;
PROJECT_CONTEXT.md links here instead of maintaining another change ledger.

Example: A to B contains X and Y. Adopt X, defer Y and record comparison B.
At B to C review new changes plus Y from A to B; do not reapply X. If C changes
X again, compare that new change against its actual local adaptation. A partial
sync never restores removed initialization skills or replaces project READMEs
with source READMEs. Record genuine conflicts before dependent edits.
