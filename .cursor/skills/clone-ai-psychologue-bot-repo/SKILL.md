---
name: clone-ai-psychologue-bot-repo
description: >-
  Shallow-clone Célia's Dr. Émile Telegram bot into
  external/Ai-psychologue-bot. Use when the user asks to clone the
  psychologue bot or runs /clone-ai-psychologue-bot-repo.
disable-model-invocation: true
---

# Clone AI psychologue bot

- Fork: https://github.com/celiadugnoille-arch/Ai-psychologue-bot
- Upstream: https://github.com/nvikou/Ai-psychologue-bot
- Default branch: `main`
- Destination: `external/Ai-psychologue-bot`

Dr. Émile is a supportive chat assistant, not a licensed clinician. Crisis messages are handled in `backend/app/services/crisis_service.py` and `i18n_service.py` and must not enter the therapy graph.

## Steps

1. If `external/Ai-psychologue-bot` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/Ai-psychologue-bot.git external/Ai-psychologue-bot`.
3. Leave the clone untracked. `external/` is gitignored. Never commit `.env`, tokens, or encryption keys.
4. Report the path, branch, and upstream. Read `README.md` and `backend/app/config.py` before editing prompts or crisis copy.
