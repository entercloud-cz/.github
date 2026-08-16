# Contributing — entercloud-cz

This file is the org-wide default. A repository with its own `CONTRIBUTING.md` overrides it,
and its own file wins on anything specific.

## Start by reading the repo's agent file

Every repo of ours carries a `CLAUDE.md` (or `AGENTS.md`) at the root. It is written for AI
assistants but it is the fastest orientation for a person too: what the project is, which
invariants must not be broken, who owns which files, and the gotchas that already caused an
incident. Read it before the code.

## Work is tracked before it is done

An untracked change is invisible to everyone else until it lands on the default branch.
So: **file the issue first**, then work. What an issue needs to be actionable:

- **Why it matters** — the impact, in one sentence. Not "improve X".
- **Done when** — verifiable criteria, including how they will be verified.
- **Likely files** — which parts of the repo this touches.

Pure questions and investigations need no issue. A fix small enough to sit inside the scope
of the issue you are already working on needs no second issue — say so when closing it.

## Branches and pull requests

One branch per issue, one issue per branch, named after the issue so the two cannot drift
apart. Merge to the default branch via a pull request whose body contains `Closes #<n>`.

Do not amend commits that are already pushed.

## Documentation belongs in exactly one place

Each document has one job: what the system *is*, what a *user* can do, the *decisions* and
what they cost, the *how-to* for operators, and the agent file's invariants. Write a fact in
the document whose job it is, and **cross-reference instead of repeating** — two copies do
not stay in step, and when they disagree both look authoritative.

Say **why**, not just what. "Added retry" is a changelog line; "retries because a shared run
id let a retry rewrite published content" is knowledge that survives.

## Shared standards

The reusable parts of this working agreement — the Claude Code skills that encode it, and the
issue tooling — live in [`entercloud-cz/dev-standards`](https://github.com/entercloud-cz/dev-standards).
Repos **vendor** them (copies committed, version pinned) so a clone works with no setup.

Change a shared file **there**, not in the consumer: a local edit is overwritten by the next
update and never reaches the other repos. Where the repo installed the drift check, CI fails
on it — but that check is a seatbelt, not a lock, so do not rely on it to notice for you.
