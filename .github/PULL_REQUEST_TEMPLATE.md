Closes #

## What changed and why

<!-- One paragraph of reasoning. The diff already says what; say why it had to. -->

## Checks

- [ ] Tests pass.
- [ ] Anything touching data **fails closed** — no silent fallback to fewer rows, to a
      default value, or to "absent" on an error that was not confirmed as absence.
- [ ] A schema migration, if any, is idempotent and guarded, and this PR body states the
      exact command to run it.
- [ ] Docs updated where behaviour changed, in the one document whose job it is.
- [ ] *(repos that vendor `dev-standards`)* vendored files untouched — `dev-standards check`.
- [ ] *(repos with lanes/owners)* I stayed in the files my lane owns, or the other owner is
      tagged and knows why.

## Maintainer steps after merge

<!-- Migrations to run, workflows to trigger, variables or secrets to set.
     "None" is a valid answer — say it rather than leaving this blank. -->
