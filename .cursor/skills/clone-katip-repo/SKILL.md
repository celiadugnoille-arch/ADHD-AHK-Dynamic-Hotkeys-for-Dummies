---
name: clone-katip-repo
description: >-
  Shallow-clone Célia's katip fork (meeting transcription and action
  items) into external/katip. Use when the user asks to clone katip or
  runs /clone-katip-repo.
disable-model-invocation: true
---

# Clone katip

- Fork: https://github.com/celiadugnoille-arch/katip
- Upstream: https://github.com/odest/katip
- Default branch: `master` (not `main`)
- Destination: `external/katip`

Transcribes recordings, lectures, and interviews, then summarizes them and extracts action items.

## Steps

1. If `external/katip` is already a git checkout, fetch and fast-forward `master`.
2. Otherwise: `git clone --depth 1 --branch master https://github.com/celiadugnoille-arch/katip.git external/katip`.
3. Leave the clone untracked. `external/` is gitignored. Never commit API keys.
4. Report the path, branch, and upstream. It is a pnpm/turbo monorepo: read `README.md`, `turbo.json`, then `apps/` and `packages/`.
