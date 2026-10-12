# FINANCE.md

<!--
Conventions every agent and every skill reads at the start of a session.
Format: the open FINANCE.md spec, https://github.com/layerzlabs/finance-md
Fill the blanks. Keep it generic enough to sit in the logic repo: entity-specific
values (account numbers, entity codes) go in finance-data/entities/<entity>/FINANCE.md.
-->

## Company

- Name: <!-- ACME Group -->
- Business: <!-- one sentence: what the company sells, to whom -->
- Entities: <!-- list, details in finance-data -->

## Units

- Reporting currency: <!-- EUR -->
- Unit in reports: <!-- thousands (k) -->
- Fiscal year: <!-- January to December -->
- Granularity: <!-- monthly actuals, monthly forecast, annual budget -->

## Sign convention

<!-- Pick one and delete the other -->
- Revenue positive, expenses negative. Subtotals are simple sums.
- All amounts positive, the line label carries the sign.

## Glossary

| Term | Meaning here |
|---|---|
| Revenue | <!-- recognised revenue, excluding VAT, net of discounts --> |
| EBITDA | <!-- definition used in the board pack --> |
| Cash | <!-- bank balances, excluding restricted cash --> |

## Structure

- P&L: <!-- main sections, top to bottom -->
- Balance sheet: <!-- main sections -->
- Cash flow: <!-- direct or indirect -->

## Rules for agents

- Never hard-code a value in a statement: statements are derived from actuals or from assumptions.
- Never mix actuals and forecast on the same line without saying which months are which.
- When a check fails, stop and explain; do not adjust a figure to make it pass.
