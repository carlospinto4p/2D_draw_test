# CLAUDE.md — 2D_draw_test

A Processing sketch (`Animation/`) that draws and animates in 2D.

## Merge Into `master` After Every Prompt

Work happens on a branch, never on `master`, but it does not stay there:
**every prompt that changes the repository ends with its branch merged
into `master`** (owner, 23rd November 2026). This holds in every
session, local, on the web or in Claude Code on the phone, and in every
one of the owner's repositories. The reason: a new session starts from
`master`, so anything left on a branch is invisible to it.

- **When**: at the end of every prompt that committed something, even
  when the larger task it belongs to is not finished. Commit what is
  done in a working state, push, then merge. Not after each commit
  within a prompt: once, at its end.
- **CI**: there is none here, so there is nothing to wait for. If
  checks are ever added, merge only once they pass on the head commit.
- **How**: open a pull request from the branch into `master` (or reuse
  the one already open for it) and merge it straight away with a merge
  commit, without asking: this rule is the standing permission. No
  squash and no rebase, so the branch's commits stay as they are and
  the next prompt continues on the same branch.
- **After merging**, check that `master` now holds the head commit, and
  tell the user it was merged. If GitHub refuses the merge (a conflict,
  a protection rule), say so and why instead of working around it.
