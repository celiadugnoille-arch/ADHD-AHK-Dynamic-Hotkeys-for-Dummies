---
name: clone-lightagent-repo
description: >-
  Shallow-clone Célia's LightAgent fork (lightweight Python agent
  framework) into external/LightAgent. Use when the user asks to clone
  LightAgent or runs /clone-lightagent-repo.
disable-model-invocation: true
---

# Clone LightAgent

- Fork: https://github.com/celiadugnoille-arch/LightAgent
- Upstream: https://github.com/wanxingai/LightAgent
- Default branch: `main`
- Destination: `external/LightAgent`

A small OpenAI-compatible agent framework with tools, memory, guardrails, tracing, lifecycle hooks, and multi-agent workflows. Compare it with `openai-agents-python` before picking a framework.

## Steps

1. If `external/LightAgent` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/LightAgent.git external/LightAgent`.
3. Leave the clone untracked. `external/` is gitignored. Never commit API keys.
4. Report the path, branch, and upstream. `README.fr.md` is the French readme. Read it or `README.md`, then `LightAgent/`, `example/`, and `skills/`.
