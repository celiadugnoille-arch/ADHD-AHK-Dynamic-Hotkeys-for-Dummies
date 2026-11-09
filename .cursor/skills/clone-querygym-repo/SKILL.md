---
name: clone-querygym-repo
description: >-
  Shallow-clone Célia's QueryGym fork (LLM query reformulation toolkit)
  into external/QueryGym. Use when the user asks to clone QueryGym or
  runs /clone-querygym-repo.
disable-model-invocation: true
---

# Clone QueryGym

- Fork: https://github.com/celiadugnoille-arch/QueryGym
- Upstream: https://github.com/ls3-lab/QueryGym
- Default branch: `main`
- Destination: `external/QueryGym`

A reproducible toolkit for LLM-based query reformulation — relevant when rewriting search queries for research work.

## Steps

1. If `external/QueryGym` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/QueryGym.git external/QueryGym`.
3. Leave the clone untracked. `external/` is gitignored. Never commit API keys.
4. Report the path, branch, and upstream. Read `README.md`, `pyproject.toml`, and `dataset_registry.yaml`, then `querygym/` and `examples/`.

The clone is large (~215 MB). Keep `--depth 1`.
