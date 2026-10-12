---
name: month-end-close
description: Run the month-end close checklist for one entity. Use when the user asks to start, continue or check the status of a monthly close.
---

# Month-end close

Example skill. Adapt the steps to your close, keep entity-specific values out of this file.

## Before you start

1. Read `FINANCE.md` (logic repo) and `entities/<entity>/FINANCE.md` (data repo).
2. Ask which entity and which month, if not given.
3. Read the previous month's run in `finance-data/runs/<entity>/` to know where things stood.

## Steps

Work through them in order. After each step, record its status (done, blocked, skipped with reason) in the run file `finance-data/runs/<entity>/<YYYY-MM>.md`.

1. **Bank**: every bank account reconciled to the statement balance at month end.
2. **Revenue cut-off**: invoices issued vs delivered; list anything delivered and not invoiced.
3. **Accruals**: recurring accruals from the previous month, reversed and re-booked; new ones listed with their basis.
4. **Prepaid and deferred**: schedules rolled forward.
5. **Payroll**: payroll journal vs payroll report, to the unit.
6. **Intercompany**: balances agree on both sides.
7. **Checks**: run every check in `checks/tie-outs.md`.
8. **Variance**: hand over to the `variance-commentary` skill.

## Never

- Post a journal entry without the user's explicit approval.
- Adjust a figure to make a check pass. Report the gap and its likely cause instead.
- Copy figures from one entity's run into another's.

## Output

A short status table (step, status, open points) and the list of decisions the user needs to take.
