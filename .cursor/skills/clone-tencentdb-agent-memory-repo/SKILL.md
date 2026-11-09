---
name: clone-tencentdb-agent-memory-repo
description: >-
  Shallow-clone Célia's TencentDB Agent Memory fork into
  external/TencentDB-Agent-Memory. Use when the user asks to clone
  TencentDB Agent Memory or runs /clone-tencentdb-agent-memory-repo.
disable-model-invocation: true
---

# Clone TencentDB Agent Memory

- Fork: https://github.com/celiadugnoille-arch/TencentDB-Agent-Memory
- Upstream: https://github.com/TencentCloud/TencentDB-Agent-Memory
- Default branch: `feat/server_team` (not `main`)
- Destination: `external/TencentDB-Agent-Memory`

A team-level memory hub for agents: chat memory, skills, LLM-wiki, and code-graph as shared assets.

## Steps

1. If `external/TencentDB-Agent-Memory` is already a git checkout, fetch and fast-forward `feat/server_team`.
2. Otherwise: `git clone --depth 1 --branch feat/server_team https://github.com/celiadugnoille-arch/TencentDB-Agent-Memory.git external/TencentDB-Agent-Memory`.
3. Leave the clone untracked. `external/` is gitignored. Never commit secrets or database credentials.
4. Report the path, branch, and upstream. Read `README.md`, `INSTALL.md`, and `README.deployment.md` before touching `MemoryCore/`, `MemoryProxy/`, or `deploy/`.

The clone is large (~65 MB). Keep `--depth 1`.
