---
name: clone-atelier-visuel-repo
description: >-
  Shallow-clone Célia's atelier-visuel fork (living structure for ideas
  and concepts) into external/atelier-visuel. Use when the user asks to
  clone atelier-visuel or runs /clone-atelier-visuel-repo.
disable-model-invocation: true
---

# Clone atelier-visuel

- Fork: https://github.com/celiadugnoille-arch/atelier-visuel
- Upstream: https://github.com/yaya56vv/atelier-visuel
- Default branch: `main`
- Destination: `external/atelier-visuel`

Structuration et sauvegarde des idées et concepts de manière vivante. The repo is documented in French.

## Steps

1. If `external/atelier-visuel` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/atelier-visuel.git external/atelier-visuel`.
3. Leave the clone untracked. `external/` is gitignored. Never commit `.env` files.
4. Report the path, branch, and upstream. Read `CENTRAL.md`, `AGENT.md`, and `ARCHITECTURE_META_GRAPHE.md` before touching `backend/` or `frontend/`; `docs-methode/` holds the working method.
