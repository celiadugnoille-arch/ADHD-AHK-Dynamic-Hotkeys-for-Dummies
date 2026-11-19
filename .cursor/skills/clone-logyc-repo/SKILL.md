---
name: clone-logyc-repo
description: >-
  Shallow-clone Célia's Logyc app (messy notes to clear professional
  documents) into external/Logyc. Use when the user asks to clone Logyc
  or runs /clone-logyc-repo.
disable-model-invocation: true
---

# Clone Logyc

- Fork: https://github.com/celiadugnoille-arch/Logyc
- Upstream: https://github.com/bienwech6-sudo/Logyc
- Default branch: `main`
- Destination: `external/Logyc`

Logyc turns disorganized notes and voice dumps into emails, comptes-rendus, and task lists.

## Steps

1. If `external/Logyc` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/Logyc.git external/Logyc`.
3. Leave the clone untracked. `external/` is gitignored. Never commit secrets.
4. Report the path, branch, and upstream. The repo is small (`main.py`, `requirements.txt`, `Procfile`); read those files before changing behavior.
