---
name: clone-mental-health-app-repo
description: >-
  Shallow-clone Célia's Mental_Health_App fork into
  external/Mental_Health_App. Use when the user asks to clone the mental
  health app or runs /clone-mental-health-app-repo.
disable-model-invocation: true
---

# Clone Mental_Health_App

- Fork: https://github.com/celiadugnoille-arch/Mental_Health_App
- Upstream: https://github.com/Shreyg-27/Mental_Health_App
- Default branch: `main`
- Destination: `external/Mental_Health_App`

A JavaScript mental-health app with a `backend/` and `frontend/` split. It is a student-style project, not a clinical tool — do not treat its content as medical guidance.

## Steps

1. If `external/Mental_Health_App` is already a git checkout, fetch and fast-forward `main`.
2. Otherwise: `git clone --depth 1 --branch main https://github.com/celiadugnoille-arch/Mental_Health_App.git external/Mental_Health_App`.
3. Leave the clone untracked. `external/` is gitignored. Never commit `.env` or database URIs.
4. Report the path, branch, and upstream. Read `README.md`, then `backend/` and `frontend/`.
