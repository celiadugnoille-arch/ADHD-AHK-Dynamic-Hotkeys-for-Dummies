---
name: clone-mindwtr-repo
description: >-
  Shallow-clone Célia's Mindwtr fork (offline GTD to-do app) into
  external/Mindwtr. Use when the user asks to clone Mindwtr or runs
  /clone-mindwtr-repo.
disable-model-invocation: true
---

# Clone Mindwtr

- Fork: https://github.com/celiadugnoille-arch/Mindwtr
- Upstream: https://github.com/dongdongbh/Mindwtr
- Default branch: `main`
- Destination: `external/Mindwtr`

A free GTD to-do app for desktop and mobile that works offline with no account. Useful as a reference for capture-first task flows.

## Steps

1. If `external/Mindwtr` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/Mindwtr.git external/Mindwtr`.
3. Leave the clone untracked. `external/` is gitignored. Never commit secrets.
4. Report the path, branch, and upstream. It is a Bun monorepo: read `README.md`, `package.json`, then `apps/` and `packages/` before changing behavior.

The clone is large (~235 MB). Keep `--depth 1` and expect the clone to take a few minutes.
