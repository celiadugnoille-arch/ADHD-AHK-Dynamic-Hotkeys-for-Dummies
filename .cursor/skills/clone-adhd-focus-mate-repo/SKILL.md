---
name: clone-adhd-focus-mate-repo
description: >-
  Shallow-clone Célia's adhd-focus-mate fork (focus companion app) into
  external/adhd-focus-mate. Use when the user asks to clone
  adhd-focus-mate or runs /clone-adhd-focus-mate-repo.
disable-model-invocation: true
---

# Clone adhd-focus-mate

- Fork: https://github.com/celiadugnoille-arch/adhd-focus-mate
- Upstream: https://github.com/skainguyen1412/adhd-focus-mate
- Default branch: `main`
- Destination: `external/adhd-focus-mate`

A Swift companion app that notices when attention drifts and nudges gently rather than alarming.

## Steps

1. If `external/adhd-focus-mate` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/adhd-focus-mate.git external/adhd-focus-mate`.
3. Leave the clone untracked. `external/` is gitignored. Never commit signing certificates or API keys.
4. Report the path, branch, and upstream. Read `README.md`, `stack_guidelines.md`, and `design_system.md` before touching `ADHDFocusMate/`.
