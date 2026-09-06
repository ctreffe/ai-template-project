# Environment Troubleshooting

This conditionally loaded registry belongs only to focused problem resolution.
It stores portable observed problems, confirmed causes, safe diagnostics and
verified durable repairs in this template or a concrete derived project. It may
retain an unresolved incident as an open task with the smallest next diagnostic
step. Do not read or update it after a quick exit. Host-specific facts belong in
ignored `TROUBLESHOOTING.local.md`; secrets and sensitive input details do not
belong in either file.

Reuse an entry only when both its stable signature and applicability match and
its diagnostic reconfirms the cause. Otherwise diagnose anew. A recorded repair
grants no access, installation, privilege, security change, Git operation,
outside write, transmission or publication authority.

## Entry Schema

Every entry records:

- **Stable signature:** Output and execution stage that distinguish the issue.
- **Applicability:** Platforms, runners, repositories or prerequisites in scope.
- **Cause:** The verified root cause, not a symptom or guess.
- **Safe diagnostic:** Bounded read-only evidence that confirms or rejects it.
- **Durable repair:** The preferred recovery and its security boundary.
- **Authorization needs:** Every approval or control-word requirement.
- **Verification:** The normal operation that must succeed before resumption.
- **Last confirmed:** ISO date and sanitized evidence scope.
- **Unresolved marker:** Only when no repair was verified; retain the problem as
  an open task and state the smallest next diagnostic step.

## Portable Known Issues

None are confirmed in the source template. Derived projects add only sanitized,
reverified patterns that remain useful beyond one host; host-specific facts stay
in their ignored local record.
