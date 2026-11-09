---
name: clone-retext-simplify-repo
description: >-
  Shallow-clone Célia's retext-simplify fork (checks phrases for simpler
  alternatives) into external/retext-simplify. Use when the user asks to
  clone retext-simplify or runs /clone-retext-simplify-repo.
disable-model-invocation: true
---

# Clone retext-simplify

- Fork: https://github.com/celiadugnoille-arch/retext-simplify
- Upstream: https://github.com/retextjs/retext-simplify
- Default branch: `main`
- Destination: `external/retext-simplify`

A retext plugin that flags complicated phrases and suggests simpler ones. Useful for plain-language passes on English text; its rule list is English-only.

## Steps

1. If `external/retext-simplify` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/retext-simplify.git external/retext-simplify`.
3. Leave the clone untracked. `external/` is gitignored.
4. Report the path, branch, and upstream. The repo is tiny: `index.js`, `lib/`, and `readme.md` are the whole surface.
