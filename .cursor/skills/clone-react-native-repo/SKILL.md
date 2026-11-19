---
name: clone-react-native-repo
description: >-
  Shallow-clone Célia's React Native fork into external/react-native. Use
  when the user asks to clone React Native or runs
  /clone-react-native-repo.
disable-model-invocation: true
---

# Clone React Native

- Fork: https://github.com/celiadugnoille-arch/react-native
- Upstream: https://github.com/react/react-native
- Default branch: `main`
- Destination: `external/react-native`

## Steps

1. If `external/react-native` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/react-native.git external/react-native`.
3. Leave the clone untracked. `external/` is gitignored. Never commit secrets.
4. Report the path, branch, and upstream. Read `AGENTS.md` and `CONTRIBUTING.md` first; the framework code lives under `packages/`.

This is the largest repo in Célia's account (~970 MB). Only clone it when the task really needs the React Native source, always with `--depth 1`, and expect several minutes. To inspect a single file, prefer the GitHub API over a full clone.
