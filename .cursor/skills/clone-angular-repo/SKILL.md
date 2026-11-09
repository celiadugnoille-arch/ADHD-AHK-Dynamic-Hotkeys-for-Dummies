---
name: clone-angular-repo
description: >-
  Shallow-clone Célia's Angular fork into external/angular. Use when the
  user asks to clone Angular or runs /clone-angular-repo.
disable-model-invocation: true
---

# Clone Angular

- Fork: https://github.com/celiadugnoille-arch/angular
- Upstream: https://github.com/angular/angular
- Default branch: `main`
- Destination: `external/angular`

## Steps

1. If `external/angular` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/angular.git external/angular`.
3. Leave the clone untracked. `external/` is gitignored. Never commit secrets.
4. Report the path, branch, and upstream. Read `AGENTS.md` and `CONTRIBUTING.md` first; framework packages live under `packages/`, docs under `adev/`, and agent skills under `skills/`.

The clone is very large (~670 MB). Only clone when the task needs the Angular source, always with `--depth 1`. For a single file, prefer the GitHub API.
