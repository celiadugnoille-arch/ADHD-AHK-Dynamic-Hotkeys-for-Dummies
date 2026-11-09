---
name: clone-awesome-adhd-repo
description: >-
  Shallow-clone Célia's awesome-adhd fork (curated ADHD apps, books, and
  resources) into external/awesome-adhd. Use when the user asks to clone
  awesome-adhd or runs /clone-awesome-adhd-repo.
disable-model-invocation: true
---

# Clone awesome-adhd

- Fork: https://github.com/celiadugnoille-arch/awesome-adhd
- Upstream: https://github.com/XargsUK/awesome-adhd
- Default branch: `main`
- Destination: `external/awesome-adhd`

A curated list of ADHD apps, books, ideas, and resources. Use it as a source list when looking for existing tools instead of inventing one.

## Steps

1. If `external/awesome-adhd` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/awesome-adhd.git external/awesome-adhd`.
3. Leave the clone untracked. `external/` is gitignored.
4. Report the path, branch, and upstream. The content is `README.md` plus `resources/`; `AGENTS.md` describes the entry format if adding a resource.

The repo is tiny (~150 KB), so cloning it is cheap.
