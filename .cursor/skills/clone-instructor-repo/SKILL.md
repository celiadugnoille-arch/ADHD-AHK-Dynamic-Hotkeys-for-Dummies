---
name: clone-instructor-repo
description: >-
  Shallow-clone Célia's instructor fork (structured LLM outputs) into
  external/instructor. Use when the user asks to clone instructor or runs
  /clone-instructor-repo.
disable-model-invocation: true
---

# Clone instructor

- Fork: https://github.com/celiadugnoille-arch/instructor
- Upstream: https://github.com/567-labs/instructor
- Default branch: `main`
- Destination: `external/instructor`

## Steps

1. If `external/instructor` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/instructor.git external/instructor`.
3. Leave the clone untracked. `external/` is gitignored. Never commit secrets.
4. Report the path, branch, and upstream. Use the clone as the source of truth for Instructor APIs instead of guessing.
