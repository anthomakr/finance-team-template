# Variant: one fractional CFO, several clients

Full guide: [GitHub for Fractional CFOs](https://layerz.cc/blog/github-for-fractional-cfos).

The two-repo rule becomes **one method repo plus one repo per client**.

```
your-account/
  cfo-method        created from this template, private, yours

client-a (the client's own GitHub organization)/
  finance           their filled FINANCE.md, mappings, runs, exports
client-b/
  finance
```

- **`cfo-method`** is this template: your skills, checks, conventions template, onboarding checklist. No client name anywhere. It improves with every client and follows you.
- **Each client repo lives in the client's organization**, with you invited as a collaborator (free on GitHub Free). At the end of the engagement the client keeps everything and you remove yourself.
- **Never improve a skill inside a client repo.** Every fix goes back to `cfo-method` through a pull request, so every client runs the same version next month.

## Review when you are alone

- **A test instead of a colleague**: rerun the change on a month you already signed, at one client at least, and put the before/after figure in the pull request.
- **The client as approver** for anything that changes their numbers (a mapping, a reclassification, a forecast assumption): open the pull request in the client repo and ask their finance lead or founder to approve.

## Onboarding a client

1. Client creates a GitHub organization and a private `finance` repo, invites you.
2. Copy `FINANCE.md` from `cfo-method` and fill it with the client at kickoff.
3. Map their chart of accounts into `finance/mappings/`.
4. Run your skills on their last closed month and compare with what they reported.
5. Each gap becomes a client mapping (client repo) or a method improvement (pull request to `cfo-method`).

## Offboarding

- Final export of the model to `.xlsx` in the client repo.
- Final changelog entry.
- Merge into `cfo-method` whatever you learned, without their data.
- Remove yourself from their organization.
