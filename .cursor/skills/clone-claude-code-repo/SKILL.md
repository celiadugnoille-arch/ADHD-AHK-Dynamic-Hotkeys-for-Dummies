---
name: clone-claude-code-repo
description: >-
  Shallow-clone Célia's Claude Code fork into external/claude-code. Use
  when the user asks to clone Claude Code or runs /clone-claude-code-repo.
disable-model-invocation: true
---

# Clone Claude Code

- Fork: https://github.com/celiadugnoille-arch/claude-code
- Upstream: https://github.com/anthropics/claude-code
- Default branch: `main`
- Destination: `external/claude-code`

The public Claude Code repo: changelog, docs, examples, and plugins. Use it as the source of truth for plugin and hook shapes instead of guessing.

## Steps

1. If `external/claude-code` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/claude-code.git external/claude-code`.
3. Leave the clone untracked. `external/` is gitignored. Never commit API keys.
4. Report the path, branch, and upstream. Read `README.md` and `CHANGELOG.md`, then `plugins/` and `examples/`.
