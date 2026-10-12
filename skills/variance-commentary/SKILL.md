---
name: variance-commentary
description: Draft the budget vs actual commentary for a closed month. Use when the user asks for variance analysis, management commentary or the "why" behind the month's numbers.
---

# Variance commentary

Example skill.

## Inputs

- Actuals and budget for the month and year to date, at the granularity defined in `FINANCE.md`.
- The materiality threshold: <!-- e.g. 5% and 10k, whichever is higher -->

## Steps

1. Compute the variance per line, month and year to date.
2. Keep only lines above the threshold.
3. For each, say **what** moved (volume, price, timing, one-off) and **where the evidence is** (the transactions or the driver that explain it).
4. Separate timing differences (will reverse) from real ones (will not).
5. Draft three sentences for the board: the headline, the main driver, what changes for the forecast.

## Rules

- Every number in the commentary comes from the data. No rounding that changes the story.
- If the cause is not in the data, write "cause to confirm with <owner>", do not guess.
- Use the sign convention from `FINANCE.md`: a favourable expense variance is said in words, not inferred from a sign.
