# The 10 rules

Read on day one. Changes to this file go through a pull request like everything else.

1. **No company data in this repo. Ever.** Mappings, ledgers, exports and outputs live in `finance-data`.
2. **No credentials in any repo.** API keys and ledger tokens go in a secret manager or the agent's own configuration.
3. **One `FINANCE.md`.** Skills read it; they do not restate conventions.
4. **Every change goes through a pull request**, including the CFO's.
5. **A change is tested on a month you already closed.** "It ran without an error" is not a test.
6. **The reviewer is not the author.** Working alone? See [`docs/fractional-cfo.md`](docs/fractional-cfo.md).
7. **One skill, one job.** A skill that "does the close" is ten skills.
8. **No changes to close skills during the close.** Fixes wait for the next business day after sign-off, unless the CFO approves an exception in the pull request.
9. **The changelog is written for an auditor**: what changed, why, who approved, in finance language.
10. **Models are reviewed in their own diff, not as Excel files.** The `.xlsx` is an export.
