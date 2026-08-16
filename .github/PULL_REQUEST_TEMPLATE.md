Closes #

## What changed and why

<!-- One paragraph of reasoning. The diff already says what; say why it had to. -->

## Checks

<!-- Only things no machine reports. CI says whether tests pass; the drift check says
     whether a vendored file was edited; CODEOWNERS routes review. None of those needs
     a human to assert it here. -->

- [ ] Anything touching data **fails closed** — no silent fallback to fewer rows, to a
      default value, or to "absent" on an error that was not confirmed as absence.
- [ ] A schema migration, if any, is idempotent and guarded, and this PR body states the
      exact command to run it.
- [ ] Docs updated where behaviour changed, in the one document whose job it is.

## Maintainer steps after merge

<!-- Migrations to run, workflows to trigger, variables or secrets to set.
     "None" is a valid answer — say it rather than leaving this blank. -->
