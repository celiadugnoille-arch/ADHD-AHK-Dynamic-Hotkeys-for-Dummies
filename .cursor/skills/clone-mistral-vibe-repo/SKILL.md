---
name: clone-mistral-vibe-repo
description: >-
  Shallow-clone Célia's mistral-vibe fork (Mistral's minimal CLI coding
  agent) into external/mistral-vibe. Use when the user asks to clone
  mistral-vibe or runs /clone-mistral-vibe-repo.
disable-model-invocation: true
---

# Clone mistral-vibe

- Fork: https://github.com/celiadugnoille-arch/mistral-vibe
- Upstream: https://github.com/mistralai/mistral-vibe
- Default branch: `main`
- Destination: `external/mistral-vibe`

A minimal CLI coding agent by Mistral. Useful as a compact reference for agent loops, tool calls, and harness design.

## Steps

1. If `external/mistral-vibe` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/mistral-vibe.git external/mistral-vibe`.
3. Leave the clone untracked. `external/` is gitignored. Never commit API keys.
4. Report the path, branch, and upstream. Read `AGENTS.md`, `README.md`, and `pyproject.toml`, then the `vibe/` and `harness/` directories.
