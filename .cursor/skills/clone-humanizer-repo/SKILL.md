---
name: clone-humanizer-repo
description: >-
  Shallow-clone the humanizer agent skill (blader/humanizer) into
  external/humanizer. Use when the user asks to clone the humanizer repo,
  add the humanizer skill source, or run /clone-humanizer-repo.
disable-model-invocation: true
---

# Clone humanizer

Célia has no `humanizer` fork. The public skill repo is
https://github.com/blader/humanizer (default branch `main`).

## Steps

1. From the workspace root, if `external/humanizer` is already a git checkout, run `git -C external/humanizer fetch --depth 1 origin main` and `git -C external/humanizer pull --ff-only`.
2. Otherwise run `git clone --depth 1 --branch main https://github.com/blader/humanizer.git external/humanizer`.
3. Do not commit `external/`. It is gitignored. Do not copy `.env` or tokens.
4. Read `external/humanizer/SKILL.md` before using the skill. Report the path, the checked-out commit, and that the source is `blader/humanizer`.
