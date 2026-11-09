---
name: clone-claude-plugins-official-repo
description: >-
  Shallow-clone Célia's claude-plugins-official fork into
  external/claude-plugins-official. Use when the user asks to clone the
  official Claude plugins directory or runs
  /clone-claude-plugins-official-repo.
disable-model-invocation: true
---

# Clone claude-plugins-official

- Fork: https://github.com/celiadugnoille-arch/claude-plugins-official
- Upstream: https://github.com/anthropics/claude-plugins-official
- Default branch: `main`
- Destination: `external/claude-plugins-official`

Anthropic's curated directory of Claude Code plugins. Read it before writing a new plugin manifest so the structure matches real, accepted examples.

## Steps

1. If `external/claude-plugins-official` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/claude-plugins-official.git external/claude-plugins-official`.
3. Leave the clone untracked. `external/` is gitignored. Never commit secrets.
4. Report the path, branch, and upstream. Read `README.md`, then browse `plugins/` and `external_plugins/`.
