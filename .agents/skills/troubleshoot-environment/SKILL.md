---
name: troubleshoot-environment
description: Resolve a concrete recurring or clear setup, policy, permission or toolchain problem, either after the resident trigger pauses ordinary work or when the maintainer explicitly invokes the skill for a known environment problem. Do not use for general optimization or expected code, content or test failures without infrastructure evidence.
---

# Troubleshoot Environment

Remove the cause of one concrete environment problem without broadening the
suspended task or the generic project boundary.

## Activation and route choice

On implicit activation, suspend the original task and state only a concise
description of the observed problem, failed operation and environment boundary.
Do not diagnose or load incident records before the maintainer chooses:

1. **Quick exit:** End this skill and return control to the ordinary task agent,
   which may seek a safe task-local workaround under normal boundaries. Perform
   no skill analysis, create no incident record and make no recovery claim.
2. **Problem resolution:** Continue with the focused workflow below.

Explicit maintainer invocation for a concrete known or recurring environment
problem enters problem resolution directly. Clarify the problem as needed and
do not offer the quick exit. General optimization is outside this skill.

## Focused problem resolution

1. Define the exact problem. Retain the original failing checkpoint, or agree
   with the maintainer on a concrete acceptance test before changing anything
   when invocation is standalone.
2. Load `TROUBLESHOOTING.local.md` when present and then
   `TROUBLESHOOTING.md`. Reuse a repair only after its stable signature,
   applicability and safe diagnostic reconfirm the same cause.
3. Investigate only this problem and recurrence risk. Diagnostic commands and
   diagnostic tests are allowed. Ask maintainer questions and proactively
   request concrete elevated authority whenever it enables an effective durable
   repair. State its exact scope and material security consequence; the
   maintainer owns the security judgment and critical questions. Do not suppress
   the option or choose a weaker solution merely to avoid elevated permission.
4. Implement the smallest authorized repair that removes the cause and prevents
   recurrence within the controlled boundary. Troubleshooting grants no access
   to `input/`, registered materials or `temp/restricted/`, and no Git, outside
   write, transmission or publication authority. When a repository control word
   is required, propose one minimal copy-ready instruction naming the exact
   recovery action, repository and material consequence; the proposal is not
   authorization.
5. Do not write a fix-specific test or insert substitute validation. Return to
   the exact checkpoint and continue the original operation normally; its
   success is the repair evidence. For standalone invocation, run the agreed
   acceptance test. Continue or reassess the repair loop if this evidence fails.
6. Only this focused route may update `TROUBLESHOOTING.md` with a portable
   problem, confirmed cause, safe diagnostic, durable repair, authority needs
   and verified acceptance path. Retain an unresolved investigation as an open
   task with its smallest next diagnostic step. Put host facts in ignored
   `TROUBLESHOOTING.local.md`; never record secrets or a quick-exit workaround.
7. Resume or close the original task only after the concrete blockage is gone.
