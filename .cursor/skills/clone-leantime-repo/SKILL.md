---
name: clone-leantime-repo
description: >-
  Shallow-clone Célia's Leantime fork (ADHD-friendly project management)
  into external/leantime. Use when the user asks to clone Leantime or
  runs /clone-leantime-repo.
disable-model-invocation: true
---

# Clone Leantime

- Fork: https://github.com/celiadugnoille-arch/leantime
- Upstream: https://github.com/Leantime/leantime
- Default branch: `master` (not `main`)
- Destination: `external/leantime`

A goals-focused project management system designed with ADHD, autism, and dyslexia in mind. Good reference for low-friction planning UI.

## Steps

1. If `external/leantime` is already a git checkout, fetch and fast-forward `master`.
2. Otherwise: `git clone --depth 1 --branch master https://github.com/celiadugnoille-arch/leantime.git external/leantime`.
3. Leave the clone untracked. `external/` is gitignored. Never commit `.env` or database credentials.
4. Report the path, branch, and upstream. It is a PHP app: read `README.md`, `CLAUDE.md`, `composer.json`, then `app/` and `config/`.

The clone is large (~260 MB). Keep `--depth 1`.
