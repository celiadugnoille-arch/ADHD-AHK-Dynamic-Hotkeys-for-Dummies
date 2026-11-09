---
name: clone-sayso-repo
description: >-
  Shallow-clone Célia's sayso fork (push-to-talk Android dictation) into
  external/sayso. Use when the user asks to clone sayso or runs
  /clone-sayso-repo.
disable-model-invocation: true
---

# Clone sayso

- Fork: https://github.com/celiadugnoille-arch/sayso
- Upstream: https://github.com/stevengonsalvez/sayso
- Default branch: `main`
- Destination: `external/sayso`

Push-to-talk dictation for Android with on-device and cloud transcription, cleanup, and a personal vocabulary. One of several dictation repos Célia follows, alongside `iDictate` and `NotelyVoice`.

## Steps

1. If `external/sayso` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/sayso.git external/sayso`.
3. Leave the clone untracked. `external/` is gitignored. Never commit API keys or keystores.
4. Report the path, branch, and upstream. Read `README.md`, `PRODUCT.md`, and `DESIGN.md` before touching `app/`.
