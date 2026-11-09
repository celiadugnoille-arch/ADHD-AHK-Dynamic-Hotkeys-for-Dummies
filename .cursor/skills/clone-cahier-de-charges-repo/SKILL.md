---
name: clone-cahier-de-charges-repo
description: >-
  Shallow-clone Célia's Cahier-de-charges fork (grade-management spec
  exercise) into external/Cahier-de-charges. Use when the user asks to
  clone Cahier-de-charges or runs /clone-cahier-de-charges-repo.
disable-model-invocation: true
---

# Clone Cahier-de-charges

- Fork: https://github.com/celiadugnoille-arch/Cahier-de-charges
- Upstream: https://github.com/Arol-123/Cahier-de-charges
- Default branch: `main`
- Destination: `external/Cahier-de-charges`

A small French coursework repo for a grade-management specification. Not to be confused with `Realisez-un-cahier-des-charges-fonctionnel-et-technique-pour-une-application`, the OpenClassrooms exercise.

## Steps

1. If `external/Cahier-de-charges` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/Cahier-de-charges.git external/Cahier-de-charges`.
3. Leave the clone untracked. `external/` is gitignored.
4. Report the path, branch, and upstream. The whole repo is two files: `Note importante.md` and `Participants cahier de charge.md`.
