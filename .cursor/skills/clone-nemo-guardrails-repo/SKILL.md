---
name: clone-nemo-guardrails-repo
description: >-
  Shallow-clone Célia's NeMo Guardrails fork into external/Guardrails.
  Use when the user asks to clone NeMo Guardrails or runs
  /clone-nemo-guardrails-repo.
disable-model-invocation: true
---

# Clone NeMo Guardrails

- Fork: https://github.com/celiadugnoille-arch/Guardrails
- Upstream: https://github.com/NVIDIA-NeMo/Guardrails
- Default branch: `develop` (not `main`)
- Destination: `external/Guardrails`

## Steps

1. If `external/Guardrails` is already a git checkout, fetch and fast-forward `develop`.
2. Otherwise: `git clone --depth 1 --branch develop https://github.com/celiadugnoille-arch/Guardrails.git external/Guardrails`.
3. Leave the clone untracked. `external/` is gitignored. Never commit secrets.
4. Report the path, branch, and upstream. Read the repo docs before writing rail configs.
