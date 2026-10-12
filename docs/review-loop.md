# The review loop

Every change, however small, follows the same path.

1. **Branch**: one branch per change, named after it (`fix-accrual-intercompany`).
2. **Change**: often written by Claude Code or another agent.
3. **Test on a closed month**: run the changed skill or check on a month you already signed. You know the answer; the change must reproduce it, or explain the difference.
4. **Pull request**: fill the template (what, why, proof, risk).
5. **Review**: someone other than the author approves or asks for changes. CODEOWNERS routes it to the right person.
6. **Merge**, then add one line to `CHANGELOG.md`.

## Enforce it

On a private repo this needs the GitHub Team plan. Then, in Settings, add a branch rule (or ruleset) on `main`:

- Require a pull request before merging, with 1 approval.
- Require review from Code Owners.
- Require the `no-company-data` status check to pass.
- Do not allow bypassing the above settings (yes, including admins).

## During the close

Close skills are frozen from day 1 of the close until sign-off. A fix found during the close is written down, then shipped through the loop afterwards. Exception only with the CFO's approval written in the pull request.
