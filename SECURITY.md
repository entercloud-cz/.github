# Security policy — entercloud-cz

## Reporting a vulnerability

**Do not open a public issue.** An issue is world-readable the moment it is filed, which
tells everyone about the hole before there is a fix.

- **On our public repositories**, use GitHub's **Report a vulnerability** button under the
  repository's *Security* tab. It opens a private advisory that only the maintainers can
  read, and it stays private until a fix ships.
- **On a private repository**, tell the maintainer directly. `CODEOWNERS` names who owns
  which paths, and the repository's agent file (`CLAUDE.md` / `AGENTS.md`) says who runs it.
- **If you are outside the organisation and cannot reach either**, write to the address on
  the profile of the account that owns the repository.

## What makes a report useful

The same things any bug report needs, plus the reason it is not a bug report:

- **What an attacker can do with it** — read data belonging to someone else, act as another
  user, run code, deny service. This is what decides urgency, not the cleverness of the flaw.
- **How to reproduce it**, precisely enough that we can watch it happen: the request, the
  input, the sequence. Say if it is intermittent — that is a fact about the flaw, not a gap
  in the report.
- **Where you saw it** — the repository, the environment, a commit or version if you have it.
- Whether it is **already public** anywhere, and whether anything suggests it has been
  exploited.

Proof-of-concept code is welcome. Please do not test against anything that is not yours: no
accessing other people's data, no denial-of-service, no changes to live systems.

## What happens next

We acknowledge the report, tell you whether we could reproduce it, and keep you posted while
it is being fixed. When the fix ships we will say so, and credit you if you want to be
credited — say either way.

If we conclude something is not a vulnerability we will explain why rather than closing in
silence, because a disagreement about severity is worth having in the open.

## Scope

This policy is the organisation-wide default and applies to any repository that does not
publish its own. Vulnerabilities in a third-party dependency belong upstream — tell us as
well if one of our repositories is exposed by it, since the fix on our side is usually a
version bump we can make immediately.
