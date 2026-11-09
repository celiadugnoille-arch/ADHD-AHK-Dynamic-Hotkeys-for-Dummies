---
name: clone-notelyvoice-repo
description: >-
  Shallow-clone Célia's NotelyVoice fork (private on-device voice
  transcription) into external/NotelyVoice. Use when the user asks to
  clone NotelyVoice or runs /clone-notelyvoice-repo.
disable-model-invocation: true
---

# Clone NotelyVoice

- Fork: https://github.com/celiadugnoille-arch/NotelyVoice
- Upstream: https://github.com/Notely-Voice/NotelyVoice
- Default branch: `main`
- Destination: `external/NotelyVoice`

A fully private speech-to-text app for Android and iOS built with Compose Multiplatform and Whisper. Nothing is uploaded; all processing is on-device.

## Steps

1. If `external/NotelyVoice` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/NotelyVoice.git external/NotelyVoice`.
3. Leave the clone untracked. `external/` is gitignored. Never commit keystores or signing secrets.
4. Report the path, branch, and upstream. Read `README.md`, then `shared/`, `core/`, and `iosApp/`.

The clone is large (~85 MB) because of bundled model and native assets. Keep `--depth 1`.
