---
name: clone-accelerated-text-repo
description: >-
  Shallow-clone Célia's accelerated-text fork (no-code natural language
  generation) into external/accelerated-text. Use when the user asks to
  clone accelerated-text or runs /clone-accelerated-text-repo.
disable-model-invocation: true
---

# Clone accelerated-text

- Fork: https://github.com/celiadugnoille-arch/accelerated-text
- Upstream: https://github.com/accelerated-text/accelerated-text
- Default branch: `master` (not `main`)
- Destination: `external/accelerated-text`

A no-code natural language generation platform: build document plans that turn data into varied text. Template-based, not LLM-based.

## Steps

1. If `external/accelerated-text` is already a git checkout, fetch and fast-forward `master`.
2. Otherwise: `git clone --depth 1 --branch master https://github.com/celiadugnoille-arch/accelerated-text.git external/accelerated-text`.
3. Leave the clone untracked. `external/` is gitignored.
4. Report the path, branch, and upstream. It runs through Docker: read `README.md`, `docker-compose.yml`, and `docs/`, then `core/`, `api/`, and `front-end/`.

The clone is ~30 MB. Keep `--depth 1`.
