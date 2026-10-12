# The `finance-data` repo

Everything specific to the company lives here, in a **separate private repo** with narrower access than `finance-logic`. Do not create it from this template: create an empty private repo and follow this structure.

```
finance-data/
  README.md                 who has access, and why
  entities/
    fr01/
      FINANCE.md            entity-specific conventions (local GAAP, account ranges)
      mappings/             chart of accounts to reporting lines, vendor rules
    uk01/
      ...
  runs/
    fr01/2026-10.md         status file written by the close skill
  exports/
    2026-10-board-pack.xlsx dated record of what was sent
```

## Rules

- Access per entity if needed: a subsidiary controller may not need the other entities.
- Exports are records of what was sent, not working files. Changes happen in the model, not in the export.
- Still no credentials. Data repo is not a secret store.
- Check your contracts, your auditor and your data-protection obligations before storing employee or client personal data here. Payroll detail usually belongs in the payroll system, not in git.
