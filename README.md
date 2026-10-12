# GitHub for Finance Teams: Repo Template

> A ready-to-use GitHub repository for a finance team that builds with AI: skills, conventions, checks and a review loop, with company data kept out by design. Free, MIT, built by a former Deloitte modelling director who now works as a fractional CFO.

[![Use this template](https://img.shields.io/badge/Use_this_template-Create_your_finance_repo-2D6BFF?logo=github)](https://github.com/anthomakr/finance-team-template/generate)

Finance teams using Claude, Claude Code or other agents end up with skills, prompts and scripts on every laptop. Nobody knows which version ran last month's close, and automations leave when their owners go on holiday. This template gives that work one shared home with three things a shared drive cannot offer:

- **History**: every version of every skill, with who changed it and why.
- **Review**: a change waits in a pull request until someone approves it.
- **Separation**: reusable logic in this repo, company data somewhere else.

Full walkthrough: **[GitHub for Finance Teams: A Setup Guide for CFOs](https://layerz.cc/blog/github-for-finance-teams)**. Working alone across several clients? See **[GitHub for Fractional CFOs](https://layerz.cc/blog/github-for-fractional-cfos)** and [`docs/fractional-cfo.md`](docs/fractional-cfo.md).

---

## The rule: two repos, not one

| Repo | Holds | Access |
|---|---|---|
| **`finance-logic`** (this template) | Skills, prompts, checks, conventions. **No company data** | The whole finance team |
| **`finance-data`** | Mappings, entity settings, close outputs, exports | Narrower, per entity if needed. Structure in [`docs/data-repo.md`](docs/data-repo.md) |

The test for where a file goes: *would it be useful, unchanged, at a different company?* Yes means logic. No means data.

This repo enforces the rule twice: a [`.gitignore`](.gitignore) that refuses spreadsheets, CSV exports and secrets, and a [GitHub Action](.github/workflows/no-company-data.yml) that fails any pull request trying to add them anyway.

---

## What's inside

```
finance-team-template/
  README.md                         this page
  RULES.md                          the 10 rules the team follows
  FINANCE.md                        conventions every agent reads first (fill the blanks)
  CHANGELOG.md                      one line per merged change, written for an auditor
  skills/
    month-end-close/SKILL.md        example skill: close checklist an agent runs
    variance-commentary/SKILL.md    example skill: budget vs actual commentary
  checks/
    tie-outs.md                     the checks every close must pass
  prompts/
    README.md                       how to store a reviewed prompt
  docs/
    data-repo.md                    structure of the separate finance-data repo
    review-loop.md                  how a change reaches production
    fractional-cfo.md               variant for one person serving several clients
  .github/
    pull_request_template.md        what / why / proof / risk
    CODEOWNERS                      who approves which area
    workflows/no-company-data.yml   blocks data files and secrets
```

---

## Set it up in an afternoon

1. **Create a GitHub organization** for the finance function (`acme-finance`), not a personal account. The repos belong to the team; people come and go.
2. **Click "Use this template"**, name the new repo `finance-logic`, make it private.
3. **Fill [`FINANCE.md`](FINANCE.md)**: currency, units, sign convention, fiscal year, glossary.
4. **Edit [`.github/CODEOWNERS`](.github/CODEOWNERS)** with the people who approve each area.
5. **Move your three most used skills** into `skills/`, one folder each.
6. **Take one change through the [review loop](docs/review-loop.md)**: branch, change, test on a month you already closed, pull request, approval, merge.
7. **Create `finance-data`** next to it, following [`docs/data-repo.md`](docs/data-repo.md).

### One paid detail

Required reviewers and branch rules only apply to **public** repositories on GitHub Free. Your finance repos are private, so without the **GitHub Team** plan anyone with write access can still merge without approval. If an auditor may ever ask who approved a change to the close, turn it on (pricing on [github.com/pricing](https://github.com/pricing)), then protect `main` and require one approval plus CODEOWNERS review.

---

## And the financial model?

Git reads text, not workbooks. It stores every version of a `.xlsx` but cannot show which formula or which number changed inside. Keep skills and conventions here; keep the model in a structured form with its own history and diff, and treat Excel as the export you send.

[Layerz](https://layerz.cc) is one way to do that: a structured spreadsheet ready for AI, where Claude builds and edits the model over MCP, every change is recorded, scenarios are branches, two versions can be diffed formula by formula, and the export to Excel stays clean. Free for one person, unlimited models. Ready-made models to fork: [finance-models](https://github.com/anthomakr/finance-models).

The conventions file follows the open [FINANCE.md](https://github.com/layerzlabs/finance-md) spec, so any agent or tool that reads it understands your model the same way.

---

## Contributing

Improvements to the example skills, checks or docs are welcome: open a pull request. Keep everything generic: no company names, no real figures.

## License

[MIT](LICENSE). Use it, fork it, rename it, sell your services on top of it.
