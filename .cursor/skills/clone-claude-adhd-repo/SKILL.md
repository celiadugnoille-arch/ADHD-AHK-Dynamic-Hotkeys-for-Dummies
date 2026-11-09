---
name: clone-claude-adhd-repo
description: >-
  Shallow-clone Célia's claude-adhd fork (gentle reminders for unfinished
  threads) into external/claude-adhd. Use when the user asks to clone
  claude-adhd or runs /clone-claude-adhd-repo.
disable-model-invocation: true
---

# Clone claude-adhd

- Fork: https://github.com/celiadugnoille-arch/claude-adhd
- Upstream: https://github.com/shaheer-00/claude-adhd
- Default branch: `master` (not `main`)
- Destination: `external/claude-adhd`

A Claude Code plugin that surfaces unfinished threads from past sessions. Upstream calls it test mode, so treat its behavior as experimental.

## Steps

1. If `external/claude-adhd` is already a git checkout, fetch and fast-forward `master`.
2. Otherwise: `git clone --depth 1 --branch master https://github.com/celiadugnoille-arch/claude-adhd.git external/claude-adhd`.
3. Leave the clone untracked. `external/` is gitignored.
4. Report the path, branch, and upstream. Read `README.md`, then `skills/`, `commands/`, and `hooks/` — the hooks are what run on session start.
