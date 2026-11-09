---
name: clone-openai-agents-python-repo
description: >-
  Shallow-clone Célia's OpenAI Agents Python fork into
  external/openai-agents-python. Use when the user asks to clone that SDK
  or runs /clone-openai-agents-python-repo.
disable-model-invocation: true
---

# Clone OpenAI Agents Python

- Fork: https://github.com/celiadugnoille-arch/openai-agents-python
- Upstream: https://github.com/openai/openai-agents-python
- Default branch: `main`
- Destination: `external/openai-agents-python`

## Steps

1. If `external/openai-agents-python` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/openai-agents-python.git external/openai-agents-python`.
3. Leave the clone untracked. `external/` is gitignored. Never commit secrets or API keys.
4. Report the path, branch, and upstream. Prefer examples and docs in the clone over remembered SDK shapes.
