---
name: clone-i-have-adhd-repo
description: >-
  Shallow-clone Célia's i-have-adhd skill fork into external/i-have-adhd.
  Use when the user asks to clone that repo or runs
  /clone-i-have-adhd-repo.
disable-model-invocation: true
---

# Clone i-have-adhd

- Fork: https://github.com/celiadugnoille-arch/i-have-adhd
- Upstream: https://github.com/ayghri/i-have-adhd
- Default branch: `main`
- Destination: `external/i-have-adhd`

## Steps

1. If `external/i-have-adhd` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/i-have-adhd.git external/i-have-adhd`.
3. Leave the clone untracked. `external/` is gitignored.
4. Report the path and branch. The skill text is `skills/i-have-adhd/SKILL.md` (also copied under `.cursor/skills/i-have-adhd/`). Read that file before applying ADHD output rules from this clone.
