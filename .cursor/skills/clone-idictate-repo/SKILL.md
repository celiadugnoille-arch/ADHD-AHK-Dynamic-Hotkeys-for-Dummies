---
name: clone-idictate-repo
description: >-
  Shallow-clone Célia's iDictate fork (Android + Wear OS dictation) into
  external/iDictate. Use when the user asks to clone iDictate or runs
  /clone-idictate-repo.
disable-model-invocation: true
---

# Clone iDictate

- Fork: https://github.com/celiadugnoille-arch/iDictate
- Upstream: https://github.com/petepiet/iDictate
- Default branch: `main`
- Destination: `external/iDictate`

Voice dictation and AI assistant for Android phone and Wear OS: transcription via OpenAI, analysis via Claude. Unlike `NotelyVoice`, it sends audio to cloud APIs.

## Steps

1. If `external/iDictate` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/iDictate.git external/iDictate`.
3. Leave the clone untracked. `external/` is gitignored. Never commit API keys or keystores.
4. Report the path, branch, and upstream. Read `README.md`, `CLAUDE.md`, and `ROADMAP.md`, then `app/` and `phone/`.
