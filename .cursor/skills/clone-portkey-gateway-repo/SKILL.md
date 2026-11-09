---
name: clone-portkey-gateway-repo
description: >-
  Shallow-clone Célia's Portkey AI Gateway fork (garde-fou-1) into
  external/garde-fou-1. Use when the user asks to clone the Portkey
  gateway or runs /clone-portkey-gateway-repo.
disable-model-invocation: true
---

# Clone Portkey gateway

- Fork: https://github.com/celiadugnoille-arch/garde-fou-1
- Upstream: https://github.com/Portkey-AI/gateway
- Default branch: `main`
- Destination: `external/garde-fou-1`

## Steps

1. If `external/garde-fou-1` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/garde-fou-1.git external/garde-fou-1`.
3. Leave the clone untracked. `external/` is gitignored. Never commit provider keys or Portkey API keys.
4. Report the path, branch, and upstream. This tree is large; read the local README and the file you need instead of scanning the whole repo.
