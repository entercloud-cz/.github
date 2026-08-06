# .github — org-wide defaults for entercloud-cz

GitHub reads this repository for **default community health files**: any repo in the
organisation that does not have its own inherits what is here. A repo's own file always wins,
so these are floors, not mandates.

| File | Applies to |
|---|---|
| `.github/ISSUE_TEMPLATE/task.yml` · `bug.yml` | every repo with no `ISSUE_TEMPLATE` of its own |
| `.github/PULL_REQUEST_TEMPLATE.md` | every repo with no PR template of its own |
| `CONTRIBUTING.md` | every repo with no `CONTRIBUTING.md` of its own |

Nothing here names a product, a person, a label or a path. That is the bar for adding
anything: if it needs one project's vocabulary, it belongs in that project's own files.

**Related:** the reusable *tooling* — Claude Code skills and issue scripts — lives in
[`entercloud-cz/dev-standards`](https://github.com/entercloud-cz/dev-standards) and is
vendored per project. This repo holds only what GitHub itself distributes.

## Checking what a repo actually uses

A repo's own files override these, so to see which templates a given repo serves:

```bash
gh api repos/entercloud-cz/<repo>/contents/.github/ISSUE_TEMPLATE   # 404 ⇒ it inherits
```
